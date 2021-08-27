---
description: La struttura PERFINFO DSHOW AVREND contiene i dati per un evento \_ di traccia di tipo GUID \_ \_ VIDEOREND. La macchina virtuale registra questo evento immediatamente prima di eseguire il rendering di un frame.
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: PERFINFO_DSHOW_AVREND struttura (Perfstruct.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AVREND
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 49cc76f4db1a5fae76678ee2d81f3e2fff0a6c5ca3d5c5532adebaec23f48215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050711"
---
# <a name="perfinfo_dshow_avrend-structure"></a>Struttura PERFINFO \_ DSHOW \_ AVREND

La `PERFINFO_DSHOW_AVREND` struttura contiene dati per un evento di traccia di tipo \_ VIDEOREND.

La macchina virtuale registra questo evento immediatamente prima di eseguire il rendering di un frame.

## <a name="syntax"></a>Sintassi


```C++
typedef struct PERFINFO_DSHOW_AVREND {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
} PERFINFO_DSHOW_AVREND, *PPERFINFO_DSHOW_AVREND;
```



## <a name="members"></a>Members

<dl> <dt>

**cycleCounter**
</dt> <dd>

Conteggio del ciclo di clock più recente (istruzione RDTSC).

</dd> <dt>

**dshowClock**
</dt> <dd>

Ora di riferimento corrente, come restituito dal [**metodo IReferenceClock::GetTime.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime)

</dd> <dt>

**sampleTime**
</dt> <dd>

Ora di inizio dell'esempio.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per abilitare questo evento, è necessario impostare il flag DXMPERF \_ VIDEOREND nel *parametro EnableFlag* quando si chiama **EnableTrace**. Questo flag è definito nel file di intestazione Dxmperf.h, incluso nelle classi DirectShow di base.

Per registrare questo evento da DirectShow filtro, usare la macro **PERFLOG \_ VIDEOREND,** definita in Dxmperf.h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Perfstruct.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Strutture](directshow-structures.md)
</dt> <dt>

[Traccia eventi in DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[GUID degli eventi di traccia](trace-guids.md)
</dt> </dl>

 

 




