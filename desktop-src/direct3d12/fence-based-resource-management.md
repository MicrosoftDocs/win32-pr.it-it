---
title: Fence-Based Gestione risorse
description: Illustra come gestire l'intervallo di vita dei dati delle risorse tramite il rilevamento dello stato di avanzamento della GPU tramite recinti. La memoria può essere usata di nuovo in modo efficace con i recinti che gestiscono con attenzione la disponibilità di spazio disponibile in memoria, ad esempio in un'implementazione del buffer circolare per un heap Upload memoria.
ms.assetid: A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cbfd9231e3013099c8382072049f1ae1478e28f00830e89fb4ecef1b835ce58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728891"
---
# <a name="fence-based-resource-management"></a>Fence-Based Gestione risorse

Illustra come gestire l'intervallo di vita dei dati delle risorse tramite il rilevamento dello stato di avanzamento della GPU tramite recinti. La memoria può essere usata di nuovo in modo efficace con i recinti che gestiscono con attenzione la disponibilità di spazio disponibile in memoria, ad esempio in un'implementazione del buffer circolare per un heap Upload memoria.

-   [Scenario di buffer circolare](#ring-buffer-scenario)
-   [Esempio di buffer circolare](#ring-buffer-sample)
-   [Argomenti correlati](#related-topics)

## <a name="ring-buffer-scenario"></a>Scenario di buffer circolare

Di seguito è riportato un esempio in cui un'app sperimenta una rara richiesta di caricamento della memoria heap.

Un buffer circolare è un modo per gestire un heap di caricamento. Il buffer circolare contiene i dati necessari per i fotogrammi successivi. L'app gestisce un puntatore di input dei dati corrente e una coda di offset dei frame per registrare ogni frame e l'offset iniziale dei dati delle risorse per tale frame.

Un'app crea un buffer circolare basato su un buffer per caricare i dati nella GPU per ogni frame. Attualmente è stato eseguito il rendering del frame 2, il buffer circolare racchiude i dati per il frame 4, tutti i dati necessari per il frame 5 sono presenti e un buffer costante di grandi dimensioni necessario per il frame 6 deve essere sottoallocato.

**Figura 1:** l'app tenta di sottoallocare per il buffer costante, ma trova memoria disponibile insufficiente.

![Memoria disponibile insufficiente in questo buffer circolare](images/ring-buffer-1.png)

**Figura 2:** tramite il polling di recinto, l'app rileva che è stato eseguito il rendering del frame 3, la coda di offset dei frame viene quindi aggiornata e segue lo stato corrente del buffer circolare. Tuttavia, la memoria disponibile non è ancora sufficientemente grande per contenere il buffer costante.

![Memoria ancora insufficiente dopo il rendering del frame 3](images/ring-buffer-2.png)

**Figura 3:** in base alla situazione, la CPU si blocca (tramite l'attesa di recinto) fino al rendering del frame 4, liberando così la memoria secondaria allocata per il frame 4.

![il frame di rendering 4 libera una maggiore parte del buffer circolare](images/ring-buffer-3.png)

**Figura 4:** la memoria disponibile è sufficientemente grande per il buffer costante e la sottoallocazione ha esito positivo. l'app copia i dati big constant buffer nella memoria usata in precedenza dai dati delle risorse per i fotogrammi 3 e 4. Il puntatore di input corrente viene infine aggiornato.

![ora c'è spazio dal fotogramma 6 nel buffer circolare](images/ring-buffer-4.png)

Se un'app implementa un buffer circolare, il buffer circolare deve essere sufficientemente grande da gestire lo scenario peggiore delle dimensioni dei dati delle risorse.

## <a name="ring-buffer-sample"></a>Esempio di buffer circolare

Il codice di esempio seguente illustra come gestire un buffer circolare, prestando attenzione alla routine di sottoallocazione che gestisce il polling e l'attesa della barriera. Per semplicità, l'esempio usa NOT SUFFICIENT MEMORY per nascondere i dettagli di "memoria disponibile insufficiente trovata nell'heap" perché tale logica (basata su \_ \_ m *\_ pDataCur* e offset all'interno *di FrameOffsetQueue*) non è strettamente correlata ad heap o recinti. L'esempio è semplificato per sacrificare la frequenza dei fotogrammi anziché l'utilizzo della memoria.

Si noti che il supporto del buffer circolare dovrebbe essere uno scenario comune. Tuttavia, la progettazione dell'heap non preclude altri utilizzi, ad esempio la parametrizzazione dell'elenco di comandi e il nuovo uso.

``` syntax
struct FrameResourceOffset
{
    UINT frameIndex;
    UINT8* pResourceOffset;
};
std::queue<FrameResourceOffset> frameOffsetQueue;

void DrawFrame()
{
    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadHeap(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float), 
            4, // Max alignment requirement for vertex data is 4 bytes.
            verticesOffset
            ));

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadHeap(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT,
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model. 
    // Create constant buffer views for the new binding model. 
    // ...

    commandQueue->Execute(commandList);
    commandQueue->AdvanceFence();
}

HRESULT SuballocateFromHeap(SIZE_T uSize, UINT uAlign)
{
    if (NOT_SUFFICIENT_MEMORY(uSize, uAlign))
    {
        // Free up resources for frames processed by GPU; see Figure 2.
        UINT lastCompletedFrame = commandQueue->GetLastCompletedFence();
        FreeUpMemoryUntilFrame( lastCompletedFrame );

        while ( NOT_SUFFICIENT_MEMORY(uSize, uAlign)
            && !frameOffsetQueue.empty() )
        {
            // Block until a new frame is processed by GPU, then free up more memory; see Figure 3.
            UINT nextGPUFrame = frameOffsetQueue.front().frameIndex;
            commandQueue->SetEventOnFenceCompletion(nextGPUFrame, hEvent);
            WaitForSingleObject(hEvent, INFINITE);
            FreeUpMemoryUntilFrame( nextGPUFrame );
        }
    }

    if (NOT_SUFFICIENT_MEMORY(uSize, uAlign))
    {
        // Apps need to create a new Heap that is large enough for this resource.
        return E_HEAPNOTLARGEENOUGH;
    }
    else
    {
        // Update current data pointer for the new resource.
        m_pDataCur = reinterpret_cast<UINT8*>(
            Align(reinterpret_cast<SIZE_T>(m_pHDataCur), uAlign)
            );

        // Update frame offset queue if this is the first resource for a new frame; see Figure 4.
        UINT currentFrame = commandQueue->GetCurrentFence();
        if ( frameOffsetQueue.empty()
            || frameOffsetQueue.back().frameIndex < currentFrame )
        {
            FrameResourceOffset offset = {currentFrame, m_pDataCur};
            frameOffsetQueue.push(offset);
        }

        return S_OK;
    }
}

void FreeUpMemoryUntilFrame(UINT lastCompletedFrame)
{
    while ( !frameOffsetQueue.empty() 
        && frameOffsetQueue.first().frameIndex <= lastCompletedFrame )
    {
        frameOffsetQueue.pop();
    }
}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[Sottoallocazione all'interno dei buffer](large-buffers.md)
</dt> </dl>

 

 




