---
description: Rappresenta la classe del tipo di evento per gli eventi di duplicazione dell'handle.
ms.assetid: a933ffaa-8c99-4b87-ad00-4c40fa4d8d26
title: Classe ObHandleDuplicateEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleDuplicateEvent
- ObHandleDuplicateEvent.Object
- ObHandleDuplicateEvent.ObjectType
- ObHandleDuplicateEvent.SourceHandle
- ObHandleDuplicateEvent.TargetHandle
- ObHandleDuplicateEvent.TargetProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0f81ff9d85c0c5de8469f563db21e2054fa065f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980687"
---
# <a name="obhandleduplicateevent-class"></a>Classe ObHandleDuplicateEvent

Rappresenta la classe del tipo di evento per gli eventi di duplicazione dell'handle.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, EventType(34), EventTypeName("DuplicateHandle")]
class ObHandleDuplicateEvent : ObTrace
{
  uint32 Object;
  uint16 ObjectType;
  uint32 SourceHandle;
  uint32 TargetHandle;
  uint32 TargetProcessId;
};
```

## <a name="members"></a>Members

La classe **ObHandleDuplicateEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **ObHandleDuplicateEvent** dispone di queste proprietà.

<dl> <dt>

**Object**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Oggetto.

</dd> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Tipo di oggetto.

</dd> <dt>

**SourceHandle**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Handle dell'oggetto di origine.

</dd> <dt>

**TargetHandle**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Handle dell'oggetto di destinazione.

</dd> <dt>

**TargetProcessId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Identificatore del processo della destinazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |



 

 




