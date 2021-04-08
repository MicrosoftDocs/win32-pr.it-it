---
description: Il codificatore audio MPEG-2 Microsoft Media Foundation è una trasformazione Media Foundation che codifica audio mono o stereo in MPEG-1 audio (ISO/IEC 11172-3) o MPEG-2 audio (ISO/IEC 13818-3).
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: Codificatore audio MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2454e542ba59f4955668bd1fcefbf5dbc0f11551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880066"
---
# <a name="mpeg-2-audio-encoder"></a><span data-ttu-id="ab606-103">Codificatore audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="ab606-103">MPEG-2 Audio Encoder</span></span>

<span data-ttu-id="ab606-104">Il codificatore audio MPEG-2 Microsoft Media Foundation è una [trasformazione Media Foundation](media-foundation-transforms.md) che codifica audio mono o stereo in MPEG-1 audio (ISO/IEC 11172-3) o MPEG-2 audio (ISO/IEC 13818-3).</span><span class="sxs-lookup"><span data-stu-id="ab606-104">The Microsoft Media Foundation MPEG-2 audio encoder is a [Media Foundation transform](media-foundation-transforms.md) that encodes mono or stereo audio to MPEG-1 audio (ISO/IEC 11172-3) or MPEG-2 audio (ISO/IEC 13818-3).</span></span>

<span data-ttu-id="ab606-105">Il codificatore supporta l'audio di livello 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="ab606-105">The encoder supports Layer 1 and Layer 2 audio.</span></span> <span data-ttu-id="ab606-106">Non supporta l'audio MPEG-Layer 3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="ab606-106">It does not support MPEG-Layer 3 (MP3) audio.</span></span> <span data-ttu-id="ab606-107">Per MPEG-2, il codificatore supporta la porzione low Sampling frequenze (LSF) dell'audio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="ab606-107">For MPEG-2, the encoder supports the Low Sampling Frequencies (LSF) portion of MPEG-2 audio.</span></span> <span data-ttu-id="ab606-108">Non supporta le estensioni multicanale.</span><span class="sxs-lookup"><span data-stu-id="ab606-108">It does not support the multichannel extensions.</span></span> <span data-ttu-id="ab606-109">Il MFT restituisce un flusso di formato elementare MPEG.</span><span class="sxs-lookup"><span data-stu-id="ab606-109">The MFT outputs an MPEG elementary stream.</span></span> <span data-ttu-id="ab606-110">Non è in grado di generare flussi elementari, flussi di programma o flussi di trasporto in pacchetto.</span><span class="sxs-lookup"><span data-stu-id="ab606-110">It cannot generate packetized elementary streams, program streams, or transport streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="ab606-111">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="ab606-111">Class Identifier</span></span>

<span data-ttu-id="ab606-112">L'identificatore di classe (CLSID) del codificatore audio MEPG-2 è **CLSID \_ CMPEG2AudioEncoderMFT**, definito nel file di intestazione wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="ab606-112">The class identifier (CLSID) of the MEPG-2 audio encoder is **CLSID\_CMPEG2AudioEncoderMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="ab606-113">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="ab606-113">Output Types</span></span>

<span data-ttu-id="ab606-114">Il tipo di output deve essere impostato per primo, prima del tipo di input.</span><span class="sxs-lookup"><span data-stu-id="ab606-114">The output type must be set first, before the input type.</span></span> <span data-ttu-id="ab606-115">Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="ab606-115">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab606-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="ab606-116">Attribute</span></span></th>
<th><span data-ttu-id="ab606-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab606-117">Description</span></span></th>
<th><span data-ttu-id="ab606-118">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="ab606-118">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ab606-119"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="ab606-119"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="ab606-120">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="ab606-120">Major type.</span></span></td>
<td><span data-ttu-id="ab606-121">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab606-121">Required.</span></span> <span data-ttu-id="ab606-122">Deve essere <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab606-122">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab606-123"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="ab606-123"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="ab606-124">Sottotipo audio.</span><span class="sxs-lookup"><span data-stu-id="ab606-124">Audio subtype.</span></span></td>
<td><span data-ttu-id="ab606-125">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab606-125">Required.</span></span> <span data-ttu-id="ab606-126">Deve essere <strong>MFAudioFormat_MPEG</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab606-126">Must be <strong>MFAudioFormat_MPEG</strong>.</span></span> <span data-ttu-id="ab606-127">Questo sottotipo viene usato sia per audio MPEG-1 che MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="ab606-127">This subtype is used for both MPEG-1 and MPEG-2 audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab606-128"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="ab606-128"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="ab606-129">Campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="ab606-129">Samples per second.</span></span></td>
<td><span data-ttu-id="ab606-130">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab606-130">Required.</span></span> <span data-ttu-id="ab606-131">Per MPEG-1 e MPEG-2 sono supportati i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ab606-131">The following values are supported for both MPEG-1 and MPEG-2:</span></span>
<ul>
<li><span data-ttu-id="ab606-132">32000</span><span class="sxs-lookup"><span data-stu-id="ab606-132">32000</span></span></li>
<li><span data-ttu-id="ab606-133">44100</span><span class="sxs-lookup"><span data-stu-id="ab606-133">44100</span></span></li>
<li><span data-ttu-id="ab606-134">48000</span><span class="sxs-lookup"><span data-stu-id="ab606-134">48000</span></span></li>
</ul>
<span data-ttu-id="ab606-135">Per MPEG-2 LSF sono inoltre supportati i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ab606-135">In addition, the following values are supported for MPEG-2 LSF:</span></span> <br/>
<ul>
<li><span data-ttu-id="ab606-136">16000</span><span class="sxs-lookup"><span data-stu-id="ab606-136">16000</span></span></li>
<li><span data-ttu-id="ab606-137">22050</span><span class="sxs-lookup"><span data-stu-id="ab606-137">22050</span></span></li>
<li><span data-ttu-id="ab606-138">24000</span><span class="sxs-lookup"><span data-stu-id="ab606-138">24000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab606-139"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="ab606-139"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="ab606-140">Numero di canali.</span><span class="sxs-lookup"><span data-stu-id="ab606-140">Number of channels.</span></span></td>
<td><span data-ttu-id="ab606-141">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab606-141">Required.</span></span> <span data-ttu-id="ab606-142">Deve essere 1 (mono) o 2 (stereo).</span><span class="sxs-lookup"><span data-stu-id="ab606-142">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab606-143"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="ab606-143"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="ab606-144">Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="ab606-144">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="ab606-145">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ab606-145">Optional.</span></span> <span data-ttu-id="ab606-146">Se impostato, il valore deve essere 0x3 per i canali stereo (front left e Right) o 0x4 per mono (canale front-end).</span><span class="sxs-lookup"><span data-stu-id="ab606-146">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab606-147"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="ab606-147"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="ab606-148">Velocità in bit del flusso MPEG codificato, in byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="ab606-148">Bit rate of the encoded MPEG stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="ab606-149">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ab606-149">Optional.</span></span><br/> <span data-ttu-id="ab606-150">Le specifiche ISO/IEC 11172-3 e ISO/IEC 13818-3 (LSF) definiscono diverse velocità in bit, a seconda della frequenza di campionamento, del numero di canali e del livello audio (1 o 2).</span><span class="sxs-lookup"><span data-stu-id="ab606-150">The ISO/IEC 11172-3 and ISO/IEC 13818-3 (LSF) specifications define several bit rates, depending on the sampling rate, the number of channels, and the audio layer (1 or 2).</span></span> <br/> <span data-ttu-id="ab606-151">Per impostazione predefinita, l'audio del codificatore è di livello 2.</span><span class="sxs-lookup"><span data-stu-id="ab606-151">The encoder defaults to Layer 2 audio.</span></span> <span data-ttu-id="ab606-152">Se l'attributo <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> non è impostato, il codificatore usa le seguenti velocità in bit predefinite:</span><span class="sxs-lookup"><span data-stu-id="ab606-152">If the <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> attribute is not set, the encoder uses the following default bit rates:</span></span><br/>
<ul>
<li><span data-ttu-id="ab606-153">MPEG-1 stereo: 224.000 bit al secondo (BPS) = 28.000 byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="ab606-153">MPEG-1 stereo: 224,000 bits per second (bps) = 28,000 bytes per second.</span></span></li>
<li><span data-ttu-id="ab606-154">MPEG-1 mono: 192.000 bps = 24.000 byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="ab606-154">MPEG-1 mono: 192,000 bps = 24,000 bytes per second.</span></span></li>
<li><span data-ttu-id="ab606-155">MPEG-2 LSF, mono o stereo: 160.000 bps = 20.000 byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="ab606-155">MPEG-2 LSF, mono or stereo: 160,000 bps = 20,000 bytes per second.</span></span></li>
</ul>
<span data-ttu-id="ab606-156">Questo attributo può essere impostato su altri valori.</span><span class="sxs-lookup"><span data-stu-id="ab606-156">This attribute can be set to other values.</span></span> <span data-ttu-id="ab606-157">Se il valore non è valido in base alle specifiche MPEG, il MFT rifiuterà il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="ab606-157">If the value is not valid according to MPEG specifications, the MFT will reject the media type.</span></span><br/> <span data-ttu-id="ab606-158">È anche possibile impostare la velocità in bit usando l'interfaccia <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ab606-158">You can also set the bit rate by using the <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> interface.</span></span> <span data-ttu-id="ab606-159">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ab606-159">See Remarks for more information.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ab606-160">Se gli attributi facoltativi non sono impostati, il codificatore li aggiunge al tipo di supporto dopo l'impostazione del tipo.</span><span class="sxs-lookup"><span data-stu-id="ab606-160">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="ab606-161">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="ab606-161">Input Types</span></span>

<span data-ttu-id="ab606-162">Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="ab606-162">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab606-163">Attributo</span><span class="sxs-lookup"><span data-stu-id="ab606-163">Attribute</span></span></th>
<th><span data-ttu-id="ab606-164">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab606-164">Description</span></span></th>
<th><span data-ttu-id="ab606-165">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="ab606-165">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ab606-166"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="ab606-166"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="ab606-167">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="ab606-167">Major type.</span></span></td>
<td><span data-ttu-id="ab606-168">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab606-168">Required.</span></span> <span data-ttu-id="ab606-169">Deve essere <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab606-169">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab606-170"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="ab606-170"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="ab606-171">Sottotipo audio.</span><span class="sxs-lookup"><span data-stu-id="ab606-171">Audio subtype.</span></span></td>
<td><span data-ttu-id="ab606-172">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab606-172">Required.</span></span> <span data-ttu-id="ab606-173">Deve essere <strong>MFAudioFormat_PCM</strong> o <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab606-173">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab606-174"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="ab606-174"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="ab606-175">Numero di bit per esempio audio.</span><span class="sxs-lookup"><span data-stu-id="ab606-175">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="ab606-176">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab606-176">Required.</span></span> <span data-ttu-id="ab606-177">Il valore deve essere 16 se il sottotipo è <strong>MFAudioFormat_PCM</strong>, oppure 32 se il sottotipo è <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab606-177">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab606-178"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="ab606-178"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="ab606-179">Campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="ab606-179">Samples per second.</span></span></td>
<td><span data-ttu-id="ab606-180">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab606-180">Required.</span></span> <span data-ttu-id="ab606-181">Deve corrispondere al tipo di output.</span><span class="sxs-lookup"><span data-stu-id="ab606-181">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab606-182"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="ab606-182"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="ab606-183">Numero di canali.</span><span class="sxs-lookup"><span data-stu-id="ab606-183">Number of channels.</span></span></td>
<td><span data-ttu-id="ab606-184">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab606-184">Required.</span></span> <span data-ttu-id="ab606-185">Deve corrispondere al tipo di output.</span><span class="sxs-lookup"><span data-stu-id="ab606-185">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab606-186"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="ab606-186"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="ab606-187">Allineamento del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="ab606-187">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="ab606-188">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab606-188">Required.</span></span> <span data-ttu-id="ab606-189">Calcolare il valore come segue:</span><span class="sxs-lookup"><span data-stu-id="ab606-189">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="ab606-190"><strong>MFAudioFormat_PCM</strong>: numero di canali × 2.</span><span class="sxs-lookup"><span data-stu-id="ab606-190"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="ab606-191"><strong>MFAudioFormat_Float</strong>: numero di canali × 4.</span><span class="sxs-lookup"><span data-stu-id="ab606-191"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab606-192"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="ab606-192"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="ab606-193">Velocità in bit del flusso AC3 codificato, in byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="ab606-193">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="ab606-194">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab606-194">Required.</span></span> <span data-ttu-id="ab606-195">È necessario che l'allineamento a blocchi sia uguale a × campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="ab606-195">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab606-196"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="ab606-196"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="ab606-197">Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="ab606-197">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="ab606-198">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ab606-198">Optional.</span></span> <span data-ttu-id="ab606-199">Se impostato, il valore deve corrispondere al tipo di output.</span><span class="sxs-lookup"><span data-stu-id="ab606-199">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab606-200"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="ab606-200"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="ab606-201">Numero di bit validi di dati audio in ogni esempio audio.</span><span class="sxs-lookup"><span data-stu-id="ab606-201">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="ab606-202">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ab606-202">Optional.</span></span> <span data-ttu-id="ab606-203">Se impostato, il valore deve essere identico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="ab606-203">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ab606-204">Il codificatore non supporta la conversione della frequenza di campionamento o la conversione stereo/mono.</span><span class="sxs-lookup"><span data-stu-id="ab606-204">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span> <span data-ttu-id="ab606-205">Se gli attributi facoltativi non sono impostati, il codificatore li aggiunge al tipo di supporto dopo l'impostazione del tipo.</span><span class="sxs-lookup"><span data-stu-id="ab606-205">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="ab606-206">Proprietà codec</span><span class="sxs-lookup"><span data-stu-id="ab606-206">Codec Properties</span></span>

<span data-ttu-id="ab606-207">Il codificatore supporta le seguenti proprietà tramite l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="ab606-207">The encoder supports the following properties through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>



| <span data-ttu-id="ab606-208">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ab606-208">Property</span></span>                                                                                | <span data-ttu-id="ab606-209">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab606-209">Description</span></span>                                                                                      | <span data-ttu-id="ab606-210">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="ab606-210">Default value</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab606-211">Codecapis \_ AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="ab606-211">CODECAPI\_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)               | <span data-ttu-id="ab606-212">Specifica la velocità in bit codificata media, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ab606-212">Specifies the average encoded bit rate, in bits per second.</span></span>                                      | <span data-ttu-id="ab606-213">Come descritto per l'attributo [MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md) nel tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="ab606-213">As described for the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output media type.</span></span>                      |
| [<span data-ttu-id="ab606-214">Codecapis \_ AVEncMPACodingMode</span><span class="sxs-lookup"><span data-stu-id="ab606-214">CODECAPI\_AVEncMPACodingMode</span></span>](../directshow/avencmpacodingmode-property.md)                       | <span data-ttu-id="ab606-215">Specifica la modalità di codifica audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="ab606-215">Specifies the MPEG audio encoding mode.</span></span>                                                          | <span data-ttu-id="ab606-216">Stereo per audio a 2 canali o canale singolo per audio a 1 canale.</span><span class="sxs-lookup"><span data-stu-id="ab606-216">Stereo for 2-channel audio, or single channel for 1-channel audio.</span></span><br/> <span data-ttu-id="ab606-217">Per l'audio a 2 canali, il codificatore supporta anche il Dual Channel e lo stereo misto.</span><span class="sxs-lookup"><span data-stu-id="ab606-217">For 2-channel audio, the encoder also supports dual channel and joint stereo.</span></span><br/> |
| [<span data-ttu-id="ab606-218">Codecapis \_ AVEncMPACopyright</span><span class="sxs-lookup"><span data-stu-id="ab606-218">CODECAPI\_AVEncMPACopyright</span></span>](../directshow/avencmpacopyright-property.md)                         | <span data-ttu-id="ab606-219">Specifica se impostare il bit di copyright nel flusso audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="ab606-219">Specifies whether to set the copyright bit in the MPEG audio stream.</span></span>                             | <span data-ttu-id="ab606-220">Nessun copyright.</span><span class="sxs-lookup"><span data-stu-id="ab606-220">No copyright.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="ab606-221">Codecapis \_ AVEncMPAEmphasisType</span><span class="sxs-lookup"><span data-stu-id="ab606-221">CODECAPI\_AVEncMPAEmphasisType</span></span>](../directshow/avencmpaemphasistype-property.md)                   | <span data-ttu-id="ab606-222">Specifica il tipo di filtro di deenfasi da usare quando il flusso codificato viene decodificato.</span><span class="sxs-lookup"><span data-stu-id="ab606-222">Specifies the type of de-emphasis filter that should be used when the encoded stream is decoded.</span></span> | <span data-ttu-id="ab606-223">Non è stata specificata alcuna enfasi.</span><span class="sxs-lookup"><span data-stu-id="ab606-223">No emphasis specified.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="ab606-224">AVEncMPAEnableRedundancyProtection</span><span class="sxs-lookup"><span data-stu-id="ab606-224">AVEncMPAEnableRedundancyProtection</span></span>](../directshow/avencmpaenableredundancyprotection-property.md) | <span data-ttu-id="ab606-225">Specifica se aggiungere un controllo di ridondanza ciclico (CRC) all'intestazione del frame.</span><span class="sxs-lookup"><span data-stu-id="ab606-225">Specifies whether to add a cyclic redundancy check (CRC) to the frame header.</span></span>                    | <span data-ttu-id="ab606-226">Un checksum CRC viene scritto nel flusso di bit.</span><span class="sxs-lookup"><span data-stu-id="ab606-226">A CRC checksum is written to the bit stream.</span></span>                                                                                                                           |
| [<span data-ttu-id="ab606-227">Codecapis \_ AVEncMPALayer</span><span class="sxs-lookup"><span data-stu-id="ab606-227">CODECAPI\_AVEncMPALayer</span></span>](../directshow/avencmpalayer-property.md)                                 | <span data-ttu-id="ab606-228">Specifica il livello audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="ab606-228">Specifies the MPEG audio layer.</span></span>                                                                  | <span data-ttu-id="ab606-229">Audio di livello 2.</span><span class="sxs-lookup"><span data-stu-id="ab606-229">Layer 2 audio.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="ab606-230">Codecapis \_ AVEncMPAOriginalBitstream</span><span class="sxs-lookup"><span data-stu-id="ab606-230">CODECAPI\_AVEncMPAOriginalBitstream</span></span>](../directshow/avencmpaoriginalbitstream-property.md)         | <span data-ttu-id="ab606-231">Specifica se impostare per il bit originale nel flusso audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="ab606-231">Specifies whether to set for the original bit in the MPEG audio stream.</span></span>                          | <span data-ttu-id="ab606-232">Il bit "originale" è disattivato.</span><span class="sxs-lookup"><span data-stu-id="ab606-232">"Original" bit is off.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="ab606-233">Codecapis \_ AVEncMPAPrivateUserBit</span><span class="sxs-lookup"><span data-stu-id="ab606-233">CODECAPI\_AVEncMPAPrivateUserBit</span></span>](../directshow/avencmpaprivateuserbit-property.md)               | <span data-ttu-id="ab606-234">Specifica se impostare per il bit utente privato nel flusso audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="ab606-234">Specifies whether to set for the private user bit in the MPEG audio stream.</span></span>                      | <span data-ttu-id="ab606-235">Il bit utente privato è disattivato.</span><span class="sxs-lookup"><span data-stu-id="ab606-235">Private user bit is off.</span></span>                                                                                                                                               |



 

<span data-ttu-id="ab606-236">Per ottenere un puntatore all'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) , chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) in MFT.</span><span class="sxs-lookup"><span data-stu-id="ab606-236">To get a pointer to the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the MFT.</span></span>

<span data-ttu-id="ab606-237">Il MFT implementa i metodi di [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) seguenti:</span><span class="sxs-lookup"><span data-stu-id="ab606-237">The MFT implements the following [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods:</span></span>

-   [<span data-ttu-id="ab606-238">**GetParameterRange**</span><span class="sxs-lookup"><span data-stu-id="ab606-238">**GetParameterRange**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [<span data-ttu-id="ab606-239">**GetParameterValues**</span><span class="sxs-lookup"><span data-stu-id="ab606-239">**GetParameterValues**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [<span data-ttu-id="ab606-240">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="ab606-240">**GetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [<span data-ttu-id="ab606-241">**IsModifiable**</span><span class="sxs-lookup"><span data-stu-id="ab606-241">**IsModifiable**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [<span data-ttu-id="ab606-242">**IsSupported**</span><span class="sxs-lookup"><span data-stu-id="ab606-242">**IsSupported**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [<span data-ttu-id="ab606-243">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="ab606-243">**SetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

<span data-ttu-id="ab606-244">Tutti gli altri metodi [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) restituiscono **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="ab606-244">All other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods return **E\_NOTIMPL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab606-245">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab606-245">Remarks</span></span>

<span data-ttu-id="ab606-246">Ogni frame audio MPEG contiene esempi audio 384 (livello 1) o 1152 (livello 2) per canale.</span><span class="sxs-lookup"><span data-stu-id="ab606-246">Each MPEG audio frame contains either 384 (Layer 1) or 1152 (Layer 2) audio samples per channel.</span></span> <span data-ttu-id="ab606-247">Ogni buffer di input per il codificatore può tuttavia contenere un numero qualsiasi di campioni PCM.</span><span class="sxs-lookup"><span data-stu-id="ab606-247">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="ab606-248">La dimensione di ogni buffer di input deve essere un multiplo dell'allineamento del blocco.</span><span class="sxs-lookup"><span data-stu-id="ab606-248">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="ab606-249">Il codificatore memorizza nella cache gli esempi di input fino a quando non è sufficiente per un frame audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="ab606-249">The encoder caches input samples until it has enough for an MPEG audio frame.</span></span>

<span data-ttu-id="ab606-250">Ogni buffer di output contiene un frame MPEG non elaborato.</span><span class="sxs-lookup"><span data-stu-id="ab606-250">Each output buffer contains one raw MPEG frame.</span></span> <span data-ttu-id="ab606-251">Le dimensioni di ogni buffer di output dipendono dalla velocità in bit e dalla frequenza di campionamento.</span><span class="sxs-lookup"><span data-stu-id="ab606-251">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

### <a name="configuring-the-encoder"></a><span data-ttu-id="ab606-252">Configurazione del codificatore</span><span class="sxs-lookup"><span data-stu-id="ab606-252">Configuring the Encoder</span></span>

<span data-ttu-id="ab606-253">Per modificare le impostazioni predefinite del codificatore, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="ab606-253">To change any of the default settings on the encoder, perform the following steps:</span></span>

1.  <span data-ttu-id="ab606-254">Creare un'istanza del codificatore MFT.</span><span class="sxs-lookup"><span data-stu-id="ab606-254">Create an instance of the encoder MFT.</span></span>
2.  <span data-ttu-id="ab606-255">Chiamare [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere l'elenco dei tipi di output preferiti.</span><span class="sxs-lookup"><span data-stu-id="ab606-255">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the list of the preferred output types.</span></span> <span data-ttu-id="ab606-256">Il codificatore enumera tutte le frequenze di campionamento sia per mono che per stereo.</span><span class="sxs-lookup"><span data-stu-id="ab606-256">The encoder enumerates all sample rates for both mono and stereo.</span></span> <span data-ttu-id="ab606-257">Selezionare uno di questi tipi di supporti, in base alla frequenza di campionamento e al numero di canali.</span><span class="sxs-lookup"><span data-stu-id="ab606-257">Select one of these media types, based on the sample rate and number of channels.</span></span> <span data-ttu-id="ab606-258">L'attributo [MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md) indica la velocità in bit predefinita, in byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="ab606-258">The [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute indicates the default bit rate, in bytes per second.</span></span>
3.  <span data-ttu-id="ab606-259">Facoltativo: è possibile eseguire l'override della velocità in bit predefinita impostando un nuovo valore per i [ \_ byte media audio MF mt \_ \_ \_ \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md) nel tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="ab606-259">Optional: You can override the default bit rate by setting a new value for [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) on the output media type.</span></span> <span data-ttu-id="ab606-260">Le velocità in bit valide dipendono dalla frequenza di campionamento, dal numero di canali e dal livello audio.</span><span class="sxs-lookup"><span data-stu-id="ab606-260">Valid bit rates depend on the sample rate, number of channels, and audio layer.</span></span>
    > [!Note]  
    > <span data-ttu-id="ab606-261">A questo punto del processo di configurazione, per impostazione predefinita il codificatore corrisponde all'audio di livello 2 e accetterà solo le velocità in bit di livello 2.</span><span class="sxs-lookup"><span data-stu-id="ab606-261">At this point in the configuration process, the encoder defaults to Layer 2 audio and will only accept Layer 2 bit rates.</span></span> <span data-ttu-id="ab606-262">Sarà possibile passare il codificatore al livello 1 in un passaggio successivo. vedere il passaggio 7.</span><span class="sxs-lookup"><span data-stu-id="ab606-262">You will be able to switch the encoder to Layer 1 in a later step (see step 7).</span></span> <span data-ttu-id="ab606-263">In tal caso, lasciare la velocità in bit predefinita per ora; è possibile modificarlo di nuovo nel passaggio 8.</span><span class="sxs-lookup"><span data-stu-id="ab606-263">In that case, leave the default bit rate for now; you can change it again in step 8.</span></span>

     

4.  <span data-ttu-id="ab606-264">Chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="ab606-264">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the output media type.</span></span> <span data-ttu-id="ab606-265">Se si imposta un valore personalizzato per [i \_ \_ byte media audio MF mt \_ \_ \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md) e la MFT rifiuta il tipo di supporto di output, è probabile che sia stata specificata una velocità in bit non valida.</span><span class="sxs-lookup"><span data-stu-id="ab606-265">If you set your own value for [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) and the MFT rejects the output media type, it is likely because you specified an invalid bit rate.</span></span>
5.  <span data-ttu-id="ab606-266">Chiamare [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) per enumerare il tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="ab606-266">Call [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) to enumerate the input media type.</span></span> <span data-ttu-id="ab606-267">Poiché la frequenza di campionamento e il numero di canali devono essere identici a quelli del tipo di output, vengono enumerate solo due opzioni: input PCM a virgola mobile a 32 bit e input PCM a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="ab606-267">Because the sample rate and number of channels must be identical to the output type, only two options are enumerated: 32-bit floating-point PCM input and 16-bit integer PCM input.</span></span> <span data-ttu-id="ab606-268">Selezionare una di queste.</span><span class="sxs-lookup"><span data-stu-id="ab606-268">Select one of these.</span></span>
6.  <span data-ttu-id="ab606-269">Chiamare [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) per impostare il tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="ab606-269">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the input media type.</span></span>
7.  <span data-ttu-id="ab606-270">Facoltativo: per codificare l'audio di livello 1, impostare la proprietà [CODEcapis \_ AVEncMPALayer](../directshow/avencmpalayer-property.md) su **eAVEncMPALayer \_ 1**.</span><span class="sxs-lookup"><span data-stu-id="ab606-270">Optional: To encode Layer 1 audio, set the [CODECAPI\_AVEncMPALayer](../directshow/avencmpalayer-property.md) property to **eAVEncMPALayer\_1**.</span></span>
8.  <span data-ttu-id="ab606-271">Facoltativo: per modificare la velocità in bit, impostare la proprietà [CODEcapis \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="ab606-271">Optional: To change the bit rate, set the [CODECAPI\_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) property.</span></span> <span data-ttu-id="ab606-272">La velocità in bit deve essere una delle frequenze di bit valide elencate nelle specifiche MPEG-1 o MPEG-2 LSF.</span><span class="sxs-lookup"><span data-stu-id="ab606-272">The bit rate must be one of the valid bit rates listed in the MPEG-1 or MPEG-2 LSF specifications.</span></span> <span data-ttu-id="ab606-273">In alternativa, è possibile chiamare [**ICodecAPI:: GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) per ottenere un elenco di velocità in bit valide, in base alle impostazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="ab606-273">Alternatively, you can call [**ICodecAPI::GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) to get a list of valid bit rates, based on the current settings.</span></span>
9.  <span data-ttu-id="ab606-274">Facoltativo: con audio a 2 canali, è possibile impostare la proprietà [CODEcapis \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) per modificare la modalità di codifica in Dual Channel o joint stereo.</span><span class="sxs-lookup"><span data-stu-id="ab606-274">Optional: With 2-channel audio, you can set the [CODECAPI\_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) property to change the coding mode to dual channel or joint stereo.</span></span> <span data-ttu-id="ab606-275">È possibile chiamare [**ICodecAPI:: GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) per ottenere le opzioni valide.</span><span class="sxs-lookup"><span data-stu-id="ab606-275">You can call [**ICodecAPI::GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) to get the valid options.</span></span> <span data-ttu-id="ab606-276">Per l'audio a 1 canale, l'unica opzione è mono.</span><span class="sxs-lookup"><span data-stu-id="ab606-276">(For 1-channel audio, the only option is mono.)</span></span>
10. <span data-ttu-id="ab606-277">Facoltativo: impostare le altre proprietà [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) elencate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="ab606-277">Optional: Set any of the other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) properties listed previously.</span></span>

<span data-ttu-id="ab606-278">È importante seguire l'ordine di questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="ab606-278">It is important to follow the order of these steps.</span></span> <span data-ttu-id="ab606-279">In particolare, impostare il tipo di supporto di output prima di modificare le proprietà [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="ab606-279">In particular, set the output media type before changing any [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) properties.</span></span> <span data-ttu-id="ab606-280">Inoltre, è necessario impostare le proprietà di **ICodecAPI** prima che il MFT riceva il primo campione di input.</span><span class="sxs-lookup"><span data-stu-id="ab606-280">Also, you must set **ICodecAPI** properties before the MFT receives the first input sample.</span></span> <span data-ttu-id="ab606-281">Dopo la ricezione dell'input da parte di MFT, le proprietà del codec sono di sola lettura e [**ICodecAPI:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) restituisce il valore **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="ab606-281">After the MFT receives input, the codec properties are read-only, and [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) returns the value **S\_FALSE**.</span></span>

### <a name="supported-bit-rates"></a><span data-ttu-id="ab606-282">Velocità in bit supportate</span><span class="sxs-lookup"><span data-stu-id="ab606-282">Supported Bit Rates</span></span>

<span data-ttu-id="ab606-283">Il codificatore supporta le seguenti velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="ab606-283">The encoder supports the following bit rates.</span></span>



<span data-ttu-id="ab606-284">MPEG-1</span><span class="sxs-lookup"><span data-stu-id="ab606-284">MPEG-1</span></span>

<span data-ttu-id="ab606-285">MPEG-2</span><span class="sxs-lookup"><span data-stu-id="ab606-285">MPEG-2</span></span>

<span data-ttu-id="ab606-286">Livello 1</span><span class="sxs-lookup"><span data-stu-id="ab606-286">Layer 1</span></span>

<span data-ttu-id="ab606-287">Livello 2</span><span class="sxs-lookup"><span data-stu-id="ab606-287">Layer 2</span></span>

<span data-ttu-id="ab606-288">Livello 1</span><span class="sxs-lookup"><span data-stu-id="ab606-288">Layer 1</span></span>

<span data-ttu-id="ab606-289">Livello 2</span><span class="sxs-lookup"><span data-stu-id="ab606-289">Layer 2</span></span>

<span data-ttu-id="ab606-290">32</span><span class="sxs-lookup"><span data-stu-id="ab606-290">32</span></span>

<span data-ttu-id="ab606-291">32\*</span><span class="sxs-lookup"><span data-stu-id="ab606-291">32\*</span></span>

<span data-ttu-id="ab606-292">32</span><span class="sxs-lookup"><span data-stu-id="ab606-292">32</span></span>

<span data-ttu-id="ab606-293">8</span><span class="sxs-lookup"><span data-stu-id="ab606-293">8</span></span>

<span data-ttu-id="ab606-294">64</span><span class="sxs-lookup"><span data-stu-id="ab606-294">64</span></span>

<span data-ttu-id="ab606-295">48\*</span><span class="sxs-lookup"><span data-stu-id="ab606-295">48\*</span></span>

<span data-ttu-id="ab606-296">38</span><span class="sxs-lookup"><span data-stu-id="ab606-296">38</span></span>

<span data-ttu-id="ab606-297">16</span><span class="sxs-lookup"><span data-stu-id="ab606-297">16</span></span>

<span data-ttu-id="ab606-298">96</span><span class="sxs-lookup"><span data-stu-id="ab606-298">96</span></span>

<span data-ttu-id="ab606-299">56\*</span><span class="sxs-lookup"><span data-stu-id="ab606-299">56\*</span></span>

<span data-ttu-id="ab606-300">56</span><span class="sxs-lookup"><span data-stu-id="ab606-300">56</span></span>

<span data-ttu-id="ab606-301">24</span><span class="sxs-lookup"><span data-stu-id="ab606-301">24</span></span>

<span data-ttu-id="ab606-302">128</span><span class="sxs-lookup"><span data-stu-id="ab606-302">128</span></span>

<span data-ttu-id="ab606-303">64</span><span class="sxs-lookup"><span data-stu-id="ab606-303">64</span></span>

<span data-ttu-id="ab606-304">64</span><span class="sxs-lookup"><span data-stu-id="ab606-304">64</span></span>

<span data-ttu-id="ab606-305">32</span><span class="sxs-lookup"><span data-stu-id="ab606-305">32</span></span>

<span data-ttu-id="ab606-306">160</span><span class="sxs-lookup"><span data-stu-id="ab606-306">160</span></span>

<span data-ttu-id="ab606-307">80\*</span><span class="sxs-lookup"><span data-stu-id="ab606-307">80\*</span></span>

<span data-ttu-id="ab606-308">80</span><span class="sxs-lookup"><span data-stu-id="ab606-308">80</span></span>

<span data-ttu-id="ab606-309">40</span><span class="sxs-lookup"><span data-stu-id="ab606-309">40</span></span>

<span data-ttu-id="ab606-310">192</span><span class="sxs-lookup"><span data-stu-id="ab606-310">192</span></span>

<span data-ttu-id="ab606-311">96</span><span class="sxs-lookup"><span data-stu-id="ab606-311">96</span></span>

<span data-ttu-id="ab606-312">96</span><span class="sxs-lookup"><span data-stu-id="ab606-312">96</span></span>

<span data-ttu-id="ab606-313">48</span><span class="sxs-lookup"><span data-stu-id="ab606-313">48</span></span>

<span data-ttu-id="ab606-314">224</span><span class="sxs-lookup"><span data-stu-id="ab606-314">224</span></span>

<span data-ttu-id="ab606-315">112</span><span class="sxs-lookup"><span data-stu-id="ab606-315">112</span></span>

<span data-ttu-id="ab606-316">112</span><span class="sxs-lookup"><span data-stu-id="ab606-316">112</span></span>

<span data-ttu-id="ab606-317">56</span><span class="sxs-lookup"><span data-stu-id="ab606-317">56</span></span>

<span data-ttu-id="ab606-318">256</span><span class="sxs-lookup"><span data-stu-id="ab606-318">256</span></span>

<span data-ttu-id="ab606-319">128</span><span class="sxs-lookup"><span data-stu-id="ab606-319">128</span></span>

<span data-ttu-id="ab606-320">128</span><span class="sxs-lookup"><span data-stu-id="ab606-320">128</span></span>

<span data-ttu-id="ab606-321">64</span><span class="sxs-lookup"><span data-stu-id="ab606-321">64</span></span>

<span data-ttu-id="ab606-322">288</span><span class="sxs-lookup"><span data-stu-id="ab606-322">288</span></span>

<span data-ttu-id="ab606-323">160</span><span class="sxs-lookup"><span data-stu-id="ab606-323">160</span></span>

<span data-ttu-id="ab606-324">144</span><span class="sxs-lookup"><span data-stu-id="ab606-324">144</span></span>

<span data-ttu-id="ab606-325">80</span><span class="sxs-lookup"><span data-stu-id="ab606-325">80</span></span>

<span data-ttu-id="ab606-326">320</span><span class="sxs-lookup"><span data-stu-id="ab606-326">320</span></span>

<span data-ttu-id="ab606-327">192</span><span class="sxs-lookup"><span data-stu-id="ab606-327">192</span></span>

<span data-ttu-id="ab606-328">160</span><span class="sxs-lookup"><span data-stu-id="ab606-328">160</span></span>

<span data-ttu-id="ab606-329">96</span><span class="sxs-lookup"><span data-stu-id="ab606-329">96</span></span>

<span data-ttu-id="ab606-330">352</span><span class="sxs-lookup"><span data-stu-id="ab606-330">352</span></span>

<span data-ttu-id="ab606-331">224\*\*</span><span class="sxs-lookup"><span data-stu-id="ab606-331">224\*\*</span></span>

<span data-ttu-id="ab606-332">176</span><span class="sxs-lookup"><span data-stu-id="ab606-332">176</span></span>

<span data-ttu-id="ab606-333">112</span><span class="sxs-lookup"><span data-stu-id="ab606-333">112</span></span>

<span data-ttu-id="ab606-334">384</span><span class="sxs-lookup"><span data-stu-id="ab606-334">384</span></span>

<span data-ttu-id="ab606-335">256\*\*</span><span class="sxs-lookup"><span data-stu-id="ab606-335">256\*\*</span></span>

<span data-ttu-id="ab606-336">192</span><span class="sxs-lookup"><span data-stu-id="ab606-336">192</span></span>

<span data-ttu-id="ab606-337">128</span><span class="sxs-lookup"><span data-stu-id="ab606-337">128</span></span>

<span data-ttu-id="ab606-338">416</span><span class="sxs-lookup"><span data-stu-id="ab606-338">416</span></span>

<span data-ttu-id="ab606-339">230\*\*</span><span class="sxs-lookup"><span data-stu-id="ab606-339">230\*\*</span></span>

<span data-ttu-id="ab606-340">224</span><span class="sxs-lookup"><span data-stu-id="ab606-340">224</span></span>

<span data-ttu-id="ab606-341">144</span><span class="sxs-lookup"><span data-stu-id="ab606-341">144</span></span>

<span data-ttu-id="ab606-342">448</span><span class="sxs-lookup"><span data-stu-id="ab606-342">448</span></span>

<span data-ttu-id="ab606-343">384\*\*</span><span class="sxs-lookup"><span data-stu-id="ab606-343">384\*\*</span></span>

<span data-ttu-id="ab606-344">256</span><span class="sxs-lookup"><span data-stu-id="ab606-344">256</span></span>

<span data-ttu-id="ab606-345">160</span><span class="sxs-lookup"><span data-stu-id="ab606-345">160</span></span>



 

<dl> <span data-ttu-id="ab606-346">\* Solo mono</span><span class="sxs-lookup"><span data-stu-id="ab606-346">\* Mono only</span></span>  
<span data-ttu-id="ab606-347">\*\* Solo stereo</span><span class="sxs-lookup"><span data-stu-id="ab606-347">\*\* Stereo only</span></span>  
</dl>

### <a name="example-media-types"></a><span data-ttu-id="ab606-348">Tipi di supporti di esempio</span><span class="sxs-lookup"><span data-stu-id="ab606-348">Example Media Types</span></span>

<span data-ttu-id="ab606-349">Di seguito è riportato un esempio dei tipi di supporto necessari per codificare un PCM a 16 bit di tipo Integer, 48-kHz audio stereo alla velocità in bit predefinita.</span><span class="sxs-lookup"><span data-stu-id="ab606-349">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate.</span></span>

<span data-ttu-id="ab606-350">Tipo di supporto di output:</span><span class="sxs-lookup"><span data-stu-id="ab606-350">Output media type:</span></span>

| <span data-ttu-id="ab606-351">Attributo</span><span class="sxs-lookup"><span data-stu-id="ab606-351">Attribute</span></span>                                                                           | <span data-ttu-id="ab606-352">Valore</span><span class="sxs-lookup"><span data-stu-id="ab606-352">Value</span></span>                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [<span data-ttu-id="ab606-353">\_ \_ tipo principale MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="ab606-353">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="ab606-354">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ab606-354">**MFMediaType\_Audio**</span></span>  |
| [<span data-ttu-id="ab606-355">sottotipo MF \_ mt \_</span><span class="sxs-lookup"><span data-stu-id="ab606-355">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="ab606-356">**\_MPEG MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="ab606-356">**MFAudioFormat\_MPEG**</span></span> |
| [<span data-ttu-id="ab606-357">\_ \_ campioni audio MF \_ mt \_ al \_ secondo</span><span class="sxs-lookup"><span data-stu-id="ab606-357">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="ab606-358">48000</span><span class="sxs-lookup"><span data-stu-id="ab606-358">48000</span></span>                   |
| [<span data-ttu-id="ab606-359">numero \_ di \_ \_ canali audio MF mt \_</span><span class="sxs-lookup"><span data-stu-id="ab606-359">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="ab606-360">2</span><span class="sxs-lookup"><span data-stu-id="ab606-360">2</span></span>                       |



 

<span data-ttu-id="ab606-361">Tipo di supporto di input:</span><span class="sxs-lookup"><span data-stu-id="ab606-361">Input media type:</span></span>

| <span data-ttu-id="ab606-362">Attributo</span><span class="sxs-lookup"><span data-stu-id="ab606-362">Attribute</span></span>                                                                                | <span data-ttu-id="ab606-363">Valore</span><span class="sxs-lookup"><span data-stu-id="ab606-363">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="ab606-364">\_ \_ tipo principale MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="ab606-364">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="ab606-365">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ab606-365">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="ab606-366">sottotipo MF \_ mt \_</span><span class="sxs-lookup"><span data-stu-id="ab606-366">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="ab606-367">**\_PCM MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="ab606-367">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="ab606-368">\_ \_ bit audio MF \_ mt \_ per \_ campione</span><span class="sxs-lookup"><span data-stu-id="ab606-368">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="ab606-369">16</span><span class="sxs-lookup"><span data-stu-id="ab606-369">16</span></span>                     |
| [<span data-ttu-id="ab606-370">\_ \_ campioni audio MF \_ mt \_ al \_ secondo</span><span class="sxs-lookup"><span data-stu-id="ab606-370">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="ab606-371">48000</span><span class="sxs-lookup"><span data-stu-id="ab606-371">48000</span></span>                  |
| [<span data-ttu-id="ab606-372">numero \_ di \_ \_ canali audio MF mt \_</span><span class="sxs-lookup"><span data-stu-id="ab606-372">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="ab606-373">2</span><span class="sxs-lookup"><span data-stu-id="ab606-373">2</span></span>                      |
| [<span data-ttu-id="ab606-374">\_ \_ \_ allineamento blocchi audio MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="ab606-374">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="ab606-375">4</span><span class="sxs-lookup"><span data-stu-id="ab606-375">4</span></span>                      |
| [<span data-ttu-id="ab606-376">\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo</span><span class="sxs-lookup"><span data-stu-id="ab606-376">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="ab606-377">192000</span><span class="sxs-lookup"><span data-stu-id="ab606-377">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="ab606-378">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab606-378">Requirements</span></span>



| <span data-ttu-id="ab606-379">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab606-379">Requirement</span></span> | <span data-ttu-id="ab606-380">Valore</span><span class="sxs-lookup"><span data-stu-id="ab606-380">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab606-381">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab606-381">Minimum supported client</span></span><br/> | <span data-ttu-id="ab606-382">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ab606-382">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ab606-383">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab606-383">Minimum supported server</span></span><br/> | <span data-ttu-id="ab606-384">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ab606-384">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ab606-385">DLL</span><span class="sxs-lookup"><span data-stu-id="ab606-385">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab606-386"><dt>Msmpeg2enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab606-386"><dt>Msmpeg2enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab606-387">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab606-387">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab606-388">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="ab606-388">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
