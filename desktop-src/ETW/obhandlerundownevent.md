---
description: Rappresenta la classe del tipo di evento per gli eventi dell'handle di oggetto correlati all'inizio e alla fine della raccolta dei dati.
ms.assetid: 96231819-f4ca-4c5c-bc19-4a76add5d3cf
title: Classe ObHandleRundownEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleRundownEvent
- ObHandleRundownEvent.Handle
- ObHandleRundownEvent.Object
- ObHandleRundownEvent.ObjectName
- ObHandleRundownEvent.ObjectType
- ObHandleRundownEvent.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5477acc1851d9799fe2bf68f9b867ab3f4c032fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980119"
---
# <a name="obhandlerundownevent-class"></a>Classe ObHandleRundownEvent

Rappresenta la classe del tipo di evento per gli eventi dell'handle di oggetto correlati all'inizio e alla fine della raccolta dei dati. Questo evento comporta l'enumerazione di tutti gli handle quando viene eseguito il rundown.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, EventType{38,39}, EventTypeName{HandleDCStart,HandleDCEnd}]
class ObHandleRundownEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
  uint32 ProcessId;
};
```

## <a name="members"></a>Members

La classe **ObHandleRundownEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **ObHandleRundownEvent** dispone di queste proprietà.

<dl> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
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

Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Nome dell'oggetto.

</dd> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Tipo di oggetto.

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Identificatore di processo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |



 

 




