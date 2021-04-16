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
# <a name="audio-events-for-legacy-audio-applications"></a><span data-ttu-id="66732-103">Eventi audio per applicazioni audio legacy</span><span class="sxs-lookup"><span data-stu-id="66732-103">Audio Events for Legacy Audio Applications</span></span>

<span data-ttu-id="66732-104">Le API audio legacy, ad esempio DirectSound, DirectShow e le funzioni **waveOutXxx** , consentono alle applicazioni di ottenere e impostare i livelli di volume dei flussi audio.</span><span class="sxs-lookup"><span data-stu-id="66732-104">Legacy audio APIs such as DirectSound, DirectShow, and the **waveOutXxx** functions enable applications to get and set the volume levels of audio streams.</span></span> <span data-ttu-id="66732-105">Le applicazioni possono usare le funzionalità di controllo del volume in queste API per visualizzare i dispositivi di scorrimento del volume nelle finestre delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="66732-105">Applications can use the volume-control capabilities in these APIs to display volume sliders in their application windows.</span></span>

<span data-ttu-id="66732-106">In Windows Vista, il programma di controllo del volume di sistema, sndvol, consente agli utenti di controllare i livelli di volume audio per le singole applicazioni.</span><span class="sxs-lookup"><span data-stu-id="66732-106">In Windows Vista, the system volume-control program, Sndvol, allows users to control the audio volume levels for individual applications.</span></span> <span data-ttu-id="66732-107">I dispositivi di scorrimento del volume visualizzati dalle applicazioni devono essere collegati ai dispositivi di scorrimento del volume corrispondenti in sndvol.</span><span class="sxs-lookup"><span data-stu-id="66732-107">The volume sliders that are displayed by applications should be linked to the corresponding volume sliders in Sndvol.</span></span> <span data-ttu-id="66732-108">Se un utente modifica il volume dell'applicazione tramite un dispositivo di scorrimento del volume in una finestra dell'applicazione, il dispositivo di scorrimento del volume corrispondente in sndvol si sposta immediatamente per indicare il nuovo livello di volume.</span><span class="sxs-lookup"><span data-stu-id="66732-108">If a user adjusts the application volume through a volume slider in an application window, then the corresponding volume slider in Sndvol immediately moves to indicate the new volume level.</span></span> <span data-ttu-id="66732-109">Viceversa, se l'utente modifica il volume dell'applicazione tramite sndvol, i dispositivi di scorrimento del volume nella finestra dell'applicazione devono essere spostati per indicare il nuovo livello di volume.</span><span class="sxs-lookup"><span data-stu-id="66732-109">Conversely, if the user adjusts the application volume through Sndvol, then the volume sliders in the application window should move to indicate the new volume level.</span></span>

<span data-ttu-id="66732-110">In Windows Vista, sndvol riflette immediatamente le modifiche del volume effettuate da un'applicazione tramite chiamate al metodo **API IDirectSoundBuffer:: sevolume** o alla funzione **waveOutSetVolume** .</span><span class="sxs-lookup"><span data-stu-id="66732-110">In Windows Vista, Sndvol immediately reflects volume changes that an application makes through calls to the **IDirectSoundBuffer::SetVolume** method or **waveOutSetVolume** function.</span></span> <span data-ttu-id="66732-111">Tuttavia, un'API audio legacy, ad esempio DirectSound o le funzioni **waveOutXxx** , non fornisce alcun mezzo per notificare a un'applicazione quando l'utente modifica il volume dell'applicazione tramite sndvol.</span><span class="sxs-lookup"><span data-stu-id="66732-111">However, a legacy audio API such as DirectSound or the **waveOutXxx** functions provides no means to notify an application when the user changes the application volume through Sndvol.</span></span> <span data-ttu-id="66732-112">Se un'applicazione visualizza un dispositivo di scorrimento del volume ma non riceve notifiche delle modifiche del volume, il dispositivo di scorrimento non rileverà le modifiche apportate dall'utente in sndvol.</span><span class="sxs-lookup"><span data-stu-id="66732-112">If an application displays a volume slider but does not receive notifications of volume changes, then the slider will fail to reflect changes made by the user in Sndvol.</span></span> <span data-ttu-id="66732-113">Per implementare il comportamento appropriato, Progettazione applicazioni deve in qualche modo compensare la mancanza di notifiche da parte dell'API audio legacy.</span><span class="sxs-lookup"><span data-stu-id="66732-113">To implement the appropriate behavior, the application designer must somehow compensate for the lack of notifications by the legacy audio API.</span></span>

<span data-ttu-id="66732-114">Una soluzione può essere che l'applicazione imposti un timer per ricordarlo periodicamente di controllare il livello del volume per verificare se è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="66732-114">One solution might be for the application to set a timer to periodically remind it to check the volume level to see if it has changed.</span></span>

<span data-ttu-id="66732-115">Una soluzione più elegante consiste nell'usare le funzionalità di notifica degli eventi delle API di base per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="66732-115">A more elegant solution is for the application to use the event notification capabilities of the core audio APIs.</span></span> <span data-ttu-id="66732-116">In particolare, l'applicazione è in grado di registrare un'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) per ricevere callback quando si verificano modifiche al volume o altri tipi di eventi audio.</span><span class="sxs-lookup"><span data-stu-id="66732-116">In particular, the application can register an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface to receive callbacks when volume changes or other types of audio events occur.</span></span> <span data-ttu-id="66732-117">Quando il volume cambia, la routine di callback di modifica del volume può aggiornare immediatamente il dispositivo di scorrimento del volume dell'applicazione in modo da riflettere la modifica.</span><span class="sxs-lookup"><span data-stu-id="66732-117">When the volume changes, the volume-change callback routine can immediately update the application's volume slider to reflect the change.</span></span>

<span data-ttu-id="66732-118">L'esempio di codice seguente illustra come un'applicazione può registrarsi per ricevere notifiche di modifiche del volume e altri eventi audio:</span><span class="sxs-lookup"><span data-stu-id="66732-118">The following code example shows how an application can register to receive notifications of volume changes and other audio events:</span></span>


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



<span data-ttu-id="66732-119">Nell'esempio di codice precedente viene implementata una classe denominata AudioVolumeEvents.</span><span class="sxs-lookup"><span data-stu-id="66732-119">The preceding code example implements a class named AudioVolumeEvents.</span></span> <span data-ttu-id="66732-120">Durante l'inizializzazione del programma, l'applicazione audio Abilita le notifiche di eventi audio creando un oggetto AudioVolumeEvents.</span><span class="sxs-lookup"><span data-stu-id="66732-120">During program initialization, the audio application enables audio-event notifications by creating an AudioVolumeEvents object.</span></span> <span data-ttu-id="66732-121">Il costruttore per questa classe accetta tre parametri di input:</span><span class="sxs-lookup"><span data-stu-id="66732-121">The constructor for this class takes three input parameters:</span></span>

-   <span data-ttu-id="66732-122">*Flow*: la direzione del flusso di dati del [dispositivo dell'endpoint audio](audio-endpoint-devices.md) (un valore di enumerazione [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) ).</span><span class="sxs-lookup"><span data-stu-id="66732-122">*flow*—the data-flow direction of the [audio endpoint device](audio-endpoint-devices.md) (an [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) enumeration value).</span></span>
-   <span data-ttu-id="66732-123">*Role*: il [ruolo](device-roles.md) corrente del dispositivo dell'endpoint (un valore di enumerazione [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ).</span><span class="sxs-lookup"><span data-stu-id="66732-123">*role*—the current [device role](device-roles.md) of the endpoint device (an [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration value).</span></span>
-   <span data-ttu-id="66732-124">*pAudioEvents*: puntatore a un oggetto (un'istanza dell'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) ) che contiene un set di routine di callback implementate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="66732-124">*pAudioEvents*—pointer to an object (an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface instance) that contains a set of callback routines that are implemented by the application.</span></span>

<span data-ttu-id="66732-125">Il costruttore fornisce i valori del flusso e del ruolo come parametri di input al metodo [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) .</span><span class="sxs-lookup"><span data-stu-id="66732-125">The constructor supplies the flow and role values as input parameters to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method.</span></span> <span data-ttu-id="66732-126">Il metodo crea un oggetto [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) che incapsula il dispositivo dell'endpoint audio con la direzione del flusso di dati e il ruolo del dispositivo specificati.</span><span class="sxs-lookup"><span data-stu-id="66732-126">The method creates an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) object that encapsulates the audio endpoint device with the specified data-flow direction and device role.</span></span>

<span data-ttu-id="66732-127">L'applicazione implementa l'oggetto a cui fa riferimento *pAudioEvents*.</span><span class="sxs-lookup"><span data-stu-id="66732-127">The application implements the object pointed to by *pAudioEvents*.</span></span> <span data-ttu-id="66732-128">(L'implementazione non è illustrata nell'esempio di codice precedente.</span><span class="sxs-lookup"><span data-stu-id="66732-128">(The implementation is not shown in the preceding code example.</span></span> <span data-ttu-id="66732-129">Per un esempio di codice che implementa un'interfaccia **IAudioSessionEvents** , vedere [eventi di sessione audio](audio-session-events.md). Ogni metodo in questa interfaccia riceve le notifiche di un particolare tipo di evento audio.</span><span class="sxs-lookup"><span data-stu-id="66732-129">For a code example that implements an **IAudioSessionEvents** interface, see [Audio Session Events](audio-session-events.md).) Each method in this interface receives notifications of a particular type of audio event.</span></span> <span data-ttu-id="66732-130">Se l'applicazione non è interessata a un particolare tipo di evento, il metodo per quel tipo di evento non deve eseguire alcuna operazione ma restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="66732-130">If the application is not interested in a particular event type, then the method for that event type should do nothing but return S\_OK.</span></span>

<span data-ttu-id="66732-131">Il metodo [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) riceve le notifiche delle modifiche del volume.</span><span class="sxs-lookup"><span data-stu-id="66732-131">The [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) method receives notifications of volume changes.</span></span> <span data-ttu-id="66732-132">In genere, questo metodo aggiorna il dispositivo di scorrimento del volume dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="66732-132">Typically, this method updates the application's volume slider.</span></span>

<span data-ttu-id="66732-133">Nell'esempio di codice precedente, il costruttore per la classe AudioVolumeEvents registra per le notifiche nella [sessione audio](audio-sessions.md) specifica del processo identificata dal GUID di sessione valore \_ null.</span><span class="sxs-lookup"><span data-stu-id="66732-133">In the preceding code example, the constructor for the AudioVolumeEvents class registers for notifications on the process-specific [audio session](audio-sessions.md) that is identified by session GUID value GUID\_NULL.</span></span> <span data-ttu-id="66732-134">Per impostazione predefinita, le API audio legacy, ad esempio DirectSound, DirectShow e le funzioni **waveOutXxx** , assegnano i flussi a questa sessione.</span><span class="sxs-lookup"><span data-stu-id="66732-134">By default, legacy audio APIs such as DirectSound, DirectShow, and the **waveOutXxx** functions assign their streams to this session.</span></span> <span data-ttu-id="66732-135">Tuttavia, un'applicazione DirectSound o DirectShow può, in alternativa, eseguire l'override del comportamento predefinito e assegnare i flussi a una sessione tra processi o a una sessione identificata da un valore GUID diverso da GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="66732-135">However, a DirectSound or DirectShow application can, as an option, override the default behavior and assign its streams to a cross-process session or to a session that is identified by a GUID value other than GUID\_NULL.</span></span> <span data-ttu-id="66732-136">Non è attualmente disponibile alcun meccanismo che consente a un'applicazione **waveOutXxx** di eseguire l'override del comportamento predefinito in modo analogo. Per un esempio di codice di un'applicazione DirectShow con questo comportamento, vedere [ruoli del dispositivo per le applicazioni DirectShow](device-roles-for-directshow-applications.md).</span><span class="sxs-lookup"><span data-stu-id="66732-136">(No mechanism is currently provided for a **waveOutXxx** application to override the default behavior in a similar manner.) For a code example of a DirectShow application with this behavior, see [Device Roles for DirectShow Applications](device-roles-for-directshow-applications.md).</span></span> <span data-ttu-id="66732-137">Per supportare un'applicazione di questo tipo, è possibile modificare il costruttore nell'esempio di codice precedente per accettare due parametri di input aggiuntivi, ovvero un GUID della sessione e un flag per indicare se la sessione da monitorare è una sessione specifica del processo o tra processi.</span><span class="sxs-lookup"><span data-stu-id="66732-137">To accommodate such an application, you can modify the constructor in the preceding code example to accept two additional input parameters—a session GUID and a flag to indicate whether the session that is to be monitored is a cross-process or process-specific session.</span></span> <span data-ttu-id="66732-138">Passare questi parametri alla chiamata al metodo [**IAudioSessionManager:: GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) nel costruttore.</span><span class="sxs-lookup"><span data-stu-id="66732-138">Pass these parameters to the call to the [**IAudioSessionManager::GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) method in the constructor.</span></span>

<span data-ttu-id="66732-139">Dopo che il costruttore chiama il metodo [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) per la registrazione per le notifiche, l'applicazione continua a ricevere le notifiche solo a condizione che esista l'interfaccia [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) o [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) .</span><span class="sxs-lookup"><span data-stu-id="66732-139">After the constructor calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register for notifications, the application continues to receive notifications for only as long as either the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) or [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interface exists.</span></span> <span data-ttu-id="66732-140">L'oggetto AudioVolumeEvents nell'esempio di codice precedente include riferimenti a tali interfacce fino a quando non viene chiamato il relativo distruttore.</span><span class="sxs-lookup"><span data-stu-id="66732-140">The AudioVolumeEvents object in the preceding code example holds references to these interfaces until its destructor is called.</span></span> <span data-ttu-id="66732-141">Questo comportamento garantisce che l'applicazione continuerà a ricevere notifiche per la durata dell'oggetto AudioVolumeEvents.</span><span class="sxs-lookup"><span data-stu-id="66732-141">This behavior ensures that the application will continue to receive notifications for the lifetime of the AudioVolumeEvents object.</span></span>

<span data-ttu-id="66732-142">Anziché selezionare in modo implicito un dispositivo audio in base al relativo ruolo del dispositivo, un'applicazione multimediale Windows precedente o DirectSound potrebbe consentire all'utente di selezionare in modo esplicito un dispositivo da un elenco di dispositivi disponibili identificati dai relativi nomi descrittivi.</span><span class="sxs-lookup"><span data-stu-id="66732-142">Instead of implicitly selecting an audio device based on its device role, a DirectSound or legacy Windows multimedia application might allow the user to explicitly select a device from a list of available devices that are identified by their friendly names.</span></span> <span data-ttu-id="66732-143">Per supportare questo comportamento, è necessario modificare l'esempio di codice precedente per generare notifiche di eventi audio per il dispositivo selezionato.</span><span class="sxs-lookup"><span data-stu-id="66732-143">To support this behavior, the preceding code example must be modified to generate audio-event notifications for the selected device.</span></span> <span data-ttu-id="66732-144">Sono necessarie due modifiche.</span><span class="sxs-lookup"><span data-stu-id="66732-144">Two modifications are required.</span></span> <span data-ttu-id="66732-145">Per prima cosa, modificare la definizione del costruttore in modo che accetti una [stringa ID endpoint](endpoint-id-strings.md) come parametro di input (al posto dei parametri Flow e Role nell'esempio di codice).</span><span class="sxs-lookup"><span data-stu-id="66732-145">First, change the constructor definition to accept an [endpoint ID string](endpoint-id-strings.md) as an input parameter (in place of the flow and role parameters in the code example).</span></span> <span data-ttu-id="66732-146">Questa stringa identifica il dispositivo dell'endpoint audio che corrisponde al dispositivo DirectSound o alla forma d'onda legacy selezionato.</span><span class="sxs-lookup"><span data-stu-id="66732-146">This string identifies the audio endpoint device that corresponds to the selected DirectSound or legacy waveform device.</span></span> <span data-ttu-id="66732-147">In secondo luogo, sostituire la chiamata al metodo [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) con una chiamata al metodo [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="66732-147">Second, replace the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method with a call to the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="66732-148">La chiamata **GetDevice** accetta la stringa ID dell'endpoint come parametro di input e crea un'istanza del dispositivo endpoint identificato dalla stringa.</span><span class="sxs-lookup"><span data-stu-id="66732-148">The **GetDevice** call takes the endpoint ID string as an input parameter and creates an instance of the endpoint device that is identified by the string.</span></span>

<span data-ttu-id="66732-149">La tecnica per ottenere la stringa dell'ID endpoint per un dispositivo DirectSound o un dispositivo di forma d'onda legacy è la seguente.</span><span class="sxs-lookup"><span data-stu-id="66732-149">The technique for obtaining the endpoint ID string for a DirectSound device or legacy waveform device is as follows.</span></span>

<span data-ttu-id="66732-150">In primo luogo, durante l'enumerazione dei dispositivi, DirectSound fornisce la stringa dell'ID endpoint per ogni dispositivo enumerato.</span><span class="sxs-lookup"><span data-stu-id="66732-150">First, during device enumeration, DirectSound supplies the endpoint ID string for each enumerated device.</span></span> <span data-ttu-id="66732-151">Per iniziare l'enumerazione dei dispositivi, l'applicazione passa un puntatore alla funzione di callback come parametro di input per la funzione **DirectSoundCreate** o **DirectSoundCaptureCreate** .</span><span class="sxs-lookup"><span data-stu-id="66732-151">To begin device enumeration, the application passes a callback function pointer as an input parameter to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function.</span></span> <span data-ttu-id="66732-152">La definizione della funzione di callback è la seguente:</span><span class="sxs-lookup"><span data-stu-id="66732-152">The definition of the callback function is:</span></span>


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



<span data-ttu-id="66732-153">In Windows Vista, il parametro *lpcstrModule* punta alla stringa dell'ID endpoint.</span><span class="sxs-lookup"><span data-stu-id="66732-153">In Windows Vista, the *lpcstrModule* parameter points to the endpoint ID string.</span></span> <span data-ttu-id="66732-154">Nelle versioni precedenti di Windows, tra cui Windows Server 2003, Windows XP e Windows 2000, il parametro *lpcstrModule* punta al nome del modulo driver per il dispositivo. Il parametro *lpcstrDescription* punta a una stringa che contiene il nome descrittivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66732-154">(In earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000, the *lpcstrModule* parameter points to the name of the driver module for the device.) The *lpcstrDescription* parameter points to a string that contains the friendly name of the device.</span></span> <span data-ttu-id="66732-155">Per ulteriori informazioni sull'enumerazione dei dispositivi DirectSound, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="66732-155">For more information about DirectSound device enumeration, see the Windows SDK documentation.</span></span>

<span data-ttu-id="66732-156">In secondo luogo, per ottenere la stringa dell'ID endpoint per un dispositivo di forma d'onda legacy, usare la funzione **waveOutMessage** o **waveInMessage** per inviare un \_ messaggio DRV QUERYFUNCTIONINSTANCEID al driver di dispositivo waveform.</span><span class="sxs-lookup"><span data-stu-id="66732-156">Second, to obtain the endpoint ID string for a legacy waveform device, use the **waveOutMessage** or **waveInMessage** function to send a DRV\_QUERYFUNCTIONINSTANCEID message to the waveform device driver.</span></span> <span data-ttu-id="66732-157">Per un esempio di codice che illustra l'uso di questo messaggio, vedere [ruoli del dispositivo per le applicazioni Windows multimediali legacy](device-roles-for-legacy-windows-multimedia-applications.md).</span><span class="sxs-lookup"><span data-stu-id="66732-157">For a code example that shows the use of this message, see [Device Roles for Legacy Windows Multimedia Applications](device-roles-for-legacy-windows-multimedia-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="66732-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66732-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66732-159">Interoperabilità con le API audio legacy</span><span class="sxs-lookup"><span data-stu-id="66732-159">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



