---
description: Tipi di supporti video non compressi
ms.assetid: 50bf2947-27ee-4092-9d3a-a1c13ee80e95
title: Tipi di supporti video non compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c90a48aed62f22a492ac22dae93761c1046750a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530487"
---
# <a name="uncompressed-video-media-types"></a>Tipi di supporti video non compressi

In questo argomento viene descritto come creare un tipo di supporto che descrive un formato video non compresso. Per ulteriori informazioni sui tipi di supporto in genere, vedere [informazioni sui tipi di supporto](about-media-types.md).

Per creare un tipo di video completo non compresso, impostare gli attributi seguenti sul puntatore all'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .



| Attributo                                                                            | Descrizione                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md)                            | Tipo principale. Impostare su **MFMediaType \_ video**.                                                                                                                                                                                          |
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)                                   | Sottotipo. Vedere [GUID del sottotipo video](video-subtype-guids.md).                                                                                                                                                                        |
| [**\_ \_ stride predefinito MF \_ mt**](mf-mt-default-stride-attribute.md)                    | Stride della superficie. Lo *stride* è il numero di byte necessari per passare da una riga di pixel a quella successiva. Impostare questo attributo se lo stride in byte non corrisponde alla larghezza del video in byte. In caso contrario, è possibile omettere questo attributo. |
| [**\_ \_ frequenza fotogrammi MF mt \_**](mf-mt-frame-rate-attribute.md)                            | Frequenza di fotogrammi.                                                                                                                                                                                                                         |
| [**\_dimensioni del \_ frame MF mt \_**](mf-mt-frame-size-attribute.md)                            | Dimensioni del frame.                                                                                                                                                                                                                         |
| [**\_modalità di \_ intreccio MF mt \_**](mf-mt-interlace-mode-attribute.md)                    | Modalità interlacciamento.                                                                                                                                                                                                                   |
| [**\_ \_ tutti gli esempi MF mt \_ \_ Independent**](mf-mt-all-samples-independent-attribute.md) | Specifica se ogni esempio è indipendente. Impostare su **true** per i formati non compressi.                                                                                                                                             |
| [**proporzioni MF \_ mt \_ pixel \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)           | Proporzioni pixel.                                                                                                                                                                                                                 |



 

Inoltre, se si conoscono i valori corretti, impostare gli attributi seguenti. (In caso contrario, omettere questi attributi).



| Attributo                                                                    | Descrizione        |
|------------------------------------------------------------------------------|--------------------|
| [**\_ \_ principali video MF \_ mt**](mf-mt-video-primaries-attribute.md)          | Colori primari.   |
| [**\_funzione di \_ trasferimento MF mt \_**](mf-mt-transfer-function-attribute.md)      | Funzione transfer. |
| [**\_ \_ matrice YUV MF \_ mt**](mf-mt-yuv-matrix-attribute.md)                    | Matrice di traslazione.   |
| [**posizione \_ di \_ Chroma del video MF mt \_ \_**](mf-mt-video-chroma-siting-attribute.md) | Ubicazione Chroma.     |
| [**\_ \_ \_ intervallo nominale video MF \_ mt**](mf-mt-video-nominal-range-attribute.md) | Intervallo nominale.     |



 

Per ulteriori informazioni, vedere [informazioni sui colori estese](extended-color-information.md). Ad esempio, se si crea un tipo di supporto che descrive uno standard video e lo standard definisce la posizione Chroma, aggiungere queste informazioni al tipo di supporto. Questa operazione consente di mantenere la fedeltà dei colori in tutta la pipeline.

Le funzioni seguenti possono risultare utili durante la creazione di un tipo di supporto video.



| Funzione                                                                     | Descrizione                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | Calcola la frequenza dei fotogrammi, in base alla durata media del frame.                                                                                                                         |
| [**MFCalculateImageSize**](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | Calcola la dimensione dell'immagine per un formato video non compresso.                                                                                                                          |
| [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | Calcola la durata media di un frame video, in base alla frequenza dei fotogrammi.                                                                                                              |
| [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | Restituisce lo stride di superficie minimo per un formato video. Per ulteriori informazioni, vedere [Image stride](image-stride.md).                                                                   |
| [**MFInitVideoFormat**](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | Inizializza una struttura [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) per alcuni formati video standard, ad esempio NTSC Television. È quindi possibile usare la struttura per inizializzare un tipo di supporto. |
| [**MFIsFormatYUV**](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | Esegue una query se un formato video è un formato YUV.                                                                                                                                      |



 

## <a name="examples"></a>Esempio

In questo esempio viene illustrata una funzione che compila le informazioni più comuni per un formato video non compresso. La funzione restituisce un puntatore di interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . È quindi possibile aggiungere altri attributi al tipo di supporto in base alle esigenze.


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



Nell'esempio successivo viene preso come input un formato video codificato e viene creato un tipo di video non compresso corrispondente. Questo tipo può essere impostato su un codificatore o un decodificatore, ad esempio.


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

[Informazioni sui colori estesi](extended-color-information.md)
</dt> <dt>

[Stride immagine](image-stride.md)
</dt> <dt>

[Tipi di supporto](media-types.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> <dt>

[GUID del sottotipo video](video-subtype-guids.md)
</dt> </dl>

 

 



