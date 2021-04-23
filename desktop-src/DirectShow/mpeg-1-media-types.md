---
description: Questa sezione elenca i tipi di supporti usati per i dati MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Tipi di supporti MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e44db1f4423365efb7814d61b35c1985142aa14
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910029"
---
# <a name="mpeg-1-media-types"></a><span data-ttu-id="ea3ee-103">Tipi di supporti MPEG-1</span><span class="sxs-lookup"><span data-stu-id="ea3ee-103">MPEG-1 Media Types</span></span>

<span data-ttu-id="ea3ee-104">Questa sezione elenca i tipi di supporti usati per i dati MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="ea3ee-104">This section lists the media types used for MPEG-1 data.</span></span>

## <a name="mpeg-1-system-stream"></a><span data-ttu-id="ea3ee-105">Flusso di sistema MPEG-1</span><span class="sxs-lookup"><span data-stu-id="ea3ee-105">MPEG-1 System Stream</span></span>



| <span data-ttu-id="ea3ee-106">Label</span><span class="sxs-lookup"><span data-stu-id="ea3ee-106">Label</span></span> | <span data-ttu-id="ea3ee-107">Valore</span><span class="sxs-lookup"><span data-stu-id="ea3ee-107">Value</span></span> |
|-----------------------|-------------------------------------------------|
| <span data-ttu-id="ea3ee-108">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-108">Major type</span></span>            | <span data-ttu-id="ea3ee-109">Flusso \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="ea3ee-109">MEDIATYPE\_Stream</span></span>                               |
| <span data-ttu-id="ea3ee-110">Subtype</span><span class="sxs-lookup"><span data-stu-id="ea3ee-110">Subtype</span></span>               | <span data-ttu-id="ea3ee-111">MEDIASUBTYPE \_ MPEG1System</span><span class="sxs-lookup"><span data-stu-id="ea3ee-111">MEDIASUBTYPE\_MPEG1System</span></span>                       |
| <span data-ttu-id="ea3ee-112">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-112">Format Type</span></span>           | <span data-ttu-id="ea3ee-113">FORMAT \_ MPEGStreams</span><span class="sxs-lookup"><span data-stu-id="ea3ee-113">FORMAT\_MPEGStreams</span></span>                             |
| <span data-ttu-id="ea3ee-114">Struttura del formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-114">Format Structure</span></span>      | [<span data-ttu-id="ea3ee-115">**AM \_ MPEGSYSTEMTYPE**</span><span class="sxs-lookup"><span data-stu-id="ea3ee-115">**AM\_MPEGSYSTEMTYPE**</span></span>](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| <span data-ttu-id="ea3ee-116">Contenuto dell'esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-116">Media Sample Contents</span></span> | <span data-ttu-id="ea3ee-117">Flusso di byte; nessun allineamento</span><span class="sxs-lookup"><span data-stu-id="ea3ee-117">Byte stream; no alignment</span></span>                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a><span data-ttu-id="ea3ee-118">Flusso di sistema MPEG-1 da Video CD</span><span class="sxs-lookup"><span data-stu-id="ea3ee-118">MPEG-1 System Stream from Video CD</span></span>



| <span data-ttu-id="ea3ee-119">Label</span><span class="sxs-lookup"><span data-stu-id="ea3ee-119">Label</span></span> | <span data-ttu-id="ea3ee-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ea3ee-120">Value</span></span> |
|-----------------------|----------------------------|
| <span data-ttu-id="ea3ee-121">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-121">Major type</span></span>            | <span data-ttu-id="ea3ee-122">Flusso \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="ea3ee-122">MEDIATYPE\_Stream</span></span>          |
| <span data-ttu-id="ea3ee-123">Subtype</span><span class="sxs-lookup"><span data-stu-id="ea3ee-123">Subtype</span></span>               | <span data-ttu-id="ea3ee-124">MEDIASUBTYPE \_ MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="ea3ee-124">MEDIASUBTYPE\_MPEG1VideoCD</span></span> |
| <span data-ttu-id="ea3ee-125">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-125">Format Type</span></span>           | <span data-ttu-id="ea3ee-126">GUID \_ NULL</span><span class="sxs-lookup"><span data-stu-id="ea3ee-126">GUID\_NULL</span></span>                 |
| <span data-ttu-id="ea3ee-127">Struttura del formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-127">Format Structure</span></span>      | <span data-ttu-id="ea3ee-128">nessuno</span><span class="sxs-lookup"><span data-stu-id="ea3ee-128">None</span></span>                       |
| <span data-ttu-id="ea3ee-129">Contenuto dell'esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-129">Media Sample Contents</span></span> | <span data-ttu-id="ea3ee-130">Flusso di byte; nessun allineamento.</span><span class="sxs-lookup"><span data-stu-id="ea3ee-130">Byte stream; no alignment.</span></span> |



 

## <a name="mpeg-1-audio-packet"></a><span data-ttu-id="ea3ee-131">Pacchetto audio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="ea3ee-131">MPEG-1 Audio Packet</span></span>



| <span data-ttu-id="ea3ee-132">Label</span><span class="sxs-lookup"><span data-stu-id="ea3ee-132">Label</span></span> | <span data-ttu-id="ea3ee-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ea3ee-133">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="ea3ee-134">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-134">Major type</span></span>            | <span data-ttu-id="ea3ee-135">MEDIATYPE \_ Audio</span><span class="sxs-lookup"><span data-stu-id="ea3ee-135">MEDIATYPE\_Audio</span></span>                               |
| <span data-ttu-id="ea3ee-136">Subtype</span><span class="sxs-lookup"><span data-stu-id="ea3ee-136">Subtype</span></span>               | <span data-ttu-id="ea3ee-137">MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="ea3ee-137">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="ea3ee-138">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-138">Format Type</span></span>           | <span data-ttu-id="ea3ee-139">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="ea3ee-139">FORMAT\_WaveFormatEx</span></span>                           |
| <span data-ttu-id="ea3ee-140">Struttura del formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-140">Format Structure</span></span>      | [<span data-ttu-id="ea3ee-141">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="ea3ee-141">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| <span data-ttu-id="ea3ee-142">Contenuto dell'esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-142">Media Sample Contents</span></span> | <span data-ttu-id="ea3ee-143">Singolo pacchetto MPEG-1, inclusa l'intestazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="ea3ee-143">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-audio-payload"></a><span data-ttu-id="ea3ee-144">MPEG-1 Audio Payload</span><span class="sxs-lookup"><span data-stu-id="ea3ee-144">MPEG-1 Audio Payload</span></span>



| <span data-ttu-id="ea3ee-145">Label</span><span class="sxs-lookup"><span data-stu-id="ea3ee-145">Label</span></span> | <span data-ttu-id="ea3ee-146">Valore</span><span class="sxs-lookup"><span data-stu-id="ea3ee-146">Value</span></span> |
|-----------------------|--------------------------------------------|
| <span data-ttu-id="ea3ee-147">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-147">Major type</span></span>            | <span data-ttu-id="ea3ee-148">MEDIATYPE \_ Audio</span><span class="sxs-lookup"><span data-stu-id="ea3ee-148">MEDIATYPE\_Audio</span></span>                           |
| <span data-ttu-id="ea3ee-149">Subtype</span><span class="sxs-lookup"><span data-stu-id="ea3ee-149">Subtype</span></span>               | <span data-ttu-id="ea3ee-150">MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="ea3ee-150">MEDIASUBTYPE\_MPEG1Payload</span></span>                 |
| <span data-ttu-id="ea3ee-151">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-151">Format Type</span></span>           | <span data-ttu-id="ea3ee-152">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="ea3ee-152">FORMAT\_WaveFormatEx</span></span>                       |
| <span data-ttu-id="ea3ee-153">Struttura del formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-153">Format Structure</span></span>      | [<span data-ttu-id="ea3ee-154">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="ea3ee-154">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| <span data-ttu-id="ea3ee-155">Contenuto dell'esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-155">Media Sample Contents</span></span> | <span data-ttu-id="ea3ee-156">Dati audio MPEG-1 allineati ai byte.</span><span class="sxs-lookup"><span data-stu-id="ea3ee-156">Byte-aligned MPEG-1 audio data.</span></span>            |



 

## <a name="mpeg-1-video-packet"></a><span data-ttu-id="ea3ee-157">Pacchetto video MPEG-1</span><span class="sxs-lookup"><span data-stu-id="ea3ee-157">MPEG-1 Video Packet</span></span>



| <span data-ttu-id="ea3ee-158">Label</span><span class="sxs-lookup"><span data-stu-id="ea3ee-158">Label</span></span> | <span data-ttu-id="ea3ee-159">Valore</span><span class="sxs-lookup"><span data-stu-id="ea3ee-159">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="ea3ee-160">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-160">Major type</span></span>            | <span data-ttu-id="ea3ee-161">MEDIATYPE \_ Video</span><span class="sxs-lookup"><span data-stu-id="ea3ee-161">MEDIATYPE\_Video</span></span>                               |
| <span data-ttu-id="ea3ee-162">Subtype</span><span class="sxs-lookup"><span data-stu-id="ea3ee-162">Subtype</span></span>               | <span data-ttu-id="ea3ee-163">MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="ea3ee-163">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="ea3ee-164">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-164">Format Type</span></span>           | <span data-ttu-id="ea3ee-165">FORMAT \_ MPEGVideo</span><span class="sxs-lookup"><span data-stu-id="ea3ee-165">FORMAT\_MPEGVideo</span></span>                              |
| <span data-ttu-id="ea3ee-166">Struttura del formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-166">Format Structure</span></span>      | [<span data-ttu-id="ea3ee-167">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="ea3ee-167">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| <span data-ttu-id="ea3ee-168">Contenuto dell'esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-168">Media Sample Contents</span></span> | <span data-ttu-id="ea3ee-169">Singolo pacchetto MPEG-1, inclusa l'intestazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="ea3ee-169">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-video-payload"></a><span data-ttu-id="ea3ee-170">Payload video MPEG-1</span><span class="sxs-lookup"><span data-stu-id="ea3ee-170">MPEG-1 Video payload</span></span>



| <span data-ttu-id="ea3ee-171">Label</span><span class="sxs-lookup"><span data-stu-id="ea3ee-171">Label</span></span> | <span data-ttu-id="ea3ee-172">Valore</span><span class="sxs-lookup"><span data-stu-id="ea3ee-172">Value</span></span> |
|-----------------------|------------------------------------------|
| <span data-ttu-id="ea3ee-173">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-173">Major type</span></span>            | <span data-ttu-id="ea3ee-174">MEDIATYPE \_ Video</span><span class="sxs-lookup"><span data-stu-id="ea3ee-174">MEDIATYPE\_Video</span></span>                         |
| <span data-ttu-id="ea3ee-175">Subtype</span><span class="sxs-lookup"><span data-stu-id="ea3ee-175">Subtype</span></span>               | <span data-ttu-id="ea3ee-176">MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="ea3ee-176">MEDIASUBTYPE\_MPEG1Payload</span></span>               |
| <span data-ttu-id="ea3ee-177">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-177">Format Type</span></span>           | <span data-ttu-id="ea3ee-178">FORMAT \_ MPEGVideo</span><span class="sxs-lookup"><span data-stu-id="ea3ee-178">FORMAT\_MPEGVideo</span></span>                        |
| <span data-ttu-id="ea3ee-179">Struttura del formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-179">Format Structure</span></span>      | [<span data-ttu-id="ea3ee-180">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="ea3ee-180">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| <span data-ttu-id="ea3ee-181">Contenuto dell'esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-181">Media Sample Contents</span></span> | <span data-ttu-id="ea3ee-182">Dati video MPEG-1 allineati ai byte.</span><span class="sxs-lookup"><span data-stu-id="ea3ee-182">Byte-aligned MPEG-1 video data.</span></span>          |



 

## <a name="mpeg-1-native-video-stream"></a><span data-ttu-id="ea3ee-183">Flusso video nativo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="ea3ee-183">MPEG-1 Native Video Stream</span></span>



| <span data-ttu-id="ea3ee-184">Label</span><span class="sxs-lookup"><span data-stu-id="ea3ee-184">Label</span></span> | <span data-ttu-id="ea3ee-185">Valore</span><span class="sxs-lookup"><span data-stu-id="ea3ee-185">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="ea3ee-186">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-186">Major type</span></span>            | <span data-ttu-id="ea3ee-187">Flusso \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="ea3ee-187">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="ea3ee-188">Subtype</span><span class="sxs-lookup"><span data-stu-id="ea3ee-188">Subtype</span></span>               | <span data-ttu-id="ea3ee-189">MEDIASUBTYPE \_ MPEG1Video</span><span class="sxs-lookup"><span data-stu-id="ea3ee-189">MEDIASUBTYPE\_ MPEG1Video</span></span>                      |
| <span data-ttu-id="ea3ee-190">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-190">Format Type</span></span>           | <span data-ttu-id="ea3ee-191">GUID \_ NULL</span><span class="sxs-lookup"><span data-stu-id="ea3ee-191">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="ea3ee-192">Struttura del formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-192">Format Structure</span></span>      | <span data-ttu-id="ea3ee-193">nessuno</span><span class="sxs-lookup"><span data-stu-id="ea3ee-193">None</span></span>                                           |
| <span data-ttu-id="ea3ee-194">Contenuto dell'esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-194">Media Sample Contents</span></span> | <span data-ttu-id="ea3ee-195">Matrice di byte del flusso video (nessun livello di sistema).</span><span class="sxs-lookup"><span data-stu-id="ea3ee-195">Array of video stream bytes (no system layer).</span></span> |



 

## <a name="mpeg-1-native-audio-stream"></a><span data-ttu-id="ea3ee-196">Flusso audio nativo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="ea3ee-196">MPEG-1 Native Audio Stream</span></span>



| <span data-ttu-id="ea3ee-197">Label</span><span class="sxs-lookup"><span data-stu-id="ea3ee-197">Label</span></span> | <span data-ttu-id="ea3ee-198">Valore</span><span class="sxs-lookup"><span data-stu-id="ea3ee-198">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="ea3ee-199">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-199">Major type</span></span>            | <span data-ttu-id="ea3ee-200">Flusso \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="ea3ee-200">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="ea3ee-201">Subtype</span><span class="sxs-lookup"><span data-stu-id="ea3ee-201">Subtype</span></span>               | <span data-ttu-id="ea3ee-202">MEDIASUBTYPE \_ MPEG1Audio</span><span class="sxs-lookup"><span data-stu-id="ea3ee-202">MEDIASUBTYPE\_ MPEG1Audio</span></span>                      |
| <span data-ttu-id="ea3ee-203">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-203">Format Type</span></span>           | <span data-ttu-id="ea3ee-204">GUID \_ NULL</span><span class="sxs-lookup"><span data-stu-id="ea3ee-204">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="ea3ee-205">Struttura del formato</span><span class="sxs-lookup"><span data-stu-id="ea3ee-205">Format Structure</span></span>      | <span data-ttu-id="ea3ee-206">nessuno</span><span class="sxs-lookup"><span data-stu-id="ea3ee-206">None</span></span>                                           |
| <span data-ttu-id="ea3ee-207">Contenuto dell'esempio multimediale</span><span class="sxs-lookup"><span data-stu-id="ea3ee-207">Media Sample Contents</span></span> | <span data-ttu-id="ea3ee-208">Matrice di byte del flusso audio (nessun livello di sistema).</span><span class="sxs-lookup"><span data-stu-id="ea3ee-208">Array of audio stream bytes (no system layer).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ea3ee-209">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea3ee-209">Remarks</span></span>

<span data-ttu-id="ea3ee-210">I filtri DirectShow MPEG-1 supportano questi tipi come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="ea3ee-210">The DirectShow MPEG-1 filters support these types as follows.</span></span>



| <span data-ttu-id="ea3ee-211">Filtra</span><span class="sxs-lookup"><span data-stu-id="ea3ee-211">Filter</span></span>               | <span data-ttu-id="ea3ee-212">Direzione</span><span class="sxs-lookup"><span data-stu-id="ea3ee-212">Direction</span></span> | <span data-ttu-id="ea3ee-213">Tipi di supporti supportati</span><span class="sxs-lookup"><span data-stu-id="ea3ee-213">Supported media types</span></span>                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3ee-214">Separatore MPEG-1</span><span class="sxs-lookup"><span data-stu-id="ea3ee-214">MPEG-1 Splitter</span></span>      | <span data-ttu-id="ea3ee-215">Input</span><span class="sxs-lookup"><span data-stu-id="ea3ee-215">Input</span></span>     | <span data-ttu-id="ea3ee-216">Flusso di sistema MPEG-1 flusso di sistemaMPEG-1 da Video CD</span><span class="sxs-lookup"><span data-stu-id="ea3ee-216">MPEG-1 system streamMPEG-1 system stream from Video CD</span></span><br/>                                                 |
| <span data-ttu-id="ea3ee-217">Separatore MPEG-1</span><span class="sxs-lookup"><span data-stu-id="ea3ee-217">MPEG-1 Splitter</span></span>      | <span data-ttu-id="ea3ee-218">Output</span><span class="sxs-lookup"><span data-stu-id="ea3ee-218">Output</span></span>    | <span data-ttu-id="ea3ee-219">Pacchetto audio MPEG-1 PAYLOAD audioMPEG-1</span><span class="sxs-lookup"><span data-stu-id="ea3ee-219">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/> <span data-ttu-id="ea3ee-220">Pacchetto video MPEG-1</span><span class="sxs-lookup"><span data-stu-id="ea3ee-220">MPEG-1 Video packet</span></span><br/> <span data-ttu-id="ea3ee-221">Payload video MPEG-1</span><span class="sxs-lookup"><span data-stu-id="ea3ee-221">MPEG-1 Video payload</span></span><br/> |
| <span data-ttu-id="ea3ee-222">Software Audio Codec</span><span class="sxs-lookup"><span data-stu-id="ea3ee-222">Software Audio Codec</span></span> | <span data-ttu-id="ea3ee-223">Input</span><span class="sxs-lookup"><span data-stu-id="ea3ee-223">Input</span></span>     | <span data-ttu-id="ea3ee-224">Pacchetto audio MPEG-1 PAYLOAD audioMPEG-1</span><span class="sxs-lookup"><span data-stu-id="ea3ee-224">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/>                                                                |
| <span data-ttu-id="ea3ee-225">Software Video Codec</span><span class="sxs-lookup"><span data-stu-id="ea3ee-225">Software Video Codec</span></span> | <span data-ttu-id="ea3ee-226">Input</span><span class="sxs-lookup"><span data-stu-id="ea3ee-226">Input</span></span>     | <span data-ttu-id="ea3ee-227">Payload video MPEG-1 pacchetto videoMPEG-1</span><span class="sxs-lookup"><span data-stu-id="ea3ee-227">MPEG-1 Video packetMPEG-1 Video payload</span></span><br/>                                                                |
| <span data-ttu-id="ea3ee-228">Software Audio Codec</span><span class="sxs-lookup"><span data-stu-id="ea3ee-228">Software Audio Codec</span></span> | <span data-ttu-id="ea3ee-229">Output</span><span class="sxs-lookup"><span data-stu-id="ea3ee-229">Output</span></span>    | <span data-ttu-id="ea3ee-230">Audio PCM</span><span class="sxs-lookup"><span data-stu-id="ea3ee-230">PCM audio</span></span>                                                                                                         |
| <span data-ttu-id="ea3ee-231">Software Video Codec</span><span class="sxs-lookup"><span data-stu-id="ea3ee-231">Software Video Codec</span></span> | <span data-ttu-id="ea3ee-232">Output</span><span class="sxs-lookup"><span data-stu-id="ea3ee-232">Output</span></span>    | <span data-ttu-id="ea3ee-233">Video non compresso (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span><span class="sxs-lookup"><span data-stu-id="ea3ee-233">Uncompressed video (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span></span>                                    |



 

<span data-ttu-id="ea3ee-234">I tipi di supporti di payload e pacchetto video MPEG-1 contengono un'intestazione di sequenza completa in modo che i dati possano essere riprodotti dal centro di un file senza la necessità di un'intestazione di sequenza per inizializzare la riproduzione video.</span><span class="sxs-lookup"><span data-stu-id="ea3ee-234">MPEG-1 Video packet and payload media types contain a complete sequence header so that data can be played from the middle of a file without needing a sequence header to initialize the video playback.</span></span>

<span data-ttu-id="ea3ee-235">L'intestazione della sequenza video viene aggiunta al tipo di dati video per il video MPEG in modo che la riproduzione possa iniziare dal centro di un flusso.</span><span class="sxs-lookup"><span data-stu-id="ea3ee-235">The video sequence header is appended to the video data type for MPEG video so that play can begin from the middle of a stream.</span></span> <span data-ttu-id="ea3ee-236">La lunghezza di questo campo è fino a 140 byte. include il codice di inizio dell'intestazione di sequenza (0x000001B3) all'inizio, insieme alle matrici di quantizzazione trovate nella prima intestazione di sequenza rilevata.</span><span class="sxs-lookup"><span data-stu-id="ea3ee-236">The length of this field is up to 140 bytes; it includes the sequence header start code (0x000001B3) at the start, along with any quantization matrices found in the first sequence header encountered.</span></span>

 

 




