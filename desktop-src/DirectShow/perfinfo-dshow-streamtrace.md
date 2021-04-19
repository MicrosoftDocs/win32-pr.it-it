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
# <a name="perfinfo_dshow_streamtrace-structure"></a>\_Struttura PERFINFO dshow \_ STREAMTRACE

La `PERFINFO_DSHOW_STREAMTRACE` struttura contiene dati per un evento di traccia DirectShow di tipo GUID \_ STREAMTRACE.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a>Members

<dl> <dt>

**id**
</dt> <dd>

Identificatore dell'evento. Vedere la sezione Osservazioni.

</dd> <dt>

**riservati**
</dt> <dd>

Riservato. Imposta su zero.

</dd> <dt>

**dshowClock**
</dt> <dd>

Tempo di flusso per questo evento, in unità di 100 nanosecondi. Questo valore è facoltativo e può essere zero.

</dd> <dt>

**data**
</dt> <dd>

Dati di evento facoltativi costituiti da quattro valori **ULONGLONG** . Il significato di questi dati dipende dall'identificatore dell'evento.

</dd> </dl>

## <a name="remarks"></a>Commenti

Sono definiti i seguenti identificatori di evento.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Identificatore evento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</td>
<td>Registrato quando il filtro del <a href="mpeg-2-demultiplexer.md">Demultiplexer MPEG-2</a> converte un timestamp di presentazione (PTS) in flusso temporale.
<ul>
<li><strong>dati</strong>[0]: Converted start time.</li>
<li><strong>dati</strong>[1]: Converted stop time.</li>
<li><strong>dati</strong>[2]. Identificatore di flusso per il pin di input.</li>
<li><strong>dati</strong>[3]: PTS that was converted.</li>
</ul></td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</td>
<td>Registrato quando il Demultiplexer MPEG-2 riceve un campione.
<ul>
<li><strong>dati</strong> [0]: Current time returned by  di <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</td>
<td>Registrato quando VMR pianifica un esempio per il rendering, immediatamente prima che VMR chiami <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock:: AdviseTime</strong></a>.
<ul>
<li><strong>dati</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</li>
</ul></td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</td>
<td>Registrato quando VMR avvia un'operazione di decodifica, ovvero quando il decodificatore chiama <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator:: BeginFrame</strong></a>. Nessun dato dell'evento.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</td>
<td>Registrato quando VMR avvia un'operazione di deinterlacciamento o di composizione video. Nessun dato dell'evento.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</td>
<td>Registrato quando il VMR Elimina un frame; Se ad esempio un campione è in ritardo.
<ul>
<li><strong>dati</strong>[0]: Sample start time.</li>
<li><strong>dati</strong>[1]: Sample end time.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_END_ADVISE</td>
<td>Registrato quando VMR riceve una notifica di avviso dall'orologio di riferimento. Nessun dato dell'evento.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_END_DECODE</td>
<td>Registrato quando VMR termina un'operazione di decodifica, ovvero quando il decodificatore chiama <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator:: EndFrame</strong></a>. Nessun dato dell'evento.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</td>
<td>Registrato quando VMR completa un'operazione di deinterlacciamento o composizione video. Nessun dato dell'evento.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_RECEIVE</td>
<td>Registrato quando VMR riceve un nuovo campione. Nessun dato dell'evento.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_RENDER_TIME</td>
<td>Registrato quando il VMR completa il rendering di un frame.
<ul>
<li><strong>dati</strong>[0]: Time that it took to render this frame.</li>
<li><strong>dati</strong>[1]: Running average of frame rendering times.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Per registrare questo evento da un filtro DirectShow, usare la funzione **PERFLOG \_ STREAMTRACE** , definita nel file di intestazione Dxmperf. h. Questa intestazione è inclusa nelle classi base di DirectShow.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Perfstruct. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture DirectShow](directshow-structures.md)
</dt> <dt>

[Traccia eventi in DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[GUID dell'evento di traccia](trace-guids.md)
</dt> </dl>

 

 
