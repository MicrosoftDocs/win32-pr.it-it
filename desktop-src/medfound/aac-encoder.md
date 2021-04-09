---
description: Il codificatore Microsoft Media Foundation AAC è una trasformazione di Media Foundation che codifica il profilo Advanced Audio Coding (AAC) Low Complexity (LC), come definito da ISO/IEC 13818-7 (MPEG-2 audio Part 7).
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: Codificatore AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec9730ffc17d7ac3d5e16d86ef5aa20a46b329cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879401"
---
# <a name="aac-encoder"></a><span data-ttu-id="18af2-103">Codificatore AAC</span><span class="sxs-lookup"><span data-stu-id="18af2-103">AAC Encoder</span></span>

<span data-ttu-id="18af2-104">Il codificatore Microsoft Media Foundation AAC è una [trasformazione di Media Foundation](media-foundation-transforms.md) che codifica il profilo Advanced Audio Coding (AAC) Low Complexity (LC), come definito da ISO/IEC 13818-7 (MPEG-2 audio Part 7).</span><span class="sxs-lookup"><span data-stu-id="18af2-104">The Microsoft Media Foundation AAC encoder is a [Media Foundation Transform](media-foundation-transforms.md) that encodes Advanced Audio Coding (AAC) Low Complexity (LC) profile, as defined by ISO/IEC 13818-7 (MPEG-2 Audio Part 7) .</span></span>

<span data-ttu-id="18af2-105">Il codificatore AAC non supporta la codifica in altri profili AAC, ad esempio Main, SSR o LTP.</span><span class="sxs-lookup"><span data-stu-id="18af2-105">The AAC encoder does not support encoding to any other AAC profiles, such as Main, SSR, or LTP.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="18af2-106">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="18af2-106">Class Identifier</span></span>

<span data-ttu-id="18af2-107">L'identificatore di classe (CLSID) del codificatore AAC è **CLSID \_ AACMFTEncoder**, definito nel file di intestazione wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="18af2-107">The class identifier (CLSID) of the AAC encoder is **CLSID\_AACMFTEncoder**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="18af2-108">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="18af2-108">Media Types</span></span>

<span data-ttu-id="18af2-109">Il codificatore AAC supporta i seguenti tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="18af2-109">The AAC encoder supports the following media types.</span></span> <span data-ttu-id="18af2-110">È possibile impostare prima i tipi in base al tipo di input dell'ordine o al tipo di output.</span><span class="sxs-lookup"><span data-stu-id="18af2-110">You can set the types in either order input type first, or output type first.</span></span>

### <a name="input-types"></a><span data-ttu-id="18af2-111">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="18af2-111">Input Types</span></span>

<span data-ttu-id="18af2-112">Impostare gli attributi seguenti sul tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="18af2-112">Set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18af2-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="18af2-113">Attribute</span></span></th>
<th><span data-ttu-id="18af2-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18af2-114">Description</span></span></th>
<th><span data-ttu-id="18af2-115">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="18af2-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="18af2-116"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="18af2-116"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="18af2-117">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="18af2-117">Major type.</span></span></td>
<td><span data-ttu-id="18af2-118">Deve essere <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="18af2-118">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18af2-119"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="18af2-119"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="18af2-120">Sottotipo.</span><span class="sxs-lookup"><span data-stu-id="18af2-120">Subtype.</span></span></td>
<td><span data-ttu-id="18af2-121">Deve essere <strong>MFAudioFormat_PCM</strong>.</span><span class="sxs-lookup"><span data-stu-id="18af2-121">Must be <strong>MFAudioFormat_PCM</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18af2-122"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="18af2-122"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="18af2-123">BITS per campione.</span><span class="sxs-lookup"><span data-stu-id="18af2-123">Bits per sample.</span></span></td>
<td><span data-ttu-id="18af2-124">Deve essere 16.</span><span class="sxs-lookup"><span data-stu-id="18af2-124">Must be 16.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18af2-125"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="18af2-125"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="18af2-126">Campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="18af2-126">Samples per second.</span></span></td>
<td><span data-ttu-id="18af2-127">Sono supportati i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="18af2-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="18af2-128">44100 (44,1 KHz)</span><span class="sxs-lookup"><span data-stu-id="18af2-128">44100 (44.1 KHz)</span></span></li>
<li><span data-ttu-id="18af2-129">48000 (48 KHz)</span><span class="sxs-lookup"><span data-stu-id="18af2-129">48000 (48 KHz)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18af2-130"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="18af2-130"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="18af2-131">Numero di canali.</span><span class="sxs-lookup"><span data-stu-id="18af2-131">Number of channels.</span></span></td>
<td><span data-ttu-id="18af2-132">Deve essere 1 (mono) o 2 (stereo) o 6 (5,1).</span><span class="sxs-lookup"><span data-stu-id="18af2-132">Must be 1 (mono) or 2 (stereo), or 6 (5.1).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="18af2-133">Il supporto per 6 canali audio è stato introdotto con Windows 10 e non è disponibile per le versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="18af2-133">Support for 6 audio channels was introduced with Windows 10 and is not available for earlier versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="18af2-134">Dopo aver impostato il tipo di input, il codificatore deriva i valori seguenti e li aggiunge al tipo di supporto:</span><span class="sxs-lookup"><span data-stu-id="18af2-134">After the input type is set, the encoder derives the following values and adds them to the media type:</span></span>

-   [<span data-ttu-id="18af2-135">**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="18af2-135">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [<span data-ttu-id="18af2-136">**\_ \_ \_ allineamento blocchi audio MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="18af2-136">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)
-   [<span data-ttu-id="18af2-137">**\_velocità in \_ bit media MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="18af2-137">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a><span data-ttu-id="18af2-138">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="18af2-138">Output Types</span></span>

<span data-ttu-id="18af2-139">Impostare gli attributi seguenti sul tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="18af2-139">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18af2-140">Attributo</span><span class="sxs-lookup"><span data-stu-id="18af2-140">Attribute</span></span></th>
<th><span data-ttu-id="18af2-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18af2-141">Description</span></span></th>
<th><span data-ttu-id="18af2-142">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="18af2-142">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="18af2-143"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="18af2-143"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="18af2-144">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="18af2-144">Major type.</span></span></td>
<td><span data-ttu-id="18af2-145">Deve essere <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="18af2-145">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18af2-146"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="18af2-146"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="18af2-147">Sottotipo audio.</span><span class="sxs-lookup"><span data-stu-id="18af2-147">Audio subtype.</span></span></td>
<td><span data-ttu-id="18af2-148">Deve essere <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="18af2-148">Must be <strong>MFAudioFormat_AAC</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18af2-149"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="18af2-149"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="18af2-150">BITS per campione.</span><span class="sxs-lookup"><span data-stu-id="18af2-150">Bits per sample.</span></span></td>
<td><span data-ttu-id="18af2-151">Deve essere 16.</span><span class="sxs-lookup"><span data-stu-id="18af2-151">Must be 16.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18af2-152"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="18af2-152"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="18af2-153">Campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="18af2-153">Samples per second.</span></span></td>
<td><span data-ttu-id="18af2-154">Deve corrispondere al tipo di input.</span><span class="sxs-lookup"><span data-stu-id="18af2-154">Must match the input type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18af2-155"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="18af2-155"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="18af2-156">Numero di canali.</span><span class="sxs-lookup"><span data-stu-id="18af2-156">Number of channels.</span></span></td>
<td><span data-ttu-id="18af2-157">Deve corrispondere al tipo di input.</span><span class="sxs-lookup"><span data-stu-id="18af2-157">Must match the input type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18af2-158"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="18af2-158"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="18af2-159">Velocità in bit del flusso AAC codificato, in byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="18af2-159">Bit rate of the encoded AAC stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="18af2-160">Sono supportati i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="18af2-160">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="18af2-161">12000</span><span class="sxs-lookup"><span data-stu-id="18af2-161">12000</span></span></li>
<li><span data-ttu-id="18af2-162">16000</span><span class="sxs-lookup"><span data-stu-id="18af2-162">16000</span></span></li>
<li><span data-ttu-id="18af2-163">20000</span><span class="sxs-lookup"><span data-stu-id="18af2-163">20000</span></span></li>
<li><span data-ttu-id="18af2-164">24000</span><span class="sxs-lookup"><span data-stu-id="18af2-164">24000</span></span></li>
</ul>
<span data-ttu-id="18af2-165">Il valore predefinito per mono e stereo è 12000 (96 Kbps).</span><span class="sxs-lookup"><span data-stu-id="18af2-165">The default value for both mono and stereo is 12000 (96 Kbps).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18af2-166"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="18af2-166"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="18af2-167">Tipo di payload AAC.</span><span class="sxs-lookup"><span data-stu-id="18af2-167">The AAC payload type.</span></span></td>
<td><span data-ttu-id="18af2-168">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="18af2-168">Optional.</span></span> <span data-ttu-id="18af2-169">Se impostato, il valore deve essere zero, a indicare che il flusso contiene solo raw_data_block elementi.</span><span class="sxs-lookup"><span data-stu-id="18af2-169">If set, the value must be zero, indicating that the stream contains raw_data_block elements only.</span></span><br/> <span data-ttu-id="18af2-170">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="18af2-170">Optional.</span></span> <span data-ttu-id="18af2-171">Se l'attributo non è impostato, il valore predefinito è zero, che indica che il flusso contiene solo raw_data_block elementi (AAC non elaborato).</span><span class="sxs-lookup"><span data-stu-id="18af2-171">If the attribute is not set, the default value is zero, indicating that the stream contains raw_data_block elements only (raw AAC).</span></span> <br/> <span data-ttu-id="18af2-172">In Windows 7, se l'attributo è impostato, il valore deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="18af2-172">In Windows 7, if this attribute is set, the value must be zero.</span></span><br/> <span data-ttu-id="18af2-173">A partire da Windows 8, il valore può essere 0 (AAC non elaborato) o 1 (ADTS AAC).</span><span class="sxs-lookup"><span data-stu-id="18af2-173">Starting in Windows 8, the value can be 0 (raw AAC) or 1 (ADTS AAC).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18af2-174"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="18af2-174"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="18af2-175">Il profilo audio AAC e il livello.</span><span class="sxs-lookup"><span data-stu-id="18af2-175">The AAC audio profile and level.</span></span></td>
<td><span data-ttu-id="18af2-176">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="18af2-176">Optional.</span></span> <span data-ttu-id="18af2-177">Sono supportati i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="18af2-177">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="18af2-178">0x29 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18af2-178">0x29 (default)</span></span></li>
<li><span data-ttu-id="18af2-179">0x2A</span><span class="sxs-lookup"><span data-stu-id="18af2-179">0x2A</span></span></li>
<li><span data-ttu-id="18af2-180">0x2B</span><span class="sxs-lookup"><span data-stu-id="18af2-180">0x2B</span></span></li>
<li><span data-ttu-id="18af2-181">0x2C</span><span class="sxs-lookup"><span data-stu-id="18af2-181">0x2C</span></span></li>
<li><span data-ttu-id="18af2-182">0x2E</span><span class="sxs-lookup"><span data-stu-id="18af2-182">0x2E</span></span></li>
<li><span data-ttu-id="18af2-183">0x2F</span><span class="sxs-lookup"><span data-stu-id="18af2-183">0x2F</span></span></li>
<li><span data-ttu-id="18af2-184">0x30</span><span class="sxs-lookup"><span data-stu-id="18af2-184">0x30</span></span></li>
<li><span data-ttu-id="18af2-185">0x31</span><span class="sxs-lookup"><span data-stu-id="18af2-185">0x31</span></span></li>
<li><span data-ttu-id="18af2-186">0x32</span><span class="sxs-lookup"><span data-stu-id="18af2-186">0x32</span></span></li>
<li><span data-ttu-id="18af2-187">0x33</span><span class="sxs-lookup"><span data-stu-id="18af2-187">0x33</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="18af2-188">Nella tabella seguente sono elencati i valori che è possibile utilizzare per l'attributo MF_MT_AAC_PROFILE_LEVEL_INDICATION.</span><span class="sxs-lookup"><span data-stu-id="18af2-188">The following table lists the values that can be used for the MF_MT_AAC_PROFILE_LEVEL_INDICATION attribute.</span></span>

| <span data-ttu-id="18af2-189">Valore MF_MT_AAC_PROFILE_LEVEL_INDICATION</span><span class="sxs-lookup"><span data-stu-id="18af2-189">MF_MT_AAC_PROFILE_LEVEL_INDICATION value</span></span> | <span data-ttu-id="18af2-190">Profilo</span><span class="sxs-lookup"><span data-stu-id="18af2-190">Profile</span></span>                           |
|------------------------------------------|-----------------------------------|
| <span data-ttu-id="18af2-191">0x29</span><span class="sxs-lookup"><span data-stu-id="18af2-191">0x29</span></span>                                     | <span data-ttu-id="18af2-192">Profilo AAC L2</span><span class="sxs-lookup"><span data-stu-id="18af2-192">AAC Profile L2</span></span>                    | 
| <span data-ttu-id="18af2-193">0x2A</span><span class="sxs-lookup"><span data-stu-id="18af2-193">0x2A</span></span>                                     | <span data-ttu-id="18af2-194">Profilo AAC L4</span><span class="sxs-lookup"><span data-stu-id="18af2-194">AAC Profile L4</span></span>                    | 
| <span data-ttu-id="18af2-195">0x2B</span><span class="sxs-lookup"><span data-stu-id="18af2-195">0x2B</span></span>                                     | <span data-ttu-id="18af2-196">Profilo AAC L5</span><span class="sxs-lookup"><span data-stu-id="18af2-196">AAC Profile L5</span></span>                    | 
| <span data-ttu-id="18af2-197">0x2C</span><span class="sxs-lookup"><span data-stu-id="18af2-197">0x2C</span></span>                                     | <span data-ttu-id="18af2-198">Profilo AAC V1 ad alta efficienza L2</span><span class="sxs-lookup"><span data-stu-id="18af2-198">High Efficiency v1 AAC Profile L2</span></span> | 
| <span data-ttu-id="18af2-199">0x2E</span><span class="sxs-lookup"><span data-stu-id="18af2-199">0x2E</span></span>                                     | <span data-ttu-id="18af2-200">Profilo AAC V1 ad alta efficienza</span><span class="sxs-lookup"><span data-stu-id="18af2-200">High Efficiency v1 AAC Profile L4</span></span> | 
| <span data-ttu-id="18af2-201">0x2F</span><span class="sxs-lookup"><span data-stu-id="18af2-201">0x2F</span></span>                                     | <span data-ttu-id="18af2-202">Profilo AAC ad alta efficienza V1 L5</span><span class="sxs-lookup"><span data-stu-id="18af2-202">High Efficiency v1 AAC Profile L5</span></span> | 
| <span data-ttu-id="18af2-203">0x30</span><span class="sxs-lookup"><span data-stu-id="18af2-203">0x30</span></span>                                     | <span data-ttu-id="18af2-204">Profilo AAC v2 ad alta efficienza L2</span><span class="sxs-lookup"><span data-stu-id="18af2-204">High Efficiency v2 AAC Profile L2</span></span> | 
| <span data-ttu-id="18af2-205">0x31</span><span class="sxs-lookup"><span data-stu-id="18af2-205">0x31</span></span>                                     | <span data-ttu-id="18af2-206">Profilo AAC v2 ad efficienza elevata L3</span><span class="sxs-lookup"><span data-stu-id="18af2-206">High Efficiency v2 AAC Profile L3</span></span> | 
| <span data-ttu-id="18af2-207">0x32</span><span class="sxs-lookup"><span data-stu-id="18af2-207">0x32</span></span>                                     | <span data-ttu-id="18af2-208">Profilo AAC v2 ad alta efficienza</span><span class="sxs-lookup"><span data-stu-id="18af2-208">High Efficiency v2 AAC Profile L4</span></span> | 
| <span data-ttu-id="18af2-209">0x33</span><span class="sxs-lookup"><span data-stu-id="18af2-209">0x33</span></span>                                     | <span data-ttu-id="18af2-210">Profilo AAC v2 ad alta efficienza (L5)</span><span class="sxs-lookup"><span data-stu-id="18af2-210">High Efficiency v2 AAC Profile L5</span></span> | 

 

<span data-ttu-id="18af2-211">Dopo aver impostato il tipo di output, il codificatore AAC aggiorna il tipo aggiungendo l'attributo [**\_ \_ \_ dati utente MF mt**](mf-mt-user-data-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="18af2-211">After the output type is set, the AAC encoder updates the type by adding the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="18af2-212">Questo attributo contiene la parte della struttura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) visualizzata dopo la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) (ovvero dopo il membro **wfx** ).</span><span class="sxs-lookup"><span data-stu-id="18af2-212">This attribute contains the portion of the [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure that appears after the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure (that is, after the **wfx** member).</span></span> <span data-ttu-id="18af2-213">Questa operazione è seguita dai dati di AudioSpecificConfig (), definiti da ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="18af2-213">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span>

<span data-ttu-id="18af2-214">Ogni esempio di output contiene un frame AAC compresso senza intestazione.</span><span class="sxs-lookup"><span data-stu-id="18af2-214">Each output sample contains one compressed AAC frame with no header.</span></span> <span data-ttu-id="18af2-215">Questo formato è equivalente all'elemento del \_ blocco di dati non elaborati \_ () definito da MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="18af2-215">This format is equivalent to the raw\_data\_block() element defined by MPEG-2.</span></span> <span data-ttu-id="18af2-216">L'attributo del [ \_ tipo di payload MF mt \_ AAC \_ \_ ](mf-mt-aac-payload-type.md) , se presente nel tipo di output, deve essere impostato su zero per indicare questo tipo di payload.</span><span class="sxs-lookup"><span data-stu-id="18af2-216">The [MF\_MT\_AAC\_PAYLOAD\_TYPE](mf-mt-aac-payload-type.md) attribute, if present in the output type, must be set to zero to indicate this payload type.</span></span>

<span data-ttu-id="18af2-217">Ogni esempio di output contiene un frame AAC compresso corrispondente a esempi di PCM 1024.</span><span class="sxs-lookup"><span data-stu-id="18af2-217">Each output sample contains one compressed AAC frame corresponding to 1024 PCM samples.</span></span> <span data-ttu-id="18af2-218">Ad esempio, alla frequenza di campionamento di 48 kHz, la durata di un frame compresso è 21,33 msec.</span><span class="sxs-lookup"><span data-stu-id="18af2-218">For example, at 48 Khz sampling rate, the duration of one compressed frame is 21.33 msec.</span></span>

<span data-ttu-id="18af2-219">Se [il \_ \_ tipo di \_ payload \_ MF mt AAC](mf-mt-aac-payload-type.md) è zero (valore predefinito), ogni esempio di output contiene un \_ \_ elemento di blocco di dati non elaborati () come definito da ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="18af2-219">If [MF\_MT\_AAC\_PAYLOAD\_TYPE](mf-mt-aac-payload-type.md) is zero (the default value), each output sample contains one raw\_data\_block() element as defined by ISO/IEC 13818-7.</span></span>

## <a name="example-media-types"></a><span data-ttu-id="18af2-220">Tipi di supporti di esempio</span><span class="sxs-lookup"><span data-stu-id="18af2-220">Example Media Types</span></span>

<span data-ttu-id="18af2-221">Di seguito è riportato un esempio dei tipi di supporti necessari per codificare dall'audio stereo a 44,1 kHz a 160 kbps a AAC non elaborato</span><span class="sxs-lookup"><span data-stu-id="18af2-221">Here is an example of the media types needed to encode from 44.1-kHz, 160-Kbps stereo audio to raw AAC</span></span>

<span data-ttu-id="18af2-222">Tipo di supporto di input:</span><span class="sxs-lookup"><span data-stu-id="18af2-222">Input media type:</span></span>



| <span data-ttu-id="18af2-223">Attributo</span><span class="sxs-lookup"><span data-stu-id="18af2-223">Attribute</span></span>                                                                                    | <span data-ttu-id="18af2-224">Valore</span><span class="sxs-lookup"><span data-stu-id="18af2-224">Value</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="18af2-225">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="18af2-225">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="18af2-226">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="18af2-226">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="18af2-227">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="18af2-227">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="18af2-228">**\_PCM MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="18af2-228">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="18af2-229">**\_ \_ bit audio MF \_ mt \_ per \_ campione**</span><span class="sxs-lookup"><span data-stu-id="18af2-229">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="18af2-230">16</span><span class="sxs-lookup"><span data-stu-id="18af2-230">16</span></span>                     |
| [<span data-ttu-id="18af2-231">**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="18af2-231">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="18af2-232">44100</span><span class="sxs-lookup"><span data-stu-id="18af2-232">44100</span></span>                  |
| [<span data-ttu-id="18af2-233">**numero \_ di \_ \_ canali audio MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="18af2-233">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="18af2-234">2</span><span class="sxs-lookup"><span data-stu-id="18af2-234">2</span></span>                      |
| [<span data-ttu-id="18af2-235">**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="18af2-235">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="18af2-236">176400 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="18af2-236">176400 (optional)</span></span>      |
| [<span data-ttu-id="18af2-237">**\_ \_ \_ allineamento blocchi audio MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="18af2-237">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="18af2-238">4 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="18af2-238">4 (optional)</span></span>           |
| [<span data-ttu-id="18af2-239">**\_ \_ tutti gli esempi MF mt \_ \_ Independent**</span><span class="sxs-lookup"><span data-stu-id="18af2-239">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)         | <span data-ttu-id="18af2-240">1 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="18af2-240">1 (optional)</span></span>           |
| [<span data-ttu-id="18af2-241">**\_velocità in \_ bit media MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="18af2-241">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                  | <span data-ttu-id="18af2-242">1411200 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="18af2-242">1411200 (optional)</span></span>     |
| [<span data-ttu-id="18af2-243">**\_esempi di \_ \_ dimensioni fisse MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="18af2-243">**MF\_MT\_FIXED\_SIZE\_SAMPLES**</span></span>](mf-mt-fixed-size-samples-attribute.md)                   | <span data-ttu-id="18af2-244">1 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="18af2-244">1 (optional)</span></span>           |



 

<span data-ttu-id="18af2-245">Tipo di supporto di output:</span><span class="sxs-lookup"><span data-stu-id="18af2-245">Output media type:</span></span>



| <span data-ttu-id="18af2-246">Attributo</span><span class="sxs-lookup"><span data-stu-id="18af2-246">Attribute</span></span>                                                                                      | <span data-ttu-id="18af2-247">Valore</span><span class="sxs-lookup"><span data-stu-id="18af2-247">Value</span></span>                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18af2-248">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="18af2-248">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="18af2-249">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="18af2-249">**MFMediaType\_Audio**</span></span>                                                                          |
| [<span data-ttu-id="18af2-250">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="18af2-250">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="18af2-251">**MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="18af2-251">**MFAudioFormat\_AAC**</span></span>                                                                          |
| [<span data-ttu-id="18af2-252">**\_ \_ bit audio MF \_ mt \_ per \_ campione**</span><span class="sxs-lookup"><span data-stu-id="18af2-252">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)              | <span data-ttu-id="18af2-253">16</span><span class="sxs-lookup"><span data-stu-id="18af2-253">16</span></span>                                                                                              |
| [<span data-ttu-id="18af2-254">**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="18af2-254">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="18af2-255">44100</span><span class="sxs-lookup"><span data-stu-id="18af2-255">44100</span></span>                                                                                           |
| [<span data-ttu-id="18af2-256">**numero \_ di \_ \_ canali audio MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="18af2-256">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="18af2-257">2</span><span class="sxs-lookup"><span data-stu-id="18af2-257">2</span></span>                                                                                               |
| [<span data-ttu-id="18af2-258">**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="18af2-258">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)   | <span data-ttu-id="18af2-259">20000</span><span class="sxs-lookup"><span data-stu-id="18af2-259">20000</span></span>                                                                                           |
| [<span data-ttu-id="18af2-260">\_tipo di payload MF mt \_ AAC \_ \_</span><span class="sxs-lookup"><span data-stu-id="18af2-260">MF\_MT\_AAC\_PAYLOAD\_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="18af2-261">0 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="18af2-261">0 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="18af2-262">\_ \_ \_ \_ \_ indicazione livello profilo audio MF mt \_ AAC</span><span class="sxs-lookup"><span data-stu-id="18af2-262">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="18af2-263">0x29 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="18af2-263">0x29 (optional)</span></span>                                                                                 |
| [<span data-ttu-id="18af2-264">**\_ \_ \_ allineamento blocchi audio MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="18af2-264">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)               | <span data-ttu-id="18af2-265">1 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="18af2-265">1 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="18af2-266">**\_ \_ tutti gli esempi MF mt \_ \_ Independent**</span><span class="sxs-lookup"><span data-stu-id="18af2-266">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)           | <span data-ttu-id="18af2-267">0 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="18af2-267">0 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="18af2-268">**\_velocità in \_ bit media MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="18af2-268">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                    | <span data-ttu-id="18af2-269">160000 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="18af2-269">160000 (optional)</span></span>                                                                               |
| [<span data-ttu-id="18af2-270">**\_ \_ dati utente MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="18af2-270">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="18af2-271">{0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} opzionale</span><span class="sxs-lookup"><span data-stu-id="18af2-271">{0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} (optional)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="18af2-272">Commenti</span><span class="sxs-lookup"><span data-stu-id="18af2-272">Remarks</span></span>

<span data-ttu-id="18af2-273">Nell'implementazione corrente ogni esempio di input deve avere un'ora e una durata valide.</span><span class="sxs-lookup"><span data-stu-id="18af2-273">In the current implementation, every input sample must have a valid time and duration.</span></span> <span data-ttu-id="18af2-274">Per impostare l'ora di esempio, chiamare [**IMFSample:: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span><span class="sxs-lookup"><span data-stu-id="18af2-274">To set the sample time, call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span></span> <span data-ttu-id="18af2-275">Per impostare la durata del campione, chiamare [**IMFSample:: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span><span class="sxs-lookup"><span data-stu-id="18af2-275">To set the sample duration, call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span></span>

<span data-ttu-id="18af2-276">Se l'ora di esempio non è impostata, il metodo [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) del codificatore restituisce **MF \_ E \_ nessun \_ \_ timestamp di esempio**.</span><span class="sxs-lookup"><span data-stu-id="18af2-276">If the sample time is not set, the encoder's [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method returns **MF\_E\_NO\_SAMPLE\_TIMESTAMP**.</span></span> <span data-ttu-id="18af2-277">Se la durata di esempio non è impostata, il metodo **ProcessInput** restituisce la **\_ durata MF E \_ nessun \_ campione \_**.</span><span class="sxs-lookup"><span data-stu-id="18af2-277">If the sample duration is not set, the **ProcessInput** method returns **MF\_E\_NO\_SAMPLE\_DURATION**.</span></span>

<span data-ttu-id="18af2-278">La durata campione può essere calcolata come segue:</span><span class="sxs-lookup"><span data-stu-id="18af2-278">Sample duration can be calculated as follows:</span></span>


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



<span data-ttu-id="18af2-279">dove *nAudioSamplesPerChannel* è il numero di campioni audio PCM per canale nel buffer di input e *nSamplesPerSec* è la frequenza di campionamento, in campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="18af2-279">where *nAudioSamplesPerChannel* is the number of PCM audio samples per channel in the input buffer, and *nSamplesPerSec* is the sampling rate, in samples per second.</span></span>

> [!Note]  
> <span data-ttu-id="18af2-280">A causa di un bug nell'implementazione corrente, se la durata dell'esempio è impostata su zero, la chiamata a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ha esito positivo, ma una chiamata successiva a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) genererà un'eccezione di divisione per zero.</span><span class="sxs-lookup"><span data-stu-id="18af2-280">Due to a bug in the current implementation, if the sample duration is set to zero, the [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) call succeeds, but a subsequent call to [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) will throw a divide-by-zero exception.</span></span> <span data-ttu-id="18af2-281">Per evitare questo errore, impostare un periodo di validità diverso da zero per ogni esempio di input.</span><span class="sxs-lookup"><span data-stu-id="18af2-281">To avoid this error, set a valid nonzero duration on each input sample.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="18af2-282">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18af2-282">Requirements</span></span>



| <span data-ttu-id="18af2-283">Requisito</span><span class="sxs-lookup"><span data-stu-id="18af2-283">Requirement</span></span> | <span data-ttu-id="18af2-284">Valore</span><span class="sxs-lookup"><span data-stu-id="18af2-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18af2-285">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18af2-285">Minimum supported client</span></span><br/> | <span data-ttu-id="18af2-286">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="18af2-286">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="18af2-287">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18af2-287">Minimum supported server</span></span><br/> | <span data-ttu-id="18af2-288">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="18af2-288">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="18af2-289">DLL</span><span class="sxs-lookup"><span data-stu-id="18af2-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18af2-290"><dt>Mfaacenc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18af2-290"><dt>Mfaacenc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18af2-291">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18af2-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18af2-292">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="18af2-292">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="18af2-293">**Decoder AAC**</span><span class="sxs-lookup"><span data-stu-id="18af2-293">**AAC Decoder**</span></span>](aac-decoder.md)
</dt> <dt>

[<span data-ttu-id="18af2-294">Tipi di supporti AAC</span><span class="sxs-lookup"><span data-stu-id="18af2-294">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="18af2-295">Tipi di supporti audio</span><span class="sxs-lookup"><span data-stu-id="18af2-295">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="18af2-296">Supporto MPEG-4 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18af2-296">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="18af2-297">Formati multimediali supportati in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18af2-297">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

