---
description: Questa sezione descrive il supporto Media Foundation per i file MKV (Matroska Media Container).
title: Supporto di Matroska Media Container (MKV)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd860f58087bc8a0f3fe95d278bfa81edc412d0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2021
ms.locfileid: "110154216"
---
# <a name="matroska-media-container-mkv-support"></a><span data-ttu-id="04baf-103">Supporto di Matroska Media Container (MKV)</span><span class="sxs-lookup"><span data-stu-id="04baf-103">Matroska Media Container (MKV) support</span></span>

<span data-ttu-id="04baf-104">Questa sezione descrive il supporto Media Foundation per i file MKV (Matroska Media Container).</span><span class="sxs-lookup"><span data-stu-id="04baf-104">This section describes the Media Foundation support for Matroska Media Container (MKV) files.</span></span>

<span data-ttu-id="04baf-105">Il formato MKV può supportare più codec video e audio, ad esempio audio H.264 e AAC.</span><span class="sxs-lookup"><span data-stu-id="04baf-105">The MKV format can support multiple video and audio codecs, such as H.264 and AAC audio.</span></span> <span data-ttu-id="04baf-106">In generale, i contenitori descrivono come vengono disposti i dati video e audio e quali informazioni supplementari vengono usate per descrivere i flussi A/V.</span><span class="sxs-lookup"><span data-stu-id="04baf-106">In general, containers describe how video and audio data is laid out and what supplementary information is used to describe those A/V streams.</span></span> <span data-ttu-id="04baf-107">I contenitori possono anche includere dati che integrano flussi A/V, ad esempio titolo, lingue dei flussi audio, tracce sottotitoli o sottotitoli, tipi di carattere per sottotitoli, immagini, informazioni sui capitoli e menu.</span><span class="sxs-lookup"><span data-stu-id="04baf-107">Containers can also include data that complements A/V streams, such as the title, languages of the audio streams, subtitle or caption tracks, fonts for those subtitles, images, chapter information, and menus.</span></span> <span data-ttu-id="04baf-108">MKV è un formato altamente flessibile che supporta molte di queste funzionalità del contenitore.</span><span class="sxs-lookup"><span data-stu-id="04baf-108">MKV is a highly flexible format that supports many of these container features.</span></span> <span data-ttu-id="04baf-109">Per altre informazioni sul formato MKV, vedere [https://matroska.org](https://matroska.org/)</span><span class="sxs-lookup"><span data-stu-id="04baf-109">For more info about the MKV format, see [https://matroska.org](https://matroska.org/)</span></span>


## <a name="mkv-container-feature-support"></a><span data-ttu-id="04baf-110">Supporto della funzionalità contenitore MKV</span><span class="sxs-lookup"><span data-stu-id="04baf-110">MKV container feature support</span></span>
<span data-ttu-id="04baf-111">Le funzionalità del contenitore MKV sono supportate nel Media Foundation nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="04baf-111">MKV container features are supported on the by Media Foundation in the following ways:</span></span>
- <span data-ttu-id="04baf-112">Se sono presenti una o più tracce video, verrà riprodotta la prima traccia.</span><span class="sxs-lookup"><span data-stu-id="04baf-112">If one or more video tracks are present, the first track will be played.</span></span>
- <span data-ttu-id="04baf-113">Se sono presenti una o più tracce audio, verrà riprodotta la prima traccia.</span><span class="sxs-lookup"><span data-stu-id="04baf-113">If one or more audio tracks are present, the first track will be played.</span></span>
- <span data-ttu-id="04baf-114">Le tracce dei sottotitoli sono supportate, ma non sono selezionate (riprodotte) per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="04baf-114">Caption tracks are supported, but are not selected (played) by default.</span></span>
- <span data-ttu-id="04baf-115">Se sono presenti uno o più tipi di carattere o immagini, il rendering di didascalie e immagini non verrà eseguito, anche se il file verrà caricato e riprodotto.</span><span class="sxs-lookup"><span data-stu-id="04baf-115">If one or more fonts or images are present, captions and images won’t render, although the file will load and play.</span></span>
- <span data-ttu-id="04baf-116">Le informazioni sul menu non sono supportate e non verranno visualizzate, ma il file verrà caricato e riprodotto.</span><span class="sxs-lookup"><span data-stu-id="04baf-116">Menu information is not supported and won’t be displayed, but the file will load and play.</span></span>
- <span data-ttu-id="04baf-117">Se i file con capitoli fanno riferimento a file supplementari, i file supplementari non verranno riprodotti.</span><span class="sxs-lookup"><span data-stu-id="04baf-117">If files with chapters refer to supplemental files, the supplemental files won’t play.</span></span>
- <span data-ttu-id="04baf-118">Le immagini di anteprima sono disponibili quando si esplorano i file nelle unità USB usando il browser di file.</span><span class="sxs-lookup"><span data-stu-id="04baf-118">Thumbnail images are available when browsing for files on USB drives using the file browser.</span></span>

<span data-ttu-id="04baf-119">Questo set di funzionalità deve consentire la riproduzione della maggior parte dei file MKV se contengono codec supportati.</span><span class="sxs-lookup"><span data-stu-id="04baf-119">This set of features should allow playback of most MKV files if they contain supported codecs.</span></span>
<span data-ttu-id="04baf-120">Sono supportati i file MKV che contengono tracce video e audio codificate con i codec elencati nella sezione seguente.</span><span class="sxs-lookup"><span data-stu-id="04baf-120">MKV files that contain video and audio tracks encoded with the codecs listed in the following section are supported.</span></span>

## <a name="supported-mkv-codecs"></a><span data-ttu-id="04baf-121">Codec MKV supportati</span><span class="sxs-lookup"><span data-stu-id="04baf-121">Supported MKV codecs</span></span>

### <a name="video-codec-support-for-mkv"></a><span data-ttu-id="04baf-122">Supporto di codec video per MKV</span><span class="sxs-lookup"><span data-stu-id="04baf-122">Video codec support for MKV</span></span>

<span data-ttu-id="04baf-123">ID Matroska: V_MPEG4/ISO/AVC</span><span class="sxs-lookup"><span data-stu-id="04baf-123">Matroska ID: V_MPEG4/ISO/AVC</span></span>

- <span data-ttu-id="04baf-124">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_H264</span><span class="sxs-lookup"><span data-stu-id="04baf-124">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_H264</span></span>
- <span data-ttu-id="04baf-125">Descrizione: video H.264</span><span class="sxs-lookup"><span data-stu-id="04baf-125">Description: H.264 video</span></span>
- <span data-ttu-id="04baf-126">Identificatori FourCC o WAV: H264</span><span class="sxs-lookup"><span data-stu-id="04baf-126">FourCC or WAV identifiers: H264</span></span>

<span data-ttu-id="04baf-127">ID Matroska: V_MPEG2</span><span class="sxs-lookup"><span data-stu-id="04baf-127">Matroska ID: V_MPEG2</span></span>

- <span data-ttu-id="04baf-128">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPEG2</span><span class="sxs-lookup"><span data-stu-id="04baf-128">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPEG2</span></span>
- <span data-ttu-id="04baf-129">Descrizione: video MPEG-2</span><span class="sxs-lookup"><span data-stu-id="04baf-129">Description: MPEG-2 video</span></span>

<span data-ttu-id="04baf-130">ID Matroska: V_MPEG1</span><span class="sxs-lookup"><span data-stu-id="04baf-130">Matroska ID: V_MPEG1</span></span>

- <span data-ttu-id="04baf-131">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPG1</span><span class="sxs-lookup"><span data-stu-id="04baf-131">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPG1</span></span>
- <span data-ttu-id="04baf-132">Descrizione: video MPEG-1</span><span class="sxs-lookup"><span data-stu-id="04baf-132">Description: MPEG-1 video</span></span>
- <span data-ttu-id="04baf-133">Identificatori FourCC o WAV: MPG1</span><span class="sxs-lookup"><span data-stu-id="04baf-133">FourCC or WAV identifiers: MPG1</span></span>

<span data-ttu-id="04baf-134">ID Matroska: V_MPEG4/MS/V3</span><span class="sxs-lookup"><span data-stu-id="04baf-134">Matroska ID: V_MPEG4/MS/V3</span></span>

- <span data-ttu-id="04baf-135">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP43</span><span class="sxs-lookup"><span data-stu-id="04baf-135">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP43</span></span>
- <span data-ttu-id="04baf-136">Descrizione: codec Microsoft MPEG 4 versione 3</span><span class="sxs-lookup"><span data-stu-id="04baf-136">Description: Microsoft MPEG 4 codec version 3</span></span>
- <span data-ttu-id="04baf-137">Identificatori FourCC o WAV: MP43</span><span class="sxs-lookup"><span data-stu-id="04baf-137">FourCC or WAV identifiers: MP43</span></span>

<span data-ttu-id="04baf-138">ID Matroska: V_MPEG4/ISO/ASP</span><span class="sxs-lookup"><span data-stu-id="04baf-138">Matroska ID: V_MPEG4/ISO/ASP</span></span>

- <span data-ttu-id="04baf-139">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="04baf-139">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="04baf-140">Descrizione: video MPEG-4 parte 2</span><span class="sxs-lookup"><span data-stu-id="04baf-140">Description: MPEG-4 part 2 video</span></span>
- <span data-ttu-id="04baf-141">Identificatori FourCC o WAV: MP4V</span><span class="sxs-lookup"><span data-stu-id="04baf-141">FourCC or WAV identifiers: MP4V</span></span>

<span data-ttu-id="04baf-142">ID Matroska: V_MS/VFW/FOURCC</span><span class="sxs-lookup"><span data-stu-id="04baf-142">Matroska ID: V_MS/VFW/FOURCC</span></span>

- <span data-ttu-id="04baf-143">Descrizione: esegue il mapping a diversi codec in genere supportati nel formato AVI disponibili nella console.</span><span class="sxs-lookup"><span data-stu-id="04baf-143">Description: Maps to several codecs usually supported in the AVI format that are available on the console.</span></span>

<span data-ttu-id="04baf-144">ID Matroska: V_THEORA</span><span class="sxs-lookup"><span data-stu-id="04baf-144">Matroska ID: V_THEORA</span></span>

- <span data-ttu-id="04baf-145">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora</span><span class="sxs-lookup"><span data-stu-id="04baf-145">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora</span></span>
- <span data-ttu-id="04baf-146">Descrizione: Theora</span><span class="sxs-lookup"><span data-stu-id="04baf-146">Description: Theora</span></span>
- <span data-ttu-id="04baf-147">Identificatori FourCC o WAV: theo</span><span class="sxs-lookup"><span data-stu-id="04baf-147">FourCC or WAV identifiers: theo</span></span>

<span data-ttu-id="04baf-148">ID Matroska: V_MPEG4/ISO/SP</span><span class="sxs-lookup"><span data-stu-id="04baf-148">Matroska ID: V_MPEG4/ISO/SP</span></span>

- <span data-ttu-id="04baf-149">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="04baf-149">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="04baf-150">Descrizione: profilo semplice ISO MPEG4 (DivX4)</span><span class="sxs-lookup"><span data-stu-id="04baf-150">Description: MPEG4 ISO simple profile (DivX4)</span></span>
- <span data-ttu-id="04baf-151">Identificatori FourCC o WAV: MP4V</span><span class="sxs-lookup"><span data-stu-id="04baf-151">FourCC or WAV identifiers: MP4V</span></span>

<span data-ttu-id="04baf-152">ID Matroska: V_MPEG4/ISO/AP</span><span class="sxs-lookup"><span data-stu-id="04baf-152">Matroska ID: V_MPEG4/ISO/AP</span></span>

- <span data-ttu-id="04baf-153">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="04baf-153">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="04baf-154">Descrizione: profilo semplice avanzato MPEG4 ISO (DivX5, XviD, FFMPEG)</span><span class="sxs-lookup"><span data-stu-id="04baf-154">Description: MPEG4 ISO advanced simple profile (DivX5, XviD, FFMPEG)</span></span>
- <span data-ttu-id="04baf-155">Identificatori FourCC o WAV: MP4V</span><span class="sxs-lookup"><span data-stu-id="04baf-155">FourCC or WAV identifiers: MP4V</span></span>


<span data-ttu-id="04baf-156">ID Matroska: V_MPEGH/ISO/HEVC</span><span class="sxs-lookup"><span data-stu-id="04baf-156">Matroska ID: V_MPEGH/ISO/HEVC</span></span> 

- <span data-ttu-id="04baf-157">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC</span><span class="sxs-lookup"><span data-stu-id="04baf-157">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC</span></span>
- <span data-ttu-id="04baf-158">Descrizione: HEVC/H.265</span><span class="sxs-lookup"><span data-stu-id="04baf-158">Description: HEVC/H.265</span></span>
- <span data-ttu-id="04baf-159">Identificatori FourCC o WAV:</span><span class="sxs-lookup"><span data-stu-id="04baf-159">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="04baf-160">ID Matroska: V_VP8</span><span class="sxs-lookup"><span data-stu-id="04baf-160">Matroska ID: V_VP8</span></span>

- <span data-ttu-id="04baf-161">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP80</span><span class="sxs-lookup"><span data-stu-id="04baf-161">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP80</span></span>
- <span data-ttu-id="04baf-162">Descrizione: Formato codec VP8</span><span class="sxs-lookup"><span data-stu-id="04baf-162">Description: VP8 Codec format</span></span>
- <span data-ttu-id="04baf-163">Identificatori FourCC o WAV: VP80</span><span class="sxs-lookup"><span data-stu-id="04baf-163">FourCC or WAV identifiers: VP80</span></span>

<span data-ttu-id="04baf-164">ID Matroska: V_VP9</span><span class="sxs-lookup"><span data-stu-id="04baf-164">Matroska ID: V_VP9</span></span>

- <span data-ttu-id="04baf-165">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP90</span><span class="sxs-lookup"><span data-stu-id="04baf-165">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP90</span></span>
- <span data-ttu-id="04baf-166">Descrizione: Formato codec VP9</span><span class="sxs-lookup"><span data-stu-id="04baf-166">Description: VP9 Codec format</span></span>
- <span data-ttu-id="04baf-167">Identificatori FourCC o WAV: VP90</span><span class="sxs-lookup"><span data-stu-id="04baf-167">FourCC or WAV identifiers: VP90</span></span>

<span data-ttu-id="04baf-168">ID Matroska: V_MJPEG</span><span class="sxs-lookup"><span data-stu-id="04baf-168">Matroska ID: V_MJPEG</span></span>

- <span data-ttu-id="04baf-169">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MJPG</span><span class="sxs-lookup"><span data-stu-id="04baf-169">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MJPG</span></span>
- <span data-ttu-id="04baf-170">Descrizione: Motion JPEG</span><span class="sxs-lookup"><span data-stu-id="04baf-170">Description: Motion JPEG</span></span>
- <span data-ttu-id="04baf-171">Identificatori FourCC o WAV: MJPG</span><span class="sxs-lookup"><span data-stu-id="04baf-171">FourCC or WAV identifiers: MJPG</span></span>

<span data-ttu-id="04baf-172">ID Matroska: V_AV1</span><span class="sxs-lookup"><span data-stu-id="04baf-172">Matroska ID: V_AV1</span></span>

- <span data-ttu-id="04baf-173">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_AV1</span><span class="sxs-lookup"><span data-stu-id="04baf-173">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_AV1</span></span>
- <span data-ttu-id="04baf-174">Descrizione: AOMedia Video 1</span><span class="sxs-lookup"><span data-stu-id="04baf-174">Description: AOMedia Video 1</span></span>
- <span data-ttu-id="04baf-175">Identificatori FourCC o WAV: AV01</span><span class="sxs-lookup"><span data-stu-id="04baf-175">FourCC or WAV identifiers: AV01</span></span>

### <a name="audio-codec-support-for-mkv"></a><span data-ttu-id="04baf-176">Supporto di codec audio per MKV</span><span class="sxs-lookup"><span data-stu-id="04baf-176">Audio codec support for MKV</span></span>

<span data-ttu-id="04baf-177">ID Matroska: A_AAC</span><span class="sxs-lookup"><span data-stu-id="04baf-177">Matroska ID: A_AAC</span></span>

- <span data-ttu-id="04baf-178">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span><span class="sxs-lookup"><span data-stu-id="04baf-178">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span></span>
- <span data-ttu-id="04baf-179">Descrizione: AAC (Advanced Audio Coding)</span><span class="sxs-lookup"><span data-stu-id="04baf-179">Description: Advanced Audio Coding (AAC)</span></span>
- <span data-ttu-id="04baf-180">Identificatori FourCC o WAV: WAVE_FORMAT_MPEG_HEAAC</span><span class="sxs-lookup"><span data-stu-id="04baf-180">FourCC or WAV identifiers: WAVE_FORMAT_MPEG_HEAAC</span></span>

<span data-ttu-id="04baf-181">ID Matroska: A_AC3</span><span class="sxs-lookup"><span data-stu-id="04baf-181">Matroska ID: A_AC3</span></span>

- <span data-ttu-id="04baf-182">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3</span><span class="sxs-lookup"><span data-stu-id="04baf-182">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3</span></span>
- <span data-ttu-id="04baf-183">Descrizione: Dolby AC3</span><span class="sxs-lookup"><span data-stu-id="04baf-183">Description: Dolby AC3</span></span>
- <span data-ttu-id="04baf-184">Identificatori FourCC o WAV: WAVE_FORMAT_DOLBY_AC3_SPDIF</span><span class="sxs-lookup"><span data-stu-id="04baf-184">FourCC or WAV identifiers: WAVE_FORMAT_DOLBY_AC3_SPDIF</span></span>

<span data-ttu-id="04baf-185">ID Matroska: A_MPEG/L3</span><span class="sxs-lookup"><span data-stu-id="04baf-185">Matroska ID: A_MPEG/L3</span></span>

- <span data-ttu-id="04baf-186">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3</span><span class="sxs-lookup"><span data-stu-id="04baf-186">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3</span></span>
- <span data-ttu-id="04baf-187">Descrizione: MPEG Audio Layer-3 (MP3)</span><span class="sxs-lookup"><span data-stu-id="04baf-187">Description: MPEG Audio Layer-3 (MP3)</span></span>
- <span data-ttu-id="04baf-188">Identificatori FourCC o WAV: WAVE_FORMAT_MPEGLAYER3</span><span class="sxs-lookup"><span data-stu-id="04baf-188">FourCC or WAV identifiers: WAVE_FORMAT_MPEGLAYER3</span></span>

<span data-ttu-id="04baf-189">ID Matroska: A_MPEG/L1</span><span class="sxs-lookup"><span data-stu-id="04baf-189">Matroska ID: A_MPEG/L1</span></span>

- <span data-ttu-id="04baf-190">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span><span class="sxs-lookup"><span data-stu-id="04baf-190">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span></span>
- <span data-ttu-id="04baf-191">Descrizione: payload audio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="04baf-191">Description: MPEG-1 audio payload</span></span>
- <span data-ttu-id="04baf-192">Identificatori FourCC o WAV: WAVE_FORMAT_MPEG</span><span class="sxs-lookup"><span data-stu-id="04baf-192">FourCC or WAV identifiers: WAVE_FORMAT_MPEG</span></span>

<span data-ttu-id="04baf-193">ID Matroska: A_PCM/INT/BIG</span><span class="sxs-lookup"><span data-stu-id="04baf-193">Matroska ID: A_PCM/INT/BIG</span></span>

- <span data-ttu-id="04baf-194">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span><span class="sxs-lookup"><span data-stu-id="04baf-194">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span></span>
- <span data-ttu-id="04baf-195">Descrizione: Audio PCM non compresso</span><span class="sxs-lookup"><span data-stu-id="04baf-195">Description: Uncompressed PCM audio</span></span>
- <span data-ttu-id="04baf-196">Identificatori FourCC o WAV: WAVE_FORMAT_PCM</span><span class="sxs-lookup"><span data-stu-id="04baf-196">FourCC or WAV identifiers: WAVE_FORMAT_PCM</span></span>

<span data-ttu-id="04baf-197">ID Matroska: A_PCM/INT/LIT</span><span class="sxs-lookup"><span data-stu-id="04baf-197">Matroska ID: A_PCM/INT/LIT</span></span>

- <span data-ttu-id="04baf-198">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span><span class="sxs-lookup"><span data-stu-id="04baf-198">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span></span>
- <span data-ttu-id="04baf-199">Descrizione: Audio PCM non compresso</span><span class="sxs-lookup"><span data-stu-id="04baf-199">Description: Uncompressed PCM audio</span></span>
- <span data-ttu-id="04baf-200">Identificatori FourCC o WAV: WAVE_FORMAT_PCM</span><span class="sxs-lookup"><span data-stu-id="04baf-200">FourCC or WAV identifiers: WAVE_FORMAT_PCM</span></span>

<span data-ttu-id="04baf-201">ID Matroska: A_PCM/FLOAT/IEEE</span><span class="sxs-lookup"><span data-stu-id="04baf-201">Matroska ID: A_PCM/FLOAT/IEEE</span></span>

- <span data-ttu-id="04baf-202">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Float</span><span class="sxs-lookup"><span data-stu-id="04baf-202">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Float</span></span>
- <span data-ttu-id="04baf-203">Descrizione: audio a virgola mobile IEEE non compresso</span><span class="sxs-lookup"><span data-stu-id="04baf-203">Description: Uncompressed IEEE floating-point audio</span></span>
- <span data-ttu-id="04baf-204">Identificatori FourCC o WAV: WAVE_FORMAT_IEEE_FLOAT</span><span class="sxs-lookup"><span data-stu-id="04baf-204">FourCC or WAV identifiers: WAVE_FORMAT_IEEE_FLOAT</span></span>

<span data-ttu-id="04baf-205">ID Matroska: A_ALAC</span><span class="sxs-lookup"><span data-stu-id="04baf-205">Matroska ID: A_ALAC</span></span>

- <span data-ttu-id="04baf-206">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_ALAC</span><span class="sxs-lookup"><span data-stu-id="04baf-206">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_ALAC</span></span>
- <span data-ttu-id="04baf-207">Descrizione: Codec audio apple senza perdita di dati</span><span class="sxs-lookup"><span data-stu-id="04baf-207">Description: Apple Lossless Audio Codec</span></span>
- <span data-ttu-id="04baf-208">Quattro identificatori CC o WAV:</span><span class="sxs-lookup"><span data-stu-id="04baf-208">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="04baf-209">ID Matroska: A_MPEG/L2</span><span class="sxs-lookup"><span data-stu-id="04baf-209">Matroska ID: A_MPEG/L2</span></span>

- <span data-ttu-id="04baf-210">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span><span class="sxs-lookup"><span data-stu-id="04baf-210">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span></span>
- <span data-ttu-id="04baf-211">Descrizione: MPEG Audio 1, 2 Livello II</span><span class="sxs-lookup"><span data-stu-id="04baf-211">Description: MPEG Audio 1, 2 Layer II</span></span>
- <span data-ttu-id="04baf-212">Identificatori FourCC o WAV: WAVE_FORMAT_MPEG</span><span class="sxs-lookup"><span data-stu-id="04baf-212">FourCC or WAV identifiers: WAVE_FORMAT_MPEG</span></span>

<span data-ttu-id="04baf-213">ID Matroska: A_DTS</span><span class="sxs-lookup"><span data-stu-id="04baf-213">Matroska ID: A_DTS</span></span>

- <span data-ttu-id="04baf-214">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD</span><span class="sxs-lookup"><span data-stu-id="04baf-214">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD</span></span>
- <span data-ttu-id="04baf-215">Descrizione: Digital Digital Esere System</span><span class="sxs-lookup"><span data-stu-id="04baf-215">Description: Digital Theatre System</span></span>
- <span data-ttu-id="04baf-216">Identificatori FourCC o WAV: WAVE_FORMAT_DTS</span><span class="sxs-lookup"><span data-stu-id="04baf-216">FourCC or WAV identifiers: WAVE_FORMAT_DTS</span></span>

<span data-ttu-id="04baf-217">ID Matroska: A_OPUS</span><span class="sxs-lookup"><span data-stu-id="04baf-217">Matroska ID: A_OPUS</span></span>

- <span data-ttu-id="04baf-218">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Opus</span><span class="sxs-lookup"><span data-stu-id="04baf-218">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Opus</span></span>
- <span data-ttu-id="04baf-219">Descrizione: Opus</span><span class="sxs-lookup"><span data-stu-id="04baf-219">Description: Opus</span></span>
- <span data-ttu-id="04baf-220">Identificatori FourCC o WAV: WAVE_FORMAT_OPUS</span><span class="sxs-lookup"><span data-stu-id="04baf-220">FourCC or WAV identifiers: WAVE_FORMAT_OPUS</span></span>

<span data-ttu-id="04baf-221">ID Matroska: A_VORBIS</span><span class="sxs-lookup"><span data-stu-id="04baf-221">Matroska ID: A_VORBIS</span></span>

- <span data-ttu-id="04baf-222">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Vorbis</span><span class="sxs-lookup"><span data-stu-id="04baf-222">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Vorbis</span></span>
- <span data-ttu-id="04baf-223">Descrizione: Vorbis</span><span class="sxs-lookup"><span data-stu-id="04baf-223">Description: Vorbis</span></span>
- <span data-ttu-id="04baf-224">Identificatori FourCC o WAV:</span><span class="sxs-lookup"><span data-stu-id="04baf-224">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="04baf-225">ID Matroska: A_FLAC</span><span class="sxs-lookup"><span data-stu-id="04baf-225">Matroska ID: A_FLAC</span></span>

- <span data-ttu-id="04baf-226">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_FLAC</span><span class="sxs-lookup"><span data-stu-id="04baf-226">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_FLAC</span></span>
- <span data-ttu-id="04baf-227">Descrizione: Codec audio senza perdita gratuita</span><span class="sxs-lookup"><span data-stu-id="04baf-227">Description: Free Lossless Audio Codec</span></span>
- <span data-ttu-id="04baf-228">Identificatori FourCC o WAV: WAVE_FORMAT_FLAC</span><span class="sxs-lookup"><span data-stu-id="04baf-228">FourCC or WAV identifiers: WAVE_FORMAT_FLAC</span></span>

<span data-ttu-id="04baf-229">ID Matroska: A_AAC/MAIN</span><span class="sxs-lookup"><span data-stu-id="04baf-229">Matroska ID: A_AAC/MAIN</span></span>

- <span data-ttu-id="04baf-230">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span><span class="sxs-lookup"><span data-stu-id="04baf-230">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span></span>
- <span data-ttu-id="04baf-231">Descrizione: Codifica audio avanzata (AAC)</span><span class="sxs-lookup"><span data-stu-id="04baf-231">Description: Advanced Audio Coding (AAC)</span></span>
- <span data-ttu-id="04baf-232">Identificatori FourCC o WAV: WAVE_FORMAT_MPEG_HEAAC</span><span class="sxs-lookup"><span data-stu-id="04baf-232">FourCC or WAV identifiers: WAVE_FORMAT_MPEG_HEAAC</span></span>

<span data-ttu-id="04baf-233">ID Matroska: A_EAC3</span><span class="sxs-lookup"><span data-stu-id="04baf-233">Matroska ID: A_EAC3</span></span>

- <span data-ttu-id="04baf-234">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus</span><span class="sxs-lookup"><span data-stu-id="04baf-234">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus</span></span>
- <span data-ttu-id="04baf-235">Descrizione: Ac-3 avanzato</span><span class="sxs-lookup"><span data-stu-id="04baf-235">Description: Enhanced AC-3</span></span>
- <span data-ttu-id="04baf-236">Identificatori FourCC o WAV:</span><span class="sxs-lookup"><span data-stu-id="04baf-236">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="04baf-237">ID Matroska: A_TRUEHD</span><span class="sxs-lookup"><span data-stu-id="04baf-237">Matroska ID: A_TRUEHD</span></span>

- <span data-ttu-id="04baf-238">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD</span><span class="sxs-lookup"><span data-stu-id="04baf-238">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD</span></span>
- <span data-ttu-id="04baf-239">Descrizione: Dolby TrueHD</span><span class="sxs-lookup"><span data-stu-id="04baf-239">Description: Dolby TrueHD</span></span>
- <span data-ttu-id="04baf-240">Identificatori FourCC o WAV:</span><span class="sxs-lookup"><span data-stu-id="04baf-240">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="04baf-241">ID Matroska: A_MS/ACM</span><span class="sxs-lookup"><span data-stu-id="04baf-241">Matroska ID: A_MS/ACM</span></span>

- <span data-ttu-id="04baf-242">MSFT Media Foundation MF_MT_SUBTYPE: esegue il mapping a WAVE_FORMAT tipi audio definiti in mmreg.h</span><span class="sxs-lookup"><span data-stu-id="04baf-242">MSFT Media Foundation MF_MT_SUBTYPE: Maps to several WAVE_FORMAT audio types defined in mmreg.h</span></span>


### <a name="subtitles-codec-support-for-mkv"></a><span data-ttu-id="04baf-243">Supporto del codec sottotitoli per MKV</span><span class="sxs-lookup"><span data-stu-id="04baf-243">Subtitles codec support for MKV</span></span>

<span data-ttu-id="04baf-244">ID Matroska: S_TEXT/ASCII</span><span class="sxs-lookup"><span data-stu-id="04baf-244">Matroska ID: S_TEXT/ASCII</span></span>

- <span data-ttu-id="04baf-245">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span><span class="sxs-lookup"><span data-stu-id="04baf-245">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span></span>
- <span data-ttu-id="04baf-246">Descrizione: testo ASCII</span><span class="sxs-lookup"><span data-stu-id="04baf-246">Description: ASCII text</span></span>

<span data-ttu-id="04baf-247">ID Matroska: S_TEXT/UTF8</span><span class="sxs-lookup"><span data-stu-id="04baf-247">Matroska ID: S_TEXT/UTF8</span></span>

- <span data-ttu-id="04baf-248">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span><span class="sxs-lookup"><span data-stu-id="04baf-248">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span></span>
- <span data-ttu-id="04baf-249">Descrizione: testo normale UTF-8</span><span class="sxs-lookup"><span data-stu-id="04baf-249">Description: UTF-8 Plain Text</span></span>

<span data-ttu-id="04baf-250">ID Matroska: S_TEXT/SSA</span><span class="sxs-lookup"><span data-stu-id="04baf-250">Matroska ID: S_TEXT/SSA</span></span>

- <span data-ttu-id="04baf-251">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span><span class="sxs-lookup"><span data-stu-id="04baf-251">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span></span>
- <span data-ttu-id="04baf-252">Descrizione: Formato sottotitoli</span><span class="sxs-lookup"><span data-stu-id="04baf-252">Description: Subtitles Format</span></span>

<span data-ttu-id="04baf-253">ID Matroska: S_TEXT/ASS</span><span class="sxs-lookup"><span data-stu-id="04baf-253">Matroska ID: S_TEXT/ASS</span></span>

- <span data-ttu-id="04baf-254">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span><span class="sxs-lookup"><span data-stu-id="04baf-254">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span></span>
- <span data-ttu-id="04baf-255">Descrizione: Formato sottotitoli avanzato</span><span class="sxs-lookup"><span data-stu-id="04baf-255">Description: Advanced Subtitles Format</span></span>

<span data-ttu-id="04baf-256">ID Matroska: S_VOBSUB</span><span class="sxs-lookup"><span data-stu-id="04baf-256">Matroska ID: S_VOBSUB</span></span>

- <span data-ttu-id="04baf-257">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_VobSub</span><span class="sxs-lookup"><span data-stu-id="04baf-257">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_VobSub</span></span>
- <span data-ttu-id="04baf-258">Descrizione: Sottotitoli VobSub</span><span class="sxs-lookup"><span data-stu-id="04baf-258">Description: VobSub subtitles</span></span>

<span data-ttu-id="04baf-259">ID Matroska: S_HDMV/PGS</span><span class="sxs-lookup"><span data-stu-id="04baf-259">Matroska ID: S_HDMV/PGS</span></span>

- <span data-ttu-id="04baf-260">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_PGS</span><span class="sxs-lookup"><span data-stu-id="04baf-260">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_PGS</span></span>
- <span data-ttu-id="04baf-261">Descrizione: sottotitoli grafici di presentazione HDMV (PGS)</span><span class="sxs-lookup"><span data-stu-id="04baf-261">Description: HDMV presentation graphics subtitles (PGS)</span></span>


## <a name="technical-details-regarding-codecs"></a><span data-ttu-id="04baf-262">Dettagli tecnici relativi ai codec</span><span class="sxs-lookup"><span data-stu-id="04baf-262">Technical details regarding codecs</span></span>

<span data-ttu-id="04baf-263">Per informazioni tecniche sui codec, vedere quanto segue.</span><span class="sxs-lookup"><span data-stu-id="04baf-263">See the following for technical details regarding codecs.</span></span>

- [<span data-ttu-id="04baf-264">Specifiche del codec Matroska</span><span class="sxs-lookup"><span data-stu-id="04baf-264">Matroska Codec Specs</span></span>](http://www.matroska.org/technical/specs/codecid/index.html)
- [<span data-ttu-id="04baf-265">GUID del sottotipo audio</span><span class="sxs-lookup"><span data-stu-id="04baf-265">Audio Subtype GUIDs</span></span>](audio-subtype-guids.md)
- [<span data-ttu-id="04baf-266">GUID del sottotipo video</span><span class="sxs-lookup"><span data-stu-id="04baf-266">Video Subtype GUIDs</span></span>](video-subtype-guids.md)


## <a name="related-topics"></a><span data-ttu-id="04baf-267">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04baf-267">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04baf-268">Formati multimediali supportati in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="04baf-268">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="04baf-269">Media Foundation guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="04baf-269">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



