---
description: Questa classe è la classe del tipo di evento per gli eventi di avvio del thread. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 412de56f-4f54-46e8-ab60-d47371247e79
title: Classe Thread_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup1
- Thread_V1_TypeGroup1.ProcessId
- Thread_V1_TypeGroup1.TThreadId
- Thread_V1_TypeGroup1.StackBase
- Thread_V1_TypeGroup1.StackLimit
- Thread_V1_TypeGroup1.UserStackBase
- Thread_V1_TypeGroup1.UserStackLimit
- Thread_V1_TypeGroup1.StartAddr
- Thread_V1_TypeGroup1.Win32StartAddr
- Thread_V1_TypeGroup1.WaitMode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 13c419b417b614eb9022d1cb7c09a84ca705b3dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967741"
---
# <a name="thread_v1_typegroup1-class"></a>\_Classe thread V1 \_ TypeGroup1

Questa classe è la classe del tipo di evento per gli eventi di avvio del thread.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{1, 3}, EventTypeName{"Start", "DCStart"}]
class Thread_V1_TypeGroup1 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  sint8  WaitMode;
};
```

## <a name="members"></a>Members

I tipi di membri della classe **thread \_ V1 \_ TypeGroup1** sono i seguenti:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **thread \_ V1 \_ TypeGroup1** dispone di queste proprietà.

<dl> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1)
</dt> </dl>

Identificatore del processo del thread che interessano l'evento.

**Windows Server 2003:** Contiene il qualificatore di formato ("x").

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

TThreadId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2)
</dt> </dl>

Identificatore del thread associato all'evento.

**Windows Server 2003:** Contiene il qualificatore di formato ("x").

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

WaitMode
</dt> <dd> <dl> <dt>

Tipo di dati: **sint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (9), Format ("c")
</dt> </dl>

Non usato.

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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Thread \_ V1**](thread-v1.md)
</dt> </dl>

 

 




