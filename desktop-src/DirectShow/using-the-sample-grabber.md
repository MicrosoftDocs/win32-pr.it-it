---
description: Il filtro Grabber di esempio è un filtro di trasformazione che può essere usato per estrarre gli esempi di supporti da un flusso mentre passano attraverso il grafico dei filtri.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Uso del grabber di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4886c796691e83e02b58ddea129d60d5004c9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314384"
---
# <a name="using-the-sample-grabber"></a><span data-ttu-id="20c4e-103">Uso del grabber di esempio</span><span class="sxs-lookup"><span data-stu-id="20c4e-103">Using the Sample Grabber</span></span>

<span data-ttu-id="20c4e-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="20c4e-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="20c4e-105">Il filtro [**grabber di esempio**](sample-grabber-filter.md) è un filtro di trasformazione che può essere usato per estrarre gli esempi di supporti da un flusso mentre passano attraverso il grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="20c4e-105">The [**Sample Grabber**](sample-grabber-filter.md) filter is a transform filter that can be used to grab media samples from a stream as they pass through the filter graph.</span></span>

<span data-ttu-id="20c4e-106">Se si vuole semplicemente estrarre una bitmap da un file video, è più semplice usare l'oggetto [mediadet (Media Detector)](media-detector--mediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="20c4e-106">If you simply want to grab a bitmap from a video file, it is easier to use the [Media Detector (MediaDet)](media-detector--mediadet.md) object.</span></span> <span data-ttu-id="20c4e-107">Per informazioni dettagliate, vedere [acquisizione di un frame di poster](grabbing-a-poster-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="20c4e-107">See [Grabbing a Poster Frame](grabbing-a-poster-frame.md) for details.</span></span> <span data-ttu-id="20c4e-108">Il grabber di esempio è più flessibile, tuttavia, perché funziona con quasi tutti i tipi di supporto (vedere [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) per le poche eccezioni) e offre un maggiore controllo per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="20c4e-108">The Sample Grabber is more flexible, however, because it works with nearly any media type (see [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) for the few exceptions), and offers more control to the application.</span></span>

-   [<span data-ttu-id="20c4e-109">Creare il gestore del grafico del filtro</span><span class="sxs-lookup"><span data-stu-id="20c4e-109">Create the Filter Graph Manager</span></span>](#create-the-filter-graph-manager)
-   [<span data-ttu-id="20c4e-110">Aggiungere il grabber di esempio al grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="20c4e-110">Add the Sample Grabber to the Filter Graph</span></span>](#add-the-sample-grabber-to-the-filter-graph)
-   [<span data-ttu-id="20c4e-111">Imposta il tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="20c4e-111">Set the Media Type</span></span>](#set-the-media-type)
-   [<span data-ttu-id="20c4e-112">Creare il grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="20c4e-112">Build the Filter Graph</span></span>](#build-the-filter-graph)
-   [<span data-ttu-id="20c4e-113">Eseguire il grafo</span><span class="sxs-lookup"><span data-stu-id="20c4e-113">Run the Graph</span></span>](#run-the-graph)
-   [<span data-ttu-id="20c4e-114">Acquisire l'esempio</span><span class="sxs-lookup"><span data-stu-id="20c4e-114">Grab the Sample</span></span>](#grab-the-sample)
-   [<span data-ttu-id="20c4e-115">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="20c4e-115">Example Code</span></span>](#example-code)
-   [<span data-ttu-id="20c4e-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="20c4e-116">Related topics</span></span>](#related-topics)

## <a name="create-the-filter-graph-manager"></a><span data-ttu-id="20c4e-117">Creare il gestore del grafico del filtro</span><span class="sxs-lookup"><span data-stu-id="20c4e-117">Create the Filter Graph Manager</span></span>

<span data-ttu-id="20c4e-118">Per iniziare, creare la [gestione del grafo del filtro](filter-graph-manager.md) e la query per le interfacce [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) .</span><span class="sxs-lookup"><span data-stu-id="20c4e-118">To start, create the [Filter Graph Manager](filter-graph-manager.md) and query for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interfaces.</span></span>


```C++
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;


    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="add-the-sample-grabber-to-the-filter-graph"></a><span data-ttu-id="20c4e-119">Aggiungere il grabber di esempio al grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="20c4e-119">Add the Sample Grabber to the Filter Graph</span></span>

<span data-ttu-id="20c4e-120">Creare un'istanza del filtro Grabber di esempio e addit al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="20c4e-120">Create an instance of the Sample Grabber filter and addit to the filter graph.</span></span> <span data-ttu-id="20c4e-121">Eseguire una query sul filtro Grabber di esempio per l'interfaccia [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="20c4e-121">Query the Sample Grabber filter for the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>


```C++
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;


    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="set-the-media-type"></a><span data-ttu-id="20c4e-122">Imposta il tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="20c4e-122">Set the Media Type</span></span>

<span data-ttu-id="20c4e-123">Quando si crea il grabber di esempio per la prima volta, non è disponibile alcun tipo di supporto preferito.</span><span class="sxs-lookup"><span data-stu-id="20c4e-123">When you first create the Sample Grabber, it has no preferred media type.</span></span> <span data-ttu-id="20c4e-124">Ciò significa che è possibile connettersi praticamente a qualsiasi filtro nel grafico, ma non si avrà alcun controllo sul tipo di dati ricevuti.</span><span class="sxs-lookup"><span data-stu-id="20c4e-124">This means you can connect to almost any filter in the graph, but you would have no control over the type of data that it received.</span></span> <span data-ttu-id="20c4e-125">Prima di creare il resto del grafo, è necessario impostare un tipo di supporto per il grabber di esempio, chiamando il metodo [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="20c4e-125">Before building the rest of the graph, therefore, you must set a media type for the Sample Grabber, by calling the [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) method.</span></span>

<span data-ttu-id="20c4e-126">Quando si connette il grabber di esempio, questo tipo di supporto viene confrontato con il tipo di supporto offerto dall'altro filtro.</span><span class="sxs-lookup"><span data-stu-id="20c4e-126">When the Sample Grabber connects, it will compare this media type against the media type offered by the other filter.</span></span> <span data-ttu-id="20c4e-127">Gli unici campi che controlla sono il tipo principale, il sottotipo e il tipo di formato.</span><span class="sxs-lookup"><span data-stu-id="20c4e-127">The only fields that it checks are the major type, subtype, and format type.</span></span> <span data-ttu-id="20c4e-128">Per uno di questi valori, il valore \_ null del GUID indica che "accetta qualsiasi valore".</span><span class="sxs-lookup"><span data-stu-id="20c4e-128">For any of these, the value GUID\_NULL means "accept any value."</span></span> <span data-ttu-id="20c4e-129">Nella maggior parte dei casi, è preferibile impostare il tipo e il sottotipo principali.</span><span class="sxs-lookup"><span data-stu-id="20c4e-129">Most of the time, you will want to set the major type and subtype.</span></span> <span data-ttu-id="20c4e-130">Il codice seguente, ad esempio, specifica un video RGB a 24 bit non compresso:</span><span class="sxs-lookup"><span data-stu-id="20c4e-130">For example, the following code specifies uncompressed 24-bit RGB video:</span></span>


```C++
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="build-the-filter-graph"></a><span data-ttu-id="20c4e-131">Creare il grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="20c4e-131">Build the Filter Graph</span></span>

<span data-ttu-id="20c4e-132">A questo punto è possibile compilare il resto del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="20c4e-132">Now you can build the rest of the filter graph.</span></span> <span data-ttu-id="20c4e-133">Poiché il grabber di esempio si connetterà solo usando il tipo di supporto specificato, questo consente di sfruttare i meccanismi di [connessione intelligente](intelligent-connect.md) del gestore del grafico dei filtri quando si compila il grafo.</span><span class="sxs-lookup"><span data-stu-id="20c4e-133">Because the Sample Grabber will only connect using the media type you have specified, this lets you take advantage of the Filter Graph Manager's [Intelligent Connect](intelligent-connect.md) mechanisms when you build the graph.</span></span>

<span data-ttu-id="20c4e-134">Se, ad esempio, è stato specificato un video non compresso, è possibile connettere un filtro di origine al grabber di esempio e il componente di gestione del filtro del grafico aggiungerà automaticamente il parser di file e il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="20c4e-134">For example, if you specified uncompressed video, you can connect a source filter to the Sample Grabber, and the Filter Graph Manager will automatically add the file parser and the decoder.</span></span> <span data-ttu-id="20c4e-135">Nell'esempio seguente viene usata la funzione helper ConnectFilters, elencata in [Connect Two filters](connect-two-filters.md):</span><span class="sxs-lookup"><span data-stu-id="20c4e-135">The following example uses the ConnectFilters helper function, which is listed in [Connect Two Filters](connect-two-filters.md):</span></span>


```C++
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;


    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }
```





<span data-ttu-id="20c4e-136">Il grabber di esempio è un filtro di trasformazione, quindi il pin di output deve essere connesso a un altro filtro.</span><span class="sxs-lookup"><span data-stu-id="20c4e-136">The Sample Grabber is a transform filter, so the output pin must be connected to another filter.</span></span> <span data-ttu-id="20c4e-137">Spesso è possibile semplicemente rimuovere gli esempi una volta completata l'operazione.</span><span class="sxs-lookup"><span data-stu-id="20c4e-137">Often, you may simply want to discard the samples after you are done with them.</span></span> <span data-ttu-id="20c4e-138">In tal caso, connettere il grabber di esempio al [**filtro renderer null**](null-renderer-filter.md), che elimina i dati ricevuti.</span><span class="sxs-lookup"><span data-stu-id="20c4e-138">In that case, connect the Sample Grabber to the [**Null Renderer Filter**](null-renderer-filter.md), which discards the data that it receives.</span></span>

<span data-ttu-id="20c4e-139">Nell'esempio seguente viene connesso il grabber di esempio al filtro renderer null:</span><span class="sxs-lookup"><span data-stu-id="20c4e-139">The following example connects the Sample Grabber to the Null Renderer filter:</span></span>


```C++
    IBaseFilter *pNullF = NULL;


    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }
```





<span data-ttu-id="20c4e-140">Tenere presente che l'inserimento del grabber di esempio tra un decodificatore video e il renderer video può danneggiare significativamente le prestazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="20c4e-140">Be aware that placing the Sample Grabber between a video decoder and the video renderer can significantly hurt rendering performance.</span></span> <span data-ttu-id="20c4e-141">Il grabber di esempio è un filtro Trans-on-Place, che indica che il buffer di output è uguale al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="20c4e-141">The Sample Grabber is a trans-in-place filter, which means the output buffer is the same as the input buffer.</span></span> <span data-ttu-id="20c4e-142">Per il rendering video, è probabile che il buffer di output si trovi nella scheda grafica, in cui le operazioni di lettura sono molto più lente, rispetto alle operazioni di lettura nella memoria principale.</span><span class="sxs-lookup"><span data-stu-id="20c4e-142">For video rendering, the output buffer is likely to be located on the graphics card, where read operations are much slower, compared with read operations in main memory.</span></span>

## <a name="run-the-graph"></a><span data-ttu-id="20c4e-143">Eseguire il grafo</span><span class="sxs-lookup"><span data-stu-id="20c4e-143">Run the Graph</span></span>

<span data-ttu-id="20c4e-144">Il grabber di esempio opera in una delle due modalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="20c4e-144">The Sample Grabber operates in one of two modes:</span></span>

-   <span data-ttu-id="20c4e-145">La modalità di buffering esegue una copia di ogni esempio prima di consegnare l'esempio downstream.</span><span class="sxs-lookup"><span data-stu-id="20c4e-145">Buffering mode makes a copy of each sample before delivering the sample downstream.</span></span>
-   <span data-ttu-id="20c4e-146">La modalità di callback richiama una funzione di callback definita dall'applicazione su ogni esempio.</span><span class="sxs-lookup"><span data-stu-id="20c4e-146">Callback mode invokes an application-defined callback function on each sample.</span></span>

<span data-ttu-id="20c4e-147">Questo articolo descrive la modalità di buffering.</span><span class="sxs-lookup"><span data-stu-id="20c4e-147">This article describes buffering mode.</span></span> <span data-ttu-id="20c4e-148">Prima di utilizzare la modalità di callback, tenere presente che la funzione di callback deve essere piuttosto limitata.</span><span class="sxs-lookup"><span data-stu-id="20c4e-148">(Before using callback mode, be aware that the callback function must be quite limited.</span></span> <span data-ttu-id="20c4e-149">In caso contrario, può ridurre drasticamente le prestazioni o anche causare deadlock.</span><span class="sxs-lookup"><span data-stu-id="20c4e-149">Otherwise, it can drastically reduce performance or even cause deadlocks.</span></span> <span data-ttu-id="20c4e-150">Per ulteriori informazioni, vedere [**ISampleGrabber:: secallback**](isamplegrabber-setcallback.md). Per attivare la modalità di buffering, chiamare il metodo [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) con il valore **true**.</span><span class="sxs-lookup"><span data-stu-id="20c4e-150">For more information, see [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).) To activate buffering mode, call the [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) method with the value **TRUE**.</span></span>

<span data-ttu-id="20c4e-151">Facoltativamente, chiamare il metodo [**ISampleGrabber:: SetOneShot**](isamplegrabber-setoneshot.md) con il valore **true**.</span><span class="sxs-lookup"><span data-stu-id="20c4e-151">Optionally, call the [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md) method with the value **TRUE**.</span></span> <span data-ttu-id="20c4e-152">In questo modo, l'grabber di esempio si arresta dopo la ricezione del primo esempio multimediale, che risulta utile se si desidera acquisire un singolo frame dal flusso.</span><span class="sxs-lookup"><span data-stu-id="20c4e-152">This causes the Sample Grabber to halt after it receives the first media sample, which is useful if you want to grab a single frame from the stream.</span></span> <span data-ttu-id="20c4e-153">Cercare l'ora desiderata, eseguire il grafo e attendere l'evento di [**\_ completamento della EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="20c4e-153">Seek to the desired time, run the graph, and wait for the [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="20c4e-154">Si noti che il livello di accuratezza del frame dipende dall'origine.</span><span class="sxs-lookup"><span data-stu-id="20c4e-154">Note that the level of frame accuracy depends on the source.</span></span> <span data-ttu-id="20c4e-155">Ad esempio, la ricerca di un file MPEG spesso non è accurata per i frame.</span><span class="sxs-lookup"><span data-stu-id="20c4e-155">For example, seeking an MPEG file is often not frame accurate.</span></span>

<span data-ttu-id="20c4e-156">Per eseguire il grafico il più rapidamente possibile, attivare il clock del grafico come descritto in [impostazione del clock del grafico](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="20c4e-156">To run the graph as fast as possible, turn of the graph clock as described in [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

<span data-ttu-id="20c4e-157">Nell'esempio seguente viene abilitata la modalità monofase e la modalità di memorizzazione nel buffer, viene eseguito il grafico del filtro e viene atteso il completamento.</span><span class="sxs-lookup"><span data-stu-id="20c4e-157">The following example enables one-shot mode and buffering mode, runs the filter graph, and waits for completion.</span></span>


```C++
    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);
```



## <a name="grab-the-sample"></a><span data-ttu-id="20c4e-158">Acquisire l'esempio</span><span class="sxs-lookup"><span data-stu-id="20c4e-158">Grab the Sample</span></span>

<span data-ttu-id="20c4e-159">In modalità di memorizzazione nel buffer, il grabber di esempio archivia una copia di ogni esempio.</span><span class="sxs-lookup"><span data-stu-id="20c4e-159">In buffering mode, the Sample Grabber stores a copy of every sample.</span></span> <span data-ttu-id="20c4e-160">Il metodo [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) copia il buffer in una matrice allocata dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="20c4e-160">The [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method copies the buffer into a caller-allocated array.</span></span> <span data-ttu-id="20c4e-161">Per determinare le dimensioni della matrice necessaria, chiamare prima **GetCurrentBuffer** con un puntatore **null** per l'indirizzo di matrice.</span><span class="sxs-lookup"><span data-stu-id="20c4e-161">To determine the size of the array that is needed, first call **GetCurrentBuffer** with a **NULL** pointer for the array address.</span></span> <span data-ttu-id="20c4e-162">Quindi allocare la matrice e chiamare il metodo una seconda volta per copiare il buffer.</span><span class="sxs-lookup"><span data-stu-id="20c4e-162">Then allocate the array and call the method a second time to copy the buffer.</span></span> <span data-ttu-id="20c4e-163">Nell'esempio seguente sono illustrati i passaggi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="20c4e-163">The following example shows these steps.</span></span>


```C++
    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }
```



<span data-ttu-id="20c4e-164">È necessario avere a disposizione il formato esatto dei dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="20c4e-164">You will need to know the exact format of the data in the buffer.</span></span> <span data-ttu-id="20c4e-165">Per ottenere queste informazioni, chiamare il metodo [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="20c4e-165">To get this information, call the [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) method.</span></span> <span data-ttu-id="20c4e-166">Questo metodo compila una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) con il formato.</span><span class="sxs-lookup"><span data-stu-id="20c4e-166">This method fills in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure with the format.</span></span>

<span data-ttu-id="20c4e-167">Per un flusso video non compresso, le informazioni sul formato sono contenute in una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="20c4e-167">For an uncompressed video stream, the format information is contained in a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="20c4e-168">Nell'esempio seguente viene illustrato come ottenere le informazioni sul formato per un flusso video non compresso.</span><span class="sxs-lookup"><span data-stu-id="20c4e-168">The following example shows how to get the format information for an uncompressed video stream.</span></span>


```C++
    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }
```



> [!Note]  
> <span data-ttu-id="20c4e-169">Il grabber di esempio non supporta [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="20c4e-169">The Sample Grabber does not support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span>

 

## <a name="example-code"></a><span data-ttu-id="20c4e-170">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="20c4e-170">Example Code</span></span>

<span data-ttu-id="20c4e-171">Ecco il codice completo per gli esempi precedenti.</span><span class="sxs-lookup"><span data-stu-id="20c4e-171">Here is the complete code for the previous examples.</span></span>

> [!Note]  
> <span data-ttu-id="20c4e-172">Questo esempio usa la funzione [SafeRelease](../medfound/saferelease.md) per rilasciare i puntatori a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="20c4e-172">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 


```C++
#include <windows.h>
#include <dshow.h>
#include "qedit.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}



HRESULT WriteBitmap(PCWSTR, BITMAPINFOHEADER*, size_t, BYTE*, size_t);

HRESULT GrabVideoBitmap(PCWSTR pszVideoFile, PCWSTR pszBitmapFile)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    IBaseFilter *pNullF = NULL;

    BYTE *pBuffer = NULL;

    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }

    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }

    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);

    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->GetConnectedMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }

    FreeMediaType(mt);

done:
    CoTaskMemFree(pBuffer);
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    SafeRelease(&pNullF);
    SafeRelease(&pSourceF);
    SafeRelease(&pGrabber);
    SafeRelease(&pGrabberF);
    SafeRelease(&pControl);
    SafeRelease(&pEvent);
    SafeRelease(&pGraph);
    return hr;
};

// Writes a bitmap file
//  pszFileName:  Output file name.
//  pBMI:         Bitmap format information (including pallete).
//  cbBMI:        Size of the BITMAPINFOHEADER, including palette, if present.
//  pData:        Pointer to the bitmap bits.
//  cbData        Size of the bitmap, in bytes.

HRESULT WriteBitmap(PCWSTR pszFileName, BITMAPINFOHEADER *pBMI, size_t cbBMI,
    BYTE *pData, size_t cbData)
{
    HANDLE hFile = CreateFile(pszFileName, GENERIC_WRITE, 0, NULL, 
        CREATE_ALWAYS, 0, NULL);
    if (hFile == NULL)
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }

    BITMAPFILEHEADER bmf = { };

    bmf.bfType = &#39;MB&#39;;
    bmf.bfSize = cbBMI+ cbData + sizeof(bmf); 
    bmf.bfOffBits = sizeof(bmf) + cbBMI; 

    DWORD cbWritten = 0;
    BOOL result = WriteFile(hFile, &bmf, sizeof(bmf), &cbWritten, NULL);
    if (result)
    {
        result = WriteFile(hFile, pBMI, cbBMI, &cbWritten, NULL);
    }
    if (result)
    {
        result = WriteFile(hFile, pData, cbData, &cbWritten, NULL);
    }

    HRESULT hr = result ? S_OK : HRESULT_FROM_WIN32(GetLastError());

    CloseHandle(hFile);

    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="20c4e-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="20c4e-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20c4e-174">Uso dei servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="20c4e-174">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 
