---
description: MpEG-2 Tipi di supporti demultiplexer
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: MpEG-2 Tipi di supporti demultiplexer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9b5276b975771ba62118976c8e63b4d5faa53d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909999"
---
# <a name="mpeg-2-demultiplexer-media-types"></a><span data-ttu-id="e35a4-103">MpEG-2 Tipi di supporti demultiplexer</span><span class="sxs-lookup"><span data-stu-id="e35a4-103">MPEG-2 Demultiplexer Media Types</span></span>

<span data-ttu-id="e35a4-104">Il [filtro MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) riconosce i tipi di supporti seguenti.</span><span class="sxs-lookup"><span data-stu-id="e35a4-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) filter recognizes the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="e35a4-105">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="e35a4-105">Input Types</span></span>

<span data-ttu-id="e35a4-106">Il tipo principale è sempre **MEDIATYPE \_ Stream.**</span><span class="sxs-lookup"><span data-stu-id="e35a4-106">The major type is always **MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="e35a4-107">Il sottotipo può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="e35a4-107">The subtype can be any of the following.</span></span>



| <span data-ttu-id="e35a4-108">GUID</span><span class="sxs-lookup"><span data-stu-id="e35a4-108">GUID</span></span>                                             | <span data-ttu-id="e35a4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e35a4-109">Description</span></span>                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e35a4-110">**TRASPORTO \_ \_ MPEG2 DEL SOTTOTIPO KSDATAFORMAT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e35a4-110">**KSDATAFORMAT\_SUBTYPE\_BDA\_MPEG2\_TRANSPORT**</span></span> | <span data-ttu-id="e35a4-111">Flusso di trasporto da un filtro di dispositivo BDA (Broadcast Driver Architecture).</span><span class="sxs-lookup"><span data-stu-id="e35a4-111">Transport stream from a Broadcast Driver Architecture (BDA) device filter.</span></span> <span data-ttu-id="e35a4-112">Il demultiplex MPEG-2 tratta questo sottotipo in modo identico a **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT.**</span><span class="sxs-lookup"><span data-stu-id="e35a4-112">The MPEG-2 demultiplexer treats this subtype identically to **MEDIASUBTYPE\_MPEG2\_TRANSPORT**.</span></span>                                |
| <span data-ttu-id="e35a4-113">**PROGRAMMA \_ MPEG2 \_ MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="e35a4-113">**MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>                 | <span data-ttu-id="e35a4-114">Flusso del programma</span><span class="sxs-lookup"><span data-stu-id="e35a4-114">Program stream</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="e35a4-115">**MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**</span><span class="sxs-lookup"><span data-stu-id="e35a4-115">**MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>               | <span data-ttu-id="e35a4-116">Flusso di trasporto (TS), con pacchetti da 188 byte</span><span class="sxs-lookup"><span data-stu-id="e35a4-116">Transport stream (TS), with 188-byte packets</span></span>                                                                                                                                                              |
| <span data-ttu-id="e35a4-117">**MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE**</span><span class="sxs-lookup"><span data-stu-id="e35a4-117">**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**</span></span>       | <span data-ttu-id="e35a4-118">Flusso di trasporto con pacchetti "strided".</span><span class="sxs-lookup"><span data-stu-id="e35a4-118">Transport stream with "strided" packets.</span></span> <span data-ttu-id="e35a4-119">Questo sottotipo indica che i pacchetti TS possono essere riempiti con byte aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="e35a4-119">This subtype indicates that the TS packets may be padded with extra bytes.</span></span> <span data-ttu-id="e35a4-120">Per altre informazioni, vedere [**MPEG2 \_ TRANSPORT \_ STRIDE.**](mpeg2-transport-stride.md)</span><span class="sxs-lookup"><span data-stu-id="e35a4-120">For more information, see [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> |



 

<span data-ttu-id="e35a4-121">Per i pacchetti di trasporto strided **(MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE),** ogni campione di supporti deve contenere un numero integrale di pacchetti di trasporto, come descritto in [**MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="e35a4-121">For strided transport packets (**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**), each media sample must contain an integral number of transport packets, as described in [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> <span data-ttu-id="e35a4-122">Per tutti gli altri tipi di input, non sono presenti restrizioni sui limiti di esempio. I singoli pacchetti possono estendersi oltre i limiti del campione.</span><span class="sxs-lookup"><span data-stu-id="e35a4-122">For all other input types, there are no restrictions on sample boundaries; individual packets can span sample boundaries.</span></span>

### <a name="output-types"></a><span data-ttu-id="e35a4-123">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="e35a4-123">Output Types</span></span>

<span data-ttu-id="e35a4-124">Il demultiplexer MPEG-2 non convalida i tipi di output. Il filtro downstream è responsabile dell'analisi dei dati ricevuti dal demultiplexer.</span><span class="sxs-lookup"><span data-stu-id="e35a4-124">The MPEG-2 Demultiplexer does not validate output types; the downstream filter is responsible for parsing the data it receives from the demultiplexer.</span></span> <span data-ttu-id="e35a4-125">Tuttavia, i tipi seguenti sono comunemente accettati dai filtri downstream come output dal demultiplexer.</span><span class="sxs-lookup"><span data-stu-id="e35a4-125">However, the following types are commonly accepted by downstream filters as output from the demultiplexer.</span></span>

### <a name="mpeg-2-sections"></a><span data-ttu-id="e35a4-126">Sezioni MPEG-2</span><span class="sxs-lookup"><span data-stu-id="e35a4-126">MPEG-2 Sections</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e35a4-127">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="e35a4-127">Major Type</span></span></td>
<td><span data-ttu-id="e35a4-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span><span class="sxs-lookup"><span data-stu-id="e35a4-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e35a4-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="e35a4-129">Subtype</span></span></td>
<td><span data-ttu-id="e35a4-130">Uno dei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e35a4-130">Any of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="e35a4-131"><strong>MEDIASUBTYPE_ATSC_SI:</strong>informazioni sul servizio ATSC.</span><span class="sxs-lookup"><span data-stu-id="e35a4-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: ATSC Service Information.</span></span></li>
<li><span data-ttu-id="e35a4-132"><strong>MEDIASUBTYPE_DVB_SI:</strong>informazioni sul servizio DVB.</span><span class="sxs-lookup"><span data-stu-id="e35a4-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: DVB Service Information.</span></span></li>
<li><span data-ttu-id="e35a4-133"><strong>MEDIASUBTYPE_ISDB_SI:</strong>Informazioni sul servizio ISDB (Integrated Services Digital Broadcasting).</span><span class="sxs-lookup"><span data-stu-id="e35a4-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: Integrated Services Digital Broadcasting (ISDB) Service Information.</span></span></li>
<li><span data-ttu-id="e35a4-134"><strong>MEDIASUBTYPE_MPEG2DATA:</strong>dati della sezione MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="e35a4-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2 section data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e35a4-135">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="e35a4-135">Format Type</span></span></td>
<td><span data-ttu-id="e35a4-136">nessuno</span><span class="sxs-lookup"><span data-stu-id="e35a4-136">None</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a><span data-ttu-id="e35a4-137">MPEG-2 Video</span><span class="sxs-lookup"><span data-stu-id="e35a4-137">MPEG-2 Video</span></span>



| <span data-ttu-id="e35a4-138">Label</span><span class="sxs-lookup"><span data-stu-id="e35a4-138">Label</span></span> | <span data-ttu-id="e35a4-139">Valore</span><span class="sxs-lookup"><span data-stu-id="e35a4-139">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="e35a4-140">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="e35a4-140">Major type</span></span>       | <span data-ttu-id="e35a4-141">**MEDIATYPE \_ Video**</span><span class="sxs-lookup"><span data-stu-id="e35a4-141">**MEDIATYPE\_Video**</span></span>                     |
| <span data-ttu-id="e35a4-142">Subtype</span><span class="sxs-lookup"><span data-stu-id="e35a4-142">Subtype</span></span>          | <span data-ttu-id="e35a4-143">**MEDIASUBTYPE \_ MPEG2 \_ VIDEO**</span><span class="sxs-lookup"><span data-stu-id="e35a4-143">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           |
| <span data-ttu-id="e35a4-144">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="e35a4-144">Format Type</span></span>      | <span data-ttu-id="e35a4-145">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="e35a4-145">**FORMAT\_MPEG2Video**</span></span>                   |
| <span data-ttu-id="e35a4-146">Struttura del formato</span><span class="sxs-lookup"><span data-stu-id="e35a4-146">Format Structure</span></span> | [<span data-ttu-id="e35a4-147">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="e35a4-147">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a><span data-ttu-id="e35a4-148">MPEG-2 Audio</span><span class="sxs-lookup"><span data-stu-id="e35a4-148">MPEG-2 Audio</span></span>



| <span data-ttu-id="e35a4-149">Label</span><span class="sxs-lookup"><span data-stu-id="e35a4-149">Label</span></span> | <span data-ttu-id="e35a4-150">Valore</span><span class="sxs-lookup"><span data-stu-id="e35a4-150">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="e35a4-151">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="e35a4-151">Major type</span></span>       | <span data-ttu-id="e35a4-152">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="e35a4-152">**MEDIATYPE\_Audio**</span></span>                 |
| <span data-ttu-id="e35a4-153">Subtype</span><span class="sxs-lookup"><span data-stu-id="e35a4-153">Subtype</span></span>          | <span data-ttu-id="e35a4-154">**MEDIASUBTYPE \_ MPEG2 \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="e35a4-154">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>       |
| <span data-ttu-id="e35a4-155">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="e35a4-155">Format Type</span></span>      | <span data-ttu-id="e35a4-156">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="e35a4-156">**FORMAT\_WaveFormatEx**</span></span>             |
| <span data-ttu-id="e35a4-157">Struttura del formato</span><span class="sxs-lookup"><span data-stu-id="e35a4-157">Format Structure</span></span> | <span data-ttu-id="e35a4-158">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e35a4-158">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e35a4-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e35a4-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e35a4-160">Tipi di supporti MPEG-2</span><span class="sxs-lookup"><span data-stu-id="e35a4-160">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
