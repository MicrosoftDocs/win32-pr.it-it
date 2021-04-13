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
# <a name="managing-the-audio-session"></a>Gestione della sessione audio

\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. \]

In questo argomento viene descritto come controllare il volume audio quando si usa MFPlay per la riproduzione audio/video.

MFPlay fornisce i metodi seguenti per controllare il volume audio durante la riproduzione.



| Metodo                                                            | Descrizione                                           |
|-------------------------------------------------------------------|-------------------------------------------------------|
| [**IMFPMediaPlayer:: sebalance**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance) | Imposta il saldo tra i canali sinistro e destro. |
| [**IMFPMediaPlayer:: semute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute)       | Disattiva o disattiva l'audio.                           |
| [**IMFPMediaPlayer:: sevolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume)   | Imposta il livello del volume.                                |



 

Per comprendere il comportamento di questi metodi, è necessario conoscere alcuni termini dell'API di sessione audio (WASAPI) di Windows, che implementa la funzionalità audio di basso livello utilizzata da MFPlay.

In WASAPI ogni flusso audio appartiene esattamente a una *sessione audio*, che è un gruppo di flussi audio correlati. In genere, un'applicazione gestisce una singola sessione audio, sebbene le applicazioni possano creare più di una sessione. Il programma di controllo del volume di sistema (sndvol) Visualizza un controllo volume per ogni sessione audio. Tramite sndvol, un utente può modificare il volume di una sessione audio dall'esterno dell'applicazione. Questo processo è illustrato nella figura seguente.

![diagramma che mostra i flussi audio che passano attraverso il controllo del volume sulla strada agli altoparlanti; applicazione e punto di sndvol al controllo del volume](images/audio-session.gif)

In MFPlay un elemento multimediale può avere uno o più flussi audio attivi (in genere solo uno). Internamente, MFPlay usa il [renderer di streaming audio](streaming-audio-renderer.md) (SAR) per eseguire il rendering dei flussi audio. A meno che non venga configurato in caso contrario, il SAR viene aggiunto alla sessione audio predefinita dell'applicazione.

I metodi audio MFPlay controllano solo i flussi che appartengono all'elemento multimediale corrente. Non influiscono sul volume per tutti gli altri flussi che appartengono alla stessa sessione audio. In termini di WASAPI, i metodi MFPlay controllano i livelli del volume *per canale* , non il livello del volume master. Questo processo è illustrato nella figura seguente.

![diagramma simile a quello precedente, ma il secondo flusso inizia in corrispondenza dell'elemento multimediale e l'applicazione punta al secondo flusso e al controllo del volume](images/audio-session02.gif)

È importante comprendere alcune implicazioni di questa funzionalità di MFPlay. In primo luogo, un'applicazione può modificare il volume di riproduzione senza influire sugli altri flussi audio. È possibile usare questa funzionalità se MFPlay per implementare la dissolvenza incrociata audio, creando due istanze dell'oggetto MFPlay e modificando il volume separatamente.

Se si usano i metodi MFPlay per modificare lo stato del volume o del silenziamento, le modifiche non vengono visualizzate in sndvol. Ad esempio, è possibile chiamare il tasto di [**disattivazione**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) per disattivare l'audio, ma sndvol non visualizzerà la sessione come disabilitata. Viceversa, se per modificare il volume di sessione viene usato SndVol, le modifiche non vengono riflesse nei valori restituiti da [**IMFPMediaPlayer:: GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) o [**IMFPMediaPlayer:: getmute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).

Per ogni istanza dell'oggetto MFPlay Player, il livello di volume effettivo è uguale a *fPlayerVolume* × *FSessionVolume*, dove *fPlayerVolume* è il valore restituito da [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume)e *fSessionVolume* è il volume master per la sessione.

Per gli scenari di riproduzione semplici, potrebbe essere preferibile usare WASAPI per controllare il volume audio per l'intera sessione, anziché usare i metodi MFPlay.

## <a name="example-code"></a>Codice di esempio

Di seguito è riportata una classe C++ che gestisce le attività di base in WASAPI:

-   Controllo del volume e dello stato di silenziamento per la sessione.
-   Recupero di notifiche ogni volta che viene modificato lo stato del volume o del silenziamento.

### <a name="class-declaration"></a>Dichiarazione di classe

La `CAudioSessionVolume` dichiarazione di classe implementa l'interfaccia [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) , ovvero l'interfaccia di callback per gli eventi di sessione audio.


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



Quando l' `CAudioSessionVolume` oggetto riceve un evento di sessione audio, invia un messaggio di finestra privata all'applicazione. L'handle della finestra e il messaggio della finestra vengono specificati come parametri per il `CAudioSessionVolume::CreateInstance` metodo statico.

### <a name="getting-the-wasapi-interface-pointers"></a>Recupero dei puntatori dell'interfaccia WASAPI

`CAudioSessionVolume` USA due interfacce WASAPI principali:

-   [**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) gestisce la sessione audio.
-   [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) controlla il livello del volume e lo stato di silenziamento della sessione.

Per ottenere queste interfacce, è necessario enumerare l'endpoint audio utilizzato dal SAR. Un *endpoint audio* è un dispositivo hardware che acquisisce o utilizza dati audio. Per la riproduzione audio, un endpoint è semplicemente un altoparlante o un altro output audio. Per impostazione predefinita, il SAR usa l'endpoint predefinito per il ruolo del dispositivo **eConsole** . Un *ruolo del dispositivo* è un ruolo assegnato per un endpoint. I ruoli del dispositivo sono specificati dall'enumerazione [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) , che è documentata in [API audio di base](../coreaudio/core-audio-apis-in-windows-vista.md).

Nel codice seguente viene illustrato come enumerare l'endpoint e ottenere le interfacce WASAPI.


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



### <a name="controlling-the-volume"></a>Controllo del volume

I `CAudioSessionVolume` metodi che controllano il volume audio chiamano i metodi [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) equivalenti. Ad esempio, `CAudioSessionVolume::SetVolume` chiama [**ISimpleAudioVolume:: SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), come illustrato nel codice seguente.


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



## <a name="complete-caudiosessionvolume-code"></a>Completare il codice CAudioSessionVolume

Di seguito è riportato l'elenco completo per i metodi della `CAudioSessionVolume` classe.


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



## <a name="requirements"></a>Requisiti

MFPlay richiede Windows 7.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di MFPlay per la riproduzione audio/video](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
