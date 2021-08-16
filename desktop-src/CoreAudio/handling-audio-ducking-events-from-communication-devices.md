---
description: L'esperienza di papera predefinita fornita dal sistema nasconde tutti i flussi non di comunicazione disponibili nel sistema all'apertura di un flusso di comunicazione.
ms.assetid: 1b92574e-7cde-49c0-a68e-223492412361
title: Considerazioni sull'implementazione per l'abbassamento delle notifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f61d7e67bd456e962442f62f59c3119c756258aadd75334e7736cbc69fba0867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957320"
---
# <a name="implementation-considerations-for-ducking-notifications"></a>Considerazioni sull'implementazione per l'abbassamento delle notifiche

[L'esperienza di paperino](stream-attenuation.md) predefinita fornita dal sistema nasconde tutti i flussi non di comunicazione disponibili nel sistema all'apertura di un flusso di comunicazione. Un'applicazione multimediale può eseguire l'override della gestione predefinita se sa quando viene avviata e terminata la sessione di comunicazione.

Si consideri lo scenario implementato dall'applicazione multimediale [nell'esempio DuckingMediaPlayer.](duckingmediaplayer.md) L'applicazione sospende il flusso audio in riproduzione quando riceve una notifica di tipo duck e continua la riproduzione quando riceve una notifica non scaricata. Gli eventi di sospensione e continuazione si riflettono nell'interfaccia utente dell'applicazione multimediale. Questa funzionalità è supportata tramite due messaggi di finestra definiti dall'applicazione, WM APP SESSION DUCKED e \_ WM APP \_ SESSION \_ \_ \_ \_ UNDUCKED. Le notifiche di ducking vengono ricevute in modo asincrono in background e l'applicazione multimediale non deve bloccare il thread di notifica per elaborare i messaggi della finestra. I messaggi della finestra devono essere elaborati nel thread dell'interfaccia utente.

Il comportamento di ducking funziona tramite un meccanismo di notifica. Per offrire un'esperienza personalizzata, l'applicazione multimediale deve [**implementare l'interfaccia IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) e registrare l'implementazione con il sistema audio. Al completamento della registrazione, l'applicazione multimediale riceve le notifiche degli eventi sotto forma di callback tramite i metodi nell'interfaccia . Il gestore di sessione che gestisce la sessione di comunicazione chiama [**IAudioVolumeDuckNotification::OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) all'apertura del flusso di comunicazione e quindi [**chiama IAudioVolumeDuckNotification::OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) quando il flusso viene chiuso nel dispositivo di comunicazione.

Il codice seguente illustra un'implementazione di esempio [**dell'interfaccia IAudioVolumeDuckNotification.**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) Per la definizione di CMediaPlayer::D uckingOptOut, vedere Getting Ducking Events from a Communication Device (Recupero di eventi da un dispositivo di comunicazione).


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

[Esperienza di paperino predefinita](stream-attenuation.md)
</dt> <dt>

[Disabilitazione dell'esperienza di ducking predefinita](disabling-the-ducking-experience.md)
</dt> <dt>

[Fornire un comportamento di papering personalizzato](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Recupero di eventi di ducking](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



