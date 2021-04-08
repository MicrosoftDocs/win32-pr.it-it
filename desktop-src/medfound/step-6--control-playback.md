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
# <a name="step-6-control-playback"></a><span data-ttu-id="75cd5-103">Passaggio 6: controllare la riproduzione</span><span class="sxs-lookup"><span data-stu-id="75cd5-103">Step 6: Control Playback</span></span>

<span data-ttu-id="75cd5-104">Questo argomento è il passaggio 6 dell'esercitazione [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="75cd5-104">This topic is step 6 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="75cd5-105">Il codice completo è illustrato nell'esempio relativo alla [riproduzione della sessione multimediale](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="75cd5-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="75cd5-106">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="75cd5-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="75cd5-107">Avvio della riproduzione</span><span class="sxs-lookup"><span data-stu-id="75cd5-107">Starting Playback</span></span>](#starting-playback)
-   [<span data-ttu-id="75cd5-108">Sospensione della riproduzione</span><span class="sxs-lookup"><span data-stu-id="75cd5-108">Pausing Playback</span></span>](#pausing-playback)
-   [<span data-ttu-id="75cd5-109">Arresto della riproduzione</span><span class="sxs-lookup"><span data-stu-id="75cd5-109">Stopping Playback</span></span>](#stopping-playback)
-   [<span data-ttu-id="75cd5-110">Ridisegno della finestra video</span><span class="sxs-lookup"><span data-stu-id="75cd5-110">Repainting the Video Window</span></span>](#repainting-the-video-window)
-   [<span data-ttu-id="75cd5-111">Ridimensionamento della finestra video</span><span class="sxs-lookup"><span data-stu-id="75cd5-111">Resizing the Video Window</span></span>](#resizing-the-video-window)
-   [<span data-ttu-id="75cd5-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="75cd5-112">Related topics</span></span>](#related-topics)

## <a name="starting-playback"></a><span data-ttu-id="75cd5-113">Avvio della riproduzione</span><span class="sxs-lookup"><span data-stu-id="75cd5-113">Starting Playback</span></span>

<span data-ttu-id="75cd5-114">Per avviare la riproduzione, chiamare [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="75cd5-114">To start playback, call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="75cd5-115">Nel codice seguente viene illustrato come avviare dalla posizione di riproduzione corrente.</span><span class="sxs-lookup"><span data-stu-id="75cd5-115">The following code shows how to start from the current playback position.</span></span>


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



<span data-ttu-id="75cd5-116">Il metodo [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) può inoltre specificare una posizione iniziale relativa all'inizio del file. Per ulteriori informazioni, vedere l'argomento di riferimento per le API.</span><span class="sxs-lookup"><span data-stu-id="75cd5-116">The [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method can also specify a starting position relative to the start of the file; see the API reference topic for more information.</span></span>

## <a name="pausing-playback"></a><span data-ttu-id="75cd5-117">Sospensione della riproduzione</span><span class="sxs-lookup"><span data-stu-id="75cd5-117">Pausing Playback</span></span>

<span data-ttu-id="75cd5-118">Per sospendere la riproduzione, chiamare [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).</span><span class="sxs-lookup"><span data-stu-id="75cd5-118">To pause playback, call [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).</span></span>


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



## <a name="stopping-playback"></a><span data-ttu-id="75cd5-119">Arresto della riproduzione</span><span class="sxs-lookup"><span data-stu-id="75cd5-119">Stopping Playback</span></span>

<span data-ttu-id="75cd5-120">Per arrestare la riproduzione, chiamare [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="75cd5-120">To stop playback, call [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span> <span data-ttu-id="75cd5-121">Mentre la riproduzione viene arrestata, l'immagine video viene deselezionata e la finestra video viene disegnata con il colore di sfondo (nero per impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="75cd5-121">While playback is stopped, the video image is cleared and the video window is painted with the background color (black by default).</span></span>


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



## <a name="repainting-the-video-window"></a><span data-ttu-id="75cd5-122">Ridisegno della finestra video</span><span class="sxs-lookup"><span data-stu-id="75cd5-122">Repainting the Video Window</span></span>

<span data-ttu-id="75cd5-123">Il [renderer video avanzato](enhanced-video-renderer.md) (EVR) consente di disegnare il video nella finestra specificata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="75cd5-123">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) draws the video in the window specified by the application.</span></span> <span data-ttu-id="75cd5-124">Questo problema si verifica in un thread separato e, nella maggior parte dei casi, l'applicazione non deve gestire questo processo.</span><span class="sxs-lookup"><span data-stu-id="75cd5-124">This occurs on a separate thread, and for the most part, your application does not need to manage this process.</span></span> <span data-ttu-id="75cd5-125">Se la riproduzione viene sospesa o arrestata, tuttavia, il EVR deve ricevere una notifica ogni volta che la finestra video riceve un messaggio di [**\_ disegno WM**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="75cd5-125">If playback is paused or stopped, however, the EVR must be notified whenever the video window receives a [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span> <span data-ttu-id="75cd5-126">Ciò consente all'EVR di ridisegnare la finestra.</span><span class="sxs-lookup"><span data-stu-id="75cd5-126">This allows the EVR to repaint the window.</span></span> <span data-ttu-id="75cd5-127">Per inviare una notifica a EVR, chiamare il metodo [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) :</span><span class="sxs-lookup"><span data-stu-id="75cd5-127">To notify the EVR, call the [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) method:</span></span>


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



<span data-ttu-id="75cd5-128">Il codice seguente illustra il gestore per il messaggio di [**\_ disegno WM**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="75cd5-128">The following code shows the handler for the [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span> <span data-ttu-id="75cd5-129">Questa funzione deve essere chiamata dal ciclo di messaggi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="75cd5-129">This function should be called from the application's message loop.</span></span>


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



<span data-ttu-id="75cd5-130">Il `HasVideo` metodo restituisce **true** se l' `CPlayer` oggetto dispone di un puntatore [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) valido.</span><span class="sxs-lookup"><span data-stu-id="75cd5-130">The `HasVideo` method returns **TRUE** if the `CPlayer` object has a valid [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) pointer.</span></span> <span data-ttu-id="75cd5-131">Vedere [passaggio 1: dichiarare la classe CPlayer](step-1--declare-the-cplayer-class.md).</span><span class="sxs-lookup"><span data-stu-id="75cd5-131">(See [Step 1: Declare the CPlayer Class](step-1--declare-the-cplayer-class.md).)</span></span>


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a><span data-ttu-id="75cd5-132">Ridimensionamento della finestra video</span><span class="sxs-lookup"><span data-stu-id="75cd5-132">Resizing the Video Window</span></span>

<span data-ttu-id="75cd5-133">Se si ridimensiona la finestra video, aggiornare il rettangolo di destinazione in EVR chiamando il metodo [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) :</span><span class="sxs-lookup"><span data-stu-id="75cd5-133">If you resize the video window, update the destination rectangle on the EVR by calling the [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) method:</span></span>


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



<span data-ttu-id="75cd5-134">[Passaggio 7: arrestare la sessione multimediale](step-7--shut-down-the-media-session.md)</span><span class="sxs-lookup"><span data-stu-id="75cd5-134">Next: [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="75cd5-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="75cd5-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75cd5-136">Riproduzione di audio/video</span><span class="sxs-lookup"><span data-stu-id="75cd5-136">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="75cd5-137">Come riprodurre file multimediali con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="75cd5-137">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
