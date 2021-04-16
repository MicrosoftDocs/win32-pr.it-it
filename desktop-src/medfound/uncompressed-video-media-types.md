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
# <a name="uncompressed-video-media-types"></a><span data-ttu-id="a9810-103">Tipi di supporti video non compressi</span><span class="sxs-lookup"><span data-stu-id="a9810-103">Uncompressed Video Media Types</span></span>

<span data-ttu-id="a9810-104">In questo argomento viene descritto come creare un tipo di supporto che descrive un formato video non compresso.</span><span class="sxs-lookup"><span data-stu-id="a9810-104">This topic describes how to create a media type that describes an uncompressed video format.</span></span> <span data-ttu-id="a9810-105">Per ulteriori informazioni sui tipi di supporto in genere, vedere [informazioni sui tipi di supporto](about-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="a9810-105">For more information about media types generally, see [About Media Types](about-media-types.md).</span></span>

<span data-ttu-id="a9810-106">Per creare un tipo di video completo non compresso, impostare gli attributi seguenti sul puntatore all'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="a9810-106">To create a complete uncompressed video type, set the following attributes on the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span>



| <span data-ttu-id="a9810-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="a9810-107">Attribute</span></span>                                                                            | <span data-ttu-id="a9810-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9810-108">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9810-109">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="a9810-109">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                            | <span data-ttu-id="a9810-110">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="a9810-110">Major type.</span></span> <span data-ttu-id="a9810-111">Impostare su **MFMediaType \_ video**.</span><span class="sxs-lookup"><span data-stu-id="a9810-111">Set to **MFMediaType\_Video**.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="a9810-112">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="a9810-112">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                   | <span data-ttu-id="a9810-113">Sottotipo.</span><span class="sxs-lookup"><span data-stu-id="a9810-113">Subtype.</span></span> <span data-ttu-id="a9810-114">Vedere [GUID del sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="a9810-114">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="a9810-115">**\_ \_ stride predefinito MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="a9810-115">**MF\_MT\_DEFAULT\_STRIDE**</span></span>](mf-mt-default-stride-attribute.md)                    | <span data-ttu-id="a9810-116">Stride della superficie.</span><span class="sxs-lookup"><span data-stu-id="a9810-116">Surface stride.</span></span> <span data-ttu-id="a9810-117">Lo *stride* è il numero di byte necessari per passare da una riga di pixel a quella successiva.</span><span class="sxs-lookup"><span data-stu-id="a9810-117">The *stride* is the number of bytes needed to go from one row of pixels to the next.</span></span> <span data-ttu-id="a9810-118">Impostare questo attributo se lo stride in byte non corrisponde alla larghezza del video in byte.</span><span class="sxs-lookup"><span data-stu-id="a9810-118">Set this attribute if the stride in bytes is not the same as the video width in bytes.</span></span> <span data-ttu-id="a9810-119">In caso contrario, è possibile omettere questo attributo.</span><span class="sxs-lookup"><span data-stu-id="a9810-119">Otherwise, you can omit this attribute.</span></span> |
| [<span data-ttu-id="a9810-120">**\_ \_ frequenza fotogrammi MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="a9810-120">**MF\_MT\_FRAME\_RATE**</span></span>](mf-mt-frame-rate-attribute.md)                            | <span data-ttu-id="a9810-121">Frequenza di fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="a9810-121">Frame rate.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="a9810-122">**\_dimensioni del \_ frame MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="a9810-122">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)                            | <span data-ttu-id="a9810-123">Dimensioni del frame.</span><span class="sxs-lookup"><span data-stu-id="a9810-123">Frame size.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="a9810-124">**\_modalità di \_ intreccio MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="a9810-124">**MF\_MT\_INTERLACE\_MODE**</span></span>](mf-mt-interlace-mode-attribute.md)                    | <span data-ttu-id="a9810-125">Modalità interlacciamento.</span><span class="sxs-lookup"><span data-stu-id="a9810-125">Interlacing mode.</span></span>                                                                                                                                                                                                                   |
| [<span data-ttu-id="a9810-126">**\_ \_ tutti gli esempi MF mt \_ \_ Independent**</span><span class="sxs-lookup"><span data-stu-id="a9810-126">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) | <span data-ttu-id="a9810-127">Specifica se ogni esempio è indipendente.</span><span class="sxs-lookup"><span data-stu-id="a9810-127">Specifies whether each sample is independent.</span></span> <span data-ttu-id="a9810-128">Impostare su **true** per i formati non compressi.</span><span class="sxs-lookup"><span data-stu-id="a9810-128">Set to **TRUE** for uncompressed formats.</span></span>                                                                                                                                             |
| [<span data-ttu-id="a9810-129">**proporzioni MF \_ mt \_ pixel \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9810-129">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)           | <span data-ttu-id="a9810-130">Proporzioni pixel.</span><span class="sxs-lookup"><span data-stu-id="a9810-130">Pixel aspect ratio.</span></span>                                                                                                                                                                                                                 |



 

<span data-ttu-id="a9810-131">Inoltre, se si conoscono i valori corretti, impostare gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="a9810-131">In addition, set the following attributes if you know the correct values.</span></span> <span data-ttu-id="a9810-132">(In caso contrario, omettere questi attributi).</span><span class="sxs-lookup"><span data-stu-id="a9810-132">(Otherwise, omit these attributes.)</span></span>



| <span data-ttu-id="a9810-133">Attributo</span><span class="sxs-lookup"><span data-stu-id="a9810-133">Attribute</span></span>                                                                    | <span data-ttu-id="a9810-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9810-134">Description</span></span>        |
|------------------------------------------------------------------------------|--------------------|
| [<span data-ttu-id="a9810-135">**\_ \_ principali video MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="a9810-135">**MF\_MT\_VIDEO\_PRIMARIES**</span></span>](mf-mt-video-primaries-attribute.md)          | <span data-ttu-id="a9810-136">Colori primari.</span><span class="sxs-lookup"><span data-stu-id="a9810-136">Color primaries.</span></span>   |
| [<span data-ttu-id="a9810-137">**\_funzione di \_ trasferimento MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="a9810-137">**MF\_MT\_TRANSFER\_FUNCTION**</span></span>](mf-mt-transfer-function-attribute.md)      | <span data-ttu-id="a9810-138">Funzione transfer.</span><span class="sxs-lookup"><span data-stu-id="a9810-138">Transfer function.</span></span> |
| [<span data-ttu-id="a9810-139">**\_ \_ matrice YUV MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="a9810-139">**MF\_MT\_YUV\_MATRIX**</span></span>](mf-mt-yuv-matrix-attribute.md)                    | <span data-ttu-id="a9810-140">Matrice di traslazione.</span><span class="sxs-lookup"><span data-stu-id="a9810-140">Transfer matrix.</span></span>   |
| [<span data-ttu-id="a9810-141">**posizione \_ di \_ Chroma del video MF mt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9810-141">**MF\_MT\_VIDEO\_CHROMA\_SITING**</span></span>](mf-mt-video-chroma-siting-attribute.md) | <span data-ttu-id="a9810-142">Ubicazione Chroma.</span><span class="sxs-lookup"><span data-stu-id="a9810-142">Chroma siting.</span></span>     |
| [<span data-ttu-id="a9810-143">**\_ \_ \_ intervallo nominale video MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="a9810-143">**MF\_MT\_VIDEO\_NOMINAL\_RANGE**</span></span>](mf-mt-video-nominal-range-attribute.md) | <span data-ttu-id="a9810-144">Intervallo nominale.</span><span class="sxs-lookup"><span data-stu-id="a9810-144">Nominal range.</span></span>     |



 

<span data-ttu-id="a9810-145">Per ulteriori informazioni, vedere [informazioni sui colori estese](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="a9810-145">For more information, see [Extended Color Information](extended-color-information.md).</span></span> <span data-ttu-id="a9810-146">Ad esempio, se si crea un tipo di supporto che descrive uno standard video e lo standard definisce la posizione Chroma, aggiungere queste informazioni al tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="a9810-146">For example, if you create a media type that describes a video standard, and the standard defines the chroma siting, add this information to the media type.</span></span> <span data-ttu-id="a9810-147">Questa operazione consente di mantenere la fedeltà dei colori in tutta la pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9810-147">Doing so helps to preserve color fidelity throughout the pipeline.</span></span>

<span data-ttu-id="a9810-148">Le funzioni seguenti possono risultare utili durante la creazione di un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="a9810-148">The following functions might be useful when creating a video media type.</span></span>



| <span data-ttu-id="a9810-149">Funzione</span><span class="sxs-lookup"><span data-stu-id="a9810-149">Function</span></span>                                                                     | <span data-ttu-id="a9810-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9810-150">Description</span></span>                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9810-151">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="a9810-151">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | <span data-ttu-id="a9810-152">Calcola la frequenza dei fotogrammi, in base alla durata media del frame.</span><span class="sxs-lookup"><span data-stu-id="a9810-152">Calculates the frame rate, given the average frame duration.</span></span>                                                                                                                         |
| [<span data-ttu-id="a9810-153">**MFCalculateImageSize**</span><span class="sxs-lookup"><span data-stu-id="a9810-153">**MFCalculateImageSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | <span data-ttu-id="a9810-154">Calcola la dimensione dell'immagine per un formato video non compresso.</span><span class="sxs-lookup"><span data-stu-id="a9810-154">Calculates the image size for an uncompressed video format.</span></span>                                                                                                                          |
| [<span data-ttu-id="a9810-155">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="a9810-155">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | <span data-ttu-id="a9810-156">Calcola la durata media di un frame video, in base alla frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="a9810-156">Calculates the average duration of a video frame, given the frame rate.</span></span>                                                                                                              |
| [<span data-ttu-id="a9810-157">**MFGetStrideForBitmapInfoHeader**</span><span class="sxs-lookup"><span data-stu-id="a9810-157">**MFGetStrideForBitmapInfoHeader**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | <span data-ttu-id="a9810-158">Restituisce lo stride di superficie minimo per un formato video.</span><span class="sxs-lookup"><span data-stu-id="a9810-158">Returns the minimum surface stride for a video format.</span></span> <span data-ttu-id="a9810-159">Per ulteriori informazioni, vedere [Image stride](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="a9810-159">For more information, see [Image Stride](image-stride.md).</span></span>                                                                   |
| [<span data-ttu-id="a9810-160">**MFInitVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="a9810-160">**MFInitVideoFormat**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | <span data-ttu-id="a9810-161">Inizializza una struttura [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) per alcuni formati video standard, ad esempio NTSC Television.</span><span class="sxs-lookup"><span data-stu-id="a9810-161">Initializes an [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) structure for some standard video formats, such as NTSC television.</span></span> <span data-ttu-id="a9810-162">È quindi possibile usare la struttura per inizializzare un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="a9810-162">You can then use the structure to initialize a media type.</span></span> |
| [<span data-ttu-id="a9810-163">**MFIsFormatYUV**</span><span class="sxs-lookup"><span data-stu-id="a9810-163">**MFIsFormatYUV**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | <span data-ttu-id="a9810-164">Esegue una query se un formato video è un formato YUV.</span><span class="sxs-lookup"><span data-stu-id="a9810-164">Queries whether a video format is a YUV format.</span></span>                                                                                                                                      |



 

## <a name="examples"></a><span data-ttu-id="a9810-165">Esempio</span><span class="sxs-lookup"><span data-stu-id="a9810-165">Examples</span></span>

<span data-ttu-id="a9810-166">In questo esempio viene illustrata una funzione che compila le informazioni più comuni per un formato video non compresso.</span><span class="sxs-lookup"><span data-stu-id="a9810-166">This example shows a function that fills in the most common information for an uncompressed video format.</span></span> <span data-ttu-id="a9810-167">La funzione restituisce un puntatore di interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="a9810-167">The function returns an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span> <span data-ttu-id="a9810-168">È quindi possibile aggiungere altri attributi al tipo di supporto in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="a9810-168">You can then add additional attributes to the media type as needed.</span></span>


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



<span data-ttu-id="a9810-169">Nell'esempio successivo viene preso come input un formato video codificato e viene creato un tipo di video non compresso corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a9810-169">The next example takes an encoded video format as input, and creates a matching uncompressed video type.</span></span> <span data-ttu-id="a9810-170">Questo tipo può essere impostato su un codificatore o un decodificatore, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="a9810-170">This type would be suitable to set on an encoder or decoder, for example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a9810-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9810-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9810-172">Informazioni sui colori estesi</span><span class="sxs-lookup"><span data-stu-id="a9810-172">Extended Color Information</span></span>](extended-color-information.md)
</dt> <dt>

[<span data-ttu-id="a9810-173">Stride immagine</span><span class="sxs-lookup"><span data-stu-id="a9810-173">Image Stride</span></span>](image-stride.md)
</dt> <dt>

[<span data-ttu-id="a9810-174">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="a9810-174">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="a9810-175">Tipi di supporti video</span><span class="sxs-lookup"><span data-stu-id="a9810-175">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="a9810-176">GUID del sottotipo video</span><span class="sxs-lookup"><span data-stu-id="a9810-176">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 



