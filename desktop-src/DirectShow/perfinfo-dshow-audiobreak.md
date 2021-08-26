---
description: La struttura PERFINFO DSHOW AUDIOBREAK contiene i dati per \_ un evento di traccia di tipo GUID \_ \_ AUDIOBREAK. Il filtro del renderer DirectSound registra questo evento quando si verifica un'interruzione nel flusso audio.
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: PERFINFO_DSHOW_AUDIOBREAK struttura (Perfstruct.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AUDIOBREAK
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: c7b8f83fffaa718c27e0333d864a564282228c0943f4d77fb653dc1800a6ddd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928191"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a>Struttura PERFINFO \_ DSHOW \_ AUDIOBREAK

La `PERFINFO_DSHOW_AUDIOBREAK` struttura contiene dati per un evento di traccia di tipo \_ AUDIOBREAK GUID.

Il [filtro del renderer DirectSound](directsound-renderer-filter.md) registra questo evento quando si verifica un'interruzione nel flusso audio.

## <a name="syntax"></a>Sintassi


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a>Members

<dl> <dt>

**cycleCounter**
</dt> <dd>

Conteggio del ciclo di clock più recente (istruzione RDTSC).

</dd> <dt>

**dshowClock**
</dt> <dd>

Posizione di scrittura corrente nel buffer DirectSound.

</dd> <dt>

**sampleTime**
</dt> <dd>

Inizio dell'interruzione audio nel buffer DirectSound.

</dd> <dt>

**sampleDuration**
</dt> <dd>

Durata dell'interruzione, in millisecondi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per abilitare questo evento, è necessario impostare il flag AUDIOBREAK \_ BIT nel *parametro EnableFlag* quando si chiama **EnableTrace**. Questo flag è definito nel file di intestazione Dxmperf.h, incluso nelle classi DirectShow base.

Per registrare questo evento da DirectShow filtro, usare la macro **PERFLOG \_ AUDIOBREAK,** definita in Dxmperf.h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
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

 

 




