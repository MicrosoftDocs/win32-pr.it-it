---
description: Configurazione di un codificatore WMV
ms.assetid: 6e690d17-da17-452a-aa9a-9701a560856b
title: Configurazione di un codificatore WMV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39001edd5901d09bc618fe92d251070d24633fb94812a9c2696b11866f3cb9cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880545"
---
# <a name="configuring-a-wmv-encoder"></a>Configurazione di un codificatore WMV

Per creare un tipo di output valido per un codificatore Windows Media Video (WMV), è necessario disporre delle informazioni seguenti:

-   Formato del video non compresso che verrà codificato.
-   Sottotipo video che rappresenta il formato WMV codificato. Vedere [VIDEO Subtype GUID (GUID sottotipo video).](video-subtype-guids.md)
-   Velocità in bit di destinazione per il flusso codificato.
-   Proprietà di configurazione da impostare nel codificatore.

Le proprietà di configurazione sono documentate nella documentazione Windows codec audio e video multimediali e api DSP. Per altre informazioni, vedere "Proprietà del flusso video" in Proprietà [di codifica.](configuring-the-encoder.md)

Per ottenere un tipo di output valido per il codificatore, seguire questa procedura.

1.  Usare la [**funzione MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) per creare un'istanza del codificatore.
2.  Eseguire una query sul codificatore per **l'interfaccia IPropertyStore.**
3.  Usare **l'interfaccia IPropertyStore** per configurare il codificatore.
4.  Chiamare [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) per impostare il tipo di video non compresso nel codificatore.
5.  Chiamare [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere l'elenco dei formati di compressione dal codificatore. I codificatori WMV non restituiscono un tipo di supporto completo da questo metodo. Nei tipi di supporti mancano due tipi di informazioni:

    -   Velocità in bit di destinazione.
    -   Dati del codec privato del codificatore.

    Prima di impostare il tipo di output nel codificatore, è necessario aggiungere entrambi questi elementi al tipo di supporto.

6.  Per specificare la velocità in bit di destinazione, impostare [**l'attributo MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) sul tipo di supporto.
7.  Aggiungere i dati del codec privato al tipo di supporto, come illustrato nella sezione successiva.
8.  Chiamare [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il tipo di supporto di compressione nel codificatore.

### <a name="private-codec-data"></a>Dati codec privati

I dati del codec privato sono una struttura di dati opachi che è necessario ottenere dal codificatore WMV e aggiungere al tipo di compressione prima di impostare il tipo di compressione nel codificatore. Per ottenere i dati privati, è necessario usare l'interfaccia **IWMCodecPrivateData,** documentata in Windows Media Format 11 SDK.

Per ottenere i dati del codec privato, seguire questa procedura:

1.  Chiamare [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere un tipo di supporto dal codificatore. Questo è il passaggio 6 della sezione precedente.
2.  Specificare la velocità in bit di destinazione impostando [**l'attributo MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) nel tipo di supporto.
3.  Convertire il tipo di supporto in [**una DMO \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) chiamando la [**funzione MFInitAMMediaTypeFromMFMediaType.**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)
4.  Eseguire una query sul codificatore **per l'interfaccia IWMCodecPrivateData.**
5.  Chiamare il **metodo IWMCodecPrivateData::SetPartialOutputType,** passando la struttura DMO [**MEDIA \_ \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) convertita.
6.  Chiamare due volte il metodo **IWMCodecPrivateData::GetPrivateData,** una volta per ottenere le dimensioni del buffer per i dati privati e una volta per copiare i dati nel buffer.
7.  Aggiungere i dati privati al tipo di supporto impostando [**l'attributo \_ MF MT \_ USER \_ DATA**](mf-mt-user-data-attribute.md) sul tipo.

L'esempio esteso seguente illustra come creare un formato di compressione WMV da un tipo di video non compresso:


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



La funzione CreateVideoEncoder crea un codificatore video per un sottotipo video specificato, ad esempio **MFVideoFormat \_ WMV3:**


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



La funzione AddPrivateData aggiunge i dati privati del codec al tipo di compressione:


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



La funzione CopyPropertyStore è una funzione helper che copia le proprietà da un archivio di proprietà a un altro:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'istanza di un codificatore MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificatori multimediali](windows-media-encoders.md)
</dt> </dl>

 

 
