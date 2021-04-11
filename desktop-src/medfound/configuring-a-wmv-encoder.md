---
description: Configurazione di un codificatore WMV
ms.assetid: 6e690d17-da17-452a-aa9a-9701a560856b
title: Configurazione di un codificatore WMV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6324071257dd9d56e33d1dc6ece4886ee73661ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127959"
---
# <a name="configuring-a-wmv-encoder"></a><span data-ttu-id="3c6d7-103">Configurazione di un codificatore WMV</span><span class="sxs-lookup"><span data-stu-id="3c6d7-103">Configuring a WMV Encoder</span></span>

<span data-ttu-id="3c6d7-104">Per creare un tipo di output valido per un codificatore Windows Media Video (WMV), è necessario disporre delle seguenti informazioni:</span><span class="sxs-lookup"><span data-stu-id="3c6d7-104">To create a valid output type for a Windows Media Video (WMV) encoder, you must have the following information:</span></span>

-   <span data-ttu-id="3c6d7-105">Il formato del video non compresso da codificare.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-105">The format of the uncompressed video that you will encode.</span></span>
-   <span data-ttu-id="3c6d7-106">Sottotipo video che repesents il formato WMV codificato.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-106">The video subtype that repesents the encoded WMV format.</span></span> <span data-ttu-id="3c6d7-107">Vedere [GUID del sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3c6d7-107">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="3c6d7-108">Velocità in bit di destinazione per il flusso codificato.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-108">The target bitrate for the encoded stream.</span></span>
-   <span data-ttu-id="3c6d7-109">Proprietà di configurazione da impostare sul codificatore.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-109">The configuration properties to set on the encoder.</span></span>

<span data-ttu-id="3c6d7-110">Le proprietà di configurazione sono documentate nella documentazione relativa a Windows Media Audio e codec video e alle API DSP.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-110">The configuration properties are documented in the Windows Media Audio and Video Codec and DSP APIs documentation.</span></span> <span data-ttu-id="3c6d7-111">Per ulteriori informazioni, vedere "proprietà del flusso video" nelle [proprietà di codifica](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="3c6d7-111">For more information, see "Video Stream Properties" in [Encoding Properties](configuring-the-encoder.md).</span></span>

<span data-ttu-id="3c6d7-112">Per ottenere un tipo di output valido per il codificatore, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-112">To get a valid output type for the encoder, perform the following steps.</span></span>

1.  <span data-ttu-id="3c6d7-113">Utilizzare la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) per creare un'istanza del codificatore.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-113">Use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function to create an instance of the encoder.</span></span>
2.  <span data-ttu-id="3c6d7-114">Eseguire una query sul codificatore per l'interfaccia **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="3c6d7-114">Query the encoder for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="3c6d7-115">Utilizzare l'interfaccia **IPropertyStore** per configurare il codificatore.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-115">Use the **IPropertyStore** interface to configure the encoder.</span></span>
4.  <span data-ttu-id="3c6d7-116">Chiamare [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) per impostare il tipo di video non compresso nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-116">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the uncompressed video type on the encoder.</span></span>
5.  <span data-ttu-id="3c6d7-117">Chiamare [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere l'elenco dei formati di compressione dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-117">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the list of compression formats from the encoder.</span></span> <span data-ttu-id="3c6d7-118">I codificatori WMV non restituiscono un tipo di supporto completo da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-118">The WMV encoders do not return a complete media type from this method.</span></span> <span data-ttu-id="3c6d7-119">Nei tipi di supporto mancano due informazioni:</span><span class="sxs-lookup"><span data-stu-id="3c6d7-119">The media types are missing two pieces of information:</span></span>

    -   <span data-ttu-id="3c6d7-120">Velocità in bit di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-120">The target bitrate.</span></span>
    -   <span data-ttu-id="3c6d7-121">Dati del codec privato dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-121">Private codec data from the encoder.</span></span>

    <span data-ttu-id="3c6d7-122">Prima di impostare il tipo di output nel codificatore, è necessario aggiungere entrambi gli elementi al tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-122">Before setting the output type on the encoder, you must add both of these items to the media type.</span></span>

6.  <span data-ttu-id="3c6d7-123">Per specificare la velocità in bit di destinazione, impostare l'attributo [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) sul tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-123">To specify the target bitrate, set the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the media type.</span></span>
7.  <span data-ttu-id="3c6d7-124">Aggiungere i dati del codec privato al tipo di supporto, come illustrato nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-124">Add the private codec data to the media type, as explained in the next section.</span></span>
8.  <span data-ttu-id="3c6d7-125">Chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il tipo di supporto di compressione nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-125">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

### <a name="private-codec-data"></a><span data-ttu-id="3c6d7-126">Dati del codec privato</span><span class="sxs-lookup"><span data-stu-id="3c6d7-126">Private Codec Data</span></span>

<span data-ttu-id="3c6d7-127">I dati del codec privato sono una struttura di dati opaca che è necessario ottenere dal codificatore WMV e aggiungere al tipo di compressione, prima di impostare il tipo di compressione nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-127">The private codec data is an opaque data structure that you must get from the WMV encoder and add to the compression type, before setting the compression type on the encoder.</span></span> <span data-ttu-id="3c6d7-128">Per ottenere i dati privati, è necessario usare l'interfaccia **IWMCodecPrivateData** , documentata in Windows Media Format 11 SDK.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-128">To get the private data, you must use the **IWMCodecPrivateData** interface, which is documented in the Windows Media Format 11 SDK.</span></span>

<span data-ttu-id="3c6d7-129">Per ottenere i dati del codec privato, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="3c6d7-129">To get the private codec data, perform the following steps:</span></span>

1.  <span data-ttu-id="3c6d7-130">Chiamare [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere un tipo di supporto dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-130">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get a media type from the encoder.</span></span> <span data-ttu-id="3c6d7-131">(Questo è il passaggio 6 della sezione precedente).</span><span class="sxs-lookup"><span data-stu-id="3c6d7-131">(This is step 6 from the previous section.)</span></span>
2.  <span data-ttu-id="3c6d7-132">Specificare la velocità in bit di destinazione impostando l'attributo [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) sul tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-132">Specify the target bitrate by setting the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the media type.</span></span>
3.  <span data-ttu-id="3c6d7-133">Convertire il tipo di supporto in una struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) chiamando la funzione [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="3c6d7-133">Convert the media type into a [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure by calling the [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) function.</span></span>
4.  <span data-ttu-id="3c6d7-134">Eseguire una query sul codificatore per l'interfaccia **IWMCodecPrivateData** .</span><span class="sxs-lookup"><span data-stu-id="3c6d7-134">Query the encoder for the **IWMCodecPrivateData** interface.</span></span>
5.  <span data-ttu-id="3c6d7-135">Chiamare il metodo **IWMCodecPrivateData:: SetPartialOutputType** , passando la struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) convertito.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-135">Call the **IWMCodecPrivateData::SetPartialOutputType** method, passing in the converted [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span>
6.  <span data-ttu-id="3c6d7-136">Chiamare il metodo **IWMCodecPrivateData:: GetPrivateData** due volte, una volta per ottenere la dimensione del buffer per i dati privati e una volta per copiare i dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-136">Call the **IWMCodecPrivateData::GetPrivateData** method twice, once to get the size of the buffer for the private data, and once to copy the data into the buffer.</span></span>
7.  <span data-ttu-id="3c6d7-137">Aggiungere i dati privati al tipo di supporto impostando l' [**attributo \_ \_ \_ dati utente MF mt**](mf-mt-user-data-attribute.md) sul tipo.</span><span class="sxs-lookup"><span data-stu-id="3c6d7-137">Add the private data to the media type by setting the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute on the type.</span></span>

<span data-ttu-id="3c6d7-138">Nell'esempio esteso seguente viene illustrato come creare un formato di compressione WMV da un tipo di video non compresso:</span><span class="sxs-lookup"><span data-stu-id="3c6d7-138">The following extended example shows how to create a WMV compression format from an uncompressed video type:</span></span>


```C++
#include <wmcodecdsp.h>
#include <Wmsdk.h>
#include <Dmo.h>
#include <mfapi.h>
#include <uuids.h>

#include <mfidl.h>
#include <mftransform.h>
#include <mferror.h>

#pragma comment(lib, "Msdmo")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "strmiids")
#pragma comment(lib, "propsys")

HRESULT GetEncodedVideoType(
    IMFMediaType *pTypeIn, 
    REFGUID subtype,
    UINT32 TargetBitrate, 
    IPropertyStore *pEncoderProps, 
    IMFMediaType **ppEncodingType,
    DWORD mftEnumFlags = MFT_ENUM_FLAG_SYNCMFT
    );

HRESULT CreateVideoEncoder(REFGUID subtype, DWORD mftEnumFlags, IMFTransform **ppMFT);
HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut);
HRESULT CopyPropertyStore(IPropertyStore *pSrc, IPropertyStore *pDest);

//
// GetEncodedVideoType
// Given an uncompressed video type, finds a suitable WMV type.
//

HRESULT GetEncodedVideoType(
    IMFMediaType *pTypeIn,          // Uncompressed format
    REFGUID subtype,                // Compression format
    UINT32 TargetBitrate,           // Target bit rate
    IPropertyStore *pEncoderProps,  // Encoder properties (can be NULL)
    IMFMediaType **ppEncodingType,  // Receives the WMV type.
    DWORD mftEnumFlags              // MFTEnumEx flags
    )
{
    HRESULT hr = S_OK;

    IMFTransform *pMFT = NULL;
    IPropertyStore *pPropStore = NULL;
    IMFMediaType *pTypeOut = NULL;

    // Instantiate the encoder
    hr = CreateVideoEncoder(subtype, mftEnumFlags, &pMFT);

    // Copy the properties to the encoder.

    if (SUCCEEDED(hr))
    {
        if (pEncoderProps)
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPropStore));

            if (SUCCEEDED(hr))
            {
                hr = CopyPropertyStore(pEncoderProps, pPropStore);
            }
        }
    }

    // Set the uncompressed type.
    if (SUCCEEDED(hr))
    {
        hr = pMFT->SetInputType(0, pTypeIn, 0);
    }

    // Get the partial output type
    if (SUCCEEDED(hr))
    {
        hr = pMFT->GetOutputAvailableType(0, 0, &pTypeOut);
    }

    // Set the bit rate.
    // You must set this before getting the codec private data.

    if (SUCCEEDED(hr))
    {
        hr = pTypeOut->SetUINT32(MF_MT_AVG_BITRATE, TargetBitrate);   
    }

    if (SUCCEEDED(hr))
    {
        hr = AddPrivateData(pMFT, pTypeOut);
    }

    if (SUCCEEDED(hr))
    {
        hr = pMFT->SetOutputType(0, pTypeOut, 0);
    }

    if (SUCCEEDED(hr))
    {
        *ppEncodingType = pTypeOut;
        (*ppEncodingType)->AddRef();
    }

    SafeRelease(&pMFT);
    SafeRelease(&pPropStore);
    SafeRelease(&pTypeOut);
    return hr;
}
```



<span data-ttu-id="3c6d7-139">La funzione CreateVideoEncoder crea un codificatore video per un sottotipo video specificato, ad esempio **MFVideoFormat \_ WMV3**:</span><span class="sxs-lookup"><span data-stu-id="3c6d7-139">The CreateVideoEncoder function creates a video encoder for a specified video subtype, such as **MFVideoFormat\_WMV3**:</span></span>


```C++
//
// CreateVideoEncoder
// Creates a video encoder for a specified video subtype.
//

HRESULT CreateVideoEncoder(
    REFGUID subtype,            // Encoding subtype.
    DWORD mftEnumFlags,         // Flags for MFTEnumEx
    IMFTransform **ppMFT        // Receives a pointer to the encoder.
    )
{
    HRESULT hr = S_OK;
    IMFTransform *pMFT = NULL;

    MFT_REGISTER_TYPE_INFO info;
    info.guidMajorType = MFMediaType_Video;
    info.guidSubtype = subtype;

    IMFActivate **ppActivates = NULL;    
    UINT32 count = 0;

    hr = MFTEnumEx(
        MFT_CATEGORY_VIDEO_ENCODER,
        mftEnumFlags | MFT_ENUM_FLAG_SORTANDFILTER,
        NULL,
        &info,
        &ppActivates,
        &count
        );

    if (count == 0)
    {
        hr = E_FAIL;
    }

    if (SUCCEEDED(hr))
    {
        hr = ppActivates[0]->ActivateObject(
            __uuidof(IMFTransform),
            (void**)&pMFT
            );
    }

    if (SUCCEEDED(hr))
    {
        *ppMFT = pMFT;
        (*ppMFT)->AddRef();
    }

    // Clean up

    for (DWORD i = 0; i < count; i++)
    {
        ppActivates[i]->Release();
    }
    CoTaskMemFree(ppActivates);
    SafeRelease(&pMFT);
    return hr;
}
```



<span data-ttu-id="3c6d7-140">La funzione AddPrivateData aggiunge i dati del codec privato al tipo di compressione:</span><span class="sxs-lookup"><span data-stu-id="3c6d7-140">The AddPrivateData function adds the private codec data to the compression type:</span></span>


```C++
//
// AddPrivateData
// Appends the private codec data to a media type.
//
// pMFT: The video encoder
// pTypeOut: A video type from the encoder's type list.
//
// The function modifies pTypeOut by adding the codec data.
//

HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
{
    HRESULT hr = S_OK;
    ULONG cbData = 0;
    BYTE *pData = NULL;

    IWMCodecPrivateData *pPrivData = NULL;

    DMO_MEDIA_TYPE mtOut = { 0 };

    // Convert the type to a DMO type.
    hr = MFInitAMMediaTypeFromMFMediaType(
        pTypeOut, 
        FORMAT_VideoInfo, 
        (AM_MEDIA_TYPE*)&mtOut
        );
    
    if (SUCCEEDED(hr))
    {
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
    }

    if (SUCCEEDED(hr))
    {
        hr = pPrivData->SetPartialOutputType(&mtOut);
    }

    //
    // Get the private codec data
    //

    // First get the buffer size.
    if (SUCCEEDED(hr))
    {
        hr = pPrivData->GetPrivateData(NULL, &cbData);
    }

    if (SUCCEEDED(hr))
    {
        pData = new BYTE[cbData];

        if (pData == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Now get the data.
    if (SUCCEEDED(hr))
    {
        hr = pPrivData->GetPrivateData(pData, &cbData);
    }

    // Add the data to the media type.
    if (SUCCEEDED(hr))
    {
        hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
    }

    delete [] pData;
    MoFreeMediaType(&mtOut);
    SafeRelease(&pPrivData);
    return hr;
}
```



<span data-ttu-id="3c6d7-141">La funzione CopyPropertyStore è una funzione helper che copia le proprietà da un archivio di proprietà a un altro:</span><span class="sxs-lookup"><span data-stu-id="3c6d7-141">The CopyPropertyStore function is a helper function that copies properties from one property store to another:</span></span>


```C++
//
// CopyPropertyStore
// Helper function to copy properties from one property
// store to another property store.
//

HRESULT CopyPropertyStore(IPropertyStore *pSrc, IPropertyStore *pDest)
{
    HRESULT hr = S_OK;
    DWORD cProps = 0;

    PROPERTYKEY key;
    PROPVARIANT var;

    PropVariantInit(&var);

    hr = pSrc->GetCount(&cProps);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cProps; i++)
        {
            hr = pSrc->GetAt(i, &key);

            if (FAILED(hr)) { break; }

            hr = pSrc->GetValue(key, &var);

            if (FAILED(hr)) { break; }

            hr = pDest->SetValue(key, var);

            if (FAILED(hr)) { break; }

            PropVariantClear(&var);
        }
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3c6d7-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c6d7-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c6d7-143">Creazione di un'istanza di un codificatore MFT</span><span class="sxs-lookup"><span data-stu-id="3c6d7-143">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="3c6d7-144">Codificatori Windows Media</span><span class="sxs-lookup"><span data-stu-id="3c6d7-144">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 
