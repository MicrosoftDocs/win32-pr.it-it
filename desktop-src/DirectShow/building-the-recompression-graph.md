---
description: Creazione del grafico di ricompressione
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: Creazione del grafico di ricompressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8ea604bead34c22c123bbabe5d88e985006a9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876082"
---
# <a name="building-the-recompression-graph"></a><span data-ttu-id="a8168-103">Creazione del grafico di ricompressione</span><span class="sxs-lookup"><span data-stu-id="a8168-103">Building the Recompression Graph</span></span>

<span data-ttu-id="a8168-104">Un tipico grafico di filtro per la ricompressione dei file AVI è simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="a8168-104">A typical filter graph for AVI file recompression looks like the following:</span></span>

![grafico di ricompressione AVI](images/avi2avi4.png)

<span data-ttu-id="a8168-106">Il [filtro Splitter AVI](avi-splitter-filter.md) estrae i dati dal [filtro di origine file (Async)](file-source--async--filter.md) e li analizza in flussi video e audio.</span><span class="sxs-lookup"><span data-stu-id="a8168-106">The [AVI Splitter Filter](avi-splitter-filter.md) pulls data from the [File Source (Async) Filter](file-source--async--filter.md) and parses it into video and audio streams.</span></span> <span data-ttu-id="a8168-107">Il video decompressore decodifica il video compresso, dove viene ricompresso dal compressore video.</span><span class="sxs-lookup"><span data-stu-id="a8168-107">The video decompressor decodes the compressed video, where it is recompressed by the video compressor.</span></span> <span data-ttu-id="a8168-108">La scelta dei decompressori dipende dal file di origine. verrà gestito automaticamente da [Intelligent Connect](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="a8168-108">The choice of decompressors depends on the source file; it will be handled automatically by [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="a8168-109">L'applicazione deve scegliere il compressore, in genere presentando un elenco all'utente.</span><span class="sxs-lookup"><span data-stu-id="a8168-109">The application must choose the compressor, typically by presenting a list to the user.</span></span> <span data-ttu-id="a8168-110">(Vedere [scelta di un filtro di compressione](choosing-a-compression-filter.md)).</span><span class="sxs-lookup"><span data-stu-id="a8168-110">(See [Choosing a Compression Filter](choosing-a-compression-filter.md).)</span></span>

<span data-ttu-id="a8168-111">Il video compresso passa quindi al [filtro Mux AVI](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a8168-111">The compressed video then goes to the [AVI Mux Filter](avi-mux-filter.md).</span></span> <span data-ttu-id="a8168-112">Il flusso audio in questo esempio non è compresso, quindi passa direttamente dalla barra di divisione AVI alla Mux AVI.</span><span class="sxs-lookup"><span data-stu-id="a8168-112">The audio stream in this example is not compressed, so it goes directly from the AVI Splitter to the AVI Mux.</span></span> <span data-ttu-id="a8168-113">Il mux AVI interleaves The Two Streams e il [filtro del writer di file](file-writer-filter.md) scrive l'output su disco.</span><span class="sxs-lookup"><span data-stu-id="a8168-113">The AVI Mux interleaves the two streams, and the [File Writer Filter](file-writer-filter.md) writes the output to disk.</span></span> <span data-ttu-id="a8168-114">Si noti che il mux AVI è necessario anche se il file originale non dispone di un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="a8168-114">Note that the AVI Mux is required even if the original file does not have an audio stream.</span></span>

<span data-ttu-id="a8168-115">Il modo più semplice per creare questo grafico di filtro consiste nell'usare il [Generatore di grafici di acquisizione](capture-graph-builder.md), un componente DirectShow per la creazione di grafici di acquisizione e altri grafici di filtri personalizzati.</span><span class="sxs-lookup"><span data-stu-id="a8168-115">The easiest way to build this filter graph is to use the [Capture Graph Builder](capture-graph-builder.md), which is a DirectShow component for building capture graphs and other custom filter graphs.</span></span>

<span data-ttu-id="a8168-116">Per iniziare, chiamare CoCreateInstance per creare il generatore del grafico di acquisizione:</span><span class="sxs-lookup"><span data-stu-id="a8168-116">Start by calling CoCreateInstance to create the Capture Graph Builder:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



<span data-ttu-id="a8168-117">Usare quindi il generatore del grafico di acquisizione per compilare il grafico del filtro:</span><span class="sxs-lookup"><span data-stu-id="a8168-117">Then use the Capture Graph Builder to build the filter graph:</span></span>

1.  <span data-ttu-id="a8168-118">Compilare la sezione rendering del grafo, che include il filtro Mux AVI e il [writer di file](file-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a8168-118">Build the rendering section of the graph, which includes the AVI Mux filter and the [File Writer](file-writer-filter.md).</span></span>
2.  <span data-ttu-id="a8168-119">Aggiungere il filtro di origine e il filtro di compressione al grafico.</span><span class="sxs-lookup"><span data-stu-id="a8168-119">Add the source filter and the compression filter to the graph.</span></span>
3.  <span data-ttu-id="a8168-120">Connettere il filtro di origine al filtro MUX.</span><span class="sxs-lookup"><span data-stu-id="a8168-120">Connect the source filter to the MUX filter.</span></span> <span data-ttu-id="a8168-121">Il generatore di grafici di acquisizione inserisce tutti i filtri splitter e decodificatore necessari per analizzare il file di origine.</span><span class="sxs-lookup"><span data-stu-id="a8168-121">The capture graph builder inserts whatever splitter and decoder filters are needed to parse the source file.</span></span> <span data-ttu-id="a8168-122">Può inoltre instradare i flussi video e audio attraverso i filtri di compressione.</span><span class="sxs-lookup"><span data-stu-id="a8168-122">It can also route the video and audio streams through compression filters.</span></span>

<span data-ttu-id="a8168-123">Le sezioni seguenti illustrano ognuno di questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="a8168-123">The following sections explain each of these steps.</span></span>

<span data-ttu-id="a8168-124">Compilare la sezione rendering</span><span class="sxs-lookup"><span data-stu-id="a8168-124">Build the Rendering Section</span></span>

<span data-ttu-id="a8168-125">Per compilare la sezione rendering del grafo, chiamare il metodo [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) .</span><span class="sxs-lookup"><span data-stu-id="a8168-125">To build the rendering section of the graph, call the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method.</span></span> <span data-ttu-id="a8168-126">Questo metodo accetta parametri di input che specificano il sottotipo di supporto per l'output e il nome del file di output.</span><span class="sxs-lookup"><span data-stu-id="a8168-126">This method takes input parameters that specify the media subtype for the output and the name of the output file.</span></span> <span data-ttu-id="a8168-127">Restituisce i puntatori al filtro MUX e al writer di file.</span><span class="sxs-lookup"><span data-stu-id="a8168-127">It returns pointers to the MUX filter and the file writer.</span></span> <span data-ttu-id="a8168-128">Il filtro MUX è necessario per la fase successiva della creazione di grafici.</span><span class="sxs-lookup"><span data-stu-id="a8168-128">The MUX filter is needed for the next stage of graph building.</span></span> <span data-ttu-id="a8168-129">Il puntatore al writer di file non è necessario per questo esempio, in modo che il parametro possa essere **null**:</span><span class="sxs-lookup"><span data-stu-id="a8168-129">The pointer to the file writer is not needed for this example, so that parameter can be **NULL**:</span></span>


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



<span data-ttu-id="a8168-130">Quando il metodo restituisce, il filtro MUX ha un conteggio dei riferimenti in attesa, quindi assicurarsi di rilasciare il puntatore in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="a8168-130">When the method returns, the MUX filter has an outstanding reference count, so be sure to release the pointer later.</span></span>

<span data-ttu-id="a8168-131">Il diagramma seguente mostra il grafico di filtro in questo punto.</span><span class="sxs-lookup"><span data-stu-id="a8168-131">The following diagram shows the filter graph at this point.</span></span>

![sezione rendering del grafico del filtro](images/avi2avi1.png)

<span data-ttu-id="a8168-133">Il filtro MUX espone due interfacce per il controllo del formato AVI:</span><span class="sxs-lookup"><span data-stu-id="a8168-133">The MUX filter exposes two interfaces for controlling the AVI format:</span></span>

-   <span data-ttu-id="a8168-134">[**Interfaccia IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): imposta la modalità di interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="a8168-134">[**IConfigInterleaving Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): Sets the interleaving mode.</span></span>
-   <span data-ttu-id="a8168-135">[**Interfaccia IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): imposta il flusso master e l'indice di compatibilità AVI.</span><span class="sxs-lookup"><span data-stu-id="a8168-135">[**IConfigAviMux Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): Sets the master stream and the AVI compatibility index.</span></span>

<span data-ttu-id="a8168-136">Aggiungere i filtri di origine e compressione</span><span class="sxs-lookup"><span data-stu-id="a8168-136">Add the Source and Compression Filters</span></span>

<span data-ttu-id="a8168-137">Il passaggio successivo consiste nell'aggiungere i filtri di origine e compressione al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="a8168-137">The next step is to add the source and compression filters to the filter graph.</span></span> <span data-ttu-id="a8168-138">Il generatore di grafici di acquisizione crea automaticamente un'istanza del gestore del grafico dei filtri quando si chiama SetOutputFileName.</span><span class="sxs-lookup"><span data-stu-id="a8168-138">The Capture Graph Builder automatically creates an instance of the Filter Graph Manager when you call SetOutputFileName.</span></span> <span data-ttu-id="a8168-139">Ottenere un puntatore a esso chiamando il metodo [**ICaptureGraphBuilder2:: GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) :</span><span class="sxs-lookup"><span data-stu-id="a8168-139">Get a pointer to it by calling the [**ICaptureGraphBuilder2::GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) method:</span></span>


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



<span data-ttu-id="a8168-140">A questo punto chiamare il metodo [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) per aggiungere il filtro di origine del file asincrono e il metodo [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il compressore video:</span><span class="sxs-lookup"><span data-stu-id="a8168-140">Now call the [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) method to add the Async File Source filter, and the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method to add the video compressor:</span></span>


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



<span data-ttu-id="a8168-141">A questo punto, il filtro di origine e il filtro di compressione non sono connessi ad altri elementi nel grafico, come illustrato nella figura seguente:</span><span class="sxs-lookup"><span data-stu-id="a8168-141">At this point, the source filter and the compression filter are not connected to anything else in the graph, as shown in the following illustration:</span></span>

![filtrare il grafico con filtri di origine e compressione](images/avi2avi2.png)

<span data-ttu-id="a8168-143">Connettere l'origine a Mux</span><span class="sxs-lookup"><span data-stu-id="a8168-143">Connect the Source to the Mux</span></span>

<span data-ttu-id="a8168-144">Il passaggio finale consiste nel connettere il filtro di origine al filtro Mux AVI, tramite il compressore video.</span><span class="sxs-lookup"><span data-stu-id="a8168-144">The final step is to connect the source filter to the AVI Mux filter, through the video compressor.</span></span> <span data-ttu-id="a8168-145">Usare il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , che connette un pin di output sul filtro di origine a un filtro di sink specificato, facoltativamente tramite un filtro di compressione.</span><span class="sxs-lookup"><span data-stu-id="a8168-145">Use the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method, which connects an output pin on the source filter to a specified sink filter, optionally through a compression filter.</span></span>

<span data-ttu-id="a8168-146">I primi due parametri specificano quale dei pin del filtro di origine connettersi, designando una categoria pin e un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="a8168-146">The first two parameters specify which of the source filter's pins to connect, by designating a pin category and a media type.</span></span> <span data-ttu-id="a8168-147">Il filtro di origine del file asincrono ha un solo pin di output, quindi questi parametri devono essere **null**.</span><span class="sxs-lookup"><span data-stu-id="a8168-147">The Async File Source filter has only one output pin, so these parameters should be **NULL**.</span></span> <span data-ttu-id="a8168-148">I tre parametri successivi specificano il filtro di origine, il filtro di compressione (se presente) e il filtro MUX.</span><span class="sxs-lookup"><span data-stu-id="a8168-148">The next three parameters specify the source filter, the compression filter (if any), and the Mux filter.</span></span>

<span data-ttu-id="a8168-149">Nell'esempio di codice seguente viene eseguito il rendering del flusso video attraverso il compressore video:</span><span class="sxs-lookup"><span data-stu-id="a8168-149">The following code example renders the video stream through the video compressor:</span></span>


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



<span data-ttu-id="a8168-150">Il diagramma seguente mostra il grafico di filtro fino a questo punto.</span><span class="sxs-lookup"><span data-stu-id="a8168-150">The following diagram shows the filter graph so far.</span></span>

![flusso video sottoposto a rendering](images/avi2avi3.png)

<span data-ttu-id="a8168-152">Supponendo che il file di origine disponga di un flusso audio, il filtro [splitter AVI](avi-splitter-filter.md) ha creato un pin di output per l'audio.</span><span class="sxs-lookup"><span data-stu-id="a8168-152">Assuming that the source file has an audio stream, the [AVI Splitter](avi-splitter-filter.md) filter has created an output pin for the audio.</span></span> <span data-ttu-id="a8168-153">Per connettere questo pin, chiamare di nuovo RenderStream:</span><span class="sxs-lookup"><span data-stu-id="a8168-153">To connect this pin, call RenderStream again:</span></span>


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



<span data-ttu-id="a8168-154">In questo caso non viene specificato alcun filtro di compressione.</span><span class="sxs-lookup"><span data-stu-id="a8168-154">Here, no compression filter is specified.</span></span> <span data-ttu-id="a8168-155">Il pin di output del filtro di origine è già connesso, quindi il metodo RenderStream Cerca un pin di output non connesso nel filtro della barra di divisione.</span><span class="sxs-lookup"><span data-stu-id="a8168-155">The source filter's output pin is already connected, so the RenderStream method searches for an unconnected output pin on the splitter filter.</span></span> <span data-ttu-id="a8168-156">Trova il pin audio e lo connette direttamente al filtro MUX.</span><span class="sxs-lookup"><span data-stu-id="a8168-156">It finds the audio pin and connects it directly to the MUX filter.</span></span> <span data-ttu-id="a8168-157">Se il file di origine non dispone di un flusso audio, la seconda chiamata a RenderStream avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a8168-157">If the source file does not have an audio stream, the second call to RenderStream will fail.</span></span> <span data-ttu-id="a8168-158">Si tratta di un comportamento previsto.</span><span class="sxs-lookup"><span data-stu-id="a8168-158">This is expected behavior.</span></span> <span data-ttu-id="a8168-159">Il grafo viene completato dopo la prima chiamata a RenderStream, quindi l'errore nella seconda chiamata è innocuo.</span><span class="sxs-lookup"><span data-stu-id="a8168-159">The graph is complete after the first call to RenderStream, so the failure in the second call is harmless.</span></span>

<span data-ttu-id="a8168-160">In questo esempio, l'ordine delle due chiamate RenderStream è importante.</span><span class="sxs-lookup"><span data-stu-id="a8168-160">In this example, the order of the two RenderStream calls is important.</span></span> <span data-ttu-id="a8168-161">Poiché la seconda chiamata non specifica un compressore, verrà connesso qualsiasi PIN non connesso dal separatore AVI.</span><span class="sxs-lookup"><span data-stu-id="a8168-161">Because the second call does not specify a compressor, it will connect any unconnected pin from the AVI Splitter.</span></span> <span data-ttu-id="a8168-162">Se si effettua questa chiamata prima dell'altra, è possibile connettere il flusso video al Mux di AVI, senza compressore video.</span><span class="sxs-lookup"><span data-stu-id="a8168-162">If you make this call before the other one, it might connect the video stream to the AVI Mux, without your video compressor.</span></span> <span data-ttu-id="a8168-163">Pertanto, la chiamata più specifica (con il filtro di compressione) deve essere eseguita per prima.</span><span class="sxs-lookup"><span data-stu-id="a8168-163">Therefore, the more specific call (with the compression filter) must happen first.</span></span>

<span data-ttu-id="a8168-164">Nella discussione precedente si presuppone che il file di origine sia un file AVI.</span><span class="sxs-lookup"><span data-stu-id="a8168-164">The previous discussion has assumed that the source file is an AVI file.</span></span> <span data-ttu-id="a8168-165">Tuttavia, questa tecnica funziona anche con altri tipi di file, ad esempio file MPEG.</span><span class="sxs-lookup"><span data-stu-id="a8168-165">However, this technique also works with other file types, such as MPEG files.</span></span> <span data-ttu-id="a8168-166">Il grafico di filtro risultante sarà leggermente diverso.</span><span class="sxs-lookup"><span data-stu-id="a8168-166">The resulting filter graph will be somewhat different.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8168-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8168-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8168-168">Ricompressione di un file AVI</span><span class="sxs-lookup"><span data-stu-id="a8168-168">Recompressing an AVI File</span></span>](recompressing-an-avi-file.md)
</dt> </dl>

 

 



