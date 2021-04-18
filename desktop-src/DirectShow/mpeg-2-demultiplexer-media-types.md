---
description: Tipi di supporti di Demultiplexer MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Tipi di supporti di Demultiplexer MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b21eecff138b987c791ecd97056fb4cf417dd98d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320694"
---
# <a name="mpeg-2-demultiplexer-media-types"></a><span data-ttu-id="d00ff-103">Tipi di supporti di Demultiplexer MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d00ff-103">MPEG-2 Demultiplexer Media Types</span></span>

<span data-ttu-id="d00ff-104">Il filtro [di MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) riconosce i seguenti tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="d00ff-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) filter recognizes the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="d00ff-105">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="d00ff-105">Input Types</span></span>

<span data-ttu-id="d00ff-106">Il tipo principale è sempre **\_ flusso MEDIATYPE**.</span><span class="sxs-lookup"><span data-stu-id="d00ff-106">The major type is always **MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="d00ff-107">Il sottotipo può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="d00ff-107">The subtype can be any of the following.</span></span>



| <span data-ttu-id="d00ff-108">GUID</span><span class="sxs-lookup"><span data-stu-id="d00ff-108">GUID</span></span>                                             | <span data-ttu-id="d00ff-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d00ff-109">Description</span></span>                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d00ff-110">**KSDATAFORMAT \_ sottotipo \_ BDA \_ \_ trasporto MPEG2**</span><span class="sxs-lookup"><span data-stu-id="d00ff-110">**KSDATAFORMAT\_SUBTYPE\_BDA\_MPEG2\_TRANSPORT**</span></span> | <span data-ttu-id="d00ff-111">Flusso di trasporto da un filtro di periferica BDA (Broadcast Driver Architecture).</span><span class="sxs-lookup"><span data-stu-id="d00ff-111">Transport stream from a Broadcast Driver Architecture (BDA) device filter.</span></span> <span data-ttu-id="d00ff-112">Il Demultiplexer MPEG-2 considera questo sottotipo in modo identico al **\_ \_ trasporto MEDIASUBTYPE MPEG2**.</span><span class="sxs-lookup"><span data-stu-id="d00ff-112">The MPEG-2 demultiplexer treats this subtype identically to **MEDIASUBTYPE\_MPEG2\_TRANSPORT**.</span></span>                                |
| <span data-ttu-id="d00ff-113">**\_Programma MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="d00ff-113">**MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>                 | <span data-ttu-id="d00ff-114">Flusso di programma</span><span class="sxs-lookup"><span data-stu-id="d00ff-114">Program stream</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="d00ff-115">**\_Trasporto MPEG2 \_ MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="d00ff-115">**MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>               | <span data-ttu-id="d00ff-116">Flusso di trasporto (TS), con pacchetti da 188 byte</span><span class="sxs-lookup"><span data-stu-id="d00ff-116">Transport stream (TS), with 188-byte packets</span></span>                                                                                                                                                              |
| <span data-ttu-id="d00ff-117">**\_ \_ Stride trasporto MPEG2 \_ MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="d00ff-117">**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**</span></span>       | <span data-ttu-id="d00ff-118">Flusso di trasporto con pacchetti "con stride".</span><span class="sxs-lookup"><span data-stu-id="d00ff-118">Transport stream with "strided" packets.</span></span> <span data-ttu-id="d00ff-119">Questo sottotipo indica che i pacchetti di Servizi terminal possono essere riempiti con byte aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="d00ff-119">This subtype indicates that the TS packets may be padded with extra bytes.</span></span> <span data-ttu-id="d00ff-120">Per ulteriori informazioni, vedere la pagina relativa allo [**\_ \_ stride del trasporto MPEG2**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="d00ff-120">For more information, see [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> |



 

<span data-ttu-id="d00ff-121">Per i pacchetti di trasporto con Stride (**MEDIASUBTYPE \_ MPEG2 \_ Transport \_ stride**), ogni esempio di supporto deve contenere un numero integrale di pacchetti di trasporto, come descritto nello [**\_ \_ stride del trasporto MPEG2**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="d00ff-121">For strided transport packets (**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**), each media sample must contain an integral number of transport packets, as described in [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> <span data-ttu-id="d00ff-122">Per tutti gli altri tipi di input, non sono previste restrizioni sui limiti di esempio; i singoli pacchetti possono estendersi sui limiti di esempio.</span><span class="sxs-lookup"><span data-stu-id="d00ff-122">For all other input types, there are no restrictions on sample boundaries; individual packets can span sample boundaries.</span></span>

### <a name="output-types"></a><span data-ttu-id="d00ff-123">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="d00ff-123">Output Types</span></span>

<span data-ttu-id="d00ff-124">Il Demultiplexer MPEG-2 non convalida i tipi di output. il filtro downstream è responsabile dell'analisi dei dati ricevuti dal Demultiplexer.</span><span class="sxs-lookup"><span data-stu-id="d00ff-124">The MPEG-2 Demultiplexer does not validate output types; the downstream filter is responsible for parsing the data it receives from the demultiplexer.</span></span> <span data-ttu-id="d00ff-125">Tuttavia, i tipi seguenti sono comunemente accettati dai filtri downstream come output del Demultiplexer.</span><span class="sxs-lookup"><span data-stu-id="d00ff-125">However, the following types are commonly accepted by downstream filters as output from the demultiplexer.</span></span>

### <a name="mpeg-2-sections"></a><span data-ttu-id="d00ff-126">Sezioni MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d00ff-126">MPEG-2 Sections</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d00ff-127">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="d00ff-127">Major Type</span></span></td>
<td><span data-ttu-id="d00ff-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span><span class="sxs-lookup"><span data-stu-id="d00ff-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d00ff-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="d00ff-129">Subtype</span></span></td>
<td><span data-ttu-id="d00ff-130">Uno dei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d00ff-130">Any of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="d00ff-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: informazioni sul servizio ATSC.</span><span class="sxs-lookup"><span data-stu-id="d00ff-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: ATSC Service Information.</span></span></li>
<li><span data-ttu-id="d00ff-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: informazioni sul servizio DVB.</span><span class="sxs-lookup"><span data-stu-id="d00ff-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: DVB Service Information.</span></span></li>
<li><span data-ttu-id="d00ff-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: informazioni sul servizio Integrated Services Digital Broadcasting (ISDB).</span><span class="sxs-lookup"><span data-stu-id="d00ff-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: Integrated Services Digital Broadcasting (ISDB) Service Information.</span></span></li>
<li><span data-ttu-id="d00ff-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: dati della sezione MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="d00ff-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2 section data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d00ff-135">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="d00ff-135">Format Type</span></span></td>
<td><span data-ttu-id="d00ff-136">nessuno</span><span class="sxs-lookup"><span data-stu-id="d00ff-136">None</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a><span data-ttu-id="d00ff-137">Video MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d00ff-137">MPEG-2 Video</span></span>



|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="d00ff-138">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="d00ff-138">Major type</span></span>       | <span data-ttu-id="d00ff-139">**Video di MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="d00ff-139">**MEDIATYPE\_Video**</span></span>                     |
| <span data-ttu-id="d00ff-140">Subtype</span><span class="sxs-lookup"><span data-stu-id="d00ff-140">Subtype</span></span>          | <span data-ttu-id="d00ff-141">**VIDEO di MEDIASUBTYPE \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="d00ff-141">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           |
| <span data-ttu-id="d00ff-142">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="d00ff-142">Format Type</span></span>      | <span data-ttu-id="d00ff-143">**FORMATO \_ mpeg2video**</span><span class="sxs-lookup"><span data-stu-id="d00ff-143">**FORMAT\_MPEG2Video**</span></span>                   |
| <span data-ttu-id="d00ff-144">Struttura Format</span><span class="sxs-lookup"><span data-stu-id="d00ff-144">Format Structure</span></span> | [<span data-ttu-id="d00ff-145">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="d00ff-145">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a><span data-ttu-id="d00ff-146">Audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d00ff-146">MPEG-2 Audio</span></span>



|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="d00ff-147">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="d00ff-147">Major type</span></span>       | <span data-ttu-id="d00ff-148">**\_Audio MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="d00ff-148">**MEDIATYPE\_Audio**</span></span>                 |
| <span data-ttu-id="d00ff-149">Subtype</span><span class="sxs-lookup"><span data-stu-id="d00ff-149">Subtype</span></span>          | <span data-ttu-id="d00ff-150">**\_Audio MPEG2 \_ MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="d00ff-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>       |
| <span data-ttu-id="d00ff-151">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="d00ff-151">Format Type</span></span>      | <span data-ttu-id="d00ff-152">**FORMATO \_ WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="d00ff-152">**FORMAT\_WaveFormatEx**</span></span>             |
| <span data-ttu-id="d00ff-153">Struttura Format</span><span class="sxs-lookup"><span data-stu-id="d00ff-153">Format Structure</span></span> | <span data-ttu-id="d00ff-154">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d00ff-154">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d00ff-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d00ff-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d00ff-156">Tipi di supporti MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d00ff-156">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
