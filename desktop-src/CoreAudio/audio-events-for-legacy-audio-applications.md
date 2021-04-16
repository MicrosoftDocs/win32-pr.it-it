---
description: Eventi audio per applicazioni audio legacy
ms.assetid: 91a93b79-2563-4b25-af5d-ca5f7d35d77b
title: Eventi audio per applicazioni audio legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fe99195910b1c1c68c0f3a1b39dd2706dde0be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127675"
---
# <a name="audio-events-for-legacy-audio-applications"></a>Eventi audio per applicazioni audio legacy

Le API audio legacy, ad esempio DirectSound, DirectShow e le funzioni **waveOutXxx** , consentono alle applicazioni di ottenere e impostare i livelli di volume dei flussi audio. Le applicazioni possono usare le funzionalità di controllo del volume in queste API per visualizzare i dispositivi di scorrimento del volume nelle finestre delle applicazioni.

In Windows Vista, il programma di controllo del volume di sistema, sndvol, consente agli utenti di controllare i livelli di volume audio per le singole applicazioni. I dispositivi di scorrimento del volume visualizzati dalle applicazioni devono essere collegati ai dispositivi di scorrimento del volume corrispondenti in sndvol. Se un utente modifica il volume dell'applicazione tramite un dispositivo di scorrimento del volume in una finestra dell'applicazione, il dispositivo di scorrimento del volume corrispondente in sndvol si sposta immediatamente per indicare il nuovo livello di volume. Viceversa, se l'utente modifica il volume dell'applicazione tramite sndvol, i dispositivi di scorrimento del volume nella finestra dell'applicazione devono essere spostati per indicare il nuovo livello di volume.

In Windows Vista, sndvol riflette immediatamente le modifiche del volume effettuate da un'applicazione tramite chiamate al metodo **API IDirectSoundBuffer:: sevolume** o alla funzione **waveOutSetVolume** . Tuttavia, un'API audio legacy, ad esempio DirectSound o le funzioni **waveOutXxx** , non fornisce alcun mezzo per notificare a un'applicazione quando l'utente modifica il volume dell'applicazione tramite sndvol. Se un'applicazione visualizza un dispositivo di scorrimento del volume ma non riceve notifiche delle modifiche del volume, il dispositivo di scorrimento non rileverà le modifiche apportate dall'utente in sndvol. Per implementare il comportamento appropriato, Progettazione applicazioni deve in qualche modo compensare la mancanza di notifiche da parte dell'API audio legacy.

Una soluzione può essere che l'applicazione imposti un timer per ricordarlo periodicamente di controllare il livello del volume per verificare se è stato modificato.

Una soluzione più elegante consiste nell'usare le funzionalità di notifica degli eventi delle API di base per l'applicazione. In particolare, l'applicazione è in grado di registrare un'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) per ricevere callback quando si verificano modifiche al volume o altri tipi di eventi audio. Quando il volume cambia, la routine di callback di modifica del volume può aggiornare immediatamente il dispositivo di scorrimento del volume dell'applicazione in modo da riflettere la modifica.

L'esempio di codice seguente illustra come un'applicazione può registrarsi per ricevere notifiche di modifiche del volume e altri eventi audio:


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



Nell'esempio di codice precedente viene implementata una classe denominata AudioVolumeEvents. Durante l'inizializzazione del programma, l'applicazione audio Abilita le notifiche di eventi audio creando un oggetto AudioVolumeEvents. Il costruttore per questa classe accetta tre parametri di input:

-   *Flow*: la direzione del flusso di dati del [dispositivo dell'endpoint audio](audio-endpoint-devices.md) (un valore di enumerazione [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) ).
-   *Role*: il [ruolo](device-roles.md) corrente del dispositivo dell'endpoint (un valore di enumerazione [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ).
-   *pAudioEvents*: puntatore a un oggetto (un'istanza dell'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) ) che contiene un set di routine di callback implementate dall'applicazione.

Il costruttore fornisce i valori del flusso e del ruolo come parametri di input al metodo [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) . Il metodo crea un oggetto [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) che incapsula il dispositivo dell'endpoint audio con la direzione del flusso di dati e il ruolo del dispositivo specificati.

L'applicazione implementa l'oggetto a cui fa riferimento *pAudioEvents*. (L'implementazione non è illustrata nell'esempio di codice precedente. Per un esempio di codice che implementa un'interfaccia **IAudioSessionEvents** , vedere [eventi di sessione audio](audio-session-events.md). Ogni metodo in questa interfaccia riceve le notifiche di un particolare tipo di evento audio. Se l'applicazione non è interessata a un particolare tipo di evento, il metodo per quel tipo di evento non deve eseguire alcuna operazione ma restituisce S \_ OK.

Il metodo [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) riceve le notifiche delle modifiche del volume. In genere, questo metodo aggiorna il dispositivo di scorrimento del volume dell'applicazione.

Nell'esempio di codice precedente, il costruttore per la classe AudioVolumeEvents registra per le notifiche nella [sessione audio](audio-sessions.md) specifica del processo identificata dal GUID di sessione valore \_ null. Per impostazione predefinita, le API audio legacy, ad esempio DirectSound, DirectShow e le funzioni **waveOutXxx** , assegnano i flussi a questa sessione. Tuttavia, un'applicazione DirectSound o DirectShow può, in alternativa, eseguire l'override del comportamento predefinito e assegnare i flussi a una sessione tra processi o a una sessione identificata da un valore GUID diverso da GUID \_ null. Non è attualmente disponibile alcun meccanismo che consente a un'applicazione **waveOutXxx** di eseguire l'override del comportamento predefinito in modo analogo. Per un esempio di codice di un'applicazione DirectShow con questo comportamento, vedere [ruoli del dispositivo per le applicazioni DirectShow](device-roles-for-directshow-applications.md). Per supportare un'applicazione di questo tipo, è possibile modificare il costruttore nell'esempio di codice precedente per accettare due parametri di input aggiuntivi, ovvero un GUID della sessione e un flag per indicare se la sessione da monitorare è una sessione specifica del processo o tra processi. Passare questi parametri alla chiamata al metodo [**IAudioSessionManager:: GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) nel costruttore.

Dopo che il costruttore chiama il metodo [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) per la registrazione per le notifiche, l'applicazione continua a ricevere le notifiche solo a condizione che esista l'interfaccia [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) o [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) . L'oggetto AudioVolumeEvents nell'esempio di codice precedente include riferimenti a tali interfacce fino a quando non viene chiamato il relativo distruttore. Questo comportamento garantisce che l'applicazione continuerà a ricevere notifiche per la durata dell'oggetto AudioVolumeEvents.

Anziché selezionare in modo implicito un dispositivo audio in base al relativo ruolo del dispositivo, un'applicazione multimediale Windows precedente o DirectSound potrebbe consentire all'utente di selezionare in modo esplicito un dispositivo da un elenco di dispositivi disponibili identificati dai relativi nomi descrittivi. Per supportare questo comportamento, è necessario modificare l'esempio di codice precedente per generare notifiche di eventi audio per il dispositivo selezionato. Sono necessarie due modifiche. Per prima cosa, modificare la definizione del costruttore in modo che accetti una [stringa ID endpoint](endpoint-id-strings.md) come parametro di input (al posto dei parametri Flow e Role nell'esempio di codice). Questa stringa identifica il dispositivo dell'endpoint audio che corrisponde al dispositivo DirectSound o alla forma d'onda legacy selezionato. In secondo luogo, sostituire la chiamata al metodo [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) con una chiamata al metodo [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) . La chiamata **GetDevice** accetta la stringa ID dell'endpoint come parametro di input e crea un'istanza del dispositivo endpoint identificato dalla stringa.

La tecnica per ottenere la stringa dell'ID endpoint per un dispositivo DirectSound o un dispositivo di forma d'onda legacy è la seguente.

In primo luogo, durante l'enumerazione dei dispositivi, DirectSound fornisce la stringa dell'ID endpoint per ogni dispositivo enumerato. Per iniziare l'enumerazione dei dispositivi, l'applicazione passa un puntatore alla funzione di callback come parametro di input per la funzione **DirectSoundCreate** o **DirectSoundCaptureCreate** . La definizione della funzione di callback è la seguente:


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



In Windows Vista, il parametro *lpcstrModule* punta alla stringa dell'ID endpoint. Nelle versioni precedenti di Windows, tra cui Windows Server 2003, Windows XP e Windows 2000, il parametro *lpcstrModule* punta al nome del modulo driver per il dispositivo. Il parametro *lpcstrDescription* punta a una stringa che contiene il nome descrittivo del dispositivo. Per ulteriori informazioni sull'enumerazione dei dispositivi DirectSound, vedere la documentazione Windows SDK.

In secondo luogo, per ottenere la stringa dell'ID endpoint per un dispositivo di forma d'onda legacy, usare la funzione **waveOutMessage** o **waveInMessage** per inviare un \_ messaggio DRV QUERYFUNCTIONINSTANCEID al driver di dispositivo waveform. Per un esempio di codice che illustra l'uso di questo messaggio, vedere [ruoli del dispositivo per le applicazioni Windows multimediali legacy](device-roles-for-legacy-windows-multimedia-applications.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interoperabilità con le API audio legacy](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



