---
description: Questa sezione elenca i tipi di supporto usati per i dati MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Tipi di supporto MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d1ff7c121c52db39d574f9bbae3650b04312e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320568"
---
# <a name="mpeg-1-media-types"></a><span data-ttu-id="6dccb-103">Tipi di supporto MPEG-1</span><span class="sxs-lookup"><span data-stu-id="6dccb-103">MPEG-1 Media Types</span></span>

<span data-ttu-id="6dccb-104">Questa sezione elenca i tipi di supporto usati per i dati MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="6dccb-104">This section lists the media types used for MPEG-1 data.</span></span>

## <a name="mpeg-1-system-stream"></a><span data-ttu-id="6dccb-105">Flusso di sistema MPEG-1</span><span class="sxs-lookup"><span data-stu-id="6dccb-105">MPEG-1 System Stream</span></span>



|                       |                                                 |
|-----------------------|-------------------------------------------------|
| <span data-ttu-id="6dccb-106">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="6dccb-106">Major type</span></span>            | <span data-ttu-id="6dccb-107">\_Flusso MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="6dccb-107">MEDIATYPE\_Stream</span></span>                               |
| <span data-ttu-id="6dccb-108">Subtype</span><span class="sxs-lookup"><span data-stu-id="6dccb-108">Subtype</span></span>               | <span data-ttu-id="6dccb-109">\_MPEG1SYSTEM MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6dccb-109">MEDIASUBTYPE\_MPEG1System</span></span>                       |
| <span data-ttu-id="6dccb-110">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="6dccb-110">Format Type</span></span>           | <span data-ttu-id="6dccb-111">FORMATO \_ MPEGStreams</span><span class="sxs-lookup"><span data-stu-id="6dccb-111">FORMAT\_MPEGStreams</span></span>                             |
| <span data-ttu-id="6dccb-112">Struttura Format</span><span class="sxs-lookup"><span data-stu-id="6dccb-112">Format Structure</span></span>      | [<span data-ttu-id="6dccb-113">**AM \_ MPEGSYSTEMTYPE**</span><span class="sxs-lookup"><span data-stu-id="6dccb-113">**AM\_MPEGSYSTEMTYPE**</span></span>](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| <span data-ttu-id="6dccb-114">Contenuto di esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="6dccb-114">Media Sample Contents</span></span> | <span data-ttu-id="6dccb-115">Flusso di byte; Nessun allineamento</span><span class="sxs-lookup"><span data-stu-id="6dccb-115">Byte stream; no alignment</span></span>                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a><span data-ttu-id="6dccb-116">Flusso di sistema MPEG-1 dal CD video</span><span class="sxs-lookup"><span data-stu-id="6dccb-116">MPEG-1 System Stream from Video CD</span></span>



|                       |                            |
|-----------------------|----------------------------|
| <span data-ttu-id="6dccb-117">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="6dccb-117">Major type</span></span>            | <span data-ttu-id="6dccb-118">\_Flusso MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="6dccb-118">MEDIATYPE\_Stream</span></span>          |
| <span data-ttu-id="6dccb-119">Subtype</span><span class="sxs-lookup"><span data-stu-id="6dccb-119">Subtype</span></span>               | <span data-ttu-id="6dccb-120">\_MPEG1VIDEOCD MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6dccb-120">MEDIASUBTYPE\_MPEG1VideoCD</span></span> |
| <span data-ttu-id="6dccb-121">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="6dccb-121">Format Type</span></span>           | <span data-ttu-id="6dccb-122">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="6dccb-122">GUID\_NULL</span></span>                 |
| <span data-ttu-id="6dccb-123">Struttura Format</span><span class="sxs-lookup"><span data-stu-id="6dccb-123">Format Structure</span></span>      | <span data-ttu-id="6dccb-124">nessuno</span><span class="sxs-lookup"><span data-stu-id="6dccb-124">None</span></span>                       |
| <span data-ttu-id="6dccb-125">Contenuto di esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="6dccb-125">Media Sample Contents</span></span> | <span data-ttu-id="6dccb-126">Flusso di byte; Nessun allineamento.</span><span class="sxs-lookup"><span data-stu-id="6dccb-126">Byte stream; no alignment.</span></span> |



 

## <a name="mpeg-1-audio-packet"></a><span data-ttu-id="6dccb-127">Pacchetto audio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="6dccb-127">MPEG-1 Audio Packet</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="6dccb-128">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="6dccb-128">Major type</span></span>            | <span data-ttu-id="6dccb-129">\_Audio MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="6dccb-129">MEDIATYPE\_Audio</span></span>                               |
| <span data-ttu-id="6dccb-130">Subtype</span><span class="sxs-lookup"><span data-stu-id="6dccb-130">Subtype</span></span>               | <span data-ttu-id="6dccb-131">\_MPEG1PACKET MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6dccb-131">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="6dccb-132">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="6dccb-132">Format Type</span></span>           | <span data-ttu-id="6dccb-133">FORMATO \_ WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="6dccb-133">FORMAT\_WaveFormatEx</span></span>                           |
| <span data-ttu-id="6dccb-134">Struttura Format</span><span class="sxs-lookup"><span data-stu-id="6dccb-134">Format Structure</span></span>      | [<span data-ttu-id="6dccb-135">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="6dccb-135">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| <span data-ttu-id="6dccb-136">Contenuto di esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="6dccb-136">Media Sample Contents</span></span> | <span data-ttu-id="6dccb-137">Singolo pacchetto MPEG-1, inclusa l'intestazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6dccb-137">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-audio-payload"></a><span data-ttu-id="6dccb-138">Payload audio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="6dccb-138">MPEG-1 Audio Payload</span></span>



|                       |                                            |
|-----------------------|--------------------------------------------|
| <span data-ttu-id="6dccb-139">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="6dccb-139">Major type</span></span>            | <span data-ttu-id="6dccb-140">\_Audio MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="6dccb-140">MEDIATYPE\_Audio</span></span>                           |
| <span data-ttu-id="6dccb-141">Subtype</span><span class="sxs-lookup"><span data-stu-id="6dccb-141">Subtype</span></span>               | <span data-ttu-id="6dccb-142">\_MPEG1PAYLOAD MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6dccb-142">MEDIASUBTYPE\_MPEG1Payload</span></span>                 |
| <span data-ttu-id="6dccb-143">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="6dccb-143">Format Type</span></span>           | <span data-ttu-id="6dccb-144">FORMATO \_ WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="6dccb-144">FORMAT\_WaveFormatEx</span></span>                       |
| <span data-ttu-id="6dccb-145">Struttura Format</span><span class="sxs-lookup"><span data-stu-id="6dccb-145">Format Structure</span></span>      | [<span data-ttu-id="6dccb-146">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="6dccb-146">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| <span data-ttu-id="6dccb-147">Contenuto di esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="6dccb-147">Media Sample Contents</span></span> | <span data-ttu-id="6dccb-148">Dati audio MPEG-1 allineati a byte.</span><span class="sxs-lookup"><span data-stu-id="6dccb-148">Byte-aligned MPEG-1 audio data.</span></span>            |



 

## <a name="mpeg-1-video-packet"></a><span data-ttu-id="6dccb-149">Pacchetto video MPEG-1</span><span class="sxs-lookup"><span data-stu-id="6dccb-149">MPEG-1 Video Packet</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="6dccb-150">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="6dccb-150">Major type</span></span>            | <span data-ttu-id="6dccb-151">Video di MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="6dccb-151">MEDIATYPE\_Video</span></span>                               |
| <span data-ttu-id="6dccb-152">Subtype</span><span class="sxs-lookup"><span data-stu-id="6dccb-152">Subtype</span></span>               | <span data-ttu-id="6dccb-153">\_MPEG1PACKET MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6dccb-153">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="6dccb-154">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="6dccb-154">Format Type</span></span>           | <span data-ttu-id="6dccb-155">FORMATO \_ mpegvideo</span><span class="sxs-lookup"><span data-stu-id="6dccb-155">FORMAT\_MPEGVideo</span></span>                              |
| <span data-ttu-id="6dccb-156">Struttura Format</span><span class="sxs-lookup"><span data-stu-id="6dccb-156">Format Structure</span></span>      | [<span data-ttu-id="6dccb-157">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="6dccb-157">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| <span data-ttu-id="6dccb-158">Contenuto di esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="6dccb-158">Media Sample Contents</span></span> | <span data-ttu-id="6dccb-159">Singolo pacchetto MPEG-1, inclusa l'intestazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6dccb-159">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-video-payload"></a><span data-ttu-id="6dccb-160">Payload video MPEG-1</span><span class="sxs-lookup"><span data-stu-id="6dccb-160">MPEG-1 Video payload</span></span>



|                       |                                          |
|-----------------------|------------------------------------------|
| <span data-ttu-id="6dccb-161">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="6dccb-161">Major type</span></span>            | <span data-ttu-id="6dccb-162">Video di MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="6dccb-162">MEDIATYPE\_Video</span></span>                         |
| <span data-ttu-id="6dccb-163">Subtype</span><span class="sxs-lookup"><span data-stu-id="6dccb-163">Subtype</span></span>               | <span data-ttu-id="6dccb-164">\_MPEG1PAYLOAD MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6dccb-164">MEDIASUBTYPE\_MPEG1Payload</span></span>               |
| <span data-ttu-id="6dccb-165">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="6dccb-165">Format Type</span></span>           | <span data-ttu-id="6dccb-166">FORMATO \_ mpegvideo</span><span class="sxs-lookup"><span data-stu-id="6dccb-166">FORMAT\_MPEGVideo</span></span>                        |
| <span data-ttu-id="6dccb-167">Struttura Format</span><span class="sxs-lookup"><span data-stu-id="6dccb-167">Format Structure</span></span>      | [<span data-ttu-id="6dccb-168">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="6dccb-168">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| <span data-ttu-id="6dccb-169">Contenuto di esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="6dccb-169">Media Sample Contents</span></span> | <span data-ttu-id="6dccb-170">Dati video MPEG-1 allineati a byte.</span><span class="sxs-lookup"><span data-stu-id="6dccb-170">Byte-aligned MPEG-1 video data.</span></span>          |



 

## <a name="mpeg-1-native-video-stream"></a><span data-ttu-id="6dccb-171">Flusso video nativo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="6dccb-171">MPEG-1 Native Video Stream</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="6dccb-172">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="6dccb-172">Major type</span></span>            | <span data-ttu-id="6dccb-173">\_Flusso MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="6dccb-173">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="6dccb-174">Subtype</span><span class="sxs-lookup"><span data-stu-id="6dccb-174">Subtype</span></span>               | <span data-ttu-id="6dccb-175">\_MPEG1VIDEO MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6dccb-175">MEDIASUBTYPE\_ MPEG1Video</span></span>                      |
| <span data-ttu-id="6dccb-176">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="6dccb-176">Format Type</span></span>           | <span data-ttu-id="6dccb-177">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="6dccb-177">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="6dccb-178">Struttura Format</span><span class="sxs-lookup"><span data-stu-id="6dccb-178">Format Structure</span></span>      | <span data-ttu-id="6dccb-179">nessuno</span><span class="sxs-lookup"><span data-stu-id="6dccb-179">None</span></span>                                           |
| <span data-ttu-id="6dccb-180">Contenuto di esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="6dccb-180">Media Sample Contents</span></span> | <span data-ttu-id="6dccb-181">Matrice di byte del flusso video (nessun livello di sistema).</span><span class="sxs-lookup"><span data-stu-id="6dccb-181">Array of video stream bytes (no system layer).</span></span> |



 

## <a name="mpeg-1-native-audio-stream"></a><span data-ttu-id="6dccb-182">Flusso audio MPEG-1 nativo</span><span class="sxs-lookup"><span data-stu-id="6dccb-182">MPEG-1 Native Audio Stream</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="6dccb-183">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="6dccb-183">Major type</span></span>            | <span data-ttu-id="6dccb-184">\_Flusso MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="6dccb-184">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="6dccb-185">Subtype</span><span class="sxs-lookup"><span data-stu-id="6dccb-185">Subtype</span></span>               | <span data-ttu-id="6dccb-186">\_MPEG1AUDIO MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6dccb-186">MEDIASUBTYPE\_ MPEG1Audio</span></span>                      |
| <span data-ttu-id="6dccb-187">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="6dccb-187">Format Type</span></span>           | <span data-ttu-id="6dccb-188">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="6dccb-188">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="6dccb-189">Struttura Format</span><span class="sxs-lookup"><span data-stu-id="6dccb-189">Format Structure</span></span>      | <span data-ttu-id="6dccb-190">nessuno</span><span class="sxs-lookup"><span data-stu-id="6dccb-190">None</span></span>                                           |
| <span data-ttu-id="6dccb-191">Contenuto di esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="6dccb-191">Media Sample Contents</span></span> | <span data-ttu-id="6dccb-192">Matrice di byte del flusso audio (nessun livello di sistema).</span><span class="sxs-lookup"><span data-stu-id="6dccb-192">Array of audio stream bytes (no system layer).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6dccb-193">Commenti</span><span class="sxs-lookup"><span data-stu-id="6dccb-193">Remarks</span></span>

<span data-ttu-id="6dccb-194">I filtri DirectShow MPEG-1 supportano questi tipi come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="6dccb-194">The DirectShow MPEG-1 filters support these types as follows.</span></span>



| <span data-ttu-id="6dccb-195">Filtra</span><span class="sxs-lookup"><span data-stu-id="6dccb-195">Filter</span></span>               | <span data-ttu-id="6dccb-196">Direzione</span><span class="sxs-lookup"><span data-stu-id="6dccb-196">Direction</span></span> | <span data-ttu-id="6dccb-197">Tipi di supporto supportati</span><span class="sxs-lookup"><span data-stu-id="6dccb-197">Supported media types</span></span>                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dccb-198">Barra di divisione MPEG-1</span><span class="sxs-lookup"><span data-stu-id="6dccb-198">MPEG-1 Splitter</span></span>      | <span data-ttu-id="6dccb-199">Input</span><span class="sxs-lookup"><span data-stu-id="6dccb-199">Input</span></span>     | <span data-ttu-id="6dccb-200">Flusso di sistema MPEG-1 System streamMPEG-1 dal CD video</span><span class="sxs-lookup"><span data-stu-id="6dccb-200">MPEG-1 system streamMPEG-1 system stream from Video CD</span></span><br/>                                                 |
| <span data-ttu-id="6dccb-201">Barra di divisione MPEG-1</span><span class="sxs-lookup"><span data-stu-id="6dccb-201">MPEG-1 Splitter</span></span>      | <span data-ttu-id="6dccb-202">Output</span><span class="sxs-lookup"><span data-stu-id="6dccb-202">Output</span></span>    | <span data-ttu-id="6dccb-203">Payload audio MPEG-1 audio packetMPEG-1</span><span class="sxs-lookup"><span data-stu-id="6dccb-203">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/> <span data-ttu-id="6dccb-204">Pacchetto video MPEG-1</span><span class="sxs-lookup"><span data-stu-id="6dccb-204">MPEG-1 Video packet</span></span><br/> <span data-ttu-id="6dccb-205">Payload video MPEG-1</span><span class="sxs-lookup"><span data-stu-id="6dccb-205">MPEG-1 Video payload</span></span><br/> |
| <span data-ttu-id="6dccb-206">Codec audio software</span><span class="sxs-lookup"><span data-stu-id="6dccb-206">Software Audio Codec</span></span> | <span data-ttu-id="6dccb-207">Input</span><span class="sxs-lookup"><span data-stu-id="6dccb-207">Input</span></span>     | <span data-ttu-id="6dccb-208">Payload audio MPEG-1 audio packetMPEG-1</span><span class="sxs-lookup"><span data-stu-id="6dccb-208">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/>                                                                |
| <span data-ttu-id="6dccb-209">Codec video software</span><span class="sxs-lookup"><span data-stu-id="6dccb-209">Software Video Codec</span></span> | <span data-ttu-id="6dccb-210">Input</span><span class="sxs-lookup"><span data-stu-id="6dccb-210">Input</span></span>     | <span data-ttu-id="6dccb-211">Payload video MPEG-1 packetMPEG-1</span><span class="sxs-lookup"><span data-stu-id="6dccb-211">MPEG-1 Video packetMPEG-1 Video payload</span></span><br/>                                                                |
| <span data-ttu-id="6dccb-212">Codec audio software</span><span class="sxs-lookup"><span data-stu-id="6dccb-212">Software Audio Codec</span></span> | <span data-ttu-id="6dccb-213">Output</span><span class="sxs-lookup"><span data-stu-id="6dccb-213">Output</span></span>    | <span data-ttu-id="6dccb-214">Audio PCM</span><span class="sxs-lookup"><span data-stu-id="6dccb-214">PCM audio</span></span>                                                                                                         |
| <span data-ttu-id="6dccb-215">Codec video software</span><span class="sxs-lookup"><span data-stu-id="6dccb-215">Software Video Codec</span></span> | <span data-ttu-id="6dccb-216">Output</span><span class="sxs-lookup"><span data-stu-id="6dccb-216">Output</span></span>    | <span data-ttu-id="6dccb-217">Video non compresso (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span><span class="sxs-lookup"><span data-stu-id="6dccb-217">Uncompressed video (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span></span>                                    |



 

<span data-ttu-id="6dccb-218">I tipi di supporto per pacchetti video e payload MPEG-1 contengono un'intestazione di sequenza completa, in modo che i dati possano essere riprodotti dal centro di un file senza che sia necessaria un'intestazione di sequenza per inizializzare la riproduzione video.</span><span class="sxs-lookup"><span data-stu-id="6dccb-218">MPEG-1 Video packet and payload media types contain a complete sequence header so that data can be played from the middle of a file without needing a sequence header to initialize the video playback.</span></span>

<span data-ttu-id="6dccb-219">L'intestazione della sequenza video viene aggiunta al tipo di dati video per MPEG video in modo che la riproduzione possa iniziare dal centro di un flusso.</span><span class="sxs-lookup"><span data-stu-id="6dccb-219">The video sequence header is appended to the video data type for MPEG video so that play can begin from the middle of a stream.</span></span> <span data-ttu-id="6dccb-220">La lunghezza di questo campo è fino a 140 byte. include il codice di avvio dell'intestazione della sequenza (0x000001B3) all'inizio, insieme alle matrici di quantizzazione trovate nella prima intestazione di sequenza rilevata.</span><span class="sxs-lookup"><span data-stu-id="6dccb-220">The length of this field is up to 140 bytes; it includes the sequence header start code (0x000001B3) at the start, along with any quantization matrices found in the first sequence header encountered.</span></span>

 

 




