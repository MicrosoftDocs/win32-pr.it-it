---
description: Deprecato. Rappresenta un istante di tempo, in genere espresso come data e ora del giorno e un calendario corrispondente.
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
ms.openlocfilehash: 5e3f0099a8e1dd7794b960af3d753085f2a32eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319986"
---
# <a name="caldatetime-structure"></a>Struttura CALDATETIME

Deprecato. Rappresenta un istante di tempo, in genere espresso come data e ora del giorno e un calendario corrispondente.

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

[Identificatore del calendario](calendar-identifiers.md) per l'istante di tempo.

</dd> <dt>

**Era**
</dt> <dd>

Informazioni sull'era per l'istante di tempo.

</dd> <dt>

**Anno**
</dt> <dd>

Anno per l'istante di tempo.

</dd> <dt>

**Mese**
</dt> <dd>

Mese per l'istante di tempo.

</dd> <dt>

**Day**
</dt> <dd>

Giorno per l'istante di tempo.

</dd> <dt>

**DayOfWeek**
</dt> <dd>

Il giorno della settimana per l'istante di tempo.

</dd> <dt>

**Ora**
</dt> <dd>

Ora dell'istante di tempo.

</dd> <dt>

**Minuto**
</dt> <dd>

Minuto per l'istante di tempo.

</dd> <dt>

**Secondo**
</dt> <dd>

Secondo oggetto per l'istante di tempo.

</dd> <dt>

**Tick**
</dt> <dd>

Segno di selezione per l'istante di tempo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di supporto della lingua nazionale](national-language-support-structures.md)
</dt> </dl>

 

 




