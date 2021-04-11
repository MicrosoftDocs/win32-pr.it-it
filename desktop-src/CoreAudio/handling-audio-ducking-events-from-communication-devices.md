---
description: L'esperienza di ducking predefinita fornita dal sistema include tutti i flussi non di comunicazione disponibili nel sistema quando si apre un flusso di comunicazione.
ms.assetid: 1b92574e-7cde-49c0-a68e-223492412361
title: Considerazioni sull'implementazione per le notifiche di ducking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de07ea23b7cdc8d726ab68a5a6554bf1713a921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127054"
---
# <a name="implementation-considerations-for-ducking-notifications"></a>Considerazioni sull'implementazione per le notifiche di ducking

L' [esperienza di ducking predefinita](stream-attenuation.md) fornita dal sistema include tutti i flussi non di comunicazione disponibili nel sistema quando si apre un flusso di comunicazione. Un'applicazione multimediale può eseguire l'override della gestione predefinita se sa quando inizia e termina la sessione di comunicazione.

Si consideri lo scenario implementato dall'applicazione multimediale nell'esempio [DuckingMediaPlayer](duckingmediaplayer.md) . L'applicazione sospende il flusso audio che sta riproducendo quando riceve una notifica Duck e continua la riproduzione quando riceve una notifica di unduck. Gli eventi di sospensione e continuazione si riflettono nell'interfaccia utente dell'applicazione multimediale. Questa operazione è supportata tramite due messaggi finestra definiti dall'applicazione, la sessione dell'app WM e la sessione dell'app WM non sono state \_ \_ \_ \_ \_ \_ eluse. Le notifiche ducking vengono ricevute in modo asincrono in background e l'applicazione multimediale non deve bloccare il thread di notifica per elaborare i messaggi della finestra. I messaggi della finestra devono essere elaborati nel thread dell'interfaccia utente.

Il comportamento di ducking funziona tramite un meccanismo di notifica. Per offrire un'esperienza personalizzata, l'applicazione multimediale deve implementare l'interfaccia [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) e registrare l'implementazione con il sistema audio. Al completamento della registrazione, l'applicazione multimediale riceve le notifiche degli eventi sotto forma di callback tramite i metodi dell'interfaccia. Il gestore sessioni che gestisce la sessione di comunicazione chiama [**IAudioVolumeDuckNotification:: OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) quando il flusso di comunicazione viene aperto e chiama [**IAudioVolumeDuckNotification:: OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) quando il flusso viene chiuso sul dispositivo di comunicazione.

Nel codice seguente viene illustrata un'implementazione di esempio dell'interfaccia [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) . Per la definizione di CMediaPlayer::D uckingOptOut, vedere Recupero di eventi ducking da un dispositivo di comunicazione.


```C++
class CMediaPlayer : public IAudioVolumeDuckNotification
{
    LONG _refCount;

    HWND _AppWindow;

    ~CMediaPlayer();

    STDMETHOD(OnVolumeDuckNotification) (LPCWSTR sessionID, 
                  UINT32 countCommunicationSessions);
    STDMETHOD(OnVolumeUnduckNotification) (LPCWSTR sessionID);

public:
    CDuckingImpl(HWND hWnd);
    HRESULT DuckingOptOut(bool GetDuckEvents);

    // IUnknown
    IFACEMETHODIMP QueryInterface(__in REFIID riid, __deref_out void **ppv);
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
};

CMediaPlayer::CMediaPlayer(HWND AppWindow) :
        _AppWindow(AppWindow),
        _refCount(1)
{
}
CMediaPlayer::~CMediaPlayer()
{
}

// When we receive a duck notification, 
// post a "Session Ducked" message to the application window.

STDMETHODIMP CMediaPlayer::OnVolumeDuckNotification(LPCWSTR SessionID, 
                                                    UINT32 CountCommunicationsSessions)
{
    PostMessage(_AppWindow, WM_APP_SESSION_DUCKED, 0, 0);
    return 0;
}


// When we receive an unduck notification, 
// post a "Session Unducked" message to the application window.

STDMETHODIMP CMediaPlayer::OnVolumeUnduckNotification(LPCWSTR SessionID)
{
    PostMessage(_AppWindow, WM_APP_SESSION_UNDUCKED, 0, 0);
    return 0;
}

IFACEMETHODIMP CMediaPlayer::QueryInterface(REFIID iid, void **pvObject)
{
    if (pvObject == NULL)
    {
        return E_POINTER;
    }
    *pvObject = NULL;
    if (iid == IID_IUnknown)
    {
        *pvObject = static_cast<IUnknown *>(static_cast<IAudioVolumeDuckNotification *>
                                                                              (this));
        AddRef();
    }
    else if (iid == __uuidof(IAudioVolumeDuckNotification))
    {
        *pvObject = static_cast<IAudioVolumeDuckNotification *>(this);
        AddRef();
    }
    else
    {
        return E_NOINTERFACE;
    }
    return S_OK;
}

IFACEMETHODIMP_(ULONG) CMediaPlayer::AddRef()
{
    return InterlockedIncrement(&_refCount);
}

IFACEMETHODIMP_(ULONG) CMediaPlayer::Release()
{
    LONG refs = InterlockedDecrement(&_refCount);

    if (refs == 0)
    {
        delete this; 
    }

    return refs;   
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di un dispositivo di comunicazione](using-the-communication-device.md)
</dt> <dt>

[Esperienza di ducking predefinita](stream-attenuation.md)
</dt> <dt>

[Disabilitazione dell'esperienza di ducking predefinita](disabling-the-ducking-experience.md)
</dt> <dt>

[Fornire un comportamento di ducking personalizzato](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Recupero di eventi ducking](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



