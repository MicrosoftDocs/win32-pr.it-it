---
description: 'Il Microsoft Media Foundation decodificatore AAC è una trasformazione Media Foundation che decodifica i profili AAC (Advanced Audio Coding) e HE-AAC (High Efficiency AAC) seguenti:'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: Decodificatore AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7554d6bc4a13fe1e4af4c51e75f1fe8a0bd38286
ms.sourcegitcommit: 3a0a8a8fdce560a81a27789a1c04172ed96147b1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/22/2021
ms.locfileid: "112436585"
---
# <a name="aac-decoder"></a><span data-ttu-id="b3e7a-103">Decodificatore AAC</span><span class="sxs-lookup"><span data-stu-id="b3e7a-103">AAC Decoder</span></span>

<span data-ttu-id="b3e7a-104">Il Microsoft Media Foundation decodificatore AAC è una [trasformazione Media Foundation](media-foundation-transforms.md) che decodifica i profili AAC (Advanced Audio Coding) e HE-AAC (High Efficiency AAC) seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3e7a-104">The Microsoft Media Foundation AAC decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes the following Advanced Audio Coding (AAC) and High Efficiency AAC (HE-AAC) profiles:</span></span>

-   <span data-ttu-id="b3e7a-105">Profilo MPEG-2 AAC Low Complexity (LC) (multicanale).</span><span class="sxs-lookup"><span data-stu-id="b3e7a-105">MPEG-2 AAC Low Complexity (LC) profile (multichannel).</span></span>
-   <span data-ttu-id="b3e7a-106">MPEG-4 HE-AAC v1 (multicanale) con core AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-106">MPEG-4 HE-AAC v1 (multichannel) with AAC-LC core.</span></span>
-   <span data-ttu-id="b3e7a-107">MPEG-4 HE-AAC v2 (stereo) con core AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-107">MPEG-4 HE-AAC v2 (stereo) with AAC-LC core.</span></span>

<span data-ttu-id="b3e7a-108">Il decodificatore AAC supporta sia flussi AAC non elaborati senza intestazioni che AAC in un flusso di trasporto dati audio (ADTS).</span><span class="sxs-lookup"><span data-stu-id="b3e7a-108">The AAC decoder supports both raw AAC streams with no headers and AAC in an audio data transport stream (ADTS).</span></span>

<span data-ttu-id="b3e7a-109">A partire Windows 8, il decodificatore AAC supporta anche la decodifica dei flussi di trasporto audio MPEG-4 con un livello multiplex (LATM) e un livello di sincronizzazione (LOAS).</span><span class="sxs-lookup"><span data-stu-id="b3e7a-109">Starting in Windows 8, the AAC decoder also supports decoding MPEG-4 audio transport streams with a multiplex layer (LATM) and synchronization layer (LOAS).</span></span> <span data-ttu-id="b3e7a-110">Può anche convertire un flusso LATM/LOAS in ADTS.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-110">It can also convert an LATM/LOAS stream to ADTS.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="b3e7a-111">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="b3e7a-111">Class Identifier</span></span>

<span data-ttu-id="b3e7a-112">L'identificatore di classe (CLSID) del codificatore AAC è **\_ CLSID CMSAACDecMFT,** definito nel file di intestazione wmcodecdsp.h.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-112">The class identifier (CLSID) of the AAC encoder is **CLSID\_CMSAACDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="b3e7a-113">Tipi di supporti</span><span class="sxs-lookup"><span data-stu-id="b3e7a-113">Media Types</span></span>

<span data-ttu-id="b3e7a-114">Il decodificatore AAC supporta i tipi di supporti seguenti.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-114">The AAC decoder supports the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="b3e7a-115">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="b3e7a-115">Input Types</span></span>

<span data-ttu-id="b3e7a-116">Il decodificatore AAC supporta i sottotipi audio seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3e7a-116">The AAC decoder supports the following audio subtypes:</span></span>



| <span data-ttu-id="b3e7a-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="b3e7a-117">Subtype</span></span>                     | <span data-ttu-id="b3e7a-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3e7a-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="b3e7a-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3e7a-119">Header</span></span>       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="b3e7a-120">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-120">**MFAudioFormat_AAC**</span></span>      | <span data-ttu-id="b3e7a-121">AAC non elaborato o AAC ADTS.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-121">Raw AAC or ADTS AAC.</span></span><br/> <span data-ttu-id="b3e7a-122">Per questo sottotipo, il tipo di supporto fornisce la frequenza di campionamento e il numero di canali prima dell'applicazione di strumenti SBR (Spectral Band Replication) e stereo parametrico (PS), se presenti.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-122">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="b3e7a-123">L'effetto dello strumento SBR è raddoppiare la frequenza di campionamento decodificata rispetto alla frequenza di campionamento AAC-LC principale.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-123">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="b3e7a-124">L'effetto dello strumento PS è decodificare stereo da un flusso AAC-LC core monocanale.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-124">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span><br/> <span data-ttu-id="b3e7a-125">Questo sottotipo equivale **a MEDIASUBTYPE_MPEG_HEAAC**, definito in wmcodecdsp.h.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-125">This subtype is equivalent to **MEDIASUBTYPE_MPEG_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="b3e7a-126">Vedere [GUID sottotipo audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="b3e7a-126">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> <br/> <span data-ttu-id="b3e7a-127">[L'origine file MPEG-4 e](mpeg-4-file-source.md) il parser ADTS generano questo sottotipo.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-127">The [MPEG-4 File Source](mpeg-4-file-source.md) and the ADTS Parser output this subtype.</span></span> <br/> | <span data-ttu-id="b3e7a-128">mfapi.h</span><span class="sxs-lookup"><span data-stu-id="b3e7a-128">mfapi.h</span></span>      |
| <span data-ttu-id="b3e7a-129">**MEDIASUBTYPE_RAW_AAC1**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-129">**MEDIASUBTYPE_RAW_AAC1**</span></span> | <span data-ttu-id="b3e7a-130">AAC non elaborato.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-130">Raw AAC.</span></span> <br/> <span data-ttu-id="b3e7a-131">Questo sottotipo viene usato per AAC contenuto in un file AVI con il tag di formato audio uguale a WAVE_FORMAT_RAW_AAC1 (0x00FF).</span><span class="sxs-lookup"><span data-stu-id="b3e7a-131">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE_FORMAT_RAW_AAC1 (0x00FF).</span></span> <br/> <span data-ttu-id="b3e7a-132">Per questo sottotipo, il tipo di supporto fornisce la frequenza di campionamento e il numero di canali dopo l'applicazione degli strumenti SBR e PS, se presenti.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-132">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="b3e7a-133">wmcodecdsp.h</span><span class="sxs-lookup"><span data-stu-id="b3e7a-133">wmcodecdsp.h</span></span> |



 

<span data-ttu-id="b3e7a-134">Per configurare il decodificatore AAC, impostare gli attributi seguenti sul tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-134">To configure the AAC decoder, set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3e7a-135">Attributo</span><span class="sxs-lookup"><span data-stu-id="b3e7a-135">Attribute</span></span></th>
<th><span data-ttu-id="b3e7a-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3e7a-136">Description</span></span></th>
<th><span data-ttu-id="b3e7a-137">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b3e7a-137">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3e7a-138"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3e7a-138"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="b3e7a-139">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-139">Major type.</span></span></td>
<td><span data-ttu-id="b3e7a-140">Deve essere <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-140">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3e7a-141"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3e7a-141"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="b3e7a-142">Sottotipo audio.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-142">Audio subtype.</span></span></td>
<td><span data-ttu-id="b3e7a-143">Per informazioni dettagliate, vedere la descrizione precedente.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-143">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3e7a-144"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="b3e7a-144"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="b3e7a-145">Profilo e livello audio.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-145">Audio profile and level.</span></span> <br/></td>
<td><span data-ttu-id="b3e7a-146">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-146">Optional.</span></span> <span data-ttu-id="b3e7a-147">Si applica solo <strong>a MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-147">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <br/> <span data-ttu-id="b3e7a-148">Il valore di questo attributo è il campo <strong>audioProfileLevelIndication,</strong> come definito da ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-148">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span> <br/> <span data-ttu-id="b3e7a-149">Se sconosciuto, impostare su zero o 0xFE ( &quot; nessun profilo audio specificato &quot; ).</span><span class="sxs-lookup"><span data-stu-id="b3e7a-149">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3e7a-150"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="b3e7a-150"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="b3e7a-151">Tipo di payload.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-151">Payload type.</span></span><br/></td>
<td><span data-ttu-id="b3e7a-152">Si applica solo <strong>a MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-152">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <span data-ttu-id="b3e7a-153">Il decodificatore supporta i tipi di payload seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3e7a-153">The decoder supports the following payload types:</span></span> <br/>
<ul>
<li><span data-ttu-id="b3e7a-154">0: AAC non elaborato.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-154">0: Raw AAC.</span></span> <span data-ttu-id="b3e7a-155">Il flusso contiene raw_data_block() solo elementi, come definito da MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-155">The stream contains raw_data_block() elements only, as defined by MPEG-2.</span></span></li>
<li><span data-ttu-id="b3e7a-156">1: ADTS.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-156">1: ADTS.</span></span> <span data-ttu-id="b3e7a-157">Il flusso contiene un adts_sequence(), come definito da MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-157">The stream contains an adts_sequence(), as defined by MPEG-2.</span></span> <span data-ttu-id="b3e7a-158">È consentito raw_data_block() per adts_frame().</span><span class="sxs-lookup"><span data-stu-id="b3e7a-158">Only one raw_data_block() per adts_frame() is allowed.</span></span></li>
<li><span data-ttu-id="b3e7a-159">3: flusso di trasporto audio con un livello di sincronizzazione (LOAS) e un livello multiplex (LATM).</span><span class="sxs-lookup"><span data-stu-id="b3e7a-159">3: Audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span> <span data-ttu-id="b3e7a-160">Dei tre tipi di LOAS, è supportato <strong>solo AudioSyncStream.</strong></span><span class="sxs-lookup"><span data-stu-id="b3e7a-160">Of the three types of LOAS, only <strong>AudioSyncStream</strong> is supported.</span></span> <span data-ttu-id="b3e7a-161">Il livello multiplex è <strong>AudioMuxElement,</strong>limitato a un programma audio e a un livello.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-161">The multiplex layer is <strong>AudioMuxElement</strong>, restricted to one audio program and one layer.</span></span></li>
</ul><span data-ttu-id="b3e7a-162">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-162">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="b3e7a-163">Se questo attributo non viene specificato, viene usato il valore predefinito 0, che specifica che il flusso contiene solo raw_data_block elementi.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-163">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3e7a-164"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3e7a-164"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="b3e7a-165">Profondità in bit desiderata dell'audio PCM decodificato.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-165">Desired bit depth of the decoded PCM audio.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b3e7a-166"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3e7a-166"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="b3e7a-167">Specifica l'assegnazione dei canali audio alle posizioni del parlante.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-167">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="b3e7a-168">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-168">Optional.</span></span> <span data-ttu-id="b3e7a-169">Per altre informazioni, vedere <a href="#format-constraints">Vincoli di formato</a>.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-169">For more information, see <a href="#format-constraints">Format Constraints</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3e7a-170"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3e7a-170"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="b3e7a-171">Numero di canali, incluso il canale a bassa frequenza (LFE), se presente.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-171">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/></td>
<td><span data-ttu-id="b3e7a-172">L'interpretazione di questo valore dipende dal sottotipo multimediale, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-172">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3e7a-173"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3e7a-173"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="b3e7a-174">Frequenza di campionamento, in campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-174">Sample rate, in samples per second.</span></span><br/></td>
<td><span data-ttu-id="b3e7a-175">L'interpretazione di questo valore dipende dal sottotipo multimediale, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-175">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3e7a-176"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3e7a-176"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="b3e7a-177">Informazioni aggiuntive sul formato.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-177">Additional format information.</span></span></td>
<td><span data-ttu-id="b3e7a-178">Il valore di questo attributo dipende dal sottotipo.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-178">The value of this attribute depends on the subtype.</span></span><br/>
<ul>
<li><span data-ttu-id="b3e7a-179"><strong>MFAudioFormat_AAC</strong>: contiene la parte della struttura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> visualizzata dopo la struttura <strong>WAVEFORMATEX,</strong> ovvero dopo il <strong>membro wfx.</strong></span><span class="sxs-lookup"><span data-stu-id="b3e7a-179"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="b3e7a-180">Questi dati sono seguiti dai dati AudioSpecificConfig(), come definito da ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-180">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="b3e7a-181"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contiene i dati AudioSpecificConfig().</span><span class="sxs-lookup"><span data-stu-id="b3e7a-181"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span> <span data-ttu-id="b3e7a-182">Questi dati devono essere visualizzati. In caso contrario, il decodificatore rifiuterà il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-182">This data must appear; otherwise, the decoder will reject the media type.</span></span></li>
</ul>
<span data-ttu-id="b3e7a-183">La lunghezza dei dati AudioSpecificConfig() è di 2 byte per AAC-LC o HE-AAC con segnalazione implicita di SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-183">The length of the AudioSpecificConfig() data is 2 bytes for AAC-LC or HE-AAC with implicit signaling of SBR/PS.</span></span> <span data-ttu-id="b3e7a-184">Si tratta di più di 2 byte per HE-AAC con segnalazione esplicita di SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-184">It is more than 2 bytes for HE-AAC with explicit signaling of SBR/PS.</span></span><br/> <span data-ttu-id="b3e7a-185">Il valore di <strong>audioObjectType</strong> definito in AudioSpecificConfig() deve essere 2, che indica AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-185">The value of <strong>audioObjectType</strong> as defined in AudioSpecificConfig() must be 2, indicating AAC-LC.</span></span> <span data-ttu-id="b3e7a-186">Il valore di <strong>extensionAudioObjectType</strong> deve essere 5 per SBR o 29 per PS.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-186">The value of <strong>extensionAudioObjectType</strong> must be 5 for SBR or 29 for PS.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a><span data-ttu-id="b3e7a-187">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="b3e7a-187">Output Types</span></span>

<span data-ttu-id="b3e7a-188">Il decodificatore supporta i tipi di output seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3e7a-188">The decoder supports the following output types:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3e7a-189">Subtype</span><span class="sxs-lookup"><span data-stu-id="b3e7a-189">Subtype</span></span></th>
<th><span data-ttu-id="b3e7a-190">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3e7a-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3e7a-191"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="b3e7a-191"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="b3e7a-192">Audio a virgola mobile IEEE.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-192">IEEE floating-point audio.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3e7a-193"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="b3e7a-193"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="b3e7a-194">Audio PCM a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-194">16-bit PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3e7a-195"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="b3e7a-195"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="b3e7a-196">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-196">Requires Windows 8.</span></span> <br/> <span data-ttu-id="b3e7a-197">Questo tipo di output può essere usato per convertire un flusso AAC nel formato LOAS/LATM nel formato ADTS.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-197">This output type can be used to convert an AAC stream in the LOAS/LATM format to ADTS format.</span></span> <br/> <span data-ttu-id="b3e7a-198">Per convertire un flusso LOAS/LATM in un flusso ADTS, impostare il tipo di input su <strong>MFAudioFormat_AAC</strong> con tipo di payload 3 (LOAS).</span><span class="sxs-lookup"><span data-stu-id="b3e7a-198">To convert an LOAS/LATM stream to an ADTS stream, set the input type to <strong>MFAudioFormat_AAC</strong> with payload type 3 (LOAS).</span></span> <span data-ttu-id="b3e7a-199">Impostare quindi il tipo di output <strong>su MFAudioFormat_AAC</strong> con tipo di payload 1 (ADTS).</span><span class="sxs-lookup"><span data-stu-id="b3e7a-199">Then set the output type to <strong>MFAudioFormat_AAC</strong> with payload type 1 (ADTS).</span></span> <span data-ttu-id="b3e7a-200">Il decodificatore riformatta il conainter senza decodificare il flusso di bit.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-200">The decoder will reformat the conainter without decoding the bitstream.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b3e7a-201">Il decodificatore non registra <strong>MFAudioFormat_AAC</strong> come tipo di output.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-201">The decoder does not register <strong>MFAudioFormat_AAC</strong> as an output type.</span></span> <span data-ttu-id="b3e7a-202">Tuttavia, se l'applicazione imposta il tipo di input come descritto, il metodo <strong></strong> <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> restituisce MFAudioFormat_AAC nell'elenco dei tipi di output disponibili.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-202">However, if the application sets the input type as described, the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> method returns <strong>MFAudioFormat_AAC</strong> in the list of available output types.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b3e7a-203">Se il flusso di input contiene più di due canali, il decodificatore AAC offre due opzioni per il formato di output:</span><span class="sxs-lookup"><span data-stu-id="b3e7a-203">If the input stream contains more than two channels, the AAC decoder provides two options for the output format:</span></span>

-   <span data-ttu-id="b3e7a-204">Stessa configurazione del canale del tipo di input.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-204">The same channel configuration as the input type.</span></span>
-   <span data-ttu-id="b3e7a-205">Ripiegato stereo.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-205">Stereo fold-down.</span></span>

## <a name="format-constraints"></a><span data-ttu-id="b3e7a-206">Vincoli di formato</span><span class="sxs-lookup"><span data-stu-id="b3e7a-206">Format Constraints</span></span>

<span data-ttu-id="b3e7a-207">La frequenza di campionamento dell'audio decodificato deve essere una delle seguenti, dopo l'applicazione di SBR (se presente):</span><span class="sxs-lookup"><span data-stu-id="b3e7a-207">The decoded audio sampling rate must be one of the following, after SBR is applied (if present):</span></span>

-   <span data-ttu-id="b3e7a-208">8 kHz</span><span class="sxs-lookup"><span data-stu-id="b3e7a-208">8 kHz</span></span>
-   <span data-ttu-id="b3e7a-209">11,025 kHz</span><span class="sxs-lookup"><span data-stu-id="b3e7a-209">11.025 kHz</span></span>
-   <span data-ttu-id="b3e7a-210">12 kHz</span><span class="sxs-lookup"><span data-stu-id="b3e7a-210">12 kHz</span></span>
-   <span data-ttu-id="b3e7a-211">16 kHz</span><span class="sxs-lookup"><span data-stu-id="b3e7a-211">16 kHz</span></span>
-   <span data-ttu-id="b3e7a-212">22,05 kHz</span><span class="sxs-lookup"><span data-stu-id="b3e7a-212">22.05 kHz</span></span>
-   <span data-ttu-id="b3e7a-213">24 kHz</span><span class="sxs-lookup"><span data-stu-id="b3e7a-213">24 kHz</span></span>
-   <span data-ttu-id="b3e7a-214">32 kHz</span><span class="sxs-lookup"><span data-stu-id="b3e7a-214">32 kHz</span></span>
-   <span data-ttu-id="b3e7a-215">44,1 kHz</span><span class="sxs-lookup"><span data-stu-id="b3e7a-215">44.1 kHz</span></span>
-   <span data-ttu-id="b3e7a-216">48 kHz</span><span class="sxs-lookup"><span data-stu-id="b3e7a-216">48 kHz</span></span>

<span data-ttu-id="b3e7a-217">Le frequenze di campionamento superiori a 48 kHz non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-217">Sampling rates above 48 kHz are not supported.</span></span>

<span data-ttu-id="b3e7a-218">Il decodificatore supporta fino a 6 canali audio.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-218">The decoder supports up to 6 audio channels.</span></span> <span data-ttu-id="b3e7a-219">Per ogni configurazione del parlante, il decodificatore prevede che gli elementi sintattici AAC vengano visualizzati in un determinato ordine.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-219">For each speaker configuration, the decoder expects the AAC syntactic elements to appear in a certain order.</span></span> <span data-ttu-id="b3e7a-220">Nella tabella seguente sono elencate le configurazioni del parlante supportate.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-220">The following table lists the supported speaker configurations.</span></span> <span data-ttu-id="b3e7a-221">La terza colonna della tabella elenca gli elementi sintattici previsti e il relativo ordine, usando la notazione seguente:</span><span class="sxs-lookup"><span data-stu-id="b3e7a-221">The third column of the table lists the expected syntactic elements and their order, using the following notation:</span></span>

-   <span data-ttu-id="b3e7a-222"><SCE1>: la single_channel_element (SCE) associata al front center speaker.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-222"><SCE1>: The single_channel_element (SCE) associated with the front center speaker.</span></span>
-   <span data-ttu-id="b3e7a-223"><SCE2>: SCE associato al parlante centrale posteriore.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-223"><SCE2>: The SCE associated with the back center speaker.</span></span>
-   <span data-ttu-id="b3e7a-224"><CPE1>: channel_pair_element (CPE) associato ai front speaker.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-224"><CPE1>: The channel_pair_element (CPE) associated with the front speakers.</span></span>
-   <span data-ttu-id="b3e7a-225"><CPE2>: CPE associato agli altoparlanti posteriore (o laterale)</span><span class="sxs-lookup"><span data-stu-id="b3e7a-225"><CPE2>: The CPE associated with the back (or side) speakers</span></span>
-   <span data-ttu-id="b3e7a-226"><LFE>: lfe_channel_element (LFE).</span><span class="sxs-lookup"><span data-stu-id="b3e7a-226"><LFE>: The lfe_channel_element (LFE).</span></span>

<span data-ttu-id="b3e7a-227">Per altre informazioni su questi elementi sintattici, vedere ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-227">For more information about these syntactic elements, refer to ISO/IEC 13818-7.</span></span>



| <span data-ttu-id="b3e7a-228">Configurazione</span><span class="sxs-lookup"><span data-stu-id="b3e7a-228">Configuration</span></span>       | <span data-ttu-id="b3e7a-229">Maschera canale</span><span class="sxs-lookup"><span data-stu-id="b3e7a-229">Channel Mask</span></span>                                                                                                                                                              | <span data-ttu-id="b3e7a-230">Elementi sintattici AAC</span><span class="sxs-lookup"><span data-stu-id="b3e7a-230">AAC Syntactic Elements</span></span>                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="b3e7a-231">Mono</span><span class="sxs-lookup"><span data-stu-id="b3e7a-231">Mono</span></span>                | <span data-ttu-id="b3e7a-232">**SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-232">**SPEAKER_FRONT_CENTER**</span></span>                                                                                                                                                | <SCE1>                                    |
| <span data-ttu-id="b3e7a-233">Stereo o doppio mono</span><span class="sxs-lookup"><span data-stu-id="b3e7a-233">Stereo or dual mono</span></span> | <span data-ttu-id="b3e7a-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span></span>                                                                                                                     | <CPE1>                                    |
| <span data-ttu-id="b3e7a-235">2/1</span><span class="sxs-lookup"><span data-stu-id="b3e7a-235">2/1</span></span>                 | <span data-ttu-id="b3e7a-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span></span>                                                                                        | <CPE1><SCE1>                        |
| <span data-ttu-id="b3e7a-237">2/2</span><span class="sxs-lookup"><span data-stu-id="b3e7a-237">2/2</span></span>                 | <span data-ttu-id="b3e7a-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                                              | <CPE1><CPE2>                        |
| <span data-ttu-id="b3e7a-239">3/0</span><span class="sxs-lookup"><span data-stu-id="b3e7a-239">3/0</span></span>                 | <span data-ttu-id="b3e7a-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span></span>                                                                                       | <SCE1><CPE1>                        |
| <span data-ttu-id="b3e7a-241">3/1</span><span class="sxs-lookup"><span data-stu-id="b3e7a-241">3/1</span></span>                 | <span data-ttu-id="b3e7a-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span></span>                                                          | <SCE1><CPE1><SCE2>            |
| <span data-ttu-id="b3e7a-243">3/2</span><span class="sxs-lookup"><span data-stu-id="b3e7a-243">3/2</span></span>                 | <span data-ttu-id="b3e7a-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                | <SCE1><CPE1><CPE2>            |
| <span data-ttu-id="b3e7a-245">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="b3e7a-245">3/2 + LFE</span></span>           | <span data-ttu-id="b3e7a-246">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-246">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span> | <SCE1><CPE1><CPE2><LFE> |



 

<span data-ttu-id="b3e7a-247">Per l'AAC non elaborato, ogni esempio di input deve contenere esattamente un frame compresso AAC completo.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-247">For raw AAC, each input sample must contain exactly one full AAC compressed frame.</span></span>

<span data-ttu-id="b3e7a-248">Per ADTS, ogni campione di input può contenere più fotogrammi audio, nonché fotogrammi parziali, che possono estendersi su limiti di campionamento.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-248">For ADTS, each input sample can contain multiple audio frames, as well as partial frames   that is, frames can span sample boundaries.</span></span> <span data-ttu-id="b3e7a-249">Ogni intestazione ADTS deve essere seguita da un frame AAC.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-249">Each ADTS header must be followed by one AAC frame.</span></span>

<span data-ttu-id="b3e7a-250">Il decodificatore AAC non supporta gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3e7a-250">The AAC decoder does not support any of the following:</span></span>

-   <span data-ttu-id="b3e7a-251">Profilo principale, Sample-Rate profilo scalabile (SRS) o Profilo di stima a lungo termine (LTP).</span><span class="sxs-lookup"><span data-stu-id="b3e7a-251">Main profile, Sample-Rate Scalable (SRS) profile, or Long Term Prediction (LTP) profile.</span></span>
-   <span data-ttu-id="b3e7a-252">Formato di interscambio dati audio (ADIF).</span><span class="sxs-lookup"><span data-stu-id="b3e7a-252">Audio data interchange format (ADIF).</span></span>
-   <span data-ttu-id="b3e7a-253">Flussi di trasporto LATM/LAOS.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-253">LATM/LAOS transport streams.</span></span>
-   <span data-ttu-id="b3e7a-254">Elementi del canale di accoppiamento (CCE).</span><span class="sxs-lookup"><span data-stu-id="b3e7a-254">Coupling channel elements (CCEs).</span></span> <span data-ttu-id="b3e7a-255">Il decodificatore ignora i fotogrammi audio con CCE.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-255">The decoder will skip audio frames with CCEs.</span></span>
-   <span data-ttu-id="b3e7a-256">AAC-LC con dimensioni del frame di 960 campioni.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-256">AAC-LC with a 960-sample frame size.</span></span> <span data-ttu-id="b3e7a-257">Sono supportati solo 1024 frame di esempio.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-257">Only 1024-sample frames are supported.</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="b3e7a-258">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="b3e7a-258">Transform Attributes</span></span>

<span data-ttu-id="b3e7a-259">Il decodificatore AAC implementa il [**metodo IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)</span><span class="sxs-lookup"><span data-stu-id="b3e7a-259">The AAC decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="b3e7a-260">Le applicazioni possono usare questo metodo per ottenere o impostare gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-260">Applications can use this method to get or set the following attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3e7a-261">Attributo</span><span class="sxs-lookup"><span data-stu-id="b3e7a-261">Attribute</span></span></th>
<th><span data-ttu-id="b3e7a-262">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3e7a-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3e7a-263"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3e7a-263"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span></span></td>
<td><span data-ttu-id="b3e7a-264">Specifica se l'audio a 2 canali è codificato come stereo o doppio mono.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-264">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span> <span data-ttu-id="b3e7a-265">Considera come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-265">Treat as read-only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3e7a-266"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3e7a-266"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span></span></td>
<td><span data-ttu-id="b3e7a-267">Specifica la modalità di riproduzione dell'audio doppio mono da parte del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-267">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="b3e7a-268">Il valore predefinito è <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Output Ch1 per gli altoparlanti sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-268">The default value is <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Output Ch1 to the left and right speakers.</span></span> <br/> <span data-ttu-id="b3e7a-269">Le applicazioni possono impostare questa proprietà per modificare il comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-269">Applications can set this property to change the default behavior.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3e7a-270"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3e7a-270"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="b3e7a-271">Il decodificatore AAC non gestisce le modifiche di formato dinamico e deve essere scaricato o svuotato prima che venga impostato un nuovo tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-271">The AAC decoder does not handle dynamic format changes, and must be flushed or drained before a new input media type is set.</span></span> <span data-ttu-id="b3e7a-272">Considerare questo attributo come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-272">Treat this attribute as read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b3e7a-273">Il decodificatore AAC segnala erroneamente il valore <strong>TRUE</strong> per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-273">The AAC decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="b3e7a-274">In Windows 7 il decodificatore segnala erroneamente il valore <strong>TRUE</strong> per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-274">In Windows 7, the decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span> <span data-ttu-id="b3e7a-275">In Windows 8, il decodificatore segnala <strong>FALSE,</strong>che è il valore corretto</span><span class="sxs-lookup"><span data-stu-id="b3e7a-275">In Windows 8, the decoder reports <strong>FALSE</strong>, which is the correct value</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a><span data-ttu-id="b3e7a-276">Tipi di supporti di esempio</span><span class="sxs-lookup"><span data-stu-id="b3e7a-276">Example Media Types</span></span>

<span data-ttu-id="b3e7a-277">Ecco un esempio del tipo di supporto di input necessario per un flusso AAC-LC a 6 canali a 48 kHz, usando un payload AAC non elaborato:</span><span class="sxs-lookup"><span data-stu-id="b3e7a-277">Here is an example of the input media type needed for a 6-channel, 48-kHz AAC-LC stream, using a raw AAC payload:</span></span>



| <span data-ttu-id="b3e7a-278">Attributo</span><span class="sxs-lookup"><span data-stu-id="b3e7a-278">Attribute</span></span>                                                                                      | <span data-ttu-id="b3e7a-279">Valore</span><span class="sxs-lookup"><span data-stu-id="b3e7a-279">Value</span></span>                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3e7a-280">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-280">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="b3e7a-281">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-281">**MFMediaType_Audio**</span></span>                                                               |
| [<span data-ttu-id="b3e7a-282">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-282">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="b3e7a-283">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-283">**MFAudioFormat_AAC**</span></span>                                                               |
| [<span data-ttu-id="b3e7a-284">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-284">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="b3e7a-285">48000</span><span class="sxs-lookup"><span data-stu-id="b3e7a-285">48000</span></span>                                                                                |
| [<span data-ttu-id="b3e7a-286">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-286">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="b3e7a-287">6</span><span class="sxs-lookup"><span data-stu-id="b3e7a-287">6</span></span>                                                                                    |
| [<span data-ttu-id="b3e7a-288">MF_MT_AAC_PAYLOAD_TYPE</span><span class="sxs-lookup"><span data-stu-id="b3e7a-288">MF_MT_AAC_PAYLOAD_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="b3e7a-289">0</span><span class="sxs-lookup"><span data-stu-id="b3e7a-289">0</span></span>                                                                                    |
| [<span data-ttu-id="b3e7a-290">**MF_MT_USER_DATA**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-290">**MF_MT_USER_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="b3e7a-291">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span><span class="sxs-lookup"><span data-stu-id="b3e7a-291">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span></span> |
| [<span data-ttu-id="b3e7a-292">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span><span class="sxs-lookup"><span data-stu-id="b3e7a-292">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="b3e7a-293">0x2a (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="b3e7a-293">0x2a (optional)</span></span>                                                                      |



 

<span data-ttu-id="b3e7a-294">I primi 12 byte di [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) corrispondono ai membri della struttura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3e7a-294">The first 12 bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspond to the following [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure members:</span></span>

-   <span data-ttu-id="b3e7a-295">**wPayloadType** = 0 (AAC non elaborato)</span><span class="sxs-lookup"><span data-stu-id="b3e7a-295">**wPayloadType** = 0 (raw AAC)</span></span>
-   <span data-ttu-id="b3e7a-296">**wAudioProfileLevelIndication** = 0x2a (profilo AAC, livello 4)</span><span class="sxs-lookup"><span data-stu-id="b3e7a-296">**wAudioProfileLevelIndication** = 0x2a (AAC Profile, Level 4)</span></span>
-   <span data-ttu-id="b3e7a-297">**wStructType** = 0</span><span class="sxs-lookup"><span data-stu-id="b3e7a-297">**wStructType** = 0</span></span>

<span data-ttu-id="b3e7a-298">Gli ultimi due byte [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contengono il valore di AudioSpecificConfig(), come definito da MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="b3e7a-298">The last two bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contain the value of AudioSpecificConfig(), as defined by MPEG-4.</span></span>

-   <span data-ttu-id="b3e7a-299">AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 bit)</span><span class="sxs-lookup"><span data-stu-id="b3e7a-299">AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 bits)</span></span>
-   <span data-ttu-id="b3e7a-300">AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bit)</span><span class="sxs-lookup"><span data-stu-id="b3e7a-300">AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bits)</span></span>
-   <span data-ttu-id="b3e7a-301">AudioSpecificConfig.channelConfiguration = 6 (4 bit)</span><span class="sxs-lookup"><span data-stu-id="b3e7a-301">AudioSpecificConfig.channelConfiguration = 6 (4 bits)</span></span>
-   <span data-ttu-id="b3e7a-302">GASpecificConfig.frameLengthFlag = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="b3e7a-302">GASpecificConfig.frameLengthFlag = 0 (1 bit)</span></span>
-   <span data-ttu-id="b3e7a-303">GASpecificConfig.dependsOnCoreCoder = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="b3e7a-303">GASpecificConfig.dependsOnCoreCoder = 0 (1 bit)</span></span>
-   <span data-ttu-id="b3e7a-304">GASpecificConfig.extensionFlag = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="b3e7a-304">GASpecificConfig.extensionFlag = 0 (1 bit)</span></span>

<span data-ttu-id="b3e7a-305">Dato questo tipo di input, usare il tipo di supporto di output seguente per ottenere l'audio PCM a virgola mobile a 6 canali a 32 bit dal decodificatore:</span><span class="sxs-lookup"><span data-stu-id="b3e7a-305">Given this input type, use the following output media type to get 6-channel, 32-bit floating point PCM audio from the decoder:</span></span>



| <span data-ttu-id="b3e7a-306">Attributo</span><span class="sxs-lookup"><span data-stu-id="b3e7a-306">Attribute</span></span>                                                                                    | <span data-ttu-id="b3e7a-307">Valore</span><span class="sxs-lookup"><span data-stu-id="b3e7a-307">Value</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [<span data-ttu-id="b3e7a-308">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-308">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="b3e7a-309">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-309">**MFMediaType_Audio**</span></span>   |
| [<span data-ttu-id="b3e7a-310">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-310">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="b3e7a-311">**MFAudioFormat_Float**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-311">**MFAudioFormat_Float**</span></span> |
| [<span data-ttu-id="b3e7a-312">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-312">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="b3e7a-313">32</span><span class="sxs-lookup"><span data-stu-id="b3e7a-313">32</span></span>                       |
| [<span data-ttu-id="b3e7a-314">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-314">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="b3e7a-315">48000</span><span class="sxs-lookup"><span data-stu-id="b3e7a-315">48000</span></span>                    |
| [<span data-ttu-id="b3e7a-316">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-316">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="b3e7a-317">6</span><span class="sxs-lookup"><span data-stu-id="b3e7a-317">6</span></span>                        |
| [<span data-ttu-id="b3e7a-318">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-318">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="b3e7a-319">1152000 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="b3e7a-319">1152000 (optional)</span></span>       |
| [<span data-ttu-id="b3e7a-320">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-320">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="b3e7a-321">24 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="b3e7a-321">24 (optional)</span></span>            |
| [<span data-ttu-id="b3e7a-322">**MF_MT_AUDIO_CHANNEL_MASK**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-322">**MF_MT_AUDIO_CHANNEL_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                   | <span data-ttu-id="b3e7a-323">0x3f (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="b3e7a-323">0x3f (optional)</span></span>          |



 

<span data-ttu-id="b3e7a-324">Se è installato Il supplemento per l'aggiornamento della piattaforma per Windows Vista, il decodificatore audio AAC è disponibile in Windows Vista, ma è accessibile solo in Windows Vista usando il lettore [di origine](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="b3e7a-324">If Platform Update Supplement for Windows Vista is installed, the AAC audio decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3e7a-325">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3e7a-325">Requirements</span></span>



| <span data-ttu-id="b3e7a-326">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3e7a-326">Requirement</span></span> | <span data-ttu-id="b3e7a-327">Valore</span><span class="sxs-lookup"><span data-stu-id="b3e7a-327">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3e7a-328">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3e7a-328">Minimum supported client</span></span><br/> | <span data-ttu-id="b3e7a-329">Solo app desktop di Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3e7a-329">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="b3e7a-330">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3e7a-330">Minimum supported server</span></span><br/> | <span data-ttu-id="b3e7a-331">Solo app desktop di Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3e7a-331">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="b3e7a-332">DLL</span><span class="sxs-lookup"><span data-stu-id="b3e7a-332">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3e7a-333"><dt>Msmpeg2adec.dll in Windows 7; </dt> <dt>MSAudDecMFT.dll in Windows 8</dt></span><span class="sxs-lookup"><span data-stu-id="b3e7a-333"><dt>Msmpeg2adec.dll on Windows 7; </dt> <dt>MSAudDecMFT.dll on Windows 8</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3e7a-334">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3e7a-334">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3e7a-335">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="b3e7a-335">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="b3e7a-336">Tipi di supporti AAC</span><span class="sxs-lookup"><span data-stu-id="b3e7a-336">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="b3e7a-337">Tipi di supporti audio</span><span class="sxs-lookup"><span data-stu-id="b3e7a-337">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="b3e7a-338">**Decodificatore audio MPEG-1/DD/AAC Microsoft**</span><span class="sxs-lookup"><span data-stu-id="b3e7a-338">**Microsoft MPEG-1/DD/AAC Audio Decoder**</span></span>](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[<span data-ttu-id="b3e7a-339">Supporto mpeg-4 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b3e7a-339">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="b3e7a-340">Formati multimediali supportati in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b3e7a-340">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>
