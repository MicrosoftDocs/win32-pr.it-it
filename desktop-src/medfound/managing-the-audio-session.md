---
description: In questo argomento viene descritto come controllare il volume audio quando si usa MFPlay per la riproduzione audio/video.
ms.assetid: 4cf3dd0f-4c8a-4720-9eb3-d23352f3a85e
title: Gestione della sessione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e5231ca02603279675fabaaac4b96a1cd001906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342656"
---
# <a name="managing-the-audio-session"></a><span data-ttu-id="752ff-103">Gestione della sessione audio</span><span class="sxs-lookup"><span data-stu-id="752ff-103">Managing the Audio Session</span></span>

<span data-ttu-id="752ff-104">\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="752ff-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="752ff-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="752ff-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="752ff-106">\]</span><span class="sxs-lookup"><span data-stu-id="752ff-106">\]</span></span>

<span data-ttu-id="752ff-107">In questo argomento viene descritto come controllare il volume audio quando si usa MFPlay per la riproduzione audio/video.</span><span class="sxs-lookup"><span data-stu-id="752ff-107">This topic describes how to control audio volume when using MFPlay for audio/video playback.</span></span>

<span data-ttu-id="752ff-108">MFPlay fornisce i metodi seguenti per controllare il volume audio durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="752ff-108">MFPlay provides the following methods to control the audio volume during playback.</span></span>



| <span data-ttu-id="752ff-109">Metodo</span><span class="sxs-lookup"><span data-stu-id="752ff-109">Method</span></span>                                                            | <span data-ttu-id="752ff-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="752ff-110">Description</span></span>                                           |
|-------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="752ff-111">**IMFPMediaPlayer:: sebalance**</span><span class="sxs-lookup"><span data-stu-id="752ff-111">**IMFPMediaPlayer::SetBalance**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance) | <span data-ttu-id="752ff-112">Imposta il saldo tra i canali sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="752ff-112">Sets the balance between the left and right channels.</span></span> |
| [<span data-ttu-id="752ff-113">**IMFPMediaPlayer:: semute**</span><span class="sxs-lookup"><span data-stu-id="752ff-113">**IMFPMediaPlayer::SetMute**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute)       | <span data-ttu-id="752ff-114">Disattiva o disattiva l'audio.</span><span class="sxs-lookup"><span data-stu-id="752ff-114">Mutes or unmutes the audio.</span></span>                           |
| [<span data-ttu-id="752ff-115">**IMFPMediaPlayer:: sevolume**</span><span class="sxs-lookup"><span data-stu-id="752ff-115">**IMFPMediaPlayer::SetVolume**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume)   | <span data-ttu-id="752ff-116">Imposta il livello del volume.</span><span class="sxs-lookup"><span data-stu-id="752ff-116">Sets the volume level.</span></span>                                |



 

<span data-ttu-id="752ff-117">Per comprendere il comportamento di questi metodi, è necessario conoscere alcuni termini dell'API di sessione audio (WASAPI) di Windows, che implementa la funzionalità audio di basso livello utilizzata da MFPlay.</span><span class="sxs-lookup"><span data-stu-id="752ff-117">To understand the behavior of these methods, you must know some terminology from the Windows Audio Session API (WASAPI), which implements the low-level audio functionality used by MFPlay.</span></span>

<span data-ttu-id="752ff-118">In WASAPI ogni flusso audio appartiene esattamente a una *sessione audio*, che è un gruppo di flussi audio correlati.</span><span class="sxs-lookup"><span data-stu-id="752ff-118">In WASAPI, every audio stream belongs to exactly one *audio session*, which is a group of related audio streams.</span></span> <span data-ttu-id="752ff-119">In genere, un'applicazione gestisce una singola sessione audio, sebbene le applicazioni possano creare più di una sessione.</span><span class="sxs-lookup"><span data-stu-id="752ff-119">Typically, an application maintains a single audio session, although applications can create more than one session.</span></span> <span data-ttu-id="752ff-120">Il programma di controllo del volume di sistema (sndvol) Visualizza un controllo volume per ogni sessione audio.</span><span class="sxs-lookup"><span data-stu-id="752ff-120">The system volume-control program (Sndvol) displays a volume control for each audio session.</span></span> <span data-ttu-id="752ff-121">Tramite sndvol, un utente può modificare il volume di una sessione audio dall'esterno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="752ff-121">Through Sndvol, a user can adjust the volume of an audio session from outside of the application.</span></span> <span data-ttu-id="752ff-122">Questo processo è illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="752ff-122">The following image illustrates this process.</span></span>

![diagramma che mostra i flussi audio che passano attraverso il controllo del volume sulla strada agli altoparlanti; applicazione e punto di sndvol al controllo del volume](images/audio-session.gif)

<span data-ttu-id="752ff-124">In MFPlay un elemento multimediale può avere uno o più flussi audio attivi (in genere solo uno).</span><span class="sxs-lookup"><span data-stu-id="752ff-124">In MFPlay, a media item can have one or more active audio streams (typically only one).</span></span> <span data-ttu-id="752ff-125">Internamente, MFPlay usa il [renderer di streaming audio](streaming-audio-renderer.md) (SAR) per eseguire il rendering dei flussi audio.</span><span class="sxs-lookup"><span data-stu-id="752ff-125">Internally, MFPlay uses the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) to render the audio streams.</span></span> <span data-ttu-id="752ff-126">A meno che non venga configurato in caso contrario, il SAR viene aggiunto alla sessione audio predefinita dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="752ff-126">Unless you configure it otherwise, the SAR joins the application's default audio session.</span></span>

<span data-ttu-id="752ff-127">I metodi audio MFPlay controllano solo i flussi che appartengono all'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="752ff-127">The MFPlay audio methods control only the streams that belong to the current media item.</span></span> <span data-ttu-id="752ff-128">Non influiscono sul volume per tutti gli altri flussi che appartengono alla stessa sessione audio.</span><span class="sxs-lookup"><span data-stu-id="752ff-128">They do not affect the volume for any other streams that belong to the same audio session.</span></span> <span data-ttu-id="752ff-129">In termini di WASAPI, i metodi MFPlay controllano i livelli del volume *per canale* , non il livello del volume master.</span><span class="sxs-lookup"><span data-stu-id="752ff-129">In terms of WASAPI, the MFPlay methods control the *per-channel* volume levels, not the master volume level.</span></span> <span data-ttu-id="752ff-130">Questo processo è illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="752ff-130">The following image illustrates this process.</span></span>

![diagramma simile a quello precedente, ma il secondo flusso inizia in corrispondenza dell'elemento multimediale e l'applicazione punta al secondo flusso e al controllo del volume](images/audio-session02.gif)

<span data-ttu-id="752ff-132">È importante comprendere alcune implicazioni di questa funzionalità di MFPlay.</span><span class="sxs-lookup"><span data-stu-id="752ff-132">It is important to understand some implications of this feature of MFPlay.</span></span> <span data-ttu-id="752ff-133">In primo luogo, un'applicazione può modificare il volume di riproduzione senza influire sugli altri flussi audio.</span><span class="sxs-lookup"><span data-stu-id="752ff-133">First, an application can adjust the playback volume without affecting other audio streams.</span></span> <span data-ttu-id="752ff-134">È possibile usare questa funzionalità se MFPlay per implementare la dissolvenza incrociata audio, creando due istanze dell'oggetto MFPlay e modificando il volume separatamente.</span><span class="sxs-lookup"><span data-stu-id="752ff-134">You could use this feature if MFPlay to implement audio cross-fading, by creating two instances of the MFPlay object and adjusting the volume separately.</span></span>

<span data-ttu-id="752ff-135">Se si usano i metodi MFPlay per modificare lo stato del volume o del silenziamento, le modifiche non vengono visualizzate in sndvol.</span><span class="sxs-lookup"><span data-stu-id="752ff-135">If you use MFPlay methods to change the volume or mute state, the changes do not appear in Sndvol.</span></span> <span data-ttu-id="752ff-136">Ad esempio, è possibile chiamare il tasto di [**disattivazione**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) per disattivare l'audio, ma sndvol non visualizzerà la sessione come disabilitata.</span><span class="sxs-lookup"><span data-stu-id="752ff-136">For example, you can call [**SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) to mute the audio, but Sndvol will not show the session as muted.</span></span> <span data-ttu-id="752ff-137">Viceversa, se per modificare il volume di sessione viene usato SndVol, le modifiche non vengono riflesse nei valori restituiti da [**IMFPMediaPlayer:: GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) o [**IMFPMediaPlayer:: getmute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).</span><span class="sxs-lookup"><span data-stu-id="752ff-137">Conversely, if SndVol is used to adjust the session volume, the changes are not reflected in the values returned by [**IMFPMediaPlayer::GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) or [**IMFPMediaPlayer::GetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).</span></span>

<span data-ttu-id="752ff-138">Per ogni istanza dell'oggetto MFPlay Player, il livello di volume effettivo è uguale a *fPlayerVolume* × *FSessionVolume*, dove *fPlayerVolume* è il valore restituito da [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume)e *fSessionVolume* è il volume master per la sessione.</span><span class="sxs-lookup"><span data-stu-id="752ff-138">For each instance of the MFPlay player object, the effective volume level equals *fPlayerVolume* × *fSessionVolume*, where *fPlayerVolume* is the value returned by [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume), and *fSessionVolume* is the master volume for the session.</span></span>

<span data-ttu-id="752ff-139">Per gli scenari di riproduzione semplici, potrebbe essere preferibile usare WASAPI per controllare il volume audio per l'intera sessione, anziché usare i metodi MFPlay.</span><span class="sxs-lookup"><span data-stu-id="752ff-139">For simple playback scenarios, it might be preferable to use the WASAPI to control the audio volume for the entire session, rather than use the MFPlay methods.</span></span>

## <a name="example-code"></a><span data-ttu-id="752ff-140">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="752ff-140">Example Code</span></span>

<span data-ttu-id="752ff-141">Di seguito è riportata una classe C++ che gestisce le attività di base in WASAPI:</span><span class="sxs-lookup"><span data-stu-id="752ff-141">What follows is a C++ class that handles the basic tasks in WASAPI:</span></span>

-   <span data-ttu-id="752ff-142">Controllo del volume e dello stato di silenziamento per la sessione.</span><span class="sxs-lookup"><span data-stu-id="752ff-142">Controlling the volume and mute state for the session.</span></span>
-   <span data-ttu-id="752ff-143">Recupero di notifiche ogni volta che viene modificato lo stato del volume o del silenziamento.</span><span class="sxs-lookup"><span data-stu-id="752ff-143">Getting notifications whenever the volume or mute state change.</span></span>

### <a name="class-declaration"></a><span data-ttu-id="752ff-144">Dichiarazione di classe</span><span class="sxs-lookup"><span data-stu-id="752ff-144">Class Declaration</span></span>

<span data-ttu-id="752ff-145">La `CAudioSessionVolume` dichiarazione di classe implementa l'interfaccia [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) , ovvero l'interfaccia di callback per gli eventi di sessione audio.</span><span class="sxs-lookup"><span data-stu-id="752ff-145">The `CAudioSessionVolume` class declaration implements the [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) interface, which is the callback interface for audio session events.</span></span>


```C++
class CAudioSessionVolume : public IAudioSessionEvents
{
public:
    // Static method to create an instance of the object.
    static HRESULT CreateInstance(
        UINT uNotificationMessage,
        HWND hwndNotification,
        CAudioSessionVolume **ppAudioSessionVolume
    );

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IAudioSessionEvents methods.

    STDMETHODIMP OnSimpleVolumeChanged(
        float NewVolume,
        BOOL NewMute,
        LPCGUID EventContext
        );

    // The remaining audio session events do not require any action.
    STDMETHODIMP OnDisplayNameChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnIconPathChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnChannelVolumeChanged(DWORD,float[],DWORD,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnGroupingParamChanged(LPCGUID,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnStateChanged(AudioSessionState)
    {
        return S_OK;
    }

    STDMETHODIMP OnSessionDisconnected(AudioSessionDisconnectReason)
    {
        return S_OK;
    }

    // Other methods
    HRESULT EnableNotifications(BOOL bEnable);
    HRESULT GetVolume(float *pflVolume);
    HRESULT SetVolume(float flVolume);
    HRESULT GetMute(BOOL *pbMute);
    HRESULT SetMute(BOOL bMute);
    HRESULT SetDisplayName(const WCHAR *wszName);

protected:
    CAudioSessionVolume(UINT uNotificationMessage, HWND hwndNotification);
    ~CAudioSessionVolume();

    HRESULT Initialize();

protected:
    LONG m_cRef;                        // Reference count.
    UINT m_uNotificationMessage;        // Window message to send when an audio event occurs.
    HWND m_hwndNotification;            // Window to receives messages.
    BOOL m_bNotificationsEnabled;       // Are audio notifications enabled?

    IAudioSessionControl    *m_pAudioSession;
    ISimpleAudioVolume      *m_pSimpleAudioVolume;
};
```



<span data-ttu-id="752ff-146">Quando l' `CAudioSessionVolume` oggetto riceve un evento di sessione audio, invia un messaggio di finestra privata all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="752ff-146">When the `CAudioSessionVolume` object receives an audio session event, it posts a private window message to the application.</span></span> <span data-ttu-id="752ff-147">L'handle della finestra e il messaggio della finestra vengono specificati come parametri per il `CAudioSessionVolume::CreateInstance` metodo statico.</span><span class="sxs-lookup"><span data-stu-id="752ff-147">The window handle and the window message are given as parameters to the static `CAudioSessionVolume::CreateInstance` method.</span></span>

### <a name="getting-the-wasapi-interface-pointers"></a><span data-ttu-id="752ff-148">Recupero dei puntatori dell'interfaccia WASAPI</span><span class="sxs-lookup"><span data-stu-id="752ff-148">Getting the WASAPI Interface Pointers</span></span>

<span data-ttu-id="752ff-149">`CAudioSessionVolume` USA due interfacce WASAPI principali:</span><span class="sxs-lookup"><span data-stu-id="752ff-149">`CAudioSessionVolume` uses two main WASAPI interfaces:</span></span>

-   <span data-ttu-id="752ff-150">[**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) gestisce la sessione audio.</span><span class="sxs-lookup"><span data-stu-id="752ff-150">[**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) manages the audio session.</span></span>
-   <span data-ttu-id="752ff-151">[**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) controlla il livello del volume e lo stato di silenziamento della sessione.</span><span class="sxs-lookup"><span data-stu-id="752ff-151">[**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) controls the volume level and mute state of the session.</span></span>

<span data-ttu-id="752ff-152">Per ottenere queste interfacce, è necessario enumerare l'endpoint audio utilizzato dal SAR.</span><span class="sxs-lookup"><span data-stu-id="752ff-152">To get these interfaces, you must enumerate the audio endpoint that is used by the SAR.</span></span> <span data-ttu-id="752ff-153">Un *endpoint audio* è un dispositivo hardware che acquisisce o utilizza dati audio.</span><span class="sxs-lookup"><span data-stu-id="752ff-153">An *audio endpoint* is a hardware device that captures or consumes audio data.</span></span> <span data-ttu-id="752ff-154">Per la riproduzione audio, un endpoint è semplicemente un altoparlante o un altro output audio.</span><span class="sxs-lookup"><span data-stu-id="752ff-154">For audio playback, an endpoint is simply a speaker or other audio output.</span></span> <span data-ttu-id="752ff-155">Per impostazione predefinita, il SAR usa l'endpoint predefinito per il ruolo del dispositivo **eConsole** .</span><span class="sxs-lookup"><span data-stu-id="752ff-155">By default, the SAR uses the default endpoint for the **eConsole** device role.</span></span> <span data-ttu-id="752ff-156">Un *ruolo del dispositivo* è un ruolo assegnato per un endpoint.</span><span class="sxs-lookup"><span data-stu-id="752ff-156">A *device role* is an assigned role for an endpoint.</span></span> <span data-ttu-id="752ff-157">I ruoli del dispositivo sono specificati dall'enumerazione [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) , che è documentata in [API audio di base](../coreaudio/core-audio-apis-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="752ff-157">Device roles are specified by the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration, which is documented in [Core Audio APIs](../coreaudio/core-audio-apis-in-windows-vista.md).</span></span>

<span data-ttu-id="752ff-158">Nel codice seguente viene illustrato come enumerare l'endpoint e ottenere le interfacce WASAPI.</span><span class="sxs-lookup"><span data-stu-id="752ff-158">The following code shows how to enumerate the endpoint and get the WASAPI interfaces.</span></span>


```C++
HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}
```



### <a name="controlling-the-volume"></a><span data-ttu-id="752ff-159">Controllo del volume</span><span class="sxs-lookup"><span data-stu-id="752ff-159">Controlling the Volume</span></span>

<span data-ttu-id="752ff-160">I `CAudioSessionVolume` metodi che controllano il volume audio chiamano i metodi [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) equivalenti.</span><span class="sxs-lookup"><span data-stu-id="752ff-160">The `CAudioSessionVolume` methods that control the audio volume call the equivalent [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) methods.</span></span> <span data-ttu-id="752ff-161">Ad esempio, `CAudioSessionVolume::SetVolume` chiama [**ISimpleAudioVolume:: SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="752ff-161">For example, `CAudioSessionVolume::SetVolume` calls [**ISimpleAudioVolume::SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), as shown in the following code.</span></span>


```C++
HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}
```



## <a name="complete-caudiosessionvolume-code"></a><span data-ttu-id="752ff-162">Completare il codice CAudioSessionVolume</span><span class="sxs-lookup"><span data-stu-id="752ff-162">Complete CAudioSessionVolume Code</span></span>

<span data-ttu-id="752ff-163">Di seguito è riportato l'elenco completo per i metodi della `CAudioSessionVolume` classe.</span><span class="sxs-lookup"><span data-stu-id="752ff-163">Here is the complete listing for the methods of the `CAudioSessionVolume` class.</span></span>


```C++
static const GUID AudioSessionVolumeCtx =
{ 0x2715279f, 0x4139, 0x4ba0, { 0x9c, 0xb1, 0xb3, 0x51, 0xf1, 0xb5, 0x8a, 0x4a } };


CAudioSessionVolume::CAudioSessionVolume(
    UINT uNotificationMessage,
    HWND hwndNotification
    )
    : m_cRef(1),
      m_uNotificationMessage(uNotificationMessage),
      m_hwndNotification(hwndNotification),
      m_bNotificationsEnabled(FALSE),
      m_pAudioSession(NULL),
      m_pSimpleAudioVolume(NULL)
{
}

CAudioSessionVolume::~CAudioSessionVolume()
{
    EnableNotifications(FALSE);

    SafeRelease(&m_pAudioSession);
    SafeRelease(&m_pSimpleAudioVolume);
};


//  Creates an instance of the CAudioSessionVolume object.

/* static */
HRESULT CAudioSessionVolume::CreateInstance(
    UINT uNotificationMessage,
    HWND hwndNotification,
    CAudioSessionVolume **ppAudioSessionVolume
    )
{

    CAudioSessionVolume *pAudioSessionVolume = new (std::nothrow)
        CAudioSessionVolume(uNotificationMessage, hwndNotification);

    if (pAudioSessionVolume == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pAudioSessionVolume->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppAudioSessionVolume = pAudioSessionVolume;
    }
    else
    {
        pAudioSessionVolume->Release();
    }

    return hr;
}


//  Initializes the CAudioSessionVolume object.

HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}

STDMETHODIMP CAudioSessionVolume::QueryInterface(REFIID riid, void **ppv)
{
    static const QITAB qit[] =
    {
        QITABENT(CAudioSessionVolume, IAudioSessionEvents),
        { 0 },
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::Release()
{
    LONG cRef = InterlockedDecrement( &m_cRef );
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}


// Enables or disables notifications from the audio session. For example, the
// application is notified if the user mutes the audio through the system
// volume-control program (Sndvol).

HRESULT CAudioSessionVolume::EnableNotifications(BOOL bEnable)
{
    HRESULT hr = S_OK;

    if (m_hwndNotification == NULL || m_pAudioSession == NULL)
    {
        return E_FAIL;
    }

    if (m_bNotificationsEnabled == bEnable)
    {
        // No change.
        return S_OK;
    }

    if (bEnable)
    {
        hr = m_pAudioSession->RegisterAudioSessionNotification(this);
    }
    else
    {
        hr = m_pAudioSession->UnregisterAudioSessionNotification(this);
    }

    if (SUCCEEDED(hr))
    {
        m_bNotificationsEnabled = bEnable;
    }

    return hr;
}


// Gets the session volume level.

HRESULT CAudioSessionVolume::GetVolume(float *pflVolume)
{
    if ( m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMasterVolume(pflVolume);
    }
}

//  Sets the session volume level.
//
//  flVolume: Ranges from 0 (silent) to 1 (full volume)

HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}


//  Gets the muting state of the session.

HRESULT CAudioSessionVolume::GetMute(BOOL *pbMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMute(pbMute);
    }
}

//  Mutes or unmutes the session audio.

HRESULT CAudioSessionVolume::SetMute(BOOL bMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMute(
            bMute,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}

//  Sets the display name for the session audio.

HRESULT CAudioSessionVolume::SetDisplayName(const WCHAR *wszName)
{
    if (m_pAudioSession == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pAudioSession->SetDisplayName(wszName, NULL);
    }
}


//  Called when the session volume level or muting state changes.
//  (Implements IAudioSessionEvents::OnSimpleVolumeChanged.)

HRESULT CAudioSessionVolume::OnSimpleVolumeChanged(
    float NewVolume,
    BOOL NewMute,
    LPCGUID EventContext
    )
{
    // Check if we should post a message to the application.

    if ( m_bNotificationsEnabled &&
        (*EventContext != AudioSessionVolumeCtx) &&
        (m_hwndNotification != NULL)
        )
    {
        // Notifications are enabled, AND
        // We did not trigger the event ourselves, AND
        // We have a valid window handle.

        // Post the message.
        ::PostMessage(
            m_hwndNotification,
            m_uNotificationMessage,
            *((WPARAM*)(&NewVolume)),  // Coerce the float.
            (LPARAM)NewMute
            );
    }
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="752ff-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="752ff-164">Requirements</span></span>

<span data-ttu-id="752ff-165">MFPlay richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="752ff-165">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="752ff-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="752ff-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="752ff-167">Uso di MFPlay per la riproduzione audio/video</span><span class="sxs-lookup"><span data-stu-id="752ff-167">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
