---
description: Questa classe è la classe del tipo di evento per gli eventi di traccia dello stack.
ms.assetid: 05117bd6-a39c-42f3-8aed-c6f758f946c6
title: Classe StackWalk_Event
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
ms.openlocfilehash: 746a7f2a9b5f6bb6316bf0d0e20e5645cea15a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980082"
---
# <a name="stackwalk_event-class"></a>\_Classe di evento StackWalk

Questa classe è la classe del tipo di evento per gli eventi di traccia dello stack.

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

La classe di **\_ evento StackWalk** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe di **\_ evento StackWalk** dispone di queste proprietà.

<dl> <dt>

**EventTimeStamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1)
</dt> </dl>

Timestamp dell'evento originale dall'intestazione dell'evento. Utilizzare questo timestamp per associare lo stack a un evento.

</dd> <dt>

**Stack1**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4), puntatore
</dt> </dl>

Indirizzo della chiamata.

</dd> <dt>

**Stack192**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (195), puntatore
</dt> </dl>

Indirizzo della chiamata.

</dd> <dt>

**StackProcess**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), Format ("x")
</dt> </dl>

Identificatore del processo dell'evento originale.

</dd> <dt>

**StackThread**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3)
</dt> </dl>

Identificatore del thread dell'evento originale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che la classe non Mostra tutte le proprietà **stack * n*** presenti tra **Stack1** e **Stack192**. Usare le dimensioni dell'evento per determinare il numero di proprietà *** n * dello stack** che contengono indirizzi validi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



 

 




