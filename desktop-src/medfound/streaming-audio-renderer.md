---
description: Il renderer di streaming audio (SAR) è un sink multimediale che esegue il rendering dell'audio.
ms.assetid: 5884a128-597d-432b-a706-e10c894d7965
title: Renderer audio di streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59c5b55f197d5e9770c6f1be55f680c7f9136f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308989"
---
# <a name="streaming-audio-renderer"></a><span data-ttu-id="e7c25-103">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="e7c25-103">Streaming Audio Renderer</span></span>

<span data-ttu-id="e7c25-104">Il renderer di streaming audio (SAR) è un sink multimediale che esegue il rendering dell'audio.</span><span class="sxs-lookup"><span data-stu-id="e7c25-104">The streaming audio renderer (SAR) is a media sink that renders audio.</span></span> <span data-ttu-id="e7c25-105">Ogni istanza del SAR esegue il rendering di un singolo flusso audio.</span><span class="sxs-lookup"><span data-stu-id="e7c25-105">Each instance of the SAR renders a single audio stream.</span></span> <span data-ttu-id="e7c25-106">Per eseguire il rendering di più flussi, usare più istanze del SAR.</span><span class="sxs-lookup"><span data-stu-id="e7c25-106">To render multiple streams, use multiple instances of the SAR.</span></span>

<span data-ttu-id="e7c25-107">Per creare il SAR, chiamare una delle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7c25-107">To create the SAR, call either of the following functions:</span></span>

-   <span data-ttu-id="e7c25-108">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer).</span><span class="sxs-lookup"><span data-stu-id="e7c25-108">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer).</span></span> <span data-ttu-id="e7c25-109">Restituisce un puntatore a SAR.</span><span class="sxs-lookup"><span data-stu-id="e7c25-109">Returns a pointer to the SAR.</span></span>
-   <span data-ttu-id="e7c25-110">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate).</span><span class="sxs-lookup"><span data-stu-id="e7c25-110">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate).</span></span> <span data-ttu-id="e7c25-111">Restituisce un puntatore a un oggetto Activation, che può essere usato per creare il SAR.</span><span class="sxs-lookup"><span data-stu-id="e7c25-111">Returns a pointer to an activation object, which can be used to create the SAR.</span></span>

<span data-ttu-id="e7c25-112">La seconda funzione, che restituisce un oggetto Activation, è obbligatoria se si sta riproducendo contenuto protetto, perché l'oggetto di attivazione deve essere serializzato nel processo protetto.</span><span class="sxs-lookup"><span data-stu-id="e7c25-112">The second function, which returns an activation object, is required if you are playing protected content, because the activation object must be serialized to the protected process.</span></span> <span data-ttu-id="e7c25-113">Per il contenuto non crittografato, è possibile usare una delle due funzioni.</span><span class="sxs-lookup"><span data-stu-id="e7c25-113">For clear content, you can use either function.</span></span>

<span data-ttu-id="e7c25-114">Il SAR può ricevere audio non compresso in formato PCM o IEEE a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="e7c25-114">The SAR can receive uncompressed audio in either PCM or IEEE floating-point format.</span></span> <span data-ttu-id="e7c25-115">Se la velocità di riproduzione è più veloce o più lenta di 1 ×, il valore di SAR regola automaticamente il passo.</span><span class="sxs-lookup"><span data-stu-id="e7c25-115">If the playback rate is faster or slower than 1×, the SAR automatically adjusts the pitch.</span></span>

## <a name="configuring-the-audio-renderer"></a><span data-ttu-id="e7c25-116">Configurazione del renderer audio</span><span class="sxs-lookup"><span data-stu-id="e7c25-116">Configuring the Audio Renderer</span></span>

<span data-ttu-id="e7c25-117">Il SAR supporta diversi attributi di configurazione.</span><span class="sxs-lookup"><span data-stu-id="e7c25-117">The SAR supports several configuration attributes.</span></span> <span data-ttu-id="e7c25-118">Il meccanismo per l'impostazione di questi attributi dipende dalla funzione chiamata per creare il SAR.</span><span class="sxs-lookup"><span data-stu-id="e7c25-118">The mechanism for setting these attributes depends on which function you call to create the SAR.</span></span> <span data-ttu-id="e7c25-119">Se si usa la funzione [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) , eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7c25-119">If you use the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function, do the following:</span></span>

1.  <span data-ttu-id="e7c25-120">Creare un nuovo archivio di attributi chiamando [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="e7c25-120">Create a new attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="e7c25-121">Aggiungere gli attributi all'archivio attributi.</span><span class="sxs-lookup"><span data-stu-id="e7c25-121">Add the attributes to the attribute store.</span></span>
3.  <span data-ttu-id="e7c25-122">Passare l'archivio attributi alla funzione [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) nel parametro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="e7c25-122">Pass the attribute store to the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function in the *pAudioAttributes* parameter.</span></span>

<span data-ttu-id="e7c25-123">Se si usa la funzione [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) , la funzione restituisce un puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) nel parametro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="e7c25-123">If you use the [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) function, the function returns a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface in the *ppActivate* parameter.</span></span> <span data-ttu-id="e7c25-124">Utilizzare questo puntatore per aggiungere gli attributi.</span><span class="sxs-lookup"><span data-stu-id="e7c25-124">Use this pointer to add the attributes.</span></span>

<span data-ttu-id="e7c25-125">Per un elenco degli attributi di configurazione, vedere [attributi del renderer audio](audio-renderer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e7c25-125">For a list of configuration attributes, see [Audio Renderer Attributes](audio-renderer-attributes.md).</span></span>

## <a name="selecting-the-audio-endpoint-device"></a><span data-ttu-id="e7c25-126">Selezione del dispositivo dell'endpoint audio</span><span class="sxs-lookup"><span data-stu-id="e7c25-126">Selecting the Audio Endpoint Device</span></span>

<span data-ttu-id="e7c25-127">Un *dispositivo endpoint audio* è un dispositivo hardware che esegue il rendering o acquisisce audio.</span><span class="sxs-lookup"><span data-stu-id="e7c25-127">An *audio endpoint device* is a hardware device that either renders or captures audio.</span></span> <span data-ttu-id="e7c25-128">Gli esempi includono altoparlanti, cuffie, microfoni e lettori CD.</span><span class="sxs-lookup"><span data-stu-id="e7c25-128">Examples include speakers, headphones, microphones, and CD players.</span></span> <span data-ttu-id="e7c25-129">Il SAR usa sempre un dispositivo di rendering audio.</span><span class="sxs-lookup"><span data-stu-id="e7c25-129">The SAR always uses an audio rendering device.</span></span> <span data-ttu-id="e7c25-130">Esistono due modi per selezionare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7c25-130">There are two ways to select the device.</span></span>

<span data-ttu-id="e7c25-131">Il primo approccio consiste nell'enumerare i dispositivi di rendering audio nel sistema, usando l'interfaccia [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="e7c25-131">The first approach is to enumerate the audio rendering devices on the system, using the [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="e7c25-132">Questa interfaccia è documentata nella documentazione principale dell'API audio.</span><span class="sxs-lookup"><span data-stu-id="e7c25-132">This interface is documented in the core audio API documentation.</span></span>

1.  <span data-ttu-id="e7c25-133">Creare l'oggetto enumeratore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7c25-133">Create the device enumerator object.</span></span>
2.  <span data-ttu-id="e7c25-134">Usare l'enumeratore Device per enumerare i dispositivi di rendering audio.</span><span class="sxs-lookup"><span data-stu-id="e7c25-134">Use the device enumerator to enumerate audio rendering devices.</span></span> <span data-ttu-id="e7c25-135">Ogni dispositivo è rappresentato da un puntatore all'interfaccia [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) .</span><span class="sxs-lookup"><span data-stu-id="e7c25-135">Each device is represented by a pointer to the [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span>
3.  <span data-ttu-id="e7c25-136">Selezionare un dispositivo in base alle proprietà del dispositivo o alla selezione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e7c25-136">Select a device, based on the device properties or the user's selection.</span></span>
4.  <span data-ttu-id="e7c25-137">Chiamare [**IMMDevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) per ottenere l'identificatore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7c25-137">Call [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to get the device identifier.</span></span>
5.  <span data-ttu-id="e7c25-138">Impostare l'identificatore del dispositivo come valore dell'attributo [**dell' \_ \_ \_ \_ \_ ID endpoint dell'attributo MF audio RENDERER**](mf-audio-renderer-attribute-endpoint-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e7c25-138">Set the device identifier as the value of the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) attribute.</span></span>

<span data-ttu-id="e7c25-139">Anziché enumerare i dispositivi, è possibile specificare il dispositivo audio in base al *ruolo*.</span><span class="sxs-lookup"><span data-stu-id="e7c25-139">Rather than enumerate devices, you can specify the audio device by its *role*.</span></span> <span data-ttu-id="e7c25-140">Un ruolo audio identifica una categoria generale di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e7c25-140">An audio role identifies a general category of usage.</span></span> <span data-ttu-id="e7c25-141">Ad esempio, il ruolo *console* è definito per i giochi e le notifiche di sistema, mentre il ruolo *multimediale* è definito per musica e filmati.</span><span class="sxs-lookup"><span data-stu-id="e7c25-141">For example, the *console* role is defined for games and system notifications, while the *multimedia* role is defined for music and movies.</span></span> <span data-ttu-id="e7c25-142">A ogni ruolo è assegnato un dispositivo di rendering audio e l'utente può modificare queste assegnazioni.</span><span class="sxs-lookup"><span data-stu-id="e7c25-142">Each role has one audio rendering device assigned to it, and the user can change these assignments.</span></span> <span data-ttu-id="e7c25-143">Se si specifica un ruolo del dispositivo, il SAR usa qualsiasi dispositivo audio assegnato a tale ruolo.</span><span class="sxs-lookup"><span data-stu-id="e7c25-143">If you specify a device role, the SAR uses whatever audio device has been assigned for that role.</span></span> <span data-ttu-id="e7c25-144">Per specificare il ruolo del dispositivo, impostare l'attributo del [**\_ \_ \_ \_ \_ ruolo endpoint dell'attributo MF audio RENDERER**](mf-audio-renderer-attribute-endpoint-role-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e7c25-144">To specify the device role, set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) attribute.</span></span>

<span data-ttu-id="e7c25-145">I due attributi elencati in questa sezione si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="e7c25-145">The two attributes listed in this section are mutually exclusive.</span></span> <span data-ttu-id="e7c25-146">Se non si imposta una di esse, il SAR usa il dispositivo audio assegnato al ruolo **eConsole** .</span><span class="sxs-lookup"><span data-stu-id="e7c25-146">If you do not set either of them, the SAR uses the audio device that is assigned to the **eConsole** role.</span></span>

<span data-ttu-id="e7c25-147">Il codice seguente enumera i dispositivi di rendering audio e assegna il primo dispositivo nell'elenco al SAR.</span><span class="sxs-lookup"><span data-stu-id="e7c25-147">The following code enumerates the audio rendering devices and assigns the first device in the list to the SAR.</span></span> <span data-ttu-id="e7c25-148">In questo esempio viene usata la funzione [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) per creare il SAR.</span><span class="sxs-lookup"><span data-stu-id="e7c25-148">This example uses the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function to create the SAR.</span></span>


```C++
#include <mmdeviceapi.h>

HRESULT hr = S_OK;

IMMDeviceEnumerator *pEnum = NULL;      // Audio device enumerator.
IMMDeviceCollection *pDevices = NULL;   // Audio device collection.
IMMDevice *pDevice = NULL;              // An audio device.
IMFAttributes *pAttributes = NULL;      // Attribute store.
IMFMediaSink *pSink = NULL;             // Streaming audio renderer (SAR)

LPWSTR wstrID = NULL;                   // Device ID.

// Create the device enumerator.
hr = CoCreateInstance(
    __uuidof(MMDeviceEnumerator), 
    NULL,
    CLSCTX_ALL, 
    __uuidof(IMMDeviceEnumerator), 
    (void**)&pEnum
    );

// Enumerate the rendering devices.
if (SUCCEEDED(hr))
{
    hr = pEnum->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pDevices);
}

// Get ID of the first device in the list.
if (SUCCEEDED(hr))
{
    hr = pDevices->Item(0, &pDevice);
}

if (SUCCEEDED(hr))
{
    hr = pDevice->GetId(&wstrID);
}

// Create an attribute store and set the device ID attribute.
if (SUCCEEDED(hr))
{
    hr = MFCreateAttributes(&pAttributes, 2);
}

if (SUCCEEDED(hr))
{
    hr = pAttributes->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

// Create the audio renderer.
if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRenderer(pAttributes, &pSink);    
}

SAFE_RELEASE(pEnum);
SAFE_RELEASE(pDevices);
SAFE_RELEASE(pDevice); 
SAFE_RELEASE(pAttributes);
CoTaskMemFree(wstrID);
```



<span data-ttu-id="e7c25-149">Per creare l'oggetto attivazione per il SAR, modificare il codice visualizzato dopo la chiamata a [**IMMDevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="e7c25-149">To create the activation object for the SAR, change the code that appears after the call to [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to the following:</span></span>


```C++
IMFActivate *pActivate = NULL;          // Activation object.

if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRendererActivate(&pActivate);    
}

if (SUCCEEDED(hr))
{
    hr = pActivate->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

SAFE_RELEASE(pActivate);
```



## <a name="selecting-the-audio-session"></a><span data-ttu-id="e7c25-150">Selezione della sessione audio</span><span class="sxs-lookup"><span data-stu-id="e7c25-150">Selecting the Audio Session</span></span>

<span data-ttu-id="e7c25-151">Una sessione audio è un gruppo di flussi audio correlati che un'applicazione può gestire collettivamente.</span><span class="sxs-lookup"><span data-stu-id="e7c25-151">An audio session is a group of related audio streams that an application can manage collectively.</span></span> <span data-ttu-id="e7c25-152">L'applicazione può controllare il livello del volume e lo stato di silenziamento di ogni sessione.</span><span class="sxs-lookup"><span data-stu-id="e7c25-152">The application can control the volume level and mute state of each session.</span></span> <span data-ttu-id="e7c25-153">Le sessioni sono identificate dal GUID.</span><span class="sxs-lookup"><span data-stu-id="e7c25-153">Sessions are identified by GUID.</span></span> <span data-ttu-id="e7c25-154">Per specificare la sessione audio per il SAR, usare l'attributo dell' [ID di sessione dell' \_ attributo MF audio \_ RENDERER \_ \_ \_ ](mf-audio-renderer-attribute-session-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e7c25-154">To specify the audio session for the SAR, use the [MF\_AUDIO\_RENDERER\_ATTRIBUTE\_SESSION\_ID](mf-audio-renderer-attribute-session-id-attribute.md) attribute.</span></span> <span data-ttu-id="e7c25-155">Se non si imposta questo attributo, il SAR viene aggiunto alla sessione predefinita per il processo, identificato dal **GUID \_ null**.</span><span class="sxs-lookup"><span data-stu-id="e7c25-155">If you do not set this attribute, the SAR joins the default session for that process, identified by **GUID\_NULL**.</span></span>

<span data-ttu-id="e7c25-156">Per impostazione predefinita, una sessione audio è specifica del processo, ovvero contiene solo flussi dal processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="e7c25-156">By default, an audio session is process-specific, meaning it contains only streams from the calling process.</span></span> <span data-ttu-id="e7c25-157">Per partecipare a una sessione tra processi, impostare l'attributo per l'attributo dei [ \_ \_ \_ \_ flag di rendering dell'audio MF](mf-audio-renderer-attribute-flags-attribute.md) con il valore **MF \_ audio \_ renderer \_ Attribute \_ flags \_ CROSSPROCESS**.</span><span class="sxs-lookup"><span data-stu-id="e7c25-157">To join a cross-process session, set the [MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS](mf-audio-renderer-attribute-flags-attribute.md) attribute with the value **MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_CROSSPROCESS**.</span></span>

<span data-ttu-id="e7c25-158">Dopo aver creato il SAR, utilizzare l'interfaccia [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) per aggiungere la sessione a un gruppo di sessioni, tutte controllate dallo stesso controllo volume nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="e7c25-158">After you create the SAR, you use the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface to join the session to a group of sessions, all of which are controlled by the same volume control in the control panel.</span></span> <span data-ttu-id="e7c25-159">È anche possibile usare questa interfaccia per impostare il nome visualizzato e l'icona che vengono visualizzati nel controllo volume.</span><span class="sxs-lookup"><span data-stu-id="e7c25-159">You can also use this interface to set the display name and the icon that appear in the volume control.</span></span>

## <a name="controlling-volume-levels"></a><span data-ttu-id="e7c25-160">Controllo di livelli di volume</span><span class="sxs-lookup"><span data-stu-id="e7c25-160">Controlling Volume Levels</span></span>

<span data-ttu-id="e7c25-161">Per controllare il livello del volume master di tutti i flussi nella sessione audio di SAR, usare l'interfaccia [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) .</span><span class="sxs-lookup"><span data-stu-id="e7c25-161">To control the master volume level of all the streams in the SAR's audio session, use the [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) interface.</span></span> <span data-ttu-id="e7c25-162">Per controllare il volume di un singolo flusso o per controllare il volume dei singoli canali all'interno di un flusso, usare l'interfaccia [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) .</span><span class="sxs-lookup"><span data-stu-id="e7c25-162">To control the volume of an individual stream, or to control the volume of individual channels within a stream, use the [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) interface.</span></span> <span data-ttu-id="e7c25-163">Entrambe le interfacce vengono ottenute chiamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice).</span><span class="sxs-lookup"><span data-stu-id="e7c25-163">Both interfaces are obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice).</span></span> <span data-ttu-id="e7c25-164">È possibile chiamare **GetService** direttamente sul SAR o chiamarlo nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="e7c25-164">You can call **GetService** directly on the SAR, or call it on the Media Session.</span></span> <span data-ttu-id="e7c25-165">I livelli di volume sono espressi come valori di attenuazione.</span><span class="sxs-lookup"><span data-stu-id="e7c25-165">Volume levels are expressed as attenuation values.</span></span> <span data-ttu-id="e7c25-166">Per ogni canale, il livello di attenuazione è il prodotto del volume master e del volume del canale.</span><span class="sxs-lookup"><span data-stu-id="e7c25-166">For each channel, the attenuation level is the product of the master volume and the channel volume.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7c25-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7c25-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7c25-168">Riproduzione di audio/video</span><span class="sxs-lookup"><span data-stu-id="e7c25-168">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 
