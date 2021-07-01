---
description: Tipi di supporti splitter MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipi di supporti splitter MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4e025fafabdeb8c437cc1d1cd6fbb843cf63e3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119976"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="36c4c-103">Tipi di supporti splitter MPEG-2</span><span class="sxs-lookup"><span data-stu-id="36c4c-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="36c4c-104">Il [filtro mpeg-2 splitter](mpeg-2-splitter.md) supporta attualmente audio e video.</span><span class="sxs-lookup"><span data-stu-id="36c4c-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="36c4c-105">Dolby AC-3 è supportato come flusso secondario come definito da DVD.</span><span class="sxs-lookup"><span data-stu-id="36c4c-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="36c4c-106">Il filtro supporta anche l'audio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="36c4c-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="36c4c-107">I tipi di supporti variano a seconda che lo splitter MPEG-2 consegnerà pacchetti PES o payload PES.</span><span class="sxs-lookup"><span data-stu-id="36c4c-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="36c4c-108">Video</span><span class="sxs-lookup"><span data-stu-id="36c4c-108">Video</span></span>

<span data-ttu-id="36c4c-109">Per i video MPEG-2, i tipi di supporti sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="36c4c-109">For MPEG-2 video, the media types are as follows.</span></span>


|                | <span data-ttu-id="36c4c-110">Output PES</span><span class="sxs-lookup"><span data-stu-id="36c4c-110">PES output</span></span> | <span data-ttu-id="36c4c-111">Output del payload</span><span class="sxs-lookup"><span data-stu-id="36c4c-111">Payload output</span></span>
|------------------|------------------------------------------|--------------------------------|
| <span data-ttu-id="36c4c-112">**Tipo principale**</span><span class="sxs-lookup"><span data-stu-id="36c4c-112">**Major type**</span></span>       | <span data-ttu-id="36c4c-113">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="36c4c-113">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="36c4c-114">**MEDIATYPE \_ Video**</span><span class="sxs-lookup"><span data-stu-id="36c4c-114">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="36c4c-115">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="36c4c-115">**Subtype**</span></span>          | <span data-ttu-id="36c4c-116">**MEDIASUBTYPE \_ MPEG2 \_ VIDEO**</span><span class="sxs-lookup"><span data-stu-id="36c4c-116">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="36c4c-117">**MEDIASUBTYPE \_ MPEG2 \_ VIDEO**</span><span class="sxs-lookup"><span data-stu-id="36c4c-117">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="36c4c-118">**Tipo di formato**</span><span class="sxs-lookup"><span data-stu-id="36c4c-118">**Format type**</span></span>      | <span data-ttu-id="36c4c-119">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="36c4c-119">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="36c4c-120">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="36c4c-120">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="36c4c-121">**Struttura del formato**</span><span class="sxs-lookup"><span data-stu-id="36c4c-121">**Format structure**</span></span> | [<span data-ttu-id="36c4c-122">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="36c4c-122">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="36c4c-123">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="36c4c-123">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="36c4c-124">AC-3 Audio</span><span class="sxs-lookup"><span data-stu-id="36c4c-124">AC-3 Audio</span></span>

<span data-ttu-id="36c4c-125">Per l'audio AC-3, i tipi di supporti sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="36c4c-125">For AC-3 audio, the media types are as follows.</span></span>

| | <span data-ttu-id="36c4c-126">Output PES</span><span class="sxs-lookup"><span data-stu-id="36c4c-126">PES output</span></span> | <span data-ttu-id="36c4c-127">Output del payload</span><span class="sxs-lookup"><span data-stu-id="36c4c-127">Payload output</span></span> |
|------------------|--------------------------------------|------------------------------|
| <span data-ttu-id="36c4c-128">**Tipo principale**</span><span class="sxs-lookup"><span data-stu-id="36c4c-128">**Major type**</span></span>       | <span data-ttu-id="36c4c-129">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="36c4c-129">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="36c4c-130">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="36c4c-130">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="36c4c-131">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="36c4c-131">**Subtype**</span></span>          | <span data-ttu-id="36c4c-132">**MEDIASUBTYPE \_ DOLBY \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="36c4c-132">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span>             | <span data-ttu-id="36c4c-133">**MEDIASUBTYPE \_ DOLBY \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="36c4c-133">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="36c4c-134">**Tipo di formato**</span><span class="sxs-lookup"><span data-stu-id="36c4c-134">**Format type**</span></span>      | <span data-ttu-id="36c4c-135">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="36c4c-135">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="36c4c-136">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="36c4c-136">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="36c4c-137">**Struttura del formato**</span><span class="sxs-lookup"><span data-stu-id="36c4c-137">**Format structure**</span></span> | <span data-ttu-id="36c4c-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="36c4c-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="36c4c-139">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="36c4c-139">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="36c4c-140">Il membro **wFormatTag** della struttura **WAVEFORMATEX** per AC-3 è attualmente **WAVE FORMAT \_ \_ UNKNOWN,** ma potrebbe cambiare.</span><span class="sxs-lookup"><span data-stu-id="36c4c-140">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="36c4c-141">MPEG-2 Audio</span><span class="sxs-lookup"><span data-stu-id="36c4c-141">MPEG-2 Audio</span></span>

<span data-ttu-id="36c4c-142">Per l'audio MPEG-2, i tipi di supporti sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="36c4c-142">For MPEG-2 audio, the media types are as follows.</span></span>



|  | <span data-ttu-id="36c4c-143">Output PES</span><span class="sxs-lookup"><span data-stu-id="36c4c-143">PES output</span></span> | <span data-ttu-id="36c4c-144">Output del payload</span><span class="sxs-lookup"><span data-stu-id="36c4c-144">Payload output</span></span> |
|------------------|-------------------------------|--------------------------------|
| <span data-ttu-id="36c4c-145">**Tipo principale**</span><span class="sxs-lookup"><span data-stu-id="36c4c-145">**Major type**</span></span>       | <span data-ttu-id="36c4c-146">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="36c4c-146">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="36c4c-147">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="36c4c-147">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="36c4c-148">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="36c4c-148">**Subtype**</span></span>          | <span data-ttu-id="36c4c-149">**MEDIASUBTYE \_ MPEG2 \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="36c4c-149">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="36c4c-150">**MEDIASUBTYPE \_ MPEG2 \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="36c4c-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="36c4c-151">**Tipo di formato**</span><span class="sxs-lookup"><span data-stu-id="36c4c-151">**Format type**</span></span>      | <span data-ttu-id="36c4c-152">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="36c4c-152">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="36c4c-153">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="36c4c-153">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="36c4c-154">**Struttura del formato**</span><span class="sxs-lookup"><span data-stu-id="36c4c-154">**Format structure**</span></span> | <span data-ttu-id="36c4c-155">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="36c4c-155">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="36c4c-156">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="36c4c-156">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="36c4c-157">Il membro **wFormatTag** della struttura **WAVEFORMATEX** per MPEG-2 Audio è attualmente **WAVE FORMAT \_ \_ UNKNOWN,** ma potrebbe cambiare.</span><span class="sxs-lookup"><span data-stu-id="36c4c-157">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="36c4c-158">Lo splitter MPEG-2 presuppone che i flussi da D0 a DF siano usati per il flusso di estensione multicanale, come per l'audio MPEG-2 DVD.</span><span class="sxs-lookup"><span data-stu-id="36c4c-158">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="36c4c-159">Pertanto, ogni volta che si seleziona il flusso C *x,* la barra di divisione inoltra anche i pacchetti per il flusso D *x.*</span><span class="sxs-lookup"><span data-stu-id="36c4c-159">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="36c4c-160">Audio di Gestione configurazione locale</span><span class="sxs-lookup"><span data-stu-id="36c4c-160">LPCM Audio</span></span>

<span data-ttu-id="36c4c-161">Per l'audio LPCM, i tipi di supporti sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="36c4c-161">For LPCM audio, the media types are as follows.</span></span>



|  | <span data-ttu-id="36c4c-162">Output PES</span><span class="sxs-lookup"><span data-stu-id="36c4c-162">PES output</span></span> | <span data-ttu-id="36c4c-163">Output del payload</span><span class="sxs-lookup"><span data-stu-id="36c4c-163">Payload output</span></span> |
|------------------|------------------------------------|------------------------------------|
| <span data-ttu-id="36c4c-164">**Tipo principale**</span><span class="sxs-lookup"><span data-stu-id="36c4c-164">**Major type**</span></span>       | <span data-ttu-id="36c4c-165">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="36c4c-165">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="36c4c-166">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="36c4c-166">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="36c4c-167">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="36c4c-167">**Subtype**</span></span>          | <span data-ttu-id="36c4c-168">**MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="36c4c-168">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="36c4c-169">**MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="36c4c-169">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="36c4c-170">**Tipo di formato**</span><span class="sxs-lookup"><span data-stu-id="36c4c-170">**Format type**</span></span>      | <span data-ttu-id="36c4c-171">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="36c4c-171">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="36c4c-172">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="36c4c-172">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="36c4c-173">**Struttura del formato**</span><span class="sxs-lookup"><span data-stu-id="36c4c-173">**Format structure**</span></span> | <span data-ttu-id="36c4c-174">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="36c4c-174">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="36c4c-175">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="36c4c-175">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="36c4c-176">Il membro **wFormatTag** della struttura **WAVEFORMATEX** per l'audio LPCM è attualmente **WAVE FORMAT \_ \_ UNKNOWN,** ma potrebbe cambiare.</span><span class="sxs-lookup"><span data-stu-id="36c4c-176">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36c4c-177">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36c4c-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36c4c-178">Tipi di supporti MPEG-2</span><span class="sxs-lookup"><span data-stu-id="36c4c-178">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
