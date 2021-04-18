---
description: Informazioni su esempi e allocatori multimediali
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: Informazioni su esempi e allocatori multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9105228e70f82aaa7c36b7e7d28cf7e748e1e2f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320478"
---
# <a name="about-media-samples-and-allocators"></a><span data-ttu-id="52bcf-103">Informazioni su esempi e allocatori multimediali</span><span class="sxs-lookup"><span data-stu-id="52bcf-103">About Media Samples and Allocators</span></span>

<span data-ttu-id="52bcf-104">I filtri distribuiscono i dati tra connessioni pin.</span><span class="sxs-lookup"><span data-stu-id="52bcf-104">Filters deliver data across pin connections.</span></span> <span data-ttu-id="52bcf-105">I dati vengono spostati dal pin di output di un filtro al pin di input di un altro filtro.</span><span class="sxs-lookup"><span data-stu-id="52bcf-105">Data moves from the output pin of one filter to the input pin of another filter.</span></span> <span data-ttu-id="52bcf-106">Il modo più comune per inviare i dati al pin di output consiste nel chiamare il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sull'input, sebbene esistano anche altri meccanismi.</span><span class="sxs-lookup"><span data-stu-id="52bcf-106">The most common way for the output pin to deliver the data is by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the input, although a few other mechanisms exist as well.</span></span>

<span data-ttu-id="52bcf-107">A seconda del filtro, è possibile allocare memoria per i dati multimediali in diversi modi: sull'heap, in una superficie DirectDraw, usando la memoria GDI condivisa o usando un altro meccanismo di allocazione.</span><span class="sxs-lookup"><span data-stu-id="52bcf-107">Depending on the filter, memory for the media data can be allocated in various ways: on the heap, in a DirectDraw surface, using shared GDI memory, or using some other allocation mechanism.</span></span> <span data-ttu-id="52bcf-108">L'oggetto responsabile dell'allocazione della memoria viene definito *allocatore*, ovvero un oggetto com che espone l'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="52bcf-108">The object responsible for allocating the memory is called an *allocator*, which is a COM object that exposes the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="52bcf-109">Quando due pin si connettono, uno dei pin deve fornire un allocatore.</span><span class="sxs-lookup"><span data-stu-id="52bcf-109">When two pins connect, one of the pins must provide an allocator.</span></span> <span data-ttu-id="52bcf-110">DirectShow definisce una sequenza di chiamate al metodo usata per stabilire quale pin fornisce l'allocatore.</span><span class="sxs-lookup"><span data-stu-id="52bcf-110">DirectShow defines a sequence of method calls that is used to establish which pin provides the allocator.</span></span> <span data-ttu-id="52bcf-111">I pin concordano anche sul numero di buffer che l'allocatore creerà e sulle dimensioni dei buffer.</span><span class="sxs-lookup"><span data-stu-id="52bcf-111">The pins also agree on the number of buffers that the allocator will create, and the size of the buffers.</span></span>

<span data-ttu-id="52bcf-112">Prima dell'inizio del flusso, l'allocatore crea un pool di buffer.</span><span class="sxs-lookup"><span data-stu-id="52bcf-112">Before streaming begins, the allocator creates a pool of buffers.</span></span> <span data-ttu-id="52bcf-113">Durante il flusso, il filtro upstream riempie i buffer con i dati e li recapita al filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="52bcf-113">During streaming, the upstream filter fills buffers with data and delivers them to the downstream filter.</span></span> <span data-ttu-id="52bcf-114">Tuttavia, il filtro upstream non assegna ai buffer i puntatori non elaborati del filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="52bcf-114">But the upstream filter does not give the downstream filter raw pointers to the buffers.</span></span> <span data-ttu-id="52bcf-115">USA invece oggetti COM denominati *esempi di supporti*, creati dall'allocatore per gestire i buffer.</span><span class="sxs-lookup"><span data-stu-id="52bcf-115">Instead, it uses COM objects called *media samples*, which the allocator creates to manage the buffers.</span></span> <span data-ttu-id="52bcf-116">Gli esempi di supporti espongono l'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="52bcf-116">Media samples expose the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="52bcf-117">Un esempio multimediale contiene:</span><span class="sxs-lookup"><span data-stu-id="52bcf-117">A media sample contains:</span></span>

-   <span data-ttu-id="52bcf-118">puntatore al buffer sottostante</span><span class="sxs-lookup"><span data-stu-id="52bcf-118">a pointer to the underlying buffer</span></span>
-   <span data-ttu-id="52bcf-119">timestamp</span><span class="sxs-lookup"><span data-stu-id="52bcf-119">a time stamp</span></span>
-   <span data-ttu-id="52bcf-120">diversi flag</span><span class="sxs-lookup"><span data-stu-id="52bcf-120">various flags</span></span>
-   <span data-ttu-id="52bcf-121">Facoltativamente, un tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="52bcf-121">optionally, a media type</span></span>

<span data-ttu-id="52bcf-122">Il timestamp definisce l'ora di presentazione, che il filtro renderer USA per pianificare il rendering.</span><span class="sxs-lookup"><span data-stu-id="52bcf-122">The time stamp defines the presentation time, which the renderer filter uses to schedule rendering.</span></span> <span data-ttu-id="52bcf-123">I flag indicano elementi come se si fosse verificato un break nei dati rispetto all'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="52bcf-123">The flags indicate things like whether there was a break in the data since the previous sample.</span></span> <span data-ttu-id="52bcf-124">Il tipo di supporto fornisce un modo per i filtri per modificare i formati a metà flusso.</span><span class="sxs-lookup"><span data-stu-id="52bcf-124">The media type provides a way for filters to change formats mid-stream.</span></span> <span data-ttu-id="52bcf-125">In genere, l'esempio non dispone di un tipo di supporto, che indica che il formato non è stato modificato rispetto all'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="52bcf-125">Usually, the sample has no media type, which indicates that the format has not changed since the previous sample.</span></span>

<span data-ttu-id="52bcf-126">Mentre un filtro usa un buffer, include il conteggio dei riferimenti nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="52bcf-126">While a filter is using a buffer, it holds reference count on the sample.</span></span> <span data-ttu-id="52bcf-127">L'allocatore utilizza il conteggio dei riferimenti per determinare quando è possibile riutilizzare il buffer.</span><span class="sxs-lookup"><span data-stu-id="52bcf-127">The allocator uses the reference count to determine when it can re-use the buffer.</span></span> <span data-ttu-id="52bcf-128">In questo modo si impedisce a un filtro di sovrascrivere un buffer che è ancora in uso da un altro filtro.</span><span class="sxs-lookup"><span data-stu-id="52bcf-128">This prevents a filter from overwriting a buffer that another filter is still using.</span></span> <span data-ttu-id="52bcf-129">Un esempio non restituisce al pool di allocatori gli esempi disponibili fino a quando non viene rilasciato da ogni filtro.</span><span class="sxs-lookup"><span data-stu-id="52bcf-129">A sample does not return to the allocator's pool of available samples until every filter has released it.</span></span>

<span data-ttu-id="52bcf-130">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="52bcf-130">For more information, see the following topics:</span></span>

-   <span data-ttu-id="52bcf-131">Nell'argomento [esempi e allocatori](samples-and-allocators.md) viene fornita una descrizione più dettagliata del funzionamento degli allocatori.</span><span class="sxs-lookup"><span data-stu-id="52bcf-131">The topic [Samples and Allocators](samples-and-allocators.md) provides a more detailed description of how allocators work.</span></span>
-   <span data-ttu-id="52bcf-132">Il flusso di dati dell'argomento [nel grafico dei filtri](data-flow-in-the-filter-graph.md) fornisce una panoramica generale del flusso di dati in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="52bcf-132">The topic [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md) gives a general overview of data flow in DirectShow.</span></span>

<span data-ttu-id="52bcf-133">Gli argomenti seguenti sono destinati agli sviluppatori che scrivono i propri filtri personalizzati:</span><span class="sxs-lookup"><span data-stu-id="52bcf-133">The following topics are intended for developers who are writing their own custom filters:</span></span>

-   [<span data-ttu-id="52bcf-134">Flusso di dati per sviluppatori di filtri</span><span class="sxs-lookup"><span data-stu-id="52bcf-134">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="52bcf-135">Thread e sezioni critiche</span><span class="sxs-lookup"><span data-stu-id="52bcf-135">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)

## <a name="related-topics"></a><span data-ttu-id="52bcf-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52bcf-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52bcf-137">Il grafico del filtro e i relativi componenti</span><span class="sxs-lookup"><span data-stu-id="52bcf-137">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



