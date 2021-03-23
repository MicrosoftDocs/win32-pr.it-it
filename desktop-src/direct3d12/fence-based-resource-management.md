---
title: Gestione delle risorse Fence-Based
description: Viene illustrato come gestire il ciclo di vita dei dati delle risorse tenendo traccia dello stato di avanzamento della GPU tramite le recinzioni. La memoria può essere riutilizzata in modo efficace con le barriere gestendo con attenzione la disponibilità dello spazio disponibile in memoria, ad esempio in un'implementazione del buffer circolare per un heap di caricamento.
ms.assetid: A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aba8afd66f8a50a54b699c6a314ba148ebcef023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104842"
---
# <a name="fence-based-resource-management"></a>Gestione delle risorse Fence-Based

Viene illustrato come gestire il ciclo di vita dei dati delle risorse tenendo traccia dello stato di avanzamento della GPU tramite le recinzioni. La memoria può essere riutilizzata in modo efficace con le barriere gestendo con attenzione la disponibilità dello spazio disponibile in memoria, ad esempio in un'implementazione del buffer circolare per un heap di caricamento.

-   [Scenario di buffer circolare](#ring-buffer-scenario)
-   [Esempio di buffer circolare](#ring-buffer-sample)
-   [Argomenti correlati](#related-topics)

## <a name="ring-buffer-scenario"></a>Scenario di buffer circolare

Di seguito è riportato un esempio in cui un'app riscontra una rara richiesta di caricamento della memoria heap.

Un buffer circolare è un modo per gestire un heap di caricamento. Il buffer circolare include i dati necessari per i successivi frame. L'app gestisce un puntatore di input dei dati corrente e una coda di offset dei frame per registrare ogni frame e l'offset iniziale dei dati delle risorse per quel frame.

Un'app crea un buffer circolare basato su un buffer per caricare i dati nella GPU per ogni frame. Al momento del rendering del frame 2, il buffer circolare esegue il wrapping dei dati per il frame 4, tutti i dati necessari per il frame 5 sono presenti e un buffer costante di grandi dimensioni necessario per il frame 6 deve essere Sottoallocato.

**Figura 1** : l'app tenta di eseguire l'allocazione secondaria per il buffer costante, ma trova memoria insufficiente.

![memoria disponibile insufficiente in questo buffer circolare](images/ring-buffer-1.png)

**Figura 2** : tramite il polling della recinzione, l'app rileva che è stato eseguito il rendering del frame 3, la coda di offset dei frame viene quindi aggiornata e lo stato corrente del buffer circolare segue. Tuttavia, la memoria libera non è ancora sufficientemente grande da contenere il buffer costante.

![la memoria è ancora insufficiente dopo il rendering del frame 3](images/ring-buffer-2.png)

**Figura 3** : data la situazione, la CPU si blocca (attraverso l'attesa di recinzione) fino a quando non viene eseguito il rendering del frame 4, il che libera la memoria allocata per il frame 4.

![il rendering del frame 4 libera più del buffer circolare](images/ring-buffer-3.png)

**Figura 4** : ora la memoria disponibile è sufficientemente grande per il buffer costante e l'assegnazione secondaria ha esito positivo; l'app copia i dati del buffer costanti di grandi dimensioni in memoria usata in precedenza dai dati delle risorse per entrambi i frame 3 e 4. Il puntatore di input corrente viene infine aggiornato.

![a questo punto è disponibile spazio nel buffer circolare del frame 6](images/ring-buffer-4.png)

Se un'app implementa un buffer circolare, il buffer circolare deve essere sufficientemente grande da far fronte allo scenario peggiore delle dimensioni dei dati delle risorse.

## <a name="ring-buffer-sample"></a>Esempio di buffer circolare

Il codice di esempio seguente mostra come può essere gestito un buffer circolare, prestando attenzione alla routine di sottoallocazione che gestisce il polling della recinzione e l'attesa. Per semplicità, nell'esempio viene usata una \_ quantità di memoria insufficiente \_ per nascondere i dettagli di "memoria libera non sufficiente trovata nell'heap" poiché tale logica (basata su *m \_ pDataCur* e offset all'interno di *FrameOffsetQueue*) non è strettamente correlata a heap o recinzioni. L'esempio è semplificato per sacrificare la frequenza dei fotogrammi anziché l'utilizzo della memoria.

Si noti che il supporto del buffer circolare dovrebbe essere uno scenario comune; Tuttavia, la progettazione dell'heap non impedisce altro utilizzo, ad esempio la parametrizzazione e il riutilizzo dell'elenco dei comandi.

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

[Sottoallocazione nei buffer](large-buffers.md)
</dt> </dl>

 

 




