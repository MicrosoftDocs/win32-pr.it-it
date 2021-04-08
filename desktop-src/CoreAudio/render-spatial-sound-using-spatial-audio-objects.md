---
description: In questo articolo vengono presentati alcuni semplici esempi che illustrano come implementare il suono spaziale utilizzando gli oggetti audio spaziali statici, gli oggetti audio spaziali dinamici e gli oggetti audio spaziali che utilizzano la funzione di trasferimento relativa di Microsoft Head (HRTF).
ms.assetid: C99C342E-0BD9-486A-92AA-F8DCB72C1B00
title: Eseguire il rendering del suono spaziale usando oggetti audio spaziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd541026aa3e144ec8333c8ac045a17970735f17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748546"
---
# <a name="render-spatial-sound-using-spatial-audio-objects"></a><span data-ttu-id="76b73-103">Eseguire il rendering del suono spaziale usando oggetti audio spaziali</span><span class="sxs-lookup"><span data-stu-id="76b73-103">Render Spatial Sound Using Spatial Audio Objects</span></span>

<span data-ttu-id="76b73-104">In questo articolo vengono presentati alcuni semplici esempi che illustrano come implementare il suono spaziale utilizzando gli oggetti audio spaziali statici, gli oggetti audio spaziali dinamici e gli oggetti audio spaziali che utilizzano la funzione di trasferimento relativa di Microsoft Head (HRTF).</span><span class="sxs-lookup"><span data-stu-id="76b73-104">This article presents some simple examples that illustrate how to implement spatial sound using static spatial audio objects, dynamic spatial audio objects, and spatial audio objects that use Microsoft's Head Relative Transfer Function (HRTF).</span></span> <span data-ttu-id="76b73-105">I passaggi di implementazione per tutte e tre queste tecniche sono molto simili e in questo articolo viene fornito un esempio di codice strutturato in modo analogo per ciascuna tecnica.</span><span class="sxs-lookup"><span data-stu-id="76b73-105">The implementation steps for all three of these techniques are very similar and this article provides a similarly structured code example for each technique.</span></span> <span data-ttu-id="76b73-106">Per esempi end-to-end completi di implementazioni audio spaziali reali, vedere il [repository GitHub Microsoft Spatial Sample Samples](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio).</span><span class="sxs-lookup"><span data-stu-id="76b73-106">For complete end-to-end examples of real-world spatial audio implementations, see [Microsoft Spatial Sound samples github repository](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio).</span></span> <span data-ttu-id="76b73-107">Per una panoramica di Windows Sonic, la soluzione a livello di piattaforma Microsoft per il supporto di suoni spaziali in Xbox e Windows, vedere [audio spaziale](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="76b73-107">For an overview of Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, see [Spatial Sound](spatial-sound.md).</span></span>

## <a name="render-audio-using-static-spatial-audio-objects"></a><span data-ttu-id="76b73-108">Eseguire il rendering dell'audio usando oggetti audio spaziali statici</span><span class="sxs-lookup"><span data-stu-id="76b73-108">Render audio using static spatial audio objects</span></span>

<span data-ttu-id="76b73-109">Un oggetto audio statico viene usato per eseguire il rendering del suono in uno dei 18 canali audio statici definiti nell'enumerazione [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) .</span><span class="sxs-lookup"><span data-stu-id="76b73-109">A static audio object is used to render sound to one of 18 static audio channels defined in the [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) enumeration.</span></span> <span data-ttu-id="76b73-110">Ognuno di questi canali rappresenta un altoparlante reale o virtualizzato in un punto fisso nello spazio che non si sposta nel tempo.</span><span class="sxs-lookup"><span data-stu-id="76b73-110">Each of these channels represents a real or virtualized speaker at a fixed point in space that does not move over time.</span></span> <span data-ttu-id="76b73-111">I canali statici disponibili in un determinato dispositivo dipendono dal formato audio spaziale utilizzato.</span><span class="sxs-lookup"><span data-stu-id="76b73-111">The static channels that are available on a particular device depend on the spatial sound format being used.</span></span> <span data-ttu-id="76b73-112">Per un elenco dei formati supportati e dei relativi conteggi dei canali, vedere [audio spaziale](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="76b73-112">For a list of the supported formats and their channel counts, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="76b73-113">Quando si Inizializza un flusso audio spaziale, è necessario specificare quale dei canali statici disponibili utilizzerà il flusso.</span><span class="sxs-lookup"><span data-stu-id="76b73-113">When you initialize a spatial audio stream, you must specify which of the available static channels the stream will use.</span></span> <span data-ttu-id="76b73-114">Le definizioni di costanti di esempio seguenti possono essere utilizzate per specificare configurazioni comuni per i parlanti e ottenere il numero di canali disponibili per ciascuna di esse.</span><span class="sxs-lookup"><span data-stu-id="76b73-114">The following example constant definitions can be used to specify common speaker configurations and get the number of channels available for each one.</span></span>


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



<span data-ttu-id="76b73-115">Il primo passaggio per il rendering dell'audio spaziale consiste nell'ottenere l'endpoint audio a cui verranno inviati i dati audio.</span><span class="sxs-lookup"><span data-stu-id="76b73-115">The first step in rendering spatial audio is to get the audio endpoint to which audio data will be sent.</span></span> <span data-ttu-id="76b73-116">Creare un'istanza di [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) e chiamare [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per ottenere il dispositivo di rendering audio predefinito.</span><span class="sxs-lookup"><span data-stu-id="76b73-116">Create an instance of [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) and call [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) to get the default audio render device.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="76b73-117">Quando si crea un flusso audio spaziale, è necessario specificare il formato audio che il flusso userà fornendo una struttura [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="76b73-117">When you create a spatial audio stream, you must specify the audio format the stream will use by providing a [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) structure.</span></span> <span data-ttu-id="76b73-118">Se si sta riproducendo audio da un file, il formato è in genere determinato dal formato del file audio.</span><span class="sxs-lookup"><span data-stu-id="76b73-118">If you are playing back audio from a file, the format is typically determined by the audio file format.</span></span> <span data-ttu-id="76b73-119">Questo esempio usa un formato mono, 48Hz a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="76b73-119">This example uses a mono, 32-bit, 48Hz format.</span></span>


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



<span data-ttu-id="76b73-120">Il passaggio successivo per il rendering dell'audio spaziale consiste nell'inizializzare un flusso audio spaziale.</span><span class="sxs-lookup"><span data-stu-id="76b73-120">The next step in rendering spatial audio is to initialize a spatial audio stream.</span></span> <span data-ttu-id="76b73-121">Per prima cosa, ottenere un'istanza di [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) chiamando [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="76b73-121">First, get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="76b73-122">Chiamare [**ISpatialAudioClient:: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) per assicurarsi che il formato audio utilizzato sia supportato.</span><span class="sxs-lookup"><span data-stu-id="76b73-122">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="76b73-123">Creare un evento che verrà usato dalla pipeline audio per notificare all'app che è pronta per più dati audio.</span><span class="sxs-lookup"><span data-stu-id="76b73-123">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="76b73-124">Popola una struttura [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) che verrà usata per inizializzare il flusso audio spaziale.</span><span class="sxs-lookup"><span data-stu-id="76b73-124">Populate a [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) structure that will be used to initialize the spatial audio stream.</span></span> <span data-ttu-id="76b73-125">In questo esempio, il campo **StaticObjectTypeMask** è impostato sulla costante **\_ stereo ChannelMask** definita in precedenza in questo articolo, vale a dire che il flusso audio può usare solo i canali anteriore destro e sinistro.</span><span class="sxs-lookup"><span data-stu-id="76b73-125">In this example, the **StaticObjectTypeMask** field is set to the **ChannelMask\_Stereo** constant defined previously in this article, meaning that only the front right and left channels can be used by the audio stream.</span></span> <span data-ttu-id="76b73-126">Poiché in questo esempio vengono utilizzati solo oggetti audio statici e nessun oggetto dinamico, il campo **MaxDynamicObjectCount** viene impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="76b73-126">Because this example uses only static audio objects and no dynamic objects, the **MaxDynamicObjectCount** field is set to 0.</span></span> <span data-ttu-id="76b73-127">Il campo **categoria** è impostato su un membro dell'enumerazione [**di \_ \_ categoria del flusso audio**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) , che definisce il modo in cui il sistema mixa il suono da questo flusso con altre origini audio.</span><span class="sxs-lookup"><span data-stu-id="76b73-127">The **Category** field is set to a member of the [**AUDIO\_STREAM\_CATEGORY**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration, which defines how the system mixes the sound from this stream with other audio sources.</span></span>

<span data-ttu-id="76b73-128">Chiamare [**ISpatialAudioClient:: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) per attivare il flusso.</span><span class="sxs-lookup"><span data-stu-id="76b73-128">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


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
> <span data-ttu-id="76b73-129">Quando si usano le interfacce [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) in un titolo XDK (Xbox One Development Kit), è necessario chiamare prima **EnableSpatialAudio** prima di chiamare [**IMMDeviceEnumerator:: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) o [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="76b73-129">When using the [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) interfaces on an Xbox One Development Kit (XDK) title, you must first call **EnableSpatialAudio** before calling [**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) or [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="76b73-130">In caso contrario, verrà restituito un errore E \_ nointerface dalla chiamata a Activate.</span><span class="sxs-lookup"><span data-stu-id="76b73-130">Failure to do so will result in an E\_NOINTERFACE error being returned from the call to Activate.</span></span> <span data-ttu-id="76b73-131">**EnableSpatialAudio** è disponibile solo per i titoli XDK e non deve essere chiamato per piattaforma UWP (Universal Windows Platform) app eseguite su Xbox One, né per i dispositivi non Xbox One.</span><span class="sxs-lookup"><span data-stu-id="76b73-131">**EnableSpatialAudio** is only available for XDK titles, and does not need to be called for Universal Windows Platform apps running on Xbox One, nor for any non-Xbox One devices.</span></span>

 

<span data-ttu-id="76b73-132">Dichiarare un puntatore per un [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) che verrà usato per scrivere dati audio in un canale statico.</span><span class="sxs-lookup"><span data-stu-id="76b73-132">Declare a pointer for an [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) that will be used to write audio data to a static channel.</span></span> <span data-ttu-id="76b73-133">Le app tipiche utilizzeranno un oggetto per ogni canale specificato nel campo **StaticObjectTypeMask** .</span><span class="sxs-lookup"><span data-stu-id="76b73-133">Typical apps will use an object for each channel specified in the **StaticObjectTypeMask** field.</span></span> <span data-ttu-id="76b73-134">Per semplicità, in questo esempio viene utilizzato solo un singolo oggetto audio statico.</span><span class="sxs-lookup"><span data-stu-id="76b73-134">For simplicity, this example only uses a single static audio object.</span></span>


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



<span data-ttu-id="76b73-135">Prima di immettere il ciclo di rendering audio, chiamare [**ISpatialAudioObjectRenderStream:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) per indicare alla pipeline multimediale di iniziare a richiedere dati audio.</span><span class="sxs-lookup"><span data-stu-id="76b73-135">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) to instruct the media pipeline to begin requesting audio data.</span></span> <span data-ttu-id="76b73-136">Questo esempio usa un contatore per arrestare il rendering dell'audio dopo 5 secondi.</span><span class="sxs-lookup"><span data-stu-id="76b73-136">This example uses a counter to stop the rendering of audio after 5 seconds.</span></span>

<span data-ttu-id="76b73-137">All'interno del ciclo di rendering, attendere l'evento di completamento del buffer, fornito quando il flusso audio spaziale è stato inizializzato, per essere segnalato.</span><span class="sxs-lookup"><span data-stu-id="76b73-137">Inside the render loop, wait for the buffer completion event, provided when the spatial audio stream was initialized, to be signaled.</span></span> <span data-ttu-id="76b73-138">È necessario impostare un limite di timeout ragionevole, ad esempio 100 ms, durante l'attesa dell'evento perché qualsiasi modifica apportata al tipo di rendering o all'endpoint provocherà mai la segnalazione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="76b73-138">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="76b73-139">In questo caso, è possibile chiamare [**ISpatialAudioObjectRenderStream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) per tentare di reimpostare il flusso audio spaziale.</span><span class="sxs-lookup"><span data-stu-id="76b73-139">In this case, you can call [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="76b73-140">Successivamente, chiamare [**ISpatialAudioObjectRenderStream:: BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) per indicare al sistema che si sta per riempire i buffer degli oggetti audio con i dati.</span><span class="sxs-lookup"><span data-stu-id="76b73-140">Next, call [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="76b73-141">Questo metodo restituisce il numero di oggetti audio dinamici disponibili, non usato in questo esempio, e il conteggio dei frame del buffer per gli oggetti audio sottoposti a rendering da questo flusso.</span><span class="sxs-lookup"><span data-stu-id="76b73-141">This method returns the number of available dynamic audio objects, not used in this example, and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="76b73-142">Se non è stato ancora creato un oggetto audio spaziale statico, crearne uno o più chiamando [**ISpatialAudioObjectRenderStream:: ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), passando un valore dall'enumerazione [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) che indica il canale statico a cui viene eseguito il rendering dell'audio dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="76b73-142">If a static spatial audio object has not yet been created, create one or more by calling [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), passing in a value from the [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) enumeration indicating the static channel to which the object's audio is rendered.</span></span>

<span data-ttu-id="76b73-143">Successivamente, chiamare [**ISpatialAudioObject:: GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) per ottenere un puntatore al buffer audio dell'oggetto audio spaziale.</span><span class="sxs-lookup"><span data-stu-id="76b73-143">Next, call [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="76b73-144">Questo metodo restituisce anche le dimensioni, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="76b73-144">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="76b73-145">Questo esempio usa un metodo helper, **WriteToAudioObjectBuffer**, per riempire il buffer con dati audio.</span><span class="sxs-lookup"><span data-stu-id="76b73-145">This example uses a helper method, **WriteToAudioObjectBuffer**, to fill the buffer with audio data.</span></span> <span data-ttu-id="76b73-146">Questo metodo viene illustrato più avanti in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="76b73-146">This method is shown later in this article.</span></span> <span data-ttu-id="76b73-147">Dopo la scrittura nel buffer, nell'esempio viene verificato se è stata raggiunta la durata di 5 secondi dell'oggetto e, in tal caso, viene chiamato [**ISpatialAudioObject:: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) per consentire alla pipeline audio di sapere che non verrà scritto alcun altro audio utilizzando questo oggetto e che l'oggetto sia impostato su **nullptr** per liberare le risorse.</span><span class="sxs-lookup"><span data-stu-id="76b73-147">After writing to the buffer, the example checks to see if the 5 second lifetime of the object has been reached, and if so, [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="76b73-148">Dopo aver scritto i dati in tutti gli oggetti audio, chiamare [**ISpatialAudioObjectRenderStream:: EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) per informare il sistema che i dati sono pronti per il rendering.</span><span class="sxs-lookup"><span data-stu-id="76b73-148">After writing data to all of your audio objects, call [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="76b73-149">È possibile chiamare **GetBuffer** solo tra una chiamata a **BeginUpdatingAudioObjects** e **EndUpdatingAudioObjects**.</span><span class="sxs-lookup"><span data-stu-id="76b73-149">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


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



<span data-ttu-id="76b73-150">Al termine del rendering dell'audio spaziale, arrestare il flusso audio spaziale chiamando [**ISpatialAudioObjectRenderStream:: Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span><span class="sxs-lookup"><span data-stu-id="76b73-150">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span></span> <span data-ttu-id="76b73-151">Se non si intende usare nuovamente il flusso, liberare le risorse chiamando [**ISpatialAudioObjectRenderStream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span><span class="sxs-lookup"><span data-stu-id="76b73-151">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span></span>


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



<span data-ttu-id="76b73-152">Il metodo helper **WriteToAudioObjectBuffer** scrive un buffer completo di esempi o il numero di campioni rimanenti specificati dal limite di tempo definito dall'app.</span><span class="sxs-lookup"><span data-stu-id="76b73-152">The **WriteToAudioObjectBuffer** helper method writes either a full buffer of samples or the number of remaining samples specified by our app-defined time limit.</span></span> <span data-ttu-id="76b73-153">Questo può essere determinato, ad esempio, dal numero di campioni rimanenti in un file audio di origine.</span><span class="sxs-lookup"><span data-stu-id="76b73-153">This could also be determined, for example, by the number of samples remaining in a source audio file.</span></span> <span data-ttu-id="76b73-154">Una semplice Wave sin, la cui frequenza viene ridimensionata in base al parametro di input *Frequency* , viene generata e scritta nel buffer.</span><span class="sxs-lookup"><span data-stu-id="76b73-154">A simple sin wave, the frequency of which is scaled by the *frequency* input parameter, is generated and written to the buffer.</span></span>


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



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a><span data-ttu-id="76b73-155">Eseguire il rendering dell'audio usando oggetti audio spaziali dinamici</span><span class="sxs-lookup"><span data-stu-id="76b73-155">Render audio using dynamic spatial audio objects</span></span>

<span data-ttu-id="76b73-156">Gli oggetti dinamici consentono di eseguire il rendering dell'audio da una posizione arbitraria nello spazio rispetto all'utente.</span><span class="sxs-lookup"><span data-stu-id="76b73-156">Dynamic objects allow you to render audio from an arbitrary position in space, relative to the user.</span></span> <span data-ttu-id="76b73-157">La posizione e il volume di un oggetto audio dinamico possono essere modificati nel tempo.</span><span class="sxs-lookup"><span data-stu-id="76b73-157">The position and volume of a dynamic audio object can be changed over time.</span></span> <span data-ttu-id="76b73-158">I giochi utilizzeranno in genere la posizione di un oggetto 3D nel mondo del gioco per specificare la posizione dell'oggetto audio dinamico associato.</span><span class="sxs-lookup"><span data-stu-id="76b73-158">Games will typically use the position of a 3D object in the game world to specify the position of the dynamic audio object associated with it.</span></span> <span data-ttu-id="76b73-159">Nell'esempio seguente viene utilizzata una struttura semplice, **My3dObject**, per archiviare il set minimo di dati necessari per rappresentare un oggetto.</span><span class="sxs-lookup"><span data-stu-id="76b73-159">The following example will use a simple structure, **My3dObject**, to store the minimum set of data needed to represent an object.</span></span> <span data-ttu-id="76b73-160">Questi dati includono un puntatore a un [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), la posizione, la velocità, il volume e la frequenza del tono per l'oggetto e un valore che archivia il numero totale di frame per cui l'oggetto deve eseguire il rendering del suono.</span><span class="sxs-lookup"><span data-stu-id="76b73-160">This data includes a pointer to an [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), the position, velocity, volume, and tone frequency for the object, and a value that stores the total number of frames for which the object should render sound.</span></span>


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



<span data-ttu-id="76b73-161">I passaggi di implementazione per gli oggetti audio dinamici sono in gran parte identici ai passaggi per gli oggetti audio statici descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="76b73-161">The implementation steps for dynamic audio objects is largely the same as the steps for static audio objects described above.</span></span> <span data-ttu-id="76b73-162">Per prima cosa, ottenere un endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="76b73-162">First, get an audio endpoint.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="76b73-163">Successivamente, inizializzare il flusso audio spaziale.</span><span class="sxs-lookup"><span data-stu-id="76b73-163">Next, initialize the spatial audio stream.</span></span> <span data-ttu-id="76b73-164">Ottenere un'istanza di [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) chiamando [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="76b73-164">Get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="76b73-165">Chiamare [**ISpatialAudioClient:: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) per assicurarsi che il formato audio utilizzato sia supportato.</span><span class="sxs-lookup"><span data-stu-id="76b73-165">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="76b73-166">Creare un evento che verrà usato dalla pipeline audio per notificare all'app che è pronta per più dati audio.</span><span class="sxs-lookup"><span data-stu-id="76b73-166">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="76b73-167">Chiamare [**ISpatialAudioClient:: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) per recuperare il numero di oggetti dinamici supportati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="76b73-167">Call [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) to retrieve the number of dynamic objects supported by the system.</span></span> <span data-ttu-id="76b73-168">Se questa chiamata restituisce 0, gli oggetti audio spaziali dinamici non sono supportati o abilitati nel dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="76b73-168">If this call returns 0, then dynamic spatial audio objects are not supported or enabled on the current device.</span></span> <span data-ttu-id="76b73-169">Per informazioni sull'abilitazione dell'audio spaziale e per informazioni dettagliate sul numero di oggetti audio dinamici disponibili per formati audio spaziali diversi, vedere [audio spaziale](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="76b73-169">For information on enabling spatial audio and for details on the number of dynamic audio objects available for different spatial audio formats, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="76b73-170">Quando si popola la struttura [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) , impostare il campo **MaxDynamicObjectCount** sul numero massimo di oggetti dinamici che l'App utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="76b73-170">When populating the [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) structure, set the **MaxDynamicObjectCount** field to the maximum number of dynamic objects your app will use.</span></span>

<span data-ttu-id="76b73-171">Chiamare [**ISpatialAudioClient:: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) per attivare il flusso.</span><span class="sxs-lookup"><span data-stu-id="76b73-171">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


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



<span data-ttu-id="76b73-172">Di seguito è riportato un codice specifico dell'app per supportare questo esempio, che genera in modo dinamico gli oggetti audio posizionati in modo casuale e li archivia in un vettore.</span><span class="sxs-lookup"><span data-stu-id="76b73-172">The following is some app-specific code to needed support this example, which will dynamically spawn randomly positioned audio objects and store them in a vector.</span></span>


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



<span data-ttu-id="76b73-173">Prima di immettere il ciclo di rendering audio, chiamare [**ISpatialAudioObjectRenderStream:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) per indicare alla pipeline multimediale di iniziare a richiedere dati audio.</span><span class="sxs-lookup"><span data-stu-id="76b73-173">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) to instruct the media pipeline to begin requesting audio data.</span></span>

<span data-ttu-id="76b73-174">All'interno del ciclo di rendering, attendere l'evento di completamento del buffer fornito quando il flusso audio spaziale è stato inizializzato per essere segnalato.</span><span class="sxs-lookup"><span data-stu-id="76b73-174">Inside the render loop, wait for the buffer completion event we provided when the spatial audio stream was initialized to be signaled.</span></span> <span data-ttu-id="76b73-175">È necessario impostare un limite di timeout ragionevole, ad esempio 100 ms, durante l'attesa dell'evento perché qualsiasi modifica apportata al tipo di rendering o all'endpoint provocherà mai la segnalazione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="76b73-175">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="76b73-176">In questo caso, è possibile chiamare [**ISpatialAudioObjectRenderStream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) per tentare di reimpostare il flusso audio spaziale.</span><span class="sxs-lookup"><span data-stu-id="76b73-176">In this case, you can call [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="76b73-177">Successivamente, chiamare [**ISpatialAudioObjectRenderStream:: BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) per indicare al sistema che si sta per riempire i buffer degli oggetti audio con i dati.</span><span class="sxs-lookup"><span data-stu-id="76b73-177">Next, call [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="76b73-178">Questo metodo restituisce il numero di oggetti audio dinamici disponibili e il numero di frame del buffer per gli oggetti audio sottoposti a rendering da questo flusso.</span><span class="sxs-lookup"><span data-stu-id="76b73-178">This method returns the number of available dynamic audio objects and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="76b73-179">Ogni volta che il contatore delle uova raggiunge il valore specificato, si attiverà un nuovo oggetto audio dinamico chiamando [**ISpatialAudioObjectRenderStream:: ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) specificando [**AudioObjectType \_ Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span><span class="sxs-lookup"><span data-stu-id="76b73-179">Whenever the spawn counter reaches the specified value, we will activate a new dynamic audio object by calling [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) specifying [**AudioObjectType\_Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span></span> <span data-ttu-id="76b73-180">Se tutti gli oggetti audio dinamici disponibili sono già stati allocati, questo metodo restituirà **SPLAUDCLNT \_ E \_ nessun \_ altro \_ oggetto**.</span><span class="sxs-lookup"><span data-stu-id="76b73-180">If all available dynamic audio objects have already been allocated, this method will return **SPLAUDCLNT\_E\_NO\_MORE\_OBJECTS**.</span></span> <span data-ttu-id="76b73-181">In questo caso, è possibile scegliere di rilasciare uno o più oggetti audio precedentemente attivati in base alle priorità specifiche dell'app.</span><span class="sxs-lookup"><span data-stu-id="76b73-181">In this case, you can choose to release one or more previously activated audio objects based on your app-specific prioritization.</span></span> <span data-ttu-id="76b73-182">Dopo la creazione dell'oggetto audio dinamico, questo viene aggiunto a una nuova struttura **My3dObject** , con valori di posizione, velocità, volume e frequenza casuale, che vengono quindi aggiunti all'elenco di oggetti attivi.</span><span class="sxs-lookup"><span data-stu-id="76b73-182">After the dynamic audio object has been created, it is added to a new **My3dObject** structure, with randomized position, velocity, volume, and frequency values, which is then added to the list of active objects.</span></span>

<span data-ttu-id="76b73-183">Eseguire quindi l'iterazione di tutti gli oggetti attivi, rappresentati in questo esempio con la struttura **My3dObject** definita dall'app.</span><span class="sxs-lookup"><span data-stu-id="76b73-183">Next, iterate over all of the active objects, represented in this example with the app-defined **My3dObject** structure.</span></span> <span data-ttu-id="76b73-184">Per ogni oggetto audio, chiamare [**ISpatialAudioObject:: GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) per ottenere un puntatore al buffer audio dell'oggetto audio spaziale.</span><span class="sxs-lookup"><span data-stu-id="76b73-184">For each audio object, call [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="76b73-185">Questo metodo restituisce anche le dimensioni, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="76b73-185">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="76b73-186">Metodo di supporto, **WriteToAudioObjectBuffer**, per riempire il buffer con dati audio.</span><span class="sxs-lookup"><span data-stu-id="76b73-186">The helper method, **WriteToAudioObjectBuffer**, to fill the buffer with audio data.</span></span> <span data-ttu-id="76b73-187">Dopo la scrittura nel buffer, nell'esempio viene aggiornata la posizione dell'oggetto audio dinamico chiamando [**ISpatialAudioObject:: seposition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition).</span><span class="sxs-lookup"><span data-stu-id="76b73-187">After writing to the buffer, the example updates the position of the dynamic audio object by calling [**ISpatialAudioObject::SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition).</span></span> <span data-ttu-id="76b73-188">Il volume dell'oggetto audio può essere modificato anche chiamando il volume [**.**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume)</span><span class="sxs-lookup"><span data-stu-id="76b73-188">The volume of the audio object can also be modified by calling [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume).</span></span> <span data-ttu-id="76b73-189">Se non si aggiorna la posizione o il volume dell'oggetto, manterrà la posizione e il volume dell'ultima volta che è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="76b73-189">If you don't update the position or volume of the object, it will retain the position and volume from the last time it was set.</span></span> <span data-ttu-id="76b73-190">Se è stata raggiunta la durata definita dall'app dell'oggetto, viene chiamato [**ISpatialAudioObject:: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) per consentire alla pipeline audio di capire che non verrà scritto alcun altro audio usando questo oggetto e che l'oggetto sia impostato su **nullptr** per liberare le risorse.</span><span class="sxs-lookup"><span data-stu-id="76b73-190">If the object's app-defined lifetime has been reached, [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="76b73-191">Dopo aver scritto i dati in tutti gli oggetti audio, chiamare [**ISpatialAudioObjectRenderStream:: EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) per informare il sistema che i dati sono pronti per il rendering.</span><span class="sxs-lookup"><span data-stu-id="76b73-191">After writing data to all of your audio objects, call [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="76b73-192">È possibile chiamare **GetBuffer** solo tra una chiamata a **BeginUpdatingAudioObjects** e **EndUpdatingAudioObjects**.</span><span class="sxs-lookup"><span data-stu-id="76b73-192">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


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



<span data-ttu-id="76b73-193">Al termine del rendering dell'audio spaziale, arrestare il flusso audio spaziale chiamando [**ISpatialAudioObjectRenderStream:: Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span><span class="sxs-lookup"><span data-stu-id="76b73-193">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span></span> <span data-ttu-id="76b73-194">Se non si intende usare nuovamente il flusso, liberare le risorse chiamando [**ISpatialAudioObjectRenderStream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span><span class="sxs-lookup"><span data-stu-id="76b73-194">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span></span>


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a><span data-ttu-id="76b73-195">Eseguire il rendering dell'audio usando oggetti audio spaziali dinamici per HRTF</span><span class="sxs-lookup"><span data-stu-id="76b73-195">Render audio using dynamic spatial audio objects for HRTF</span></span>

<span data-ttu-id="76b73-196">Un altro set di API, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) e [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), Abilita l'audio spaziale che usa la funzione di trasferimento Head-relativa di Microsoft (HRTF) per attenuare i suoni per simulare la posizione del emettitore nello spazio, rispetto all'utente, che può essere modificato nel tempo.</span><span class="sxs-lookup"><span data-stu-id="76b73-196">Another set of APIs, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) and [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), enable spatial audio that uses Microsoft's Head-relative Transfer Function (HRTF) to attenuate sounds to simulate the emitter's position in space, relative to the user, which can be changed over time.</span></span> <span data-ttu-id="76b73-197">Oltre alla posizione, gli oggetti audio HRTF consentono di specificare un orientamento nello spazio, una direzione di emissione del suono, ad esempio una forma cono o cardioide, e un modello di decadimento quando l'oggetto viene spostato più vicino e ulteriormente dal listener virtuale.</span><span class="sxs-lookup"><span data-stu-id="76b73-197">In addition to position, HRTF audio objects allow you to specify an orientation in space, a directivity in which sound is emitted, such as a cone or cardioid shape, and a decay model as the object moves nearer and further from the virtual listener.</span></span> <span data-ttu-id="76b73-198">Si noti che queste interfacce HRTF sono disponibili solo quando l'utente ha selezionato Windows Sonic per le cuffie come motore audio spaziale per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76b73-198">Note that these HRTF interfaces are only available when the user has selected Windows Sonic for Headphones as the spatial audio engine for the device.</span></span> <span data-ttu-id="76b73-199">Per informazioni sulla configurazione di un dispositivo per l'utilizzo di Windows Sonic per le cuffie, vedere [audio spaziale](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="76b73-199">For information on configuring a device to use Windows Sonic for Headphones, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="76b73-200">Le API [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) e [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) consentono a un'applicazione di usare direttamente il percorso di rendering di Windows Sonic per le cuffie.</span><span class="sxs-lookup"><span data-stu-id="76b73-200">The [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) and [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) APIs allow an application to explicitly use the Windows Sonic for Headphones render path directly.</span></span> <span data-ttu-id="76b73-201">Queste API non supportano formati audio spaziali, ad esempio Dolby Atmos per Home Theater o Dolby Atmos per le cuffie, né lo spostamento del formato di output controllato dal cliente tramite il pannello di controllo **audio** , né la riproduzione su altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="76b73-201">These APIs do not support spatial sound formats such as Dolby Atmos for Home Theater or Dolby Atmos for Headphones, nor consumer-controlled output format switching via the **Sound** control panel, nor playback over speakers.</span></span> <span data-ttu-id="76b73-202">Queste interfacce sono destinate all'uso in applicazioni di realtà mista di Windows che vogliono usare Windows Sonic per le funzionalità specifiche delle cuffie, ad esempio i set di impostazioni ambientali e attenuazione basati sulla distanza specificati a livello di codice, all'esterno delle pipeline tipiche di creazione di contenuti.</span><span class="sxs-lookup"><span data-stu-id="76b73-202">These interfaces are intended for use in Windows Mixed Reality applications that want to use Windows Sonic for Headphones-specific capabilities (such as environmental presets and distance-based rolloff specified programmatically, outside of typical content authoring pipelines).</span></span> <span data-ttu-id="76b73-203">La maggior parte degli scenari di giochi e realtà virtuali preferisce invece usare [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) .</span><span class="sxs-lookup"><span data-stu-id="76b73-203">Most games and virtual reality scenarios will prefer to use [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) instead.</span></span> <span data-ttu-id="76b73-204">I passaggi di implementazione per entrambi i set di API sono quasi identici, quindi è possibile implementare entrambe le tecnologie e passare al runtime a seconda della funzionalità disponibile sul dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="76b73-204">The implementation steps for both API sets are almost identical, so it is possible to implement both technologies and switch at runtime depending on which feature is available on the current device.</span></span>

<span data-ttu-id="76b73-205">Le app in realtà mista usano in genere la posizione di un oggetto 3D nel mondo virtuale per specificare la posizione dell'oggetto audio dinamico associato.</span><span class="sxs-lookup"><span data-stu-id="76b73-205">Mixed-reality apps will typically use the position of a 3D object in the virtual world to specify the position of the dynamic audio object associated with it.</span></span> <span data-ttu-id="76b73-206">Nell'esempio seguente viene utilizzata una struttura semplice, **My3dObjectForHrtf**, per archiviare il set minimo di dati necessari per rappresentare un oggetto.</span><span class="sxs-lookup"><span data-stu-id="76b73-206">The following example will use a simple structure, **My3dObjectForHrtf**, to store the minimum set of data needed to represent an object.</span></span> <span data-ttu-id="76b73-207">Questi dati includono un puntatore a un [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), la posizione, l'orientamento, la velocità e la frequenza del tono per l'oggetto e un valore che archivia il numero totale di frame per cui l'oggetto deve eseguire il rendering del suono.</span><span class="sxs-lookup"><span data-stu-id="76b73-207">This data includes a pointer to an [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), the position, orientation, velocity, and tone frequency for the object, and a value that stores the total number of frames for which the object should render sound.</span></span>


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



<span data-ttu-id="76b73-208">I passaggi di implementazione per gli oggetti audio HRTF dinamici sono in gran parte identici ai passaggi per gli oggetti audio dinamici descritti nella sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="76b73-208">The implementation steps for dynamic HRTF audio objects is largely the same as the steps for dynamic audio objects described in the previous section.</span></span> <span data-ttu-id="76b73-209">Per prima cosa, ottenere un endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="76b73-209">First, get an audio endpoint.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="76b73-210">Successivamente, inizializzare il flusso audio spaziale.</span><span class="sxs-lookup"><span data-stu-id="76b73-210">Next, initialize the spatial audio stream.</span></span> <span data-ttu-id="76b73-211">Ottenere un'istanza di [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) chiamando [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="76b73-211">Get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="76b73-212">Chiamare [**ISpatialAudioClient:: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) per assicurarsi che il formato audio utilizzato sia supportato.</span><span class="sxs-lookup"><span data-stu-id="76b73-212">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="76b73-213">Creare un evento che verrà usato dalla pipeline audio per notificare all'app che è pronta per più dati audio.</span><span class="sxs-lookup"><span data-stu-id="76b73-213">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="76b73-214">Chiamare [**ISpatialAudioClient:: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) per recuperare il numero di oggetti dinamici supportati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="76b73-214">Call [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) to retrieve the number of dynamic objects supported by the system.</span></span> <span data-ttu-id="76b73-215">Se questa chiamata restituisce 0, gli oggetti audio spaziali dinamici non sono supportati o abilitati nel dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="76b73-215">If this call returns 0, then dynamic spatial audio objects are not supported or enabled on the current device.</span></span> <span data-ttu-id="76b73-216">Per informazioni sull'abilitazione dell'audio spaziale e per informazioni dettagliate sul numero di oggetti audio dinamici disponibili per formati audio spaziali diversi, vedere [audio spaziale](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="76b73-216">For information on enabling spatial audio and for details on the number of dynamic audio objects available for different spatial audio formats, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="76b73-217">Quando si popola la struttura [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) , impostare il campo **MaxDynamicObjectCount** sul numero massimo di oggetti dinamici che l'App utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="76b73-217">When populating the [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) structure, set the **MaxDynamicObjectCount** field to the maximum number of dynamic objects your app will use.</span></span> <span data-ttu-id="76b73-218">I param di attivazione per HRTF supportano alcuni parametri aggiuntivi, ad esempio [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)e [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), che specificano i valori predefiniti di queste impostazioni per i nuovi oggetti creati dal flusso.</span><span class="sxs-lookup"><span data-stu-id="76b73-218">The activation params for HRTF supports a few additional parameters, such as a [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), a [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), a [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype), and a [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), which specify the default values of these settings for new objects created from the stream.</span></span> <span data-ttu-id="76b73-219">Questi parametri sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="76b73-219">These parameters are optional.</span></span> <span data-ttu-id="76b73-220">Impostare i campi su **nullptr** per non specificare valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="76b73-220">Set the fields to **nullptr** to provide no default values.</span></span>

<span data-ttu-id="76b73-221">Chiamare [**ISpatialAudioClient:: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) per attivare il flusso.</span><span class="sxs-lookup"><span data-stu-id="76b73-221">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


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



<span data-ttu-id="76b73-222">Di seguito è riportato un codice specifico dell'app per supportare questo esempio, che genera in modo dinamico gli oggetti audio posizionati in modo casuale e li archivia in un vettore.</span><span class="sxs-lookup"><span data-stu-id="76b73-222">The following is some app-specific code to needed support this example, which will dynamically spawn randomly positioned audio objects and store them in a vector.</span></span>


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



<span data-ttu-id="76b73-223">Prima di immettere il ciclo di rendering audio, chiamare [**ISpatialAudioObjectRenderStreamForHrtf:: Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) per indicare alla pipeline multimediale di iniziare a richiedere dati audio.</span><span class="sxs-lookup"><span data-stu-id="76b73-223">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStreamForHrtf::Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) to instruct the media pipeline to begin requesting audio data.</span></span>

<span data-ttu-id="76b73-224">All'interno del ciclo di rendering, attendere l'evento di completamento del buffer fornito quando il flusso audio spaziale è stato inizializzato per essere segnalato.</span><span class="sxs-lookup"><span data-stu-id="76b73-224">Inside the render loop, wait for the buffer completion event we provided when the spatial audio stream was initialized to be signaled.</span></span> <span data-ttu-id="76b73-225">È necessario impostare un limite di timeout ragionevole, ad esempio 100 ms, durante l'attesa dell'evento perché qualsiasi modifica apportata al tipo di rendering o all'endpoint provocherà mai la segnalazione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="76b73-225">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="76b73-226">In questo caso, è possibile chiamare [**ISpatialAudioRenderStreamForHrtf:: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) per tentare di reimpostare il flusso audio spaziale.</span><span class="sxs-lookup"><span data-stu-id="76b73-226">In this case, you can call [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="76b73-227">Successivamente, chiamare [**ISpatialAudioRenderStreamForHrtf:: BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) per indicare al sistema che si sta per riempire i buffer degli oggetti audio con i dati.</span><span class="sxs-lookup"><span data-stu-id="76b73-227">Next, call [**ISpatialAudioRenderStreamForHrtf::BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="76b73-228">Questo metodo restituisce il numero di oggetti audio dinamici disponibili, non usato in questo esempio, e il conteggio dei frame del buffer per gli oggetti audio sottoposti a rendering da questo flusso.</span><span class="sxs-lookup"><span data-stu-id="76b73-228">This method returns the number of available dynamic audio objects, not used in this example, and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="76b73-229">Ogni volta che il contatore delle uova raggiunge il valore specificato, si attiverà un nuovo oggetto audio dinamico chiamando [**ISpatialAudioRenderStreamForHrtf:: ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) specificando [**AudioObjectType \_ Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span><span class="sxs-lookup"><span data-stu-id="76b73-229">Whenever the spawn counter reaches the specified value, we will activate a new dynamic audio object by calling [**ISpatialAudioRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) specifying [**AudioObjectType\_Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span></span> <span data-ttu-id="76b73-230">Se tutti gli oggetti audio dinamici disponibili sono già stati allocati, questo metodo restituirà **SPLAUDCLNT \_ E \_ nessun \_ altro \_ oggetto**.</span><span class="sxs-lookup"><span data-stu-id="76b73-230">If all available dynamic audio objects have already been allocated, this method will return **SPLAUDCLNT\_E\_NO\_MORE\_OBJECTS**.</span></span> <span data-ttu-id="76b73-231">In questo caso, è possibile scegliere di rilasciare uno o più oggetti audio precedentemente attivati in base alle priorità specifiche dell'app.</span><span class="sxs-lookup"><span data-stu-id="76b73-231">In this case, you can choose to release one or more previously activated audio objects based on your app-specific prioritization.</span></span> <span data-ttu-id="76b73-232">Dopo la creazione dell'oggetto audio dinamico, questo viene aggiunto a una nuova struttura **My3dObjectForHrtf** , con valori di posizione, rotazione, velocità, volume e frequenza casuali, che vengono quindi aggiunti all'elenco degli oggetti attivi.</span><span class="sxs-lookup"><span data-stu-id="76b73-232">After the dynamic audio object has been created, it is added to a new **My3dObjectForHrtf** structure, with randomized position, rotation, velocity, volume, and frequency values, which is then added to the list of active objects.</span></span>

<span data-ttu-id="76b73-233">Eseguire quindi l'iterazione di tutti gli oggetti attivi, rappresentati in questo esempio con la struttura **My3dObjectForHrtf** definita dall'app.</span><span class="sxs-lookup"><span data-stu-id="76b73-233">Next, iterate over all of the active objects, represented in this example with the app-defined **My3dObjectForHrtf** structure.</span></span> <span data-ttu-id="76b73-234">Per ogni oggetto audio, chiamare [**ISpatialAudioObjectForHrtf:: GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) per ottenere un puntatore al buffer audio dell'oggetto audio spaziale.</span><span class="sxs-lookup"><span data-stu-id="76b73-234">For each audio object, call [**ISpatialAudioObjectForHrtf::GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="76b73-235">Questo metodo restituisce anche le dimensioni, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="76b73-235">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="76b73-236">Il metodo helper, **WriteToAudioObjectBuffer**, elencato in precedenza in questo articolo, per riempire il buffer con dati audio.</span><span class="sxs-lookup"><span data-stu-id="76b73-236">The helper method, **WriteToAudioObjectBuffer**, listed previously in this article, to fill the buffer with audio data.</span></span> <span data-ttu-id="76b73-237">Dopo la scrittura nel buffer, nell'esempio vengono aggiornate la posizione e l'orientamento dell'oggetto audio HRTF chiamando [**ISpatialAudioObjectForHrtf:: seposition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) e [**ISpatialAudioObjectForHrtf::**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation)sequester.</span><span class="sxs-lookup"><span data-stu-id="76b73-237">After writing to the buffer, the example updates the position and orientation of the HRTF audio object by calling [**ISpatialAudioObjectForHrtf::SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) and [**ISpatialAudioObjectForHrtf::SetOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation).</span></span> <span data-ttu-id="76b73-238">In questo esempio viene usato un metodo helper, **CalculateEmitterConeOrientationMatrix**, per calcolare la matrice di orientamento in base alla direzione a cui punta l'oggetto 3D.</span><span class="sxs-lookup"><span data-stu-id="76b73-238">In this example, a helper method, **CalculateEmitterConeOrientationMatrix**, is used to calculate the orientation matrix given the direction the 3D object is pointing.</span></span> <span data-ttu-id="76b73-239">Di seguito è illustrata l'implementazione di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="76b73-239">The implementation of this method is shown below.</span></span> <span data-ttu-id="76b73-240">Il volume dell'oggetto audio può essere modificato anche chiamando [**ISpatialAudioObjectForHrtf:: Segain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain).</span><span class="sxs-lookup"><span data-stu-id="76b73-240">The volume of the audio object can also be modified by calling [**ISpatialAudioObjectForHrtf::SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain).</span></span> <span data-ttu-id="76b73-241">Se non si aggiorna la posizione, l'orientamento o il volume dell'oggetto, manterrà la posizione, l'orientamento e il volume dell'ultima volta in cui è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="76b73-241">If you don't update the position, orientation, or volume of the object, it will retain the position, orientation, and volume from the last time it was set.</span></span> <span data-ttu-id="76b73-242">Se è stata raggiunta la durata definita dall'app dell'oggetto, viene chiamato [**ISpatialAudioObjectForHrtf:: SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) per consentire alla pipeline audio di capire che non verrà scritto alcun altro audio usando questo oggetto e che l'oggetto sia impostato su **nullptr** per liberare le risorse.</span><span class="sxs-lookup"><span data-stu-id="76b73-242">If the object's app-defined lifetime has been reached, [**ISpatialAudioObjectForHrtf::SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="76b73-243">Dopo aver scritto i dati in tutti gli oggetti audio, chiamare [**ISpatialAudioRenderStreamForHrtf:: EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) per informare il sistema che i dati sono pronti per il rendering.</span><span class="sxs-lookup"><span data-stu-id="76b73-243">After writing data to all of your audio objects, call [**ISpatialAudioRenderStreamForHrtf::EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="76b73-244">È possibile chiamare **GetBuffer** solo tra una chiamata a **BeginUpdatingAudioObjects** e **EndUpdatingAudioObjects**.</span><span class="sxs-lookup"><span data-stu-id="76b73-244">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


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



<span data-ttu-id="76b73-245">Al termine del rendering dell'audio spaziale, arrestare il flusso audio spaziale chiamando [**ISpatialAudioRenderStreamForHrtf:: Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76b73-245">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioRenderStreamForHrtf::Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)).</span></span> <span data-ttu-id="76b73-246">Se non si intende usare nuovamente il flusso, liberare le risorse chiamando [**ISpatialAudioRenderStreamForHrtf:: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76b73-246">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).</span></span>


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



<span data-ttu-id="76b73-247">Nell'esempio di codice riportato di seguito viene illustrata l'implementazione del metodo helper **CalculateEmitterConeOrientationMatrix** , che è stato usato nell'esempio precedente per calcolare la matrice di orientamento in base alla direzione a cui punta l'oggetto 3D.</span><span class="sxs-lookup"><span data-stu-id="76b73-247">The following code example shows the implementation of the **CalculateEmitterConeOrientationMatrix** helper method which was used in the example above to calculate the orientation matrix given the direction the 3D object is pointing.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="76b73-248">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76b73-248">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76b73-249">Audio spaziale</span><span class="sxs-lookup"><span data-stu-id="76b73-249">Spatial Sound</span></span>](spatial-sound.md)
</dt> <dt>

[<span data-ttu-id="76b73-250">**ISpatialAudioClient**</span><span class="sxs-lookup"><span data-stu-id="76b73-250">**ISpatialAudioClient**</span></span>](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[<span data-ttu-id="76b73-251">**ISpatialAudioObject**</span><span class="sxs-lookup"><span data-stu-id="76b73-251">**ISpatialAudioObject**</span></span>](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 
