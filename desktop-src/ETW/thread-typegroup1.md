---
description: Questa classe è la classe del tipo di evento per gli eventi di inizio e di fine del thread. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: d9e3e33a-0e59-4753-a8d8-5320cbae9d95
title: Classe Thread_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_TypeGroup1
- Thread_TypeGroup1.ProcessId
- Thread_TypeGroup1.TThreadId
- Thread_TypeGroup1.StackBase
- Thread_TypeGroup1.StackLimit
- Thread_TypeGroup1.UserStackBase
- Thread_TypeGroup1.UserStackLimit
- Thread_TypeGroup1.Affinity
- Thread_TypeGroup1.Win32StartAddr
- Thread_TypeGroup1.TebBase
- Thread_TypeGroup1.SubProcessTag
- Thread_TypeGroup1.BasePriority
- Thread_TypeGroup1.PagePriority
- Thread_TypeGroup1.IoPriority
- Thread_TypeGroup1.ThreadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75352efbe044f5fee837c496c394fe28e2dbbbfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130706"
---
# <a name="thread_typegroup1-class"></a>\_Classe thread TypeGroup1

Questa classe è la classe del tipo di evento per gli eventi di inizio e di fine del thread.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_TypeGroup1 : Thread
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 Affinity;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
  uint8  BasePriority;
  uint8  PagePriority;
  uint8  IoPriority;
  uint8  ThreadFlags;
};
```

## <a name="members"></a>Members

La classe **thread \_ TypeGroup1** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **thread \_ TypeGroup1** dispone di queste proprietà.

<dl> <dt>

Affinità
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (7), puntatore
</dt> </dl>

Set di processori in cui è consentita l'esecuzione del thread.

</dd> <dt>

Relativa BasePriority
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (11)
</dt> </dl>

Priorità dell'utilità di pianificazione del thread (vedere la funzione [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) ).

</dd> <dt>

IoPriority
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (13)
</dt> </dl>

Un hint di priorità i/o per la pianificazione di IOs generati dal thread.

</dd> <dt>

PagePriority
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (12)
</dt> </dl>

Hint di priorità della pagina di memoria per le pagine di memoria a cui accede il thread.

</dd> <dt>

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

ThreadFlags
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (14)
</dt> </dl>

Non usato.

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
</dt> </dl>

 

 
