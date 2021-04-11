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
# <a name="implementation-considerations-for-ducking-notifications"></a><span data-ttu-id="ea65b-103">Considerazioni sull'implementazione per le notifiche di ducking</span><span class="sxs-lookup"><span data-stu-id="ea65b-103">Implementation Considerations for Ducking Notifications</span></span>

<span data-ttu-id="ea65b-104">L' [esperienza di ducking predefinita](stream-attenuation.md) fornita dal sistema include tutti i flussi non di comunicazione disponibili nel sistema quando si apre un flusso di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="ea65b-104">The [Default Ducking Experience](stream-attenuation.md) provided by the system ducks all non-communication streams available in the system when a communication stream opens.</span></span> <span data-ttu-id="ea65b-105">Un'applicazione multimediale può eseguire l'override della gestione predefinita se sa quando inizia e termina la sessione di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="ea65b-105">A media application can override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="ea65b-106">Si consideri lo scenario implementato dall'applicazione multimediale nell'esempio [DuckingMediaPlayer](duckingmediaplayer.md) .</span><span class="sxs-lookup"><span data-stu-id="ea65b-106">Consider the scenario implemented by the media application in the [DuckingMediaPlayer](duckingmediaplayer.md) sample.</span></span> <span data-ttu-id="ea65b-107">L'applicazione sospende il flusso audio che sta riproducendo quando riceve una notifica Duck e continua la riproduzione quando riceve una notifica di unduck.</span><span class="sxs-lookup"><span data-stu-id="ea65b-107">The application pauses the audio stream that it is playing when it receives a duck notification and continues playback when it receives an unduck notification.</span></span> <span data-ttu-id="ea65b-108">Gli eventi di sospensione e continuazione si riflettono nell'interfaccia utente dell'applicazione multimediale.</span><span class="sxs-lookup"><span data-stu-id="ea65b-108">The pause and continue events are reflected in the media application's user interface.</span></span> <span data-ttu-id="ea65b-109">Questa operazione è supportata tramite due messaggi finestra definiti dall'applicazione, la sessione dell'app WM e la sessione dell'app WM non sono state \_ \_ \_ \_ \_ \_ eluse.</span><span class="sxs-lookup"><span data-stu-id="ea65b-109">This is supported through two application-defined window messages, WM\_APP\_SESSION\_DUCKED and WM\_APP\_SESSION\_UNDUCKED.</span></span> <span data-ttu-id="ea65b-110">Le notifiche ducking vengono ricevute in modo asincrono in background e l'applicazione multimediale non deve bloccare il thread di notifica per elaborare i messaggi della finestra.</span><span class="sxs-lookup"><span data-stu-id="ea65b-110">The ducking notifications are received asynchronously in the background and the media application must not block the notification thread to process the window messages.</span></span> <span data-ttu-id="ea65b-111">I messaggi della finestra devono essere elaborati nel thread dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ea65b-111">The window messages must be processed on the user interface thread.</span></span>

<span data-ttu-id="ea65b-112">Il comportamento di ducking funziona tramite un meccanismo di notifica.</span><span class="sxs-lookup"><span data-stu-id="ea65b-112">The ducking behavior works through a notification mechanism.</span></span> <span data-ttu-id="ea65b-113">Per offrire un'esperienza personalizzata, l'applicazione multimediale deve implementare l'interfaccia [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) e registrare l'implementazione con il sistema audio.</span><span class="sxs-lookup"><span data-stu-id="ea65b-113">To provide a customized experience, the media application must implement the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface and register the implementation with the audio system.</span></span> <span data-ttu-id="ea65b-114">Al completamento della registrazione, l'applicazione multimediale riceve le notifiche degli eventi sotto forma di callback tramite i metodi dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ea65b-114">Upon successful registration, the media application receives event notifications in the form of callbacks through the methods in the interface.</span></span> <span data-ttu-id="ea65b-115">Il gestore sessioni che gestisce la sessione di comunicazione chiama [**IAudioVolumeDuckNotification:: OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) quando il flusso di comunicazione viene aperto e chiama [**IAudioVolumeDuckNotification:: OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) quando il flusso viene chiuso sul dispositivo di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="ea65b-115">The session manager handling the communication session calls [**IAudioVolumeDuckNotification::OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) when the communication stream opens and then calls [**IAudioVolumeDuckNotification::OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) when the stream is closed on the communication device.</span></span>

<span data-ttu-id="ea65b-116">Nel codice seguente viene illustrata un'implementazione di esempio dell'interfaccia [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) .</span><span class="sxs-lookup"><span data-stu-id="ea65b-116">The following code shows a sample implementation of the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface.</span></span> <span data-ttu-id="ea65b-117">Per la definizione di CMediaPlayer::D uckingOptOut, vedere Recupero di eventi ducking da un dispositivo di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="ea65b-117">For the definition of CMediaPlayer::DuckingOptOut, see Getting Ducking Events from a Communication Device.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ea65b-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea65b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea65b-119">Uso di un dispositivo di comunicazione</span><span class="sxs-lookup"><span data-stu-id="ea65b-119">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="ea65b-120">Esperienza di ducking predefinita</span><span class="sxs-lookup"><span data-stu-id="ea65b-120">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="ea65b-121">Disabilitazione dell'esperienza di ducking predefinita</span><span class="sxs-lookup"><span data-stu-id="ea65b-121">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="ea65b-122">Fornire un comportamento di ducking personalizzato</span><span class="sxs-lookup"><span data-stu-id="ea65b-122">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="ea65b-123">Recupero di eventi ducking</span><span class="sxs-lookup"><span data-stu-id="ea65b-123">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



