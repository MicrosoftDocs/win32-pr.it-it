---
description: Questo argomento è il passaggio 5 dell'esercitazione come riprodurre file multimediali con Media Foundation.
ms.assetid: db9b896f-6f56-47b1-b129-331c984e0b16
title: 'Passaggio 5: gestire gli eventi della sessione multimediale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ea3092189644f800a5cb27d2e8b07744f5d90c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320803"
---
# <a name="step-5-handle-media-session-events"></a><span data-ttu-id="d17c2-103">Passaggio 5: gestire gli eventi della sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="d17c2-103">Step 5: Handle Media Session Events</span></span>

<span data-ttu-id="d17c2-104">Questo argomento è il passaggio 5 dell'esercitazione [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="d17c2-104">This topic is step 5 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="d17c2-105">Il codice completo è illustrato nell'esempio relativo alla [riproduzione della sessione multimediale](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="d17c2-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="d17c2-106">Per informazioni di base su questo argomento, vedere [generatori di eventi multimediali](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="d17c2-106">For background on this topic, read [Media Event Generators](media-event-generators.md).</span></span> <span data-ttu-id="d17c2-107">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d17c2-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d17c2-108">Recupero degli eventi di sessione</span><span class="sxs-lookup"><span data-stu-id="d17c2-108">Getting Session Events</span></span>](#getting-session-events)
-   [<span data-ttu-id="d17c2-109">MESessionTopologyStatus</span><span class="sxs-lookup"><span data-stu-id="d17c2-109">MESessionTopologyStatus</span></span>](#mesessiontopologystatus)
-   [<span data-ttu-id="d17c2-110">MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="d17c2-110">MEEndOfPresentation</span></span>](#meendofpresentation)
-   [<span data-ttu-id="d17c2-111">MENewPresentation</span><span class="sxs-lookup"><span data-stu-id="d17c2-111">MENewPresentation</span></span>](#menewpresentation)
-   [<span data-ttu-id="d17c2-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d17c2-112">Related topics</span></span>](#related-topics)

## <a name="getting-session-events"></a><span data-ttu-id="d17c2-113">Recupero degli eventi di sessione</span><span class="sxs-lookup"><span data-stu-id="d17c2-113">Getting Session Events</span></span>

<span data-ttu-id="d17c2-114">Per ottenere gli eventi dalla sessione multimediale, l'oggetto CPlayer chiama il metodo [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) , come illustrato nel [passaggio 4: creare la sessione multimediale](step-4--create-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="d17c2-114">To get events from the Media Session, the CPlayer object calls the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method, as shown in [Step 4: Create the Media Session](step-4--create-the-media-session.md).</span></span> <span data-ttu-id="d17c2-115">Questo metodo è asincrono, ovvero viene restituito immediatamente al chiamante.</span><span class="sxs-lookup"><span data-stu-id="d17c2-115">This method is asynchronous, meaning it returns to the caller immediately.</span></span> <span data-ttu-id="d17c2-116">Quando si verifica l'evento della sessione successiva, la sessione multimediale chiama il metodo [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) dell'oggetto CPlayer.</span><span class="sxs-lookup"><span data-stu-id="d17c2-116">When the next session event occurs, the Media Session calls the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of the CPlayer object.</span></span>

<span data-ttu-id="d17c2-117">È importante ricordare che [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) viene chiamato da un thread di lavoro, non dal thread dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d17c2-117">It is important to remember that [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) gets called from a worker thread, not from the application thread.</span></span> <span data-ttu-id="d17c2-118">Pertanto, l'implementazione di **Invoke** deve essere multithread-safe.</span><span class="sxs-lookup"><span data-stu-id="d17c2-118">Therefore, the implementation of **Invoke** must be multithread-safe.</span></span> <span data-ttu-id="d17c2-119">Un approccio consiste nel proteggere i dati dei membri con una sezione critica.</span><span class="sxs-lookup"><span data-stu-id="d17c2-119">One approach would be to protect the member data with a critical section.</span></span> <span data-ttu-id="d17c2-120">Tuttavia, la `CPlayer` classe Mostra un approccio alternativo:</span><span class="sxs-lookup"><span data-stu-id="d17c2-120">However, the `CPlayer` class shows an alternative approach:</span></span>

1.  <span data-ttu-id="d17c2-121">Nel metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) l'oggetto CPlayer pubblica un messaggio di **\_ \_ \_ evento WM App Player** nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d17c2-121">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, the CPlayer object posts a **WM\_APP\_PLAYER\_EVENT** message to the application.</span></span> <span data-ttu-id="d17c2-122">Il parametro del messaggio è un puntatore [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="d17c2-122">The message parameter is an [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) pointer.</span></span>
2.  <span data-ttu-id="d17c2-123">L'applicazione riceve il messaggio di **\_ \_ \_ evento WM App Player** .</span><span class="sxs-lookup"><span data-stu-id="d17c2-123">The application receives the **WM\_APP\_PLAYER\_EVENT** message.</span></span>
3.  <span data-ttu-id="d17c2-124">L'applicazione chiama il `CPlayer::HandleEvent` metodo passando il puntatore [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="d17c2-124">The application calls the `CPlayer::HandleEvent` method, passing in the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) pointer.</span></span>
4.  <span data-ttu-id="d17c2-125">Il `HandleEvent` metodo risponde all'evento.</span><span class="sxs-lookup"><span data-stu-id="d17c2-125">The `HandleEvent` method responds to the event.</span></span>

<span data-ttu-id="d17c2-126">Il codice seguente illustra il metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) :</span><span class="sxs-lookup"><span data-stu-id="d17c2-126">The following code shows the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method:</span></span>


```C++
//  Callback for the asynchronous BeginGetEvent method.

HRESULT CPlayer::Invoke(IMFAsyncResult *pResult)
{
    MediaEventType meType = MEUnknown;  // Event type

    IMFMediaEvent *pEvent = NULL;

    // Get the event from the event queue.
    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event type. 
    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (meType == MESessionClosed)
    {
        // The session was closed. 
        // The application is waiting on the m_hCloseEvent event handle. 
        SetEvent(m_hCloseEvent);
    }
    else
    {
        // For all other events, get the next event in the queue.
        hr = m_pSession->BeginGetEvent(this, NULL);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Check the application state. 
        
    // If a call to IMFMediaSession::Close is pending, it means the 
    // application is waiting on the m_hCloseEvent event and
    // the application's message loop is blocked. 

    // Otherwise, post a private window message to the application. 

    if (m_state != Closing)
    {
        // Leave a reference count on the event.
        pEvent->AddRef();

        PostMessage(m_hwndEvent, WM_APP_PLAYER_EVENT, 
            (WPARAM)pEvent, (LPARAM)meType);
    }

done:
    SafeRelease(&pEvent);
    return S_OK;
}
```



<span data-ttu-id="d17c2-127">Il metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d17c2-127">The [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method performs the following steps:</span></span>

1.  <span data-ttu-id="d17c2-128">Chiamare [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) per ottenere l'evento.</span><span class="sxs-lookup"><span data-stu-id="d17c2-128">Call [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) to get the event.</span></span> <span data-ttu-id="d17c2-129">Questo metodo restituisce un puntatore all'interfaccia [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="d17c2-129">This method returns a pointer to the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface.</span></span>
2.  <span data-ttu-id="d17c2-130">Chiamare [**IMFMediaEvent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) per ottenere il codice dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d17c2-130">Call [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) to get the event code.</span></span>
3.  <span data-ttu-id="d17c2-131">Se il codice dell'evento è [MESessionClosed](mesessionclosed.md), chiamare seevent per impostare l'evento *m \_ hCloseEvent* .</span><span class="sxs-lookup"><span data-stu-id="d17c2-131">If the event code is [MESessionClosed](mesessionclosed.md), call SetEvent to set the *m\_hCloseEvent* event.</span></span> <span data-ttu-id="d17c2-132">Il motivo di questo passaggio è illustrato nel [passaggio 7: arrestare la sessione multimediale](step-7--shut-down-the-media-session.md)e anche nei commenti del codice.</span><span class="sxs-lookup"><span data-stu-id="d17c2-132">The reason for this step is explained in [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md), and also in the code comments.</span></span>
4.  <span data-ttu-id="d17c2-133">Per tutti gli altri codici evento, chiamare [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) per richiedere l'evento successivo.</span><span class="sxs-lookup"><span data-stu-id="d17c2-133">For all other event codes, call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) to request the next event.</span></span>
5.  <span data-ttu-id="d17c2-134">Pubblica un messaggio di **\_ \_ \_ evento WM App Player** nella finestra.</span><span class="sxs-lookup"><span data-stu-id="d17c2-134">Post a **WM\_APP\_PLAYER\_EVENT** message to the window.</span></span>

<span data-ttu-id="d17c2-135">Il codice seguente illustra il metodo HandleEvent, che viene chiamato quando l'applicazione riceve il messaggio di **\_ \_ \_ evento WM App Player** :</span><span class="sxs-lookup"><span data-stu-id="d17c2-135">The following code shows the HandleEvent method, which is called when the application receives the **WM\_APP\_PLAYER\_EVENT** message:</span></span>


```C++
HRESULT CPlayer::HandleEvent(UINT_PTR pEventPtr)
{
    HRESULT hrStatus = S_OK;            
    MediaEventType meType = MEUnknown;  

    IMFMediaEvent *pEvent = (IMFMediaEvent*)pEventPtr;

    if (pEvent == NULL)
    {
        return E_POINTER;
    }

    // Get the event type.
    HRESULT hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event status. If the operation that triggered the event 
    // did not succeed, the status is a failure code.
    hr = pEvent->GetStatus(&hrStatus);

    // Check if the async operation succeeded.
    if (SUCCEEDED(hr) && FAILED(hrStatus)) 
    {
        hr = hrStatus;
    }
    if (FAILED(hr))
    {
        goto done;
    }

    switch(meType)
    {
    case MESessionTopologyStatus:
        hr = OnTopologyStatus(pEvent);
        break;

    case MEEndOfPresentation:
        hr = OnPresentationEnded(pEvent);
        break;

    case MENewPresentation:
        hr = OnNewPresentation(pEvent);
        break;

    default:
        hr = OnSessionEvent(pEvent, meType);
        break;
    }

done:
    SafeRelease(&pEvent);
    return hr;
}
```



<span data-ttu-id="d17c2-136">Questo metodo chiama [**IMFMediaEvent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) per ottenere il tipo di evento e [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) per ottenere l'esito positivo del codice di errore associato all'evento.</span><span class="sxs-lookup"><span data-stu-id="d17c2-136">This method calls [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) to get the event type and [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) to get the success of failure code associated with the event.</span></span> <span data-ttu-id="d17c2-137">L'azione successiva eseguita dipende dal codice evento.</span><span class="sxs-lookup"><span data-stu-id="d17c2-137">The next action taken depends on the event code.</span></span>

## <a name="mesessiontopologystatus"></a><span data-ttu-id="d17c2-138">MESessionTopologyStatus</span><span class="sxs-lookup"><span data-stu-id="d17c2-138">MESessionTopologyStatus</span></span>

<span data-ttu-id="d17c2-139">L'evento [MESessionTopologyStatus](mesessiontopologystatus.md) segnala una modifica dello stato della topologia.</span><span class="sxs-lookup"><span data-stu-id="d17c2-139">The [MESessionTopologyStatus](mesessiontopologystatus.md) event signals a change in the status of the topology.</span></span> <span data-ttu-id="d17c2-140">L'attributo di [**\_ \_ \_ stato topologia evento MF**](mf-event-topology-status-attribute.md) dell'oggetto evento contiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="d17c2-140">The [**MF\_EVENT\_TOPOLOGY\_STATUS**](mf-event-topology-status-attribute.md) attribute of the event object contains the status.</span></span> <span data-ttu-id="d17c2-141">Per questo esempio, l'unico valore di interesse è **MF \_ TOPOSTATUS \_ Ready**, che indica che la riproduzione è pronta per l'avvio.</span><span class="sxs-lookup"><span data-stu-id="d17c2-141">For this example, the only value of interest is **MF\_TOPOSTATUS\_READY**, which indicates that playback is ready to start.</span></span>


```C++
HRESULT CPlayer::OnTopologyStatus(IMFMediaEvent *pEvent)
{
    UINT32 status; 

    HRESULT hr = pEvent->GetUINT32(MF_EVENT_TOPOLOGY_STATUS, &status);
    if (SUCCEEDED(hr) && (status == MF_TOPOSTATUS_READY))
    {
        SafeRelease(&m_pVideoDisplay);

        // Get the IMFVideoDisplayControl interface from EVR. This call is
        // expected to fail if the media file does not have a video stream.

        (void)MFGetService(m_pSession, MR_VIDEO_RENDER_SERVICE, 
            IID_PPV_ARGS(&m_pVideoDisplay));

        hr = StartPlayback();
    }
    return hr;
}
```



<span data-ttu-id="d17c2-142">Il `CPlayer::StartPlayback` metodo è illustrato nel [passaggio 6: controllare la riproduzione](step-6--control-playback.md).</span><span class="sxs-lookup"><span data-stu-id="d17c2-142">The `CPlayer::StartPlayback` method is shown in [Step 6: Control Playback](step-6--control-playback.md).</span></span>

<span data-ttu-id="d17c2-143">Questo esempio chiama anche [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'interfaccia [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) dal [renderer video avanzato](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="d17c2-143">This example also calls [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface from the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="d17c2-144">Questa interfaccia è necessaria per gestire il ridisegno e il ridimensionamento della finestra video, mostrata anche nel [passaggio 6: controllare la riproduzione](step-6--control-playback.md).</span><span class="sxs-lookup"><span data-stu-id="d17c2-144">This interface is needed to handle repainting and resizing the video window, also shown in [Step 6: Control Playback](step-6--control-playback.md).</span></span>

## <a name="meendofpresentation"></a><span data-ttu-id="d17c2-145">MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="d17c2-145">MEEndOfPresentation</span></span>

<span data-ttu-id="d17c2-146">L'evento [MEEndOfPresentation](meendofpresentation.md) segnala che la riproduzione ha raggiunto la fine del file.</span><span class="sxs-lookup"><span data-stu-id="d17c2-146">The [MEEndOfPresentation](meendofpresentation.md) event signals that playback has reached the end of the file.</span></span> <span data-ttu-id="d17c2-147">La sessione multimediale passa automaticamente allo stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="d17c2-147">The Media Session automatically switches back to the stopped state.</span></span>


```C++
//  Handler for MEEndOfPresentation event.
HRESULT CPlayer::OnPresentationEnded(IMFMediaEvent *pEvent)
{
    // The session puts itself into the stopped state automatically.
    m_state = Stopped;
    return S_OK;
}
```



## <a name="menewpresentation"></a><span data-ttu-id="d17c2-148">MENewPresentation</span><span class="sxs-lookup"><span data-stu-id="d17c2-148">MENewPresentation</span></span>

<span data-ttu-id="d17c2-149">L'evento [MENewPresentation](menewpresentation.md) segnala l'inizio di una nuova presentazione.</span><span class="sxs-lookup"><span data-stu-id="d17c2-149">The [MENewPresentation](menewpresentation.md) event signals the start of a new presentation.</span></span> <span data-ttu-id="d17c2-150">I dati dell'evento sono un puntatore [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) per la nuova presentazione.</span><span class="sxs-lookup"><span data-stu-id="d17c2-150">The event data is an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer for the new presentation.</span></span>

<span data-ttu-id="d17c2-151">In molti casi, l'evento non verrà visualizzato.</span><span class="sxs-lookup"><span data-stu-id="d17c2-151">In many cases, you will not receive this event at all.</span></span> <span data-ttu-id="d17c2-152">In tal caso, usare il puntatore [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) per creare una nuova topologia di riproduzione, come illustrato in [passaggio 3: aprire un file multimediale](step-3--open-a-media-file.md).</span><span class="sxs-lookup"><span data-stu-id="d17c2-152">If you do, use the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer to create a new playback topology, as shown in [Step 3: Open a Media File](step-3--open-a-media-file.md).</span></span> <span data-ttu-id="d17c2-153">Accodare quindi la nuova topologia nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="d17c2-153">Then queue the new topology on the Media Session.</span></span>


```C++
//  Handler for MENewPresentation event.
//
//  This event is sent if the media source has a new presentation, which 
//  requires a new topology. 

HRESULT CPlayer::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFTopology *pTopology = NULL;

    // Get the presentation descriptor from the event.
    HRESULT hr = GetEventObject(pEvent, &pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pPD,  m_hwndVideo,&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

done:
    SafeRelease(&pTopology);
    SafeRelease(&pPD);
    return S_OK;
}
```



<span data-ttu-id="d17c2-154">[Passaggio 6: controllare la riproduzione](step-6--control-playback.md)</span><span class="sxs-lookup"><span data-stu-id="d17c2-154">Next: [Step 6: Control Playback](step-6--control-playback.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="d17c2-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d17c2-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d17c2-156">Riproduzione di audio/video</span><span class="sxs-lookup"><span data-stu-id="d17c2-156">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="d17c2-157">Come riprodurre file multimediali con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d17c2-157">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



