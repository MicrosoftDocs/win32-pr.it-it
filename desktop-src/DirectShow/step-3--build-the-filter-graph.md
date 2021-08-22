---
description: Questo argomento è il passaggio 3 dell'esercitazione Riproduzione audio/video in DirectShow.
ms.assetid: 45679c14-2671-420d-9766-61f2b2bb713a
title: 'Passaggio 3: Compilare il filtro Graph'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad4903e08b19e15721c8b62f130261bb4d05fcd94d544380b2e501f56d60704d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072505"
---
# <a name="step-3-build-the-filter-graph"></a>Passaggio 3: Compilare il filtro Graph

Questo argomento è il passaggio 3 dell'esercitazione [Riproduzione audio/video in DirectShow](audio-video-playback-in-directshow.md). Il codice completo è illustrato nell'argomento DirectShow [Esempio di riproduzione](directshow-playback-example.md).

Il passaggio successivo consiste nel creare un grafico di filtro per riprodurre il file multimediale.

### <a name="opening-a-media-file"></a>Apertura di un file multimediale

Il `DShowPlayer::OpenFile` metodo apre un file multimediale per la riproduzione. Questo metodo esegue le operazioni seguenti:

1.  Crea un nuovo grafico di filtro (vuoto).
2.  Chiama [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) per aggiungere un filtro di origine per il file specificato.
3.  Esegue il rendering dei flussi nel filtro di origine.


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



### <a name="creating-the-filter-graph-manager"></a>Creazione del filtro Graph Manager

Il `DShowPlayer::InitializeGraph` metodo crea un nuovo grafico di filtro. Questo metodo esegue le operazioni seguenti:

1.  Chiama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare una nuova istanza di [Filter Graph Manager.](filter-graph-manager.md)
2.  Esegue una query Graph Gestione filtri per [**le interfacce IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) [**e IMediaEventEx.**](/windows/desktop/api/Control/nn-control-imediaeventex)
3.  Chiama [**IMediaEventEx::SetNotifyWindow per**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) configurare la notifica degli eventi. Per altre informazioni, vedere [Notifica degli eventi in DirectShow](event-notification-in-directshow.md).


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



### <a name="rendering-the-streams"></a>Rendering del Flussi

Il passaggio successivo consiste nel connettere il filtro di origine a uno o più filtri renderer.

Il `DShowPlayer::RenderStreams` metodo esegue i passaggi seguenti.

1.  Esegue una query su Filter Graph Manager per [**l'interfaccia IFilterGraph2.**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
2.  Aggiunge un filtro del renderer video al grafico dei filtri.
3.  Aggiunge il [filtro del renderer DirectSound](directsound-renderer-filter.md) al grafico dei filtri per supportare la riproduzione audio. Per altre informazioni sull'aggiunta di filtri al grafico dei filtri, vedere [Aggiungere un filtro in base a CLSID.](add-a-filter-by-clsid.md)
4.  Enumera i segnaposto di output nel filtro di origine. Per altre informazioni sull'enumerazione dei pin, vedere [Enumerazione dei pin.](enumerating-pins.md)
5.  Per ogni pin, chiama il [**metodo IFilterGraph2::RenderEx.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) Questo metodo connette il pin di output a un filtro renderer, aggiungendo filtri intermedi, se necessario(ad esempio decodificatori).
6.  Chiama `CVideoRenderer::FinalizeGraph` per completare l'inizializzazione del renderer video.
7.  Rimuove il [filtro del renderer DirectSound](directsound-renderer-filter.md) se tale filtro non è connesso a un altro filtro. Ciò può verificarsi se il file di origine non contiene un flusso audio.


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



Di seguito è riportato il codice `RemoveUnconnectedRenderer` per la funzione , usato nell'esempio precedente.


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



### <a name="releasing-the-filter-graph"></a>Rilascio del filtro Graph

Quando l'applicazione viene chiusa, deve rilasciare il grafico del filtro, come illustrato nel codice seguente.


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



Passaggio [4: Aggiungere il renderer video](step-4--add-the-video-renderer.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione audio/video in DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow Esempio di riproduzione](directshow-playback-example.md)
</dt> <dt>

[Compilazione del filtro Graph](building-the-filter-graph.md)
</dt> <dt>

[Tecniche Graph-Building generali](general-graph-building-techniques.md)
</dt> </dl>

 

 
