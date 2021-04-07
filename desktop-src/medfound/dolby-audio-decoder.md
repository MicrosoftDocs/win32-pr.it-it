---
description: Il decoder audio Dolby è un MFT che decodifica Dolby Digital (AC-3) e Dolby Digital Plus.
ms.assetid: A968914A-E4C5-4472-8776-C73F5910089A
title: Decoder audio Dolby
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f1d8ca21cb3ab86f1fdbeddf03624aaaffb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749263"
---
# <a name="dolby-audio-decoder"></a><span data-ttu-id="5867f-103">Decoder audio Dolby</span><span class="sxs-lookup"><span data-stu-id="5867f-103">Dolby Audio Decoder</span></span>

<span data-ttu-id="5867f-104">Il decoder audio Dolby è una [trasformazione Media Foundation](media-foundation-transforms.md) (MFT) che decodifica i tipi di flusso seguenti:</span><span class="sxs-lookup"><span data-stu-id="5867f-104">The Dolby audio decoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that decodes the following stream types:</span></span>

-   <span data-ttu-id="5867f-105">Dolby Digital, chiamato anche Dolby AC-3</span><span class="sxs-lookup"><span data-stu-id="5867f-105">Dolby Digital, also called Dolby AC-3</span></span>
-   <span data-ttu-id="5867f-106">Dolby Digital Plus, detto anche Enhanced AC-3 (E-AC-3)</span><span class="sxs-lookup"><span data-stu-id="5867f-106">Dolby Digital Plus, also called Enhanced AC-3 (E-AC-3)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5867f-107">Per le versioni di Windows precedenti a Windows 8, l'implementazione Microsoft della tecnologia Dolby Digital è limitata ai sensi del programma di licenza Dolby Digital per l'uso da parte delle applicazioni Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5867f-107">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="5867f-108">Per ulteriori informazioni su questi formati, vedere la sezione relativa alla revisione B del documento ATSC (Advanced Television Systems Committee) per il documento ATSC ( *Digital Audio Compression standard)*.</span><span class="sxs-lookup"><span data-stu-id="5867f-108">For more information about these formats, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

<span data-ttu-id="5867f-109">Il decodificatore può anche convertire un flusso Dolby Digital Plus in formato Dolby Digital per l'output AC-3 S/PIDF o formattare un flusso Dolby Digital Plus per l'output digitale HDMI.</span><span class="sxs-lookup"><span data-stu-id="5867f-109">The decoder can also convert a Dolby Digital Plus stream to Dolby Digital format for AC-3 S/PIDF output, or format a Dolby Digital Plus stream for HDMI digital output.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="5867f-110">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="5867f-110">Class Identifier</span></span>

<span data-ttu-id="5867f-111">L'identificatore di classe (CLSID) del decodificatore Dolby audio è **CLSID \_ CMSDDPlusDecMFT**, definito nel file di intestazione wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="5867f-111">The class identifier (CLSID) of the Dolby audio decoder is **CLSID\_CMSDDPlusDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="input-types"></a><span data-ttu-id="5867f-112">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="5867f-112">Input Types</span></span>

<span data-ttu-id="5867f-113">Il decodificatore Dolby audio supporta i sottotipi di input seguenti.</span><span class="sxs-lookup"><span data-stu-id="5867f-113">The Dolby audio decoder supports the following input subtypes.</span></span>



| <span data-ttu-id="5867f-114">Subtype</span><span class="sxs-lookup"><span data-stu-id="5867f-114">Subtype</span></span>                                 | <span data-ttu-id="5867f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5867f-115">Description</span></span>                                                                                                                                                 | <span data-ttu-id="5867f-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5867f-116">Header</span></span>       |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="5867f-117">**MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="5867f-117">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span>            | <span data-ttu-id="5867f-118">Audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="5867f-118">Dolby Digital audio.</span></span>                                                                                                                                        | <span data-ttu-id="5867f-119">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="5867f-119">mfapi.h</span></span>      |
| <span data-ttu-id="5867f-120">**\_DVM MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="5867f-120">**MEDIASUBTYPE\_DVM**</span></span>                   | <span data-ttu-id="5867f-121">Audio Dolby Digital; vedere [**sottotipi audio**](../directshow/audio-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="5867f-121">Dolby Digital audio; see [**Audio Subtypes**](../directshow/audio-subtypes.md).</span></span> <span data-ttu-id="5867f-122">Questo sottotipo può essere usato in modo interscambiabile con **MEDIASUBTYPE \_ Dolby \_ AC3**.</span><span class="sxs-lookup"><span data-stu-id="5867f-122">This subtype can be used interchangeably with **MEDIASUBTYPE\_DOLBY\_AC3**.</span></span><br/> | <span data-ttu-id="5867f-123">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="5867f-123">wmcodecdsp.h</span></span> |
| <span data-ttu-id="5867f-124">**MFAudioFormat \_ Dolby \_ Digital \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="5867f-124">**MFAudioFormat\_Dolby\_Digital\_Plus**</span></span> | <span data-ttu-id="5867f-125">Audio Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="5867f-125">Dolby Digital Plus audio.</span></span>                                                                                                                                   | <span data-ttu-id="5867f-126">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="5867f-126">mfapi.h</span></span>      |



 

<span data-ttu-id="5867f-127">Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="5867f-127">The following table lists the requires and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5867f-128">Attributo</span><span class="sxs-lookup"><span data-stu-id="5867f-128">Attribute</span></span></th>
<th><span data-ttu-id="5867f-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5867f-129">Description</span></span></th>
<th><span data-ttu-id="5867f-130">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="5867f-130">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5867f-131"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="5867f-131"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="5867f-132">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="5867f-132">Major type.</span></span></td>
<td><span data-ttu-id="5867f-133">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5867f-133">Required.</span></span> <span data-ttu-id="5867f-134">Deve essere <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="5867f-134">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5867f-135"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="5867f-135"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="5867f-136">Sottotipo audio.</span><span class="sxs-lookup"><span data-stu-id="5867f-136">Audio subtype.</span></span></td>
<td><span data-ttu-id="5867f-137">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5867f-137">Required.</span></span> <span data-ttu-id="5867f-138">Per informazioni dettagliate, vedere la tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="5867f-138">See the previous table for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5867f-139"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="5867f-139"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="5867f-140">Frequenza di campionamento, in campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="5867f-140">Sample rate, in samples per second.</span></span></td>
<td><span data-ttu-id="5867f-141">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5867f-141">Optional.</span></span> <span data-ttu-id="5867f-142">I valori validi sono: 48000, 44100, 32000, 24000, 22050 e 16000.</span><span class="sxs-lookup"><span data-stu-id="5867f-142">Valid values are: 48000, 44100, 32000, 24000, 22050, and 16000.</span></span> <span data-ttu-id="5867f-143">Se questo attributo non è impostato, il valore predefinito è 48000.</span><span class="sxs-lookup"><span data-stu-id="5867f-143">If this attribute is not set, the default value is 48000.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5867f-144">I flussi Dolby AC-3 sono limitati alle tre tariffe più elevate in questo elenco.</span><span class="sxs-lookup"><span data-stu-id="5867f-144">Dolby AC-3 streams are limited to the three highest rates in this list.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5867f-145"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="5867f-145"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="5867f-146">Numero di canali, incluso il canale LFE (Low Frequency), se presente.</span><span class="sxs-lookup"><span data-stu-id="5867f-146">Number of channels, including the low frequency (LFE) channel, if present.</span></span></td>
<td><span data-ttu-id="5867f-147">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5867f-147">Optional.</span></span> <span data-ttu-id="5867f-148">I valori validi sono compresi tra 1 (mono) e 8 (configurazione del canale 7,1).</span><span class="sxs-lookup"><span data-stu-id="5867f-148">Valid values are in the range 1 (mono) to 8 (7.1 channel configuration).</span></span> <span data-ttu-id="5867f-149">Se questo attributo non è impostato, il valore predefinito è 2 (stereo).</span><span class="sxs-lookup"><span data-stu-id="5867f-149">If this attribute is not set, the default value is 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5867f-150"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="5867f-150"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="5867f-151">Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="5867f-151">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="5867f-152">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5867f-152">Optional.</span></span> <span data-ttu-id="5867f-153">Se specificato, il valore deve essere coerente con il numero di canali audio.</span><span class="sxs-lookup"><span data-stu-id="5867f-153">If specified, the value must be consistent with the number of audio channels.</span></span> <span data-ttu-id="5867f-154">Se l'attributo non è impostato, il decodificatore utilizza una maschera di canale predefinita, in base al numero di canali.</span><span class="sxs-lookup"><span data-stu-id="5867f-154">If the attribute is not set, the decoder uses a default channel mask, based on the number of channels.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5867f-155">La tabella seguente elenca le configurazioni del canale Dolby supportate.</span><span class="sxs-lookup"><span data-stu-id="5867f-155">The following table lists the supported Dolby channel configurations.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5867f-156">Configurazione del canale</span><span class="sxs-lookup"><span data-stu-id="5867f-156">Channel configuration</span></span></th>
<th><span data-ttu-id="5867f-157">Numero di canali</span><span class="sxs-lookup"><span data-stu-id="5867f-157">Number of channels</span></span></th>
<th><span data-ttu-id="5867f-158">Maschere del canale</span><span class="sxs-lookup"><span data-stu-id="5867f-158">Channel masks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5867f-159">1/0 (mono)</span><span class="sxs-lookup"><span data-stu-id="5867f-159">1/0 (mono)</span></span></td>
<td><span data-ttu-id="5867f-160">1</span><span class="sxs-lookup"><span data-stu-id="5867f-160">1</span></span></td>
<td><span data-ttu-id="5867f-161">0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="5867f-161">0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5867f-162">2/0 (stereo) o 1 + 1 (doppio mono)</span><span class="sxs-lookup"><span data-stu-id="5867f-162">2/0 (stereo) or 1+1 (dual mono)</span></span></td>
<td><span data-ttu-id="5867f-163">2</span><span class="sxs-lookup"><span data-stu-id="5867f-163">2</span></span></td>
<td><span data-ttu-id="5867f-164">0x3 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="5867f-164">0x3 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5867f-165">3/0</span><span class="sxs-lookup"><span data-stu-id="5867f-165">3/0</span></span></td>
<td><span data-ttu-id="5867f-166">3</span><span class="sxs-lookup"><span data-stu-id="5867f-166">3</span></span></td>
<td><span data-ttu-id="5867f-167">0x7 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</span><span class="sxs-lookup"><span data-stu-id="5867f-167">0x7 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5867f-168">2/1</span><span class="sxs-lookup"><span data-stu-id="5867f-168">2/1</span></span></td>
<td><span data-ttu-id="5867f-169">3</span><span class="sxs-lookup"><span data-stu-id="5867f-169">3</span></span></td>
<td><span data-ttu-id="5867f-170">0x103 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="5867f-170">0x103 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_CENTER</strong>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5867f-171">3/1</span><span class="sxs-lookup"><span data-stu-id="5867f-171">3/1</span></span></td>
<td><span data-ttu-id="5867f-172">4</span><span class="sxs-lookup"><span data-stu-id="5867f-172">4</span></span></td>
<td><span data-ttu-id="5867f-173">0x107 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="5867f-173">0x107 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_CENTER</strong>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5867f-174">2/2</span><span class="sxs-lookup"><span data-stu-id="5867f-174">2/2</span></span></td>
<td><span data-ttu-id="5867f-175">4</span><span class="sxs-lookup"><span data-stu-id="5867f-175">4</span></span></td>
<td><span data-ttu-id="5867f-176">0x33 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="5867f-176">0x33 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="5867f-177">oppure</span><span class="sxs-lookup"><span data-stu-id="5867f-177">or</span></span><br/> <span data-ttu-id="5867f-178">0x603 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="5867f-178">0x603 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5867f-179">3/2</span><span class="sxs-lookup"><span data-stu-id="5867f-179">3/2</span></span></td>
<td><span data-ttu-id="5867f-180">5</span><span class="sxs-lookup"><span data-stu-id="5867f-180">5</span></span></td>
<td><span data-ttu-id="5867f-181">0x37 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="5867f-181">0x37 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="5867f-182">oppure</span><span class="sxs-lookup"><span data-stu-id="5867f-182">or</span></span><br/> <span data-ttu-id="5867f-183">0x607 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="5867f-183">0x607 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5867f-184">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="5867f-184">3/2 + LFE</span></span></td>
<td><span data-ttu-id="5867f-185">6</span><span class="sxs-lookup"><span data-stu-id="5867f-185">6</span></span></td>
<td><span data-ttu-id="5867f-186">0x3F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="5867f-186">0x3F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="5867f-187">oppure</span><span class="sxs-lookup"><span data-stu-id="5867f-187">or</span></span><br/> <span data-ttu-id="5867f-188">0x60F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="5867f-188">0x60F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5867f-189">3/2/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="5867f-189">3/2/2 + LFE</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5867f-190">Solo Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="5867f-190">Dolby Digital Plus only.</span></span>
</blockquote>
<br/> <br/></td>
<td><span data-ttu-id="5867f-191">8</span><span class="sxs-lookup"><span data-stu-id="5867f-191">8</span></span></td>
<td><span data-ttu-id="5867f-192">0x63F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</span><span class="sxs-lookup"><span data-stu-id="5867f-192">0x63F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5867f-193">Inoltre, le configurazioni di canale 1/0, 2/0, 3/0, 2/1, 3/1 e 2/2 possono essere visualizzate anche con un canale LFE.</span><span class="sxs-lookup"><span data-stu-id="5867f-193">In addition, channel configurations 1/0, 2/0, 3/0, 2/1, 3/1, and 2/2 may also appear with an LFE channel.</span></span>

## <a name="output-types"></a><span data-ttu-id="5867f-194">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="5867f-194">Output Types</span></span>

<span data-ttu-id="5867f-195">Il decodificatore Dolby audio supporta i sottotipi di output seguenti.</span><span class="sxs-lookup"><span data-stu-id="5867f-195">The Dolby audio decoder supports the following output subtypes.</span></span>



| <span data-ttu-id="5867f-196">Subtype</span><span class="sxs-lookup"><span data-stu-id="5867f-196">Subtype</span></span>                                                   | <span data-ttu-id="5867f-197">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5867f-197">Description</span></span>                                                                                                                               | <span data-ttu-id="5867f-198">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5867f-198">Header</span></span>    |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5867f-199">**MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**</span><span class="sxs-lookup"><span data-stu-id="5867f-199">**MFAudioFormat\_Dolby\_AC3\_SPDIF**</span></span>                      | <span data-ttu-id="5867f-200">Audio Dolby AC-3 formattato per l'output digitale S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="5867f-200">Dolby AC-3 audio formatted for S/PDIF digital output.</span></span>                                                                                     | <span data-ttu-id="5867f-201">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="5867f-201">mfapi.h</span></span>   |
| <span data-ttu-id="5867f-202">**\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ Digital \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="5867f-202">**KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS**</span></span> | <span data-ttu-id="5867f-203">Dolby Digital Plus audio formattato per l'output digitale HDMI.</span><span class="sxs-lookup"><span data-stu-id="5867f-203">Dolby Digital Plus audio formatted for HDMI digital output.</span></span>                                                                               | <span data-ttu-id="5867f-204">ksmedia. h</span><span class="sxs-lookup"><span data-stu-id="5867f-204">ksmedia.h</span></span> |
| <span data-ttu-id="5867f-205">**\_Float MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="5867f-205">**MFAudioFormat\_Float**</span></span>                                  | <span data-ttu-id="5867f-206">Audio PCM a virgola mobile IEEE a 32 bit</span><span class="sxs-lookup"><span data-stu-id="5867f-206">IEEE 32-bit floating-point PCM audio</span></span><br/> <span data-ttu-id="5867f-207">**Windows 10**: stereo, 5,1, 7,1</span><span class="sxs-lookup"><span data-stu-id="5867f-207">**Windows 10**: stereo, 5.1, 7.1</span></span><br/> <span data-ttu-id="5867f-208">**Versioni precedenti**: stereo, 5,1</span><span class="sxs-lookup"><span data-stu-id="5867f-208">**Previous versions**: stereo, 5.1</span></span><br/> | <span data-ttu-id="5867f-209">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="5867f-209">mfapi.h</span></span>   |
| <span data-ttu-id="5867f-210">**\_PCM MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="5867f-210">**MFAudioFormat\_PCM**</span></span>                                    | <span data-ttu-id="5867f-211">audio PCM a 16 bit</span><span class="sxs-lookup"><span data-stu-id="5867f-211">16-bit PCM audio</span></span><br/> <span data-ttu-id="5867f-212">**Windows 10**: stereo, 5,1, 7,1</span><span class="sxs-lookup"><span data-stu-id="5867f-212">**Windows 10**: stereo, 5.1, 7.1</span></span><br/> <span data-ttu-id="5867f-213">**Versioni precedenti**: stereo, 5,1</span><span class="sxs-lookup"><span data-stu-id="5867f-213">**Previous versions**: stereo, 5.1</span></span><br/>                     | <span data-ttu-id="5867f-214">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="5867f-214">mfapi.h</span></span>   |



 

<span data-ttu-id="5867f-215">Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="5867f-215">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5867f-216">Attributo</span><span class="sxs-lookup"><span data-stu-id="5867f-216">Attribute</span></span></th>
<th><span data-ttu-id="5867f-217">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5867f-217">Description</span></span></th>
<th><span data-ttu-id="5867f-218">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="5867f-218">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5867f-219"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="5867f-219"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="5867f-220">Tipo principale.</span><span class="sxs-lookup"><span data-stu-id="5867f-220">Major type.</span></span></td>
<td><span data-ttu-id="5867f-221">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5867f-221">Required.</span></span> <span data-ttu-id="5867f-222">Deve essere <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="5867f-222">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5867f-223"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="5867f-223"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="5867f-224">Sottotipo audio.</span><span class="sxs-lookup"><span data-stu-id="5867f-224">Audio subtype.</span></span></td>
<td><span data-ttu-id="5867f-225">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5867f-225">Required.</span></span> <span data-ttu-id="5867f-226">Per informazioni dettagliate, vedere la tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="5867f-226">See the previous table for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5867f-227"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="5867f-227"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="5867f-228">Frequenza di campionamento, in campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="5867f-228">Sample rate, in samples per second.</span></span></td>
<td><span data-ttu-id="5867f-229">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5867f-229">Required.</span></span> <span data-ttu-id="5867f-230">I valori validi sono: 48000, 44100, 32000, 24000, 22050 e 16000.</span><span class="sxs-lookup"><span data-stu-id="5867f-230">Valid values are: 48000, 44100, 32000, 24000, 22050, and 16000.</span></span> <span data-ttu-id="5867f-231">La frequenza di campionamento dell'output deve essere identica alla frequenza di campionamento di input.</span><span class="sxs-lookup"><span data-stu-id="5867f-231">The output sample rate must be identical to the input sample rate.</span></span> <span data-ttu-id="5867f-232">Il decodificatore non può modificare la frequenza di campionamento del flusso.</span><span class="sxs-lookup"><span data-stu-id="5867f-232">The decoder cannot change the sampling rate of the stream.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5867f-233"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="5867f-233"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="5867f-234">Numero di canali, incluso il canale LFE (Low Frequency), se presente.</span><span class="sxs-lookup"><span data-stu-id="5867f-234">Number of channels, including the low frequency (LFE) channel, if present.</span></span></td>
<td><span data-ttu-id="5867f-235">Obbligatorio per l'output del PCM.</span><span class="sxs-lookup"><span data-stu-id="5867f-235">Required for PCM output.</span></span> <br/> <span data-ttu-id="5867f-236">Non necessario per l'output digitale.</span><span class="sxs-lookup"><span data-stu-id="5867f-236">Not needed for digital output.</span></span> <br/> <span data-ttu-id="5867f-237">Se il tipo di input è mono, stereo o dual-mono (tutti senza canale LFE), l'unico valore valido è 2, per l'output stereo.</span><span class="sxs-lookup"><span data-stu-id="5867f-237">If the input type is mono, stereo, or dual-mono (all without LFE channel), the only valid value is 2, for stereo output.</span></span> <span data-ttu-id="5867f-238">In caso contrario, il valore può essere:</span><span class="sxs-lookup"><span data-stu-id="5867f-238">Otherwise, the value can be:</span></span> <br/>
<ul>
<li><span data-ttu-id="5867f-239">2 per downmix stereo</span><span class="sxs-lookup"><span data-stu-id="5867f-239">2 for stereo downmix</span></span></li>
<li><span data-ttu-id="5867f-240">6 per le configurazioni di canale 5,1</span><span class="sxs-lookup"><span data-stu-id="5867f-240">6 for 5.1 channel configurations</span></span></li>
<li><span data-ttu-id="5867f-241">8 per le configurazioni di canale 7,1</span><span class="sxs-lookup"><span data-stu-id="5867f-241">8 for 7.1 channel configurations</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5867f-242"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="5867f-242"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="5867f-243">Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="5867f-243">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="5867f-244">Obbligatorio per l'output PCM se il numero di canali è maggiore di 2.</span><span class="sxs-lookup"><span data-stu-id="5867f-244">Required for PCM output if the number of channels is greater than 2.</span></span> <span data-ttu-id="5867f-245">Il valore deve essere:</span><span class="sxs-lookup"><span data-stu-id="5867f-245">The value must be:</span></span><br/>
<ul>
<li><span data-ttu-id="5867f-246">0x3 per output stereo</span><span class="sxs-lookup"><span data-stu-id="5867f-246">0x3 for stereo output</span></span></li>
<li><span data-ttu-id="5867f-247">0x3F per l'output del canale 5,1</span><span class="sxs-lookup"><span data-stu-id="5867f-247">0x3F for 5.1 channel output</span></span></li>
<li><span data-ttu-id="5867f-248">0x63F per l'output del canale 7,1</span><span class="sxs-lookup"><span data-stu-id="5867f-248">0x63F for 7.1 channel output</span></span></li>
</ul>
<span data-ttu-id="5867f-249">Non necessario per l'output digitale.</span><span class="sxs-lookup"><span data-stu-id="5867f-249">Not needed for digital output.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5867f-250"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="5867f-250"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="5867f-251">Numero di bit per esempio audio.</span><span class="sxs-lookup"><span data-stu-id="5867f-251">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="5867f-252">Obbligatorio per l'output del PCM.</span><span class="sxs-lookup"><span data-stu-id="5867f-252">Required for PCM output.</span></span> <span data-ttu-id="5867f-253">Il valore deve essere 32 per <strong>MFAudioFormat_Float</strong>e 16 per <strong>MFAudioFormat_PCM</strong>.</span><span class="sxs-lookup"><span data-stu-id="5867f-253">The value must be 32 for <strong>MFAudioFormat_Float</strong>, and 16 for <strong>MFAudioFormat_PCM</strong>.</span></span><br/> <span data-ttu-id="5867f-254">Non necessario per l'output digitale.</span><span class="sxs-lookup"><span data-stu-id="5867f-254">Not needed for digital output.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5867f-255"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="5867f-255"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="5867f-256">Numero di bit validi di dati audio in ogni esempio audio.</span><span class="sxs-lookup"><span data-stu-id="5867f-256">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="5867f-257">Facoltativo per l'output del PCM.</span><span class="sxs-lookup"><span data-stu-id="5867f-257">Optional for PCM output.</span></span> <span data-ttu-id="5867f-258">Se impostato, il valore deve essere identico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="5867f-258">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span><br/> <span data-ttu-id="5867f-259">Non necessario per i sottotipi di output digitali.</span><span class="sxs-lookup"><span data-stu-id="5867f-259">Not needed for the digital output subtypes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5867f-260"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="5867f-260"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="5867f-261">Allineamento del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="5867f-261">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="5867f-262">Facoltativo per l'output del PCM.</span><span class="sxs-lookup"><span data-stu-id="5867f-262">Optional for PCM output.</span></span> <span data-ttu-id="5867f-263">Non necessario per l'output digitale.</span><span class="sxs-lookup"><span data-stu-id="5867f-263">Not needed for digital output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5867f-264"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="5867f-264"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="5867f-265">Numero medio di byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="5867f-265">Average number of bytes per second.</span></span></td>
<td><span data-ttu-id="5867f-266">Facoltativo per l'output del PCM.</span><span class="sxs-lookup"><span data-stu-id="5867f-266">Optional for PCM output.</span></span> <span data-ttu-id="5867f-267">Non necessario per l'output digitale.</span><span class="sxs-lookup"><span data-stu-id="5867f-267">Not needed for digital output.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="transform-attributes"></a><span data-ttu-id="5867f-268">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="5867f-268">Transform Attributes</span></span>

<span data-ttu-id="5867f-269">Il decoder audio Dolby implementa il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="5867f-269">The Dolby audio decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="5867f-270">L'applicazione può utilizzare questo metodo per ottenere o impostare gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5867f-270">The application can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="5867f-271">Attributo</span><span class="sxs-lookup"><span data-stu-id="5867f-271">Attribute</span></span>                                                                                | <span data-ttu-id="5867f-272">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5867f-272">Description</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5867f-273">Codecapis \_ AVDecAudioDualMono</span><span class="sxs-lookup"><span data-stu-id="5867f-273">CODECAPI\_AVDecAudioDualMono</span></span>](../directshow/avdecaudiodualmono-property.md)                        | <span data-ttu-id="5867f-274">Specifica se un flusso audio Dolby a 2 canali è codificato come stereo o dual-mono.</span><span class="sxs-lookup"><span data-stu-id="5867f-274">Specifies whether a 2-channel Dolby audio stream is encoded as stereo or dual-mono.</span></span> <span data-ttu-id="5867f-275">Prima che il primo frame Dolby venga decodificato, il valore è **eAVDecAudioDualMono non \_ specificato**.</span><span class="sxs-lookup"><span data-stu-id="5867f-275">Before the first Dolby frame is decoded, the value is **eAVDecAudioDualMono\_UnSpecified**.</span></span> <span data-ttu-id="5867f-276">Dopo l'inizio della decodifica, il valore riflette il frame Dolby più recente.</span><span class="sxs-lookup"><span data-stu-id="5867f-276">After decoding begins, the value reflects the most recent Dolby frame.</span></span><br/> <span data-ttu-id="5867f-277">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5867f-277">Read-only.</span></span> <br/> |
| [<span data-ttu-id="5867f-278">Codecapis \_ AVDecAudioDualMonoReproMode</span><span class="sxs-lookup"><span data-stu-id="5867f-278">CODECAPI\_AVDecAudioDualMonoReproMode</span></span>](../directshow/avdecaudiodualmonorepromode-property.md)      | <span data-ttu-id="5867f-279">Specifica la modalità di riproduzione audio dual-mono da parte del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="5867f-279">Specifies how the decoder reproduces dual-mono audio.</span></span> <span data-ttu-id="5867f-280">Il valore predefinito è **eAVDecAudioDualMonoReproMode \_ Left \_ mono**.</span><span class="sxs-lookup"><span data-stu-id="5867f-280">The default value is **eAVDecAudioDualMonoReproMode\_LEFT\_MONO**.</span></span> <span data-ttu-id="5867f-281">L'applicazione può impostare questa proprietà in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="5867f-281">The application can set this property at any time.</span></span><br/> <span data-ttu-id="5867f-282">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5867f-282">Read/write.</span></span><br/>                                                                            |
| [<span data-ttu-id="5867f-283">Codecapis \_ AVDecCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="5867f-283">CODECAPI\_AVDecCommonMeanBitRate</span></span>](../directshow/avdeccommonmeanbitrate.md)                         | <span data-ttu-id="5867f-284">Per i flussi Dolby Digital (AC-3), specifica la velocità in bit del flusso di input in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="5867f-284">For Dolby Digital (AC-3) streams, specifies the bit rate of the input stream in bits per second.</span></span> <span data-ttu-id="5867f-285">Per Dolby Digital Plus (E-AC3), il valore è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="5867f-285">For Dolby Digital Plus (E-AC3), the value is always zero.</span></span><br/> <span data-ttu-id="5867f-286">Sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5867f-286">Read only.</span></span><br/>                                                                                              |
| [<span data-ttu-id="5867f-287">Codecapis \_ AVDecDDDynamicRangeScaleHigh</span><span class="sxs-lookup"><span data-stu-id="5867f-287">CODECAPI\_AVDecDDDynamicRangeScaleHigh</span></span>](../directshow/avdecdddynamicrangescalehigh-property.md)    | <span data-ttu-id="5867f-288">Il taglio di alto livello quando il decodificatore esegue il controllo dinamico degli intervalli.</span><span class="sxs-lookup"><span data-stu-id="5867f-288">The high-level cut when the decoder performs dynamic range control.</span></span><br/> <span data-ttu-id="5867f-289">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5867f-289">Read/write.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="5867f-290">Codecapis \_ AVDecDDDynamicRangeScaleLow</span><span class="sxs-lookup"><span data-stu-id="5867f-290">CODECAPI\_AVDecDDDynamicRangeScaleLow</span></span>](../directshow/avdecdddynamicrangescalelow-property.md)      | <span data-ttu-id="5867f-291">Boost di basso livello quando il decodificatore esegue il controllo dinamico degli intervalli.</span><span class="sxs-lookup"><span data-stu-id="5867f-291">The low-level boost when the decoder performs dynamic range control.</span></span><br/> <span data-ttu-id="5867f-292">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5867f-292">Read/write.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="5867f-293">Codecapis \_ AVDecDDOperationalMode</span><span class="sxs-lookup"><span data-stu-id="5867f-293">CODECAPI\_AVDecDDOperationalMode</span></span>](../directshow/avdecddoperationalmode-property.md)                | <span data-ttu-id="5867f-294">Modalità di controllo della compressione.</span><span class="sxs-lookup"><span data-stu-id="5867f-294">The compression control mode.</span></span><br/> <span data-ttu-id="5867f-295">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5867f-295">Read/write.</span></span><br/>                                                                                                                                                                                                                          |
| [<span data-ttu-id="5867f-296">Codecapis \_ AVDecDDStereoDownMixMode</span><span class="sxs-lookup"><span data-stu-id="5867f-296">CODECAPI\_AVDecDDStereoDownMixMode</span></span>](codecapi-avdecddstereodownmixmode.md)              | <span data-ttu-id="5867f-297">Tipo di downmix stereo.</span><span class="sxs-lookup"><span data-stu-id="5867f-297">The type of stereo downmix.</span></span> <span data-ttu-id="5867f-298">Questa proprietà si applica quando l'input è un flusso multicanale e l'output è un flusso stereo.</span><span class="sxs-lookup"><span data-stu-id="5867f-298">This property applies when the input is a multichannel stream and the output is a stereo stream.</span></span><br/> <span data-ttu-id="5867f-299">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5867f-299">Read/write.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="5867f-300">la \_ \_ modifica del \_ formato \_ dinamico del supporto MFT</span><span class="sxs-lookup"><span data-stu-id="5867f-300">MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE</span></span>](mft-support-dynamic-format-change-attribute.md) | <span data-ttu-id="5867f-301">Questo attributo restituisce **false**, che indica che il decodificatore deve essere svuotato prima che venga impostato un nuovo tipo di input.</span><span class="sxs-lookup"><span data-stu-id="5867f-301">This attribute returns **FALSE**, indicating that the decoder must be drained before a new input type is set.</span></span><br/> <span data-ttu-id="5867f-302">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5867f-302">Read/write.</span></span><br/>                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="5867f-303">Commenti</span><span class="sxs-lookup"><span data-stu-id="5867f-303">Remarks</span></span>

<span data-ttu-id="5867f-304">Il decodificatore accetta solo flussi Dolby RAW, come definito da A/52B.</span><span class="sxs-lookup"><span data-stu-id="5867f-304">The decoder accepts only raw Dolby streams, as defined by A/52B.</span></span> <span data-ttu-id="5867f-305">I payload, ad esempio i flussi elementari in pacchetto (PES) non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="5867f-305">Payloads such as Packetized Elementary Streams (PES) are not supported.</span></span> <span data-ttu-id="5867f-306">Per Dolby Digital Plus, il decodificatore decodifica fino a 5,1 canali.</span><span class="sxs-lookup"><span data-stu-id="5867f-306">For Dolby Digital Plus, the decoder decodes up to 5.1 channels.</span></span> <span data-ttu-id="5867f-307">In Windows 10, i flussi di canale 7,1 vengono decodificati senza downmix.</span><span class="sxs-lookup"><span data-stu-id="5867f-307">On Windows 10, 7.1 channel streams are decoded without downmix.</span></span> <span data-ttu-id="5867f-308">Nelle versioni precedenti del sistema operativo, se il flusso è di 7,1 canali, solo il canale 5,1 downmix verrà decodificato.</span><span class="sxs-lookup"><span data-stu-id="5867f-308">On previous OS versions, if the stream is 7.1 channels, only the 5.1 channel downmix will be decoded.</span></span> <span data-ttu-id="5867f-309">Se il flusso è Dolby Digital Plus con più di un sottoflusso indipendente, viene decodificato solo il sottoflusso indipendente 0.</span><span class="sxs-lookup"><span data-stu-id="5867f-309">If the stream is Dolby Digital Plus with more than one independent substream, only independent substream 0 is decoded.</span></span> <span data-ttu-id="5867f-310">Il decodificatore ignora gli altri sottoflussi indipendenti.</span><span class="sxs-lookup"><span data-stu-id="5867f-310">The decoder skips other independent substreams.</span></span> <span data-ttu-id="5867f-311">Il decodificatore ignora inoltre tutti i sottoflussi dipendenti.</span><span class="sxs-lookup"><span data-stu-id="5867f-311">In addition, the decoder skips all dependent substreams.</span></span> <span data-ttu-id="5867f-312">Il decodificatore supporta la decrittografia e la decodifica dei flussi protetti dalla tecnologia di Rights Management digitale (DRM).</span><span class="sxs-lookup"><span data-stu-id="5867f-312">The decoder supports decryption and decoding of streams that are protected by Digital Rights Management (DRM) technology.</span></span>

<span data-ttu-id="5867f-313">Se il tipo di supporto di input ha una configurazione del canale diversa da mono, stereo o dual-mono (tutti senza canale LFE), il decodificatore fornisce due opzioni per le configurazioni del canale di output:</span><span class="sxs-lookup"><span data-stu-id="5867f-313">If the input media type has a channel configuration other than mono, stereo, or dual-mono (all without LFE channel), the decoder provides two options for the output channel configurations:</span></span>

-   <span data-ttu-id="5867f-314">output a 8 canali (configurazione del canale 7,1)</span><span class="sxs-lookup"><span data-stu-id="5867f-314">8-channel output (7.1 channel configuration)</span></span>
-   <span data-ttu-id="5867f-315">output a 6 canali (configurazione del canale 5,1)</span><span class="sxs-lookup"><span data-stu-id="5867f-315">6-channel output (5.1 channel configuration)</span></span>
-   <span data-ttu-id="5867f-316">Downmix stereo</span><span class="sxs-lookup"><span data-stu-id="5867f-316">Stereo downmix</span></span>

<span data-ttu-id="5867f-317">Se è selezionata l'opzione downmix stereo, il tipo di downmix può essere impostato su MFT usando la proprietà [CODEcapis \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) .</span><span class="sxs-lookup"><span data-stu-id="5867f-317">If stereo downmix is selected, the type of downmix can be set on the MFT by using the [CODECAPI\_AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) property.</span></span>

<span data-ttu-id="5867f-318">Se il tipo di output è **MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**, ogni buffer di output contiene 6.144 byte.</span><span class="sxs-lookup"><span data-stu-id="5867f-318">If the output type is **MFAudioFormat\_Dolby\_AC3\_SPDIF**, each output buffer contains 6,144 bytes.</span></span> <span data-ttu-id="5867f-319">Il buffer inizia con un'intestazione S/PDIF a 8 byte, seguita da un frame AC-3 compresso, seguito da un riempimento pari a zero a 6.144 byte.</span><span class="sxs-lookup"><span data-stu-id="5867f-319">The buffer starts with an 8-byte S/PDIF header, followed by a compressed AC-3 frame, followed by zero padding to 6,144 bytes.</span></span>

<span data-ttu-id="5867f-320">Se il tipo di output è **KSDATAFORMAT \_ sottotipo \_ IEC61937 \_ Dolby \_ Digital \_ Plus**, ogni buffer di output contiene 24.576 byte.</span><span class="sxs-lookup"><span data-stu-id="5867f-320">If the output type is **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS**, each output buffer contains 24,576 bytes.</span></span> <span data-ttu-id="5867f-321">Il buffer inizia con un'intestazione S/PDIF a 8 byte, seguita da un frame Dolby Digital Plus compresso da 1 a 6, che corrisponde a campioni PCM 1.536, seguiti da zero padding a 24.576 byte.</span><span class="sxs-lookup"><span data-stu-id="5867f-321">The buffer starts with an 8-byte S/PDIF header, followed by 1–6 compressed Dolby Digital Plus frames corresponding to 1,536 PCM samples, followed by zero padding to 24,576 bytes.</span></span> <span data-ttu-id="5867f-322">Per l'output HDMI, viene compresso solo il substream 0 indipendente.</span><span class="sxs-lookup"><span data-stu-id="5867f-322">For HDMI output, only independent substream 0 is packed.</span></span>

<span data-ttu-id="5867f-323">Il decodificatore MFT viene registrato con il flag di **enumerazione MFT flag \_ \_ \_ FIELDOFUSE**, che indica che il MFT deve essere sbloccato dall'applicazione prima dell'uso.</span><span class="sxs-lookup"><span data-stu-id="5867f-323">The decoder MFT is registered with the flag **MFT\_ENUM\_FLAG\_FIELDOFUSE**, which indicates that the MFT that must be unlocked by the application before use.</span></span> <span data-ttu-id="5867f-324">Per ulteriori informazioni, vedere [restrizioni relative all'utilizzo dei campi](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="5867f-324">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5867f-325">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5867f-325">Requirements</span></span>



| <span data-ttu-id="5867f-326">Requisito</span><span class="sxs-lookup"><span data-stu-id="5867f-326">Requirement</span></span> | <span data-ttu-id="5867f-327">Valore</span><span class="sxs-lookup"><span data-stu-id="5867f-327">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5867f-328">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5867f-328">Minimum supported client</span></span><br/> | <span data-ttu-id="5867f-329">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5867f-329">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="5867f-330">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5867f-330">Minimum supported server</span></span><br/> | <span data-ttu-id="5867f-331">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5867f-331">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="5867f-332">DLL</span><span class="sxs-lookup"><span data-stu-id="5867f-332">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5867f-333"><dt>Msauddecmft.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5867f-333"><dt>Msauddecmft.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5867f-334">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5867f-334">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5867f-335">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="5867f-335">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
