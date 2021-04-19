---
description: La \_ struttura PERFINFO dshow \_ AUDIOBREAK contiene i dati per un evento di traccia di tipo GUID \_ AUDIOBREAK. Il filtro renderer DirectSound registra questo evento quando si verifica un'interruzioni nel flusso audio.
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: Struttura PERFINFO_DSHOW_AUDIOBREAK (Perfstruct. h)
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
ms.openlocfilehash: 599befea67b28acbedffd5c98ebce84aadf70838
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332267"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a>\_Struttura PERFINFO dshow \_ AUDIOBREAK

La `PERFINFO_DSHOW_AUDIOBREAK` struttura contiene dati per un evento di traccia di tipo GUID \_ AUDIOBREAK.

Il filtro [renderer DirectSound](directsound-renderer-filter.md) registra questo evento quando si verifica un'interruzioni nel flusso audio.

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

Numero di cicli di clock più recenti (istruzione RDTSC).

</dd> <dt>

**dshowClock**
</dt> <dd>

Posizione di scrittura corrente nel buffer DirectSound.

</dd> <dt>

**sampleTime**
</dt> <dd>

Inizio dell'interruzioni audio nel buffer DirectSound.

</dd> <dt>

**sampleDuration**
</dt> <dd>

Durata dell'intervallo, in millisecondi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per abilitare questo evento, è necessario impostare il \_ flag di bit AUDIOBREAK nel parametro *EnableFlag* quando si chiama **EnableTrace**. Questo flag è definito nel file di intestazione Dxmperf. h, incluso nelle classi base di DirectShow.

Per registrare questo evento da un filtro DirectShow, usare la **macro \_ AUDIOBREAK di PERFLOG** , definita in Dxmperf. h.

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

 

 




