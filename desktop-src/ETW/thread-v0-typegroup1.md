---
description: Questa classe è la classe del tipo di evento per gli eventi del thread. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: cc668fef-48fe-4948-8fe5-4351f7a033d1
title: Classe Thread_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V0_TypeGroup1
- Thread_V0_TypeGroup1.TThreadId
- Thread_V0_TypeGroup1.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f6fa7ae1f50e005fe8f66e918a4a8360a0e8f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978223"
---
# <a name="thread_v0_typegroup1-class"></a>\_ \_ Classe TypeGroup1 di thread V0

Questa classe è la classe del tipo di evento per gli eventi del thread.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V0_TypeGroup1 : Thread_V0
{
  uint32 TThreadId;
  uint32 ProcessId;
};
```

## <a name="members"></a>Members

La classe **thread \_ V0 \_ TypeGroup1** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ TypeGroup1 del thread V0** presenta queste proprietà.

<dl> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), Format ("x")
</dt> </dl>

Identificatore del processo del thread che interessano l'evento.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), Format ("x")
</dt> </dl>

Identificatore del thread associato all'evento.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Thread \_ V0**](thread-v0.md)
</dt> </dl>

 

 




