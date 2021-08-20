---
description: Tipi di supporti video non compressi
ms.assetid: 50bf2947-27ee-4092-9d3a-a1c13ee80e95
title: Tipi di supporti video non compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d01dab1179e0fc77872a7122e915e67c4c70dc98afd9586f02569c53e61547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057588"
---
# <a name="uncompressed-video-media-types"></a>Tipi di supporti video non compressi

In questo argomento viene descritto come creare un tipo di supporto che descrive un formato video non compresso. Per altre informazioni sui tipi di supporti in genere, vedere [About Media Types](about-media-types.md).

Per creare un tipo di video non compresso completo, impostare gli attributi seguenti sul puntatore [**all'interfaccia IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)



| Attributo                                                                            | Descrizione                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md)                            | Tipo principale. Impostare su **MFMediaType \_ Video.**                                                                                                                                                                                          |
| [**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)                                   | Sottotipo. Vedere [VIDEO Subtype GUID (GUID sottotipo video).](video-subtype-guids.md)                                                                                                                                                                        |
| [**MF \_ MT \_ DEFAULT \_ STRIDE**](mf-mt-default-stride-attribute.md)                    | Stride della superficie. Lo *stride* è il numero di byte necessari per passare da una riga di pixel a quella successiva. Impostare questo attributo se lo stride in byte non corrisponde alla larghezza del video in byte. In caso contrario, è possibile omettere questo attributo. |
| [**FREQUENZA \_ DEI \_ FOTOGRAMMI MF MT \_**](mf-mt-frame-rate-attribute.md)                            | Frequenza dei fotogrammi.                                                                                                                                                                                                                         |
| [**DIMENSIONI DEL \_ FRAME MF \_ \_ MT**](mf-mt-frame-size-attribute.md)                            | Dimensioni del frame.                                                                                                                                                                                                                         |
| [**MODALITÀ \_ INTERLACE MF MT \_ \_**](mf-mt-interlace-mode-attribute.md)                    | Modalità di interlacciamento.                                                                                                                                                                                                                   |
| [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) | Specifica se ogni campione è indipendente. Impostare su **TRUE per** i formati non compressi.                                                                                                                                             |
| [**PROPORZIONI \_ IN PIXEL MF MT \_ \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)           | Proporzioni pixel.                                                                                                                                                                                                                 |



 

Inoltre, impostare gli attributi seguenti se si conoscono i valori corretti. In caso contrario, omettere questi attributi.



| Attributo                                                                    | Descrizione        |
|------------------------------------------------------------------------------|--------------------|
| [**PRIMARIE \_ VIDEO MF MT \_ \_**](mf-mt-video-primaries-attribute.md)          | Primarie di colore.   |
| [**FUNZIONE MF \_ MT \_ TRANSFER \_**](mf-mt-transfer-function-attribute.md)      | Funzione transfer. |
| [**MF \_ MT \_ YUV \_ MATRIX**](mf-mt-yuv-matrix-attribute.md)                    | Matrice di trasferimento.   |
| [**MF \_ MT \_ VIDEO \_ CHROMA \_ SITING**](mf-mt-video-chroma-siting-attribute.md) | Siting di chroma.     |
| [**MF \_ MT \_ VIDEO \_ NOMINAL \_ RANGE**](mf-mt-video-nominal-range-attribute.md) | Intervallo nominale.     |



 

Per altre informazioni, vedere [Extended Color Information](extended-color-information.md). Ad esempio, se si crea un tipo di supporto che descrive uno standard video e lo standard definisce il siting di chroma, aggiungere queste informazioni al tipo di supporto. In questo modo è possibile mantenere la fedeltà dei colori in tutta la pipeline.

Le funzioni seguenti possono essere utili quando si crea un tipo di supporto video.



| Funzione                                                                     | Descrizione                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | Calcola la frequenza dei fotogrammi, in base alla durata media dei fotogrammi.                                                                                                                         |
| [**MFCalculateImageSize**](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | Calcola le dimensioni dell'immagine per un formato video non compresso.                                                                                                                          |
| [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | Calcola la durata media di un fotogramma video, in base alla frequenza dei fotogrammi.                                                                                                              |
| [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | Restituisce lo stride minimo della superficie per un formato video. Per altre informazioni, vedere [Stride immagine.](image-stride.md)                                                                   |
| [**MFInitVideoFormat**](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | Inizializza una [**struttura MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) per alcuni formati video standard, ad esempio tv NTSC. È quindi possibile usare la struttura per inizializzare un tipo di supporto. |
| [**MFIsFormatYUV**](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | Esegue una query per determinare se un formato video è un formato YUV.                                                                                                                                      |



 

## <a name="examples"></a>Esempio

Questo esempio mostra una funzione che inserisce le informazioni più comuni per un formato video non compresso. La funzione restituisce un [**puntatore a interfaccia IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) È quindi possibile aggiungere altri attributi al tipo di supporto in base alle esigenze.


```C++
HRESULT CreateUncompressedVideoType(
    DWORD                fccFormat,  // FOURCC or D3DFORMAT value.     
    UINT32               width, 
    UINT32               height,
    MFVideoInterlaceMode interlaceMode,
    const MFRatio&       frameRate,
    const MFRatio&       par,
    IMFMediaType         **ppType
    )
{
    if (ppType == NULL)
    {
        return E_POINTER;
    }

    GUID    subtype = MFVideoFormat_Base;
    LONG    lStride = 0;
    UINT    cbImage = 0;

    IMFMediaType *pType = NULL;

    // Set the subtype GUID from the FOURCC or D3DFORMAT value.
    subtype.Data1 = fccFormat;

    HRESULT hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_INTERLACE_MODE, interlaceMode);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the default stride value.
    hr = pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the image size in bytes.
    hr = MFCalculateImageSize(subtype, width, height, &cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_SAMPLE_SIZE, cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_FIXED_SIZE_SAMPLES, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Frame rate
    hr = MFSetAttributeRatio(pType, MF_MT_FRAME_RATE, frameRate.Numerator, 
        frameRate.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Pixel aspect ratio
    hr = MFSetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, par.Numerator, 
        par.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppType = pType;
    (*ppType)->AddRef();

done:
    SafeRelease(&pType);
    return hr;
}
```



L'esempio seguente accetta un formato video codificato come input e crea un tipo di video non compresso corrispondente. Questo tipo, ad esempio, può essere impostato su un codificatore o decodificatore.


```C++
HRESULT ConvertVideoTypeToUncompressedType(
    IMFMediaType *pType,    // Pointer to an encoded video type.
    const GUID& subtype,    // Uncompressed subtype (eg, RGB-32, AYUV)
    IMFMediaType **ppType   // Receives a matching uncompressed video type.
    )
{
    IMFMediaType *pTypeUncomp = NULL;

    HRESULT hr = S_OK;
    GUID majortype = { 0 };
    MFRatio par = { 0 };

    hr = pType->GetMajorType(&majortype);

    if (majortype != MFMediaType_Video)
    {
        return MF_E_INVALIDMEDIATYPE;
    }

    // Create a new media type and copy over all of the items.
    // This ensures that extended color information is retained.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pTypeUncomp);
    }

    if (SUCCEEDED(hr))
    {
        hr = pType->CopyAllItems(pTypeUncomp);
    }

    // Set the subtype.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetGUID(MF_MT_SUBTYPE, subtype);
    }

    // Uncompressed means all samples are independent.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    }

    // Fix up PAR if not set on the original type.
    if (SUCCEEDED(hr))
    {
        hr = MFGetAttributeRatio(
            pTypeUncomp, 
            MF_MT_PIXEL_ASPECT_RATIO, 
            (UINT32*)&par.Numerator, 
            (UINT32*)&par.Denominator
            );

        // Default to square pixels.
        if (FAILED(hr))
        {
            hr = MFSetAttributeRatio(
                pTypeUncomp, 
                MF_MT_PIXEL_ASPECT_RATIO, 
                1, 1
                );
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppType = pTypeUncomp;
        (*ppType)->AddRef();
    }

    SafeRelease(&pTypeUncomp);
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni estese sui colori](extended-color-information.md)
</dt> <dt>

[Stride dell'immagine](image-stride.md)
</dt> <dt>

[Tipi di supporti](media-types.md)
</dt> <dt>

[Tipi di file multimediali video](video-media-types.md)
</dt> <dt>

[GUID sottotipo video](video-subtype-guids.md)
</dt> </dl>

 

 



