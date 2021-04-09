---
description: In questo argomento viene descritto come specificare il formato di un flusso AAC (Advanced Audio Coding) in Media Foundation.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: Tipi di supporti AAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95423b26a0e2a327b599011e88a05ab2ab58c5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968849"
---
# <a name="aac-media-types"></a><span data-ttu-id="582d3-103">Tipi di supporti AAC</span><span class="sxs-lookup"><span data-stu-id="582d3-103">AAC Media Types</span></span>

<span data-ttu-id="582d3-104">In questo argomento viene descritto come specificare il formato di un flusso AAC (Advanced Audio Coding) in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="582d3-104">This topic describes how to specify the format of an Advanced Audio Coding (AAC) stream in Media Foundation.</span></span>

<span data-ttu-id="582d3-105">Per audio AAC sono definiti due sottotipi:</span><span class="sxs-lookup"><span data-stu-id="582d3-105">Two subtypes are defined for AAC audio:</span></span>



| <span data-ttu-id="582d3-106">Subtype</span><span class="sxs-lookup"><span data-stu-id="582d3-106">Subtype</span></span>                     | <span data-ttu-id="582d3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="582d3-107">Description</span></span>          | <span data-ttu-id="582d3-108">Intestazione</span><span class="sxs-lookup"><span data-stu-id="582d3-108">Header</span></span>       |
|-----------------------------|----------------------|--------------|
| <span data-ttu-id="582d3-109">**MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="582d3-109">**MFAudioFormat\_AAC**</span></span>      | <span data-ttu-id="582d3-110">AAC non elaborato o ADTS AAC.</span><span class="sxs-lookup"><span data-stu-id="582d3-110">Raw AAC or ADTS AAC.</span></span> | <span data-ttu-id="582d3-111">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="582d3-111">mfapi.h</span></span>      |
| <span data-ttu-id="582d3-112">**MEDIASUBTYPE \_ RAW \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="582d3-112">**MEDIASUBTYPE\_RAW\_AAC1**</span></span> | <span data-ttu-id="582d3-113">AAC non elaborato.</span><span class="sxs-lookup"><span data-stu-id="582d3-113">Raw AAC.</span></span>             | <span data-ttu-id="582d3-114">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="582d3-114">wmcodecdsp.h</span></span> |



 

<dl> <dt>

<span data-ttu-id="582d3-115"><span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat \_ AAC</span><span class="sxs-lookup"><span data-stu-id="582d3-115"><span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat\_AAC</span></span>
</dt> <dd>

<span data-ttu-id="582d3-116">Per questo sottotipo, il tipo di supporto fornisce la frequenza di campionamento e il numero di canali prima dell'applicazione degli strumenti di replica della banda spettrale (SBR) e dello stereo parametrico (PS), se presenti.</span><span class="sxs-lookup"><span data-stu-id="582d3-116">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="582d3-117">L'effetto dello strumento SBR consiste nel raddoppiare la frequenza di campionamento decodificata rispetto alla frequenza di campionamento AAC-LC di base.</span><span class="sxs-lookup"><span data-stu-id="582d3-117">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="582d3-118">L'effetto dello strumento PS è la decodifica dello stereo da un flusso AAC-LC Core mono-Channel.</span><span class="sxs-lookup"><span data-stu-id="582d3-118">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span>

<span data-ttu-id="582d3-119">Questo sottotipo è equivalente a **MEDIASUBTYPE \_ MPEG \_ HEAAC**, definito in wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="582d3-119">This subtype is equivalent to **MEDIASUBTYPE\_MPEG\_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="582d3-120">Vedere [GUID del sottotipo audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="582d3-120">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="582d3-121"><span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE \_ RAW \_ AAC1</span><span class="sxs-lookup"><span data-stu-id="582d3-121"><span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE\_RAW\_AAC1</span></span>
</dt> <dd>

<span data-ttu-id="582d3-122">Questo sottotipo viene usato per AAC contenuto in un file AVI con il tag di formato audio uguale a WAVE \_ Format \_ RAW \_ AAC1 (0x00FF).</span><span class="sxs-lookup"><span data-stu-id="582d3-122">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE\_FORMAT\_RAW\_AAC1 (0x00FF).</span></span>

<span data-ttu-id="582d3-123">Per questo sottotipo, il tipo di supporto fornisce la frequenza di campionamento e il numero di canali dopo l'applicazione degli strumenti SBR e PS, se presenti.</span><span class="sxs-lookup"><span data-stu-id="582d3-123">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span>

</dd> </dl>

<span data-ttu-id="582d3-124">Gli attributi del tipo di supporto seguenti si applicano all'audio AAC.</span><span class="sxs-lookup"><span data-stu-id="582d3-124">The following media type attributes apply to AAC audio.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="582d3-125">Attributo</span><span class="sxs-lookup"><span data-stu-id="582d3-125">Attribute</span></span></th>
<th><span data-ttu-id="582d3-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="582d3-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="582d3-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="582d3-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="582d3-128">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="582d3-128">Major type.</span></span> <span data-ttu-id="582d3-129">Deve essere <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="582d3-129">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="582d3-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="582d3-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="582d3-131">Sottotipo audio.</span><span class="sxs-lookup"><span data-stu-id="582d3-131">Audio subtype.</span></span> <span data-ttu-id="582d3-132">Per informazioni dettagliate, vedere la descrizione precedente.</span><span class="sxs-lookup"><span data-stu-id="582d3-132">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="582d3-133"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="582d3-133"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="582d3-134">Profilo audio e livello.</span><span class="sxs-lookup"><span data-stu-id="582d3-134">Audio profile and level.</span></span> <br/> <span data-ttu-id="582d3-135">Il valore di questo attributo è il campo <strong>audioProfileLevelIndication</strong> , come definito da ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="582d3-135">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span><br/> <span data-ttu-id="582d3-136">Se è sconosciuto, impostare su zero o 0xFE ( &quot; nessun profilo audio specificato &quot; ).</span><span class="sxs-lookup"><span data-stu-id="582d3-136">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="582d3-137"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="582d3-137"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="582d3-138">Velocità in bit del flusso AAC codificato, in byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="582d3-138">Bit rate of the encoded AAC stream, in bytes per second.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="582d3-139"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="582d3-139"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="582d3-140">Tipo di payload.</span><span class="sxs-lookup"><span data-stu-id="582d3-140">Payload type.</span></span><br/> <span data-ttu-id="582d3-141">Si applica solo ai <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="582d3-141">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span><br/> <span data-ttu-id="582d3-142"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="582d3-142"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="582d3-143">Se questo attributo non viene specificato, viene usato il valore predefinito 0, che specifica che il flusso contiene solo elementi raw_data_block.</span><span class="sxs-lookup"><span data-stu-id="582d3-143">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="582d3-144"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="582d3-144"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="582d3-145">Profondità di bit dell'audio PCM decodificato.</span><span class="sxs-lookup"><span data-stu-id="582d3-145">Bit depth of the decoded PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="582d3-146"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="582d3-146"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="582d3-147">Assegnazione dei canali audio alle posizioni degli oratori.</span><span class="sxs-lookup"><span data-stu-id="582d3-147">Assignment of audio channels to speaker positions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="582d3-148"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="582d3-148"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="582d3-149">Numero di canali, incluso il canale LFE (Low Frequency), se presente.</span><span class="sxs-lookup"><span data-stu-id="582d3-149">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/> <span data-ttu-id="582d3-150">L'interpretazione di questo valore dipende dal sottotipo di supporto, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="582d3-150">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="582d3-151"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="582d3-151"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="582d3-152">Frequenza di campionamento, in campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="582d3-152">Sample rate, in samples per second.</span></span><br/> <span data-ttu-id="582d3-153">L'interpretazione di questo valore dipende dal sottotipo di supporto, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="582d3-153">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="582d3-154"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="582d3-154"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="582d3-155">Il valore di questo attributo dipende dal sottotipo:</span><span class="sxs-lookup"><span data-stu-id="582d3-155">The value of this attribute depends on the subtype:</span></span><br/>
<ul>
<li><span data-ttu-id="582d3-156"><strong>MFAudioFormat_AAC</strong>: contiene la parte della struttura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> visualizzata dopo la struttura <strong>WAVEFORMATEX</strong> (ovvero dopo il membro <strong>wfx</strong> ).</span><span class="sxs-lookup"><span data-stu-id="582d3-156"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="582d3-157">Questa operazione è seguita dai dati di AudioSpecificConfig (), definiti da ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="582d3-157">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="582d3-158"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contiene i dati AudioSpecificConfig ().</span><span class="sxs-lookup"><span data-stu-id="582d3-158"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="582d3-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="582d3-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="582d3-160">Tipi di supporti audio</span><span class="sxs-lookup"><span data-stu-id="582d3-160">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="582d3-161">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="582d3-161">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="582d3-162">Supporto MPEG-4 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="582d3-162">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="582d3-163">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="582d3-163">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

