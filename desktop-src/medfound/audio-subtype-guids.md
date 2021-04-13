---
description: GUID del sottotipo audio
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: GUID del sottotipo audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04192f19f530c288b9aef7b5718b8329ea108bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484132"
---
# <a name="audio-subtype-guids"></a><span data-ttu-id="3cc9d-103">GUID del sottotipo audio</span><span class="sxs-lookup"><span data-stu-id="3cc9d-103">Audio Subtype GUIDs</span></span>

<span data-ttu-id="3cc9d-104">Sono definiti i seguenti GUID del sottotipo audio.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-104">The following audio subtype GUIDs are defined.</span></span> <span data-ttu-id="3cc9d-105">Per specificare il sottotipo, impostare l'attributo del [**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md) sul tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-105">To specify the subtype, set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="3cc9d-106">Eccetto dove indicato, queste costanti sono definite nel file di intestazione mfapi. h.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-106">Except where noted, these constants are defined in the header file mfapi.h.</span></span>

<span data-ttu-id="3cc9d-107">Quando si usano questi sottotipi, impostare l'attributo [di \_ \_ \_ tipo principale MF mt](mf-mt-major-type-attribute.md) su **MFMediaType \_ audio**.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-107">When these subtypes are used, set the [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio**.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3cc9d-108">GUID</span><span class="sxs-lookup"><span data-stu-id="3cc9d-108">GUID</span></span></th>
<th><span data-ttu-id="3cc9d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cc9d-109">Description</span></span></th>
<th><span data-ttu-id="3cc9d-110">Tag Format (FOURCC)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-110">Format Tag (FOURCC)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3cc9d-111"><strong>MEDIASUBTYPE_RAW_AAC1</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-111"><strong>MEDIASUBTYPE_RAW_AAC1</strong></span></span></td>
<td><span data-ttu-id="3cc9d-112">Codifica audio avanzata (AAC).</span><span class="sxs-lookup"><span data-stu-id="3cc9d-112">Advanced Audio Coding (AAC).</span></span><br/> <span data-ttu-id="3cc9d-113">Questo sottotipo viene usato per AAC contenuto in un file AVI con un tag di formato audio uguale a 0x00FF.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-113">This subtype is used for AAC contained in an AVI file with an audio format tag equal to 0x00FF.</span></span> <br/> <span data-ttu-id="3cc9d-114">Per altre informazioni, vedere <a href="aac-decoder.md"><strong>decoder AAC</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-114">For more information, see <a href="aac-decoder.md"><strong>AAC Decoder</strong></a>.</span></span><br/> <span data-ttu-id="3cc9d-115">Definito in wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="3cc9d-115">Defined in wmcodecdsp.h</span></span><br/></td>
<td><span data-ttu-id="3cc9d-116">WAVE_FORMAT_RAW_AAC1 (0x00FF)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-116">WAVE_FORMAT_RAW_AAC1 (0x00FF)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc9d-117"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-117"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="3cc9d-118">Codifica audio avanzata (AAC).</span><span class="sxs-lookup"><span data-stu-id="3cc9d-118">Advanced Audio Coding (AAC).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3cc9d-119">Equivale a MEDIASUBTYPE_MPEG_HEAAC, definito in wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-119">Equivalent to MEDIASUBTYPE_MPEG_HEAAC, defined in wmcodecdsp.h.</span></span>
</blockquote>
<br/> <span data-ttu-id="3cc9d-120">Il flusso può contenere dati AAC non elaborati o dati AAC in un flusso ADTS (Audio Data Transport Stream).</span><span class="sxs-lookup"><span data-stu-id="3cc9d-120">The stream can contain raw AAC data or AAC data in an Audio Data Transport Stream (ADTS) stream.</span></span><br/> <span data-ttu-id="3cc9d-121">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="3cc9d-121">For more information, see:</span></span><br/>
<ul>
<li><span data-ttu-id="3cc9d-122"><a href="aac-decoder.md"><strong>Decoder AAC</strong></a></span><span class="sxs-lookup"><span data-stu-id="3cc9d-122"><a href="aac-decoder.md"><strong>AAC Decoder</strong></a></span></span></li>
<li><span data-ttu-id="3cc9d-123"><a href="mpeg-4-file-source.md">Origine file MPEG-4</a></span><span class="sxs-lookup"><span data-stu-id="3cc9d-123"><a href="mpeg-4-file-source.md">MPEG-4 File Source</a></span></span></li>
</ul></td>
<td><span data-ttu-id="3cc9d-124">WAVE_FORMAT_MPEG_HEAAC (0x1610)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-124">WAVE_FORMAT_MPEG_HEAAC (0x1610)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc9d-125"><strong>MFAudioFormat_ADTS</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-125"><strong>MFAudioFormat_ADTS</strong></span></span></td>
<td><span data-ttu-id="3cc9d-126">Non usato.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-126">Not used.</span></span></td>
<td><span data-ttu-id="3cc9d-127">WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-127">WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc9d-128"><strong>MFAudioFormat_ALAC</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-128"><strong>MFAudioFormat_ALAC</strong></span></span></td>
<td><span data-ttu-id="3cc9d-129">Codec audio Apple Lossless</span><span class="sxs-lookup"><span data-stu-id="3cc9d-129">Apple Lossless Audio Codec</span></span><br/> <span data-ttu-id="3cc9d-130">Supportato in Windows 10 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-130">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="3cc9d-131">WAVE_FORMAT_ALAC (0x6C61)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-131">WAVE_FORMAT_ALAC (0x6C61)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc9d-132"><strong>MFAudioFormat_AMR_NB</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-132"><strong>MFAudioFormat_AMR_NB</strong></span></span></td>
<td><span data-ttu-id="3cc9d-133">Audio multifrequenza adattativi</span><span class="sxs-lookup"><span data-stu-id="3cc9d-133">Adaptative Multi-Rate audio</span></span><br/> <span data-ttu-id="3cc9d-134">Supportato in Windows 8.1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-134">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="3cc9d-135">WAVE_FORMAT_AMR_NB</span><span class="sxs-lookup"><span data-stu-id="3cc9d-135">WAVE_FORMAT_AMR_NB</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc9d-136"><strong>MFAudioFormat_AMR_WB</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-136"><strong>MFAudioFormat_AMR_WB</strong></span></span></td>
<td><span data-ttu-id="3cc9d-137">Audio a banda larga multifrequenza adattativi</span><span class="sxs-lookup"><span data-stu-id="3cc9d-137">Adaptative Multi-Rate Wideband audio</span></span><br/> <span data-ttu-id="3cc9d-138">Supportato in Windows 8.1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-138">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="3cc9d-139">WAVE_FORMAT_AMR_WB</span><span class="sxs-lookup"><span data-stu-id="3cc9d-139">WAVE_FORMAT_AMR_WB</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc9d-140"><strong>MFAudioFormat_AMR_WP</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-140"><strong>MFAudioFormat_AMR_WP</strong></span></span></td>
<td><span data-ttu-id="3cc9d-141">Supportato in Windows 8.1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-141">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="3cc9d-142">WAVE_FORMAT_AMR_WP</span><span class="sxs-lookup"><span data-stu-id="3cc9d-142">WAVE_FORMAT_AMR_WP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc9d-143"><strong>MFAudioFormat_Dolby_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-143"><strong>MFAudioFormat_Dolby_AC3</strong></span></span></td>
<td><span data-ttu-id="3cc9d-144">Dolby Digital (AC-3).</span><span class="sxs-lookup"><span data-stu-id="3cc9d-144">Dolby Digital (AC-3).</span></span><br/> <span data-ttu-id="3cc9d-145">Stesso valore GUID di <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, definito in ksuuids. h</span><span class="sxs-lookup"><span data-stu-id="3cc9d-145">Same GUID value as <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, which is defined in ksuuids.h</span></span><br/></td>
<td><span data-ttu-id="3cc9d-146">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-146">None.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc9d-147"><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-147"><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></span></span></td>
<td><span data-ttu-id="3cc9d-148">Audio Dolby AC-3 sull'interfaccia digitale Sony/Philips (S/PDIF).</span><span class="sxs-lookup"><span data-stu-id="3cc9d-148">Dolby AC-3 audio over Sony/Philips Digital Interface (S/PDIF).</span></span><br/> <span data-ttu-id="3cc9d-149">Questo valore GUID è identico ai sottotipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="3cc9d-149">This GUID value is identical to the following subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="3cc9d-150"><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, definito in ksmedia. h.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-150"><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, defined in ksmedia.h.</span></span></li>
<li><span data-ttu-id="3cc9d-151"><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, definito in UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-151"><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, defined in uuids.h.</span></span></li>
</ul></td>
<td><span data-ttu-id="3cc9d-152">WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-152">WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc9d-153"><strong>MFAudioFormat_Dolby_DDPlus</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-153"><strong>MFAudioFormat_Dolby_DDPlus</strong></span></span></td>
<td><span data-ttu-id="3cc9d-154">Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-154">Dolby Digital Plus.</span></span><br/> <span data-ttu-id="3cc9d-155">Stesso valore GUID di <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, definito in wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-155">Same GUID value as <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, which is defined in wmcodecdsp.h.</span></span><br/></td>
<td><span data-ttu-id="3cc9d-156">nessuno</span><span class="sxs-lookup"><span data-stu-id="3cc9d-156">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc9d-157"><strong>MFAudioFormat_DRM</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-157"><strong>MFAudioFormat_DRM</strong></span></span></td>
<td><span data-ttu-id="3cc9d-158">Dati audio crittografati usati con il percorso audio protetto.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-158">Encrypted audio data used with secure audio path.</span></span></td>
<td><span data-ttu-id="3cc9d-159">WAVE_FORMAT_DRM (ad esempio 0x0009)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-159">WAVE_FORMAT_DRM (0x0009)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc9d-160"><strong>MFAudioFormat_DTS</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-160"><strong>MFAudioFormat_DTS</strong></span></span></td>
<td><span data-ttu-id="3cc9d-161">Audio di Digital Theater Systems (DTS).</span><span class="sxs-lookup"><span data-stu-id="3cc9d-161">Digital Theater Systems (DTS) audio.</span></span></td>
<td><span data-ttu-id="3cc9d-162">WAVE_FORMAT_DTS (0x0008)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-162">WAVE_FORMAT_DTS (0x0008)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc9d-163"><strong>MFAudioFormat_FLAC</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-163"><strong>MFAudioFormat_FLAC</strong></span></span></td>
<td><span data-ttu-id="3cc9d-164">Codec audio lossless gratuito</span><span class="sxs-lookup"><span data-stu-id="3cc9d-164">Free Lossless Audio Codec</span></span><br/> <span data-ttu-id="3cc9d-165">Supportato in Windows 10 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-165">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="3cc9d-166">WAVE_FORMAT_FLAC (0xF1AC)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-166">WAVE_FORMAT_FLAC (0xF1AC)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc9d-167"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-167"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="3cc9d-168">Audio a virgola mobile IEEE non compresso.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-168">Uncompressed IEEE floating-point audio.</span></span></td>
<td><span data-ttu-id="3cc9d-169">WAVE_FORMAT_IEEE_FLOAT (0x0003)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-169">WAVE_FORMAT_IEEE_FLOAT (0x0003)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc9d-170"><strong>MFAudioFormat_Float_SpatialObjects</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-170"><strong>MFAudioFormat_Float_SpatialObjects</strong></span></span></td>
<td><span data-ttu-id="3cc9d-171">Audio a virgola mobile IEEE non compresso.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-171">Uncompressed IEEE floating-point audio.</span></span></td>
<td><span data-ttu-id="3cc9d-172">nessuno</span><span class="sxs-lookup"><span data-stu-id="3cc9d-172">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc9d-173"><strong>MFAudioFormat_MP3</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-173"><strong>MFAudioFormat_MP3</strong></span></span></td>
<td><span data-ttu-id="3cc9d-174">MPEG Audio Layer-3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="3cc9d-174">MPEG Audio Layer-3 (MP3).</span></span></td>
<td><span data-ttu-id="3cc9d-175">WAVE_FORMAT_MPEGLAYER3 (0x0055)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-175">WAVE_FORMAT_MPEGLAYER3 (0x0055)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc9d-176"><strong>MFAudioFormat_MPEG</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-176"><strong>MFAudioFormat_MPEG</strong></span></span></td>
<td><span data-ttu-id="3cc9d-177">Payload audio MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-177">MPEG-1 audio payload.</span></span></td>
<td><span data-ttu-id="3cc9d-178">WAVE_FORMAT_MPEG (0x0050)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-178">WAVE_FORMAT_MPEG (0x0050)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc9d-179"><strong>MFAudioFormat_MSP1</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-179"><strong>MFAudioFormat_MSP1</strong></span></span></td>
<td><span data-ttu-id="3cc9d-180">Codec Windows Media Audio 9 Voice.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-180">Windows Media Audio 9 Voice codec.</span></span></td>
<td><span data-ttu-id="3cc9d-181">WAVE_FORMAT_WMAVOICE9 (0x000A)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-181">WAVE_FORMAT_WMAVOICE9 (0x000A)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc9d-182"><strong>MFAudioFormat_Opus</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-182"><strong>MFAudioFormat_Opus</strong></span></span></td>
<td><span data-ttu-id="3cc9d-183">Opus</span><span class="sxs-lookup"><span data-stu-id="3cc9d-183">Opus</span></span><br/> <span data-ttu-id="3cc9d-184">Supportato in Windows 10 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-184">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="3cc9d-185">WAVE_FORMAT_OPUS (0x704F)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-185">WAVE_FORMAT_OPUS (0x704F)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc9d-186"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-186"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="3cc9d-187">Audio PCM non compresso.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-187">Uncompressed PCM audio.</span></span></td>
<td><span data-ttu-id="3cc9d-188">WAVE_FORMAT_PCM (1)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-188">WAVE_FORMAT_PCM (1)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc9d-189"><strong>MFAudioFormat_QCELP</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-189"><strong>MFAudioFormat_QCELP</strong></span></span></td>
<td><span data-ttu-id="3cc9d-190">Audio di QCELP (codice Qualcomm Excited Linear Prediction).</span><span class="sxs-lookup"><span data-stu-id="3cc9d-190">QCELP (Qualcomm Code Excited Linear Prediction) audio.</span></span></td>
<td><span data-ttu-id="3cc9d-191">nessuno</span><span class="sxs-lookup"><span data-stu-id="3cc9d-191">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc9d-192"><strong>MFAudioFormat_WMASPDIF</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-192"><strong>MFAudioFormat_WMASPDIF</strong></span></span></td>
<td><span data-ttu-id="3cc9d-193">Codec Windows Media Audio 9 Professional su S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-193">Windows Media Audio 9 Professional codec over S/PDIF.</span></span></td>
<td><span data-ttu-id="3cc9d-194">WAVE_FORMAT_WMASPDIF (0x0164)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-194">WAVE_FORMAT_WMASPDIF (0x0164)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc9d-195"><strong>MFAudioFormat_WMAudio_Lossless</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-195"><strong>MFAudioFormat_WMAudio_Lossless</strong></span></span></td>
<td><span data-ttu-id="3cc9d-196">Codec Windows Media Audio 9 Lossless o Windows Media Audio Codec 9,1.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-196">Windows Media Audio 9 Lossless codec or Windows Media Audio 9.1 codec.</span></span></td>
<td><span data-ttu-id="3cc9d-197">WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-197">WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc9d-198"><strong>MFAudioFormat_WMAudioV8</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-198"><strong>MFAudioFormat_WMAudioV8</strong></span></span></td>
<td><span data-ttu-id="3cc9d-199">Windows Media Audio 8 codec, il codec Windows Media Audio 9 o il codec Windows Media Audio 9,1.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-199">Windows Media Audio 8 codec, Windows Media Audio 9 codec, or Windows Media Audio 9.1 codec.</span></span></td>
<td><span data-ttu-id="3cc9d-200">WAVE_FORMAT_WMAUDIO2 (0x0161)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-200">WAVE_FORMAT_WMAUDIO2 (0x0161)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc9d-201"><strong>MFAudioFormat_WMAudioV9</strong></span><span class="sxs-lookup"><span data-stu-id="3cc9d-201"><strong>MFAudioFormat_WMAudioV9</strong></span></span></td>
<td><span data-ttu-id="3cc9d-202">Codec Windows Media Audio 9 Professional o Windows Media Audio Codec Professional 9,1.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-202">Windows Media Audio 9 Professional codec or Windows Media Audio 9.1 Professional codec.</span></span></td>
<td><span data-ttu-id="3cc9d-203">WAVE_FORMAT_WMAUDIO3 (0x0162)</span><span class="sxs-lookup"><span data-stu-id="3cc9d-203">WAVE_FORMAT_WMAUDIO3 (0x0162)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3cc9d-204">I tag di formato elencati nella terza colonna di questa tabella vengono utilizzati nella struttura **WAVEFORMATEX** e vengono definiti nel file di intestazione mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-204">The format tags listed in the third column of this table are used in the **WAVEFORMATEX** structure, and are defined in the header file mmreg.h.</span></span>

<span data-ttu-id="3cc9d-205">Dato un tag di formato audio, è possibile creare un GUID del sottotipo audio come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="3cc9d-205">Given an audio format tag, you can create an audio subtype GUID as follows:</span></span>

1.  <span data-ttu-id="3cc9d-206">Iniziare con il valore **MFAudioFormat \_ base**, definito in mfaph. i.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-206">Start with the value **MFAudioFormat\_Base**, which is defined in mfaph.i.</span></span>
2.  <span data-ttu-id="3cc9d-207">Sostituire il primo **valore DWORD** del GUID con il tag di formato.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-207">Replace the first **DWORD** of this GUID with the format tag.</span></span>

<span data-ttu-id="3cc9d-208">È possibile usare la [**macro \_ MEDIATYPE \_ GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) per definire una nuova costante GUID che segue questo modello.</span><span class="sxs-lookup"><span data-stu-id="3cc9d-208">You can use the [**DEFINE\_MEDIATYPE\_GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) macro to define a new GUID constant that follows this pattern.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cc9d-209">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3cc9d-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cc9d-210">Tipi di supporti audio</span><span class="sxs-lookup"><span data-stu-id="3cc9d-210">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="3cc9d-211">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="3cc9d-211">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="3cc9d-212">GUID di tipo multimediale</span><span class="sxs-lookup"><span data-stu-id="3cc9d-212">Media Type GUIDs</span></span>](media-type-guids.md)
</dt> <dt>

[<span data-ttu-id="3cc9d-213">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="3cc9d-213">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




