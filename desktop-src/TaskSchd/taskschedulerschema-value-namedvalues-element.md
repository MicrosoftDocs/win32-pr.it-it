---
title: Elemento Value (namedValues)
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
ms.openlocfilehash: 2583d7fcaa9a9832e54c405200397e40948204546cb81e89a90ceb6949e218e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610416"
---
# <a name="value-namedvalues-element"></a>Elemento Value (namedValues)

Contiene il valore associato a un nome in una coppia nome-valore.

``` syntax
<xs:element name="Value"
    type="namedValue"
    minOccurs="1"
    maxOccurs="32"
 />
```

**L'elemento** Value è definito dal [**tipo complesso namedValues.**](taskschedulerschema-namedvalues-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                              | Derivato da                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ValueQueries (eventTriggerType)**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md) | Specifica una raccolta di query XPath denominate. Ogni query nella raccolta viene applicata all'ultimo XML dell'evento corrispondente restituito dalla query di sottoscrizione specificata [**nell'elemento Subscription.**](taskschedulerschema-subscription-eventtriggertype-element.md) Il nome della query può essere usato come variabile nel messaggio di un'azione ShowMessage.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**Proprietà Value di ITaskNamedValuePair.**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value)

Per lo sviluppo di script, [**vedere TaskNamedValuePair.Value.**](tasknamedvaluepair-value.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





