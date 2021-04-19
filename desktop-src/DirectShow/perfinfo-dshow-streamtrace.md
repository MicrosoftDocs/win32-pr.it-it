---
description: La \_ struttura PERFINFO dshow \_ STREAMTRACE contiene i dati per un evento di traccia DirectShow di tipo GUID \_ STREAMTRACE.
ms.assetid: 41fbf95c-e86c-4c64-898f-01fbf5f8839c
title: Struttura PERFINFO_DSHOW_STREAMTRACE (Perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_STREAMTRACE
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 2bee4f3c11cf8462c8292cc412a6da5d9f9bfa78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325914"
---
# <a name="perfinfo_dshow_streamtrace-structure"></a><span data-ttu-id="0edc8-103">\_Struttura PERFINFO dshow \_ STREAMTRACE</span><span class="sxs-lookup"><span data-stu-id="0edc8-103">PERFINFO\_DSHOW\_STREAMTRACE structure</span></span>

<span data-ttu-id="0edc8-104">La `PERFINFO_DSHOW_STREAMTRACE` struttura contiene dati per un evento di traccia DirectShow di tipo GUID \_ STREAMTRACE.</span><span class="sxs-lookup"><span data-stu-id="0edc8-104">The `PERFINFO_DSHOW_STREAMTRACE` structure contains data for a DirectShow trace event of type GUID\_STREAMTRACE.</span></span>

## <a name="syntax"></a><span data-ttu-id="0edc8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0edc8-105">Syntax</span></span>


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a><span data-ttu-id="0edc8-106">Members</span><span class="sxs-lookup"><span data-stu-id="0edc8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0edc8-107">**id**</span><span class="sxs-lookup"><span data-stu-id="0edc8-107">**id**</span></span>
</dt> <dd>

<span data-ttu-id="0edc8-108">Identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0edc8-108">Event identifier.</span></span> <span data-ttu-id="0edc8-109">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="0edc8-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0edc8-110">**riservati**</span><span class="sxs-lookup"><span data-stu-id="0edc8-110">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="0edc8-111">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0edc8-111">Reserved.</span></span> <span data-ttu-id="0edc8-112">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="0edc8-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="0edc8-113">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="0edc8-113">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="0edc8-114">Tempo di flusso per questo evento, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="0edc8-114">Stream time for this event, in 100-nanosecond units.</span></span> <span data-ttu-id="0edc8-115">Questo valore è facoltativo e può essere zero.</span><span class="sxs-lookup"><span data-stu-id="0edc8-115">This value is optional and can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0edc8-116">**data**</span><span class="sxs-lookup"><span data-stu-id="0edc8-116">**data**</span></span>
</dt> <dd>

<span data-ttu-id="0edc8-117">Dati di evento facoltativi costituiti da quattro valori **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="0edc8-117">Optional event data consisting of four **ULONGLONG** values.</span></span> <span data-ttu-id="0edc8-118">Il significato di questi dati dipende dall'identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0edc8-118">The meaning of this data depends on the event identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0edc8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="0edc8-119">Remarks</span></span>

<span data-ttu-id="0edc8-120">Sono definiti i seguenti identificatori di evento.</span><span class="sxs-lookup"><span data-stu-id="0edc8-120">The following event identifiers are defined.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0edc8-121">Identificatore evento</span><span class="sxs-lookup"><span data-stu-id="0edc8-121">Event identifier</span></span></th>
<th><span data-ttu-id="0edc8-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0edc8-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0edc8-123">PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</span><span class="sxs-lookup"><span data-stu-id="0edc8-123">PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</span></span></td>
<td><span data-ttu-id="0edc8-124">Registrato quando il filtro del <a href="mpeg-2-demultiplexer.md">Demultiplexer MPEG-2</a> converte un timestamp di presentazione (PTS) in flusso temporale.</span><span class="sxs-lookup"><span data-stu-id="0edc8-124">Logged when the <a href="mpeg-2-demultiplexer.md">MPEG-2 Demultiplexer</a> filter converts a presentation time stamp (PTS) to stream time.</span></span>
<ul>
<li><span data-ttu-id="0edc8-125"><strong>dati</strong>[0]: Converted start time.</span><span class="sxs-lookup"><span data-stu-id="0edc8-125"><strong>data</strong>[0]: Converted start time.</span></span></li>
<li><span data-ttu-id="0edc8-126"><strong>dati</strong>[1]: Converted stop time.</span><span class="sxs-lookup"><span data-stu-id="0edc8-126"><strong>data</strong>[1]: Converted stop time.</span></span></li>
<li><span data-ttu-id="0edc8-127"><strong>dati</strong>[2].</span><span class="sxs-lookup"><span data-stu-id="0edc8-127"><strong>data</strong>[2].</span></span> <span data-ttu-id="0edc8-128">Identificatore di flusso per il pin di input.</span><span class="sxs-lookup"><span data-stu-id="0edc8-128">Stream identifier for the input pin.</span></span></li>
<li><span data-ttu-id="0edc8-129"><strong>dati</strong>[3]: PTS that was converted.</span><span class="sxs-lookup"><span data-stu-id="0edc8-129"><strong>data</strong>[3]: PTS that was converted.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0edc8-130">PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</span><span class="sxs-lookup"><span data-stu-id="0edc8-130">PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</span></span></td>
<td><span data-ttu-id="0edc8-131">Registrato quando il Demultiplexer MPEG-2 riceve un campione.</span><span class="sxs-lookup"><span data-stu-id="0edc8-131">Logged when MPEG-2 Demultiplexer receives a sample.</span></span>
<ul>
<li><span data-ttu-id="0edc8-132"><strong>dati</strong> [0]: Current time returned by  di <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0edc8-132"><strong>data</strong>[0]: Current time returned by <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0edc8-133">PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</span><span class="sxs-lookup"><span data-stu-id="0edc8-133">PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</span></span></td>
<td><span data-ttu-id="0edc8-134">Registrato quando VMR pianifica un esempio per il rendering, immediatamente prima che VMR chiami <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock:: AdviseTime</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0edc8-134">Logged when the VMR schedules a sample for rendering, immediately before the VMR calls <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock::AdviseTime</strong></a>.</span></span>
<ul>
<li><span data-ttu-id="0edc8-135"><strong>dati</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</span><span class="sxs-lookup"><span data-stu-id="0edc8-135"><strong>data</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0edc8-136">PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</span><span class="sxs-lookup"><span data-stu-id="0edc8-136">PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</span></span></td>
<td><span data-ttu-id="0edc8-137">Registrato quando VMR avvia un'operazione di decodifica, ovvero quando il decodificatore chiama <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator:: BeginFrame</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0edc8-137">Logged when the VMR begins a decoding operation—that is, when the decoder calls <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator::BeginFrame</strong></a>.</span></span> <span data-ttu-id="0edc8-138">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0edc8-138">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0edc8-139">PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</span><span class="sxs-lookup"><span data-stu-id="0edc8-139">PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</span></span></td>
<td><span data-ttu-id="0edc8-140">Registrato quando VMR avvia un'operazione di deinterlacciamento o di composizione video.</span><span class="sxs-lookup"><span data-stu-id="0edc8-140">Logged when the VMR begins a deinterlacing or video compositing operation.</span></span> <span data-ttu-id="0edc8-141">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0edc8-141">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0edc8-142">PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</span><span class="sxs-lookup"><span data-stu-id="0edc8-142">PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</span></span></td>
<td><span data-ttu-id="0edc8-143">Registrato quando il VMR Elimina un frame; Se ad esempio un campione è in ritardo.</span><span class="sxs-lookup"><span data-stu-id="0edc8-143">Logged when the VMR drops a frame; for example, if a sample was late.</span></span>
<ul>
<li><span data-ttu-id="0edc8-144"><strong>dati</strong>[0]: Sample start time.</span><span class="sxs-lookup"><span data-stu-id="0edc8-144"><strong>data</strong>[0]: Sample start time.</span></span></li>
<li><span data-ttu-id="0edc8-145"><strong>dati</strong>[1]: Sample end time.</span><span class="sxs-lookup"><span data-stu-id="0edc8-145"><strong>data</strong>[1]: Sample end time.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0edc8-146">PERFINFO_STREAMTRACE_VMR_END_ADVISE</span><span class="sxs-lookup"><span data-stu-id="0edc8-146">PERFINFO_STREAMTRACE_VMR_END_ADVISE</span></span></td>
<td><span data-ttu-id="0edc8-147">Registrato quando VMR riceve una notifica di avviso dall'orologio di riferimento.</span><span class="sxs-lookup"><span data-stu-id="0edc8-147">Logged when the VMR receives an advise notification from the reference clock.</span></span> <span data-ttu-id="0edc8-148">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0edc8-148">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0edc8-149">PERFINFO_STREAMTRACE_VMR_END_DECODE</span><span class="sxs-lookup"><span data-stu-id="0edc8-149">PERFINFO_STREAMTRACE_VMR_END_DECODE</span></span></td>
<td><span data-ttu-id="0edc8-150">Registrato quando VMR termina un'operazione di decodifica, ovvero quando il decodificatore chiama <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator:: EndFrame</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0edc8-150">Logged when the VMR ends a decoding operation—that is, when the decoder calls <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator::EndFrame</strong></a>.</span></span> <span data-ttu-id="0edc8-151">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0edc8-151">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0edc8-152">PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</span><span class="sxs-lookup"><span data-stu-id="0edc8-152">PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</span></span></td>
<td><span data-ttu-id="0edc8-153">Registrato quando VMR completa un'operazione di deinterlacciamento o composizione video.</span><span class="sxs-lookup"><span data-stu-id="0edc8-153">Logged when the VMR completes a deinterlacing or video compositing operation.</span></span> <span data-ttu-id="0edc8-154">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0edc8-154">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0edc8-155">PERFINFO_STREAMTRACE_VMR_RECEIVE</span><span class="sxs-lookup"><span data-stu-id="0edc8-155">PERFINFO_STREAMTRACE_VMR_RECEIVE</span></span></td>
<td><span data-ttu-id="0edc8-156">Registrato quando VMR riceve un nuovo campione.</span><span class="sxs-lookup"><span data-stu-id="0edc8-156">Logged when the VMR receives a new sample.</span></span> <span data-ttu-id="0edc8-157">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0edc8-157">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0edc8-158">PERFINFO_STREAMTRACE_VMR_RENDER_TIME</span><span class="sxs-lookup"><span data-stu-id="0edc8-158">PERFINFO_STREAMTRACE_VMR_RENDER_TIME</span></span></td>
<td><span data-ttu-id="0edc8-159">Registrato quando il VMR completa il rendering di un frame.</span><span class="sxs-lookup"><span data-stu-id="0edc8-159">Logged when the VMR finishes rendering a frame.</span></span>
<ul>
<li><span data-ttu-id="0edc8-160"><strong>dati</strong>[0]: Time that it took to render this frame.</span><span class="sxs-lookup"><span data-stu-id="0edc8-160"><strong>data</strong>[0]: Time that it took to render this frame.</span></span></li>
<li><span data-ttu-id="0edc8-161"><strong>dati</strong>[1]: Running average of frame rendering times.</span><span class="sxs-lookup"><span data-stu-id="0edc8-161"><strong>data</strong>[1]: Running average of frame rendering times.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0edc8-162">Per registrare questo evento da un filtro DirectShow, usare la funzione **PERFLOG \_ STREAMTRACE** , definita nel file di intestazione Dxmperf. h.</span><span class="sxs-lookup"><span data-stu-id="0edc8-162">To log this event from a DirectShow filter, use the **PERFLOG\_STREAMTRACE** function, which is defined in the header file Dxmperf.h.</span></span> <span data-ttu-id="0edc8-163">Questa intestazione è inclusa nelle classi base di DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0edc8-163">This header is included in the DirectShow base classes.</span></span>

## <a name="requirements"></a><span data-ttu-id="0edc8-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0edc8-164">Requirements</span></span>



| <span data-ttu-id="0edc8-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="0edc8-165">Requirement</span></span> | <span data-ttu-id="0edc8-166">Valore</span><span class="sxs-lookup"><span data-stu-id="0edc8-166">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0edc8-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0edc8-167">Header</span></span><br/> | <dl> <span data-ttu-id="0edc8-168"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-168"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0edc8-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0edc8-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0edc8-170">Strutture DirectShow</span><span class="sxs-lookup"><span data-stu-id="0edc8-170">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="0edc8-171">Traccia eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="0edc8-171">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="0edc8-172">GUID dell'evento di traccia</span><span class="sxs-lookup"><span data-stu-id="0edc8-172">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 
