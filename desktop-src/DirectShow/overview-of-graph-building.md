---
description: Panoramica della creazione di grafici
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Panoramica della creazione di grafici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69ef9ea0f4f9e21d33372ad2a37a59b512d5dcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124365"
---
# <a name="overview-of-graph-building"></a><span data-ttu-id="ae2a2-103">Panoramica della creazione di grafici</span><span class="sxs-lookup"><span data-stu-id="ae2a2-103">Overview of Graph Building</span></span>

<span data-ttu-id="ae2a2-104">Per creare un grafico di filtro, iniziare creando un'istanza di Filter Graph Manager:</span><span class="sxs-lookup"><span data-stu-id="ae2a2-104">To create a filter graph, begin by creating an instance of the Filter Graph Manager:</span></span>


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



<span data-ttu-id="ae2a2-105">Filter Graph Manager supporta i seguenti metodi di creazione di grafici:</span><span class="sxs-lookup"><span data-stu-id="ae2a2-105">The Filter Graph Manager supports the following graph-building methods:</span></span>

-   <span data-ttu-id="ae2a2-106">[**IFilterGraph:: ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) tenta di effettuare una connessione diretta tra due pin.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-106">[**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) tries to make a direct connection between two pins.</span></span> <span data-ttu-id="ae2a2-107">Se i pin non possono connettersi, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-107">If the pins cannot connect, the method fails.</span></span>
-   <span data-ttu-id="ae2a2-108">[**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connette due pin.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-108">[**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connects two pins.</span></span> <span data-ttu-id="ae2a2-109">Se possibile, esegue una connessione diretta.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-109">If possible, it makes a direct connection.</span></span> <span data-ttu-id="ae2a2-110">In caso contrario, vengono utilizzati filtri intermedi per completare la connessione.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-110">Otherwise, it uses intermediate filters to complete the connection.</span></span>
-   <span data-ttu-id="ae2a2-111">[**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) inizia da un pin di output e compila il resto del grafo.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-111">[**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) starts from an output pin and builds the rest of the graph.</span></span> <span data-ttu-id="ae2a2-112">Questo metodo aggiunge i filtri in base alle esigenze, lavorando a valle, fino a raggiungere un filtro renderer.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-112">This methods adds filters as needed, working downstream, until it reaches a renderer filter.</span></span>
-   <span data-ttu-id="ae2a2-113">[**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) compila un grafo completo per la riproduzione di file.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-113">[**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) builds a complete file-playback graph.</span></span>
-   <span data-ttu-id="ae2a2-114">[**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) aggiunge un filtro al grafico.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-114">[**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) adds a filter to the graph.</span></span> <span data-ttu-id="ae2a2-115">Il filtro non viene connesso.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-115">It does not connect the filter.</span></span> <span data-ttu-id="ae2a2-116">È necessario creare il filtro prima di chiamare questo metodo, chiamando **CoCreateInstance** o utilizzando il mapper del filtro o l'enumeratore di dispositivi di sistema.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-116">You must create the filter before calling this method, either by calling **CoCreateInstance** or by using the Filter Mapper or System Device Enumerator.</span></span>

<span data-ttu-id="ae2a2-117">Questi metodi forniscono tre approcci di base per la compilazione del grafo:</span><span class="sxs-lookup"><span data-stu-id="ae2a2-117">These methods provide three basic approaches to building the graph:</span></span>

1.  <span data-ttu-id="ae2a2-118">Filter Graph Manager compila l'intero grafico.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-118">The Filter Graph Manager builds the entire graph.</span></span>
2.  <span data-ttu-id="ae2a2-119">Il gestore del grafico del filtro compila parte del grafico.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-119">The Filter Graph Manager builds part of the graph.</span></span>
3.  <span data-ttu-id="ae2a2-120">L'applicazione compila l'intero grafico.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-120">The application builds the entire graph.</span></span>

<span data-ttu-id="ae2a2-121">**Filter Graph Manager compila l'intero grafico**</span><span class="sxs-lookup"><span data-stu-id="ae2a2-121">**The Filter Graph Manager Builds the Entire Graph**</span></span>

<span data-ttu-id="ae2a2-122">Se si vuole semplicemente riprodurre un file creato in un formato riconosciuto, ad esempio AVI, MPEG, WAV o MP3, usare il metodo **RenderFile** .</span><span class="sxs-lookup"><span data-stu-id="ae2a2-122">If you simply want to play a file that is authored in a recognized format, such as AVI, MPEG, WAV, or MP3, use the **RenderFile** method.</span></span> <span data-ttu-id="ae2a2-123">Questo articolo [illustra come eseguire](how-to-play-a-file.md) questa operazione.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-123">The article [How To Play a File](how-to-play-a-file.md) shows how to do this.</span></span>

<span data-ttu-id="ae2a2-124">Il metodo **RenderFile** inizia con la ricerca nel registro di sistema di un filtro di origine in grado di analizzare il file.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-124">The **RenderFile** method starts by looking in the registry for a source filter that can parse the file.</span></span> <span data-ttu-id="ae2a2-125">Usa il protocollo (ad esempio " `https://` " nell'URL), l'estensione di file o i modelli di byte predefiniti nel file per determinare il filtro di origine.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-125">It uses the protocol (such as " `https://` " in the URL), the file extension, or pre-defined byte patterns in the file to determine the source filter.</span></span> <span data-ttu-id="ae2a2-126">Per informazioni dettagliate, vedere la pagina relativa alla [registrazione di un tipo di file personalizzato](registering-a-custom-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="ae2a2-126">For details, see [Registering a Custom File Type](registering-a-custom-file-type.md).</span></span>

<span data-ttu-id="ae2a2-127">Per creare il resto del grafo, il gestore del grafico di filtro usa un processo iterativo in cui accetta i tipi di supporto supportati da un filtro sui pin di output e Cerca nel registro di sistema i filtri che accettano tale tipo di supporto come input.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-127">To build the rest of the graph, the Filter Graph Manager uses an iterative process wherein it takes the media types that a filter supports on its output pins, and searches the registry for filters that will accept that media type as input.</span></span> <span data-ttu-id="ae2a2-128">USA diversi criteri per limitare la ricerca e assegnare priorità ai filtri:</span><span class="sxs-lookup"><span data-stu-id="ae2a2-128">It uses several criteria to narrow the search and prioritize filters:</span></span>

-   <span data-ttu-id="ae2a2-129">La *categoria Filter* identifica la funzionalità generale del filtro.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-129">The *filter category* identifies the general functionality of the filter.</span></span>
-   <span data-ttu-id="ae2a2-130">Il tipo di supporto descrive il tipo di dati che il filtro può accettare come input o recapitare come output.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-130">The media type describes what kind of data the filter can accept as input or deliver as output.</span></span>
-   <span data-ttu-id="ae2a2-131">Il *merito* determina l'ordine in cui vengono tentati i filtri.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-131">The *merit* determines the order in which filters are tried.</span></span> <span data-ttu-id="ae2a2-132">Se due filtri nella stessa categoria di filtro supportano entrambi gli stessi tipi di input, il gestore del grafico di filtro seleziona quello con il valore di Merit massimo.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-132">If two filters in the same filter category both support the same input types, the Filter Graph Manager selects the one with the highest merit value.</span></span> <span data-ttu-id="ae2a2-133">Ai filtri viene assegnato intenzionalmente un valore di Merit basso perché sono progettati per finalità specializzate e devono essere aggiunti al grafico solo dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-133">Some filters are purposely given a low merit value because they are designed for specialized purposes and should only be added to the graph by the application.</span></span>

<span data-ttu-id="ae2a2-134">Filter Graph Manager usa l'oggetto [Filter Mapper](filter-mapper.md) per eseguire ricerche nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-134">The Filter Graph Manager uses the [Filter Mapper](filter-mapper.md) object to search the registry.</span></span>

<span data-ttu-id="ae2a2-135">Quando ogni filtro viene aggiunto, il gestore del grafico del filtro tenta di connetterlo al pin di output del filtro precedente.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-135">As each filter is added, the Filter Graph Manager tries to connect it to the previous filter's output pin.</span></span> <span data-ttu-id="ae2a2-136">I filtri negoziano per determinare se possono connettersi e, in tal caso, quale tipo di supporto utilizzare per la connessione.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-136">The filters negotiate to determine whether they can connect, and if so, what media type to use for the connection.</span></span> <span data-ttu-id="ae2a2-137">Se il nuovo filtro non è in grado di connettersi, il gestore del grafico del filtro lo ignora e tenta un altro filtro.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-137">If the new filter cannot connect, the Filter Graph Manager discards it and tries another filter.</span></span> <span data-ttu-id="ae2a2-138">Questo processo continua fino a quando non viene eseguito il rendering di ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-138">This process continues until every stream is rendered.</span></span>

<span data-ttu-id="ae2a2-139">**Filter Graph Manager compila parte del grafico**</span><span class="sxs-lookup"><span data-stu-id="ae2a2-139">**The Filter Graph Manager Builds Part of the Graph**</span></span>

<span data-ttu-id="ae2a2-140">Per eseguire un'operazione oltre a riprodurre semplicemente un file, l'applicazione deve eseguire almeno alcune delle operazioni di compilazione del grafo.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-140">To do something beyond simply playing a file, your application must perform at least some of the graph building work.</span></span> <span data-ttu-id="ae2a2-141">Ad esempio, un'applicazione di acquisizione video deve selezionare un filtro origine di acquisizione e aggiungerlo al grafico.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-141">For example, a video capture application must select a capture source filter and add it to the graph.</span></span> <span data-ttu-id="ae2a2-142">Se si scrivono dati in un file AVI, è necessario aggiungere al grafico i filtri mux e writer di file AVI.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-142">If you are writing data to an AVI file, you must add the AVI Mux and File Writer filters to the graph.</span></span> <span data-ttu-id="ae2a2-143">Tuttavia, spesso è possibile consentire a Filter Graph Manager di completare il grafo.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-143">However, it is often possible to let the Filter Graph Manager complete the graph.</span></span> <span data-ttu-id="ae2a2-144">È ad esempio possibile eseguire il rendering di un PIN per l'anteprima chiamando il metodo **Render** .</span><span class="sxs-lookup"><span data-stu-id="ae2a2-144">For example, you can render a pin for preview by calling the **Render** method.</span></span>

<span data-ttu-id="ae2a2-145">**L'applicazione compila l'intero grafico**</span><span class="sxs-lookup"><span data-stu-id="ae2a2-145">**The Application Builds the Entire Graph**</span></span>

<span data-ttu-id="ae2a2-146">In alcuni scenari, è possibile che l'applicazione debba compilare il grafico aggiungendo e connettendo ogni filtro.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-146">In some scenarios, your application may need to build the graph by adding and connecting each filter.</span></span> <span data-ttu-id="ae2a2-147">In questo caso, è probabile che si conoscano in particolare i filtri da aggiungere al grafico.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-147">In this case, you probably know specifically which filters should be added to the graph.</span></span> <span data-ttu-id="ae2a2-148">Con questo approccio, l'applicazione aggiunge ogni filtro chiamando **addFilter**, enumera i pin sui filtri e li connette chiamando **Connect** o **ConnectDirect**.</span><span class="sxs-lookup"><span data-stu-id="ae2a2-148">With this approach, the application adds each filter by calling **AddFilter**, enumerates the pins on the filters, and connects them by calling either **Connect** or **ConnectDirect**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae2a2-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ae2a2-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae2a2-150">Creazione di grafici con il generatore di grafici di acquisizione</span><span class="sxs-lookup"><span data-stu-id="ae2a2-150">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[<span data-ttu-id="ae2a2-151">Enumerazione dei dispositivi e dei filtri</span><span class="sxs-lookup"><span data-stu-id="ae2a2-151">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="ae2a2-152">Enumerazione di oggetti in un grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="ae2a2-152">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="ae2a2-153">Tecniche di Graph-Building generali</span><span class="sxs-lookup"><span data-stu-id="ae2a2-153">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="ae2a2-154">Creazione del grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="ae2a2-154">Building the Filter Graph</span></span>](building-the-filter-graph.md)
</dt> </dl>

 

 



