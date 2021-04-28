---
description: 'Thread_V2_TypeGroup1: questa classe è la classe del tipo di evento per gli eventi di inizio e fine del thread. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Thread_V2_TypeGroup1 classe
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
ms.openlocfilehash: 24ac4655fc374c40eb530828229a319f9ee1375e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105659"
---
# <a name="thread_v2_typegroup1-class"></a>Classe \_ \_ TypeGroup1 thread V2

Questa classe è la classe del tipo di evento per gli eventi di inizio e fine del thread.

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

La **classe \_ \_ TypeGroup1 thread V2** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ TypeGroup1 thread V2** ha queste proprietà.

<dl> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Format("x")
</dt> </dl>

Identificatore del processo del thread coinvolto nell'evento.

</dd> <dt>

StackBase
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3), Pointer
</dt> </dl>

Indirizzo di base dello stack del thread.

</dd> <dt>

StackLimit
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4), Pointer
</dt> </dl>

Limite dello stack del thread.

</dd> <dt>

StartAddr
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(7), Puntatore
</dt> </dl>

Indirizzo di memoria in corrispondenza del quale viene avviata la traccia.

</dd> <dt>

SubProcessTag
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(10), Format("x")
</dt> </dl>

Identifica il servizio se il thread è di proprietà di un servizio; in caso contrario, zero.

</dd> <dt>

TebBase
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(9), Puntatore
</dt> </dl>

Indirizzo di base del blocco dell'ambiente thread.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), Format("x")
</dt> </dl>

Identificatore di thread del thread coinvolto nell'evento.

</dd> <dt>

UserStackBase
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(5), Puntatore
</dt> </dl>

Indirizzo di base dello stack in modalità utente del thread.

</dd> <dt>

UserStackLimit
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(6), Pointer
</dt> </dl>

Limite dello stack in modalità utente del thread.

</dd> <dt>

Win32StartAddr
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(8), Pointer
</dt> </dl>

Indirizzo iniziale della funzione che deve essere eseguita da questo thread.

</dd> </dl>

## <a name="remarks"></a>Commenti

I tipi di evento DCStart e DCEnd enumerano rispettivamente i thread attualmente in esecuzione al momento dell'avvio e della fine della sessione del kernel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Thread**](thread.md)
</dt> <dt>

[**Thread \_ V2**](thread-v2.md)
</dt> </dl>

 

 




