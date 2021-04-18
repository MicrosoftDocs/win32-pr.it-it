---
description: Microsoft Media Foundation supporta l'acquisizione audio e video.
ms.assetid: 8a9d96f8-1096-4b66-a2ec-8a95d754ea72
title: Acquisizione audio/video in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506c14ee4ab94a27cfafbe18a97ffa8f05676f1f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320691"
---
# <a name="audiovideo-capture-in-media-foundation"></a><span data-ttu-id="78df7-103">Acquisizione audio/video in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="78df7-103">Audio/Video Capture in Media Foundation</span></span>

<span data-ttu-id="78df7-104">Microsoft Media Foundation supporta l'acquisizione audio e video.</span><span class="sxs-lookup"><span data-stu-id="78df7-104">Microsoft Media Foundation supports audio and video capture.</span></span> <span data-ttu-id="78df7-105">I dispositivi di acquisizione video sono supportati tramite il driver di classe UVC ed è necessario che siano compatibili con UVC 1,1.</span><span class="sxs-lookup"><span data-stu-id="78df7-105">Video capture devices are supported through the UVC class driver and must be compatible with UVC 1.1.</span></span> <span data-ttu-id="78df7-106">I dispositivi di acquisizione audio sono supportati tramite l'API di sessione audio di Windows (WASAPI).</span><span class="sxs-lookup"><span data-stu-id="78df7-106">Audio capture devices are supported through Windows Audio Session API (WASAPI).</span></span>

<span data-ttu-id="78df7-107">Un dispositivo di acquisizione è rappresentato in Media Foundation da un oggetto di origine multimediale, che espone l'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="78df7-107">A capture device is represented in Media Foundation by a media source object, which exposes the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="78df7-108">Nella maggior parte dei casi, l'applicazione non userà direttamente questa interfaccia, ma userà un'API di livello superiore, ad esempio il [lettore di origine](source-reader.md) , per controllare il dispositivo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="78df7-108">In most cases, the application will not use this interface directly, but will use a higher-level API such as the [Source Reader](source-reader.md) to control the capture device.</span></span>

## <a name="enumerate-capture-devices"></a><span data-ttu-id="78df7-109">Enumera i dispositivi di acquisizione</span><span class="sxs-lookup"><span data-stu-id="78df7-109">Enumerate Capture Devices</span></span>

<span data-ttu-id="78df7-110">Per enumerare i dispositivi di acquisizione nel sistema, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="78df7-110">To enumerate the capture devices on the system, perform the following steps:</span></span>

1.  <span data-ttu-id="78df7-111">Chiamare la funzione [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="78df7-111">Call the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function to create an attribute store.</span></span>
2.  <span data-ttu-id="78df7-112">Impostare l'attributo del [ \_ tipo di origine dell' \_ attributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="78df7-112">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to one of the following values:</span></span>

    | <span data-ttu-id="78df7-113">Valore</span><span class="sxs-lookup"><span data-stu-id="78df7-113">Value</span></span>                                                    | <span data-ttu-id="78df7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78df7-114">Description</span></span>                      |
    |----------------------------------------------------------|----------------------------------|
    | <span data-ttu-id="78df7-115">**\_tipo di origine dell'attributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="78df7-115">**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**</span></span> | <span data-ttu-id="78df7-116">Enumerare i dispositivi di acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="78df7-116">Enumerate audio capture devices.</span></span> |
    | <span data-ttu-id="78df7-117">**\_tipo di origine dell'attributo MF DEVSOURCE \_ \_ \_ \_ VidCap \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="78df7-117">**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**</span></span> | <span data-ttu-id="78df7-118">Enumerare i dispositivi di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="78df7-118">Enumerate video capture devices.</span></span> |

    

     

3.  <span data-ttu-id="78df7-119">Chiamare la funzione [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="78df7-119">Call the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span> <span data-ttu-id="78df7-120">Questa funzione alloca una matrice di puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="78df7-120">This function allocates an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers.</span></span> <span data-ttu-id="78df7-121">Ogni puntatore rappresenta un oggetto attivazione per un dispositivo nel sistema.</span><span class="sxs-lookup"><span data-stu-id="78df7-121">Each pointer represents an activation object for one device on the system.</span></span>
4.  <span data-ttu-id="78df7-122">Chiamare il metodo [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) per creare un'istanza dell'origine multimediale da uno degli oggetti attivazione.</span><span class="sxs-lookup"><span data-stu-id="78df7-122">Call the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method to create an instance of the media source from one of the activation objects.</span></span>

<span data-ttu-id="78df7-123">Nell'esempio seguente viene creata un'origine multimediale per il primo dispositivo di acquisizione video nell'elenco enumerazione:</span><span class="sxs-lookup"><span data-stu-id="78df7-123">The following example creates a media source for the first video capture device in the enumeration list:</span></span>


```C++
HRESULT CreateVideoCaptureDevice(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    UINT32 count = 0;

    IMFAttributes *pConfig = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to hold the search criteria.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Request video capture devices.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }

    // Enumerate the devices,
    if (SUCCEEDED(hr))
    {
        hr = MFEnumDeviceSources(pConfig, &ppDevices, &count);
    }

    // Create a media source for the first device in the list.
    if (SUCCEEDED(hr))
    {
        if (count > 0)
        {
            hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(ppSource));
        }
        else
        {
            hr = MF_E_NOT_FOUND;
        }
    }

    for (DWORD i = 0; i < count; i++)
    {
        ppDevices[i]->Release();
    }
    CoTaskMemFree(ppDevices);
    return hr;
}
```



<span data-ttu-id="78df7-124">È possibile eseguire una query sugli oggetti attivazione per diversi attributi, inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="78df7-124">You can query the activation objects for various attributes, including the following:</span></span>

-   <span data-ttu-id="78df7-125">L'attributo del [ \_ \_ \_ \_ nome descrittivo dell'attributo MF DEVSOURCE](mf-devsource-attribute-friendly-name.md) contiene il nome visualizzato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78df7-125">The [MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME](mf-devsource-attribute-friendly-name.md) attribute contains the display name of the device.</span></span> <span data-ttu-id="78df7-126">Il nome visualizzato è adatto per la visualizzazione all'utente, ma potrebbe non essere univoco.</span><span class="sxs-lookup"><span data-stu-id="78df7-126">The display name is suitable for showing to the user, but might not be unique.</span></span>
-   <span data-ttu-id="78df7-127">Per i dispositivi video, l'attributo del [ \_ \_ \_ \_ \_ \_ \_ collegamento simbolico VidCap del tipo di origine dell'attributo MF DEVSOURCE](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) contiene il collegamento simbolico al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78df7-127">For video devices, the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute contains the symbolic link to the device.</span></span> <span data-ttu-id="78df7-128">Il collegamento simbolico identifica in modo univoco il dispositivo nel sistema, ma non è una stringa leggibile.</span><span class="sxs-lookup"><span data-stu-id="78df7-128">The symbolic link uniquely identifies the device on the system, but is not a readable string.</span></span>
-   <span data-ttu-id="78df7-129">Per i dispositivi audio, [il \_ tipo di origine dell'attributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ endpoint \_ ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) contiene l'ID dell'endpoint audio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78df7-129">For audio devices, the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attribute contains the audio endpoint ID of the device.</span></span> <span data-ttu-id="78df7-130">L'ID dell'endpoint audio è simile a un collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="78df7-130">The audio endpoint ID is similar to a symbolic link.</span></span> <span data-ttu-id="78df7-131">Identifica in modo univoco il dispositivo nel sistema, ma non è una stringa leggibile.</span><span class="sxs-lookup"><span data-stu-id="78df7-131">It uniquely identifies the device on the system, but is not a readable string.</span></span>

<span data-ttu-id="78df7-132">Nell'esempio seguente viene accettata una matrice di puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) e viene stampato il nome visualizzato di ogni dispositivo nella finestra di debug:</span><span class="sxs-lookup"><span data-stu-id="78df7-132">The following example takes an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers and prints the display name of each device to the debug window:</span></span>


```C++
void DebugShowDeviceNames(IMFActivate **ppDevices, UINT count)
{
    for (DWORD i = 0; i < count; i++)
    {
        HRESULT hr = S_OK;
        WCHAR *szFriendlyName = NULL;
    
        // Try to get the display name.
        UINT32 cchName;
        hr = ppDevices[i]->GetAllocatedString(
            MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME,
            &szFriendlyName, &cchName);

        if (SUCCEEDED(hr))
        {
            OutputDebugString(szFriendlyName);
            OutputDebugString(L"\n");
        }
        CoTaskMemFree(szFriendlyName);
    }
}
```



<span data-ttu-id="78df7-133">Se si conosce già il collegamento simbolico per un dispositivo video, è disponibile un altro modo per creare l'origine multimediale per il dispositivo:</span><span class="sxs-lookup"><span data-stu-id="78df7-133">If you already know the symbolic link for a video device, there is another way to create the media source for the device:</span></span>

1.  <span data-ttu-id="78df7-134">Chiamare [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="78df7-134">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span>
2.  <span data-ttu-id="78df7-135">Impostare l'attributo del [ \_ tipo di origine dell' \_ attributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) su **MF \_ DEVSOURCE \_ attributo \_ tipo di origine \_ \_ VidCap \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="78df7-135">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="78df7-136">Impostare l'attributo del [ \_ \_ \_ \_ \_ \_ \_ collegamento simbolico del tipo di origine dell'attributo MF DEVSOURCE VidCap](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) sul collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="78df7-136">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute to the symbolic link.</span></span>
4.  <span data-ttu-id="78df7-137">Chiamare la funzione [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) o [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="78df7-137">Call either the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span> <span data-ttu-id="78df7-138">Il primo restituisce un puntatore [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="78df7-138">The former returns an [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) pointer.</span></span> <span data-ttu-id="78df7-139">Il secondo restituisce un puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) a un oggetto Activation.</span><span class="sxs-lookup"><span data-stu-id="78df7-139">The latter returns an [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer to an activation object.</span></span> <span data-ttu-id="78df7-140">Per creare l'origine, è possibile usare l'oggetto Activation.</span><span class="sxs-lookup"><span data-stu-id="78df7-140">You can use the activation object to create the source.</span></span> <span data-ttu-id="78df7-141">È possibile effettuare il marshalling di un oggetto Activation a un altro processo, pertanto è utile se si desidera creare l'origine in un altro processo.</span><span class="sxs-lookup"><span data-stu-id="78df7-141">(An activation object can be marshaled to another process, so it is useful if you want to create the source in another process.</span></span> <span data-ttu-id="78df7-142">Per ulteriori informazioni, vedere [oggetti Activation](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="78df7-142">For more information, see [Activation Objects](activation-objects.md).)</span></span>

<span data-ttu-id="78df7-143">Nell'esempio seguente viene preso il collegamento simbolico di un dispositivo video e viene creata un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="78df7-143">The following example takes the symbolic link of a video device and creates a media source.</span></span>


```C++
HRESULT CreateVideoCaptureDevice(PCWSTR *pszSymbolicLink, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to video.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }


    // Set the symbolic link.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
            (LPCWSTR)pszSymbolicLink
            );            
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



<span data-ttu-id="78df7-144">Esiste un modo equivalente per creare un dispositivo audio dall'ID dell'endpoint audio:</span><span class="sxs-lookup"><span data-stu-id="78df7-144">There is an equivalent way to create an audio device from the audio endpoint ID:</span></span>

1.  <span data-ttu-id="78df7-145">Chiamare [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="78df7-145">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span>
2.  <span data-ttu-id="78df7-146">Impostare l'attributo del [ \_ tipo di origine dell' \_ attributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) su **MF \_ DEVSOURCE \_ attributo \_ tipo di origine \_ \_ AUDCAP \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="78df7-146">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="78df7-147">Impostare il [ \_ tipo di \_ origine attributo MF DEVSOURCE \_ \_ \_ AUDCAP \_ endpoint \_ ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attributo sull'ID endpoint.</span><span class="sxs-lookup"><span data-stu-id="78df7-147">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attribute to the endpoint ID.</span></span>
4.  <span data-ttu-id="78df7-148">Chiamare la funzione [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) o [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="78df7-148">Call either the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span>

<span data-ttu-id="78df7-149">Nell'esempio seguente viene preso un ID di endpoint audio e viene creata un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="78df7-149">The following example takes an audio endpoint ID and creates a media source.</span></span>


```C++
HRESULT CreateAudioCaptureDevice(PCWSTR *pszEndPointID, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to audio.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID
            );
    }

    // Set the endpoint ID.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID,
            (LPCWSTR)pszEndPointID
            ); 
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



## <a name="use-a-capture-device"></a><span data-ttu-id="78df7-150">Usare un dispositivo di acquisizione</span><span class="sxs-lookup"><span data-stu-id="78df7-150">Use a capture device</span></span>

<span data-ttu-id="78df7-151">Dopo aver creato l'origine multimediale per un dispositivo di acquisizione, usare il [lettore di origine](source-reader.md) per ottenere i dati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78df7-151">After you create the media source for a capture device, use the [Source Reader](source-reader.md) to get data from the device.</span></span> <span data-ttu-id="78df7-152">Il lettore di origine fornisce esempi di supporti che contengono i dati audio o i fotogrammi video di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="78df7-152">The Source Reader delivers media samples that contain the capture audio data or video frames.</span></span> <span data-ttu-id="78df7-153">Il passaggio successivo dipende dallo scenario dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="78df7-153">The next step depends on your application scenario:</span></span>

-   <span data-ttu-id="78df7-154">Anteprima video: usare Microsoft Direct3D o Direct2D per visualizzare il video.</span><span class="sxs-lookup"><span data-stu-id="78df7-154">Video preview: Use Microsoft Direct3D or Direct2D to display the video.</span></span>
-   <span data-ttu-id="78df7-155">Acquisizione file: usare il [writer di sink](sink-writer.md) per codificare il file.</span><span class="sxs-lookup"><span data-stu-id="78df7-155">File capture: Use the [Sink Writer](sink-writer.md) to encode the file.</span></span>
-   <span data-ttu-id="78df7-156">Anteprima audio: usare [WASAPI](/windows/desktop/CoreAudio/wasapi).</span><span class="sxs-lookup"><span data-stu-id="78df7-156">Audio preview: Use [WASAPI](/windows/desktop/CoreAudio/wasapi).</span></span>

<span data-ttu-id="78df7-157">Se si vuole combinare l'acquisizione audio con acquisizione video, usare l' *origine del supporto aggregato*.</span><span class="sxs-lookup"><span data-stu-id="78df7-157">If you want to combine audio capture with video capture, use the *aggregate media source*.</span></span> <span data-ttu-id="78df7-158">L'origine del supporto di aggregazione contiene una raccolta di origini multimediali e combina tutti i relativi flussi in un singolo oggetto di origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="78df7-158">The aggregate media source contains a collection of media sources and combines all of their streams into a single media source object.</span></span> <span data-ttu-id="78df7-159">Per creare un'istanza dell'origine multimediale aggregata, chiamare la funzione [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) .</span><span class="sxs-lookup"><span data-stu-id="78df7-159">To create an instance of the aggregate media source, call the [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) function.</span></span>

## <a name="shut-down-the-capture-device"></a><span data-ttu-id="78df7-160">Arrestare il dispositivo di acquisizione</span><span class="sxs-lookup"><span data-stu-id="78df7-160">Shut down the capture device</span></span>

<span data-ttu-id="78df7-161">Quando il dispositivo di acquisizione non è più necessario, è necessario arrestare il dispositivo chiamando [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sull'oggetto [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) ottenuto chiamando [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) o [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="78df7-161">When the capture device is no longer needed, you must shut down the device by calling [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) object you obtained by calling [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="78df7-162">La mancata chiamata di **Shutdown** può generare collegamenti di memoria perché il sistema può contenere un riferimento alle risorse **IMFMediaSource** fino a quando non viene chiamato **Shutdown** .</span><span class="sxs-lookup"><span data-stu-id="78df7-162">Failure to call **Shutdown** can result in memory links because the system may keep a reference to **IMFMediaSource** resources until **Shutdown** is called.</span></span>


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



<span data-ttu-id="78df7-163">Se è stata allocata una stringa contenente il collegamento simbolico a un dispositivo di acquisizione, è necessario rilasciare anche questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="78df7-163">If you allocated a string containing the symbolic link to a capture device, you should release this object as well.</span></span>


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a><span data-ttu-id="78df7-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="78df7-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78df7-165">Acquisizione di audio/video</span><span class="sxs-lookup"><span data-stu-id="78df7-165">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> </dl>

 

 
