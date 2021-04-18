---
description: 'Il decodificatore Microsoft Media Foundation AAC è una trasformazione Media Foundation che decodifica i profili AAC (Advanced Audio Coding) ed High Efficiency AAC (HE-AAC) seguenti:'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: Decoder AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82dde090dee98cddce9658366bde593b5fc779d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306768"
---
# <a name="aac-decoder"></a><span data-ttu-id="08f8c-103">Decoder AAC</span><span class="sxs-lookup"><span data-stu-id="08f8c-103">AAC Decoder</span></span>

<span data-ttu-id="08f8c-104">Il decodificatore Microsoft Media Foundation AAC è una [trasformazione Media Foundation](media-foundation-transforms.md) che decodifica i profili AAC (Advanced Audio Coding) ed High Efficiency AAC (HE-AAC) seguenti:</span><span class="sxs-lookup"><span data-stu-id="08f8c-104">The Microsoft Media Foundation AAC decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes the following Advanced Audio Coding (AAC) and High Efficiency AAC (HE-AAC) profiles:</span></span>

-   <span data-ttu-id="08f8c-105">Profilo MPEG-2 AAC con complessità bassa (LC) (multicanale).</span><span class="sxs-lookup"><span data-stu-id="08f8c-105">MPEG-2 AAC Low Complexity (LC) profile (multichannel).</span></span>
-   <span data-ttu-id="08f8c-106">MPEG-4 HE-AAC V1 (multicanale) con AAC-LC core.</span><span class="sxs-lookup"><span data-stu-id="08f8c-106">MPEG-4 HE-AAC v1 (multichannel) with AAC-LC core.</span></span>
-   <span data-ttu-id="08f8c-107">MPEG-4 HE-AAC v2 (stereo) con AAC-LC core.</span><span class="sxs-lookup"><span data-stu-id="08f8c-107">MPEG-4 HE-AAC v2 (stereo) with AAC-LC core.</span></span>

<span data-ttu-id="08f8c-108">Il decodificatore AAC supporta entrambi i flussi AAC non elaborati senza intestazioni e AAC in un flusso di trasporto dati audio (ADTS).</span><span class="sxs-lookup"><span data-stu-id="08f8c-108">The AAC decoder supports both raw AAC streams with no headers and AAC in an audio data transport stream (ADTS).</span></span>

<span data-ttu-id="08f8c-109">A partire da Windows 8, il decodificatore AAC supporta anche la decodifica dei flussi di trasporto audio MPEG-4 con un livello multiplex (LATM) e un livello di sincronizzazione (LOAS).</span><span class="sxs-lookup"><span data-stu-id="08f8c-109">Starting in Windows 8, the AAC decoder also supports decoding MPEG-4 audio transport streams with a multiplex layer (LATM) and synchronization layer (LOAS).</span></span> <span data-ttu-id="08f8c-110">Può anche convertire un flusso LATM/LOAS in ADTS.</span><span class="sxs-lookup"><span data-stu-id="08f8c-110">It can also convert an LATM/LOAS stream to ADTS.</span></span>

## <a name="media-types"></a><span data-ttu-id="08f8c-111">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="08f8c-111">Media Types</span></span>

<span data-ttu-id="08f8c-112">Il decodificatore AAC supporta i seguenti tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="08f8c-112">The AAC decoder supports the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="08f8c-113">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="08f8c-113">Input Types</span></span>

<span data-ttu-id="08f8c-114">Il decodificatore AAC supporta i sottotipi audio seguenti:</span><span class="sxs-lookup"><span data-stu-id="08f8c-114">The AAC decoder supports the following audio subtypes:</span></span>



| <span data-ttu-id="08f8c-115">Subtype</span><span class="sxs-lookup"><span data-stu-id="08f8c-115">Subtype</span></span>                     | <span data-ttu-id="08f8c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08f8c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="08f8c-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08f8c-117">Header</span></span>       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="08f8c-118">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="08f8c-118">**MFAudioFormat_AAC**</span></span>      | <span data-ttu-id="08f8c-119">AAC non elaborato o ADTS AAC.</span><span class="sxs-lookup"><span data-stu-id="08f8c-119">Raw AAC or ADTS AAC.</span></span><br/> <span data-ttu-id="08f8c-120">Per questo sottotipo, il tipo di supporto fornisce la frequenza di campionamento e il numero di canali prima dell'applicazione degli strumenti di replica della banda spettrale (SBR) e dello stereo parametrico (PS), se presenti.</span><span class="sxs-lookup"><span data-stu-id="08f8c-120">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="08f8c-121">L'effetto dello strumento SBR consiste nel raddoppiare la frequenza di campionamento decodificata rispetto alla frequenza di campionamento AAC-LC di base.</span><span class="sxs-lookup"><span data-stu-id="08f8c-121">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="08f8c-122">L'effetto dello strumento PS è la decodifica dello stereo da un flusso AAC-LC Core mono-Channel.</span><span class="sxs-lookup"><span data-stu-id="08f8c-122">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span><br/> <span data-ttu-id="08f8c-123">Questo sottotipo è equivalente a **MEDIASUBTYPE_MPEG_HEAAC**, definito in wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="08f8c-123">This subtype is equivalent to **MEDIASUBTYPE_MPEG_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="08f8c-124">Vedere [GUID del sottotipo audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="08f8c-124">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> <br/> <span data-ttu-id="08f8c-125">L' [origine file MPEG-4](mpeg-4-file-source.md) e il parser ADTS restituiscono questo sottotipo.</span><span class="sxs-lookup"><span data-stu-id="08f8c-125">The [MPEG-4 File Source](mpeg-4-file-source.md) and the ADTS Parser output this subtype.</span></span> <br/> | <span data-ttu-id="08f8c-126">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="08f8c-126">mfapi.h</span></span>      |
| <span data-ttu-id="08f8c-127">**MEDIASUBTYPE_RAW_AAC1**</span><span class="sxs-lookup"><span data-stu-id="08f8c-127">**MEDIASUBTYPE_RAW_AAC1**</span></span> | <span data-ttu-id="08f8c-128">AAC non elaborato.</span><span class="sxs-lookup"><span data-stu-id="08f8c-128">Raw AAC.</span></span> <br/> <span data-ttu-id="08f8c-129">Questo sottotipo viene usato per AAC contenuto in un file AVI con tag di formato audio uguale a WAVE_FORMAT_RAW_AAC1 (0x00FF).</span><span class="sxs-lookup"><span data-stu-id="08f8c-129">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE_FORMAT_RAW_AAC1 (0x00FF).</span></span> <br/> <span data-ttu-id="08f8c-130">Per questo sottotipo, il tipo di supporto fornisce la frequenza di campionamento e il numero di canali dopo l'applicazione degli strumenti SBR e PS, se presenti.</span><span class="sxs-lookup"><span data-stu-id="08f8c-130">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="08f8c-131">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="08f8c-131">wmcodecdsp.h</span></span> |



 

<span data-ttu-id="08f8c-132">Per configurare il decodificatore AAC, impostare i seguenti attributi sul tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="08f8c-132">To configure the AAC decoder, set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08f8c-133">Attributo</span><span class="sxs-lookup"><span data-stu-id="08f8c-133">Attribute</span></span></th>
<th><span data-ttu-id="08f8c-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08f8c-134">Description</span></span></th>
<th><span data-ttu-id="08f8c-135">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="08f8c-135">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08f8c-136"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="08f8c-136"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="08f8c-137">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="08f8c-137">Major type.</span></span></td>
<td><span data-ttu-id="08f8c-138">Deve essere <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="08f8c-138">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08f8c-139"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="08f8c-139"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="08f8c-140">Sottotipo audio.</span><span class="sxs-lookup"><span data-stu-id="08f8c-140">Audio subtype.</span></span></td>
<td><span data-ttu-id="08f8c-141">Per informazioni dettagliate, vedere la descrizione precedente.</span><span class="sxs-lookup"><span data-stu-id="08f8c-141">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08f8c-142"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="08f8c-142"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="08f8c-143">Profilo audio e livello.</span><span class="sxs-lookup"><span data-stu-id="08f8c-143">Audio profile and level.</span></span> <br/></td>
<td><span data-ttu-id="08f8c-144">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="08f8c-144">Optional.</span></span> <span data-ttu-id="08f8c-145">Si applica solo ai <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="08f8c-145">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <br/> <span data-ttu-id="08f8c-146">Il valore di questo attributo è il campo <strong>audioProfileLevelIndication</strong> , come definito da ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="08f8c-146">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span> <br/> <span data-ttu-id="08f8c-147">Se è sconosciuto, impostare su zero o 0xFE ( &quot; nessun profilo audio specificato &quot; ).</span><span class="sxs-lookup"><span data-stu-id="08f8c-147">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08f8c-148"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="08f8c-148"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="08f8c-149">Tipo di payload.</span><span class="sxs-lookup"><span data-stu-id="08f8c-149">Payload type.</span></span><br/></td>
<td><span data-ttu-id="08f8c-150">Si applica solo ai <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="08f8c-150">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <span data-ttu-id="08f8c-151">Il decodificatore supporta i tipi di payload seguenti:</span><span class="sxs-lookup"><span data-stu-id="08f8c-151">The decoder supports the following payload types:</span></span> <br/>
<ul>
<li><span data-ttu-id="08f8c-152">0: AAC non elaborato.</span><span class="sxs-lookup"><span data-stu-id="08f8c-152">0: Raw AAC.</span></span> <span data-ttu-id="08f8c-153">Il flusso contiene solo gli elementi raw_data_block (), come definito da MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="08f8c-153">The stream contains raw_data_block() elements only, as defined by MPEG-2.</span></span></li>
<li><span data-ttu-id="08f8c-154">1: ADTS.</span><span class="sxs-lookup"><span data-stu-id="08f8c-154">1: ADTS.</span></span> <span data-ttu-id="08f8c-155">Il flusso contiene un adts_sequence (), come definito da MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="08f8c-155">The stream contains an adts_sequence(), as defined by MPEG-2.</span></span> <span data-ttu-id="08f8c-156">È consentita una sola raw_data_block () per adts_frame ().</span><span class="sxs-lookup"><span data-stu-id="08f8c-156">Only one raw_data_block() per adts_frame() is allowed.</span></span></li>
<li><span data-ttu-id="08f8c-157">3: flusso del trasporto audio con un livello di sincronizzazione (LOAS) e un livello multiplex (LATM).</span><span class="sxs-lookup"><span data-stu-id="08f8c-157">3: Audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span> <span data-ttu-id="08f8c-158">Dei tre tipi di LOAS, è supportato solo <strong>AudioSyncStream</strong> .</span><span class="sxs-lookup"><span data-stu-id="08f8c-158">Of the three types of LOAS, only <strong>AudioSyncStream</strong> is supported.</span></span> <span data-ttu-id="08f8c-159">Il livello multiplex è <strong>AudioMuxElement</strong>, limitato a un solo programma audio e a un livello.</span><span class="sxs-lookup"><span data-stu-id="08f8c-159">The multiplex layer is <strong>AudioMuxElement</strong>, restricted to one audio program and one layer.</span></span></li>
</ul><span data-ttu-id="08f8c-160">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="08f8c-160">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="08f8c-161">Se questo attributo non viene specificato, viene usato il valore predefinito 0, che specifica che il flusso contiene solo elementi raw_data_block.</span><span class="sxs-lookup"><span data-stu-id="08f8c-161">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08f8c-162"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="08f8c-162"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="08f8c-163">Profondità di bit desiderata dell'audio PCM decodificato.</span><span class="sxs-lookup"><span data-stu-id="08f8c-163">Desired bit depth of the decoded PCM audio.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="08f8c-164"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="08f8c-164"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="08f8c-165">Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="08f8c-165">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="08f8c-166">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="08f8c-166">Optional.</span></span> <span data-ttu-id="08f8c-167">Per altre informazioni, vedere <a href="#format-constraints">vincoli di formato</a>.</span><span class="sxs-lookup"><span data-stu-id="08f8c-167">For more information, see <a href="#format-constraints">Format Constraints</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08f8c-168"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="08f8c-168"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="08f8c-169">Numero di canali, incluso il canale LFE (Low Frequency), se presente.</span><span class="sxs-lookup"><span data-stu-id="08f8c-169">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/></td>
<td><span data-ttu-id="08f8c-170">L'interpretazione di questo valore dipende dal sottotipo di supporto, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="08f8c-170">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08f8c-171"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="08f8c-171"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="08f8c-172">Frequenza di campionamento, in campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="08f8c-172">Sample rate, in samples per second.</span></span><br/></td>
<td><span data-ttu-id="08f8c-173">L'interpretazione di questo valore dipende dal sottotipo di supporto, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="08f8c-173">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08f8c-174"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="08f8c-174"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="08f8c-175">Ulteriori informazioni sul formato.</span><span class="sxs-lookup"><span data-stu-id="08f8c-175">Additional format information.</span></span></td>
<td><span data-ttu-id="08f8c-176">Il valore di questo attributo dipende dal sottotipo.</span><span class="sxs-lookup"><span data-stu-id="08f8c-176">The value of this attribute depends on the subtype.</span></span><br/>
<ul>
<li><span data-ttu-id="08f8c-177"><strong>MFAudioFormat_AAC</strong>: contiene la parte della struttura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> visualizzata dopo la struttura <strong>WAVEFORMATEX</strong> (ovvero dopo il membro <strong>wfx</strong> ).</span><span class="sxs-lookup"><span data-stu-id="08f8c-177"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="08f8c-178">Questa operazione è seguita dai dati di AudioSpecificConfig (), definiti da ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="08f8c-178">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="08f8c-179"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contiene i dati AudioSpecificConfig ().</span><span class="sxs-lookup"><span data-stu-id="08f8c-179"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span> <span data-ttu-id="08f8c-180">Devono essere visualizzati i dati. in caso contrario, il decodificatore rifiuterà il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="08f8c-180">This data must appear; otherwise, the decoder will reject the media type.</span></span></li>
</ul>
<span data-ttu-id="08f8c-181">La lunghezza dei dati di AudioSpecificConfig () è di 2 byte per AAC-LC o HE-AAC con segnalazione implicita di SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="08f8c-181">The length of the AudioSpecificConfig() data is 2 bytes for AAC-LC or HE-AAC with implicit signaling of SBR/PS.</span></span> <span data-ttu-id="08f8c-182">È più di 2 byte per HE-AAC con segnalazione esplicita di SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="08f8c-182">It is more than 2 bytes for HE-AAC with explicit signaling of SBR/PS.</span></span><br/> <span data-ttu-id="08f8c-183">Il valore di <strong>audioObjectType</strong> come definito in AudioSpecificConfig () deve essere 2, che indica AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="08f8c-183">The value of <strong>audioObjectType</strong> as defined in AudioSpecificConfig() must be 2, indicating AAC-LC.</span></span> <span data-ttu-id="08f8c-184">Il valore di <strong>extensionAudioObjectType</strong> deve essere 5 per SBR o 29 per PS.</span><span class="sxs-lookup"><span data-stu-id="08f8c-184">The value of <strong>extensionAudioObjectType</strong> must be 5 for SBR or 29 for PS.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a><span data-ttu-id="08f8c-185">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="08f8c-185">Output Types</span></span>

<span data-ttu-id="08f8c-186">Il decodificatore supporta i tipi di output seguenti:</span><span class="sxs-lookup"><span data-stu-id="08f8c-186">The decoder supports the following output types:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08f8c-187">Subtype</span><span class="sxs-lookup"><span data-stu-id="08f8c-187">Subtype</span></span></th>
<th><span data-ttu-id="08f8c-188">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08f8c-188">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08f8c-189"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="08f8c-189"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="08f8c-190">Audio a virgola mobile IEEE.</span><span class="sxs-lookup"><span data-stu-id="08f8c-190">IEEE floating-point audio.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08f8c-191"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="08f8c-191"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="08f8c-192">audio PCM a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="08f8c-192">16-bit PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08f8c-193"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="08f8c-193"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="08f8c-194">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="08f8c-194">Requires Windows 8.</span></span> <br/> <span data-ttu-id="08f8c-195">Questo tipo di output può essere usato per convertire un flusso AAC nel formato LOAS/LATM in formato ADTS.</span><span class="sxs-lookup"><span data-stu-id="08f8c-195">This output type can be used to convert an AAC stream in the LOAS/LATM format to ADTS format.</span></span> <br/> <span data-ttu-id="08f8c-196">Per convertire un flusso LOAS/LATM in un flusso ADTS, impostare il tipo di input su <strong>MFAudioFormat_AAC</strong> con payload di tipo 3 (LOAS).</span><span class="sxs-lookup"><span data-stu-id="08f8c-196">To convert an LOAS/LATM stream to an ADTS stream, set the input type to <strong>MFAudioFormat_AAC</strong> with payload type 3 (LOAS).</span></span> <span data-ttu-id="08f8c-197">Impostare quindi il tipo di output su <strong>MFAudioFormat_AAC</strong> con payload di tipo 1 (ADTS).</span><span class="sxs-lookup"><span data-stu-id="08f8c-197">Then set the output type to <strong>MFAudioFormat_AAC</strong> with payload type 1 (ADTS).</span></span> <span data-ttu-id="08f8c-198">Il decodificatore riformatterà il Conainter senza decodificare il Bitstream.</span><span class="sxs-lookup"><span data-stu-id="08f8c-198">The decoder will reformat the conainter without decoding the bitstream.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="08f8c-199">Il decodificatore non registra <strong>MFAudioFormat_AAC</strong> come tipo di output.</span><span class="sxs-lookup"><span data-stu-id="08f8c-199">The decoder does not register <strong>MFAudioFormat_AAC</strong> as an output type.</span></span> <span data-ttu-id="08f8c-200">Tuttavia, se l'applicazione imposta il tipo di input come descritto, il metodo <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform:: GetOutputAvailableType</strong></a> restituisce <strong>MFAudioFormat_AAC</strong> nell'elenco dei tipi di output disponibili.</span><span class="sxs-lookup"><span data-stu-id="08f8c-200">However, if the application sets the input type as described, the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> method returns <strong>MFAudioFormat_AAC</strong> in the list of available output types.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="08f8c-201">Se il flusso di input contiene più di due canali, il decodificatore AAC fornisce due opzioni per il formato di output:</span><span class="sxs-lookup"><span data-stu-id="08f8c-201">If the input stream contains more than two channels, the AAC decoder provides two options for the output format:</span></span>

-   <span data-ttu-id="08f8c-202">La stessa configurazione del canale del tipo di input.</span><span class="sxs-lookup"><span data-stu-id="08f8c-202">The same channel configuration as the input type.</span></span>
-   <span data-ttu-id="08f8c-203">Riduzioni stereo.</span><span class="sxs-lookup"><span data-stu-id="08f8c-203">Stereo fold-down.</span></span>

## <a name="format-constraints"></a><span data-ttu-id="08f8c-204">Vincoli di formato</span><span class="sxs-lookup"><span data-stu-id="08f8c-204">Format Constraints</span></span>

<span data-ttu-id="08f8c-205">La frequenza di campionamento audio decodificata deve essere una delle seguenti, dopo l'applicazione di SBR (se presente):</span><span class="sxs-lookup"><span data-stu-id="08f8c-205">The decoded audio sampling rate must be one of the following, after SBR is applied (if present):</span></span>

-   <span data-ttu-id="08f8c-206">8 kHz</span><span class="sxs-lookup"><span data-stu-id="08f8c-206">8 kHz</span></span>
-   <span data-ttu-id="08f8c-207">11,025 kHz</span><span class="sxs-lookup"><span data-stu-id="08f8c-207">11.025 kHz</span></span>
-   <span data-ttu-id="08f8c-208">12 kHz</span><span class="sxs-lookup"><span data-stu-id="08f8c-208">12 kHz</span></span>
-   <span data-ttu-id="08f8c-209">16 kHz</span><span class="sxs-lookup"><span data-stu-id="08f8c-209">16 kHz</span></span>
-   <span data-ttu-id="08f8c-210">22,05 kHz</span><span class="sxs-lookup"><span data-stu-id="08f8c-210">22.05 kHz</span></span>
-   <span data-ttu-id="08f8c-211">24 kHz</span><span class="sxs-lookup"><span data-stu-id="08f8c-211">24 kHz</span></span>
-   <span data-ttu-id="08f8c-212">32 kHz</span><span class="sxs-lookup"><span data-stu-id="08f8c-212">32 kHz</span></span>
-   <span data-ttu-id="08f8c-213">44,1 kHz</span><span class="sxs-lookup"><span data-stu-id="08f8c-213">44.1 kHz</span></span>
-   <span data-ttu-id="08f8c-214">48 kHz</span><span class="sxs-lookup"><span data-stu-id="08f8c-214">48 kHz</span></span>

<span data-ttu-id="08f8c-215">Le frequenze di campionamento superiori a 48 kHz non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="08f8c-215">Sampling rates above 48 kHz are not supported.</span></span>

<span data-ttu-id="08f8c-216">Il decodificatore supporta fino a 6 canali audio.</span><span class="sxs-lookup"><span data-stu-id="08f8c-216">The decoder supports up to 6 audio channels.</span></span> <span data-ttu-id="08f8c-217">Per ogni configurazione dell'altoparlante, il decodificatore prevede che gli elementi sintattici AAC siano visualizzati in un determinato ordine.</span><span class="sxs-lookup"><span data-stu-id="08f8c-217">For each speaker configuration, the decoder expects the AAC syntactic elements to appear in a certain order.</span></span> <span data-ttu-id="08f8c-218">Nella tabella seguente sono elencate le configurazioni supportate per i relatori.</span><span class="sxs-lookup"><span data-stu-id="08f8c-218">The following table lists the supported speaker configurations.</span></span> <span data-ttu-id="08f8c-219">Nella terza colonna della tabella sono elencati gli elementi sintattici previsti e il relativo ordine, utilizzando la notazione seguente:</span><span class="sxs-lookup"><span data-stu-id="08f8c-219">The third column of the table lists the expected syntactic elements and their order, using the following notation:</span></span>

-   <span data-ttu-id="08f8c-220"><SCE1>: Il single_channel_element (SCE) associato all'altoparlante del centro anteriore.</span><span class="sxs-lookup"><span data-stu-id="08f8c-220"><SCE1>: The single_channel_element (SCE) associated with the front center speaker.</span></span>
-   <span data-ttu-id="08f8c-221"><SCE2>: SCE associata all'altoparlante back-Center.</span><span class="sxs-lookup"><span data-stu-id="08f8c-221"><SCE2>: The SCE associated with the back center speaker.</span></span>
-   <span data-ttu-id="08f8c-222"><CPE1>: La channel_pair_element (CPE) associata agli altoparlanti anteriori.</span><span class="sxs-lookup"><span data-stu-id="08f8c-222"><CPE1>: The channel_pair_element (CPE) associated with the front speakers.</span></span>
-   <span data-ttu-id="08f8c-223"><CPE2>: CPE associato agli altoparlanti back (o Side)</span><span class="sxs-lookup"><span data-stu-id="08f8c-223"><CPE2>: The CPE associated with the back (or side) speakers</span></span>
-   <span data-ttu-id="08f8c-224"><LFE>: Il lfe_channel_element (LFE).</span><span class="sxs-lookup"><span data-stu-id="08f8c-224"><LFE>: The lfe_channel_element (LFE).</span></span>

<span data-ttu-id="08f8c-225">Per ulteriori informazioni su questi elementi sintattici, vedere ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="08f8c-225">For more information about these syntactic elements, refer to ISO/IEC 13818-7.</span></span>



| <span data-ttu-id="08f8c-226">Configurazione</span><span class="sxs-lookup"><span data-stu-id="08f8c-226">Configuration</span></span>       | <span data-ttu-id="08f8c-227">Maschera di canale</span><span class="sxs-lookup"><span data-stu-id="08f8c-227">Channel Mask</span></span>                                                                                                                                                              | <span data-ttu-id="08f8c-228">Elementi sintattici AAC</span><span class="sxs-lookup"><span data-stu-id="08f8c-228">AAC Syntactic Elements</span></span>                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="08f8c-229">Mono</span><span class="sxs-lookup"><span data-stu-id="08f8c-229">Mono</span></span>                | <span data-ttu-id="08f8c-230">**SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="08f8c-230">**SPEAKER_FRONT_CENTER**</span></span>                                                                                                                                                | <SCE1>                                    |
| <span data-ttu-id="08f8c-231">Stereo o dual mono</span><span class="sxs-lookup"><span data-stu-id="08f8c-231">Stereo or dual mono</span></span> | <span data-ttu-id="08f8c-232">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="08f8c-232">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span></span>                                                                                                                     | <CPE1>                                    |
| <span data-ttu-id="08f8c-233">2/1</span><span class="sxs-lookup"><span data-stu-id="08f8c-233">2/1</span></span>                 | <span data-ttu-id="08f8c-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="08f8c-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span></span>                                                                                        | <CPE1><SCE1>                        |
| <span data-ttu-id="08f8c-235">2/2</span><span class="sxs-lookup"><span data-stu-id="08f8c-235">2/2</span></span>                 | <span data-ttu-id="08f8c-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="08f8c-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                                              | <CPE1><CPE2>                        |
| <span data-ttu-id="08f8c-237">3/0</span><span class="sxs-lookup"><span data-stu-id="08f8c-237">3/0</span></span>                 | <span data-ttu-id="08f8c-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="08f8c-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span></span>                                                                                       | <SCE1><CPE1>                        |
| <span data-ttu-id="08f8c-239">3/1</span><span class="sxs-lookup"><span data-stu-id="08f8c-239">3/1</span></span>                 | <span data-ttu-id="08f8c-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="08f8c-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span></span>                                                          | <SCE1><CPE1><SCE2>            |
| <span data-ttu-id="08f8c-241">3/2</span><span class="sxs-lookup"><span data-stu-id="08f8c-241">3/2</span></span>                 | <span data-ttu-id="08f8c-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="08f8c-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                | <SCE1><CPE1><CPE2>            |
| <span data-ttu-id="08f8c-243">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="08f8c-243">3/2 + LFE</span></span>           | <span data-ttu-id="08f8c-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="08f8c-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span> | <SCE1><CPE1><CPE2><LFE> |



 

<span data-ttu-id="08f8c-245">Per i dati AAC non elaborati, ogni esempio di input deve contenere esattamente un frame compresso AAC completo.</span><span class="sxs-lookup"><span data-stu-id="08f8c-245">For raw AAC, each input sample must contain exactly one full AAC compressed frame.</span></span>

<span data-ttu-id="08f8c-246">Per ADTS, ogni esempio di input può contenere più frame audio, oltre a frame parziali, i frame possono estendersi sui limiti di esempio.</span><span class="sxs-lookup"><span data-stu-id="08f8c-246">For ADTS, each input sample can contain multiple audio frames, as well as partial frames   that is, frames can span sample boundaries.</span></span> <span data-ttu-id="08f8c-247">Ogni intestazione ADTS deve essere seguita da un frame AAC.</span><span class="sxs-lookup"><span data-stu-id="08f8c-247">Each ADTS header must be followed by one AAC frame.</span></span>

<span data-ttu-id="08f8c-248">Il decodificatore AAC non supporta nessuno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="08f8c-248">The AAC decoder does not support any of the following:</span></span>

-   <span data-ttu-id="08f8c-249">Profilo principale, profilo Sample-Rate scalabile (SRS) o profilo di stima a lungo termine (LTP).</span><span class="sxs-lookup"><span data-stu-id="08f8c-249">Main profile, Sample-Rate Scalable (SRS) profile, or Long Term Prediction (LTP) profile.</span></span>
-   <span data-ttu-id="08f8c-250">Formato di interscambio dati audio (ADIF).</span><span class="sxs-lookup"><span data-stu-id="08f8c-250">Audio data interchange format (ADIF).</span></span>
-   <span data-ttu-id="08f8c-251">Flussi di trasporto LATM/LAOS.</span><span class="sxs-lookup"><span data-stu-id="08f8c-251">LATM/LAOS transport streams.</span></span>
-   <span data-ttu-id="08f8c-252">Elementi del canale di accoppiamento (CCEs).</span><span class="sxs-lookup"><span data-stu-id="08f8c-252">Coupling channel elements (CCEs).</span></span> <span data-ttu-id="08f8c-253">Il decodificatore ignorerà i frame audio con CCEs.</span><span class="sxs-lookup"><span data-stu-id="08f8c-253">The decoder will skip audio frames with CCEs.</span></span>
-   <span data-ttu-id="08f8c-254">AAC-LC con una dimensione del fotogramma 960-Sample.</span><span class="sxs-lookup"><span data-stu-id="08f8c-254">AAC-LC with a 960-sample frame size.</span></span> <span data-ttu-id="08f8c-255">Sono supportati solo i frame 1024-Sample.</span><span class="sxs-lookup"><span data-stu-id="08f8c-255">Only 1024-sample frames are supported.</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="08f8c-256">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="08f8c-256">Transform Attributes</span></span>

<span data-ttu-id="08f8c-257">Il decodificatore AAC implementa il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="08f8c-257">The AAC decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="08f8c-258">Le applicazioni possono utilizzare questo metodo per ottenere o impostare gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="08f8c-258">Applications can use this method to get or set the following attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08f8c-259">Attributo</span><span class="sxs-lookup"><span data-stu-id="08f8c-259">Attribute</span></span></th>
<th><span data-ttu-id="08f8c-260">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08f8c-260">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08f8c-261"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span><span class="sxs-lookup"><span data-stu-id="08f8c-261"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span></span></td>
<td><span data-ttu-id="08f8c-262">Specifica se l'audio a 2 canali è codificato come stereo o doppia mono.</span><span class="sxs-lookup"><span data-stu-id="08f8c-262">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span> <span data-ttu-id="08f8c-263">Considera come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="08f8c-263">Treat as read-only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08f8c-264"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="08f8c-264"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span></span></td>
<td><span data-ttu-id="08f8c-265">Specifica il modo in cui il decodificatore riproduce audio mono doppio.</span><span class="sxs-lookup"><span data-stu-id="08f8c-265">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="08f8c-266">Il valore predefinito è <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: output CH1 sugli altoparlanti sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="08f8c-266">The default value is <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Output Ch1 to the left and right speakers.</span></span> <br/> <span data-ttu-id="08f8c-267">Le applicazioni possono impostare questa proprietà per modificare il comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="08f8c-267">Applications can set this property to change the default behavior.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08f8c-268"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="08f8c-268"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="08f8c-269">Il decodificatore AAC non gestisce le modifiche del formato dinamico e deve essere svuotato o svuotato prima che venga impostato un nuovo tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="08f8c-269">The AAC decoder does not handle dynamic format changes, and must be flushed or drained before a new input media type is set.</span></span> <span data-ttu-id="08f8c-270">Considerare questo attributo come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="08f8c-270">Treat this attribute as read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="08f8c-271">Il decodificatore AAC segnala erroneamente un valore <strong>true</strong> per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="08f8c-271">The AAC decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="08f8c-272">In Windows 7, il decodificatore segnala erroneamente il valore <strong>true</strong> per l'attributo.</span><span class="sxs-lookup"><span data-stu-id="08f8c-272">In Windows 7, the decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span> <span data-ttu-id="08f8c-273">In Windows 8, il decodificatore segnala <strong>false</strong>, ovvero il valore corretto</span><span class="sxs-lookup"><span data-stu-id="08f8c-273">In Windows 8, the decoder reports <strong>FALSE</strong>, which is the correct value</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a><span data-ttu-id="08f8c-274">Tipi di supporti di esempio</span><span class="sxs-lookup"><span data-stu-id="08f8c-274">Example Media Types</span></span>

<span data-ttu-id="08f8c-275">Di seguito è riportato un esempio del tipo di supporto di input necessario per un flusso AAC-LC a 6 canali, 48-kHz, usando un payload AAC non elaborato:</span><span class="sxs-lookup"><span data-stu-id="08f8c-275">Here is an example of the input media type needed for a 6-channel, 48-kHz AAC-LC stream, using a raw AAC payload:</span></span>



| <span data-ttu-id="08f8c-276">Attributo</span><span class="sxs-lookup"><span data-stu-id="08f8c-276">Attribute</span></span>                                                                                      | <span data-ttu-id="08f8c-277">Valore</span><span class="sxs-lookup"><span data-stu-id="08f8c-277">Value</span></span>                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="08f8c-278">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="08f8c-278">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="08f8c-279">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="08f8c-279">**MFMediaType_Audio**</span></span>                                                               |
| [<span data-ttu-id="08f8c-280">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="08f8c-280">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="08f8c-281">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="08f8c-281">**MFAudioFormat_AAC**</span></span>                                                               |
| [<span data-ttu-id="08f8c-282">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="08f8c-282">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="08f8c-283">48000</span><span class="sxs-lookup"><span data-stu-id="08f8c-283">48000</span></span>                                                                                |
| [<span data-ttu-id="08f8c-284">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="08f8c-284">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="08f8c-285">6</span><span class="sxs-lookup"><span data-stu-id="08f8c-285">6</span></span>                                                                                    |
| [<span data-ttu-id="08f8c-286">MF_MT_AAC_PAYLOAD_TYPE</span><span class="sxs-lookup"><span data-stu-id="08f8c-286">MF_MT_AAC_PAYLOAD_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="08f8c-287">0</span><span class="sxs-lookup"><span data-stu-id="08f8c-287">0</span></span>                                                                                    |
| [<span data-ttu-id="08f8c-288">**MF_MT_USER_DATA**</span><span class="sxs-lookup"><span data-stu-id="08f8c-288">**MF_MT_USER_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="08f8c-289">{0x00, 0x00, 0x2A, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0XB0}</span><span class="sxs-lookup"><span data-stu-id="08f8c-289">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span></span> |
| [<span data-ttu-id="08f8c-290">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span><span class="sxs-lookup"><span data-stu-id="08f8c-290">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="08f8c-291">0x2A (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="08f8c-291">0x2a (optional)</span></span>                                                                      |



 

<span data-ttu-id="08f8c-292">I primi 12 byte di [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) corrispondono ai seguenti membri della struttura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) :</span><span class="sxs-lookup"><span data-stu-id="08f8c-292">The first 12 bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspond to the following [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure members:</span></span>

-   <span data-ttu-id="08f8c-293">**wPayloadType** = 0 (AAC non elaborato)</span><span class="sxs-lookup"><span data-stu-id="08f8c-293">**wPayloadType** = 0 (raw AAC)</span></span>
-   <span data-ttu-id="08f8c-294">**wAudioProfileLevelIndication** = 0X2a (profilo AAC, livello 4)</span><span class="sxs-lookup"><span data-stu-id="08f8c-294">**wAudioProfileLevelIndication** = 0x2a (AAC Profile, Level 4)</span></span>
-   <span data-ttu-id="08f8c-295">**wStructType** = 0</span><span class="sxs-lookup"><span data-stu-id="08f8c-295">**wStructType** = 0</span></span>

<span data-ttu-id="08f8c-296">Gli ultimi due byte di [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contengono il valore di AudioSpecificConfig (), come definito da MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="08f8c-296">The last two bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contain the value of AudioSpecificConfig(), as defined by MPEG-4.</span></span>

-   <span data-ttu-id="08f8c-297">AudioSpecificConfig. audioObjectType = 2 (AAC LC) (5 bit)</span><span class="sxs-lookup"><span data-stu-id="08f8c-297">AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 bits)</span></span>
-   <span data-ttu-id="08f8c-298">AudioSpecificConfig. samplingFrequencyIndex = 3 (4 bit)</span><span class="sxs-lookup"><span data-stu-id="08f8c-298">AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bits)</span></span>
-   <span data-ttu-id="08f8c-299">AudioSpecificConfig. channelConfiguration = 6 (4 bit)</span><span class="sxs-lookup"><span data-stu-id="08f8c-299">AudioSpecificConfig.channelConfiguration = 6 (4 bits)</span></span>
-   <span data-ttu-id="08f8c-300">GASpecificConfig. frameLengthFlag = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="08f8c-300">GASpecificConfig.frameLengthFlag = 0 (1 bit)</span></span>
-   <span data-ttu-id="08f8c-301">GASpecificConfig. dependsOnCoreCoder = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="08f8c-301">GASpecificConfig.dependsOnCoreCoder = 0 (1 bit)</span></span>
-   <span data-ttu-id="08f8c-302">GASpecificConfig. extensionFlag = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="08f8c-302">GASpecificConfig.extensionFlag = 0 (1 bit)</span></span>

<span data-ttu-id="08f8c-303">Dato questo tipo di input, usare il seguente tipo di supporto di output per ottenere audio PCM a virgola mobile a 6 canali a 32 bit dal decodificatore:</span><span class="sxs-lookup"><span data-stu-id="08f8c-303">Given this input type, use the following output media type to get 6-channel, 32-bit floating point PCM audio from the decoder:</span></span>



| <span data-ttu-id="08f8c-304">Attributo</span><span class="sxs-lookup"><span data-stu-id="08f8c-304">Attribute</span></span>                                                                                    | <span data-ttu-id="08f8c-305">Valore</span><span class="sxs-lookup"><span data-stu-id="08f8c-305">Value</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [<span data-ttu-id="08f8c-306">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="08f8c-306">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="08f8c-307">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="08f8c-307">**MFMediaType_Audio**</span></span>   |
| [<span data-ttu-id="08f8c-308">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="08f8c-308">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="08f8c-309">**MFAudioFormat_Float**</span><span class="sxs-lookup"><span data-stu-id="08f8c-309">**MFAudioFormat_Float**</span></span> |
| [<span data-ttu-id="08f8c-310">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span><span class="sxs-lookup"><span data-stu-id="08f8c-310">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="08f8c-311">32</span><span class="sxs-lookup"><span data-stu-id="08f8c-311">32</span></span>                       |
| [<span data-ttu-id="08f8c-312">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="08f8c-312">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="08f8c-313">48000</span><span class="sxs-lookup"><span data-stu-id="08f8c-313">48000</span></span>                    |
| [<span data-ttu-id="08f8c-314">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="08f8c-314">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="08f8c-315">6</span><span class="sxs-lookup"><span data-stu-id="08f8c-315">6</span></span>                        |
| [<span data-ttu-id="08f8c-316">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="08f8c-316">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="08f8c-317">1152000 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="08f8c-317">1152000 (optional)</span></span>       |
| [<span data-ttu-id="08f8c-318">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span><span class="sxs-lookup"><span data-stu-id="08f8c-318">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="08f8c-319">24 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="08f8c-319">24 (optional)</span></span>            |
| [<span data-ttu-id="08f8c-320">**MF_MT_AUDIO_CHANNEL_MASK**</span><span class="sxs-lookup"><span data-stu-id="08f8c-320">**MF_MT_AUDIO_CHANNEL_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                   | <span data-ttu-id="08f8c-321">0x3F (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="08f8c-321">0x3f (optional)</span></span>          |



 

<span data-ttu-id="08f8c-322">Se è installato il supplemento di aggiornamento della piattaforma per Windows Vista, il decodificatore audio AAC è disponibile in Windows Vista, ma è accessibile solo in Windows Vista tramite il [lettore di origine](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="08f8c-322">If Platform Update Supplement for Windows Vista is installed, the AAC audio decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="08f8c-323">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08f8c-323">Requirements</span></span>



| <span data-ttu-id="08f8c-324">Requisito</span><span class="sxs-lookup"><span data-stu-id="08f8c-324">Requirement</span></span> | <span data-ttu-id="08f8c-325">Valore</span><span class="sxs-lookup"><span data-stu-id="08f8c-325">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08f8c-326">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08f8c-326">Minimum supported client</span></span><br/> | <span data-ttu-id="08f8c-327">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="08f8c-327">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="08f8c-328">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08f8c-328">Minimum supported server</span></span><br/> | <span data-ttu-id="08f8c-329">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="08f8c-329">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="08f8c-330">DLL</span><span class="sxs-lookup"><span data-stu-id="08f8c-330">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08f8c-331"><dt>Msmpeg2adec.dll su Windows 7; </dt> <dt>MSAudDecMFT.dll in Windows 8</dt></span><span class="sxs-lookup"><span data-stu-id="08f8c-331"><dt>Msmpeg2adec.dll on Windows 7; </dt> <dt>MSAudDecMFT.dll on Windows 8</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08f8c-332">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08f8c-332">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f8c-333">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="08f8c-333">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="08f8c-334">Tipi di supporti AAC</span><span class="sxs-lookup"><span data-stu-id="08f8c-334">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="08f8c-335">Tipi di supporti audio</span><span class="sxs-lookup"><span data-stu-id="08f8c-335">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="08f8c-336">**Decoder audio Microsoft MPEG-1/gg/AAC**</span><span class="sxs-lookup"><span data-stu-id="08f8c-336">**Microsoft MPEG-1/DD/AAC Audio Decoder**</span></span>](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[<span data-ttu-id="08f8c-337">Supporto MPEG-4 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08f8c-337">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="08f8c-338">Formati multimediali supportati in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08f8c-338">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>
