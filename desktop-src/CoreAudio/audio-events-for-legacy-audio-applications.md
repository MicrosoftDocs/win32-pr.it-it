---
description: Eventi audio per applicazioni audio legacy
ms.assetid: 91a93b79-2563-4b25-af5d-ca5f7d35d77b
title: Eventi audio per applicazioni audio legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e030561123ba8501a66a2837bcc323a6505226a80c385f3dcaa532b2e6cd8c58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018489"
---
# <a name="audio-events-for-legacy-audio-applications"></a>Eventi audio per applicazioni audio legacy

Le API audio legacy, ad esempio DirectSound, DirectShow e le funzioni **waveOutXxx,** consentono alle applicazioni di ottenere e impostare i livelli di volume dei flussi audio. Le applicazioni possono usare le funzionalità di controllo del volume in queste API per visualizzare i dispositivi di scorrimento del volume nelle finestre dell'applicazione.

In Windows Vista, il programma di controllo del volume di sistema, Sndvol, consente agli utenti di controllare i livelli di volume audio per le singole applicazioni. I dispositivi di scorrimento del volume visualizzati dalle applicazioni devono essere collegati ai dispositivi di scorrimento del volume corrispondenti in Sndvol. Se un utente regola il volume dell'applicazione tramite un dispositivo di scorrimento del volume in una finestra dell'applicazione, il dispositivo di scorrimento del volume corrispondente in Sndvol si sposta immediatamente per indicare il nuovo livello di volume. Al contrario, se l'utente regola il volume dell'applicazione tramite Sndvol, i dispositivi di scorrimento del volume nella finestra dell'applicazione devono essere spostati per indicare il nuovo livello di volume.

In Windows Vista, Sndvol riflette immediatamente le modifiche al volume apportate da un'applicazione tramite chiamate al metodo **IDirectSoundBuffer::SetVolume** o alla funzione **waveOutSetVolume.** Tuttavia, un'API audio legacy, ad esempio DirectSound o le funzioni **waveOutXxx,** non consente di inviare notifiche a un'applicazione quando l'utente modifica il volume dell'applicazione tramite Sndvol. Se un'applicazione visualizza un dispositivo di scorrimento del volume ma non riceve notifiche di modifiche del volume, il dispositivo di scorrimento non rifletterà le modifiche apportate dall'utente in Sndvol. Per implementare il comportamento appropriato, la finestra di progettazione dell'applicazione deve in qualche modo compensare la mancanza di notifiche da parte dell'API audio legacy.

Una soluzione potrebbe essere che l'applicazione imposta un timer per ricordargli periodicamente di controllare il livello del volume per verificare se è stato modificato.

Una soluzione più elegante è che l'applicazione usi le funzionalità di notifica degli eventi delle API audio principali. In particolare, l'applicazione può registrare [**un'interfaccia IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) per ricevere callback quando si verificano modifiche del volume o altri tipi di eventi audio. Quando il volume cambia, la routine di callback di modifica del volume può aggiornare immediatamente il dispositivo di scorrimento del volume dell'applicazione per riflettere la modifica.

L'esempio di codice seguente illustra come un'applicazione può registrarsi per ricevere notifiche relative alle modifiche del volume e ad altri eventi audio:


```C++
//-----------------------------------------------------------
// Register the application to receive notifications when the
// volume level changes on the default process-specific audio
// session (with session GUID value GUID_NULL) on the audio
// endpoint device with the specified data-flow direction
// (eRender or eCapture) and device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class AudioVolumeEvents
{
    HRESULT _hrStatus;
    IAudioSessionManager *_pManager;
    IAudioSessionControl *_pControl;
    IAudioSessionEvents *_pAudioEvents;
public:
    AudioVolumeEvents(EDataFlow, ERole, IAudioSessionEvents*);
    ~AudioVolumeEvents();
    HRESULT GetStatus() { return _hrStatus; };
};

// Constructor
AudioVolumeEvents::AudioVolumeEvents(EDataFlow flow, ERole role,
                                     IAudioSessionEvents *pAudioEvents)
{
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    _hrStatus = S_OK;
    _pManager = NULL;
    _pControl = NULL;
    _pAudioEvents = pAudioEvents;

    if (_pAudioEvents == NULL)
    {
        _hrStatus = E_POINTER;
        return;
    }

    _pAudioEvents->AddRef();

    // Get the enumerator for the audio endpoint devices
    // on this system.
    _hrStatus = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                                 NULL, CLSCTX_INPROC_SERVER,
                                 __uuidof(IMMDeviceEnumerator),
                                 (void**)&pEnumerator);
    EXIT_ON_ERROR(_hrStatus)

    // Get the audio endpoint device with the specified data-flow
    // direction (eRender or eCapture) and device role.
    _hrStatus = pEnumerator->GetDefaultAudioEndpoint(flow, role,
                                                     &pDevice);
    EXIT_ON_ERROR(_hrStatus)

    // Get the session manager for the endpoint device.
    _hrStatus = pDevice->Activate(__uuidof(IAudioSessionManager),
                                  CLSCTX_INPROC_SERVER, NULL,
                                  (void**)&_pManager);
    EXIT_ON_ERROR(_hrStatus)

    // Get the control interface for the process-specific audio
    // session with session GUID = GUID_NULL. This is the session
    // that an audio stream for a DirectSound, DirectShow, waveOut,
    // or PlaySound application stream belongs to by default.
    _hrStatus = _pManager->GetAudioSessionControl(NULL, 0, &_pControl);
    EXIT_ON_ERROR(_hrStatus)

    _hrStatus = _pControl->RegisterAudioSessionNotification(_pAudioEvents);
    EXIT_ON_ERROR(_hrStatus)

Exit:
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
}

// Destructor
AudioVolumeEvents::~AudioVolumeEvents()
{
    if (_pControl != NULL)
    {
        _pControl->UnregisterAudioSessionNotification(_pAudioEvents);
    }
    SAFE_RELEASE(_pManager)
    SAFE_RELEASE(_pControl)
    SAFE_RELEASE(_pAudioEvents)
};
```



L'esempio di codice precedente implementa una classe denominata AudioVolumeEvents. Durante l'inizializzazione del programma, l'applicazione audio abilita le notifiche degli eventi audio creando un oggetto AudioVolumeEvents. Il costruttore per questa classe accetta tre parametri di input:

-   *flow:* direzione del flusso di dati del dispositivo [endpoint audio](audio-endpoint-devices.md) (valore di [**enumerazione EDataFlow).**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow)
-   *role:* ruolo del [dispositivo endpoint corrente](device-roles.md) (valore di enumerazione [**ERole).**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)
-   *pAudioEvents:* puntatore a un oggetto (un'istanza [**dell'interfaccia IAudioSessionEvents)**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) che contiene un set di routine di callback implementate dall'applicazione.

Il costruttore fornisce i valori del flusso e del ruolo come parametri di input al metodo [**IMMDeviceEnumerator::GetDefaultAudioEndpoint.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) Il metodo crea un [**oggetto IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) che incapsula il dispositivo endpoint audio con la direzione del flusso di dati e il ruolo del dispositivo specificati.

L'applicazione implementa l'oggetto a cui *punta pAudioEvents*. L'implementazione non è illustrata nell'esempio di codice precedente. Per un esempio di codice che implementa **un'interfaccia IAudioSessionEvents,** vedere [Eventi di sessione audio.](audio-session-events.md) Ogni metodo in questa interfaccia riceve notifiche di un particolare tipo di evento audio. Se l'applicazione non è interessata a un particolare tipo di evento, il metodo per tale tipo di evento non deve eseguire alcuna operazione, ma restituire S \_ OK.

Il [**metodo IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) riceve notifiche delle modifiche del volume. In genere, questo metodo aggiorna il dispositivo di scorrimento del volume dell'applicazione.

Nell'esempio di codice precedente il costruttore per la classe AudioVolumeEvents registra per le notifiche nella sessione [audio](audio-sessions.md) specifica del processo identificata dal valore GUID della sessione \_ GUID NULL. Per impostazione predefinita, le API audio legacy, ad esempio DirectSound, DirectShow e le funzioni **waveOutXxx,** assegnano i flussi a questa sessione. Tuttavia, un'applicazione DirectSound o DirectShow può, come opzione, eseguire l'override del comportamento predefinito e assegnare i relativi flussi a una sessione tra processi o a una sessione identificata da un valore GUID diverso da GUID \_ NULL. Non è attualmente disponibile alcun meccanismo per **un'applicazione waveOutXxx** per eseguire l'override del comportamento predefinito in modo simile. Per un esempio di codice di un'DirectShow con questo comportamento, vedere Ruoli del dispositivo [per DirectShow applicazioni](device-roles-for-directshow-applications.md). Per supportare un'applicazione di questo tipo, è possibile modificare il costruttore nell'esempio di codice precedente in modo da accettare due parametri di input aggiuntivi, ovvero un GUID di sessione e un flag per indicare se la sessione da monitorare è una sessione tra processi o specifica del processo. Passare questi parametri alla chiamata al [**metodo IAudioSessionManager::GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) nel costruttore.

Dopo che il costruttore ha chiamato il metodo [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) per la registrazione per le notifiche, l'applicazione continua a ricevere notifiche solo per il tempo in cui esiste [**l'interfaccia IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) o [**IAudioSessionManager.**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) L'oggetto AudioVolumeEvents nell'esempio di codice precedente contiene riferimenti a queste interfacce fino a quando non viene chiamato il distruttore. Questo comportamento garantisce che l'applicazione continuerà a ricevere notifiche per la durata dell'oggetto AudioVolumeEvents.

Invece di selezionare in modo implicito un dispositivo audio in base al ruolo del dispositivo, un'applicazione multimediale DirectSound o Windows legacy potrebbe consentire all'utente di selezionare in modo esplicito un dispositivo da un elenco di dispositivi disponibili identificati dai nomi descrittivi. Per supportare questo comportamento, è necessario modificare l'esempio di codice precedente per generare notifiche di eventi audio per il dispositivo selezionato. Sono necessarie due modifiche. Modificare prima di tutto la definizione del costruttore in modo che accetti una stringa [di ID endpoint](endpoint-id-strings.md) come parametro di input (al posto dei parametri del flusso e del ruolo nell'esempio di codice). Questa stringa identifica il dispositivo endpoint audio che corrisponde al dispositivo DirectSound o alla forma d'onda legacy selezionato. Sostituire quindi la chiamata al metodo [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) con una chiamata al metodo [**IMMDeviceEnumerator::GetDevice.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) La **chiamata GetDevice** accetta la stringa dell'ID endpoint come parametro di input e crea un'istanza del dispositivo endpoint identificata dalla stringa.

La tecnica per ottenere la stringa di ID endpoint per un dispositivo DirectSound o un dispositivo waveform legacy è la seguente.

In primo luogo, durante l'enumerazione del dispositivo, DirectSound fornisce la stringa dell'ID endpoint per ogni dispositivo enumerato. Per iniziare l'enumerazione dei dispositivi, l'applicazione passa un puntatore a funzione di callback come parametro di input alla **funzione DirectSoundCreate** **o DirectSoundCaptureCreate.** La definizione della funzione di callback è:


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



In Windows Vista, il *parametro lpcstrModule* punta alla stringa dell'ID endpoint. Nelle versioni precedenti di Windows, tra cui Windows Server 2003, Windows XP e Windows 2000, il parametro *lpcstrModule* punta al nome del modulo driver per il dispositivo. Il *parametro lpcstrDescription* punta a una stringa che contiene il nome descrittivo del dispositivo. Per altre informazioni sull'enumerazione dei dispositivi DirectSound, vedere la documentazione Windows SDK.

In secondo momento, per ottenere la stringa dell'ID endpoint per un dispositivo waveform legacy, usare la funzione **waveOutMessage** o **waveInMessage** per inviare un messaggio DRV QUERYFUNCTIONINSTANCEID al driver del dispositivo \_ waveform. Per un esempio di codice che illustra l'uso di questo messaggio, vedere Ruoli del dispositivo per applicazioni [Windows multimediali](device-roles-for-legacy-windows-multimedia-applications.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interoperabilità con LE API audio legacy](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



