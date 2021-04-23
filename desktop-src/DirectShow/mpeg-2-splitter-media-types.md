---
description: Tipi di supporti con separatore MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipi di supporti con separatore MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e878acaea8bc87bee2bf5c46a6f7e66c7aa0a485
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909428"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="1071f-103">Tipi di supporti con separatore MPEG-2</span><span class="sxs-lookup"><span data-stu-id="1071f-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="1071f-104">Il [filtro mpeg-2 splitter](mpeg-2-splitter.md) supporta attualmente audio e video.</span><span class="sxs-lookup"><span data-stu-id="1071f-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="1071f-105">Dolby AC-3 è supportato come flusso secondario come definito da DVD.</span><span class="sxs-lookup"><span data-stu-id="1071f-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="1071f-106">Il filtro supporta anche l'audio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="1071f-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="1071f-107">I tipi di supporti variano a seconda che la barra di divisione MPEG-2 invii pacchetti PES o payload PES.</span><span class="sxs-lookup"><span data-stu-id="1071f-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="1071f-108">Video</span><span class="sxs-lookup"><span data-stu-id="1071f-108">Video</span></span>

<span data-ttu-id="1071f-109">Per i video MPEG-2, i tipi di file multimediali sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="1071f-109">For MPEG-2 video, the media types are as follows.</span></span>



| <span data-ttu-id="1071f-110">Label</span><span class="sxs-lookup"><span data-stu-id="1071f-110">Label</span></span> | <span data-ttu-id="1071f-111">Valore</span><span class="sxs-lookup"><span data-stu-id="1071f-111">Value</span></span> |
|------------------|------------------------------------------|--------------------------------|
|                  | <span data-ttu-id="1071f-112">Output PES</span><span class="sxs-lookup"><span data-stu-id="1071f-112">PES output</span></span>                               | <span data-ttu-id="1071f-113">Output del payload</span><span class="sxs-lookup"><span data-stu-id="1071f-113">Payload output</span></span>                 |
| <span data-ttu-id="1071f-114">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="1071f-114">Major Type</span></span>       | <span data-ttu-id="1071f-115">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="1071f-115">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="1071f-116">**MEDIATYPE \_ Video**</span><span class="sxs-lookup"><span data-stu-id="1071f-116">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="1071f-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="1071f-117">Subtype</span></span>          | <span data-ttu-id="1071f-118">**MEDIASUBTYPE \_ MPEG2 \_ VIDEO**</span><span class="sxs-lookup"><span data-stu-id="1071f-118">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="1071f-119">**MEDIASUBTYPE \_ MPEG2 \_ VIDEO**</span><span class="sxs-lookup"><span data-stu-id="1071f-119">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="1071f-120">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="1071f-120">Format Type</span></span>      | <span data-ttu-id="1071f-121">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="1071f-121">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="1071f-122">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="1071f-122">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="1071f-123">Struttura del formato</span><span class="sxs-lookup"><span data-stu-id="1071f-123">Format Structure</span></span> | [<span data-ttu-id="1071f-124">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="1071f-124">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="1071f-125">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="1071f-125">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="1071f-126">AC-3 Audio</span><span class="sxs-lookup"><span data-stu-id="1071f-126">AC-3 Audio</span></span>

<span data-ttu-id="1071f-127">Per l'audio AC-3, i tipi di supporti sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="1071f-127">For AC-3 audio, the media types are as follows.</span></span>



| <span data-ttu-id="1071f-128">Label</span><span class="sxs-lookup"><span data-stu-id="1071f-128">Label</span></span> | <span data-ttu-id="1071f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="1071f-129">Value</span></span> |
|------------------|--------------------------------------|------------------------------|
|                  | <span data-ttu-id="1071f-130">Output PES</span><span class="sxs-lookup"><span data-stu-id="1071f-130">PES output</span></span>                           | <span data-ttu-id="1071f-131">Output del payload</span><span class="sxs-lookup"><span data-stu-id="1071f-131">Payload output</span></span>               |
| <span data-ttu-id="1071f-132">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="1071f-132">Major Type</span></span>       | <span data-ttu-id="1071f-133">MEDIATYPE \_ MPEG2 \_ PES</span><span class="sxs-lookup"><span data-stu-id="1071f-133">MEDIATYPE\_MPEG2\_PES</span></span>                | <span data-ttu-id="1071f-134">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="1071f-134">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="1071f-135">Subtype</span><span class="sxs-lookup"><span data-stu-id="1071f-135">Subtype</span></span>          | <span data-ttu-id="1071f-136">MEDIASUBTYPE \_ DOLBY \_ AC3</span><span class="sxs-lookup"><span data-stu-id="1071f-136">MEDIASUBTYPE\_DOLBY\_AC3</span></span>             | <span data-ttu-id="1071f-137">**MEDIASUBTYPE \_ DOLBY \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="1071f-137">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="1071f-138">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="1071f-138">Format Type</span></span>      | <span data-ttu-id="1071f-139">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="1071f-139">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="1071f-140">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="1071f-140">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="1071f-141">Struttura del formato</span><span class="sxs-lookup"><span data-stu-id="1071f-141">Format Structure</span></span> | <span data-ttu-id="1071f-142">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1071f-142">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="1071f-143">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="1071f-143">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="1071f-144">Il membro **wFormatTag** della struttura **WAVEFORMATEX** per AC-3 è attualmente **WAVE FORMAT \_ \_ UNKNOWN,** ma potrebbe cambiare.</span><span class="sxs-lookup"><span data-stu-id="1071f-144">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="1071f-145">MPEG-2 Audio</span><span class="sxs-lookup"><span data-stu-id="1071f-145">MPEG-2 Audio</span></span>

<span data-ttu-id="1071f-146">Per l'audio MPEG-2, i tipi di supporti sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="1071f-146">For MPEG-2 audio, the media types are as follows.</span></span>



| <span data-ttu-id="1071f-147">Label</span><span class="sxs-lookup"><span data-stu-id="1071f-147">Label</span></span> | <span data-ttu-id="1071f-148">Valore</span><span class="sxs-lookup"><span data-stu-id="1071f-148">Value</span></span> |
|------------------|-------------------------------|--------------------------------|
|                  | <span data-ttu-id="1071f-149">Output PES</span><span class="sxs-lookup"><span data-stu-id="1071f-149">PES output</span></span>                    | <span data-ttu-id="1071f-150">Output del payload</span><span class="sxs-lookup"><span data-stu-id="1071f-150">Payload output</span></span>                 |
| <span data-ttu-id="1071f-151">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="1071f-151">Major Type</span></span>       | <span data-ttu-id="1071f-152">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="1071f-152">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="1071f-153">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="1071f-153">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="1071f-154">Subtype</span><span class="sxs-lookup"><span data-stu-id="1071f-154">Subtype</span></span>          | <span data-ttu-id="1071f-155">**MEDIASUBTYE \_ MPEG2 \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="1071f-155">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="1071f-156">**MEDIASUBTYPE \_ MPEG2 \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="1071f-156">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="1071f-157">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="1071f-157">Format Type</span></span>      | <span data-ttu-id="1071f-158">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="1071f-158">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="1071f-159">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="1071f-159">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="1071f-160">Struttura del formato</span><span class="sxs-lookup"><span data-stu-id="1071f-160">Format Structure</span></span> | <span data-ttu-id="1071f-161">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="1071f-161">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="1071f-162">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="1071f-162">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="1071f-163">Il membro **wFormatTag** della struttura **WAVEFORMATEX** per l'audio MPEG-2 è attualmente **WAVE FORMAT \_ \_ UNKNOWN,** ma questo potrebbe cambiare.</span><span class="sxs-lookup"><span data-stu-id="1071f-163">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="1071f-164">Lo splitter MPEG-2 presuppone che i flussi da D0 a DF siano usati per il flusso di estensione multicanale, come per l'audio DVD MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="1071f-164">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="1071f-165">Pertanto, ogni volta che viene selezionato il flusso C *x,* la barra di divisione inoltra anche i pacchetti per il flusso D *x.*</span><span class="sxs-lookup"><span data-stu-id="1071f-165">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="1071f-166">Audio di Gestione configurazione locale</span><span class="sxs-lookup"><span data-stu-id="1071f-166">LPCM Audio</span></span>

<span data-ttu-id="1071f-167">Per l'audio di Gestione configurazione locale, i tipi di supporti sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="1071f-167">For LPCM audio, the media types are as follows.</span></span>



| <span data-ttu-id="1071f-168">Label</span><span class="sxs-lookup"><span data-stu-id="1071f-168">Label</span></span> | <span data-ttu-id="1071f-169">Valore</span><span class="sxs-lookup"><span data-stu-id="1071f-169">Value</span></span> |
|------------------|------------------------------------|------------------------------------|
|                  | <span data-ttu-id="1071f-170">Output PES</span><span class="sxs-lookup"><span data-stu-id="1071f-170">PES output</span></span>                         | <span data-ttu-id="1071f-171">Output del payload</span><span class="sxs-lookup"><span data-stu-id="1071f-171">Payload output</span></span>                     |
| <span data-ttu-id="1071f-172">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="1071f-172">Major Type</span></span>       | <span data-ttu-id="1071f-173">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="1071f-173">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="1071f-174">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="1071f-174">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="1071f-175">Subtype</span><span class="sxs-lookup"><span data-stu-id="1071f-175">Subtype</span></span>          | <span data-ttu-id="1071f-176">**MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="1071f-176">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="1071f-177">**MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="1071f-177">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="1071f-178">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="1071f-178">Format Type</span></span>      | <span data-ttu-id="1071f-179">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="1071f-179">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="1071f-180">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="1071f-180">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="1071f-181">Struttura del formato</span><span class="sxs-lookup"><span data-stu-id="1071f-181">Format Structure</span></span> | <span data-ttu-id="1071f-182">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="1071f-182">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="1071f-183">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="1071f-183">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="1071f-184">Il membro **wFormatTag** della struttura **WAVEFORMATEX** per l'audio LPCM è attualmente **WAVE FORMAT \_ \_ UNKNOWN,** ma potrebbe cambiare.</span><span class="sxs-lookup"><span data-stu-id="1071f-184">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1071f-185">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1071f-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1071f-186">Tipi di supporti MPEG-2</span><span class="sxs-lookup"><span data-stu-id="1071f-186">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
