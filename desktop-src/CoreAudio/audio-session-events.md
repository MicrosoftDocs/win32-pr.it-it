---
description: Eventi della sessione audio
ms.assetid: 6943b405-0807-412b-a149-fc3a8ece1b48
title: Eventi della sessione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ec5de18c883f817c2f650ccfc48ad0149ac84e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966142"
---
# <a name="audio-session-events"></a><span data-ttu-id="1a8b2-103">Eventi della sessione audio</span><span class="sxs-lookup"><span data-stu-id="1a8b2-103">Audio Session Events</span></span>

<span data-ttu-id="1a8b2-104">Un'applicazione che gestisce flussi audio in modalità condivisa può registrarsi per ricevere notifiche quando si verificano eventi di sessione.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-104">An application that manages shared-mode audio streams can register to receive notifications when session events occur.</span></span> <span data-ttu-id="1a8b2-105">Come spiegato in precedenza, ogni flusso appartiene a una [sessione audio](audio-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="1a8b2-105">As explained previously, each stream belongs to an [audio session](audio-sessions.md).</span></span> <span data-ttu-id="1a8b2-106">Un evento di sessione viene avviato da una modifica dello stato di una sessione audio.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-106">A session event is initiated by a change in the status of an audio session.</span></span>

<span data-ttu-id="1a8b2-107">Un'applicazione client può registrarsi per ricevere notifiche dei seguenti tipi di eventi di sessione:</span><span class="sxs-lookup"><span data-stu-id="1a8b2-107">A client application can register to receive notifications of the following types of session events:</span></span>

-   <span data-ttu-id="1a8b2-108">Il livello del volume master o lo stato di muting della sessione submix è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-108">The master volume level or muting state of the session submix has changed.</span></span>
-   <span data-ttu-id="1a8b2-109">Il livello del volume di uno o più canali della sessione submix è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-109">The volume level of one or more channels of the session submix has changed.</span></span>
-   <span data-ttu-id="1a8b2-110">La sessione è stata disconnessa.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-110">The session has been disconnected.</span></span>
-   <span data-ttu-id="1a8b2-111">Lo stato dell'attività della sessione è stato modificato in attivo, inattivo o scaduto.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-111">The activity state of the session has changed to active, inactive, or expired.</span></span>
-   <span data-ttu-id="1a8b2-112">Alla sessione è stato assegnato un nuovo parametro di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-112">The session has been assigned a new grouping parameter.</span></span>
-   <span data-ttu-id="1a8b2-113">È stata modificata una proprietà dell'interfaccia utente della sessione (icona o nome visualizzato).</span><span class="sxs-lookup"><span data-stu-id="1a8b2-113">A user-interface property of the session (icon or display name) has changed.</span></span>

<span data-ttu-id="1a8b2-114">Il client riceve le notifiche di questi eventi tramite i metodi nell'implementazione dell'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="1a8b2-114">The client receives notifications of these events through the methods in its implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="1a8b2-115">Diversamente dalle altre interfacce in WASAPI, implementate dal modulo di sistema WASAPI, il client implementa **IAudioSessionEvents**.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-115">Unlike the other interfaces in WASAPI, which are implemented by the WASAPI system module, the client implements **IAudioSessionEvents**.</span></span> <span data-ttu-id="1a8b2-116">I metodi in questa interfaccia ricevono callback dal modulo di sistema WASAPI quando si verificano eventi di sessione.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-116">The methods in this interface receive callbacks from the WASAPI system module when session events occur.</span></span>

<span data-ttu-id="1a8b2-117">Per iniziare a ricevere le notifiche, il client chiama il metodo [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) per registrare l'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="1a8b2-117">To begin receiving notifications, the client calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register its [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="1a8b2-118">Quando il client non richiede più notifiche, chiama il metodo [**IAudioSessionControl:: UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) per eliminare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-118">When the client no longer requires notifications, it calls the [**IAudioSessionControl::UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) method to delete the registration.</span></span>

<span data-ttu-id="1a8b2-119">Nell'esempio di codice seguente viene illustrata una possibile implementazione dell'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) :</span><span class="sxs-lookup"><span data-stu-id="1a8b2-119">The following code example shows a possible implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface:</span></span>


```C++
//-----------------------------------------------------------
// Client implementation of IAudioSessionEvents interface.
// WASAPI calls these methods to notify the application when
// a parameter or property of the audio session changes.
//-----------------------------------------------------------
class CAudioSessionEvents : public IAudioSessionEvents
{
    LONG _cRef;

public:
    CAudioSessionEvents() :
        _cRef(1)
    {
    }

    ~CAudioSessionEvents()
    {
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID  riid,
                                VOID  **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioSessionEvents) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioSessionEvents*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Notification methods for audio session events

    HRESULT STDMETHODCALLTYPE OnDisplayNameChanged(
                                LPCWSTR NewDisplayName,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnIconPathChanged(
                                LPCWSTR NewIconPath,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnSimpleVolumeChanged(
                                float NewVolume,
                                BOOL NewMute,
                                LPCGUID EventContext)
    {
        if (NewMute)
        {
            printf("MUTE\n");
        }
        else
        {
            printf("Volume = %d percent\n",
                   (UINT32)(100*NewVolume + 0.5));
        }

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnChannelVolumeChanged(
                                DWORD ChannelCount,
                                float NewChannelVolumeArray[],
                                DWORD ChangedChannel,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnGroupingParamChanged(
                                LPCGUID NewGroupingParam,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnStateChanged(
                                AudioSessionState NewState)
    {
        char *pszState = "?????";

        switch (NewState)
        {
        case AudioSessionStateActive:
            pszState = "active";
            break;
        case AudioSessionStateInactive:
            pszState = "inactive";
            break;
        }
        printf("New session state = %s\n", pszState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnSessionDisconnected(
              AudioSessionDisconnectReason DisconnectReason)
    {
        char *pszReason = "?????";

        switch (DisconnectReason)
        {
        case DisconnectReasonDeviceRemoval:
            pszReason = "device removed";
            break;
        case DisconnectReasonServerShutdown:
            pszReason = "server shut down";
            break;
        case DisconnectReasonFormatChanged:
            pszReason = "format changed";
            break;
        case DisconnectReasonSessionLogoff:
            pszReason = "user logged off";
            break;
        case DisconnectReasonSessionDisconnected:
            pszReason = "session disconnected";
            break;
        case DisconnectReasonExclusiveModeOverride:
            pszReason = "exclusive-mode override";
            break;
        }
        printf("Audio session disconnected (reason: %s)\n",
               pszReason);

        return S_OK;
    }
};
```



<span data-ttu-id="1a8b2-120">La classe CAudioSessionEvents nell'esempio di codice precedente è un'implementazione dell'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="1a8b2-120">The CAudioSessionEvents class in the preceding code example is an implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="1a8b2-121">Questa particolare implementazione potrebbe far parte di un'applicazione console che stampa informazioni sugli eventi di sessione in una finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-121">This particular implementation might be part of a console application that prints information about session events to a Command Prompt window.</span></span> <span data-ttu-id="1a8b2-122">Poiché **IAudioSessionEvents** eredita da [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), la definizione della classe contiene le implementazioni dei metodi **IUnknown** [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)e [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="1a8b2-122">Because **IAudioSessionEvents** inherits from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), the class definition contains implementations of the **IUnknown** methods [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="1a8b2-123">I metodi pubblici rimanenti nella definizione della classe sono specifici dell'interfaccia **IAudioSessionEvents** .</span><span class="sxs-lookup"><span data-stu-id="1a8b2-123">The remaining public methods in the class definition are specific to the **IAudioSessionEvents** interface.</span></span>

<span data-ttu-id="1a8b2-124">Alcuni client potrebbero non essere interessati al monitoraggio di tutti i tipi di eventi di sessione.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-124">Some clients might not be interested in monitoring all types of session events.</span></span> <span data-ttu-id="1a8b2-125">Nell'esempio di codice precedente, diversi metodi di notifica nella classe CAudioSessionEvents non eseguono alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-125">In the preceding code example, several notification methods in the CAudioSessionEvents class do nothing.</span></span> <span data-ttu-id="1a8b2-126">Ad esempio, il metodo [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) non esegue alcuna operazione tranne per restituire il codice di stato \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-126">For example, the [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) method does nothing except to return status code S\_OK.</span></span> <span data-ttu-id="1a8b2-127">Questa applicazione non monitora i volumi di canale perché non modifica i volumi del canale (chiamando i metodi nell'interfaccia [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) ) e non condivide la sessione con altre applicazioni che potrebbero modificare i volumi del canale.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-127">This application does not monitor channel volumes because it does not change the channel volumes (by calling the methods in the [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) interface), and it does not share the session with other applications that might change the channel volumes.</span></span>

<span data-ttu-id="1a8b2-128">Gli unici tre metodi della classe CAudioSessionEvents che inviano notifiche all'utente degli eventi di sessione sono [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)e [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected).</span><span class="sxs-lookup"><span data-stu-id="1a8b2-128">The only three methods in the CAudioSessionEvents class that notify the user of session events are [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged), and [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected).</span></span> <span data-ttu-id="1a8b2-129">Ad esempio, se l'utente esegue il programma di controllo del volume di sistema, sndvol, e usa il controllo volume in sndvol per modificare il livello di volume dell'applicazione, `OnSimpleVolumeChanged` stampa immediatamente il nuovo livello di volume.</span><span class="sxs-lookup"><span data-stu-id="1a8b2-129">For example, if the user runs the system volume-control program, Sndvol, and uses the volume control in Sndvol to change the application's volume level, `OnSimpleVolumeChanged` immediately prints the new volume level.</span></span>

<span data-ttu-id="1a8b2-130">Per un esempio di codice che registra e Annulla la registrazione dell'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) di un client, vedere [eventi audio per le applicazioni audio legacy](audio-events-for-legacy-audio-applications.md).</span><span class="sxs-lookup"><span data-stu-id="1a8b2-130">For a code example that registers and unregisters a client's [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface, see [Audio Events for Legacy Audio Applications](audio-events-for-legacy-audio-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a8b2-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a8b2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a8b2-132">Sessioni audio</span><span class="sxs-lookup"><span data-stu-id="1a8b2-132">Audio Sessions</span></span>](audio-sessions.md)
</dt> </dl>

 

 
