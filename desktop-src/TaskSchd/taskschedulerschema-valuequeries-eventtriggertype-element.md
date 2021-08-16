---
title: Elemento ValueQueries (eventTriggerType)
description: Contiene una sequenza di elementi ognuno dei quali contiene un nome e un valore di query XPath.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- Elemento ValueQueries Utilità di pianificazione
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fecf58696618f1f0f359754bc29aa10680dd1717fe55ffe9fc3e87d0b361b76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355344"
---
# <a name="valuequeries-eventtriggertype-element"></a>Elemento ValueQueries (eventTriggerType)

Contiene una sequenza di elementi ognuno dei quali contiene un nome e un valore di query XPath. Le query vengono applicate a un evento restituito dalla sottoscrizione di eventi specificata [**nell'elemento Subscription.**](taskschedulerschema-subscription-eventtriggertype-element.md) Il nome del valore della query XPath può essere utilizzato come variabile nella sezione azione di un'attività.

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

**L'elemento ValueQueries** è definito dal [**tipo complesso eventTriggerType.**](taskschedulerschema-eventtriggertype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                      | Derivato da                                                                 | Descrizione                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger (triggerGroup)**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**Proprietà ValueQueries di IEventTrigger.**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries)

Per lo sviluppo di script, [**vedere EventTrigger.ValueQueries.**](eventtrigger-valuequeries.md)

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che specifica un trigger di evento usando questo elemento, vedere Esempio di trigger di evento [(XML).](/previous-versions//aa446889(v=vs.85))

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

