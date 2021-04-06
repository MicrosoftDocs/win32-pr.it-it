---
title: Valore (namedValues) (elemento)
description: Contiene il valore associato a un nome in una coppia nome-valore.
ms.assetid: d5582b55-0b9b-4fed-a425-9d15a1a62fb7
keywords:
- Elemento Value Utilità di pianificazione
topic_type:
- apiref
api_name:
- Value
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afa12156a15ff399f3cbc967a5fd9c612df582b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743319"
---
# <a name="value-namedvalues-element"></a>Valore (namedValues) (elemento)

Contiene il valore associato a un nome in una coppia nome-valore.

``` syntax
<xs:element name="Value"
    type="namedValue"
    minOccurs="1"
    maxOccurs="32"
 />
```

L'elemento **value** è definito dal tipo complesso [**namedValues**](taskschedulerschema-namedvalues-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                              | Derivato da                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ValueQueries (eventTriggerType)**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md) | Specifica una raccolta di query XPath denominate. Ogni query della raccolta viene applicata all'ultimo XML dell'evento corrispondente restituito dalla query di sottoscrizione specificata nell'elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) . Il nome della query può essere utilizzato come variabile nel messaggio di un'azione ShowMessage.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**proprietà Value di ITaskNamedValuePair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).

Per lo sviluppo di script, vedere [**TaskNamedValuePair. Value**](tasknamedvaluepair-value.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





