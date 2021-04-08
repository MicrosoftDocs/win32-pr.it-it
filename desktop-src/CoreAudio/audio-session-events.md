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
# <a name="audio-session-events"></a>Eventi della sessione audio

Un'applicazione che gestisce flussi audio in modalità condivisa può registrarsi per ricevere notifiche quando si verificano eventi di sessione. Come spiegato in precedenza, ogni flusso appartiene a una [sessione audio](audio-sessions.md). Un evento di sessione viene avviato da una modifica dello stato di una sessione audio.

Un'applicazione client può registrarsi per ricevere notifiche dei seguenti tipi di eventi di sessione:

-   Il livello del volume master o lo stato di muting della sessione submix è stato modificato.
-   Il livello del volume di uno o più canali della sessione submix è stato modificato.
-   La sessione è stata disconnessa.
-   Lo stato dell'attività della sessione è stato modificato in attivo, inattivo o scaduto.
-   Alla sessione è stato assegnato un nuovo parametro di raggruppamento.
-   È stata modificata una proprietà dell'interfaccia utente della sessione (icona o nome visualizzato).

Il client riceve le notifiche di questi eventi tramite i metodi nell'implementazione dell'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . Diversamente dalle altre interfacce in WASAPI, implementate dal modulo di sistema WASAPI, il client implementa **IAudioSessionEvents**. I metodi in questa interfaccia ricevono callback dal modulo di sistema WASAPI quando si verificano eventi di sessione.

Per iniziare a ricevere le notifiche, il client chiama il metodo [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) per registrare l'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . Quando il client non richiede più notifiche, chiama il metodo [**IAudioSessionControl:: UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) per eliminare la registrazione.

Nell'esempio di codice seguente viene illustrata una possibile implementazione dell'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) :


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



La classe CAudioSessionEvents nell'esempio di codice precedente è un'implementazione dell'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . Questa particolare implementazione potrebbe far parte di un'applicazione console che stampa informazioni sugli eventi di sessione in una finestra del prompt dei comandi. Poiché **IAudioSessionEvents** eredita da [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), la definizione della classe contiene le implementazioni dei metodi **IUnknown** [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)e [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). I metodi pubblici rimanenti nella definizione della classe sono specifici dell'interfaccia **IAudioSessionEvents** .

Alcuni client potrebbero non essere interessati al monitoraggio di tutti i tipi di eventi di sessione. Nell'esempio di codice precedente, diversi metodi di notifica nella classe CAudioSessionEvents non eseguono alcuna operazione. Ad esempio, il metodo [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) non esegue alcuna operazione tranne per restituire il codice di stato \_ OK. Questa applicazione non monitora i volumi di canale perché non modifica i volumi del canale (chiamando i metodi nell'interfaccia [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) ) e non condivide la sessione con altre applicazioni che potrebbero modificare i volumi del canale.

Gli unici tre metodi della classe CAudioSessionEvents che inviano notifiche all'utente degli eventi di sessione sono [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)e [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Ad esempio, se l'utente esegue il programma di controllo del volume di sistema, sndvol, e usa il controllo volume in sndvol per modificare il livello di volume dell'applicazione, `OnSimpleVolumeChanged` stampa immediatamente il nuovo livello di volume.

Per un esempio di codice che registra e Annulla la registrazione dell'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) di un client, vedere [eventi audio per le applicazioni audio legacy](audio-events-for-legacy-audio-applications.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessioni audio](audio-sessions.md)
</dt> </dl>

 

 
