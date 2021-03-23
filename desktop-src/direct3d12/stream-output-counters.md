---
title: Contatori output flusso
description: L'output del flusso è la capacità della GPU di scrivere i vertici in un buffer. Lo stato del monitoraggio dei contatori di output del flusso.
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d2f3a823f5f4b5d2d5f365235d7e3f8817207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103408"
---
# <a name="stream-output-counters"></a><span data-ttu-id="7d042-104">Contatori output flusso</span><span class="sxs-lookup"><span data-stu-id="7d042-104">Stream Output Counters</span></span>

<span data-ttu-id="7d042-105">L'output del flusso è la capacità della GPU di scrivere i vertici in un buffer.</span><span class="sxs-lookup"><span data-stu-id="7d042-105">Stream output is the ability of the GPU to write vertices to a buffer.</span></span> <span data-ttu-id="7d042-106">Lo stato del monitoraggio dei contatori di output del flusso.</span><span class="sxs-lookup"><span data-stu-id="7d042-106">The stream output counters monitor progress.</span></span>

-   [<span data-ttu-id="7d042-107">Differenze nei contatori dei flussi da Direct3D 11 a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7d042-107">Differences in Stream Counters from Direct3D 11 to Direct3D 12</span></span>](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [<span data-ttu-id="7d042-108">BufferFilledSize</span><span class="sxs-lookup"><span data-stu-id="7d042-108">BufferFilledSize</span></span>](#bufferfilledsize)
-   [<span data-ttu-id="7d042-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d042-109">Related topics</span></span>](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="7d042-110">Differenze nei contatori dei flussi da Direct3D 11 a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7d042-110">Differences in Stream Counters from Direct3D 11 to Direct3D 12</span></span>

<span data-ttu-id="7d042-111">Come parte del processo di output del flusso, la GPU deve conoscerne la posizione corrente nel buffer in cui sta scrivendo.</span><span class="sxs-lookup"><span data-stu-id="7d042-111">As a part of the stream output process, the GPU has to know the current location in the buffer that it is writing to.</span></span> <span data-ttu-id="7d042-112">In Direct3D 11 la memoria per archiviare questo percorso viene allocata dal driver e l'unico modo per le applicazioni di modificare questo valore è tramite il metodo **SOSetTargets** .</span><span class="sxs-lookup"><span data-stu-id="7d042-112">In Direct3D 11, memory to store this location is allocated by the driver and the only way for applications to manipulate this value is via the **SOSetTargets** method.</span></span> <span data-ttu-id="7d042-113">In Direct3D 12, le app allocano memoria per archiviare questo percorso corrente.</span><span class="sxs-lookup"><span data-stu-id="7d042-113">In Direct3D 12, apps allocate memory to store this current location.</span></span> <span data-ttu-id="7d042-114">Non esistono metodi speciali per modificare questo valore e le app possono leggere/scrivere il valore con CPU o GPU.</span><span class="sxs-lookup"><span data-stu-id="7d042-114">There are no special ways to manipulate this value, and apps are free to read/write the value with the CPU or GPU.</span></span>

## <a name="bufferfilledsize"></a><span data-ttu-id="7d042-115">BufferFilledSize</span><span class="sxs-lookup"><span data-stu-id="7d042-115">BufferFilledSize</span></span>

<span data-ttu-id="7d042-116">L'applicazione è responsabile dell'allocazione di spazio di archiviazione per una quantità a 32 bit denominata *BufferFilledSize*.</span><span class="sxs-lookup"><span data-stu-id="7d042-116">The application is responsible for allocating storage for a 32-bit quantity called the *BufferFilledSize*.</span></span> <span data-ttu-id="7d042-117">Contiene il numero di byte di dati nel buffer di output del flusso.</span><span class="sxs-lookup"><span data-stu-id="7d042-117">This contains the number of bytes of data in the stream-output buffer.</span></span> <span data-ttu-id="7d042-118">Questo spazio di archiviazione può essere inserito nello stesso o in una risorsa diversa da quella che contiene i dati di output del flusso.</span><span class="sxs-lookup"><span data-stu-id="7d042-118">This storage can be placed in the same, or a different, resource as the one that contains the stream-output data.</span></span> <span data-ttu-id="7d042-119">Questo valore è accessibile dalla GPU nella fase Stream-output per determinare la posizione in cui aggiungere i nuovi dati dei vertici nel buffer.</span><span class="sxs-lookup"><span data-stu-id="7d042-119">This value is accessed by the GPU in the stream-output stage to determine where to append new vertex data in the buffer.</span></span> <span data-ttu-id="7d042-120">Questo valore è inoltre accessibile dalla GPU per determinare quando si è verificato l'overflow.</span><span class="sxs-lookup"><span data-stu-id="7d042-120">Additionally, this value is accessed by the GPU to determine when overflow has occurred.</span></span>

<span data-ttu-id="7d042-121">Vedere la struttura [**D3D12 \_ Stream \_ output \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).</span><span class="sxs-lookup"><span data-stu-id="7d042-121">Refer to the structure [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).</span></span>

<span data-ttu-id="7d042-122">Il livello di debug convaliderà quanto segue in [**ID3D12GraphicsCommandList:: SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):</span><span class="sxs-lookup"><span data-stu-id="7d042-122">The debug layer will validate the following in [**ID3D12GraphicsCommandList::SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):</span></span>

-   <span data-ttu-id="7d042-123">*BufferFilledSize* rientra nell'intervallo implicito da {*OffsetInBytes*, *sizeInBytes*} se è specificata una risorsa non null.</span><span class="sxs-lookup"><span data-stu-id="7d042-123">*BufferFilledSize* falls in the range implied by {*OffsetInBytes*, *SizeInBytes*}, if a non-NULL resource is specified.</span></span>
-   <span data-ttu-id="7d042-124">*BufferFilledSizeOffsetInBytes* è un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="7d042-124">*BufferFilledSizeOffsetInBytes* is a multiple of 4.</span></span>
-   <span data-ttu-id="7d042-125">*BufferFilledSizeOffsetInBytes* è compreso nell'intervallo della risorsa che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="7d042-125">*BufferFilledSizeOffsetInBytes* is within the range of the containing resource.</span></span>
-   <span data-ttu-id="7d042-126">La risorsa specificata è un buffer.</span><span class="sxs-lookup"><span data-stu-id="7d042-126">The specified resource is a buffer.</span></span>

<span data-ttu-id="7d042-127">Il runtime non convaliderà il tipo di heap associato al buffer di output del flusso, perché l'output del flusso è supportato in tutti i tipi di heap.</span><span class="sxs-lookup"><span data-stu-id="7d042-127">The runtime will not validate the heap type associated with the stream output buffer, as stream output is supported in all heap types.</span></span>

<span data-ttu-id="7d042-128">Le firme radice devono specificare se l'output del flusso verrà usato, usando i flag dei [**\_ \_ \_ flag di firma radice D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) .</span><span class="sxs-lookup"><span data-stu-id="7d042-128">Root signatures must specify if stream output will be used, by using the [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags.</span></span>

<span data-ttu-id="7d042-129">\_ \_ Il flag di firma radice D3D12 consente di \_ \_ \_ \_ specificare l'output del flusso per le firme radice create in HLSL, in modo analogo a come vengono specificati gli altri flag.</span><span class="sxs-lookup"><span data-stu-id="7d042-129">D3D12\_ROOT\_SIGNATURE\_FLAG\_ALLOW\_STREAM\_OUTPUT can be specified for root signatures authored in HLSL, in a manner similar to how the other flags are specified.</span></span>

<span data-ttu-id="7d042-130">[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) avrà esito negativo se il geometry shader contiene l'output del flusso ma la firma radice non ha il flag di \_ firma radice D3D12 \_ \_ \_ Consenti \_ set di flag di output del flusso \_ .</span><span class="sxs-lookup"><span data-stu-id="7d042-130">[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) will fail if the geometry shader contains stream-output but the root signature does not have the D3D12\_ROOT\_SIGNATURE\_FLAG\_ALLOW\_STREAM\_OUTPUT flag set.</span></span>

<span data-ttu-id="7d042-131">Quando una risorsa viene usata come destinazione di output del flusso, le risorse usate devono trovarsi nello \_ stato del flusso di stato della risorsa D3D12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7d042-131">When a resource is used as a stream-output target, the resources used must be in the D3D12\_RESOURCE\_STATE\_STREAM\_OUT state.</span></span> <span data-ttu-id="7d042-132">Questo vale sia per i dati dei vertici sia per i *BufferFilledSize* (che possono trovarsi nelle stesse risorse o in risorse separate).</span><span class="sxs-lookup"><span data-stu-id="7d042-132">This applies to both the vertex data and the *BufferFilledSize* (which can be in the same or separate resources).</span></span>

<span data-ttu-id="7d042-133">Non sono disponibili API speciali per impostare gli offset del buffer di output del flusso perché le applicazioni possono scrivere direttamente nella *BufferFilledSize* con la CPU o la GPU.</span><span class="sxs-lookup"><span data-stu-id="7d042-133">There are no special APIs to set stream-output buffer offsets because applications can write to the *BufferFilledSize* with the CPU or GPU directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d042-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d042-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d042-135">Contatori e query</span><span class="sxs-lookup"><span data-stu-id="7d042-135">Counters and Queries</span></span>](counters-and-queries.md)
</dt> </dl>

 

 




