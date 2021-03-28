---
description: Rappresenta la classe del tipo di evento per gli eventi di creazione o chiusura dell'handle.
ms.assetid: 39d27cdf-fa51-4fb1-8998-7150ca627eff
title: Classe ObHandleEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleEvent
- ObHandleEvent.Handle
- ObHandleEvent.Object
- ObHandleEvent.ObjectName
- ObHandleEvent.ObjectType
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae293684bd09322c7193035d374e5e2bad21447f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980114"
---
# <a name="obhandleevent-class"></a>Classe ObHandleEvent

Rappresenta la classe del tipo di evento per gli eventi di creazione o chiusura dell'handle.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, EventType{32,33}, EventTypeName{CreateHandle,CloseHandle}]
class ObHandleEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
};
```

## <a name="members"></a>Members

La classe **ObHandleEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **ObHandleEvent** dispone di queste proprietà.

<dl> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Handle dell'oggetto.

</dd> <dt>

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

**ObjectName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Nome dell'oggetto.

</dd> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Tipo di oggetto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |



 

 




