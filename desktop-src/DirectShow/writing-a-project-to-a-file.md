---
description: Scrittura di un progetto in un file
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: Scrittura di un progetto in un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f63ddbc6a021362134d420220f7e25c662553f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313391"
---
# <a name="writing-a-project-to-a-file"></a><span data-ttu-id="841ad-103">Scrittura di un progetto in un file</span><span class="sxs-lookup"><span data-stu-id="841ad-103">Writing a Project to a File</span></span>

<span data-ttu-id="841ad-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="841ad-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="841ad-105">Questo articolo descrive come scrivere un progetto di [servizi di modifica DirectShow](directshow-editing-services.md) in un file.</span><span class="sxs-lookup"><span data-stu-id="841ad-105">This article describes how to write a [DirectShow Editing Services](directshow-editing-services.md) project to a file.</span></span> <span data-ttu-id="841ad-106">In primo luogo viene descritto come scrivere un file con il motore di rendering di base.</span><span class="sxs-lookup"><span data-stu-id="841ad-106">First it describes how to write a file with the basic render engine.</span></span> <span data-ttu-id="841ad-107">Viene quindi descritta la ricompressione intelligente con il motore di rendering intelligente.</span><span class="sxs-lookup"><span data-stu-id="841ad-107">Then it describes smart recompression with the smart render engine.</span></span>

<span data-ttu-id="841ad-108">Per una panoramica su come i servizi di modifica DirectShow eseguono il rendering dei progetti, vedere [informazioni sui motori di rendering](about-the-render-engines.md).</span><span class="sxs-lookup"><span data-stu-id="841ad-108">For an overview of how DirectShow Editing Services renders projects, see [About the Render Engines](about-the-render-engines.md).</span></span>

<span data-ttu-id="841ad-109">**Uso del motore di rendering di base**</span><span class="sxs-lookup"><span data-stu-id="841ad-109">**Using the Basic Render Engine**</span></span>

<span data-ttu-id="841ad-110">Iniziare compilando il front-end del grafo, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="841ad-110">Start by building the front end of the graph, as follows:</span></span>

1.  <span data-ttu-id="841ad-111">Creare il motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="841ad-111">Create the render engine.</span></span>
2.  <span data-ttu-id="841ad-112">Specificare la sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="841ad-112">Specify the timeline.</span></span>
3.  <span data-ttu-id="841ad-113">Impostare l'intervallo di rendering.</span><span class="sxs-lookup"><span data-stu-id="841ad-113">Set the render range.</span></span> <span data-ttu-id="841ad-114">Facoltativa</span><span class="sxs-lookup"><span data-stu-id="841ad-114">(Optional)</span></span>
4.  <span data-ttu-id="841ad-115">Compilare il front-end del grafo.</span><span class="sxs-lookup"><span data-stu-id="841ad-115">Build the front end of the graph.</span></span>

<span data-ttu-id="841ad-116">Nell'esempio di codice seguente vengono illustrati questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="841ad-116">The following code example shows these steps.</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



<span data-ttu-id="841ad-117">Aggiungere quindi i filtri multiplexer e di scrittura file al grafico filtro.</span><span class="sxs-lookup"><span data-stu-id="841ad-117">Next, add multiplexer and file-writing filters to the filter graph.</span></span> <span data-ttu-id="841ad-118">Il modo più semplice per eseguire questa operazione è il [Generatore Graph di acquisizione](capture-graph-builder.md), un componente DirectShow per la creazione di grafici di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="841ad-118">The easiest way to do this is with the [Capture Graph Builder](capture-graph-builder.md), a DirectShow component for building capture graphs.</span></span> <span data-ttu-id="841ad-119">Il generatore di grafici di acquisizione espone l'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="841ad-119">The capture graph builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="841ad-120">Eseguire la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="841ad-120">Perform the following steps:</span></span>

1.  <span data-ttu-id="841ad-121">Creare un'istanza del generatore di grafici di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="841ad-121">Create an instance of the capture graph builder.</span></span>
2.  <span data-ttu-id="841ad-122">Ottenere un puntatore al grafo e passarlo al generatore di grafici.</span><span class="sxs-lookup"><span data-stu-id="841ad-122">Obtain a pointer to the graph and pass it to the graph builder.</span></span>
3.  <span data-ttu-id="841ad-123">Specificare il nome e il tipo di supporto del file di output.</span><span class="sxs-lookup"><span data-stu-id="841ad-123">Specify the name and media type of the output file.</span></span> <span data-ttu-id="841ad-124">Questo passaggio ottiene anche un puntatore al filtro Mux, che è necessario in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="841ad-124">This step also obtains a pointer to the mux filter, which is required later.</span></span>

<span data-ttu-id="841ad-125">Nell'esempio di codice seguente vengono illustrati questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="841ad-125">The following code example shows these steps.</span></span>


```C++
CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, CLSCTX_INPROC, 
    IID_ICaptureGraphBuilder2, (void **)&pBuilder);

// Get a pointer to the graph front end.
IGraphBuilder *pGraph;
pRender->GetFilterGraph(&pGraph);
pBuilder->SetFiltergraph(pGraph);

// Create the file-writing section.
IBaseFilter *pMux;
pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("Output.avi"), &pMux, NULL);
```



<span data-ttu-id="841ad-126">Infine, connettere i pin di output sul front-end al filtro MUX.</span><span class="sxs-lookup"><span data-stu-id="841ad-126">Finally, connect the output pins on the front end to the mux filter.</span></span>

1.  <span data-ttu-id="841ad-127">Recuperare il numero di gruppi.</span><span class="sxs-lookup"><span data-stu-id="841ad-127">Retrieve the number of groups.</span></span>
2.  <span data-ttu-id="841ad-128">Per ogni pin, ottenere un puntatore al pin.</span><span class="sxs-lookup"><span data-stu-id="841ad-128">For each pin, obtain a pointer to the pin.</span></span>
3.  <span data-ttu-id="841ad-129">Facoltativamente, creare un'istanza di un filtro di compressione per comprimere il flusso.</span><span class="sxs-lookup"><span data-stu-id="841ad-129">Optionally, create an instance of a compression filter to compress the stream.</span></span> <span data-ttu-id="841ad-130">Il tipo di compressore dipenderà dal tipo di supporto del gruppo.</span><span class="sxs-lookup"><span data-stu-id="841ad-130">The type of compressor will depend on the media type of the group.</span></span> <span data-ttu-id="841ad-131">È possibile utilizzare l' [enumeratore System Device](system-device-enumerator.md) per enumerare i filtri di compressione disponibili.</span><span class="sxs-lookup"><span data-stu-id="841ad-131">You can use the [System Device Enumerator](system-device-enumerator.md) to enumerate the available compression filters.</span></span> <span data-ttu-id="841ad-132">Per altre informazioni, vedere [enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="841ad-132">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>
4.  <span data-ttu-id="841ad-133">Facoltativamente, impostare parametri di compressione, ad esempio la frequenza dei fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="841ad-133">Optionally, set compression parameters such as the key-frame rate.</span></span> <span data-ttu-id="841ad-134">Questo passaggio è descritto in dettaglio più avanti in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="841ad-134">This step is discussed in detail later in the article.</span></span>
5.  <span data-ttu-id="841ad-135">Chiamare [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span><span class="sxs-lookup"><span data-stu-id="841ad-135">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span> <span data-ttu-id="841ad-136">Questo metodo accetta puntatori al pin, al filtro di compressione (se presente) e al multiplexer.</span><span class="sxs-lookup"><span data-stu-id="841ad-136">This method takes pointers to the pin, the compression filter (if any), and the multiplexer.</span></span>

<span data-ttu-id="841ad-137">Nell'esempio di codice seguente viene illustrato come connettere i pin di output.</span><span class="sxs-lookup"><span data-stu-id="841ad-137">The following code example shows how to connect the output pins.</span></span>


```C++
long NumGroups;
pTimeline->GetGroupCount(&NumGroups);

// Loop through the groups and get the output pins.
for (i = 0; i < NumGroups; i++)
{
    IPin *pPin;
    if (pRender->GetGroupOutputPin(i, &pPin) == S_OK) 
    {
        IBaseFilter *pCompressor;
        // Create a compressor filter. (Not shown.)
        // Set compression parameters. (Not shown.)

        // Connect the pin.
        pBuilder->RenderStream(NULL, NULL, pPin, pCompressor, pMux);
        pCompressor->Release();
        pPin->Release();
    }
}
```



<span data-ttu-id="841ad-138">Per impostare i parametri di compressione (passaggio 4, in precedenza), usare l'interfaccia [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) .</span><span class="sxs-lookup"><span data-stu-id="841ad-138">To set compression parameters (step 4, previously), use the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface.</span></span> <span data-ttu-id="841ad-139">Questa interfaccia viene esposta nei pin di output dei filtri di compressione.</span><span class="sxs-lookup"><span data-stu-id="841ad-139">This interface is exposed on the output pins of compression filters.</span></span> <span data-ttu-id="841ad-140">Enumerare i pin del filtro di compressione ed eseguire una query su ogni pin di output per **IAMVideoCompression**.</span><span class="sxs-lookup"><span data-stu-id="841ad-140">Enumerate the compression filter's pins, and query each output pin for **IAMVideoCompression**.</span></span> <span data-ttu-id="841ad-141">Per informazioni sull'enumerazione dei pin, vedere [enumerazione dei pin](enumerating-pins.md). Assicurarsi di rilasciare tutti i puntatori di interfaccia ottenuti durante questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="841ad-141">(For information about enumerating pins, see [Enumerating Pins](enumerating-pins.md).) Be sure to release all the interface pointers that you obtained during this step.</span></span>

<span data-ttu-id="841ad-142">Dopo aver compilato il grafico del filtro, chiamare il metodo [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) in gestione grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="841ad-142">After you build the filter graph, call the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method on the filter graph manager.</span></span> <span data-ttu-id="841ad-143">Durante l'esecuzione del grafico di filtro, i dati vengono scritti in un file.</span><span class="sxs-lookup"><span data-stu-id="841ad-143">As the filter graph runs, it writes the data to a file.</span></span> <span data-ttu-id="841ad-144">Usare la notifica degli eventi per attendere il completamento della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="841ad-144">Use event notification to wait for playback to complete.</span></span> <span data-ttu-id="841ad-145">(Vedere [rispondere agli eventi](responding-to-events.md)). Al termine della riproduzione, è necessario chiamare in modo esplicito [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) per arrestare il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="841ad-145">(See [Responding to Events](responding-to-events.md).) When playback finishes, you must explicitly call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) to stop the filter graph.</span></span> <span data-ttu-id="841ad-146">In caso contrario, il file non viene scritto correttamente.</span><span class="sxs-lookup"><span data-stu-id="841ad-146">Otherwise, the file is not written correctly.</span></span>

<span data-ttu-id="841ad-147">**Uso del motore di rendering intelligente**</span><span class="sxs-lookup"><span data-stu-id="841ad-147">**Using the Smart Render Engine**</span></span>

<span data-ttu-id="841ad-148">Per ottenere i vantaggi della ricompressione intelligente, usare il motore di rendering intelligente al posto del motore di rendering di base.</span><span class="sxs-lookup"><span data-stu-id="841ad-148">To get the benefits of smart recompression, use the smart render engine in place of the basic render engine.</span></span> <span data-ttu-id="841ad-149">I passaggi per la compilazione del grafo sono quasi identici.</span><span class="sxs-lookup"><span data-stu-id="841ad-149">The steps in building the graph are almost the same.</span></span> <span data-ttu-id="841ad-150">La differenza principale consiste nel fatto che la compressione viene gestita nel front-end del grafo, non nella sezione relativa alla scrittura di file.</span><span class="sxs-lookup"><span data-stu-id="841ad-150">The major difference is that compression is handled in the front end of the graph, not in the file-writing section.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="841ad-151">Non usare il motore di rendering intelligente per leggere o scrivere file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="841ad-151">Do not use the smart render engine to read or write Windows Media files.</span></span>

 

<span data-ttu-id="841ad-152">Ogni gruppo di video dispone di una proprietà che specifica il formato di compressione per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="841ad-152">Each video group has a property that specifies the compression format for that group.</span></span> <span data-ttu-id="841ad-153">Il formato di compressione deve corrispondere esattamente al formato non compresso del gruppo in altezza, larghezza, profondità dei bit e frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="841ad-153">The compression format must exactly match the group's uncompressed format in height, width, bit depth, and frame rate.</span></span> <span data-ttu-id="841ad-154">Il motore di rendering intelligente utilizza il formato di compressione quando costruisce il grafo.</span><span class="sxs-lookup"><span data-stu-id="841ad-154">The smart render engine uses the compression format when it constructs the graph.</span></span> <span data-ttu-id="841ad-155">Prima di impostare il formato di compressione, assicurarsi di impostare il formato non compresso per il gruppo chiamando [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="841ad-155">Before you set the compression format, make sure to set the uncompressed format for that group by calling [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md).</span></span>

<span data-ttu-id="841ad-156">Per impostare il formato di compressione di un gruppo, chiamare il metodo [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) .</span><span class="sxs-lookup"><span data-stu-id="841ad-156">To set a group's compression format, call the [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method.</span></span> <span data-ttu-id="841ad-157">Questo metodo accetta un puntatore a una struttura [**SCompFmt0**](scompfmt0.md) .</span><span class="sxs-lookup"><span data-stu-id="841ad-157">This method takes a pointer to an [**SCompFmt0**](scompfmt0.md) structure.</span></span> <span data-ttu-id="841ad-158">La struttura **SCompFmt0** ha due membri: **nFormatId**, che deve essere zero e **mediaType**, ovvero una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="841ad-158">The **SCompFmt0** structure has two members: **nFormatId**, which must be zero, and **MediaType**, which is an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="841ad-159">Inizializzare la struttura del **\_ \_ tipo di supporto am** con le informazioni sul formato.</span><span class="sxs-lookup"><span data-stu-id="841ad-159">Initialize the **AM\_MEDIA\_TYPE** structure with the format information.</span></span>

> [!Note]  
> <span data-ttu-id="841ad-160">Se si vuole che il progetto finale abbia lo stesso formato di uno dei file di origine, è possibile ottenere la \_ struttura del tipo di supporto am \_ direttamente dal file di origine, usando il rilevatore di contenuti multimediali.</span><span class="sxs-lookup"><span data-stu-id="841ad-160">If you want the final project to have the same format as one of your source files, you can get the AM\_MEDIA\_TYPE structure directly from the source file, using the media detector.</span></span> <span data-ttu-id="841ad-161">Vedere [**IMediaDet:: Get \_ StreamMediaType**](imediadet-get-streammediatype.md).</span><span class="sxs-lookup"><span data-stu-id="841ad-161">See [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md).</span></span>

 

<span data-ttu-id="841ad-162">Eseguire il cast della variabile [**SCompFmt0**](scompfmt0.md) a un puntatore di tipo **Long**, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="841ad-162">Cast the [**SCompFmt0**](scompfmt0.md) variable to a pointer of type **long**, as shown in the following example.</span></span>


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



<span data-ttu-id="841ad-163">Il motore di rendering intelligente cerca automaticamente un filtro di compressione compatibile.</span><span class="sxs-lookup"><span data-stu-id="841ad-163">The smart render engine automatically searches for a compatible compression filter.</span></span> <span data-ttu-id="841ad-164">È anche possibile specificare un filtro di compressione per un gruppo chiamando [**ISmartRenderEngine:: SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).</span><span class="sxs-lookup"><span data-stu-id="841ad-164">You can also specify a compression filter for a group by calling [**ISmartRenderEngine::SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).</span></span>

<span data-ttu-id="841ad-165">Per compilare il grafo, usare la stessa procedura descritta per il motore di rendering di base nella sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="841ad-165">To build the graph, use the same steps that were described for the Basic Render Engine in the previous section.</span></span> <span data-ttu-id="841ad-166">Le uniche differenze sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="841ad-166">The only differences are the following:</span></span>

-   <span data-ttu-id="841ad-167">Usare il motore di rendering intelligente, non il motore di rendering di base.</span><span class="sxs-lookup"><span data-stu-id="841ad-167">Use the smart render engine, not the basic render engine.</span></span> <span data-ttu-id="841ad-168">L'identificatore di classe è CLSID \_ SmartRenderEngine.</span><span class="sxs-lookup"><span data-stu-id="841ad-168">The class identifier is CLSID\_SmartRenderEngine.</span></span>
-   <span data-ttu-id="841ad-169">Impostare i parametri di compressione dopo aver compilato il front-end, ma prima di eseguire il rendering dei pin di output.</span><span class="sxs-lookup"><span data-stu-id="841ad-169">Set compression parameters after you build the front end but before you render the output pins.</span></span> <span data-ttu-id="841ad-170">Chiamare il metodo [**ISmartRenderEngine:: GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) per ottenere un puntatore al filtro di compressione di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="841ad-170">Call the [**ISmartRenderEngine::GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) method to obtain a pointer to a group's compression filter.</span></span> <span data-ttu-id="841ad-171">Quindi eseguire una query per l'interfaccia [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="841ad-171">Then query for the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface, as described previously.</span></span>
-   <span data-ttu-id="841ad-172">Quando si esegue il rendering dei pin di output, non è necessario inserire un filtro di compressione.</span><span class="sxs-lookup"><span data-stu-id="841ad-172">When you render the output pins, there is no need to insert a compression filter.</span></span> <span data-ttu-id="841ad-173">Il flusso è già compresso.</span><span class="sxs-lookup"><span data-stu-id="841ad-173">The stream is already compressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="841ad-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="841ad-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="841ad-175">Rendering di un progetto</span><span class="sxs-lookup"><span data-stu-id="841ad-175">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



