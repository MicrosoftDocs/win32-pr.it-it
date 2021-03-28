---
description: Questa classe è la classe del tipo di evento per gli eventi di fine thread. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: c495bf22-04ce-4285-8e7e-152e4ab65823
title: Classe Thread_V1_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup2
- Thread_V1_TypeGroup2.ProcessId
- Thread_V1_TypeGroup2.TThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3e56590127b2317813d7431a1cc646fbe76e35a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527289"
---
# <a name="thread_v1_typegroup2-class"></a>\_Classe thread V1 \_ TypeGroup2

Questa classe è la classe del tipo di evento per gli eventi di fine thread.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{2, 4}, EventTypeName{"End", "DCEnd"}]
class Thread_V1_TypeGroup2 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
};
```

## <a name="members"></a>Members

I tipi di membri della classe **thread \_ V1 \_ TypeGroup2** sono i seguenti:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **thread \_ V1 \_ TypeGroup2** dispone di queste proprietà.

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

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Thread \_ V1**](thread-v1.md)
</dt> </dl>

 

 




