---
description: Il decoder audio Dolby è un Media Foundation Transform (MFT) che codifica mono o stereo audio in Dolby Digital, detto anche Dolby AC-3.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Codificatore audio Dolby Digital
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6c5b59bc09cd8c0fd56f22703ef8afdfe3921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305398"
---
# <a name="dolby-digital-audio-encoder"></a><span data-ttu-id="062b5-103">Codificatore audio Dolby Digital</span><span class="sxs-lookup"><span data-stu-id="062b5-103">Dolby Digital Audio Encoder</span></span>

<span data-ttu-id="062b5-104">Il decoder audio Dolby è un [Media Foundation Transform](media-foundation-transforms.md) (MFT) che codifica mono o stereo audio in Dolby Digital, detto anche Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="062b5-104">The Dolby audio decoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that encodes mono or stereo audio to Dolby Digital, also called Dolby AC-3.</span></span> <span data-ttu-id="062b5-105">Il codificatore non supporta l'input multicanale, ad esempio la configurazione del canale 5,1.</span><span class="sxs-lookup"><span data-stu-id="062b5-105">The encoder does not support multi-channel input, such as the 5.1 channel configuration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="062b5-106">Per le versioni di Windows precedenti a Windows 8, l'implementazione Microsoft della tecnologia Dolby Digital è limitata ai sensi del programma di licenza Dolby Digital per l'uso da parte delle applicazioni Microsoft.</span><span class="sxs-lookup"><span data-stu-id="062b5-106">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="062b5-107">Per ulteriori informazioni sull'audio Dolby Digital, vedere la sezione relativa alla revisione B per il documento ATSC (Advanced Television Systems Committee), *ovvero AC-3, E-AC-3*.</span><span class="sxs-lookup"><span data-stu-id="062b5-107">For more information about Dolby Digital audio, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="062b5-108">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="062b5-108">Class Identifier</span></span>

<span data-ttu-id="062b5-109">L'identificatore di classe (CLSID) del decodificatore Dolby audio è **CLSID \_ CMSDolbyDigitalEncMFT**, definito nel file di intestazione wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="062b5-109">The class identifier (CLSID) of the Dolby audio decoder is **CLSID\_CMSDolbyDigitalEncMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="062b5-110">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="062b5-110">Output Types</span></span>

<span data-ttu-id="062b5-111">Il tipo di output deve essere impostato per primo, prima del tipo di input.</span><span class="sxs-lookup"><span data-stu-id="062b5-111">The output type must be set first, before the input type.</span></span> <span data-ttu-id="062b5-112">Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="062b5-112">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="062b5-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="062b5-113">Attribute</span></span></th>
<th><span data-ttu-id="062b5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="062b5-114">Description</span></span></th>
<th><span data-ttu-id="062b5-115">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="062b5-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="062b5-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="062b5-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="062b5-117">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="062b5-117">Major type.</span></span></td>
<td><span data-ttu-id="062b5-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="062b5-118">Required.</span></span> <span data-ttu-id="062b5-119">Deve essere <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="062b5-119">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="062b5-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="062b5-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="062b5-121">Sottotipo audio.</span><span class="sxs-lookup"><span data-stu-id="062b5-121">Audio subtype.</span></span></td>
<td><span data-ttu-id="062b5-122">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="062b5-122">Required.</span></span> <span data-ttu-id="062b5-123">Deve essere <strong>MFAudioFormat_Dolby_AC3</strong>.</span><span class="sxs-lookup"><span data-stu-id="062b5-123">Must be <strong>MFAudioFormat_Dolby_AC3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="062b5-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="062b5-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="062b5-125">Campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="062b5-125">Samples per second.</span></span></td>
<td><span data-ttu-id="062b5-126">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="062b5-126">Required.</span></span> <span data-ttu-id="062b5-127">Sono supportati i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="062b5-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="062b5-128">32000</span><span class="sxs-lookup"><span data-stu-id="062b5-128">32000</span></span></li>
<li><span data-ttu-id="062b5-129">44100</span><span class="sxs-lookup"><span data-stu-id="062b5-129">44100</span></span></li>
<li><span data-ttu-id="062b5-130">48000</span><span class="sxs-lookup"><span data-stu-id="062b5-130">48000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="062b5-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="062b5-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="062b5-132">Numero di canali.</span><span class="sxs-lookup"><span data-stu-id="062b5-132">Number of channels.</span></span></td>
<td><span data-ttu-id="062b5-133">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="062b5-133">Required.</span></span> <span data-ttu-id="062b5-134">Deve essere 1 (mono) o 2 (stereo).</span><span class="sxs-lookup"><span data-stu-id="062b5-134">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="062b5-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="062b5-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="062b5-136">Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="062b5-136">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="062b5-137">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="062b5-137">Optional.</span></span> <span data-ttu-id="062b5-138">Se impostato, il valore deve essere 0x3 per i canali stereo (front left e Right) o 0x4 per mono (canale front-end).</span><span class="sxs-lookup"><span data-stu-id="062b5-138">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="062b5-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="062b5-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="062b5-140">Velocità in bit del flusso AC-3 codificato, in byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="062b5-140">Bit rate of the encoded AC-3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="062b5-141">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="062b5-141">Optional.</span></span> <span data-ttu-id="062b5-142">Vedere la sezione Osservazioni per i valori validi.</span><span class="sxs-lookup"><span data-stu-id="062b5-142">See Remarks for valid values.</span></span> <span data-ttu-id="062b5-143">Se questo attributo non è impostato, il codificatore usa una velocità in bit predefinita, come descritto in note.</span><span class="sxs-lookup"><span data-stu-id="062b5-143">If this attribute is not set, the encoder uses a default bit rate, as described in Remarks.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="062b5-144">Se gli attributi facoltativi non sono impostati, il codificatore li aggiunge al tipo di supporto dopo l'impostazione del tipo.</span><span class="sxs-lookup"><span data-stu-id="062b5-144">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="062b5-145">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="062b5-145">Input Types</span></span>

<span data-ttu-id="062b5-146">Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="062b5-146">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="062b5-147">Attributo</span><span class="sxs-lookup"><span data-stu-id="062b5-147">Attribute</span></span></th>
<th><span data-ttu-id="062b5-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="062b5-148">Description</span></span></th>
<th><span data-ttu-id="062b5-149">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="062b5-149">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="062b5-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="062b5-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="062b5-151">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="062b5-151">Major type.</span></span></td>
<td><span data-ttu-id="062b5-152">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="062b5-152">Required.</span></span> <span data-ttu-id="062b5-153">Deve essere <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="062b5-153">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="062b5-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="062b5-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="062b5-155">Sottotipo audio.</span><span class="sxs-lookup"><span data-stu-id="062b5-155">Audio subtype.</span></span></td>
<td><span data-ttu-id="062b5-156">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="062b5-156">Required.</span></span> <span data-ttu-id="062b5-157">Deve essere <strong>MFAudioFormat_PCM</strong> o <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="062b5-157">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="062b5-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="062b5-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="062b5-159">Numero di bit per esempio audio.</span><span class="sxs-lookup"><span data-stu-id="062b5-159">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="062b5-160">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="062b5-160">Required.</span></span> <span data-ttu-id="062b5-161">Il valore deve essere 16 se il sottotipo è <strong>MFAudioFormat_PCM</strong>, oppure 32 se il sottotipo è <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="062b5-161">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="062b5-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="062b5-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="062b5-163">Campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="062b5-163">Samples per second.</span></span></td>
<td><span data-ttu-id="062b5-164">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="062b5-164">Required.</span></span> <span data-ttu-id="062b5-165">Deve corrispondere al tipo di output.</span><span class="sxs-lookup"><span data-stu-id="062b5-165">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="062b5-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="062b5-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="062b5-167">Numero di canali.</span><span class="sxs-lookup"><span data-stu-id="062b5-167">Number of channels.</span></span></td>
<td><span data-ttu-id="062b5-168">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="062b5-168">Required.</span></span> <span data-ttu-id="062b5-169">Deve corrispondere al tipo di output.</span><span class="sxs-lookup"><span data-stu-id="062b5-169">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="062b5-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="062b5-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="062b5-171">Allineamento del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="062b5-171">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="062b5-172">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="062b5-172">Required.</span></span> <span data-ttu-id="062b5-173">Calcolare il valore come segue:</span><span class="sxs-lookup"><span data-stu-id="062b5-173">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="062b5-174"><strong>MFAudioFormat_PCM</strong>: numero di canali × 2.</span><span class="sxs-lookup"><span data-stu-id="062b5-174"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="062b5-175"><strong>MFAudioFormat_Float</strong>: numero di canali × 4.</span><span class="sxs-lookup"><span data-stu-id="062b5-175"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="062b5-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="062b5-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="062b5-177">Velocità in bit del flusso AC3 codificato, in byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="062b5-177">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="062b5-178">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="062b5-178">Required.</span></span> <span data-ttu-id="062b5-179">È necessario che l'allineamento a blocchi sia uguale a × campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="062b5-179">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="062b5-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="062b5-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="062b5-181">Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="062b5-181">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="062b5-182">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="062b5-182">Optional.</span></span> <span data-ttu-id="062b5-183">Se impostato, il valore deve corrispondere al tipo di output.</span><span class="sxs-lookup"><span data-stu-id="062b5-183">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="062b5-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="062b5-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="062b5-185">Numero di bit validi di dati audio in ogni esempio audio.</span><span class="sxs-lookup"><span data-stu-id="062b5-185">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="062b5-186">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="062b5-186">Optional.</span></span> <span data-ttu-id="062b5-187">Se impostato, il valore deve essere identico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="062b5-187">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="062b5-188">Il codificatore non supporta la conversione della frequenza di campionamento o la conversione stereo/mono.</span><span class="sxs-lookup"><span data-stu-id="062b5-188">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span>

## <a name="remarks"></a><span data-ttu-id="062b5-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="062b5-189">Remarks</span></span>

<span data-ttu-id="062b5-190">Ogni frame audio Dolby AC-3 contiene 1536 di esempi audio per canale.</span><span class="sxs-lookup"><span data-stu-id="062b5-190">Each Dolby AC-3 audio frame contains 1536 audio samples per channel.</span></span> <span data-ttu-id="062b5-191">Ogni buffer di input per il codificatore può tuttavia contenere un numero qualsiasi di campioni PCM.</span><span class="sxs-lookup"><span data-stu-id="062b5-191">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="062b5-192">La dimensione di ogni buffer di input deve essere un multiplo dell'allineamento del blocco.</span><span class="sxs-lookup"><span data-stu-id="062b5-192">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="062b5-193">Il codificatore memorizza nella cache gli esempi di input fino a quando non dispone di un numero sufficiente di campioni audio 1536 per canale; a questo punto il codificatore restituisce un frame AC-3.</span><span class="sxs-lookup"><span data-stu-id="062b5-193">The encoder caches input samples until it has enough for 1536 audio samples per channel; at which point the encoder outputs one AC-3 frame.</span></span>

<span data-ttu-id="062b5-194">Ogni buffer di output contiene un frame AC-3 non elaborato.</span><span class="sxs-lookup"><span data-stu-id="062b5-194">Each output buffer contains one raw AC-3 frame.</span></span> <span data-ttu-id="062b5-195">La durata è equivalente alla durata di 1536 campioni PCM alla frequenza di campionamento corrente (32 msec) alla frequenza di campionamento 48 kHz, 34,83 msec a 44,1 kHz e 48 msec a 32 kHz.</span><span class="sxs-lookup"><span data-stu-id="062b5-195">The duration is equivalent to the duration of 1536 PCM samples at the current sampling rate (32 msec) at 48 kHz sample rate, 34.83 msec at 44.1 kHz, and 48 msec at 32 kHz).</span></span> <span data-ttu-id="062b5-196">Le dimensioni di ogni buffer di output dipendono dalla velocità in bit e dalla frequenza di campionamento.</span><span class="sxs-lookup"><span data-stu-id="062b5-196">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

<span data-ttu-id="062b5-197">Per specificare la velocità in bit di codifica, impostare l'attributo [MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md) nel tipo di output.</span><span class="sxs-lookup"><span data-stu-id="062b5-197">To specify the encoding bit rate, set the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output type.</span></span> <span data-ttu-id="062b5-198">La tabella seguente illustra la relazione tra la velocità in bit di codifica e i \_ \_ byte media audio MF mt \_ \_ \_ al \_ secondo.</span><span class="sxs-lookup"><span data-stu-id="062b5-198">The following table shows the relation between encoding bit rate and MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND.</span></span>



| <span data-ttu-id="062b5-199">Velocità in bit (Kbps)</span><span class="sxs-lookup"><span data-stu-id="062b5-199">Bit rate (kbps)</span></span> | [<span data-ttu-id="062b5-200">\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo</span><span class="sxs-lookup"><span data-stu-id="062b5-200">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="062b5-201">Commenti</span><span class="sxs-lookup"><span data-stu-id="062b5-201">Remarks</span></span>                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="062b5-202">64</span><span class="sxs-lookup"><span data-stu-id="062b5-202">64</span></span>              | <span data-ttu-id="062b5-203">8000</span><span class="sxs-lookup"><span data-stu-id="062b5-203">8000</span></span>                                                                                     | <span data-ttu-id="062b5-204">Solo mono.</span><span class="sxs-lookup"><span data-stu-id="062b5-204">Mono only.</span></span>                                              |
| <span data-ttu-id="062b5-205">80</span><span class="sxs-lookup"><span data-stu-id="062b5-205">80</span></span>              | <span data-ttu-id="062b5-206">10000</span><span class="sxs-lookup"><span data-stu-id="062b5-206">10000</span></span>                                                                                    | <span data-ttu-id="062b5-207">Solo mono.</span><span class="sxs-lookup"><span data-stu-id="062b5-207">Mono only.</span></span>                                              |
| <span data-ttu-id="062b5-208">96</span><span class="sxs-lookup"><span data-stu-id="062b5-208">96</span></span>              | <span data-ttu-id="062b5-209">12000</span><span class="sxs-lookup"><span data-stu-id="062b5-209">12000</span></span>                                                                                    | <span data-ttu-id="062b5-210">Solo mono.</span><span class="sxs-lookup"><span data-stu-id="062b5-210">Mono only.</span></span>                                              |
| <span data-ttu-id="062b5-211">112</span><span class="sxs-lookup"><span data-stu-id="062b5-211">112</span></span>             | <span data-ttu-id="062b5-212">14000</span><span class="sxs-lookup"><span data-stu-id="062b5-212">14000</span></span>                                                                                    | <span data-ttu-id="062b5-213">Solo mono.</span><span class="sxs-lookup"><span data-stu-id="062b5-213">Mono only.</span></span>                                              |
| <span data-ttu-id="062b5-214">128</span><span class="sxs-lookup"><span data-stu-id="062b5-214">128</span></span>             | <span data-ttu-id="062b5-215">16000</span><span class="sxs-lookup"><span data-stu-id="062b5-215">16000</span></span>                                                                                    | <span data-ttu-id="062b5-216">Mono o stereo.</span><span class="sxs-lookup"><span data-stu-id="062b5-216">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="062b5-217">160</span><span class="sxs-lookup"><span data-stu-id="062b5-217">160</span></span>             | <span data-ttu-id="062b5-218">20000</span><span class="sxs-lookup"><span data-stu-id="062b5-218">20000</span></span>                                                                                    | <span data-ttu-id="062b5-219">Mono o stereo.</span><span class="sxs-lookup"><span data-stu-id="062b5-219">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="062b5-220">192</span><span class="sxs-lookup"><span data-stu-id="062b5-220">192</span></span>             | <span data-ttu-id="062b5-221">24000</span><span class="sxs-lookup"><span data-stu-id="062b5-221">24000</span></span>                                                                                    | <span data-ttu-id="062b5-222">Mono o stereo.</span><span class="sxs-lookup"><span data-stu-id="062b5-222">Mono or stereo.</span></span> <span data-ttu-id="062b5-223">Questa è l'impostazione predefinita per mono.</span><span class="sxs-lookup"><span data-stu-id="062b5-223">This is the default setting for mono.</span></span>   |
| <span data-ttu-id="062b5-224">224</span><span class="sxs-lookup"><span data-stu-id="062b5-224">224</span></span>             | <span data-ttu-id="062b5-225">28000</span><span class="sxs-lookup"><span data-stu-id="062b5-225">28000</span></span>                                                                                    | <span data-ttu-id="062b5-226">Mono o stereo.</span><span class="sxs-lookup"><span data-stu-id="062b5-226">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="062b5-227">256</span><span class="sxs-lookup"><span data-stu-id="062b5-227">256</span></span>             | <span data-ttu-id="062b5-228">32000</span><span class="sxs-lookup"><span data-stu-id="062b5-228">32000</span></span>                                                                                    | <span data-ttu-id="062b5-229">Mono o stereo.</span><span class="sxs-lookup"><span data-stu-id="062b5-229">Mono or stereo.</span></span> <span data-ttu-id="062b5-230">Questa è l'impostazione predefinita per stereo.</span><span class="sxs-lookup"><span data-stu-id="062b5-230">This is the default setting for stereo.</span></span> |
| <span data-ttu-id="062b5-231">320</span><span class="sxs-lookup"><span data-stu-id="062b5-231">320</span></span>             | <span data-ttu-id="062b5-232">40000</span><span class="sxs-lookup"><span data-stu-id="062b5-232">40000</span></span>                                                                                    | <span data-ttu-id="062b5-233">Solo stereo.</span><span class="sxs-lookup"><span data-stu-id="062b5-233">Stereo only.</span></span>                                            |
| <span data-ttu-id="062b5-234">384</span><span class="sxs-lookup"><span data-stu-id="062b5-234">384</span></span>             | <span data-ttu-id="062b5-235">48000</span><span class="sxs-lookup"><span data-stu-id="062b5-235">48000</span></span>                                                                                    | <span data-ttu-id="062b5-236">Solo stereo.</span><span class="sxs-lookup"><span data-stu-id="062b5-236">Stereo only.</span></span>                                            |
| <span data-ttu-id="062b5-237">448</span><span class="sxs-lookup"><span data-stu-id="062b5-237">448</span></span>             | <span data-ttu-id="062b5-238">56000</span><span class="sxs-lookup"><span data-stu-id="062b5-238">56000</span></span>                                                                                    | <span data-ttu-id="062b5-239">Solo stereo.</span><span class="sxs-lookup"><span data-stu-id="062b5-239">Stereo only.</span></span>                                            |



 

<span data-ttu-id="062b5-240">La velocità in bit di codifica predefinita è impostata su 256 kbps per stereo e 192 kbps per mono.</span><span class="sxs-lookup"><span data-stu-id="062b5-240">The default encoding bit rate is set at 256 kbps for stereo and 192 kbps for mono.</span></span> <span data-ttu-id="062b5-241">Le impostazioni predefinite sono riflesse nei tipi di supporto restituiti dal metodo [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) del codificatore.</span><span class="sxs-lookup"><span data-stu-id="062b5-241">The default settings are reflected in the media types returned by the encoder's [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

### <a name="example-media-types"></a><span data-ttu-id="062b5-242">Tipi di supporti di esempio</span><span class="sxs-lookup"><span data-stu-id="062b5-242">Example Media Types</span></span>

<span data-ttu-id="062b5-243">Di seguito è riportato un esempio dei tipi di supporto necessari per codificare un PCM a 16 bit di tipo Integer, audio stereo 48-kHz alla velocità in bit predefinita di 256 kbps.</span><span class="sxs-lookup"><span data-stu-id="062b5-243">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate of 256 kbps.</span></span>

<span data-ttu-id="062b5-244">Tipo di supporto di output:</span><span class="sxs-lookup"><span data-stu-id="062b5-244">Output media type:</span></span>

| <span data-ttu-id="062b5-245">Attributo</span><span class="sxs-lookup"><span data-stu-id="062b5-245">Attribute</span></span>                                                                           | <span data-ttu-id="062b5-246">Valore</span><span class="sxs-lookup"><span data-stu-id="062b5-246">Value</span></span>                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="062b5-247">\_ \_ tipo principale MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="062b5-247">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="062b5-248">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="062b5-248">**MFMediaType\_Audio**</span></span>        |
| [<span data-ttu-id="062b5-249">sottotipo MF \_ mt \_</span><span class="sxs-lookup"><span data-stu-id="062b5-249">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="062b5-250">**MFAudioFormat \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="062b5-250">**MFAudioFormat\_Dolby\_AC3**</span></span> |
| [<span data-ttu-id="062b5-251">\_ \_ campioni audio MF \_ mt \_ al \_ secondo</span><span class="sxs-lookup"><span data-stu-id="062b5-251">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="062b5-252">48000</span><span class="sxs-lookup"><span data-stu-id="062b5-252">48000</span></span>                         |
| [<span data-ttu-id="062b5-253">numero \_ di \_ \_ canali audio MF mt \_</span><span class="sxs-lookup"><span data-stu-id="062b5-253">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="062b5-254">2</span><span class="sxs-lookup"><span data-stu-id="062b5-254">2</span></span>                             |



 

<span data-ttu-id="062b5-255">Tipo di supporto di input:</span><span class="sxs-lookup"><span data-stu-id="062b5-255">Input media type:</span></span>

| <span data-ttu-id="062b5-256">Attributo</span><span class="sxs-lookup"><span data-stu-id="062b5-256">Attribute</span></span>                                                                                | <span data-ttu-id="062b5-257">Valore</span><span class="sxs-lookup"><span data-stu-id="062b5-257">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="062b5-258">\_ \_ tipo principale MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="062b5-258">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="062b5-259">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="062b5-259">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="062b5-260">sottotipo MF \_ mt \_</span><span class="sxs-lookup"><span data-stu-id="062b5-260">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="062b5-261">**\_PCM MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="062b5-261">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="062b5-262">\_ \_ bit audio MF \_ mt \_ per \_ campione</span><span class="sxs-lookup"><span data-stu-id="062b5-262">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="062b5-263">16</span><span class="sxs-lookup"><span data-stu-id="062b5-263">16</span></span>                     |
| [<span data-ttu-id="062b5-264">\_ \_ campioni audio MF \_ mt \_ al \_ secondo</span><span class="sxs-lookup"><span data-stu-id="062b5-264">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="062b5-265">48000</span><span class="sxs-lookup"><span data-stu-id="062b5-265">48000</span></span>                  |
| [<span data-ttu-id="062b5-266">numero \_ di \_ \_ canali audio MF mt \_</span><span class="sxs-lookup"><span data-stu-id="062b5-266">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="062b5-267">2</span><span class="sxs-lookup"><span data-stu-id="062b5-267">2</span></span>                      |
| [<span data-ttu-id="062b5-268">\_ \_ \_ allineamento blocchi audio MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="062b5-268">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="062b5-269">4</span><span class="sxs-lookup"><span data-stu-id="062b5-269">4</span></span>                      |
| [<span data-ttu-id="062b5-270">\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo</span><span class="sxs-lookup"><span data-stu-id="062b5-270">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="062b5-271">192000</span><span class="sxs-lookup"><span data-stu-id="062b5-271">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="062b5-272">Requisiti</span><span class="sxs-lookup"><span data-stu-id="062b5-272">Requirements</span></span>



| <span data-ttu-id="062b5-273">Requisito</span><span class="sxs-lookup"><span data-stu-id="062b5-273">Requirement</span></span> | <span data-ttu-id="062b5-274">Valore</span><span class="sxs-lookup"><span data-stu-id="062b5-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="062b5-275">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="062b5-275">Minimum supported client</span></span><br/> | <span data-ttu-id="062b5-276">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="062b5-276">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                       |
| <span data-ttu-id="062b5-277">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="062b5-277">Minimum supported server</span></span><br/> | <span data-ttu-id="062b5-278">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="062b5-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="062b5-279">DLL</span><span class="sxs-lookup"><span data-stu-id="062b5-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="062b5-280"><dt>Msac3enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="062b5-280"><dt>Msac3enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="062b5-281">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="062b5-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="062b5-282">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="062b5-282">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 




