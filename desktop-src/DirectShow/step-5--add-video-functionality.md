---
description: Questo argomento è il passaggio 5 dell'esercitazione Riproduzione audio/video in DirectShow.
ms.assetid: 9d7a40e0-4327-4ca3-b430-2be02f80c16f
title: 'Passaggio 5: Aggiungere funzionalità video'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968c35916f90f226305eb987058d14cc7891d250961e2b8a41a1756ec3794b1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951780"
---
# <a name="step-5-add-video-functionality"></a>Passaggio 5: Aggiungere funzionalità video

Questo argomento è il passaggio 5 dell'esercitazione [Riproduzione audio/video in DirectShow](audio-video-playback-in-directshow.md). Il codice completo è illustrato nell'argomento DirectShow [esempio di riproduzione](directshow-playback-example.md).

Per garantire che il video venga visualizzato correttamente, l'applicazione deve rispondere ai messaggi [**WM \_ PAINT**](../gdi/wm-paint.md), [**WM \_ SIZE**](../winmsg/wm-size.md)e [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md) come indicato di seguito.

### <a name="handle-wm_paint-messages"></a>Gestire i messaggi \_ WM PAINT

Quando l'applicazione riceve un [**messaggio WM \_ PAINT,**](../gdi/wm-paint.md) il renderer video potrebbe dover ridisegnare l'ultimo fotogramma video. Per il [**filtro Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR), chiamare [**IMFVideoDisplayControl::RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).


```C++
HRESULT CEVR::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pVideoDisplay)
    {
        return m_pVideoDisplay->RepaintVideo();
    }
    else
    {
        return S_OK;
    }
}
```



Per il [filtro del renderer di combinazione](video-mixing-renderer-filter-9.md) video 9 (VMR-9), chiamare [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).


```C++
HRESULT CVMR9::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



Per il [filtro del renderer di combinazione](video-mixing-renderer-filter-7.md) video 7 (VMR-7), chiamare [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).


```C++
HRESULT CVMR7::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



### <a name="handle-wm_size-messages"></a>Gestire i messaggi WM \_ SIZE

Se le dimensioni della finestra video cambiano, inviare una notifica al renderer video per ridimensionare il video. Per l'EVR, chiamare [**IMFVideoDisplayControl::SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).


```C++
HRESULT CEVR::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pVideoDisplay == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pVideoDisplay->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pVideoDisplay->SetVideoPosition(NULL, &rc);
    }
}
```



Per VMR-9, chiamare [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).


```C++
HRESULT CVMR9::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



Per VMR-7, chiamare [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).


```C++
HRESULT CVMR7::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {
        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



### <a name="handle-wm_displaychange-messages"></a>Gestire i messaggi WM \_ DISPLAYCHANGE

Se la modalità di visualizzazione cambia, è necessario inviare una notifica al filtro VMR-9 o VMR-7. Per VMR-9, chiamare [**IVMRWindowlessControl9::D isplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).


```C++
HRESULT CVMR9::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



Per VMR-7, chiamare [**IVMRWindowlessControl::D isplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).


```C++
HRESULT CVMR7::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



Non è necessario ricevere una notifica all'EVR quando cambia la modalità di visualizzazione.

Passaggio [6: Gestire gli Graph eventi](step-6--handle-graph-events.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione audio/video in DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow Esempio di riproduzione](directshow-playback-example.md)
</dt> <dt>

[Uso del filtro DirectShow EVR](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Uso del renderer di combinazione video](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
