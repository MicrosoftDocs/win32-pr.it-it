---
description: Questo argomento è il passaggio 4 della riproduzione audio/video dell'esercitazione in DirectShow.
ms.assetid: 34f35a95-1981-4467-a581-46db96c05224
title: 'Passaggio 4: aggiungere il renderer video'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17a0622909525f69cf64fd374c8512a8fa9bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320050"
---
# <a name="step-4-add-the-video-renderer"></a><span data-ttu-id="9b698-103">Passaggio 4: aggiungere il renderer video</span><span class="sxs-lookup"><span data-stu-id="9b698-103">Step 4: Add the Video Renderer</span></span>

<span data-ttu-id="9b698-104">Questo argomento è il passaggio 4 della [riproduzione audio/video dell'esercitazione in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="9b698-104">This topic is step 4 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="9b698-105">Il codice completo è illustrato nell'esempio relativo alla [riproduzione DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="9b698-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="9b698-106">DirectShow fornisce diversi filtri che eseguono il rendering del video:</span><span class="sxs-lookup"><span data-stu-id="9b698-106">DirectShow provides several different filters that render video:</span></span>

-   <span data-ttu-id="9b698-107">[**Filtro renderer video migliorato**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="9b698-107">[**Enhanced Video Renderer Filter**](enhanced-video-renderer-filter.md) (EVR)</span></span>
-   <span data-ttu-id="9b698-108">[Filtro renderer video mixing 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="9b698-108">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>
-   <span data-ttu-id="9b698-109">[Filtro renderer video mixing 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="9b698-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>

<span data-ttu-id="9b698-110">Per ulteriori informazioni sulle differenze tra questi filtri, vedere [scelta del renderer video appropriato](choosing-the-right-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="9b698-110">For more information about the differences between these filters, see [Choosing the Right Video Renderer](choosing-the-right-renderer.md).</span></span>

<span data-ttu-id="9b698-111">In questa esercitazione ogni filtro renderer video è incluso in una classe che astrae alcune delle differenze tra di essi.</span><span class="sxs-lookup"><span data-stu-id="9b698-111">In this tutorial, each video renderer filter is wrapped by a class that abstracts some of the differences between them.</span></span> <span data-ttu-id="9b698-112">Queste classi derivano tutte da una classe di base astratta denominata `CVideoRenderer` .</span><span class="sxs-lookup"><span data-stu-id="9b698-112">These classes all derive from an abstract base class named `CVideoRenderer`.</span></span> <span data-ttu-id="9b698-113">La dichiarazione di `CVideoRenderer` è illustrata nel [passaggio 2: dichiarare CVideoRenderer e le classi derivate](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="9b698-113">The declaration of `CVideoRenderer` is shown in [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>

<span data-ttu-id="9b698-114">Il metodo seguente tenta di creare ogni renderer video a sua volta, a partire da EVR, quindi da VMR-9 e infine da VMR-7.</span><span class="sxs-lookup"><span data-stu-id="9b698-114">The following method tries to create each video renderer in turn, starting with the EVR, then the VMR-9, and finally the VMR-7.</span></span>


```C++
HRESULT DShowPlayer::CreateVideoRenderer()
{
    HRESULT hr = E_FAIL;

    enum { Try_EVR, Try_VMR9, Try_VMR7 };

    for (DWORD i = Try_EVR; i <= Try_VMR7; i++)
    {
        switch (i)
        {
        case Try_EVR:
            m_pVideo = new (std::nothrow) CEVR();
            break;

        case Try_VMR9:
            m_pVideo = new (std::nothrow) CVMR9();
            break;

        case Try_VMR7:
            m_pVideo = new (std::nothrow) CVMR7();
            break;
        }

        if (m_pVideo == NULL)
        {
            hr = E_OUTOFMEMORY;
            break;
        }

        hr = m_pVideo->AddToGraph(m_pGraph, m_hwnd);
        if (SUCCEEDED(hr))
        {
            break;
        }

        delete m_pVideo;
        m_pVideo = NULL;
    }
    return hr;
}

```



### <a name="evr-filter"></a><span data-ttu-id="9b698-115">Filtro EVR</span><span class="sxs-lookup"><span data-stu-id="9b698-115">EVR Filter</span></span>

<span data-ttu-id="9b698-116">Il codice seguente crea il filtro EVR e lo aggiunge al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="9b698-116">The following code creates the EVR filter and adds it to the filter graph.</span></span> <span data-ttu-id="9b698-117">La funzione `AddFilterByCLSID` usata in questo esempio è illustrata nell'argomento [aggiungere un filtro in base a CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="9b698-117">The function `AddFilterByCLSID` used in this example is shown in the topic [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span>


```C++
HRESULT CEVR::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pEVR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_EnhancedVideoRenderer, 
        &pEVR, L"EVR");

    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitializeEVR(pEVR, hwnd, &m_pVideoDisplay);
    if (FAILED(hr))
    {
        goto done;
    }

    // Note: Because IMFVideoDisplayControl is a service interface,
    // you cannot QI the pointer to get back the IBaseFilter pointer.
    // Therefore, we need to cache the IBaseFilter pointer.

    m_pEVR = pEVR;
    m_pEVR->AddRef();

done:
    SafeRelease(&pEVR);
    return hr;
}
```



<span data-ttu-id="9b698-118">La `InitializeEVR` funzione Inizializza il filtro EVR.</span><span class="sxs-lookup"><span data-stu-id="9b698-118">The `InitializeEVR` function initializes the EVR filter.</span></span> <span data-ttu-id="9b698-119">Questa funzione esegue i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="9b698-119">This function performs the following steps.</span></span>

1.  <span data-ttu-id="9b698-120">Esegue una query sul filtro per l'interfaccia [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="9b698-120">Queries the filter for the [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="9b698-121">Chiama [**IMFGetService:: GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere un puntatore all'interfaccia [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="9b698-121">Calls [**IMFGetService::GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) interface.</span></span>
3.  <span data-ttu-id="9b698-122">Chiama [**IMFVideoDisplayControl:: SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) per impostare la finestra del video.</span><span class="sxs-lookup"><span data-stu-id="9b698-122">Calls [**IMFVideoDisplayControl::SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) to set the video window.</span></span>
4.  <span data-ttu-id="9b698-123">Chiama [**IMFVideoDisplayControl:: SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) per configurare il EVR per mantenere le proporzioni video.</span><span class="sxs-lookup"><span data-stu-id="9b698-123">Calls [**IMFVideoDisplayControl::SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) to configure the EVR to preserve the video aspect ratio.</span></span>

<span data-ttu-id="9b698-124">Nel codice seguente viene illustrata la `InitializeEVR` funzione.</span><span class="sxs-lookup"><span data-stu-id="9b698-124">The following code shows the `InitializeEVR` function.</span></span>


```C++
HRESULT InitializeEVR( 
    IBaseFilter *pEVR,              // Pointer to the EVR
    HWND hwnd,                      // Clipping window
    IMFVideoDisplayControl** ppDisplayControl
    ) 
{ 
    IMFGetService *pGS = NULL;
    IMFVideoDisplayControl *pDisplay = NULL;

    HRESULT hr = pEVR->QueryInterface(IID_PPV_ARGS(&pGS)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGS->GetService(MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&pDisplay));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pDisplay->SetVideoWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pDisplay->SetAspectRatioMode(MFVideoARMode_PreservePicture);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IMFVideoDisplayControl pointer to the caller.
    *ppDisplayControl = pDisplay;
    (*ppDisplayControl)->AddRef();

done:
    SafeRelease(&pGS);
    SafeRelease(&pDisplay);
    return hr; 
} 
```



<span data-ttu-id="9b698-125">Dopo la compilazione del grafo, `DShowPlayer::RenderStreams` chiama `CVideoRenderer::FinalizeGraph` .</span><span class="sxs-lookup"><span data-stu-id="9b698-125">After the graph is built, the `DShowPlayer::RenderStreams` calls `CVideoRenderer::FinalizeGraph`.</span></span> <span data-ttu-id="9b698-126">Questo metodo esegue l'inizializzazione o la pulizia finale.</span><span class="sxs-lookup"><span data-stu-id="9b698-126">This method performs any final initialization or cleanup.</span></span> <span data-ttu-id="9b698-127">Nel codice seguente viene illustrata l' `CEVR` implementazione di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="9b698-127">The following code shows the `CEVR` implementation of this method.</span></span>


```C++
HRESULT CEVR::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pEVR == NULL)
    {
        return S_OK;
    }

    BOOL bRemoved;
    HRESULT hr = RemoveUnconnectedRenderer(pGraph, m_pEVR, &bRemoved);
    if (bRemoved)
    {
        SafeRelease(&m_pEVR);
        SafeRelease(&m_pVideoDisplay);
    }
    return hr;
}
```



<span data-ttu-id="9b698-128">Se EVR non è connesso ad altri filtri, questo metodo rimuove il EVR dal grafico.</span><span class="sxs-lookup"><span data-stu-id="9b698-128">If the EVR is not connected to any other filter, this method removes the EVR from the graph.</span></span> <span data-ttu-id="9b698-129">Questo problema può verificarsi se il file multimediale non contiene un flusso video.</span><span class="sxs-lookup"><span data-stu-id="9b698-129">This can occur if the media file does not contain a video stream.</span></span>

### <a name="vmr-9-filter"></a><span data-ttu-id="9b698-130">Filtro VMR-9</span><span class="sxs-lookup"><span data-stu-id="9b698-130">VMR-9 Filter</span></span>

<span data-ttu-id="9b698-131">Il codice seguente crea il filtro VMR-9 e lo aggiunge al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="9b698-131">The following code creates the VMR-9 filter and adds it to the filter graph.</span></span>


```C++
HRESULT CVMR9::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer9, 
        &pVMR, L"VMR-9");
    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR 
        // is connected.
        hr = InitWindowlessVMR9(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



<span data-ttu-id="9b698-132">La `InitWindowlessVMR9` funzione Inizializza VMR-9 per la modalità senza finestra.</span><span class="sxs-lookup"><span data-stu-id="9b698-132">The `InitWindowlessVMR9` function initializes the VMR-9 for windowless mode.</span></span> <span data-ttu-id="9b698-133">(Per altre informazioni sulla modalità senza finestra, vedere [modalità senza finestra VMR](vmr-windowless-mode.md)). Questa funzione esegue i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="9b698-133">(For more information about windowless mode, see [VMR Windowless Mode](vmr-windowless-mode.md).) This function performs the following steps.</span></span>

1.  <span data-ttu-id="9b698-134">Esegue una query sul filtro VMR-9 per l'interfaccia [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) .</span><span class="sxs-lookup"><span data-stu-id="9b698-134">Queries the VMR-9 filter for the [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) interface.</span></span>
2.  <span data-ttu-id="9b698-135">Chiama il metodo [**IVMRFilterConfig9:: SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) per impostare la modalità senza finestra.</span><span class="sxs-lookup"><span data-stu-id="9b698-135">Calls the [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) method to set windowless mode.</span></span>
3.  <span data-ttu-id="9b698-136">Esegue una query sul filtro VMR-9 per l'interfaccia [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="9b698-136">Queries the VMR-9 filter for the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>
4.  <span data-ttu-id="9b698-137">Chiama il metodo [**IVMRWindowlessControl9:: SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) per impostare la finestra del video.</span><span class="sxs-lookup"><span data-stu-id="9b698-137">Calls the [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) method to set the video window.</span></span>
5.  <span data-ttu-id="9b698-138">Chiama il metodo [**IVMRWindowlessControl9:: SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) per mantenere le proporzioni video.</span><span class="sxs-lookup"><span data-stu-id="9b698-138">Calls the [**IVMRWindowlessControl9::SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) method to preserve the video aspect ratio.</span></span>

<span data-ttu-id="9b698-139">Nel codice seguente viene illustrata la `InitWindowlessVMR9` funzione.</span><span class="sxs-lookup"><span data-stu-id="9b698-139">The following code shows the `InitWindowlessVMR9` function.</span></span>


```C++
HRESULT InitWindowlessVMR9( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl9** ppWC   // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig9 * pConfig = NULL; 
    IVMRWindowlessControl9 *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMR9Mode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR9ARMode_LetterBox);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



<span data-ttu-id="9b698-140">Il `CVMR9::FinalizeGraph` metodo controlla se il filtro VMR-9 è connesso e, in caso contrario, lo rimuove dal grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="9b698-140">The `CVMR9::FinalizeGraph` method checks if the VMR-9 filter is connected, and if not, removes it from the filter graph.</span></span>


```C++
HRESULT CVMR9::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



### <a name="vmr-7-filter"></a><span data-ttu-id="9b698-141">Filtro VMR-7</span><span class="sxs-lookup"><span data-stu-id="9b698-141">VMR-7 Filter</span></span>

<span data-ttu-id="9b698-142">I passaggi per il filtro VMR-7 sono quasi identici a quelli per VMR-9, ad eccezione del fatto che vengono usate le interfacce VMR-7.</span><span class="sxs-lookup"><span data-stu-id="9b698-142">The steps for the VMR-7 filter are nearly identical to those for the VMR-9, except the VMR-7 interfaces are used instead.</span></span> <span data-ttu-id="9b698-143">Il codice seguente crea il filtro VMR-7 e lo aggiunge al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="9b698-143">The following code creates the VMR-7 filter and adds it to the filter graph.</span></span>


```C++
HRESULT CVMR7::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer, 
        &pVMR, L"VMR-7");

    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR
        // is connected.
        hr = InitWindowlessVMR(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



<span data-ttu-id="9b698-144">La `InitWindowlessVMR` funzione Inizializza VMR-7 per la modalità senza finestra.</span><span class="sxs-lookup"><span data-stu-id="9b698-144">The `InitWindowlessVMR` function initializes the VMR-7 for windowless mode.</span></span> <span data-ttu-id="9b698-145">Questa funzione esegue i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="9b698-145">This function performs the following steps.</span></span>

1.  <span data-ttu-id="9b698-146">Esegue una query sul filtro VMR-7 per l'interfaccia [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) .</span><span class="sxs-lookup"><span data-stu-id="9b698-146">Queries the VMR-7 filter for the [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) interface.</span></span>
2.  <span data-ttu-id="9b698-147">Chiama il metodo [**IVMRFilterConfig:: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) per impostare la modalità senza finestra.</span><span class="sxs-lookup"><span data-stu-id="9b698-147">Calls the [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) method to set windowless mode.</span></span>
3.  <span data-ttu-id="9b698-148">Esegue una query sul filtro VMR-7 per l'interfaccia [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="9b698-148">Queries the VMR-7 filter for the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>
4.  <span data-ttu-id="9b698-149">Chiama il metodo [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) per impostare la finestra del video.</span><span class="sxs-lookup"><span data-stu-id="9b698-149">Calls the [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) method to set the video window.</span></span>
5.  <span data-ttu-id="9b698-150">Chiama il metodo [**IVMRWindowlessControl:: SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) per mantenere le proporzioni video.</span><span class="sxs-lookup"><span data-stu-id="9b698-150">Calls the [**IVMRWindowlessControl::SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) method to preserve the video aspect ratio.</span></span>

<span data-ttu-id="9b698-151">Nel codice seguente viene illustrata la `InitWindowlessVMR` funzione.</span><span class="sxs-lookup"><span data-stu-id="9b698-151">The following code shows the `InitWindowlessVMR` function.</span></span>


```C++
HRESULT InitWindowlessVMR( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl** ppWC    // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig* pConfig = NULL; 
    IVMRWindowlessControl *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR_ARMODE_LETTER_BOX);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



<span data-ttu-id="9b698-152">Il `CVMR7::FinalizeGraph` metodo controlla se il filtro VMR-7 è connesso e, in caso contrario, lo rimuove dal grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="9b698-152">The `CVMR7::FinalizeGraph` method checks if the VMR-7 filter is connected, and if not, removes it from the filter graph.</span></span>


```C++
HRESULT CVMR7::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="9b698-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b698-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b698-154">Esempio di riproduzione DirectShow</span><span class="sxs-lookup"><span data-stu-id="9b698-154">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="9b698-155">Uso del filtro EVR DirectShow</span><span class="sxs-lookup"><span data-stu-id="9b698-155">Using the DirectShow EVR Filter</span></span>](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[<span data-ttu-id="9b698-156">Uso del renderer video mixing</span><span class="sxs-lookup"><span data-stu-id="9b698-156">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
