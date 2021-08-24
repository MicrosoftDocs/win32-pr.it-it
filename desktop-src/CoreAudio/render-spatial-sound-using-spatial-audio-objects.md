---
description: Questo articolo presenta alcuni semplici esempi che illustrano come implementare l'audio spaziale usando oggetti audio spaziali statici, oggetti audio spaziali dinamici e oggetti audio spaziali che usano la funzione Head Relative Transfer Function (HRTF) di Microsoft.
ms.assetid: C99C342E-0BD9-486A-92AA-F8DCB72C1B00
title: Eseguire il rendering dell'audio spaziale usando oggetti audio spaziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9498b1792ed884624afef859f3f8c70d6001d91be5dff15211717651dc4767
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642501"
---
# <a name="render-spatial-sound-using-spatial-audio-objects"></a>Eseguire il rendering dell'audio spaziale usando oggetti audio spaziali

Questo articolo presenta alcuni semplici esempi che illustrano come implementare l'audio spaziale usando oggetti audio spaziali statici, oggetti audio spaziali dinamici e oggetti audio spaziali che usano la funzione Head Relative Transfer Function (HRTF) di Microsoft. I passaggi di implementazione per tutte e tre queste tecniche sono molto simili e questo articolo fornisce un esempio di codice strutturato in modo analogo per ogni tecnica. Per esempi end-to-end completi di implementazioni audio spaziali reali, vedere il repository GitHub degli esempi di [audio spaziale Microsoft.](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio) Per una panoramica di Windows Sonic, la soluzione microsoft a livello di piattaforma per il supporto del suono spaziale in Xbox e Windows, vedere [Spatial Sound (Audio spaziale).](spatial-sound.md)

## <a name="render-audio-using-static-spatial-audio-objects"></a>Eseguire il rendering dell'audio usando oggetti audio spaziali statici

Un oggetto audio statico viene usato per eseguire il rendering dell'audio in uno dei 18 canali audio statici definiti [**nell'enumerazione AudioObjectType.**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) Ognuno di questi canali rappresenta un parlante reale o virtualizzato in un punto fisso nello spazio che non si sposta nel tempo. I canali statici disponibili in un determinato dispositivo dipendono dal formato audio spaziale in uso. Per un elenco dei formati supportati e dei relativi conteggi dei canali, vedere [Audio spaziale.](spatial-sound.md)

Quando si inizializza un flusso audio spaziale, è necessario specificare quali canali statici disponibili verranno utilizzati dal flusso. Le definizioni costanti di esempio seguenti possono essere usate per specificare configurazioni comuni della voce e ottenere il numero di canali disponibili per ognuna.


```C++
const AudioObjectType ChannelMask_Mono = AudioObjectType_FrontCenter;
const AudioObjectType ChannelMask_Stereo = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight);
const AudioObjectType ChannelMask_2_1 = (AudioObjectType)(ChannelMask_Stereo | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_Quad = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_BackLeft | AudioObjectType_BackRight);
const AudioObjectType ChannelMask_4_1 = (AudioObjectType)(ChannelMask_Quad | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_5_1 = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_FrontCenter | AudioObjectType_LowFrequency | AudioObjectType_SideLeft | AudioObjectType_SideRight);
const AudioObjectType ChannelMask_7_1 = (AudioObjectType)(ChannelMask_5_1 | AudioObjectType_BackLeft | AudioObjectType_BackRight);

const UINT32 MaxStaticObjectCount_7_1_4 = 12;
const AudioObjectType ChannelMask_7_1_4 = (AudioObjectType)(ChannelMask_7_1 | AudioObjectType_TopFrontLeft | AudioObjectType_TopFrontRight | AudioObjectType_TopBackLeft | AudioObjectType_TopBackRight);

const UINT32 MaxStaticObjectCount_7_1_4_4 = 16;
const AudioObjectType ChannelMask_7_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4 | AudioObjectType_BottomFrontLeft | AudioObjectType_BottomFrontRight |AudioObjectType_BottomBackLeft | AudioObjectType_BottomBackRight);

const UINT32 MaxStaticObjectCount_8_1_4_4 = 17;
const AudioObjectType ChannelMask_8_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4_4 | AudioObjectType_BackCenter);
```



Il primo passaggio per il rendering dell'audio spaziale consiste nell'ottenere l'endpoint audio a cui verranno inviati i dati audio. Creare un'istanza di [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) e [**chiamare GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per ottenere il dispositivo di rendering audio predefinito.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Quando si crea un flusso audio spaziale, è necessario specificare il formato audio che verrà utilizzato dal flusso fornendo una [struttura WAVEFORMATEX.](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) Se si riproduce l'audio da un file, il formato è in genere determinato dal formato del file audio. Questo esempio usa un formato mono a 32 bit a 48 Hz.


```C++
WAVEFORMATEX format;
format.wFormatTag = WAVE_FORMAT_IEEE_FLOAT;
format.wBitsPerSample = 32;
format.nChannels = 1;
format.nSamplesPerSec = 48000;
format.nBlockAlign = (format.wBitsPerSample >> 3) * format.nChannels;
format.nAvgBytesPerSec = format.nBlockAlign * format.nSamplesPerSec;
format.cbSize = 0;
```



Il passaggio successivo per il rendering dell'audio spaziale consiste nell'inizializzare un flusso audio spaziale. Per prima cosa, ottenere [**un'istanza di ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) chiamando [**IMMDevice::Activate.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) Chiamare [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) per assicurarsi che il formato audio in uso sia supportato. Creare un evento che verrà utilizzato dalla pipeline audio per notificare all'app che è pronta per altri dati audio.

Popolare una [**struttura SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) che verrà usata per inizializzare il flusso audio spaziale. In questo esempio il campo **StaticObjectTypeMask** è impostato sulla costante **Stereo ChannelMask \_** definita in precedenza in questo articolo, vale a dire che solo i canali a destra e a sinistra possono essere usati dal flusso audio. Poiché questo esempio usa solo oggetti audio statici e nessun oggetto dinamico, il **campo MaxDynamicObjectCount** è impostato su 0. Il **campo Category** è impostato su un membro dell'enumerazione AUDIO STREAM [**\_ \_ CATEGORY,**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) che definisce il modo in cui il sistema combina il suono di questo flusso con altre origini audio.

Chiamare [**ISpatialAudioClient::ActivateSpatialAudioStream per**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) attivare il flusso.


```C++
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;

// Activate ISpatialAudioClient on the desired audio-device 
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = ChannelMask_Stereo;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = 0;
streamParams.Category = AudioCategory_SoundEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT activationParams;
PropVariantInit(&activationParams);
activationParams.vt = VT_BLOB;
activationParams.blob.cbSize = sizeof(streamParams);
activationParams.blob.pBlobData = reinterpret_cast<BYTE *>(&streamParams);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;
hr = spatialAudioClient->ActivateSpatialAudioStream(&activationParams, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



> [!Note]  
> Quando si usano le interfacce [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) in un titolo di Xbox One Development Kit (XDK), è necessario chiamare **EnableSpatialAudio** prima di chiamare [**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) o [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). In caso negativo, verrà restituito un errore E \_ NOINTERFACE dalla chiamata ad Activate. **EnableSpatialAudio** è disponibile solo per i titoli XDK e non deve essere chiamato per le app della piattaforma Universal Windows in esecuzione in Xbox One, né per dispositivi non Xbox One.

 

Dichiarare un puntatore per [**un oggetto ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) che verrà usato per scrivere dati audio in un canale statico. Le app tipiche useranno un oggetto per ogni canale specificato nel **campo StaticObjectTypeMask.** Per semplicità, in questo esempio viene utilizzato solo un singolo oggetto audio statico.


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



Prima di entrare nel ciclo di rendering audio, chiamare [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) per indicare alla pipeline multimediale di iniziare a richiedere dati audio. Questo esempio usa un contatore per arrestare il rendering dell'audio dopo 5 secondi.

All'interno del ciclo di rendering attendere che l'evento di completamento del buffer, fornito quando è stato inizializzato il flusso audio spaziale, sia segnalato. È consigliabile impostare un limite di timeout ragionevole, ad esempio 100 ms, durante l'attesa dell'evento perché qualsiasi modifica al tipo di rendering o all'endpoint causerà che l'evento non verrà mai segnalato. In questo caso, è possibile chiamare [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) per tentare di reimpostare il flusso audio spaziale.

Chiamare quindi [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) per far sapere al sistema che si sta per riempire i buffer degli oggetti audio con dati. Questo metodo restituisce il numero di oggetti audio dinamici disponibili, non utilizzati in questo esempio, e il conteggio dei fotogrammi del buffer per gli oggetti audio di cui viene eseguito il rendering da questo flusso.

Se non è ancora stato creato un oggetto audio spaziale statico, crearne uno o più chiamando [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), passando un valore dell'enumerazione [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) che indica il canale statico a cui viene eseguito il rendering dell'audio dell'oggetto.

Chiamare quindi [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) per ottenere un puntatore al buffer audio dell'oggetto audio spaziale. Questo metodo restituisce anche le dimensioni del buffer, in byte. Questo esempio usa un metodo helper, **WriteToAudioObjectBuffer,** per riempire il buffer con dati audio. Questo metodo viene illustrato più avanti in questo articolo. Dopo la scrittura nel buffer, l'esempio verifica se è stata raggiunta la durata di 5 secondi dell'oggetto e, in tal caso, viene chiamato [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) per far sapere alla pipeline audio che non verrà scritto altro audio usando questo oggetto e che l'oggetto è impostato su **nullptr** per liberare le risorse.

Dopo aver scritto i dati in tutti gli oggetti audio, chiamare [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) per far sapere al sistema che i dati sono pronti per il rendering. È possibile chiamare **GetBuffer solo** tra una chiamata a **BeginUpdatingAudioObjects** ed **EndUpdatingAudioObjects.**


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

// This example will render 5 seconds of audio samples
UINT totalFrameCount = format.nSamplesPerSec * 5;

bool isRendering = true;
while (isRendering)
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        hr = spatialAudioStream->Reset();

        if (hr != S_OK)
        {
            // handle the error
            break;
        }
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of dynamic objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    if (audioObjectFrontLeft == nullptr)
    {
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_FrontLeft, &audioObjectFrontLeft);
        if (hr != S_OK) break;
    }

    // Get the buffer to write audio data
    hr = audioObjectFrontLeft->GetBuffer(&buffer, &bufferLength);

    if (totalFrameCount >= frameCount)
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, 200.0f, format.nSamplesPerSec);

        totalFrameCount -= frameCount;
    }
    else
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), totalFrameCount, 750.0f, format.nSamplesPerSec);

        // Set end of stream for the last buffer 
        hr = audioObjectFrontLeft->SetEndOfStream(totalFrameCount);

        audioObjectFrontLeft = nullptr; // Release the object

        isRendering = false;
    }

    // Let the audio engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
};
```



Al termine del rendering dell'audio spaziale, arrestare il flusso audio spaziale chiamando [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop). Se non si userà di nuovo il flusso, liberarne le risorse chiamando [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



Il metodo helper **WriteToAudioObjectBuffer** scrive un buffer completo di esempi o il numero di campioni rimanenti specificato dal limite di tempo definito dall'app. Questo può anche essere determinato, ad esempio, dal numero di campioni rimanenti in un file audio di origine. Una semplice ondata di sin, la cui frequenza viene ridimensionata dal parametro di input *frequency,* viene generata e scritta nel buffer.


```C++
void WriteToAudioObjectBuffer(FLOAT* buffer, UINT frameCount, FLOAT frequency, UINT samplingRate)
{
    const double PI = 4 * atan2(1.0, 1.0);
    static double _radPhase = 0.0;

    double step = 2 * PI * frequency / samplingRate;

    for (UINT i = 0; i < frameCount; i++)
    {
        double sample = sin(_radPhase);

        buffer[i] = FLOAT(sample);

        _radPhase += step; // next frame phase

        if (_radPhase >= 2 * PI)
        {
            _radPhase -= 2 * PI;
        }
    }
}
```



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a>Eseguire il rendering dell'audio usando oggetti audio spaziali dinamici

Gli oggetti dinamici consentono di eseguire il rendering dell'audio da una posizione arbitraria nello spazio rispetto all'utente. La posizione e il volume di un oggetto audio dinamico possono essere modificati nel tempo. I giochi usano in genere la posizione di un oggetto 3D nel mondo del gioco per specificare la posizione dell'oggetto audio dinamico associato. Nell'esempio seguente verrà utilizzata una struttura semplice, **My3dObject**, per archiviare il set minimo di dati necessario per rappresentare un oggetto. Questi dati includono un puntatore a [**un oggetto ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), la posizione, la velocità, il volume e la frequenza del tono per l'oggetto e un valore che archivia il numero totale di fotogrammi per cui l'oggetto deve eseguire il rendering dell'audio.


```C++
struct My3dObject
{
    Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float volume;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



I passaggi di implementazione per gli oggetti audio dinamici sono in gran parte uguali a quelli per gli oggetti audio statici descritti in precedenza. Ottenere prima di tutto un endpoint audio.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Inizializzare quindi il flusso audio spaziale. Ottenere un'istanza [**di ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) chiamando [**IMMDevice::Activate.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) Chiamare [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) per assicurarsi che il formato audio in uso sia supportato. Creare un evento che verrà utilizzato dalla pipeline audio per notificare all'app che è pronta per altri dati audio.

Chiamare [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) per recuperare il numero di oggetti dinamici supportati dal sistema. Se questa chiamata restituisce 0, gli oggetti audio spaziali dinamici non sono supportati o abilitati nel dispositivo corrente. Per informazioni sull'abilitazione dell'audio spaziale e per informazioni dettagliate sul numero di oggetti audio dinamici disponibili per diversi formati audio spaziali, vedere [Audio spaziale.](spatial-sound.md)

Quando si popola la [**struttura SpatialAudioObjectRenderStreamActivationParams,**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) impostare il campo **MaxDynamicObjectCount** sul numero massimo di oggetti dinamici che verranno utilizzati dall'app.

Chiamare [**ISpatialAudioClient::ActivateSpatialAudioStream per**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) attivare il flusso.


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

if (maxDynamicObjectCount == 0)
{
    // Dynamic objects are unsupported
    return;
}

// Set the maximum number of dynamic audio objects that will be used
SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;;
hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



Di seguito è riportato un codice specifico dell'app che deve supportare questo esempio, che genera dinamicamente oggetti audio posizionati in modo casuale e li archivia in un vettore.


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObject> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-25, 25); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-1, 1); // uniform distribution for random velocity
std::uniform_real_distribution<> vol_dist(0.5, 1.0); // uniform distribution for random volume
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch
int spawnCounter = 0;
```



Prima di entrare nel ciclo di rendering audio, chiamare [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) per indicare alla pipeline multimediale di iniziare a richiedere dati audio.

All'interno del ciclo di rendering, attendere l'evento di completamento del buffer fornito quando è stato inizializzato il flusso audio spaziale per la segnalazione. È consigliabile impostare un limite di timeout ragionevole, ad esempio 100 ms, durante l'attesa dell'evento perché qualsiasi modifica al tipo di rendering o all'endpoint causerà che l'evento non verrà mai segnalato. In questo caso, è possibile chiamare [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) per tentare di reimpostare il flusso audio spaziale.

Chiamare quindi [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) per far sapere al sistema che si sta per riempire i buffer degli oggetti audio con dati. Questo metodo restituisce il numero di oggetti audio dinamici disponibili e il numero di frame del buffer per gli oggetti audio di cui viene eseguito il rendering da questo flusso.

Ogni volta che il contatore di generazione raggiunge il valore specificato, attiveremo un nuovo oggetto audio dinamico chiamando [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) specificando [**AudioObjectType \_ Dynamic.**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) Se tutti gli oggetti audio dinamici disponibili sono già stati allocati, questo metodo restituirà **SPLAUDCLNT \_ E NO MORE \_ \_ \_ OBJECTS**. In questo caso, è possibile scegliere di rilasciare uno o più oggetti audio attivati in precedenza in base alla priorità specifica dell'app. Dopo la creazione, l'oggetto audio dinamico viene aggiunto a una nuova struttura **My3dObject,** con valori casuali di posizione, velocità, volume e frequenza, che vengono quindi aggiunti all'elenco di oggetti attivi.

Scorrere quindi tutti gli oggetti attivi, rappresentati in questo esempio con la struttura **My3dObject** definita dall'app. Per ogni oggetto audio, chiamare [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) per ottenere un puntatore al buffer audio dell'oggetto audio spaziale. Questo metodo restituisce anche le dimensioni del buffer, in byte. Il metodo helper **WriteToAudioObjectBuffer** per riempire il buffer con dati audio. Dopo la scrittura nel buffer, l'esempio aggiorna la posizione dell'oggetto audio dinamico chiamando [**ISpatialAudioObject::SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition). Il volume dell'oggetto audio può anche essere modificato chiamando [**SetVolume.**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume) Se non si aggiorna la posizione o il volume dell'oggetto, manterrà la posizione e il volume dall'ultima impostazione. Se è stata raggiunta la durata definita dall'app dell'oggetto, viene chiamato [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) per far sapere alla pipeline audio che non verrà scritto altro audio usando questo oggetto e che l'oggetto è impostato su **nullptr** per liberare le risorse.

Dopo aver scritto i dati in tutti gli oggetti audio, chiamare [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) per far sapere al sistema che i dati sono pronti per il rendering. È possibile chiamare **GetBuffer solo** tra una chiamata a **BeginUpdatingAudioObjects** ed **EndUpdatingAudioObjects.**


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObject obj = {
                audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(vol_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObject>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;
            it->audioObject->SetVolume(it->volume);

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
} while (objectVector.size() > 0);
```



Al termine del rendering dell'audio spaziale, arrestare il flusso audio spaziale chiamando [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop). Se non si userà di nuovo il flusso, liberarne le risorse chiamando [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a>Eseguire il rendering dell'audio usando oggetti audio spaziali dinamici per HRTF

Un altro set di API, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) e [**ISpatialAudioObjectForHrtf,**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf)consente l'audio spaziale che usa la funzione di trasferimento head-relativo (HRTF) di Microsoft per attenuare i suoni per simulare la posizione dell'emettitore nello spazio, rispetto all'utente, che può essere modificata nel tempo. Oltre alla posizione, gli oggetti audio HRTF consentono di specificare un orientamento nello spazio, una direttavità in cui viene emesso il suono, ad esempio una forma conica o conica e un modello di decadimento quando l'oggetto si avvicina e si allontana dal listener virtuale. Si noti che queste interfacce HRTF sono disponibili solo quando l'utente ha selezionato Windows Sonic per cuffie come motore audio spaziale per il dispositivo. Per informazioni sulla configurazione di un dispositivo per l'uso Windows Sonic per cuffie, vedere [Audio spaziale.](spatial-sound.md)

Le [**API ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) e [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) consentono a un'applicazione di usare in modo esplicito il Windows Sonic per cuffie di rendering direttamente. Queste API non supportano formati audio spaziali come Dolby Atmos for Home Theater o Dolby Atmos for Headphones, né il cambio di  formato di output controllato dal consumer tramite il pannello di controllo Audio, né la riproduzione su altoparlanti. Queste interfacce sono destinate all'uso in applicazioni Windows Mixed Reality che vogliono usare funzionalità specifiche di Windows Sonic per cuffie, ad esempio set di impostazioni ambientali e rolloff basato sulla distanza specificati a livello di codice, al di fuori delle pipeline di creazione di contenuto tipiche. La maggior parte dei giochi e degli scenari di realtà virtuale preferisce usare [**invece ISpatialAudioClient.**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) I passaggi di implementazione per entrambi i set di API sono quasi identici, quindi è possibile implementare entrambe le tecnologie e passare in fase di esecuzione a seconda della funzionalità disponibile nel dispositivo corrente.

Le app di realtà mista in genere usano la posizione di un oggetto 3D nel mondo virtuale per specificare la posizione dell'oggetto audio dinamico associato. Nell'esempio seguente verrà utilizzata una struttura semplice, **My3dObjectForHrtf,** per archiviare il set minimo di dati necessario per rappresentare un oggetto . Questi dati includono un puntatore a [**un oggetto ISpatialAudioObjectForHrtf,**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf)la posizione, l'orientamento, la velocità e la frequenza del tono per l'oggetto e un valore che archivia il numero totale di fotogrammi per cui l'oggetto deve eseguire il rendering del suono.


```C++
struct My3dObjectForHrtf
{
    Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float yRotationRads;
    float deltaYRotation;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



I passaggi di implementazione per gli oggetti audio HRTF dinamici sono in gran parte uguali a quelli per gli oggetti audio dinamici descritti nella sezione precedente. Per prima cosa, ottenere un endpoint audio.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Inizializzare quindi il flusso audio spaziale. Ottenere [**un'istanza di ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) chiamando [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Chiamare [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) per assicurarsi che il formato audio in uso sia supportato. Creare un evento che verrà utilizzato dalla pipeline audio per notificare all'app che è pronta per altri dati audio.

Chiamare [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) per recuperare il numero di oggetti dinamici supportati dal sistema. Se questa chiamata restituisce 0, gli oggetti audio spaziali dinamici non sono supportati o abilitati nel dispositivo corrente. Per informazioni sull'abilitazione dell'audio spaziale e per informazioni dettagliate sul numero di oggetti audio dinamici disponibili per diversi formati audio spaziali, vedere [Audio spaziale](spatial-sound.md).

Quando si popola la [**struttura SpatialAudioHrtfActivationParams,**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) impostare il campo **MaxDynamicObjectCount** sul numero massimo di oggetti dinamici che verranno utilizzati dall'app. I parametri di attivazione per HRTF supportano alcuni parametri aggiuntivi, ad esempio [**SpatialAudioHrtfDistanceDecay,**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay) [**SpatialAudioHrtfDirectivityUnion,**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion) [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)e [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), che specificano i valori predefiniti di queste impostazioni per i nuovi oggetti creati dal flusso. Questi parametri sono facoltativi. Impostare i campi su **nullptr per** non fornire valori predefiniti.

Chiamare [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) per attivare il flusso.


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStreamForHrtf>  spatialAudioStreamForHrtf;
hr = spatialAudioClient->IsSpatialAudioStreamAvailable(__uuidof(spatialAudioStreamForHrtf), NULL);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

SpatialAudioHrtfActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = NULL;

SpatialAudioHrtfDistanceDecay decayModel;
decayModel.CutoffDistance = 100;
decayModel.MaxGain = 3.98f;
decayModel.MinGain = float(1.58439 * pow(10, -5));
decayModel.Type = SpatialAudioHrtfDistanceDecayType::SpatialAudioHrtfDistanceDecay_NaturalDecay;
decayModel.UnityGainDistance = 1;

streamParams.DistanceDecay = &decayModel;

SpatialAudioHrtfDirectivity directivity;
directivity.Type = SpatialAudioHrtfDirectivityType::SpatialAudioHrtfDirectivity_Cone;
directivity.Scaling = 1.0f;

SpatialAudioHrtfDirectivityCone cone;
cone.directivity = directivity;
cone.InnerAngle = 0.1f;
cone.OuterAngle = 0.2f;

SpatialAudioHrtfDirectivityUnion directivityUnion;
directivityUnion.Cone = cone;
streamParams.Directivity = &directivityUnion;

SpatialAudioHrtfEnvironmentType environment = SpatialAudioHrtfEnvironmentType::SpatialAudioHrtfEnvironment_Large;
streamParams.Environment = &environment;

SpatialAudioHrtfOrientation orientation = { 1,0,0,0,1,0,0,0,1 }; // identity matrix
streamParams.Orientation = &orientation;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStreamForHrtf), (void**)&spatialAudioStreamForHrtf);
```



Di seguito è riportato un codice specifico dell'app per supportare questo esempio, che genera dinamicamente oggetti audio posizionati in modo casuale e li archivia in un vettore.


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObjectForHrtf> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-10, 10); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-.02, .02); // uniform distribution for random velocity
std::uniform_real_distribution<> yRotation_dist(-3.14, 3.14); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> deltaYRotation_dist(.01, .02); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch

int spawnCounter = 0;
```



Prima di immettere il ciclo di rendering audio, chiamare [**ISpatialAudioObjectRenderStreamForHrtf::Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) per indicare alla pipeline multimediale di iniziare a richiedere i dati audio.

All'interno del ciclo di rendering attendere l'evento di completamento del buffer fornito quando è stato inizializzato il flusso audio spaziale per la segnalazione. È necessario impostare un limite di timeout ragionevole, ad esempio 100 ms, durante l'attesa dell'evento perché qualsiasi modifica al tipo di rendering o all'endpoint causerà che l'evento non verrà mai segnalato. In questo caso, è possibile chiamare [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) per tentare di reimpostare il flusso audio spaziale.

Chiamare quindi [**ISpatialAudioRenderStreamForHrtf::BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) per far sapere al sistema che si sta per riempire i buffer degli oggetti audio con dati. Questo metodo restituisce il numero di oggetti audio dinamici disponibili, non usati in questo esempio, e il numero di fotogrammi del buffer per gli oggetti audio sottoposti a rendering da questo flusso.

Ogni volta che il contatore di generazione raggiunge il valore specificato, si attiverà un nuovo oggetto audio dinamico chiamando [**ISpatialAudioRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) specificando [**AudioObjectType \_ Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype). Se tutti gli oggetti audio dinamici disponibili sono già stati allocati, questo metodo restituirà **SPLAUDCLNT \_ E NO MORE \_ \_ \_ OBJECTS**. In questo caso, è possibile scegliere di rilasciare uno o più oggetti audio attivati in precedenza in base alla priorità specifica dell'app. Dopo la creazione, l'oggetto audio dinamico viene aggiunto a una nuova struttura **My3dObjectForHrtf,** con valori casuali di posizione, rotazione, velocità, volume e frequenza, che viene quindi aggiunto all'elenco di oggetti attivi.

Scorrere quindi tutti gli oggetti attivi, rappresentati in questo esempio con la struttura **My3dObjectForHrtf** definita dall'app. Per ogni oggetto audio, chiamare [**ISpatialAudioObjectForHrtf::GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) per ottenere un puntatore al buffer audio dell'oggetto audio spaziale. Questo metodo restituisce anche le dimensioni del buffer, in byte. Il metodo helper **WriteToAudioObjectBuffer,** elencato in precedenza in questo articolo, per riempire il buffer con dati audio. Dopo la scrittura nel buffer, l'esempio aggiorna la posizione e l'orientamento dell'oggetto audio HRTF chiamando [**ISpatialAudioObjectForHrtf::SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) e [**ISpatialAudioObjectForHrtf::SetOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation). In questo esempio viene usato un metodo helper, **CalculateEmitterConeOrientationMatrix,** per calcolare la matrice di orientamento in base alla direzione di puntamento dell'oggetto 3D. L'implementazione di questo metodo è illustrata di seguito. Il volume dell'oggetto audio può essere modificato anche chiamando [**ISpatialAudioObjectForHrtf::SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain). Se non si aggiorna la posizione, l'orientamento o il volume dell'oggetto, l'oggetto manterrà la posizione, l'orientamento e il volume dall'ultima volta che è stato impostato. Se è stata raggiunta la durata definita dall'app dell'oggetto, viene chiamato [**ISpatialAudioObjectForHrtf::SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) per far sapere alla pipeline audio che non verrà scritto altro audio usando questo oggetto e che l'oggetto è impostato su **nullptr** per liberare le risorse.

Dopo aver scritto dati in tutti gli oggetti audio, chiamare [**ISpatialAudioRenderStreamForHrtf::EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) per far sapere al sistema che i dati sono pronti per il rendering. È possibile chiamare **GetBuffer solo** tra una chiamata a **BeginUpdatingAudioObjects** e **EndUpdatingAudioObjects**.


```C++
// Start streaming / rendering 
hr = spatialAudioStreamForHrtf->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStreamForHrtf->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
        hr = spatialAudioStreamForHrtf->ActivateSpatialAudioObjectForHrtf(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObjectForHrtf obj = { audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(yRotation_dist(gen))),
                static_cast<float>(static_cast<float>(deltaYRotation_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObjectForHrtf>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;


            Windows::Foundation::Numerics::float3 emitterDirection = Windows::Foundation::Numerics::float3(cos(it->yRotationRads), 0, sin(it->yRotationRads));
            Windows::Foundation::Numerics::float3 listenerDirection = Windows::Foundation::Numerics::float3(0, 0, 1);
            DirectX::XMFLOAT4X4 rotationMatrix;

            DirectX::XMMATRIX rotation = CalculateEmitterConeOrientationMatrix(emitterDirection, listenerDirection);
            XMStoreFloat4x4(&rotationMatrix, rotation);

            SpatialAudioHrtfOrientation orientation = {
                rotationMatrix._11, rotationMatrix._12, rotationMatrix._13,
                rotationMatrix._21, rotationMatrix._22, rotationMatrix._23,
                rotationMatrix._31, rotationMatrix._32, rotationMatrix._33
            };

            it->audioObject->SetOrientation(&orientation);
            it->yRotationRads += it->deltaYRotation;

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStreamForHrtf->EndUpdatingAudioObjects();

} while (objectVector.size() > 0);
```



Al termine del rendering dell'audio spaziale, arrestare il flusso audio spaziale chiamando [**ISpatialAudioRenderStreamForHrtf::Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)). Se non si sta per usare di nuovo il flusso, liberare le relative risorse chiamando [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



L'esempio di codice seguente illustra l'implementazione del metodo helper **CalculateEmitterConeOrientationMatrix** usato nell'esempio precedente per calcolare la matrice di orientamento in base alla direzione di puntamento dell'oggetto 3D.


```C++
DirectX::XMMATRIX CalculateEmitterConeOrientationMatrix(Windows::Foundation::Numerics::float3 listenerOrientationFront, Windows::Foundation::Numerics::float3 emitterDirection)
{
    DirectX::XMVECTOR vListenerDirection = DirectX::XMLoadFloat3(&listenerOrientationFront);
    DirectX::XMVECTOR vEmitterDirection = DirectX::XMLoadFloat3(&emitterDirection);
    DirectX::XMVECTOR vCross = DirectX::XMVector3Cross(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vDot = DirectX::XMVector3Dot(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vAngle = DirectX::XMVectorACos(vDot);
    float angle = DirectX::XMVectorGetX(vAngle);

    // The angle must be non-zero
    if (fabsf(angle) > FLT_EPSILON)
    {
        // And less than PI
        if (fabsf(angle) < DirectX::XM_PI)
        {
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }

        // If equal to PI, find any other non-collinear vector to generate the perpendicular vector to rotate about
        else
        {
            DirectX::XMFLOAT3 vector = { 1.0f, 1.0f, 1.0f };
            if (listenerOrientationFront.x != 0.0f)
            {
                vector.x = -listenerOrientationFront.x;
            }
            else if (listenerOrientationFront.y != 0.0f)
            {
                vector.y = -listenerOrientationFront.y;
            }
            else // if (_listenerOrientationFront.z != 0.0f)
            {
                vector.z = -listenerOrientationFront.z;
            }
            DirectX::XMVECTOR vVector = DirectX::XMLoadFloat3(&vector);
            vVector = DirectX::XMVector3Normalize(vVector);
            vCross = DirectX::XMVector3Cross(vVector, vEmitterDirection);
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }
    }

    // If the angle is zero, use an identity matrix
    return DirectX::XMMatrixIdentity();
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Audio spaziale](spatial-sound.md)
</dt> <dt>

[**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 
