---
title: Attività iniziali con XInput
description: XInput è un'API che consente alle applicazioni di ricevere input dal controller Xbox per Windows. Sono supportati gli effetti di rombo del controller e l'input vocale e l'output.
ms.assetid: 7b5eec3e-b3da-de5c-c926-8258c1418ef0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a9ca17e3046db676887290b9b9dcbb7318f2dc89d4dd9543cbe790bf271b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962500"
---
# <a name="getting-started-with-xinput"></a>Attività iniziali con XInput

XInput è un'API che consente alle applicazioni di ricevere input dal controller Xbox per Windows. Sono supportati gli effetti di rombo del controller e l'input vocale e l'output.

Questo argomento offre una breve panoramica delle funzionalità di XInput e di come configurarlo in un'applicazione. Include quanto segue:

-   [Introduzione a XInput](#introduction-to-xinput)
    -   [The Xbox Controller](#the-xbox-controller)
-   [Uso di XInput](#using-xinput)
    -   [Più controller](#multiple-controllers)
    -   [Recupero dello stato del controller](#getting-controller-state)
    -   [Zona di insodd](#dead-zone)
    -   [Impostazione degli effetti di vibrazione](#setting-vibration-effects)
    -   [Recupero di identificatori di dispositivo audio](#getting-audio-device-identifiers)
    -   [Recupero di GUID DirectSound (solo DirectX SDK legacy)](#getting-directsound-guids-legacy-directx-sdk-only)
-   [Argomenti correlati](#related-topics)

## <a name="introduction-to-xinput"></a>Introduzione a XInput

La console Xbox usa un controller di gioco compatibile con Windows. Le applicazioni possono usare l'API XInput per comunicare con questi controller quando sono collegati a un PC Windows (è possibile collegare fino a quattro controller univoci alla volta).

Usando questa API, qualsiasi controller Xbox connesso può essere sottoposto a query per il relativo stato ed è possibile impostare gli effetti di vibrazione. È anche possibile eseguire query sui controller con il visore collegato per i dispositivi di input audio e di output che possono essere usati con il visore per l'elaborazione vocale.

### <a name="the-xbox-controller"></a>The Xbox Controller

Il controller Xbox ha due bastoni direzionali analogici, ognuno con un pulsante digitale, due trigger analogici, un pad direzionale digitale con quattro direzioni e otto pulsanti digitali. Gli stati di ognuno di questi input vengono restituiti nella struttura [**XINPUT \_ GAMEPAD**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) quando viene chiamata la [**funzione XInputGetState.**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate)

Il controller ha anche due motori a vibrazione per fornire effetti di feedback della forza all'utente. Le velocità di questi motori vengono specificate nella struttura [**XINPUT \_ VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) passata alla funzione [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) per impostare gli effetti di vibrazione.

Facoltativamente, è possibile collegare un visore al controller. Il visore ha un microfono per l'input vocale e una cuffia per l'output audio. È possibile chiamare la [**funzione XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) o [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) legacy per ottenere gli identificatori di dispositivo che corrispondono ai dispositivi per il microfono e le cuffia. È quindi possibile usare le [API Core Audio per](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) ricevere l'input vocale e inviare l'output audio.

## <a name="using-xinput"></a>Uso di XInput

L'uso di XInput è semplice come chiamare le funzioni XInput in base alle esigenze. Usando le funzioni XInput, è possibile recuperare lo stato del controller, ottenere gli ID audio del visore e impostare gli effetti di rombo del controller.

### <a name="multiple-controllers"></a>Più controller

L'API XInput supporta fino a quattro controller connessi in qualsiasi momento. Tutte le funzioni XInput richiedono un *parametro dwUserIndex* passato per identificare il controller impostato o sottoposto a query. Questo ID sarà compreso tra 0 e 3 e verrà impostato automaticamente da XInput. Il numero corrisponde alla porta a cui è collegato il controller e non è modificabile.

Ogni controller visualizza l'ID che usa accendendo un quadrante sull'anello di luce al centro del controller. Un *valore dwUserIndex* pari a 0 corrisponde al quadrante superiore sinistro. la numerazione procede intorno all'anello in senso orario.

Le applicazioni devono supportare più controller.

### <a name="getting-controller-state"></a>Recupero dello stato del controller

Per tutta la durata di un'applicazione, il recupero dello stato da un controller verrà probabilmente eseguito più spesso. Da fotogramma a frame in un'applicazione di gioco, è necessario recuperare lo stato e aggiornare le informazioni sul gioco in modo da riflettere le modifiche del controller.

Per recuperare lo stato, usare la [**funzione XInputGetState:**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate)

```cpp
DWORD dwResult;    
for (DWORD i=0; i< XUSER_MAX_COUNT; i++ )
{
    XINPUT_STATE state;
    ZeroMemory( &state, sizeof(XINPUT_STATE) );

    // Simply get the state of the controller from XInput.
    dwResult = XInputGetState( i, &state );

    if( dwResult == ERROR_SUCCESS )
    {
        // Controller is connected
    }
    else
    {
        // Controller is not connected
    }
}
```

Si noti che il valore restituito [**di XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) può essere usato per determinare se il controller è connesso. Le applicazioni devono definire una struttura per contenere le informazioni sul controller interno. Queste informazioni devono essere confrontate con i risultati di **XInputGetState** per determinare quali modifiche, ad esempio la pressione di pulsanti o i delta del controller analogico, sono state apportate a tale frame. Nell'esempio precedente g *\_ Controllers rappresenta* una struttura di questo tipo.

Dopo aver recuperato lo stato in una [**struttura XINPUT \_ STATE,**](/windows/desktop/api/XInput/ns-xinput-xinput_state) è possibile verificarlo per verificare la presenza di modifiche e ottenere informazioni specifiche sullo stato del controller.

Il *membro dwPacketNumber* della struttura [**XINPUT \_ STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) può essere usato per verificare se lo stato del controller è stato modificato dopo l'ultima chiamata a [**XInputGetState.**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) Se *dwPacketNumber* non cambia tra due chiamate sequenziali a **XInputGetState,** lo stato non è stato modificato. Se è diverso, l'applicazione deve controllare il membro *Gamepad* della struttura **XINPUT \_ STATE** per ottenere informazioni più dettagliate sullo stato.

Per motivi di prestazioni, non chiamare [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) per uno slot utente "vuoto" per ogni frame. È consigliabile invece eseguire uno spazio per i controlli per i nuovi controller ogni pochi secondi.

### <a name="dead-zone"></a>Zona di insodd

Per consentire agli utenti di avere un'esperienza di gioco coerente, il gioco deve implementare correttamente la zona non corretta. La zona non identificabile è il "movimento" segnalato dal controller anche quando le levette analogiche non vengono toccate e centrate. Esiste anche una zona non attiva per i 2 trigger analogici.

> [!Note]  
> I giochi che usano XInput che non filtrano affatto la zona non disponibile avranno un'esperienza di gioco scadente. Si noti che alcuni controller sono più sensibili di altri, quindi la zona non operativa può variare da unità a unità. È consigliabile testare i giochi con diversi controller Xbox in sistemi diversi.

Le applicazioni devono usare "zone non attive" su input analoghi (trigger, bastoni) per indicare quando un movimento è stato effettuato sufficientemente sulla levetta o sul trigger per essere considerato valido.

L'applicazione deve verificare la presenza di zone non attendibili e rispondere in modo appopriate, come in questo esempio:

```cpp
XINPUT_STATE state = g_Controllers[i].state;

float LX = state.Gamepad.sThumbLX;
float LY = state.Gamepad.sThumbLY;

//determine how far the controller is pushed
float magnitude = sqrt(LX*LX + LY*LY);

//determine the direction the controller is pushed
float normalizedLX = LX / magnitude;
float normalizedLY = LY / magnitude;

float normalizedMagnitude = 0;

//check if the controller is outside a circular dead zone
if (magnitude > INPUT_DEADZONE)
{
    //clip the magnitude at its expected maximum value
    if (magnitude > 32767) magnitude = 32767;

    //adjust magnitude relative to the end of the dead zone
    magnitude -= INPUT_DEADZONE;

    //optionally normalize the magnitude with respect to its expected range
    //giving a magnitude value of 0.0 to 1.0
    normalizedMagnitude = magnitude / (32767 - INPUT_DEADZONE);
}
else //if the controller is in the deadzone zero out the magnitude
{
    magnitude = 0.0;
    normalizedMagnitude = 0.0;
}

//repeat for right thumb stick
```

Questo esempio calcola il vettore di direzione del controller e la distanza lungo il vettore in cui è stato inserito il controller. In questo modo è possibile applicare un deadzone circolare semplicemente controllando se la grandezza del controller è maggiore del valore di deadzone. Inoltre, il codice normalizza la grandezza del controller, che può quindi essere moltiplicata per un fattore specifico del gioco per convertire la posizione del controller in unità rilevanti per il gioco.

Si noti che è possibile definire zone non attive per i bastoni e i trigger (da 0 a 65534) oppure usare i deadzone specificati definiti come DEADZONE XINPUT \_ GAMEPAD \_ LEFT \_ \_ THUMB, XINPUT \_ GAMEPAD RIGHT THUMB DEADZONE e \_ \_ \_ XINPUT \_ GAMEPAD \_ TRIGGER THRESHOLD in \_ XInput.h:

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

Dopo aver applicato il deadzone, può essere utile ridimensionare l'intervallo risultante a virgola mobile \[ 0.0..1.0 (come nell'esempio precedente) e, facoltativamente, applicare una trasformazione \] non lineare.

Ad esempio, con i giochi di guida, può essere utile cubire il risultato per offrire un'idea migliore per guidare le automobili usando un gamepad, poiché la riduzione del risultato offre una maggiore precisione negli intervalli inferiori, che è consigliabile, perché i giocatori in genere applicano forza debole per ottenere un movimento sottile o applicare la forza dura in un'unica direzione per ottenere risposta rd.

### <a name="setting-vibration-effects"></a>Impostazione degli effetti di vibrazione

Oltre a ottenere lo stato del controller, è anche possibile inviare dati di vibrazione al controller per modificare il feedback fornito all'utente del controller. Il controller contiene due motori rombo che possono essere controllati in modo indipendente passando valori alla [**funzione XInputSetState.**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate)

La velocità di ogni motore può essere specificata usando un valore WORD nella struttura [**XINPUT \_ VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) passata alla [**funzione XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) come indicato di seguito:

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

Si noti che il motore destro è il motore ad alta frequenza, il motore sinistro è il motore a bassa frequenza. Non sempre devono essere impostate sulla stessa quantità, perché forniscono effetti diversi.

### <a name="getting-audio-device-identifiers"></a>Recupero di identificatori di dispositivo audio

Il visore per un controller Xbox ha queste funzioni:

-   Registrare l'audio usando un microfono
-   Riprodurre un suono con una cuffia

Usare questo codice per ottenere gli identificatori di dispositivo per il visore:

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

Dopo aver ottenuto gli identificatori di dispositivo, è possibile creare le interfacce appropriate. Ad esempio, se si usa XAudio 2.8, usare questo codice per creare una voce master per questo dispositivo:

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

Per informazioni su come usare l'identificatore di dispositivo captureId, vedere [Acquisizione di un flusso.](/windows/desktop/CoreAudio/capturing-a-stream)

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a>Recupero di GUID DirectSound (solo DirectX SDK legacy)

Il visore che può essere connesso a un controller Xbox ha due funzioni: è in grado di registrare l'audio usando un microfono e di riprodurre il suono usando una cuffia. Nell'API XInput queste funzioni vengono completate tramite [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85))usando le interfacce **IDirectSound8** e **IDirectSoundCapture8.**

Per associare il microfono e la cuffia visore alle interfacce [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) appropriate, è necessario ottenere DirectSoundGUIDs per i dispositivi di acquisizione ed esecuzione del rendering chiamando [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).

> [!Note]  
> L'uso di [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) legacy non è consigliato e non è disponibile nelle app Windows Store. Le informazioni in questa sezione si applicano solo alla versione DirectX SDK di XInput (XInput 1.3). La Windows 8 di XInput (XInput 1.4) usa esclusivamente gli identificatori di dispositivo WASAPI (Audio Session API) di Windows ottenuti tramite [**XInputGetAudioDeviceIds.**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids)

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

Dopo aver recuperato i GUID, è possibile creare le interfacce appropriate chiamando DirectSoundCreate8 e DirectSoundCaptureCreate8 nel modo seguente:

```cpp
// Create IDirectSound8 using the controller's render device
if( FAILED( hr = DirectSoundCreate8( &dsRenderGuid, &pDS, NULL ) ) )
   return hr;

// Set coop level to DSSCL_PRIORITY
if( FAILED( hr = pDS->SetCooperativeLevel( hWnd, DSSCL_NORMAL ) ) )
   return hr;

// Create IDirectSoundCapture using the controller's capture device
if( FAILED( hr = DirectSoundCaptureCreate8( &dsCaptureGuid, &pDSCapture, NULL ) ) )
   return hr;
```

## <a name="related-topics"></a>Argomenti correlati

[Guida di riferimento alla programmazione](programming-reference.md)