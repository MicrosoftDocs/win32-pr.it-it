---
description: Questa classe è la classe del tipo di evento per gli eventi del registro di sistema. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 59c455a0-af7e-4fd5-9af4-07ff72ee0545
title: Classe Registry_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V1_TypeGroup1
- Registry_V1_TypeGroup1.Status
- Registry_V1_TypeGroup1.KeyHandle
- Registry_V1_TypeGroup1.ElapsedTime
- Registry_V1_TypeGroup1.Index
- Registry_V1_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2cd77ad0c12769c657b4e7c23c1fe1993a248481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879514"
---
# <a name="registry_v1_typegroup1-class"></a>\_ \_ Classe TypeGroup1 del registro di sistema V1

Questa classe è la classe del tipo di evento per gli eventi del registro di sistema.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "RunDown"}]
class Registry_V1_TypeGroup1 : Registry
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  uint32 Index;
  string KeyName;
};
```

## <a name="members"></a>Members

La **classe \_ \_ TypeGroup1 del registro di sistema V1** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Per la classe **\_ \_ TypeGroup1 del registro di sistema V1** sono presenti queste proprietà.

<dl> <dt>

ElapsedTime
</dt> <dd> <dl> <dt>

Tipo di dati: **sint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3)
</dt> </dl>

Tempo trascorso per l'operazione del registro di sistema.

</dd> <dt>

Indice
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4)
</dt> </dl>

Indice della sottochiave per l'operazione del registro di sistema (ad esempio EnumerateKey).

</dd> <dt>

KeyHandle
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), puntatore
</dt> </dl>

Handle per la chiave del registro di sistema.

</dd> <dt>

KeyName
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

nome della chiave del Registro di sistema.

</dd> <dt>

Stato
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Valore NTSTATUS dell'operazione del registro di sistema.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Registro**](registry.md)
</dt> <dt>

[**Registro di sistema \_ V1**](registry-v1.md)
</dt> </dl>

 

 




