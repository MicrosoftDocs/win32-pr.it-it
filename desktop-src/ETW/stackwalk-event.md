---
description: Questa classe è la classe del tipo di evento per gli eventi di analisi dello stack.
ms.assetid: 05117bd6-a39c-42f3-8aed-c6f758f946c6
title: StackWalk_Event classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk_Event
- StackWalk_Event.EventTimeStamp
- StackWalk_Event.StackProcess
- StackWalk_Event.StackThread
- StackWalk_Event.Stack1
- StackWalk_Event.Stack192
api_type:
- NA
api_location: ''
ms.openlocfilehash: 672d8fc609c14a43ca2692b5cf8a46356a00cccb9c06371e515bc102706c3638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069701"
---
# <a name="stackwalk_event-class"></a>Classe di evento StackWalk \_

Questa classe è la classe del tipo di evento per gli eventi di analisi dello stack.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{32}, EventTypeName{"Stack"}]
class StackWalk_Event : StackWalk
{
  uint64 EventTimeStamp;
  uint32 StackProcess;
  uint32 StackThread;
  uint32 Stack1;
  uint32 Stack192;
};
```

## <a name="members"></a>Members

La **classe di \_ evento StackWalk** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe di \_ evento StackWalk** ha queste proprietà.

<dl> <dt>

**EventTimeStamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1)
</dt> </dl>

Timestamp dell'evento originale dall'intestazione dell'evento. Usare questo timestamp per associare lo stack a un evento.

</dd> <dt>

**Stack1**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4), puntatore
</dt> </dl>

Indirizzo della chiamata.

</dd> <dt>

**Stack192**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(195), puntatore
</dt> </dl>

Indirizzo della chiamata.

</dd> <dt>

**StackProcess**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), format("x")
</dt> </dl>

Identificatore del processo dell'evento originale.

</dd> <dt>

**StackThread**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3)
</dt> </dl>

Identificatore del thread dell'evento originale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che la classe non mostra tutte le **proprietà Stack*n*** esistenti tra **Stack1** e **Stack192.** Usare le dimensioni dell'evento per determinare il numero **di proprietà Stack*n*** che contengono indirizzi validi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



 

 




