---
description: Thread e sezioni critiche
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Thread e sezioni critiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576cb28e7e382db92328adf09980a825e71b5a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350336"
---
# <a name="threads-and-critical-sections"></a><span data-ttu-id="4ef3c-103">Thread e sezioni critiche</span><span class="sxs-lookup"><span data-stu-id="4ef3c-103">Threads and Critical Sections</span></span>

<span data-ttu-id="4ef3c-104">Questa sezione descrive il threading nei filtri DirectShow e i passaggi da eseguire per evitare arresti anomali o deadlock in un filtro personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4ef3c-104">This section describes threading in DirectShow filters, and the steps you should take to avoid crashes or deadlocks in a custom filter.</span></span>

<span data-ttu-id="4ef3c-105">Negli esempi di questa sezione viene usato pseudocodice per illustrare il codice che è necessario scrivere.</span><span class="sxs-lookup"><span data-stu-id="4ef3c-105">The examples in this section use pseudocode to illustrate the code you will need to write.</span></span> <span data-ttu-id="4ef3c-106">Si presuppone che un filtro personalizzato usi classi derivate dalle classi base di DirectShow, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="4ef3c-106">They assume that a custom filter is using classes derived from the DirectShow base classes, as follows:</span></span>

-   <span data-ttu-id="4ef3c-107">CMyInputPin: derivato da [**CBaseInputPin**](cbaseinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="4ef3c-107">CMyInputPin: Derived from [**CBaseInputPin**](cbaseinputpin.md).</span></span>
-   <span data-ttu-id="4ef3c-108">CMyOutputPin: derivato da [**CBaseOutputPin**](cbaseoutputpin.md).</span><span class="sxs-lookup"><span data-stu-id="4ef3c-108">CMyOutputPin: Derived from [**CBaseOutputPin**](cbaseoutputpin.md).</span></span>
-   <span data-ttu-id="4ef3c-109">CMyFilter: derivato da [**CBaseFilter**](cbasefilter.md).</span><span class="sxs-lookup"><span data-stu-id="4ef3c-109">CMyFilter: Derived from [**CBaseFilter**](cbasefilter.md).</span></span>
-   <span data-ttu-id="4ef3c-110">CMyInputAllocator: allocatore del PIN di input, derivato da [**CMemAllocator**](cmemallocator.md).</span><span class="sxs-lookup"><span data-stu-id="4ef3c-110">CMyInputAllocator: The input pin's allocator, derived from [**CMemAllocator**](cmemallocator.md).</span></span> <span data-ttu-id="4ef3c-111">Non tutti i filtri necessitano di un allocatore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4ef3c-111">Not every filter needs a custom allocator.</span></span> <span data-ttu-id="4ef3c-112">Per molti filtri, la classe **CMemAllocator** è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="4ef3c-112">For many filters, the **CMemAllocator** class is sufficient.</span></span>

<span data-ttu-id="4ef3c-113">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="4ef3c-113">This section contains the following topics.</span></span>

-   [<span data-ttu-id="4ef3c-114">Il flusso e i thread dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="4ef3c-114">The Streaming and Application Threads</span></span>](the-streaming-and-application-threads.md)
-   [<span data-ttu-id="4ef3c-115">Sospensione in corso</span><span class="sxs-lookup"><span data-stu-id="4ef3c-115">Pausing</span></span>](pausing.md)
-   [<span data-ttu-id="4ef3c-116">Ricezione e distribuzione di esempi</span><span class="sxs-lookup"><span data-stu-id="4ef3c-116">Receiving and Delivering Samples</span></span>](receiving-and-delivering-samples.md)
-   [<span data-ttu-id="4ef3c-117">Distribuzione della fine del flusso</span><span class="sxs-lookup"><span data-stu-id="4ef3c-117">Delivering the End of Stream</span></span>](delivering-the-end-of-stream.md)
-   [<span data-ttu-id="4ef3c-118">Scaricamento dei dati</span><span class="sxs-lookup"><span data-stu-id="4ef3c-118">Flushing Data</span></span>](flushing-data.md)
-   [<span data-ttu-id="4ef3c-119">Stopping</span><span class="sxs-lookup"><span data-stu-id="4ef3c-119">Stopping</span></span>](stopping.md)
-   [<span data-ttu-id="4ef3c-120">Recupero di buffer</span><span class="sxs-lookup"><span data-stu-id="4ef3c-120">Getting Buffers</span></span>](getting-buffers.md)
-   [<span data-ttu-id="4ef3c-121">Thread di streaming e gestione del grafo dei filtri</span><span class="sxs-lookup"><span data-stu-id="4ef3c-121">Streaming Threads and the Filter Graph Manager</span></span>](streaming-threads-and-the-filter-graph-manager.md)
-   [<span data-ttu-id="4ef3c-122">Riepilogo del threading del filtro</span><span class="sxs-lookup"><span data-stu-id="4ef3c-122">Summary of Filter Threading</span></span>](summary-of-filter-threading.md)

## <a name="related-topics"></a><span data-ttu-id="4ef3c-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ef3c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ef3c-124">Flusso di dati per sviluppatori di filtri</span><span class="sxs-lookup"><span data-stu-id="4ef3c-124">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> <dt>

[<span data-ttu-id="4ef3c-125">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="4ef3c-125">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



