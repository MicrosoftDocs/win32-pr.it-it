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
# <a name="uncompressed-audio-media-types"></a>Tipi di supporti audio non compressi

Per creare un tipo audio non compresso completo, impostare almeno gli attributi seguenti sul puntatore all'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .



| Attributo                                                                                    | Descrizione                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md)                                    | Tipo principale. Impostare su \_ audio MFMediaType.                                                                                       |
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)                                           | Sottotipo. Vedere [GUID del sottotipo audio](audio-subtype-guids.md).                                                                 |
| [**numero \_ di \_ \_ canali audio MF mt \_**](mf-mt-audio-num-channels-attribute.md)                   | Numero dei canali audio.                                                                                                    |
| [**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**](mf-mt-audio-samples-per-second-attribute.md)      | Numero di campioni audio al secondo.                                                                                          |
| [**\_ \_ \_ allineamento blocchi audio MF \_ mt**](mf-mt-audio-block-alignment-attribute.md)             | Allineamento del blocco.                                                                                                             |
| [**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) | Numero medio di byte al secondo.                                                                                          |
| [**\_ \_ bit audio MF \_ mt \_ per \_ campione**](mf-mt-audio-bits-per-sample-attribute.md)            | Numero di bit per esempio audio.                                                                                             |
| [**\_ \_ tutti gli esempi MF mt \_ \_ Independent**](mf-mt-all-samples-independent-attribute.md)         | Specifica se ogni esempio audio è indipendente. Impostare su **true** per i \_ formati MFAudioFormat PCM e MFAudioFormat \_ float. |



 

Inoltre, per alcuni formati audio sono necessari gli attributi seguenti.



| Attributo                                                                                      | Descrizione                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ bit validi per l'audio MF mt \_ \_ \_ per \_ campione**](mf-mt-audio-valid-bits-per-sample-attribute.md) | Numero di bit validi di dati audio in ogni esempio audio. Impostare questo attributo se gli esempi audio contengono spaziatura interna, ovvero se il numero di bit validi in ogni campione audio è inferiore alle dimensioni del campione. |
| [**\_ \_ \_ maschera canale audio MF \_ mt**](mf-mt-audio-channel-mask-attribute.md)                     | Assegnazione dei canali audio alle posizioni degli altoparlanti. Impostare questo attributo per i flussi audio multicanale, ad esempio 5,1. Questo attributo non è necessario per l'audio mono o stereo.                       |



 

### <a name="example-code"></a>Codice di esempio

Il codice seguente illustra come creare un tipo di supporto per l'audio PCM non compresso.


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



Nell'esempio successivo viene preso come input un formato audio codificato e viene creato un tipo di audio PCM corrispondente. Questo tipo può essere impostato su un codificatore o un decodificatore, ad esempio.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti audio](audio-media-types.md)
</dt> </dl>

 

 



