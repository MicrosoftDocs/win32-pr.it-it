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
# <a name="fence-based-resource-management"></a><span data-ttu-id="bd02e-104">Gestione delle risorse Fence-Based</span><span class="sxs-lookup"><span data-stu-id="bd02e-104">Fence-Based Resource Management</span></span>

<span data-ttu-id="bd02e-105">Viene illustrato come gestire il ciclo di vita dei dati delle risorse tenendo traccia dello stato di avanzamento della GPU tramite le recinzioni.</span><span class="sxs-lookup"><span data-stu-id="bd02e-105">Shows how to manage resource data life-span by tracking GPU progress via fences.</span></span> <span data-ttu-id="bd02e-106">La memoria può essere riutilizzata in modo efficace con le barriere gestendo con attenzione la disponibilità dello spazio disponibile in memoria, ad esempio in un'implementazione del buffer circolare per un heap di caricamento.</span><span class="sxs-lookup"><span data-stu-id="bd02e-106">Memory can be effectively re-used with fences carefully managing the availability of free space in memory, such as in a ring buffer implementation for an Upload heap.</span></span>

-   [<span data-ttu-id="bd02e-107">Scenario di buffer circolare</span><span class="sxs-lookup"><span data-stu-id="bd02e-107">Ring buffer scenario</span></span>](#ring-buffer-scenario)
-   [<span data-ttu-id="bd02e-108">Esempio di buffer circolare</span><span class="sxs-lookup"><span data-stu-id="bd02e-108">Ring buffer sample</span></span>](#ring-buffer-sample)
-   [<span data-ttu-id="bd02e-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd02e-109">Related topics</span></span>](#related-topics)

## <a name="ring-buffer-scenario"></a><span data-ttu-id="bd02e-110">Scenario di buffer circolare</span><span class="sxs-lookup"><span data-stu-id="bd02e-110">Ring buffer scenario</span></span>

<span data-ttu-id="bd02e-111">Di seguito è riportato un esempio in cui un'app riscontra una rara richiesta di caricamento della memoria heap.</span><span class="sxs-lookup"><span data-stu-id="bd02e-111">The following is an example in which an app experiences a rare demand for upload heap memory.</span></span>

<span data-ttu-id="bd02e-112">Un buffer circolare è un modo per gestire un heap di caricamento.</span><span class="sxs-lookup"><span data-stu-id="bd02e-112">A ring buffer is one way to manage an upload heap.</span></span> <span data-ttu-id="bd02e-113">Il buffer circolare include i dati necessari per i successivi frame.</span><span class="sxs-lookup"><span data-stu-id="bd02e-113">The ring buffer holds data required for the next few frames.</span></span> <span data-ttu-id="bd02e-114">L'app gestisce un puntatore di input dei dati corrente e una coda di offset dei frame per registrare ogni frame e l'offset iniziale dei dati delle risorse per quel frame.</span><span class="sxs-lookup"><span data-stu-id="bd02e-114">The app maintains a current data input pointer, and a frame offset queue to record each frame and starting offset of resource data for that frame.</span></span>

<span data-ttu-id="bd02e-115">Un'app crea un buffer circolare basato su un buffer per caricare i dati nella GPU per ogni frame.</span><span class="sxs-lookup"><span data-stu-id="bd02e-115">An app creates a ring-buffer based upon a buffer to upload data to the GPU for each frame.</span></span> <span data-ttu-id="bd02e-116">Al momento del rendering del frame 2, il buffer circolare esegue il wrapping dei dati per il frame 4, tutti i dati necessari per il frame 5 sono presenti e un buffer costante di grandi dimensioni necessario per il frame 6 deve essere Sottoallocato.</span><span class="sxs-lookup"><span data-stu-id="bd02e-116">Currently frame 2 has been rendered, the ring buffer wraps around the data for frame 4, all the data required for frame 5 is present, and a large constant buffer required for frame 6 needs to be sub-allocated.</span></span>

<span data-ttu-id="bd02e-117">**Figura 1** : l'app tenta di eseguire l'allocazione secondaria per il buffer costante, ma trova memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="bd02e-117">**Figure 1** : the app tries to sub-allocate for the constant buffer, but finds insufficient free memory.</span></span>

![memoria disponibile insufficiente in questo buffer circolare](images/ring-buffer-1.png)

<span data-ttu-id="bd02e-119">**Figura 2** : tramite il polling della recinzione, l'app rileva che è stato eseguito il rendering del frame 3, la coda di offset dei frame viene quindi aggiornata e lo stato corrente del buffer circolare segue. Tuttavia, la memoria libera non è ancora sufficientemente grande da contenere il buffer costante.</span><span class="sxs-lookup"><span data-stu-id="bd02e-119">**Figure 2** : through fence polling, the app discovers that frame 3 has been rendered, the frame offset queue is then updated, and the current state of the ring buffer follows - however, free memory is still not large enough to accommodate the constant buffer.</span></span>

![la memoria è ancora insufficiente dopo il rendering del frame 3](images/ring-buffer-2.png)

<span data-ttu-id="bd02e-121">**Figura 3** : data la situazione, la CPU si blocca (attraverso l'attesa di recinzione) fino a quando non viene eseguito il rendering del frame 4, il che libera la memoria allocata per il frame 4.</span><span class="sxs-lookup"><span data-stu-id="bd02e-121">**Figure 3** : given the situation, the CPU blocks itself (via fence waiting) until frame 4 has been rendered, which frees up the memory sub-allocated for frame 4.</span></span>

![il rendering del frame 4 libera più del buffer circolare](images/ring-buffer-3.png)

<span data-ttu-id="bd02e-123">**Figura 4** : ora la memoria disponibile è sufficientemente grande per il buffer costante e l'assegnazione secondaria ha esito positivo; l'app copia i dati del buffer costanti di grandi dimensioni in memoria usata in precedenza dai dati delle risorse per entrambi i frame 3 e 4.</span><span class="sxs-lookup"><span data-stu-id="bd02e-123">**Figure 4** : now free memory is large enough for the constant buffer, and sub-allocation succeeds; the app copies the big constant buffer data to memory previously used by resource data for both frames 3 and 4.</span></span> <span data-ttu-id="bd02e-124">Il puntatore di input corrente viene infine aggiornato.</span><span class="sxs-lookup"><span data-stu-id="bd02e-124">The current input pointer is finally updated.</span></span>

![a questo punto è disponibile spazio nel buffer circolare del frame 6](images/ring-buffer-4.png)

<span data-ttu-id="bd02e-126">Se un'app implementa un buffer circolare, il buffer circolare deve essere sufficientemente grande da far fronte allo scenario peggiore delle dimensioni dei dati delle risorse.</span><span class="sxs-lookup"><span data-stu-id="bd02e-126">If an app implements a ring buffer, the ring buffer must be large enough to cope with the worse-case scenario of the sizes of resource data.</span></span>

## <a name="ring-buffer-sample"></a><span data-ttu-id="bd02e-127">Esempio di buffer circolare</span><span class="sxs-lookup"><span data-stu-id="bd02e-127">Ring buffer sample</span></span>

<span data-ttu-id="bd02e-128">Il codice di esempio seguente mostra come può essere gestito un buffer circolare, prestando attenzione alla routine di sottoallocazione che gestisce il polling della recinzione e l'attesa.</span><span class="sxs-lookup"><span data-stu-id="bd02e-128">The following sample code shows how a ring buffer can be managed, paying attention to the sub-allocation routine that handles fence polling and waiting.</span></span> <span data-ttu-id="bd02e-129">Per semplicità, nell'esempio viene usata una \_ quantità di memoria insufficiente \_ per nascondere i dettagli di "memoria libera non sufficiente trovata nell'heap" poiché tale logica (basata su *m \_ pDataCur* e offset all'interno di *FrameOffsetQueue*) non è strettamente correlata a heap o recinzioni.</span><span class="sxs-lookup"><span data-stu-id="bd02e-129">For simplicity, the sample uses NOT\_SUFFICIENT\_MEMORY to hide the details of “not sufficient free memory found in the heap” since that logic (based on *m\_pDataCur* and offsets inside *FrameOffsetQueue*) is not tightly related to heaps or fences.</span></span> <span data-ttu-id="bd02e-130">L'esempio è semplificato per sacrificare la frequenza dei fotogrammi anziché l'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="bd02e-130">The sample is simplified to sacrifice frame rate instead of memory utilization.</span></span>

<span data-ttu-id="bd02e-131">Si noti che il supporto del buffer circolare dovrebbe essere uno scenario comune; Tuttavia, la progettazione dell'heap non impedisce altro utilizzo, ad esempio la parametrizzazione e il riutilizzo dell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="bd02e-131">Note that, ring-buffer support is expected to be a popular scenario; however, the heap design does not preclude other usage, such as command list parameterization and re-use.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="bd02e-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd02e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd02e-133">**ID3D12Fence**</span><span class="sxs-lookup"><span data-stu-id="bd02e-133">**ID3D12Fence**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[<span data-ttu-id="bd02e-134">Sottoallocazione nei buffer</span><span class="sxs-lookup"><span data-stu-id="bd02e-134">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 




