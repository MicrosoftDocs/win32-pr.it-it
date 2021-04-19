---
description: Tipi di supporti audio non compressi
ms.assetid: 130a18a9-1c86-4d16-a8ae-ed57bf50f9bb
title: Tipi di supporti audio non compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d15f7211ef16d4280476f93744650b88742073
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320576"
---
# <a name="uncompressed-audio-media-types"></a><span data-ttu-id="dd08f-103">Tipi di supporti audio non compressi</span><span class="sxs-lookup"><span data-stu-id="dd08f-103">Uncompressed Audio Media Types</span></span>

<span data-ttu-id="dd08f-104">Per creare un tipo audio non compresso completo, impostare almeno gli attributi seguenti sul puntatore all'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="dd08f-104">To create a complete uncompressed audio type, set at least the following attributes on the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span>



| <span data-ttu-id="dd08f-105">Attributo</span><span class="sxs-lookup"><span data-stu-id="dd08f-105">Attribute</span></span>                                                                                    | <span data-ttu-id="dd08f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd08f-106">Description</span></span>                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd08f-107">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="dd08f-107">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="dd08f-108">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="dd08f-108">Major type.</span></span> <span data-ttu-id="dd08f-109">Impostare su \_ audio MFMediaType.</span><span class="sxs-lookup"><span data-stu-id="dd08f-109">Set to MFMediaType\_Audio.</span></span>                                                                                       |
| [<span data-ttu-id="dd08f-110">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="dd08f-110">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="dd08f-111">Sottotipo.</span><span class="sxs-lookup"><span data-stu-id="dd08f-111">Subtype.</span></span> <span data-ttu-id="dd08f-112">Vedere [GUID del sottotipo audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="dd08f-112">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>                                                                 |
| [<span data-ttu-id="dd08f-113">**numero \_ di \_ \_ canali audio MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="dd08f-113">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="dd08f-114">Numero dei canali audio.</span><span class="sxs-lookup"><span data-stu-id="dd08f-114">Number of audio channels.</span></span>                                                                                                    |
| [<span data-ttu-id="dd08f-115">**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="dd08f-115">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="dd08f-116">Numero di campioni audio al secondo.</span><span class="sxs-lookup"><span data-stu-id="dd08f-116">Number of audio samples per second.</span></span>                                                                                          |
| [<span data-ttu-id="dd08f-117">**\_ \_ \_ allineamento blocchi audio MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="dd08f-117">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="dd08f-118">Allineamento del blocco.</span><span class="sxs-lookup"><span data-stu-id="dd08f-118">Block alignment.</span></span>                                                                                                             |
| [<span data-ttu-id="dd08f-119">**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="dd08f-119">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="dd08f-120">Numero medio di byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="dd08f-120">Average number of bytes per second.</span></span>                                                                                          |
| [<span data-ttu-id="dd08f-121">**\_ \_ bit audio MF \_ mt \_ per \_ campione**</span><span class="sxs-lookup"><span data-stu-id="dd08f-121">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="dd08f-122">Numero di bit per esempio audio.</span><span class="sxs-lookup"><span data-stu-id="dd08f-122">Number of bits per audio sample.</span></span>                                                                                             |
| [<span data-ttu-id="dd08f-123">**\_ \_ tutti gli esempi MF mt \_ \_ Independent**</span><span class="sxs-lookup"><span data-stu-id="dd08f-123">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)         | <span data-ttu-id="dd08f-124">Specifica se ogni esempio audio è indipendente.</span><span class="sxs-lookup"><span data-stu-id="dd08f-124">Specifies whether each audio sample is independent.</span></span> <span data-ttu-id="dd08f-125">Impostare su **true** per i \_ formati MFAudioFormat PCM e MFAudioFormat \_ float.</span><span class="sxs-lookup"><span data-stu-id="dd08f-125">Set to **TRUE** for MFAudioFormat\_PCM and MFAudioFormat\_Float formats.</span></span> |



 

<span data-ttu-id="dd08f-126">Inoltre, per alcuni formati audio sono necessari gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="dd08f-126">In addition, the following attributes are required for some audio formats.</span></span>



| <span data-ttu-id="dd08f-127">Attributo</span><span class="sxs-lookup"><span data-stu-id="dd08f-127">Attribute</span></span>                                                                                      | <span data-ttu-id="dd08f-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd08f-128">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd08f-129">**\_ \_ bit validi per l'audio MF mt \_ \_ \_ per \_ campione**</span><span class="sxs-lookup"><span data-stu-id="dd08f-129">**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-valid-bits-per-sample-attribute.md) | <span data-ttu-id="dd08f-130">Numero di bit validi di dati audio in ogni esempio audio.</span><span class="sxs-lookup"><span data-stu-id="dd08f-130">Number of valid bits of audio data in each audio sample.</span></span> <span data-ttu-id="dd08f-131">Impostare questo attributo se gli esempi audio contengono spaziatura interna, ovvero se il numero di bit validi in ogni campione audio è inferiore alle dimensioni del campione.</span><span class="sxs-lookup"><span data-stu-id="dd08f-131">Set this attribute if the audio samples have padding—that is, if the number of valid bits in each audio sample is less than the sample size.</span></span> |
| [<span data-ttu-id="dd08f-132">**\_ \_ \_ maschera canale audio MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="dd08f-132">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                     | <span data-ttu-id="dd08f-133">Assegnazione dei canali audio alle posizioni degli altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="dd08f-133">The assignment of audio channels to speaker positions.</span></span> <span data-ttu-id="dd08f-134">Impostare questo attributo per i flussi audio multicanale, ad esempio 5,1.</span><span class="sxs-lookup"><span data-stu-id="dd08f-134">Set this attribute for multichannel audio streams, such as 5.1.</span></span> <span data-ttu-id="dd08f-135">Questo attributo non è necessario per l'audio mono o stereo.</span><span class="sxs-lookup"><span data-stu-id="dd08f-135">This attribute is not required for mono or stereo audio.</span></span>                       |



 

### <a name="example-code"></a><span data-ttu-id="dd08f-136">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="dd08f-136">Example Code</span></span>

<span data-ttu-id="dd08f-137">Il codice seguente illustra come creare un tipo di supporto per l'audio PCM non compresso.</span><span class="sxs-lookup"><span data-stu-id="dd08f-137">The following code shows how to create a media type for uncompressed PCM audio.</span></span>


```C++
HRESULT CreatePCMAudioType(
    UINT32 sampleRate,        // Samples per second
    UINT32 bitsPerSample,     // Bits per sample
    UINT32 cChannels,         // Number of channels
    IMFMediaType **ppType     // Receives a pointer to the media type.
    )
{
    HRESULT hr = S_OK;

    IMFMediaType *pType = NULL;

    // Calculate derived values.
    UINT32 blockAlign = cChannels * (bitsPerSample / 8);
    UINT32 bytesPerSecond = blockAlign * sampleRate;

    // Create the empty media type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set attributes on the type.
    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Audio);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_PCM);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_NUM_CHANNELS, cChannels);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_SAMPLES_PER_SECOND, sampleRate);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, blockAlign);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_AVG_BYTES_PER_SECOND, bytesPerSecond);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_BITS_PER_SAMPLE, bitsPerSample);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the type to the caller.
    *ppType = pType;
    (*ppType)->AddRef();

done:
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="dd08f-138">Nell'esempio successivo viene preso come input un formato audio codificato e viene creato un tipo di audio PCM corrispondente.</span><span class="sxs-lookup"><span data-stu-id="dd08f-138">The next example takes an encoded audio format as input, and creates a matching PCM audio type.</span></span> <span data-ttu-id="dd08f-139">Questo tipo può essere impostato su un codificatore o un decodificatore, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="dd08f-139">This type would be suitable to set on an encoder or decoder, for example.</span></span>


```C++
//-------------------------------------------------------------------
// ConvertAudioTypeToPCM
//
// Given an audio media type (which might describe a compressed audio
// format), returns a media type that describes the equivalent
// uncompressed PCM format.
//-------------------------------------------------------------------

HRESULT ConvertAudioTypeToPCM(
    IMFMediaType *pType,        // Pointer to an encoded audio type.
    IMFMediaType **ppType       // Receives a matching PCM audio type.
    )
{
    HRESULT hr = S_OK;

    GUID majortype = { 0 };
    GUID subtype = { 0 };

    UINT32 cChannels = 0;
    UINT32 samplesPerSec = 0;
    UINT32 bitsPerSample = 0;

    hr = pType->GetMajorType(&majortype);
    if (FAILED(hr)) 
    { 
        return hr;
    }

    if (majortype != MFMediaType_Audio)
    {
        return MF_E_INVALIDMEDIATYPE;
    }

    // Get the audio subtype.
    hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
    if (FAILED(hr)) 
    { 
        return hr;
    }

    if (subtype == MFAudioFormat_PCM)
    {
        // This is already a PCM audio type. Return the same pointer.

        *ppType = pType;
        (*ppType)->AddRef();

        return S_OK;
    }

    // Get the sample rate and other information from the audio format.

    cChannels = MFGetAttributeUINT32(pType, MF_MT_AUDIO_NUM_CHANNELS, 0);
    samplesPerSec = MFGetAttributeUINT32(pType, MF_MT_AUDIO_SAMPLES_PER_SECOND, 0);
    bitsPerSample = MFGetAttributeUINT32(pType, MF_MT_AUDIO_BITS_PER_SAMPLE, 16);

    // Note: Some encoded audio formats do not contain a value for bits/sample.
    // In that case, use a default value of 16. Most codecs will accept this value.

    if (cChannels == 0 || samplesPerSec == 0)
    {
        return MF_E_INVALIDTYPE;
    }

    // Create the corresponding PCM audio type.
    hr = CreatePCMAudioType(samplesPerSec, bitsPerSample, cChannels, ppType);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="dd08f-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dd08f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd08f-141">Tipi di supporti audio</span><span class="sxs-lookup"><span data-stu-id="dd08f-141">Audio Media Types</span></span>](audio-media-types.md)
</dt> </dl>

 

 



