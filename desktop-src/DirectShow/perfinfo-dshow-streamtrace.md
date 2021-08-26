---
description: La struttura PERFINFO DSHOW STREAMTRACE contiene i dati per un evento \_ DirectShow di traccia di tipo GUID \_ \_ STREAMTRACE.
ms.assetid: 41fbf95c-e86c-4c64-898f-01fbf5f8839c
title: PERFINFO_DSHOW_STREAMTRACE struttura (Perfstruct.h)
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
ms.openlocfilehash: e17d013d90b133f9c6819b8d9ddf4b5970582cae
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477006"
---
# <a name="perfinfo_dshow_streamtrace-structure"></a>Struttura PERFINFO \_ DSHOW \_ STREAMTRACE

La `PERFINFO_DSHOW_STREAMTRACE` struttura contiene dati per un evento DirectShow di traccia di tipo GUID \_ STREAMTRACE.

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

**Riservati**
</dt> <dd>

Riservato. Imposta su zero.

</dd> <dt>

**dshowClock**
</dt> <dd>

Tempo di streaming per questo evento, in unità di 100 nanosecondi. Questo valore è facoltativo e può essere zero.

</dd> <dt>

**data**
</dt> <dd>

Dati di evento facoltativi costituiti da **quattro valori ULONGLONG.** Il significato di questi dati dipende dall'identificatore dell'evento.

</dd> </dl>

## <a name="remarks"></a>Commenti

Vengono definiti gli identificatori di evento seguenti.




| Identificatore evento | Descrizione | 
|------------------|-------------|
| PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION | Registrato quando il <a href="mpeg-2-demultiplexer.md">filtro MPEG-2 Demultiplexer</a> converte un timestamp di presentazione (PTS) in ora di flusso.<ul><li><strong>data</strong>[0]: ora di inizio convertita.</li><li><strong>data</strong>[1]: ora di arresto convertita.</li><li><strong>data</strong>[2]. Identificatore del flusso per il pin di input.</li><li><strong>data</strong>[3]: PTS convertito.</li></ul> | 
| PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE | Registrato quando MPEG-2 Demultiplexer riceve un esempio.<ul><li><strong>data</strong>[0]: ora corrente restituita da <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE | Registrato quando la macchina virtuale pianifica un esempio per il rendering, immediatamente prima che la macchina virtuale <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>chiami IReferenceClock::AdviseTime</strong></a>.<ul><li><strong>data</strong>[0]: ora di riferimento dell'inizio del flusso, che corrisponde all'ora del flusso zero.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE | Registrato quando il vmr inizia un'operazione di decodifica, ovvero quando il decodificatore chiama <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator::BeginFrame</strong></a>. Nessun dato dell'evento. | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE | Registrato quando il vmr inizia un'operazione di dinterlacing o composizione video. Nessun dato dell'evento. | 
| PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME | Registrato quando la macchina virtuale elimina un frame; ad esempio se un campione è in ritardo.<ul><li><strong>data</strong>[0]: ora di inizio di esempio.</li><li><strong>data</strong>[1]: ora di fine del campione.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_END_ADVISE | Registrato quando il vmr riceve una notifica di avviso dall'orologio di riferimento. Nessun dato dell'evento. | 
| PERFINFO_STREAMTRACE_VMR_END_DECODE | Registrato quando la macchina virtuale termina un'operazione di decodifica, ovvero quando il decodificatore chiama <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator::EndFrame</strong></a>. Nessun dato dell'evento. | 
| PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE | Registrato quando la macchina virtuale completa un'operazione di composizione video o di dinterlacciamento. Nessun dato dell'evento. | 
| PERFINFO_STREAMTRACE_VMR_RECEIVE | Registrato quando la macchina virtuale riceve un nuovo esempio. Nessun dato dell'evento. | 
| PERFINFO_STREAMTRACE_VMR_RENDER_TIME | Registrato al termine del rendering di un frame da parte della macchina virtuale.<ul><li><strong>data</strong>[0]: tempo impiegato per il rendering di questo frame.</li><li><strong>data</strong>[1]: media dei tempi di rendering dei fotogrammi in esecuzione.</li></ul> | 




 

Per registrare questo evento da un filtro DirectShow, usare la funzione **\_ PERFLOG STREAMTRACE,** definita nel file di intestazione Dxmperf.h. Questa intestazione è inclusa nelle classi DirectShow base.

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Perfstruct.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Strutture](directshow-structures.md)
</dt> <dt>

[Event Tracing in DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[GUID degli eventi di traccia](trace-guids.md)
</dt> </dl>

 

 
