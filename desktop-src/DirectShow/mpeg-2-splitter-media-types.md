---
description: Tipi di supporto per la barra di divisione MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipi di supporto per la barra di divisione MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb10310bd126346c8e1558801200682792836d92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320597"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="faa24-103">Tipi di supporto per la barra di divisione MPEG-2</span><span class="sxs-lookup"><span data-stu-id="faa24-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="faa24-104">Il filtro [splitter MPEG-2](mpeg-2-splitter.md) supporta attualmente audio e video.</span><span class="sxs-lookup"><span data-stu-id="faa24-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="faa24-105">Dolby AC-3 è supportato come sottoflusso come definito da DVD.</span><span class="sxs-lookup"><span data-stu-id="faa24-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="faa24-106">Il filtro supporta anche audio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="faa24-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="faa24-107">I tipi di supporto variano a seconda che il separatore MPEG-2 stia distribuendo pacchetti PES o payload di PES.</span><span class="sxs-lookup"><span data-stu-id="faa24-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="faa24-108">Video</span><span class="sxs-lookup"><span data-stu-id="faa24-108">Video</span></span>

<span data-ttu-id="faa24-109">Per il video MPEG-2, i tipi di supporto sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="faa24-109">For MPEG-2 video, the media types are as follows.</span></span>



|                  |                                          |                                |
|------------------|------------------------------------------|--------------------------------|
|                  | <span data-ttu-id="faa24-110">Output PES</span><span class="sxs-lookup"><span data-stu-id="faa24-110">PES output</span></span>                               | <span data-ttu-id="faa24-111">Output payload</span><span class="sxs-lookup"><span data-stu-id="faa24-111">Payload output</span></span>                 |
| <span data-ttu-id="faa24-112">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="faa24-112">Major Type</span></span>       | <span data-ttu-id="faa24-113">**\_PES MEDIATYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="faa24-113">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="faa24-114">**Video di MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="faa24-114">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="faa24-115">Subtype</span><span class="sxs-lookup"><span data-stu-id="faa24-115">Subtype</span></span>          | <span data-ttu-id="faa24-116">**VIDEO di MEDIASUBTYPE \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="faa24-116">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="faa24-117">**VIDEO di MEDIASUBTYPE \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="faa24-117">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="faa24-118">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="faa24-118">Format Type</span></span>      | <span data-ttu-id="faa24-119">**FORMATO \_ mpeg2video**</span><span class="sxs-lookup"><span data-stu-id="faa24-119">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="faa24-120">**FORMATO \_ mpeg2video**</span><span class="sxs-lookup"><span data-stu-id="faa24-120">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="faa24-121">Struttura Format</span><span class="sxs-lookup"><span data-stu-id="faa24-121">Format Structure</span></span> | [<span data-ttu-id="faa24-122">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="faa24-122">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="faa24-123">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="faa24-123">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="faa24-124">Audio AC-3</span><span class="sxs-lookup"><span data-stu-id="faa24-124">AC-3 Audio</span></span>

<span data-ttu-id="faa24-125">Per l'audio AC-3, i tipi di supporto sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="faa24-125">For AC-3 audio, the media types are as follows.</span></span>



|                  |                                      |                              |
|------------------|--------------------------------------|------------------------------|
|                  | <span data-ttu-id="faa24-126">Output PES</span><span class="sxs-lookup"><span data-stu-id="faa24-126">PES output</span></span>                           | <span data-ttu-id="faa24-127">Output payload</span><span class="sxs-lookup"><span data-stu-id="faa24-127">Payload output</span></span>               |
| <span data-ttu-id="faa24-128">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="faa24-128">Major Type</span></span>       | <span data-ttu-id="faa24-129">\_PES MEDIATYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="faa24-129">MEDIATYPE\_MPEG2\_PES</span></span>                | <span data-ttu-id="faa24-130">**\_Audio MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="faa24-130">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="faa24-131">Subtype</span><span class="sxs-lookup"><span data-stu-id="faa24-131">Subtype</span></span>          | <span data-ttu-id="faa24-132">MEDIASUBTYPE \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="faa24-132">MEDIASUBTYPE\_DOLBY\_AC3</span></span>             | <span data-ttu-id="faa24-133">**MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="faa24-133">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="faa24-134">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="faa24-134">Format Type</span></span>      | <span data-ttu-id="faa24-135">FORMATO \_ WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="faa24-135">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="faa24-136">**FORMATO \_ WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="faa24-136">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="faa24-137">Struttura Format</span><span class="sxs-lookup"><span data-stu-id="faa24-137">Format Structure</span></span> | <span data-ttu-id="faa24-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="faa24-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="faa24-139">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="faa24-139">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="faa24-140">Il membro **wFormatTag** della struttura **WAVEFORMATEX** per AC-3 è attualmente **\_ \_ sconosciuto nel formato Wave**, ma questo potrebbe cambiare.</span><span class="sxs-lookup"><span data-stu-id="faa24-140">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="faa24-141">Audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="faa24-141">MPEG-2 Audio</span></span>

<span data-ttu-id="faa24-142">Per l'audio MPEG-2, i tipi di supporto sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="faa24-142">For MPEG-2 audio, the media types are as follows.</span></span>



|                  |                               |                                |
|------------------|-------------------------------|--------------------------------|
|                  | <span data-ttu-id="faa24-143">Output PES</span><span class="sxs-lookup"><span data-stu-id="faa24-143">PES output</span></span>                    | <span data-ttu-id="faa24-144">Output payload</span><span class="sxs-lookup"><span data-stu-id="faa24-144">Payload output</span></span>                 |
| <span data-ttu-id="faa24-145">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="faa24-145">Major Type</span></span>       | <span data-ttu-id="faa24-146">**\_PES MEDIATYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="faa24-146">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="faa24-147">**\_Audio MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="faa24-147">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="faa24-148">Subtype</span><span class="sxs-lookup"><span data-stu-id="faa24-148">Subtype</span></span>          | <span data-ttu-id="faa24-149">**\_Audio MPEG2 \_ MEDIASUBTYE**</span><span class="sxs-lookup"><span data-stu-id="faa24-149">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="faa24-150">**\_Audio MPEG2 \_ MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="faa24-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="faa24-151">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="faa24-151">Format Type</span></span>      | <span data-ttu-id="faa24-152">**FORMATO \_ WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="faa24-152">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="faa24-153">**FORMATO \_ WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="faa24-153">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="faa24-154">Struttura Format</span><span class="sxs-lookup"><span data-stu-id="faa24-154">Format Structure</span></span> | <span data-ttu-id="faa24-155">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="faa24-155">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="faa24-156">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="faa24-156">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="faa24-157">Il membro **wFormatTag** della struttura **WAVEFORMATEX** per l'audio MPEG-2 è **attualmente \_ \_ sconosciuto**, ma questo potrebbe cambiare.</span><span class="sxs-lookup"><span data-stu-id="faa24-157">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="faa24-158">Il separatore MPEG-2 presuppone che i flussi da D0 a DF vengano usati per il flusso di estensioni multicanale, come per l'audio MPEG-2 DVD.</span><span class="sxs-lookup"><span data-stu-id="faa24-158">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="faa24-159">Pertanto, ogni volta che si seleziona Stream C *x* , la barra di divisione inoltra anche i pacchetti per il flusso D *x* .</span><span class="sxs-lookup"><span data-stu-id="faa24-159">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="faa24-160">Audio LPCM</span><span class="sxs-lookup"><span data-stu-id="faa24-160">LPCM Audio</span></span>

<span data-ttu-id="faa24-161">Per l'audio LPCM, i tipi di supporto sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="faa24-161">For LPCM audio, the media types are as follows.</span></span>



|                  |                                    |                                    |
|------------------|------------------------------------|------------------------------------|
|                  | <span data-ttu-id="faa24-162">Output PES</span><span class="sxs-lookup"><span data-stu-id="faa24-162">PES output</span></span>                         | <span data-ttu-id="faa24-163">Output payload</span><span class="sxs-lookup"><span data-stu-id="faa24-163">Payload output</span></span>                     |
| <span data-ttu-id="faa24-164">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="faa24-164">Major Type</span></span>       | <span data-ttu-id="faa24-165">**\_PES MEDIATYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="faa24-165">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="faa24-166">**\_Audio MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="faa24-166">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="faa24-167">Subtype</span><span class="sxs-lookup"><span data-stu-id="faa24-167">Subtype</span></span>          | <span data-ttu-id="faa24-168">**\_audio MEDIASUBTYPE DVD \_ LPCM \_**</span><span class="sxs-lookup"><span data-stu-id="faa24-168">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="faa24-169">**\_audio MEDIASUBTYPE DVD \_ LPCM \_**</span><span class="sxs-lookup"><span data-stu-id="faa24-169">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="faa24-170">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="faa24-170">Format Type</span></span>      | <span data-ttu-id="faa24-171">**FORMATO \_ WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="faa24-171">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="faa24-172">**FORMATO \_ WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="faa24-172">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="faa24-173">Struttura Format</span><span class="sxs-lookup"><span data-stu-id="faa24-173">Format Structure</span></span> | <span data-ttu-id="faa24-174">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="faa24-174">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="faa24-175">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="faa24-175">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="faa24-176">Il membro **wFormatTag** della struttura **WAVEFORMATEX** per l'audio LPCM è **attualmente \_ \_ sconosciuto**, ma questo potrebbe cambiare.</span><span class="sxs-lookup"><span data-stu-id="faa24-176">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="faa24-177">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="faa24-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faa24-178">Tipi di supporti MPEG-2</span><span class="sxs-lookup"><span data-stu-id="faa24-178">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
