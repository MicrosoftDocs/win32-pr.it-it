---
description: Questo argomento è il passaggio 3 della riproduzione audio/video dell'esercitazione in DirectShow.
ms.assetid: 45679c14-2671-420d-9766-61f2b2bb713a
title: 'Passaggio 3: creare il grafico del filtro'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a770ad823a2578fab88a09cc44a3c7f2be4a4ca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316328"
---
# <a name="step-3-build-the-filter-graph"></a><span data-ttu-id="3a07e-103">Passaggio 3: creare il grafico del filtro</span><span class="sxs-lookup"><span data-stu-id="3a07e-103">Step 3: Build the Filter Graph</span></span>

<span data-ttu-id="3a07e-104">Questo argomento è il passaggio 3 della [riproduzione audio/video dell'esercitazione in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="3a07e-104">This topic is step 3 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="3a07e-105">Il codice completo è illustrato nell'esempio relativo alla [riproduzione DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="3a07e-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="3a07e-106">Il passaggio successivo consiste nel creare un grafico di filtro per riprodurre il file multimediale.</span><span class="sxs-lookup"><span data-stu-id="3a07e-106">The next step is to build a filter graph to play the media file.</span></span>

### <a name="opening-a-media-file"></a><span data-ttu-id="3a07e-107">Apertura di un file multimediale</span><span class="sxs-lookup"><span data-stu-id="3a07e-107">Opening a Media File</span></span>

<span data-ttu-id="3a07e-108">Il `DShowPlayer::OpenFile` metodo apre un file multimediale per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="3a07e-108">The `DShowPlayer::OpenFile` method opens a media file for playback.</span></span> <span data-ttu-id="3a07e-109">Questo metodo esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a07e-109">This method does the following:</span></span>

1.  <span data-ttu-id="3a07e-110">Crea un nuovo grafico di filtro (vuoto).</span><span class="sxs-lookup"><span data-stu-id="3a07e-110">Creates a new (empty) filter graph.</span></span>
2.  <span data-ttu-id="3a07e-111">Chiama [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) per aggiungere un filtro di origine per il file specificato.</span><span class="sxs-lookup"><span data-stu-id="3a07e-111">Calls [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add a source filter for the specified file.</span></span>
3.  <span data-ttu-id="3a07e-112">Esegue il rendering dei flussi sul filtro di origine.</span><span class="sxs-lookup"><span data-stu-id="3a07e-112">Renders the streams on the source filter.</span></span>


```C++
HRESULT DShowPlayer::OpenFile(PCWSTR pszFileName)
{
    IBaseFilter *pSource = NULL;

    // Create a new filter graph. (This also closes the old one, if any.)
    HRESULT hr = InitializeGraph();
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the source filter to the graph.
    hr = m_pGraph->AddSourceFilter(pszFileName, NULL, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Try to render the streams.
    hr = RenderStreams(pSource);

done:
    if (FAILED(hr))
    {
        TearDownGraph();
    }
    SafeRelease(&pSource);
    return hr;
}
```



### <a name="creating-the-filter-graph-manager"></a><span data-ttu-id="3a07e-113">Creazione di Filter Graph Manager</span><span class="sxs-lookup"><span data-stu-id="3a07e-113">Creating the Filter Graph Manager</span></span>

<span data-ttu-id="3a07e-114">Il `DShowPlayer::InitializeGraph` metodo crea un nuovo grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="3a07e-114">The `DShowPlayer::InitializeGraph` method creates a new filter graph.</span></span> <span data-ttu-id="3a07e-115">Questo metodo esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a07e-115">This method does the following:</span></span>

1.  <span data-ttu-id="3a07e-116">Chiama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare una nuova istanza di [Filter Graph Manager](filter-graph-manager.md).</span><span class="sxs-lookup"><span data-stu-id="3a07e-116">Calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a new instance of the [Filter Graph Manager](filter-graph-manager.md).</span></span>
2.  <span data-ttu-id="3a07e-117">Esegue una query su Filter Graph Manager per le interfacce [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) .</span><span class="sxs-lookup"><span data-stu-id="3a07e-117">Queries the Filter Graph Manager for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interfaces.</span></span>
3.  <span data-ttu-id="3a07e-118">Chiama [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) per impostare la notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="3a07e-118">Calls [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) to set up event notification.</span></span> <span data-ttu-id="3a07e-119">Per altre informazioni, vedere [notifica degli eventi in DirectShow](event-notification-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="3a07e-119">For more information, see [Event Notification in DirectShow](event-notification-in-directshow.md).</span></span>


```C++
HRESULT DShowPlayer::InitializeGraph()
{
    TearDownGraph();

    // Create the Filter Graph Manager.
    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set up event notification.
    hr = m_pEvent->SetNotifyWindow((OAHWND)m_hwnd, WM_GRAPH_EVENT, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = STATE_STOPPED;

done:
    return hr;
}
```



### <a name="rendering-the-streams"></a><span data-ttu-id="3a07e-120">Rendering dei flussi</span><span class="sxs-lookup"><span data-stu-id="3a07e-120">Rendering the Streams</span></span>

<span data-ttu-id="3a07e-121">Il passaggio successivo consiste nel connettere il filtro di origine a uno o più filtri renderer.</span><span class="sxs-lookup"><span data-stu-id="3a07e-121">The next step is to connect the source filter to one or more renderer filters.</span></span>

<span data-ttu-id="3a07e-122">Il `DShowPlayer::RenderStreams` metodo esegue i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a07e-122">The `DShowPlayer::RenderStreams` method performs the following steps.</span></span>

1.  <span data-ttu-id="3a07e-123">Esegue una query su Filter Graph Manager per l'interfaccia [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) .</span><span class="sxs-lookup"><span data-stu-id="3a07e-123">Queries the Filter Graph Manager for the [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) interface.</span></span>
2.  <span data-ttu-id="3a07e-124">Aggiunge un filtro renderer video al grafico filtro.</span><span class="sxs-lookup"><span data-stu-id="3a07e-124">Adds a video renderer filter to the filter graph.</span></span>
3.  <span data-ttu-id="3a07e-125">Consente di aggiungere il [filtro renderer DirectSound](directsound-renderer-filter.md) al grafico di filtro per supportare la riproduzione audio.</span><span class="sxs-lookup"><span data-stu-id="3a07e-125">Adds the [DirectSound Renderer Filter](directsound-renderer-filter.md) to the filter graph, to support audio playback.</span></span> <span data-ttu-id="3a07e-126">Per ulteriori informazioni sull'aggiunta di filtri al grafico di filtro, vedere [aggiungere un filtro in base a CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="3a07e-126">For more information about adding filters to the filter graph, see [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span>
4.  <span data-ttu-id="3a07e-127">Enumera i pin di output sul filtro di origine.</span><span class="sxs-lookup"><span data-stu-id="3a07e-127">Enumerates the output pins on the source filter.</span></span> <span data-ttu-id="3a07e-128">Per ulteriori informazioni sull'enumerazione dei pin, vedere [enumerazione dei pin](enumerating-pins.md).</span><span class="sxs-lookup"><span data-stu-id="3a07e-128">For more information about enumerating pins, see [Enumerating Pins](enumerating-pins.md).</span></span>
5.  <span data-ttu-id="3a07e-129">Per ogni pin, chiama il metodo [**IFilterGraph2:: RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) .</span><span class="sxs-lookup"><span data-stu-id="3a07e-129">For each pin, calls the [**IFilterGraph2::RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) method.</span></span> <span data-ttu-id="3a07e-130">Questo metodo connette il pin di output a un filtro renderer, aggiungendo filtri intermedi se necessario, ad esempio i decodificatori.</span><span class="sxs-lookup"><span data-stu-id="3a07e-130">This method connects the output pin to a renderer filter, adding intermediate filters if needed (such as decoders).</span></span>
6.  <span data-ttu-id="3a07e-131">Chiama `CVideoRenderer::FinalizeGraph` per completare l'inizializzazione del renderer video.</span><span class="sxs-lookup"><span data-stu-id="3a07e-131">Calls `CVideoRenderer::FinalizeGraph` to finish initializing the video renderer.</span></span>
7.  <span data-ttu-id="3a07e-132">Rimuove il filtro [renderer DirectSound](directsound-renderer-filter.md) se il filtro non è connesso a un altro filtro.</span><span class="sxs-lookup"><span data-stu-id="3a07e-132">Removes the [DirectSound Renderer](directsound-renderer-filter.md) filter if that filter is not connected to another filter.</span></span> <span data-ttu-id="3a07e-133">Questo problema può verificarsi se il file di origine non contiene un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="3a07e-133">This can occur if the source file does not contain an audio stream.</span></span>


```C++
// Render the streams from a source filter. 

HRESULT DShowPlayer::RenderStreams(IBaseFilter *pSource)
{
    BOOL bRenderedAnyPin = FALSE;

    IFilterGraph2 *pGraph2 = NULL;
    IEnumPins *pEnum = NULL;
    IBaseFilter *pAudioRenderer = NULL;
    HRESULT hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&pGraph2));
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the video renderer to the graph
    hr = CreateVideoRenderer();
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the DSound Renderer to the graph.
    hr = AddFilterByCLSID(m_pGraph, CLSID_DSoundRender, 
        &pAudioRenderer, L"Audio Renderer");
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate the pins on the source filter.
    hr = pSource->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    // Loop through all the pins
    IPin *pPin;
    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {           
        // Try to render this pin. 
        // It's OK if we fail some pins, if at least one pin renders.
        HRESULT hr2 = pGraph2->RenderEx(pPin, AM_RENDEREX_RENDERTOEXISTINGRENDERERS, NULL);

        pPin->Release();
        if (SUCCEEDED(hr2))
        {
            bRenderedAnyPin = TRUE;
        }
    }

    hr = m_pVideo->FinalizeGraph(m_pGraph);
    if (FAILED(hr))
    {
        goto done;
    }

    // Remove the audio renderer, if not used.
    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(m_pGraph, pAudioRenderer, &bRemoved);

done:
    SafeRelease(&pEnum);
    SafeRelease(&pAudioRenderer);
    SafeRelease(&pGraph2);

    // If we succeeded to this point, make sure we rendered at least one 
    // stream.
    if (SUCCEEDED(hr))
    {
        if (!bRenderedAnyPin)
        {
            hr = VFW_E_CANNOT_RENDER;
        }
    }
    return hr;
}
```



<span data-ttu-id="3a07e-134">Ecco il codice per la `RemoveUnconnectedRenderer` funzione, che viene usato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="3a07e-134">Here is the code for the `RemoveUnconnectedRenderer` function, which is used in the previous example.</span></span>


```C++
HRESULT RemoveUnconnectedRenderer(IGraphBuilder *pGraph, IBaseFilter *pRenderer, BOOL *pbRemoved)
{
    IPin *pPin = NULL;

    *pbRemoved = FALSE;

    // Look for a connected input pin on the renderer.

    HRESULT hr = FindConnectedPin(pRenderer, PINDIR_INPUT, &pPin);
    SafeRelease(&pPin);

    // If this function succeeds, the renderer is connected, so we don't remove it.
    // If it fails, it means the renderer is not connected to anything, so
    // we remove it.

    if (FAILED(hr))
    {
        hr = pGraph->RemoveFilter(pRenderer);
        *pbRemoved = TRUE;
    }

    return hr;
}
```



### <a name="releasing-the-filter-graph"></a><span data-ttu-id="3a07e-135">Rilascio del grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="3a07e-135">Releasing the Filter Graph</span></span>

<span data-ttu-id="3a07e-136">Quando l'applicazione viene chiusa, deve rilasciare il grafico di filtro, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="3a07e-136">When the application exits, it must release the filter graph, as shown in the following code.</span></span>


```C++
void DShowPlayer::TearDownGraph()
{
    // Stop sending event messages
    if (m_pEvent)
    {
        m_pEvent->SetNotifyWindow((OAHWND)NULL, NULL, NULL);
    }

    SafeRelease(&m_pGraph);
    SafeRelease(&m_pControl);
    SafeRelease(&m_pEvent);

    delete m_pVideo;
    m_pVideo = NULL;

    m_state = STATE_NO_GRAPH;
}
```



<span data-ttu-id="3a07e-137">[Passaggio 4: aggiungere il renderer video](step-4--add-the-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="3a07e-137">Next: [Step 4: Add the Video Renderer](step-4--add-the-video-renderer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a07e-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a07e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a07e-139">Riproduzione audio/video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="3a07e-139">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="3a07e-140">Esempio di riproduzione DirectShow</span><span class="sxs-lookup"><span data-stu-id="3a07e-140">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="3a07e-141">Creazione del grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="3a07e-141">Building the Filter Graph</span></span>](building-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="3a07e-142">Tecniche di Graph-Building generali</span><span class="sxs-lookup"><span data-stu-id="3a07e-142">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 
