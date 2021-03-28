---
description: Questa classe è la classe del tipo di evento per gli eventi di inizio e di fine del thread. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Classe Thread_V2_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2_TypeGroup1
- Thread_V2_TypeGroup1.ProcessId
- Thread_V2_TypeGroup1.TThreadId
- Thread_V2_TypeGroup1.StackBase
- Thread_V2_TypeGroup1.StackLimit
- Thread_V2_TypeGroup1.UserStackBase
- Thread_V2_TypeGroup1.UserStackLimit
- Thread_V2_TypeGroup1.StartAddr
- Thread_V2_TypeGroup1.Win32StartAddr
- Thread_V2_TypeGroup1.TebBase
- Thread_V2_TypeGroup1.SubProcessTag
api_type:
- NA
api_location: ''
ms.openlocfilehash: c89d573f4eda2580002bedfd0ad17eb9b50c1575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232086"
---
# <a name="thread_v2_typegroup1-class"></a>\_Classe thread v2 \_ TypeGroup1

Questa classe è la classe del tipo di evento per gli eventi di inizio e di fine del thread.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V2_TypeGroup1 : Thread_V2
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
};
```

## <a name="members"></a>Members

La classe **thread \_ v2 \_ TypeGroup1** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **thread \_ v2 \_ TypeGroup1** dispone di queste proprietà.

<dl> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), Format ("x")
</dt> </dl>

Identificatore del processo del thread che interessano l'evento.

</dd> <dt>

StackBase
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3), puntatore
</dt> </dl>

Indirizzo di base dello stack del thread.

</dd> <dt>

StackLimit
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4), puntatore
</dt> </dl>

Limite dello stack del thread.

</dd> <dt>

StartAddr
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (7), puntatore
</dt> </dl>

Indirizzo di memoria in cui viene avviata la traccia.

</dd> <dt>

SubProcessTag
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (10), Format ("x")
</dt> </dl>

Identifica il servizio se il thread è di proprietà di un servizio. in caso contrario, zero.

</dd> <dt>

TebBase
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (9), puntatore
</dt> </dl>

Indirizzo di base blocco ambiente thread.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), Format ("x")
</dt> </dl>

Identificatore del thread associato all'evento.

</dd> <dt>

UserStackBase
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (5), puntatore
</dt> </dl>

Indirizzo di base dello stack in modalità utente del thread.

</dd> <dt>

UserStackLimit
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (6), puntatore
</dt> </dl>

Limite dello stack in modalità utente del thread.

</dd> <dt>

Win32StartAddr
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (8), puntatore
</dt> </dl>

Indirizzo iniziale della funzione che deve essere eseguita da questo thread.

</dd> </dl>

## <a name="remarks"></a>Commenti

I tipi di evento DCStart e DCEnd enumerano i thread attualmente in esecuzione nel momento in cui la sessione kernel inizia e termina, rispettivamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Thread**](thread.md)
</dt> <dt>

[**Thread \_ v2**](thread-v2.md)
</dt> </dl>

 

 




