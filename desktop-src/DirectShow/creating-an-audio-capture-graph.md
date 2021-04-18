---
description: Creazione di un grafico di acquisizione audio
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Creazione di un grafico di acquisizione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3c731a7dc498fcb7180bc56ae6a7f94dbec6d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304322"
---
# <a name="creating-an-audio-capture-graph"></a><span data-ttu-id="6124c-103">Creazione di un grafico di acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="6124c-103">Creating an Audio Capture Graph</span></span>

<span data-ttu-id="6124c-104">Il primo passaggio per un'applicazione di acquisizione audio consiste nel creare un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="6124c-104">The first step for an audio capture application is to build a filter graph.</span></span> <span data-ttu-id="6124c-105">La configurazione del grafico dipende dal tipo di file che si desidera creare.</span><span class="sxs-lookup"><span data-stu-id="6124c-105">The configuration of the graph depends on the type of file that you want to create.</span></span>

-   <span data-ttu-id="6124c-106">File AVI solo audio: filtro di acquisizione audio per il filtro [Mux AVI](avi-mux-filter.md) e Mux AVI al filtro del [writer di file](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="6124c-106">Audio-only AVI file: Audio Capture Filter to [AVI Mux](avi-mux-filter.md) filter, and AVI Mux to [File Writer](file-writer-filter.md) filter.</span></span>
-   <span data-ttu-id="6124c-107">File WAV: filtro di acquisizione audio per l' [esempio di filtro WavDest](wavdest-filter-sample.md) nel filtro del writer di file</span><span class="sxs-lookup"><span data-stu-id="6124c-107">WAV file: Audio Capture Filter to [WavDest Filter Sample](wavdest-filter-sample.md) to File Writer Filter</span></span>
-   <span data-ttu-id="6124c-108">File Windows Media Audio (WMA): filtro di acquisizione audio per il filtro del [writer ASF WM](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="6124c-108">Windows Media Audio (.wma) file: Audio Capture Filter to [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

<span data-ttu-id="6124c-109">Il filtro WavDest viene fornito come esempio SDK.</span><span class="sxs-lookup"><span data-stu-id="6124c-109">The WavDest filter is provided as an SDK sample.</span></span> <span data-ttu-id="6124c-110">Per usarlo, è necessario compilare e registrare il filtro.</span><span class="sxs-lookup"><span data-stu-id="6124c-110">To use it, you must build and register the filter.</span></span>

<span data-ttu-id="6124c-111">Per utilizzare il filtro del writer ASF, è necessario installare Windows Media SDK e ottenere una chiave software per sbloccare il filtro.</span><span class="sxs-lookup"><span data-stu-id="6124c-111">To use the ASF Writer filter, you must install the Windows Media SDK and obtain a software key to unlock the filter.</span></span> <span data-ttu-id="6124c-112">Per ulteriori informazioni, vedere [utilizzo di Windows Media in DirectShow](using-windows-media-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="6124c-112">For more information, see [Using Windows Media in DirectShow](using-windows-media-in-directshow.md).</span></span>

<span data-ttu-id="6124c-113">È possibile compilare il grafo del filtro usando l'oggetto [Capture Graph Builder](capture-graph-builder.md) oppure è possibile compilare il grafo "Manually"; ovvero, fare in modo che l'applicazione aggiunga e connetta ogni filtro a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="6124c-113">You can build the filter graph using the [Capture Graph Builder](capture-graph-builder.md) object, or you can build the graph "manually"; that is, have the application programmatically add and connect each filter.</span></span> <span data-ttu-id="6124c-114">Questo articolo descrive l'approccio manuale.</span><span class="sxs-lookup"><span data-stu-id="6124c-114">This article describes the manual approach.</span></span> <span data-ttu-id="6124c-115">Per ulteriori informazioni sull'utilizzo del generatore di grafici di acquisizione, vedere [acquisizione video](video-capture.md).</span><span class="sxs-lookup"><span data-stu-id="6124c-115">For more information about using the Capture Graph Builder, see [Video Capture](video-capture.md).</span></span> <span data-ttu-id="6124c-116">Gran parte delle informazioni contenute in questo articolo si applica solo ai grafici di solo audio.</span><span class="sxs-lookup"><span data-stu-id="6124c-116">Much of the information in that article applies to audio-only graphs.</span></span>

<span data-ttu-id="6124c-117">Aggiunta del dispositivo di acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="6124c-117">Adding the Audio Capture Device</span></span>

<span data-ttu-id="6124c-118">Poiché il filtro di acquisizione audio comunica con un dispositivo hardware specifico, non è possibile chiamare semplicemente **CoCreateInstance** per creare il filtro.</span><span class="sxs-lookup"><span data-stu-id="6124c-118">Because the Audio Capture Filter communicates with a specific hardware device, you cannot simply call **CoCreateInstance** to create the filter.</span></span> <span data-ttu-id="6124c-119">Usare invece l' [enumeratore System Device](system-device-enumerator.md) per enumerare tutti i dispositivi nella categoria "origini di acquisizione audio", identificata dall'identificatore di classe CLSID \_ AudioInputDeviceCategory.</span><span class="sxs-lookup"><span data-stu-id="6124c-119">Instead, use the [System Device Enumerator](system-device-enumerator.md) to enumerate all of the devices in the "Audio Capture Sources" category, which is identified by the class identifier CLSID\_AudioInputDeviceCategory.</span></span>

<span data-ttu-id="6124c-120">L'enumeratore System Device restituisce un elenco di moniker per i dispositivi. il nome descrittivo di ogni moniker corrisponde al nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6124c-120">The System Device Enumerator returns a list of monikers for the devices; each moniker's friendly name corresponds to the name of the device.</span></span> <span data-ttu-id="6124c-121">Scegliere uno dei moniker restituiti e usarlo per creare un'istanza del filtro di acquisizione audio per quel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6124c-121">Choose one of the returned monikers and use it to create an instance of the Audio Capture Filter for that device.</span></span> <span data-ttu-id="6124c-122">Aggiungere il filtro al grafico filtro.</span><span class="sxs-lookup"><span data-stu-id="6124c-122">Add the filter to the filter graph.</span></span> <span data-ttu-id="6124c-123">Il dispositivo di registrazione audio preferito dell'utente viene visualizzato per primo nell'elenco dei moniker.</span><span class="sxs-lookup"><span data-stu-id="6124c-123">The user's preferred audio recording device appears first in the moniker list.</span></span> <span data-ttu-id="6124c-124">(L'utente seleziona un dispositivo preferito facendo clic su suoni e Multimedia nel pannello di controllo).</span><span class="sxs-lookup"><span data-stu-id="6124c-124">(The user selects a preferred device by clicking Sounds and Multimedia in Control Panel.)</span></span>

<span data-ttu-id="6124c-125">Per ulteriori informazioni, vedere [using the System Device Enumerator](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="6124c-125">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="6124c-126">Per specificare l'input da cui eseguire l'acquisizione, ottenere l'interfaccia [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) dal filtro di acquisizione audio e chiamare il metodo **put \_ Enable** per specificare l'input.</span><span class="sxs-lookup"><span data-stu-id="6124c-126">To specify which input to capture from, obtain the [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) interface from the Audio Capture filter and call the **put\_Enable** method to specify the input.</span></span> <span data-ttu-id="6124c-127">Una limitazione di questo metodo, tuttavia, è che diversi dispositivi hardware possono usare stringhe diverse per identificare gli input.</span><span class="sxs-lookup"><span data-stu-id="6124c-127">One limitation of this method, however, is that different hardware devices may use different strings to identify their inputs.</span></span> <span data-ttu-id="6124c-128">Ad esempio, una scheda può usare "Microphone" per identificare l'input del microfono e un'altra scheda può usare "MIC".</span><span class="sxs-lookup"><span data-stu-id="6124c-128">For example, one card may use "Microphone" to identify the microphone input and another card may use "Mic".</span></span> <span data-ttu-id="6124c-129">Per determinare l'identificatore di stringa per un determinato input, usare le funzioni multimediali di Windows [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85))e [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6124c-129">To determine the string identifier for a given input, use the Windows Multimedia functions [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85)), and [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)).</span></span> <span data-ttu-id="6124c-130">Per ulteriori informazioni, vedere l'argomento relativo alle [query del dispositivo mixer](/windows/desktop/Multimedia/mixer-device-queries) di MSDN.</span><span class="sxs-lookup"><span data-stu-id="6124c-130">See the MSDN topic [Mixer Device Queries](/windows/desktop/Multimedia/mixer-device-queries) for more information.</span></span>

<span data-ttu-id="6124c-131">Aggiunta del multiplexer e del writer di file</span><span class="sxs-lookup"><span data-stu-id="6124c-131">Adding the Multiplexer and the File Writer</span></span>

<span data-ttu-id="6124c-132">Un grafico di acquisizione audio deve contenere un multiplexer e un writer di file.</span><span class="sxs-lookup"><span data-stu-id="6124c-132">An audio capture graph must contain a multiplexer and a file writer.</span></span>

<span data-ttu-id="6124c-133">Un *multiplexer* è un filtro che combina uno o più flussi in un singolo flusso con un formato specifico.</span><span class="sxs-lookup"><span data-stu-id="6124c-133">A *multiplexer* is a filter that combines one or more streams into a single stream with a particular format.</span></span> <span data-ttu-id="6124c-134">Ad esempio, il filtro Mux AVI combina i flussi audio e video in un flusso AVI con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="6124c-134">For example, the AVI Mux filter combines audio and video streams into an interleaved AVI stream.</span></span> <span data-ttu-id="6124c-135">Per l'acquisizione audio, in genere è presente un solo flusso audio, ma i dati audio devono comunque essere inclusi in un formato che può essere salvato su disco, che richiede un multiplexer.</span><span class="sxs-lookup"><span data-stu-id="6124c-135">For audio capture, there is typically only a single audio stream, but the audio data must still be packaged into a format that can be saved to disk, which requires a multiplexer.</span></span> <span data-ttu-id="6124c-136">La scelta del multiplexer dipende dal formato di destinazione:</span><span class="sxs-lookup"><span data-stu-id="6124c-136">The choice of multiplexer depends on the target format:</span></span>

-   <span data-ttu-id="6124c-137">AVI: multiplexer AVI</span><span class="sxs-lookup"><span data-stu-id="6124c-137">AVI: AVI Multiplexer</span></span>
-   <span data-ttu-id="6124c-138">WAV: WavDest</span><span class="sxs-lookup"><span data-stu-id="6124c-138">WAV: WavDest</span></span>
-   <span data-ttu-id="6124c-139">WMA: ASF Writer</span><span class="sxs-lookup"><span data-stu-id="6124c-139">WMA: ASF Writer</span></span>

<span data-ttu-id="6124c-140">Un *writer di file* è un filtro che scrive i dati in ingresso in un file.</span><span class="sxs-lookup"><span data-stu-id="6124c-140">A *file writer* is a filter that writes incoming data to a file.</span></span> <span data-ttu-id="6124c-141">Per i file AVI o WAV, usare il [filtro del writer di file](file-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="6124c-141">For AVI or WAV files, use the [File Writer Filter](file-writer-filter.md).</span></span> <span data-ttu-id="6124c-142">Per i file WMA, il writer ASF funge sia da multiplexer che da writer di file.</span><span class="sxs-lookup"><span data-stu-id="6124c-142">For WMA files, the ASF Writer acts as both multiplexer and file writer.</span></span>

<span data-ttu-id="6124c-143">Dopo aver creato i filtri e averli aggiunti al grafico, connettere il pin di output del filtro di acquisizione audio al pin di input del multiplexer e connettere il pin di output del multiplexer al pin di input del writer del filtro (presupponendo che si tratta di filtri distinti).</span><span class="sxs-lookup"><span data-stu-id="6124c-143">After you create the filters and add them to the graph, connect the Audio Capture Filter's output pin to the multiplexer's input pin, and connect the multiplexer's output pin to the filter writer's input pin (assuming these are separate filters).</span></span> <span data-ttu-id="6124c-144">Per specificare il nome del file, eseguire una query sul writer di file per l'interfaccia [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) e chiamare il metodo [**IFileSinkFilter:: myFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) .</span><span class="sxs-lookup"><span data-stu-id="6124c-144">To specify the file name, query the file writer for the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface and call the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method.</span></span>

### <a name="example-code"></a><span data-ttu-id="6124c-145">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="6124c-145">Example Code</span></span>

<span data-ttu-id="6124c-146">Nell'esempio seguente viene illustrato come compilare un grafico di acquisizione audio usando il filtro WavDest.</span><span class="sxs-lookup"><span data-stu-id="6124c-146">The following example shows how to build an audio capture graph using the WavDest filter.</span></span> <span data-ttu-id="6124c-147">Gli stessi principi valgono per gli altri tipi di file.</span><span class="sxs-lookup"><span data-stu-id="6124c-147">The same principles apply for the other file types.</span></span>


```C++
IBaseFilter *pSrc = NULL, *pWaveDest = NULL, *pWriter = NULL;
IFileSinkFilter *pSink= NULL;
IGraphBuilder *pGraph;

// Create the Filter Graph Manager.
hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void**)&pGraph);

// This example omits error handling.

// Not shown: Use the System Device Enumerator to create the 
// audio capture filter.

// Add the audio capture filter to the filter graph. 
hr = pGraph->AddFilter(pSrc, L"Capture");

// Add the WavDest and the File Writer.
hr = AddFilterByCLSID(pGraph, CLSID_WavDest, L"WavDest", &pWaveDest);
hr = AddFilterByCLSID(pGraph, CLSID_FileWriter, L"File Writer", &pWriter);

// Set the file name.
hr = pWriter->QueryInterface(IID_IFileSinkFilter, (void**)&pSink);
hr = pSink->SetFileName(L"C:\\MyWavFile.wav", NULL);

// Connect the filters.
hr = ConnectFilters(pGraph, pSrc, pWaveDest);
hr = ConnectFilters(pGraph, pWaveDest, pWriter);

// Not shown: Release interface pointers.

```



<span data-ttu-id="6124c-148">Questo esempio usa la `AddFilterByCLSID` funzione descritta in [aggiungere un filtro in base a CLSID](add-a-filter-by-clsid.md)e la `ConnectFilters` funzione descritta in [connettere due filtri](connect-two-filters.md).</span><span class="sxs-lookup"><span data-stu-id="6124c-148">This example uses the `AddFilterByCLSID` function described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the `ConnectFilters` function described in [Connect Two Filters](connect-two-filters.md).</span></span> <span data-ttu-id="6124c-149">Nessuna di queste è un'API DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6124c-149">Neither of these is a DirectShow API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6124c-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6124c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6124c-151">Acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="6124c-151">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 
