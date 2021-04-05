---
title: Introduzione con XInput
description: XInput è un'API che consente alle applicazioni di ricevere input dal controller Xbox per Windows. Sono supportati gli effetti Rumble del controller e l'input vocale e l'output.
ms.assetid: 7b5eec3e-b3da-de5c-c926-8258c1418ef0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f590f54bbb2641881cf89cd6d31539d75665c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727658"
---
# <a name="getting-started-with-xinput"></a>Introduzione con XInput

XInput è un'API che consente alle applicazioni di ricevere input dal controller Xbox per Windows. Sono supportati gli effetti Rumble del controller e l'input vocale e l'output.

Questo argomento fornisce una breve panoramica delle funzionalità di XInput e di come configurarlo in un'applicazione. Include quanto segue:

-   [Introduzione a XInput](#introduction-to-xinput)
    -   [Controller Xbox](#the-xbox-controller)
-   [Uso di XInput](#using-xinput)
    -   [Più controller](#multiple-controllers)
    -   [Recupero dello stato del controller](#getting-controller-state)
    -   [Zona non recapitata](#dead-zone)
    -   [Impostazione degli effetti di vibrazione](#setting-vibration-effects)
    -   [Recupero degli identificatori di dispositivo audio](#getting-audio-device-identifiers)
    -   [Recupero di GUID DirectSound (solo legacy DirectX SDK)](#getting-directsound-guids-legacy-directx-sdk-only)
-   [Argomenti correlati](#related-topics)

## <a name="introduction-to-xinput"></a>Introduzione a XInput

La console Xbox usa un controller di gioco compatibile con Windows. Le applicazioni possono usare l'API XInput per comunicare con questi controller quando sono collegati a un PC Windows (fino a quattro controller univoci possono essere collegati alla volta).

Utilizzando questa API, è possibile eseguire query su qualsiasi controller Xbox connesso per lo stato e impostare gli effetti di vibrazione. È anche possibile eseguire query sui controller con l'auricolare collegato per i dispositivi di input e output audio che possono essere usati con la cuffia per l'elaborazione vocale.

### <a name="the-xbox-controller"></a>Controller Xbox

Il controller Xbox ha due stick direzionali analoghi, ognuno con un pulsante digitale, due trigger analoghi, un pad direzionale digitale con quattro direzioni e otto pulsanti digitali. Gli Stati di ognuno di questi input vengono restituiti nella struttura [**del \_ Gamepad XINPUT**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) quando viene chiamata la funzione [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) .

Il controller ha anche due motori di vibrazione per fornire agli utenti effetti sul feedback forzato. Le velocità di questi motori vengono specificate nella struttura [**di \_ vibrazione XINPUT**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) che viene passata alla funzione [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) per impostare gli effetti di vibrazione.

Facoltativamente, una cuffia può essere connessa al controller. La cuffia ha un microfono per l'input vocale e una cuffia per l'output audio. È possibile chiamare la funzione [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) o legacy [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) per ottenere gli identificatori del dispositivo che corrispondono ai dispositivi per il microfono e la cuffia. È quindi possibile usare le [API audio principali](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) per ricevere l'input vocale e inviare l'output audio.

## <a name="using-xinput"></a>Uso di XInput

L'uso di XInput è semplice come chiamare le funzioni XInput in base alle esigenze. Usando le funzioni XInput, è possibile recuperare lo stato del controller, ottenere gli ID audio della cuffia e impostare gli effetti Rumble del controller.

### <a name="multiple-controllers"></a>Più controller

L'API XInput supporta fino a quattro controller connessi in qualsiasi momento. Per tutte le funzioni XInput è necessario un parametro *dwUserIndex* passato per identificare il controller impostato o sottoposto a query. Questo ID sarà compreso nell'intervallo 0-3 e verrà impostato automaticamente da XInput. Il numero corrisponde alla porta a cui il controller è collegato e non è modificabile.

Ogni controller Visualizza l'ID che sta usando illuminando un quadrante sull'"anello di luce" al centro del controller. Un valore *dwUserIndex* pari a 0 corrisponde al quadrante superiore sinistro; la numerazione continua intorno all'anello in ordine orario.

Le applicazioni devono supportare più controller.

### <a name="getting-controller-state"></a>Recupero dello stato del controller

Per tutta la durata di un'applicazione, è probabile che il recupero dello stato da un controller venga eseguito più spesso. Dal frame al frame in un'applicazione di gioco, è necessario recuperare lo stato e aggiornare le informazioni sul gioco in modo da riflettere le modifiche del controller.

Per recuperare lo stato, usare la funzione [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) :

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

Si noti che il valore restituito di [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) può essere usato per determinare se il controller è connesso. Le applicazioni devono definire una struttura per conservare informazioni interne sul controller; Queste informazioni devono essere confrontate con i risultati di **XInputGetState** per determinare quali modifiche sono state apportate, ad esempio le pressioni dei pulsanti o i delta dei controller analoghi. Nell'esempio precedente, i *\_ controller g* rappresentano una struttura di questo tipo.

Una volta recuperato lo stato in una struttura [**di \_ stato XINPUT**](/windows/desktop/api/XInput/ns-xinput-xinput_state) , è possibile verificarne le modifiche e ottenere informazioni specifiche sullo stato del controller.

Il membro *dwPacketNumber* della struttura [**di \_ stato XINPUT**](/windows/desktop/api/XInput/ns-xinput-xinput_state) può essere usato per verificare se lo stato del controller è stato modificato dall'ultima chiamata a [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate). Se *dwPacketNumber* non viene modificato tra due chiamate sequenziali a **XInputGetState**, non sono state apportate modifiche allo stato. Se è diverso, l'applicazione deve controllare il membro del *Gamepad* della struttura di **\_ stato XINPUT** per ottenere informazioni più dettagliate sullo stato.

Per motivi di prestazioni, non chiamare [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) per uno slot utente ' Empty ' ogni frame. Si consiglia di verificare la presenza di nuovi controller a intervalli di pochi secondi.

### <a name="dead-zone"></a>Zona non recapitata

Per consentire agli utenti di avere un'esperienza di gioco coerente, il gioco deve implementare correttamente l'area di lavoro. L'area inattiva è rappresentata dai valori di "movimento" segnalati dal controller anche quando i ThumbSticks analoghi non vengono modificati e centrati. Esiste anche un'area inattiva per i 2 trigger analoghi.

> [!Note]  
> I giochi che usano XInput che non filtrano l'area insufficiente comportano una scarsa giocabilità. Si noti che alcuni controller sono più sensibili di altri, pertanto l'area inattiva può variare da unità a unità. Si consiglia di testare i giochi con diversi controller Xbox su sistemi diversi.

Le applicazioni devono usare "zone inattive" sugli input analoghi (trigger, stick) per indicare quando uno spostamento è stato sufficientemente appropriato per essere considerato valido.

L'applicazione deve controllare le zone non recapitabili e rispondere a appopriately, come nell'esempio seguente:

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

Questo esempio calcola il vettore di direzione del controller e la distanza del vettore con cui è stato effettuato il push del controller. In questo modo è possibile applicare un DeadZone circolare semplicemente controllando se la grandezza del controller è maggiore del valore di DeadZone. Inoltre, il codice normalizza la Magnitude del controller che può quindi essere moltiplicato per un fattore specifico del gioco per convertire la posizione del controller in unità rilevanti per il gioco.

Si noti che è possibile definire zone inattive per i bastoni e i trigger (ovunque si trovino da 0-65534) oppure usare il zone morte fornito definito come XINPUT \_ Gamepad \_ Left \_ Thumb \_ DEADZONE, XINPUT \_ Gamepad \_ right \_ Thumb \_ DEADZONE e XINPUT \_ Gamepad \_ trigger \_ Threshold in XINPUT. h:

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

Una volta applicato il DeadZone, può risultare utile ridimensionare l'intervallo risultante \[ 0.0.. 1.0 a \] virgola mobile (come nell'esempio precedente) e, facoltativamente, applicare una trasformazione non lineare.

Ad esempio, con la guida ai giochi, può essere utile creare un cubo per il risultato in modo da ottenere una migliore sensazione di guidare le auto usando un gamepad, in quanto cubi il risultato offre una maggiore precisione negli intervalli inferiori, che è auspicabile, perché i giocatori in genere applicano la forza morbida per ottenere un leggero movimento o applicare una forzatura totale in una direzione per ottenere la risposta Rd

### <a name="setting-vibration-effects"></a>Impostazione degli effetti di vibrazione

Oltre a ottenere lo stato del controller, è anche possibile inviare dati di vibrazione al controller per modificare il feedback fornito all'utente del controller. Il controller contiene due motori Rumble che possono essere controllati in modo indipendente passando i valori alla funzione [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) .

La velocità di ogni motore può essere specificata usando un valore di parola nella struttura di [**\_ vibrazione XINPUT**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) che viene passata alla funzione [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) nel modo seguente:

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

Si noti che il motore a destra è il motore ad alta frequenza, il motore di sinistra è il motore a bassa frequenza. Non è sempre necessario impostare la stessa quantità, perché forniscono effetti diversi.

### <a name="getting-audio-device-identifiers"></a>Recupero degli identificatori di dispositivo audio

La cuffia per un controller Xbox dispone di queste funzioni:

-   Registrare un suono usando un microfono
-   Riprodurre un suono con una cuffia

Usare questo codice per ottenere gli identificatori del dispositivo per la cuffia:

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

Una volta ottenuti gli identificatori del dispositivo, è possibile creare le interfacce appropriate. Se ad esempio si usa XAudio 2,8, usare questo codice per creare una voce di mastering per questo dispositivo:

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

Per informazioni su come usare l'identificatore del dispositivo captureId, vedere [acquisizione di un flusso](/windows/desktop/CoreAudio/capturing-a-stream).

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a>Recupero di GUID DirectSound (solo legacy DirectX SDK)

L'auricolare che può essere connesso a un controller Xbox ha due funzioni: può registrare un suono usando un microfono ed è in grado di riprodurre il suono con una cuffia. Nell'API XInput queste funzioni vengono eseguite tramite [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)), usando le interfacce **IDirectSound8** e **IDirectSoundCapture8** .

Per associare il microfono e la cuffia auricolare alle interfacce [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) appropriate, è necessario ottenere il DirectSoundGUIDs per i dispositivi di acquisizione e rendering chiamando [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).

> [!Note]  
> L'uso di [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) legacy non è consigliato e non è disponibile nelle app di Windows Store. Le informazioni in questa sezione si applicano solo alla versione di XInput di DirectX SDK (XInput 1,3). La versione di Windows 8 di XInput (XInput 1,4) usa esclusivamente identificatori di dispositivo WASAPI (Windows Audio Session API) ottenuti tramite [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

Una volta recuperati i GUID, è possibile creare le interfacce appropriate chiamando DirectSoundCreate8 e DirectSoundCaptureCreate8 come segue:

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