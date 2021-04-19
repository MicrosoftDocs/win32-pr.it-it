---
description: La \_ struttura PERFINFO dshow \_ AVREND contiene i dati per un evento di traccia di tipo GUID \_ VIDEOREND. VMR registra questo evento immediatamente prima di eseguire il rendering di un frame.
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: Struttura PERFINFO_DSHOW_AVREND (Perfstruct. h)
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
ms.openlocfilehash: ee2d944d086f9c1a4ea7944f023321dfbc06d547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332263"
---
# <a name="perfinfo_dshow_avrend-structure"></a>\_Struttura PERFINFO dshow \_ AVREND

La `PERFINFO_DSHOW_AVREND` struttura contiene dati per un evento di traccia di tipo GUID \_ VIDEOREND.

VMR registra questo evento immediatamente prima di eseguire il rendering di un frame.

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

Numero di cicli di clock più recenti (istruzione RDTSC).

</dd> <dt>

**dshowClock**
</dt> <dd>

Ora di riferimento corrente, restituita dal metodo [**IReferenceClock:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .

</dd> <dt>

**sampleTime**
</dt> <dd>

Ora di inizio dell'esempio.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per abilitare questo evento, è necessario impostare il \_ flag DXMPERF VIDEOREND nel parametro *EnableFlag* quando si chiama **EnableTrace**. Questo flag è definito nel file di intestazione Dxmperf. h, incluso nelle classi base di DirectShow.

Per registrare questo evento da un filtro DirectShow, usare la **macro \_ VIDEOREND di PERFLOG** , definita in Dxmperf. h.

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

 

 




