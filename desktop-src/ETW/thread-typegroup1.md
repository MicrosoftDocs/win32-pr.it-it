---
description: 'Thread_TypeGroup1 classe: questa classe è la classe del tipo di evento per gli eventi di inizio e fine del thread. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: d9e3e33a-0e59-4753-a8d8-5320cbae9d95
title: Thread_TypeGroup1 classe
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
ms.openlocfilehash: 9693bef4449cc076710a74dd9cef88ae608754b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105709"
---
# <a name="thread_typegroup1-class"></a>Classe \_ TypeGroup1 del thread

Questa classe è la classe del tipo di evento per gli eventi di inizio e fine del thread.

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

La **classe \_ Thread TypeGroup1** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Thread TypeGroup1** ha queste proprietà.

<dl> <dt>

Affinità
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(7), Pointer
</dt> </dl>

Set di processori in cui è consentita l'esecuzione del thread.

</dd> <dt>

BasePriority
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(11)
</dt> </dl>

Priorità dell'utilità di pianificazione del thread (vedere la [**funzione SetThreadPriority).**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)

</dd> <dt>

IoPriority
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(13)
</dt> </dl>

Hint di priorità di I/O per la pianificazione degli I/O generati dal thread.

</dd> <dt>

PagePriority
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(12)
</dt> </dl>

Hint di priorità della pagina di memoria per le pagine di memoria a cui accede il thread.

</dd> <dt>

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

ThreadFlags
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(14)
</dt> </dl>

Non usato.

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

Qualificatori: WmiDataId(6), Puntatore
</dt> </dl>

Limite dello stack in modalità utente del thread.

</dd> <dt>

Win32StartAddr
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(8), Puntatore
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
</dt> </dl>

 

 
