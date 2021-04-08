---
description: Creazione di grafici con il generatore di grafici di acquisizione
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: Creazione di grafici con il generatore di grafici di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e48347a73cdac545723ac226cc58a0175dec5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876957"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a><span data-ttu-id="a124d-103">Creazione di grafici con il generatore di grafici di acquisizione</span><span class="sxs-lookup"><span data-stu-id="a124d-103">Building Graphs with the Capture Graph Builder</span></span>

<span data-ttu-id="a124d-104">Nonostante il nome, il generatore di grafici di acquisizione è utile per la creazione di molti tipi di grafici di filtri personalizzati, non solo per l'acquisizione dei grafici.</span><span class="sxs-lookup"><span data-stu-id="a124d-104">Despite its name, the Capture Graph Builder is useful for building many kinds of custom filter graphs, not only capture graphs.</span></span> <span data-ttu-id="a124d-105">Questo articolo fornisce una breve panoramica su come usare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="a124d-105">This article provides a brief overview of how to use this object.</span></span>

<span data-ttu-id="a124d-106">Il generatore di grafici di acquisizione espone l'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="a124d-106">The Capture Graph Builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="a124d-107">Per iniziare, chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare il generatore del grafico di acquisizione e il gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="a124d-107">Start by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Capture Graph Builder and the Filter Graph Manager.</span></span> <span data-ttu-id="a124d-108">Inizializzare quindi il generatore del grafico di acquisizione chiamando [**ICaptureGraphBuilder2:: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) con un puntatore al gestore del grafico di filtro, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="a124d-108">Then initialize the Capture Graph Builder by calling [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) with a pointer to the Filter Graph Manager, as follows:</span></span>


```C++
IGraphBuilder *pGraph = NULL;
ICaptureGraphBuilder2 *pBuilder = NULL;

// Create the Filter Graph Manager.
HRESULT hr =  CoCreateInstance(CLSID_FilterGraph, NULL,
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);

if (SUCCEEDED(hr))
{
    // Create the Capture Graph Builder.
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL,
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, 
        (void **)&pBuilder);
    if (SUCCEEDED(hr))
    {
        pBuilder->SetFiltergraph(pGraph);
    }
};
```



## <a name="connecting-filters"></a><span data-ttu-id="a124d-109">Connessione di filtri</span><span class="sxs-lookup"><span data-stu-id="a124d-109">Connecting Filters</span></span>

<span data-ttu-id="a124d-110">Il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) connette due o tre filtri insieme in una catena.</span><span class="sxs-lookup"><span data-stu-id="a124d-110">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method connects two or three filters together in a chain.</span></span> <span data-ttu-id="a124d-111">In genere, il metodo funziona meglio quando ogni filtro non contiene più di un pin di input o di output dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="a124d-111">Generally, the method works best when each filter has no more than one input pin or output pin of the same type.</span></span> <span data-ttu-id="a124d-112">Questa discussione inizia ignorando i primi due parametri di **RenderStream** e concentrandosi sugli ultimi tre parametri.</span><span class="sxs-lookup"><span data-stu-id="a124d-112">This discussion begins by ignoring the first two parameters of **RenderStream** and focusing on the last three parameters.</span></span> <span data-ttu-id="a124d-113">Il terzo parametro è un puntatore [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , che può specificare un filtro (come puntatore di interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) ) o un pin di output (come puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) ).</span><span class="sxs-lookup"><span data-stu-id="a124d-113">The third parameter is an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer, which can specify either a filter (as an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface pointer) or an output pin (as an [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface pointer).</span></span> <span data-ttu-id="a124d-114">Il quarto e il quinto parametro specificano i puntatori **IBaseFilter** .</span><span class="sxs-lookup"><span data-stu-id="a124d-114">The fourth and fifth parameters specify **IBaseFilter** pointers.</span></span> <span data-ttu-id="a124d-115">Il metodo **RenderStream** connette tutti e tre i filtri in una catena.</span><span class="sxs-lookup"><span data-stu-id="a124d-115">The **RenderStream** method connects all three filters in a chain.</span></span> <span data-ttu-id="a124d-116">Si supponga, ad esempio, che *a*, *B* e *C* siano filtri.</span><span class="sxs-lookup"><span data-stu-id="a124d-116">For example, suppose that *A*, *B*, and *C* are filters.</span></span> <span data-ttu-id="a124d-117">Si supponga per ora che ogni filtro includa esattamente un pin di input e un pin di output.</span><span class="sxs-lookup"><span data-stu-id="a124d-117">Assume for now that each filter has exactly one input pin and one output pin.</span></span> <span data-ttu-id="a124d-118">La chiamata seguente connette a a B, quindi B a C:</span><span class="sxs-lookup"><span data-stu-id="a124d-118">The following call connects A to B, and then B to C:</span></span>

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

<span data-ttu-id="a124d-119">Tutte le connessioni sono "intelligenti", vale a dire che i filtri aggiuntivi vengono aggiunti al grafico in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="a124d-119">All connections are "intelligent," meaning that additional filters are added to the graph as needed.</span></span> <span data-ttu-id="a124d-120">Per informazioni dettagliate, vedere [connessione intelligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="a124d-120">For details, see [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="a124d-121">Per connettere solo due filtri, impostare il valore intermedio su **null**.</span><span class="sxs-lookup"><span data-stu-id="a124d-121">To connect just two filters, set the middle value to **NULL**.</span></span> <span data-ttu-id="a124d-122">Questa chiamata, ad esempio, connette a C:</span><span class="sxs-lookup"><span data-stu-id="a124d-122">For example, this call connects A to C:</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

<span data-ttu-id="a124d-123">È possibile creare catene più lunghe chiamando il metodo due volte:</span><span class="sxs-lookup"><span data-stu-id="a124d-123">You can create longer chains by calling the method twice:</span></span>

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

<span data-ttu-id="a124d-124">Se l'ultimo parametro è **null**, il metodo individua automaticamente un renderer predefinito.</span><span class="sxs-lookup"><span data-stu-id="a124d-124">If the last parameter is **NULL**, the method automatically locates a default renderer.</span></span> <span data-ttu-id="a124d-125">Usa il [renderer video](video-renderer-filter.md) per video e il [renderer DirectSound](directsound-renderer-filter.md) per l'audio.</span><span class="sxs-lookup"><span data-stu-id="a124d-125">It uses the [Video Renderer](video-renderer-filter.md) for video and the [DirectSound Renderer](directsound-renderer-filter.md) for audio.</span></span> <span data-ttu-id="a124d-126">Così</span><span class="sxs-lookup"><span data-stu-id="a124d-126">Thus:</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

<span data-ttu-id="a124d-127">equivale a</span><span class="sxs-lookup"><span data-stu-id="a124d-127">is equivalent to</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

<span data-ttu-id="a124d-128">dove *R* è il renderer appropriato.</span><span class="sxs-lookup"><span data-stu-id="a124d-128">where *R* is the appropriate renderer.</span></span> <span data-ttu-id="a124d-129">Tuttavia, per connettere il filtro renderer video mixing anziché il renderer video, è necessario specificarlo in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="a124d-129">To connect the Video Mixing Renderer filter instead of the Video Renderer, however, you must specify it explicitly.</span></span>

<span data-ttu-id="a124d-130">Se si specifica un filtro nel terzo parametro, anziché un PIN, potrebbe essere necessario indicare quale pin di output deve essere usato per la connessione.</span><span class="sxs-lookup"><span data-stu-id="a124d-130">If you specify a filter in the third parameter, rather than a pin, you may need to indicate which output pin should be used for the connection.</span></span> <span data-ttu-id="a124d-131">Questo è lo scopo dei primi due parametri del metodo.</span><span class="sxs-lookup"><span data-stu-id="a124d-131">That is the purpose of the method's first two parameters.</span></span> <span data-ttu-id="a124d-132">Il primo parametro si applica solo ai filtri di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a124d-132">The first parameter applies only to capture filters.</span></span> <span data-ttu-id="a124d-133">Specifica un GUID che indica una categoria di pin.</span><span class="sxs-lookup"><span data-stu-id="a124d-133">It specifies a GUID that indicates a pin category.</span></span> <span data-ttu-id="a124d-134">Per un elenco completo delle categorie, vedere [impostare la proprietà pin](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="a124d-134">For a complete list of categories, see [Pin Property Set](pin-property-set.md).</span></span> <span data-ttu-id="a124d-135">Due categorie sono valide per tutti i filtri di acquisizione:</span><span class="sxs-lookup"><span data-stu-id="a124d-135">Two of the categories are valid for all capture filters:</span></span>

-   <span data-ttu-id="a124d-136">**\_ \_ blocca acquisizione categoria**</span><span class="sxs-lookup"><span data-stu-id="a124d-136">**PIN\_CATEGORY\_CAPTURE**</span></span>
-   <span data-ttu-id="a124d-137">**\_anteprima categoria \_ pin**</span><span class="sxs-lookup"><span data-stu-id="a124d-137">**PIN\_CATEGORY\_PREVIEW**</span></span>

<span data-ttu-id="a124d-138">Se un filtro di acquisizione non fornisce pin distinti per l'acquisizione e l'anteprima, il metodo [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserisce un filtro di [Smart Tee](smart-tee-filter.md) , che suddivide il flusso in un flusso di acquisizione e in un flusso di anteprima.</span><span class="sxs-lookup"><span data-stu-id="a124d-138">If a capture filter does not supply separate pins for capture and preview, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="a124d-139">Dal punto di vista dell'applicazione, è possibile considerare semplicemente tutti i filtri di acquisizione come aventi pin distinti e ignorare la topologia sottostante del grafo.</span><span class="sxs-lookup"><span data-stu-id="a124d-139">From the application's standpoint, you can simply treat all capture filters as having separate pins and ignore the underlying topology of the graph.</span></span>

<span data-ttu-id="a124d-140">Per l'acquisizione di file, connettere il pin di acquisizione a un filtro MUX.</span><span class="sxs-lookup"><span data-stu-id="a124d-140">For file capture, connect the capture pin to a mux filter.</span></span> <span data-ttu-id="a124d-141">Per l'anteprima in tempo reale, connettere il pin di anteprima a un renderer.</span><span class="sxs-lookup"><span data-stu-id="a124d-141">For live preview, connect the preview pin to a renderer.</span></span> <span data-ttu-id="a124d-142">Se si passa a due categorie, il grafico potrebbe eliminare un numero eccessivo di fotogrammi durante l'acquisizione dei file; Tuttavia, se il grafo è connesso correttamente, i frame di anteprima vengono eliminati in base alle esigenze, in modo da mantenere la velocità effettiva nel flusso di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a124d-142">If you switch the two categories, the graph might drop an excessive number of frames during the file capture; but if the graph is connected properly, it drops preview frames as needed in order to maintain throughput on the capture stream.</span></span>

<span data-ttu-id="a124d-143">Nell'esempio seguente viene illustrato come connettere entrambi i flussi:</span><span class="sxs-lookup"><span data-stu-id="a124d-143">The following example shows how to connect both streams:</span></span>


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



<span data-ttu-id="a124d-144">Alcuni filtri di acquisizione supportano anche le didascalie chiuse, indicate dalla **\_ categoria pin \_ VBI**.</span><span class="sxs-lookup"><span data-stu-id="a124d-144">Some capture filters also support closed captions, indicated by **PIN\_CATEGORY\_VBI**.</span></span> <span data-ttu-id="a124d-145">Per acquisire le didascalie chiuse in un file, eseguire il rendering di questa categoria nel filtro MUX.</span><span class="sxs-lookup"><span data-stu-id="a124d-145">To capture the closed captions to a file, render this category to the mux filter.</span></span> <span data-ttu-id="a124d-146">Per visualizzare le didascalie chiuse nella finestra di anteprima, connettersi al renderer:</span><span class="sxs-lookup"><span data-stu-id="a124d-146">To view the closed captions in your preview window, connect to the renderer:</span></span>


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



<span data-ttu-id="a124d-147">Il secondo parametro di [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifica il tipo di supporto ed è in genere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="a124d-147">The second parameter to [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifies the media type, and is typically one of the following:</span></span>

-   <span data-ttu-id="a124d-148">\_Audio MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="a124d-148">MEDIATYPE\_Audio</span></span>
-   <span data-ttu-id="a124d-149">Video di MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="a124d-149">MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="a124d-150">MEDIATYPE con \_ interfoliazione (DV)</span><span class="sxs-lookup"><span data-stu-id="a124d-150">MEDIATYPE\_Interleaved (DV)</span></span>

<span data-ttu-id="a124d-151">È possibile utilizzare questo parametro ogni volta che i pin di output del filtro supportano l'enumerazione dei tipi di supporto preferiti.</span><span class="sxs-lookup"><span data-stu-id="a124d-151">You can use this parameter whenever the filter's output pins support the enumeration of preferred media types.</span></span> <span data-ttu-id="a124d-152">Per le origini file, il generatore di grafici di acquisizione aggiunge automaticamente un filtro del parser, se necessario, e quindi esegue una query sui tipi di supporto nel parser.</span><span class="sxs-lookup"><span data-stu-id="a124d-152">For file sources, the Capture Graph Builder automatically adds a parser filter if needed, and then queries the media types on the parser.</span></span> <span data-ttu-id="a124d-153">Per un esempio, vedere [ricompressione di un file AVI](recompressing-an-avi-file.md). Se, inoltre, l'ultimo filtro della catena include diversi pin di input, il metodo tenterà di enumerare i tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="a124d-153">(For an example, see [Recompressing an AVI File](recompressing-an-avi-file.md).) Also, if the last filter in the chain has several input pins, the method attempts to enumerate their media types.</span></span> <span data-ttu-id="a124d-154">Tuttavia, non tutti i filtri supportano questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a124d-154">However, not all filters support this functionality.</span></span>

## <a name="finding-interfaces-on-filters-and-pins"></a><span data-ttu-id="a124d-155">Ricerca di interfacce su filtri e pin</span><span class="sxs-lookup"><span data-stu-id="a124d-155">Finding Interfaces on Filters and Pins</span></span>

<span data-ttu-id="a124d-156">Dopo aver compilato un grafo, in genere è necessario individuare varie interfacce esposte da filtri e pin nel grafico.</span><span class="sxs-lookup"><span data-stu-id="a124d-156">After you build a graph, you will typically need to locate various interfaces exposed by filters and pins in the graph.</span></span> <span data-ttu-id="a124d-157">Ad esempio, un filtro di acquisizione potrebbe esporre l'interfaccia [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) , mentre i pin di output del filtro potrebbero esporre l'interfaccia [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="a124d-157">For example, a capture filter might expose the [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface, while the filter's output pins might expose the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface.</span></span>

<span data-ttu-id="a124d-158">Il modo più semplice per trovare un'interfaccia consiste nell'usare il metodo [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) .</span><span class="sxs-lookup"><span data-stu-id="a124d-158">The simplest way to find an interface is to use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method.</span></span> <span data-ttu-id="a124d-159">Questo metodo consente di visualizzare il grafico (filtri e pin) fino a individuare l'interfaccia desiderata.</span><span class="sxs-lookup"><span data-stu-id="a124d-159">This method walks the graph (filters and pins) until it locates the desired interface.</span></span> <span data-ttu-id="a124d-160">È possibile specificare il punto di partenza per la ricerca ed è possibile limitare la ricerca ai filtri upstream o downstream dal punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="a124d-160">You can specify the starting point for the search, and you can limit the search to filters upstream or downstream from the starting point.</span></span>

<span data-ttu-id="a124d-161">L'esempio seguente cerca l'interfaccia [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) in un pin di anteprima video:</span><span class="sxs-lookup"><span data-stu-id="a124d-161">The following example searches for the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface on a video preview pin:</span></span>


```C++
IAMStreamConfig *pConfig = NULL;
HRESULT hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, 
    &MEDIATYPE_Video,
    pVCap, 
    IID_IAMStreamConfig, 
    (void**)&pConfig
);
if (SUCCESSFUL(hr))
{
    /* ... */
    pConfig->Release();
}
```



> [!Note]  
> <span data-ttu-id="a124d-162">L'argomento [trovare un'interfaccia in un filtro o un pin](find-an-interface-on-a-filter-or-pin.md) Mostra un approccio alternativo che usa l'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) anziché [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2).</span><span class="sxs-lookup"><span data-stu-id="a124d-162">The topic [Find an Interface on a Filter or Pin](find-an-interface-on-a-filter-or-pin.md) shows an alternative approach that uses the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface instead of [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2).</span></span> <span data-ttu-id="a124d-163">L'approccio da usare dipende dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a124d-163">Which approach to use depends on your application.</span></span> <span data-ttu-id="a124d-164">Se l'applicazione usa già **ICaptureGraphBuilder2** per compilare il grafo, [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) è un approccio valido.</span><span class="sxs-lookup"><span data-stu-id="a124d-164">If your application already uses **ICaptureGraphBuilder2** to build the graph, then [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) is a good approach.</span></span> <span data-ttu-id="a124d-165">In caso contrario, provare a usare i metodi **IGraphBuilder** .</span><span class="sxs-lookup"><span data-stu-id="a124d-165">Otherwise, consider using the **IGraphBuilder** methods.</span></span>

 

## <a name="finding-pins"></a><span data-ttu-id="a124d-166">Ricerca di pin</span><span class="sxs-lookup"><span data-stu-id="a124d-166">Finding Pins</span></span>

<span data-ttu-id="a124d-167">Meno comunemente, potrebbe essere necessario individuare un singolo pin in un filtro, sebbene nella maggior parte dei casi i metodi [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) e [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) consentano di evitare il problema.</span><span class="sxs-lookup"><span data-stu-id="a124d-167">Less commonly, you may need to locate an individual pin on a filter, although in most cases the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) and [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) methods will save you the trouble.</span></span> <span data-ttu-id="a124d-168">Se è necessario trovare un pin particolare su un filtro, il metodo helper [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) è utile.</span><span class="sxs-lookup"><span data-stu-id="a124d-168">If you do need to find a particular pin on a filter, the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) helper method is useful.</span></span> <span data-ttu-id="a124d-169">Specificare la categoria, il tipo di supporto (video o audio), la direzione e se il PIN deve essere scollegato.</span><span class="sxs-lookup"><span data-stu-id="a124d-169">Specify the category, the media type (video or audio), the direction, and whether the pin must be unconnected.</span></span>

<span data-ttu-id="a124d-170">Ad esempio, il codice seguente cerca un pin di anteprima video non connesso in un filtro di acquisizione:</span><span class="sxs-lookup"><span data-stu-id="a124d-170">For example, the following code searches for an unconnected video preview pin on a capture filter:</span></span>


```C++
IPin *pPin = NULL;
hr = pBuild->FindPin(
    pCap,                   // Pointer to the filter to search.
    PINDIR_OUTPUT,          // Search for an output pin.
    &PIN_CATEGORY_PREVIEW,  // Search for a preview pin.
    &MEDIATYPE_Video,       // Search for a video pin.
    TRUE,                   // The pin must be unconnected. 
    0,                      // Return the first matching pin (index 0).
    &pPin);                 // This variable receives the IPin pointer.
if (SUCCESSFUL(hr))
{
    /* ... */
    pPin->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="a124d-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a124d-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a124d-172">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="a124d-172">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
