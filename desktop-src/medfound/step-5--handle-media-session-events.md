---
description: Questo argomento è il passaggio 5 dell'esercitazione Come riprodurre file multimediali con Media Foundation.
ms.assetid: db9b896f-6f56-47b1-b129-331c984e0b16
title: 'Passaggio 5: Gestire gli eventi della sessione multimediale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be80d8d336cb5f3996c72d806259ae8c74eed464245ac439fdd356f091965bde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721901"
---
# <a name="step-5-handle-media-session-events"></a>Passaggio 5: Gestire gli eventi della sessione multimediale

Questo argomento è il passaggio 5 dell'esercitazione [Come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md). Il codice completo è illustrato nell'argomento [Esempio di riproduzione di sessioni multimediali](media-session-playback-example.md).

Per informazioni di base su questo argomento, vedere [Media Event Generators](media-event-generators.md). In questo argomento sono incluse le sezioni seguenti:

-   [Recupero di eventi di sessione](#getting-session-events)
-   [MESessionTopologyStatus](#mesessiontopologystatus)
-   [MEEndOfPresentation](#meendofpresentation)
-   [MENewPresentation](#menewpresentation)
-   [Argomenti correlati](#related-topics)

## <a name="getting-session-events"></a>Recupero di eventi di sessione

Per ottenere eventi dalla sessione multimediale, l'oggetto CPlayer chiama il metodo [**IMFMediaEventGenerator::BeginGetEvent,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) come illustrato in [Passaggio 4: Creare](step-4--create-the-media-session.md)la sessione multimediale . Questo metodo è asincrono, ovvero viene restituito immediatamente al chiamante. Quando si verifica l'evento di sessione successivo, la sessione multimediale chiama il [**metodo IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) dell'oggetto CPlayer.

È importante ricordare che [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) viene chiamato da un thread di lavoro, non dal thread dell'applicazione. Pertanto, l'implementazione **di Invoke** deve essere multithread-safe. Un approccio consiste nel proteggere i dati dei membri con una sezione critica. Tuttavia, la `CPlayer` classe mostra un approccio alternativo:

1.  Nel metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) l'oggetto CPlayer invia un **messaggio WM APP PLAYER \_ \_ \_ EVENT** all'applicazione. Il parametro message è un [**puntatore IMFMediaEvent.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
2.  L'applicazione riceve il **messaggio DI EVENTO WM APP \_ \_ PLAYER. \_**
3.  L'applicazione chiama `CPlayer::HandleEvent` il metodo , passando il [**puntatore IMFMediaEvent.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
4.  Il `HandleEvent` metodo risponde all'evento .

Il codice seguente illustra il [**metodo Invoke:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)


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



Il [**metodo Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) esegue i passaggi seguenti:

1.  Chiamare [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) per ottenere l'evento. Questo metodo restituisce un puntatore [**all'interfaccia IMFMediaEvent.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
2.  Chiamare [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) per ottenere il codice evento.
3.  Se il codice evento è [MESessionClosed,](mesessionclosed.md)chiamare SetEvent per impostare *l'evento m \_ hCloseEvent.* Il motivo di questo passaggio è illustrato in [Passaggio 7: Arrestare](step-7--shut-down-the-media-session.md)la sessione multimediale e anche nei commenti del codice.
4.  Per tutti gli altri codici evento, chiamare [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) per richiedere l'evento successivo.
5.  Pubblicare **un messaggio DI EVENTO \_ \_ \_ WM APP PLAYER** nella finestra.

Il codice seguente illustra il metodo HandleEvent, che viene chiamato quando l'applicazione riceve il messaggio **WM \_ APP PLAYER \_ \_ EVENT:**


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



Questo metodo chiama [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) per ottenere il tipo di evento e [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) per ottenere l'esito positivo del codice di errore associato all'evento. L'azione successiva eseguita dipende dal codice evento.

## <a name="mesessiontopologystatus"></a>MESessionTopologyStatus

[L'evento MESessionTopologyStatus](mesessiontopologystatus.md) segnala una modifica dello stato della topologia. [**L'attributo \_ MF EVENT \_ TOPOLOGY \_ STATUS**](mf-event-topology-status-attribute.md) dell'oggetto evento contiene lo stato. Per questo esempio, l'unico valore di interesse è **MF \_ TOPOSTATUS \_ READY,** che indica che la riproduzione è pronta per l'avvio.


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



Il `CPlayer::StartPlayback` metodo è illustrato in Passaggio [6: Controllare la riproduzione.](step-6--control-playback.md)

Questo esempio chiama [**anche MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere [**l'interfaccia IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) da [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR). Questa interfaccia è necessaria per gestire il ridisegno e il ridimensionamento della finestra video, come illustrato anche in [Passaggio 6: Controllare la riproduzione.](step-6--control-playback.md)

## <a name="meendofpresentation"></a>MEEndOfPresentation

[L'evento MEEndOfPresentation](meendofpresentation.md) segnala che la riproduzione ha raggiunto la fine del file. La sessione multimediale torna automaticamente allo stato arrestato.


```C++
//  Handler for MEEndOfPresentation event.
HRESULT CPlayer::OnPresentationEnded(IMFMediaEvent *pEvent)
{
    // The session puts itself into the stopped state automatically.
    m_state = Stopped;
    return S_OK;
}
```



## <a name="menewpresentation"></a>MENewPresentation

[L'evento MENewPresentation](menewpresentation.md) segnala l'inizio di una nuova presentazione. I dati dell'evento sono un [**puntatore IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) per la nuova presentazione.

In molti casi, questo evento non verrà ricevuto affatto. In questo caso, usare il [**puntatore IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) per creare una nuova topologia di riproduzione, come illustrato in [Passaggio 3: Aprire un file multimediale.](step-3--open-a-media-file.md) Accodare quindi la nuova topologia nella sessione multimediale.


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



Passaggio [6: Controllare la riproduzione](step-6--control-playback.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> <dt>

[Come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



