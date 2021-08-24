---
description: Deprecato. Rappresenta un istante nel tempo, in genere espresso come data e ora del giorno e un calendario corrispondente.
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: Struttura CALDATETIME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 700e11f27b673d9ff706483cc4abcf2f06cd7d8bb779ef8eaf9b51a6d81b4068
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822831"
---
# <a name="caldatetime-structure"></a>Struttura CALDATETIME

Deprecato. Rappresenta un istante nel tempo, in genere espresso come data e ora del giorno e un calendario corrispondente.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _caldatetime {
  CALID CalId;
  UINT  Era;
  UINT  Year;
  UINT  Month;
  UINT  Day;
  UINT  DayOfWeek;
  UINT  Hour;
  UINT  Minute;
  UINT  Second;
  ULONG Tick;
} CALDATETIME, *LPCALDATETIME;
```



## <a name="members"></a>Members

<dl> <dt>

**CalId**
</dt> <dd>

Identificatore [di calendario](calendar-identifiers.md) per l'istante nel tempo.

</dd> <dt>

**Era**
</dt> <dd>

Informazioni sull'era per l'istante nel tempo.

</dd> <dt>

**Year**
</dt> <dd>

Anno per l'istante nel tempo.

</dd> <dt>

**Month**
</dt> <dd>

Mese per l'istante nel tempo.

</dd> <dt>

**Day**
</dt> <dd>

Giorno per l'istante nel tempo.

</dd> <dt>

**DayOfWeek**
</dt> <dd>

Giorno della settimana per l'istante nel tempo.

</dd> <dt>

**Ora**
</dt> <dd>

Ora per l'istante nel tempo.

</dd> <dt>

**minuto**
</dt> <dd>

Minuto per l'istante nel tempo.

</dd> <dt>

**Secondo**
</dt> <dd>

Secondo per l'istante nel tempo.

</dd> <dt>

**spuntare**
</dt> <dd>

Tick per l'istante nel tempo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di supporto linguistico nazionale](national-language-support-structures.md)
</dt> </dl>

 

 




