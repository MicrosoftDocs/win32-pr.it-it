---
description: Questo argomento è il passaggio 4 dell'esercitazione Riproduzione audio/video in DirectShow.
ms.assetid: 34f35a95-1981-4467-a581-46db96c05224
title: 'Passaggio 4: Aggiungere il renderer video'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2d73dce5bba34f92c8df59cd9730ef1e25b57b9757039d9bda5c2e4432d734
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051411"
---
# <a name="step-4-add-the-video-renderer"></a>Passaggio 4: Aggiungere il renderer video

Questo argomento è il passaggio 4 dell'esercitazione [Riproduzione audio/video in DirectShow](audio-video-playback-in-directshow.md). Il codice completo è illustrato nell'argomento DirectShow [Esempio di riproduzione](directshow-playback-example.md).

DirectShow offre diversi filtri che eseguono il rendering del video:

-   [**Filtro EVR (Enhanced Video Renderer Filter)**](enhanced-video-renderer-filter.md)
-   [Filtro del renderer di combinazione video 9](video-mixing-renderer-filter-9.md) (VMR-9)
-   [Filtro del renderer di combinazione video 7](video-mixing-renderer-filter-7.md) (VMR-7)

Per altre informazioni sulle differenze tra questi filtri, vedere [Scelta del renderer video giusto.](choosing-the-right-renderer.md)

In questa esercitazione viene eseguito il wrapping di ogni filtro del renderer video da una classe che astrae alcune delle differenze tra di essi. Tutte queste classi derivano da una classe di base astratta denominata `CVideoRenderer` . La dichiarazione di `CVideoRenderer` è illustrata in [Passaggio 2: Dichiarare CVideoRenderer e le classi derivate](step-2--declare-cvideorenderer-and-derived-classes.md).

Il metodo seguente tenta di creare ogni renderer video a turno, a partire da EVR, quindi vmr-9 e infine VMR-7.


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



### <a name="evr-filter"></a>Filtro EVR

Il codice seguente crea il filtro EVR e lo aggiunge al grafico dei filtri. La funzione `AddFilterByCLSID` usata in questo esempio è illustrata nell'argomento Aggiungere un filtro in base al [CLSID](add-a-filter-by-clsid.md).


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



La `InitializeEVR` funzione inizializza il filtro EVR. Questa funzione esegue i passaggi seguenti.

1.  Esegue una query sul filtro per [**l'interfaccia IMFGetService.**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)
2.  Chiama [**IMFGetService::GetService per**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) ottenere un [**puntatore all'interfaccia IMFVideoDisplayControl.**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol)
3.  Chiama [**IMFVideoDisplayControl::SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) per impostare la finestra video.
4.  Chiama [**IMFVideoDisplayControl::SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) per configurare EVR in modo da mantenere le proporzioni video.

Il codice seguente illustra la `InitializeEVR` funzione .


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



Dopo aver compilato il grafo, `DShowPlayer::RenderStreams` chiama `CVideoRenderer::FinalizeGraph` . Questo metodo esegue qualsiasi inizializzazione o pulizia finale. Nel codice seguente viene illustrata `CEVR` l'implementazione di questo metodo.


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



Se l'EVR non è connesso ad altri filtri, questo metodo rimuove l'EVR dal grafo. Ciò può verificarsi se il file multimediale non contiene un flusso video.

### <a name="vmr-9-filter"></a>Filtro VMR-9

Il codice seguente crea il filtro VMR-9 e lo aggiunge al grafico dei filtri.


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



La `InitWindowlessVMR9` funzione inizializza VMR-9 per la modalità senza finestra. Per altre informazioni sulla modalità senza finestra, vedere [Modalità senza finestra di VMR.](vmr-windowless-mode.md) Questa funzione esegue i passaggi seguenti.

1.  Esegue una query sul filtro VMR-9 per [**l'interfaccia IVMRFilterConfig9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9)
2.  Chiama il [**metodo IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) per impostare la modalità senza finestra.
3.  Esegue una query sul filtro VMR-9 per [**l'interfaccia IVMRWindowlessControl9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9)
4.  Chiama il [**metodo IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) per impostare la finestra video.
5.  Chiama il [**metodo IVMRWindowlessControl9::SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) per mantenere le proporzioni del video.

Il codice seguente illustra la `InitWindowlessVMR9` funzione .


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



Il `CVMR9::FinalizeGraph` metodo controlla se il filtro VMR-9 è connesso e, in caso contrario, lo rimuove dal grafico dei filtri.


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



### <a name="vmr-7-filter"></a>Filtro VMR-7

I passaggi per il filtro VMR-7 sono quasi identici a quelli per VMR-9, ad eccezione delle interfacce VMR-7. Il codice seguente crea il filtro VMR-7 e lo aggiunge al grafico dei filtri.


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



La `InitWindowlessVMR` funzione inizializza VMR-7 per la modalità senza finestra. Questa funzione esegue i passaggi seguenti.

1.  Esegue una query sul filtro VMR-7 per [**l'interfaccia IVMRFilterConfig.**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig)
2.  Chiama il [**metodo IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) per impostare la modalità senza finestra.
3.  Esegue una query sul filtro VMR-7 per [**l'interfaccia IVMRWindowlessControl.**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol)
4.  Chiama il [**metodo IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) per impostare la finestra video.
5.  Chiama il [**metodo IVMRWindowlessControl::SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) per mantenere le proporzioni del video.

Il codice seguente illustra la `InitWindowlessVMR` funzione .


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



Il `CVMR7::FinalizeGraph` metodo controlla se il filtro VMR-7 è connesso e, in caso contrario, lo rimuove dal grafico dei filtri.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Esempio di riproduzione](directshow-playback-example.md)
</dt> <dt>

[Uso del DirectShow EVR](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Uso del renderer di combinazione di video](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
