---
description: Microsoft Media Foundation.
ms.assetid: 4C397139-6553-4707-B737-7C31C5D423BA
title: Codificatore audio MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea2b22d2fe8cd51f9a2990970493e0415f34d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049663"
---
# <a name="mp3-audio-encoder"></a><span data-ttu-id="3bdd1-103">Codificatore audio MP3</span><span class="sxs-lookup"><span data-stu-id="3bdd1-103">MP3 Audio Encoder</span></span>

<span data-ttu-id="3bdd1-104">Il codificatore audio Microsoft Media Foundation MP3 è una [trasformazione di Media Foundation](media-foundation-transforms.md) (MFT) che codifica audio MPEG-1 Layer 3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="3bdd1-104">The Microsoft Media Foundation MP3 audio encoder is a [Media Foundation Transform](media-foundation-transforms.md) (MFT) that encodes MPEG-1 layer 3 (MP3) audio.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="3bdd1-105">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="3bdd1-105">Class Identifier</span></span>

<span data-ttu-id="3bdd1-106">L'identificatore di classe (CLSID) del codificatore MP3 è **CLSID \_ MP3ACMCodecWrapper**, definito nel file di intestazione wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-106">The class identifier (CLSID) of the MP3 encoder is **CLSID\_MP3ACMCodecWrapper**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="3bdd1-107">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="3bdd1-107">Media Types</span></span>

<span data-ttu-id="3bdd1-108">Il codificatore MP3 supporta i tipi di supporto seguenti.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-108">The MP3 encoder supports the following media types.</span></span> <span data-ttu-id="3bdd1-109">Il tipo di output deve essere impostato prima del tipo di input.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-109">The output type must be set before the input type.</span></span>

### <a name="output-types"></a><span data-ttu-id="3bdd1-110">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="3bdd1-110">Output Types</span></span>

<span data-ttu-id="3bdd1-111">Impostare gli attributi seguenti sul tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-111">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3bdd1-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="3bdd1-112">Attribute</span></span></th>
<th><span data-ttu-id="3bdd1-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bdd1-113">Description</span></span></th>
<th><span data-ttu-id="3bdd1-114">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="3bdd1-114">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3bdd1-115"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3bdd1-115"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="3bdd1-116">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-116">Major type.</span></span></td>
<td><span data-ttu-id="3bdd1-117">Deve essere <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-117">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3bdd1-118"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3bdd1-118"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="3bdd1-119">Sottotipo audio.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-119">Audio subtype.</span></span></td>
<td><span data-ttu-id="3bdd1-120">Deve essere <strong>MFAudioFormat_MP3</strong>.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-120">Must be <strong>MFAudioFormat_MP3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3bdd1-121"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="3bdd1-121"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="3bdd1-122">Velocità in bit del flusso MP3 codificato, in byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-122">Bit rate of the encoded MP3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="3bdd1-123">Il codificatore supporta tutte le velocità in bit definite dallo standard (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256 o 320 Kbps).</span><span class="sxs-lookup"><span data-stu-id="3bdd1-123">The encoder supports all bit rates defined by the standard (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, or 320 Kbps).</span></span><br/> <span data-ttu-id="3bdd1-124">Le velocità in bit predefinite sono di 128 kbps per mono e 320 kbps per lo stereo.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-124">The default bit rates are 128 Kbps for mono and 320 Kbps for stereo.</span></span><br/> <span data-ttu-id="3bdd1-125">Utilizzare questo attributo per specificare la velocità in bit codificata.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-125">Use this attribute to specify the encoded bit rate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3bdd1-126"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="3bdd1-126"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="3bdd1-127">Numero di canali.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-127">Number of channels.</span></span></td>
<td><span data-ttu-id="3bdd1-128">Sono supportati i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3bdd1-128">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="3bdd1-129">1 (mono)</span><span class="sxs-lookup"><span data-stu-id="3bdd1-129">1 (mono)</span></span></li>
<li><span data-ttu-id="3bdd1-130">2 (stereo)</span><span class="sxs-lookup"><span data-stu-id="3bdd1-130">2 (stereo)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3bdd1-131"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="3bdd1-131"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="3bdd1-132">Campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-132">Samples per second.</span></span></td>
<td><span data-ttu-id="3bdd1-133">Sono supportati i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3bdd1-133">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="3bdd1-134">48000 (48 KHz)</span><span class="sxs-lookup"><span data-stu-id="3bdd1-134">48000 (48 KHz)</span></span></li>
<li><span data-ttu-id="3bdd1-135">44100 (44,1 KHz)</span><span class="sxs-lookup"><span data-stu-id="3bdd1-135">44100 (44.1 KHz)</span></span></li>
<li><span data-ttu-id="3bdd1-136">32000 (32 KHz)</span><span class="sxs-lookup"><span data-stu-id="3bdd1-136">32000 (32 KHz)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3bdd1-137"><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></span><span class="sxs-lookup"><span data-stu-id="3bdd1-137"><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></span></span></td>
<td><span data-ttu-id="3bdd1-138">Dati codec aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-138">Additional codec data.</span></span></td>
<td><span data-ttu-id="3bdd1-139">Questo attributo contiene i 12 byte della struttura <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> che seguono il membro <strong>wfx</strong> di tale struttura.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-139">This attribute contains the 12 bytes of the <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> structure that follow the <strong>wfx</strong> member of that structure.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3bdd1-140">In alternativa, è possibile compilare una struttura [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) e chiamare [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) per convertire la struttura in un tipo di supporto Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-140">Alternatively, you can fill in an [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) structure and call [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) to convert the structure to a Media Foundation media type.</span></span>

### <a name="input-types"></a><span data-ttu-id="3bdd1-141">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="3bdd1-141">Input Types</span></span>

<span data-ttu-id="3bdd1-142">Impostare gli attributi seguenti sul tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-142">Set the following attributes on the input media type.</span></span>



| <span data-ttu-id="3bdd1-143">Attributo</span><span class="sxs-lookup"><span data-stu-id="3bdd1-143">Attribute</span></span>                                                                               | <span data-ttu-id="3bdd1-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bdd1-144">Description</span></span>         | <span data-ttu-id="3bdd1-145">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="3bdd1-145">Remarks</span></span>                         |
|-----------------------------------------------------------------------------------------|---------------------|---------------------------------|
| [<span data-ttu-id="3bdd1-146">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="3bdd1-146">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="3bdd1-147">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-147">Major type.</span></span>         | <span data-ttu-id="3bdd1-148">Deve essere **MFMediaType \_ audio**.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-148">Must be **MFMediaType\_Audio**.</span></span> |
| [<span data-ttu-id="3bdd1-149">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="3bdd1-149">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="3bdd1-150">Sottotipo.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-150">Subtype.</span></span>            | <span data-ttu-id="3bdd1-151">Deve essere **MFAudioFormat \_ PCM**.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-151">Must be **MFAudioFormat\_PCM**.</span></span> |
| [<span data-ttu-id="3bdd1-152">**\_ \_ bit audio MF \_ mt \_ per \_ campione**</span><span class="sxs-lookup"><span data-stu-id="3bdd1-152">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)       | <span data-ttu-id="3bdd1-153">BITS per campione.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-153">Bits per sample.</span></span>    | <span data-ttu-id="3bdd1-154">Deve essere 16.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-154">Must be 16.</span></span>                     |
| [<span data-ttu-id="3bdd1-155">**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="3bdd1-155">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="3bdd1-156">Campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-156">Samples per second.</span></span> | <span data-ttu-id="3bdd1-157">Deve corrispondere al tipo di output.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-157">Must match the output type.</span></span>     |
| [<span data-ttu-id="3bdd1-158">**numero \_ di \_ \_ canali audio MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="3bdd1-158">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="3bdd1-159">Numero di canali.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-159">Number of channels.</span></span> | <span data-ttu-id="3bdd1-160">Deve corrispondere al tipo di output.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-160">Must match the output type.</span></span>     |



 

<span data-ttu-id="3bdd1-161">Il codificatore supporta solo input PCM a 16 bit di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-161">The encoder supports only 16-bit integer PCM input.</span></span> <span data-ttu-id="3bdd1-162">Non supporta l'input a virgola mobile a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-162">It does not support 32-bit floating point input.</span></span>

### <a name="media-formats"></a><span data-ttu-id="3bdd1-163">Formati multimediali</span><span class="sxs-lookup"><span data-stu-id="3bdd1-163">Media Formats</span></span>

<span data-ttu-id="3bdd1-164">Lo standard MPEG-1 e MPEG-2 definisce i formati audio 252 di livello 3.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-164">The MPEG-1 and MPEG-2 standard defines 252 layer 3 audio formats.</span></span> <span data-ttu-id="3bdd1-165">Il codificatore MP3 supporta lo standard con alcune eccezioni, oltre ad alcuni formati aggiuntivi, come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-165">The MP3 encoder supports the standard with some exceptions, as well as some additional formats, as described below.</span></span> <span data-ttu-id="3bdd1-166">Il livello 3 è definito come segue:</span><span class="sxs-lookup"><span data-stu-id="3bdd1-166">Layer 3 is defined as:</span></span>



| <span data-ttu-id="3bdd1-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bdd1-167">Requirement</span></span> | <span data-ttu-id="3bdd1-168">Valore</span><span class="sxs-lookup"><span data-stu-id="3bdd1-168">Value</span></span> |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3bdd1-169">Canali</span><span class="sxs-lookup"><span data-stu-id="3bdd1-169">Channels</span></span>                         | <span data-ttu-id="3bdd1-170">mono o stereo</span><span class="sxs-lookup"><span data-stu-id="3bdd1-170">mono or stereo</span></span>                                                |
| <span data-ttu-id="3bdd1-171">Velocità di campionamento MPEG-1 in kHz</span><span class="sxs-lookup"><span data-stu-id="3bdd1-171">MPEG-1 sample rates in kHz</span></span>       | <span data-ttu-id="3bdd1-172">44,1, 48, 32</span><span class="sxs-lookup"><span data-stu-id="3bdd1-172">44.1, 48, 32</span></span>                                                  |
| <span data-ttu-id="3bdd1-173">Velocità in bit codificate MPEG-1 in kbps</span><span class="sxs-lookup"><span data-stu-id="3bdd1-173">MPEG-1 encoded bit rates in kbps</span></span> | <span data-ttu-id="3bdd1-174">32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320</span><span class="sxs-lookup"><span data-stu-id="3bdd1-174">32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320</span></span> |
| <span data-ttu-id="3bdd1-175">Velocità di campionamento MPEG-2 in kHz</span><span class="sxs-lookup"><span data-stu-id="3bdd1-175">MPEG-2 sample rates in kHz</span></span>       | <span data-ttu-id="3bdd1-176">8, 11,025, 12, 16, 22,05, 24</span><span class="sxs-lookup"><span data-stu-id="3bdd1-176">8, 11.025, 12, 16, 22.05, 24</span></span>                                  |
| <span data-ttu-id="3bdd1-177">Velocità in bit codificate MPEG-2 in kbps</span><span class="sxs-lookup"><span data-stu-id="3bdd1-177">MPEG-2 encoded bit rates in kbps</span></span> | <span data-ttu-id="3bdd1-178">8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160</span><span class="sxs-lookup"><span data-stu-id="3bdd1-178">8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160</span></span>          |



 

<span data-ttu-id="3bdd1-179">Il codificatore MP3 supporta inoltre i formati seguenti.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-179">The MP3 encoder also supports the following formats.</span></span>



| <span data-ttu-id="3bdd1-180">Frequenza di campionamento</span><span class="sxs-lookup"><span data-stu-id="3bdd1-180">Sample Rate</span></span> | <span data-ttu-id="3bdd1-181">Velocità in bit</span><span class="sxs-lookup"><span data-stu-id="3bdd1-181">Bit Rate</span></span>     | <span data-ttu-id="3bdd1-182">Numero canale</span><span class="sxs-lookup"><span data-stu-id="3bdd1-182">Channel Number</span></span> |
|-------------|--------------|----------------|
| <span data-ttu-id="3bdd1-183">8000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-183">8000</span></span>        | <span data-ttu-id="3bdd1-184">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-184">18000, 20000</span></span> | <span data-ttu-id="3bdd1-185">2</span><span class="sxs-lookup"><span data-stu-id="3bdd1-185">2</span></span>              |
| <span data-ttu-id="3bdd1-186">11025</span><span class="sxs-lookup"><span data-stu-id="3bdd1-186">11025</span></span>       | <span data-ttu-id="3bdd1-187">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-187">18000, 20000</span></span> | <span data-ttu-id="3bdd1-188">1 o 2</span><span class="sxs-lookup"><span data-stu-id="3bdd1-188">1 or 2</span></span>         |
| <span data-ttu-id="3bdd1-189">12000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-189">12000</span></span>       | <span data-ttu-id="3bdd1-190">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-190">18000, 20000</span></span> | <span data-ttu-id="3bdd1-191">1 o 2</span><span class="sxs-lookup"><span data-stu-id="3bdd1-191">1 or 2</span></span>         |
| <span data-ttu-id="3bdd1-192">16000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-192">16000</span></span>       | <span data-ttu-id="3bdd1-193">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-193">18000, 20000</span></span> | <span data-ttu-id="3bdd1-194">1</span><span class="sxs-lookup"><span data-stu-id="3bdd1-194">1</span></span>              |
| <span data-ttu-id="3bdd1-195">32000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-195">32000</span></span>       | <span data-ttu-id="3bdd1-196">144000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-196">144000</span></span>       | <span data-ttu-id="3bdd1-197">1 o 2</span><span class="sxs-lookup"><span data-stu-id="3bdd1-197">1 or 2</span></span>         |
| <span data-ttu-id="3bdd1-198">44100</span><span class="sxs-lookup"><span data-stu-id="3bdd1-198">44100</span></span>       | <span data-ttu-id="3bdd1-199">144000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-199">144000</span></span>       | <span data-ttu-id="3bdd1-200">1 o 2</span><span class="sxs-lookup"><span data-stu-id="3bdd1-200">1 or 2</span></span>         |
| <span data-ttu-id="3bdd1-201">48000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-201">48000</span></span>       | <span data-ttu-id="3bdd1-202">144000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-202">144000</span></span>       | <span data-ttu-id="3bdd1-203">1 o 2</span><span class="sxs-lookup"><span data-stu-id="3bdd1-203">1 or 2</span></span>         |



 

<span data-ttu-id="3bdd1-204">Il codificatore MP3 non supporta i formati seguenti definiti dallo standard.</span><span class="sxs-lookup"><span data-stu-id="3bdd1-204">The MP3 encoder does not support the following formats defined by the standard.</span></span>



| <span data-ttu-id="3bdd1-205">Frequenza di campionamento</span><span class="sxs-lookup"><span data-stu-id="3bdd1-205">Sample Rate</span></span> | <span data-ttu-id="3bdd1-206">Velocità in bit</span><span class="sxs-lookup"><span data-stu-id="3bdd1-206">Bit Rates</span></span>                                    | <span data-ttu-id="3bdd1-207">Numero canale</span><span class="sxs-lookup"><span data-stu-id="3bdd1-207">Channel Number</span></span> |
|-------------|----------------------------------------------|----------------|
| <span data-ttu-id="3bdd1-208">12000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-208">12000</span></span>       | <span data-ttu-id="3bdd1-209">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-209">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="3bdd1-210">1 o 2</span><span class="sxs-lookup"><span data-stu-id="3bdd1-210">1 or 2</span></span>         |
| <span data-ttu-id="3bdd1-211">11025</span><span class="sxs-lookup"><span data-stu-id="3bdd1-211">11025</span></span>       | <span data-ttu-id="3bdd1-212">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-212">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="3bdd1-213">1 o 2</span><span class="sxs-lookup"><span data-stu-id="3bdd1-213">1 or 2</span></span>         |
| <span data-ttu-id="3bdd1-214">8000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-214">8000</span></span>        | <span data-ttu-id="3bdd1-215">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-215">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="3bdd1-216">1 o 2</span><span class="sxs-lookup"><span data-stu-id="3bdd1-216">1 or 2</span></span>         |
| <span data-ttu-id="3bdd1-217">8000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-217">8000</span></span>        | <span data-ttu-id="3bdd1-218">8000, 11025, 12000, 16000, 22050, 24000</span><span class="sxs-lookup"><span data-stu-id="3bdd1-218">8000, 11025, 12000, 16000, 22050, 24000</span></span>      | <span data-ttu-id="3bdd1-219">2</span><span class="sxs-lookup"><span data-stu-id="3bdd1-219">2</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="3bdd1-220">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bdd1-220">Requirements</span></span>



| <span data-ttu-id="3bdd1-221">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bdd1-221">Requirement</span></span> | <span data-ttu-id="3bdd1-222">Valore</span><span class="sxs-lookup"><span data-stu-id="3bdd1-222">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3bdd1-223">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bdd1-223">Minimum supported client</span></span><br/> | <span data-ttu-id="3bdd1-224">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3bdd1-224">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="3bdd1-225">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bdd1-225">Minimum supported server</span></span><br/> | <span data-ttu-id="3bdd1-226">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3bdd1-226">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3bdd1-227">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bdd1-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bdd1-228">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="3bdd1-228">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
