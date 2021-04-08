---
description: Questo argomento è il passaggio 6 dell'esercitazione come riprodurre file multimediali con Media Foundation.
ms.assetid: e2e3e95b-41b2-45fb-b495-0e700220e5f5
title: 'Passaggio 6: controllare la riproduzione'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdfecea3484ac6b06cc44e23fd3bd1b3235324e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880054"
---
# <a name="step-6-control-playback"></a>Passaggio 6: controllare la riproduzione

Questo argomento è il passaggio 6 dell'esercitazione [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md). Il codice completo è illustrato nell'esempio relativo alla [riproduzione della sessione multimediale](media-session-playback-example.md).

In questo argomento sono incluse le sezioni seguenti:

-   [Avvio della riproduzione](#starting-playback)
-   [Sospensione della riproduzione](#pausing-playback)
-   [Arresto della riproduzione](#stopping-playback)
-   [Ridisegno della finestra video](#repainting-the-video-window)
-   [Ridimensionamento della finestra video](#resizing-the-video-window)
-   [Argomenti correlati](#related-topics)

## <a name="starting-playback"></a>Avvio della riproduzione

Per avviare la riproduzione, chiamare [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start). Nel codice seguente viene illustrato come avviare dalla posizione di riproduzione corrente.


```C++
//  Start playback from the current position. 
HRESULT CPlayer::StartPlayback()
{
    assert(m_pSession != NULL);

    PROPVARIANT varStart;
    PropVariantInit(&varStart);

    HRESULT hr = m_pSession->Start(&GUID_NULL, &varStart);
    if (SUCCEEDED(hr))
    {
        // Note: Start is an asynchronous operation. However, we
        // can treat our state as being already started. If Start
        // fails later, we'll get an MESessionStarted event with
        // an error code, and we will update our state then.
        m_state = Started;
    }
    PropVariantClear(&varStart);
    return hr;
}

//  Start playback from paused or stopped.
HRESULT CPlayer::Play()
{
    if (m_state != Paused && m_state != Stopped)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL || m_pSource == NULL)
    {
        return E_UNEXPECTED;
    }
    return StartPlayback();
}

```



Il metodo [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) può inoltre specificare una posizione iniziale relativa all'inizio del file. Per ulteriori informazioni, vedere l'argomento di riferimento per le API.

## <a name="pausing-playback"></a>Sospensione della riproduzione

Per sospendere la riproduzione, chiamare [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).


```C++
//  Pause playback.
HRESULT CPlayer::Pause()    
{
    if (m_state != Started)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL || m_pSource == NULL)
    {
        return E_UNEXPECTED;
    }

    HRESULT hr = m_pSession->Pause();
    if (SUCCEEDED(hr))
    {
        m_state = Paused;
    }

    return hr;
}
```



## <a name="stopping-playback"></a>Arresto della riproduzione

Per arrestare la riproduzione, chiamare [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop). Mentre la riproduzione viene arrestata, l'immagine video viene deselezionata e la finestra video viene disegnata con il colore di sfondo (nero per impostazione predefinita).


```C++
// Stop playback.
HRESULT CPlayer::Stop()
{
    if (m_state != Started && m_state != Paused)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL)
    {
        return E_UNEXPECTED;
    }

    HRESULT hr = m_pSession->Stop();
    if (SUCCEEDED(hr))
    {
        m_state = Stopped;
    }
    return hr;
}
```



## <a name="repainting-the-video-window"></a>Ridisegno della finestra video

Il [renderer video avanzato](enhanced-video-renderer.md) (EVR) consente di disegnare il video nella finestra specificata dall'applicazione. Questo problema si verifica in un thread separato e, nella maggior parte dei casi, l'applicazione non deve gestire questo processo. Se la riproduzione viene sospesa o arrestata, tuttavia, il EVR deve ricevere una notifica ogni volta che la finestra video riceve un messaggio di [**\_ disegno WM**](../gdi/wm-paint.md) . Ciò consente all'EVR di ridisegnare la finestra. Per inviare una notifica a EVR, chiamare il metodo [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) :


```C++
//  Repaint the video window. Call this method on WM_PAINT.

HRESULT CPlayer::Repaint()
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



Il codice seguente illustra il gestore per il messaggio di [**\_ disegno WM**](../gdi/wm-paint.md) . Questa funzione deve essere chiamata dal ciclo di messaggi dell'applicazione.


```C++
//  Handler for WM_PAINT messages.
void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer && g_pPlayer->HasVideo())
    {
        // Video is playing. Ask the player to repaint.
        g_pPlayer->Repaint();
    }
    else
    {
        // The video is not playing, so we must paint the application window.
        RECT rc;
        GetClientRect(hwnd, &rc);
        FillRect(hdc, &rc, (HBRUSH) COLOR_WINDOW);
    }
    EndPaint(hwnd, &ps);
}
```



Il `HasVideo` metodo restituisce **true** se l' `CPlayer` oggetto dispone di un puntatore [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) valido. Vedere [passaggio 1: dichiarare la classe CPlayer](step-1--declare-the-cplayer-class.md).


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a>Ridimensionamento della finestra video

Se si ridimensiona la finestra video, aggiornare il rettangolo di destinazione in EVR chiamando il metodo [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) :


```C++
//  Resize the video rectangle.
//
//  Call this method if the size of the video window changes.

HRESULT CPlayer::ResizeVideo(WORD width, WORD height)
{
    if (m_pVideoDisplay)
    {
        // Set the destination rectangle.
        // Leave the default source rectangle (0,0,1,1).

        RECT rcDest = { 0, 0, width, height };

        return m_pVideoDisplay->SetVideoPosition(NULL, &rcDest);
    }
    else
    {
        return S_OK;
    }
}
```



[Passaggio 7: arrestare la sessione multimediale](step-7--shut-down-the-media-session.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> <dt>

[Come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
