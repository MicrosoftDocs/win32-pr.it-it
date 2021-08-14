---
description: 'Registry_TypeGroup1: questa classe è la classe del tipo di evento per gli eventi del Registro di sistema. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 8d0e9d97-3837-46da-a217-13e943580352
title: Registry_TypeGroup1 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_TypeGroup1
- Registry_TypeGroup1.InitialTime
- Registry_TypeGroup1.Status
- Registry_TypeGroup1.Index
- Registry_TypeGroup1.KeyHandle
- Registry_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7bdb280f78f0c38cbb887920425c018ded1505aa2f1e01cc0981e292f9d139a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394243"
---
# <a name="registry_typegroup1-class"></a>Classe \_ TypeGroup1 del Registro di sistema

Questa classe è la classe del tipo di evento per gli eventi del Registro di sistema.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "KCBCreate", "KCBDelete", "KCBRundownBegin", "KCBRundownEnd", "Virtualize", "Close"}]
class Registry_TypeGroup1 : Registry
{
  sint64 InitialTime;
  uint32 Status;
  uint32 Index;
  uint32 KeyHandle;
  string KeyName;
};
```

## <a name="members"></a>Members

La **classe \_ Registry TypeGroup1** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Registry TypeGroup1** ha queste proprietà.

<dl> <dt>

Indice
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3)
</dt> </dl>

Indice della sottochiave per l'operazione del Registro di sistema, ad esempio EnumerateKey.

</dd> <dt>

InitialTime
</dt> <dd> <dl> <dt>

Tipo di dati: **sint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1)
</dt> </dl>

Ora iniziale dell'operazione del Registro di sistema.

</dd> <dt>

KeyHandle
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4), Pointer
</dt> </dl>

Handle per la chiave del Registro di sistema.

</dd> <dt>

KeyName
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(5), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

nome della chiave del Registro di sistema.

</dd> <dt>

Stato
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), Pointer
</dt> </dl>

Valore NTSTATUS dell'operazione del Registro di sistema.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Registro**](registry.md)
</dt> </dl>

 

 




