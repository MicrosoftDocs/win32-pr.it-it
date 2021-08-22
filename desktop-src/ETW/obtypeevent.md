---
description: Rappresenta la classe del tipo di evento per gli eventi di tipo oggetto correlati all'inizio e alla fine della raccolta dati.
ms.assetid: 16b21f61-e734-4f51-9b11-e507b5957107
title: Classe ObTypeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTypeEvent
- ObTypeEvent.ObjectType
- ObTypeEvent.Reserved
- ObTypeEvent.TypeName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3659d89baa94da0c3161f7bcd6c9ff94d27efef467af8caafa70adfe1c4a7b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070052"
---
# <a name="obtypeevent-class"></a>Classe ObTypeEvent

Rappresenta la classe del tipo di evento per gli eventi di tipo oggetto correlati all'inizio e alla fine della raccolta dati. Questo evento comporta il mapping dei valori di indice del tipo ai nomi dei tipi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, EventType{36,37}, EventTypeName{TypeDCStart,TypeDCEnd}]
class ObTypeEvent : ObTrace
{
  uint16 ObjectType;
  uint16 Reserved;
  string TypeName;
};
```

## <a name="members"></a>Members

La **classe ObTypeEvent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe ObTypeEvent** ha queste proprietà.

<dl> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Tipo di oggetto.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Riservato.

</dd> <dt>

**Typename**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Nome del tipo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |



 

 




