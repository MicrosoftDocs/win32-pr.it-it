---
title: Elemento ValueQueries (eventTriggerType)
description: Contiene una sequenza di elementi ognuno dei quali contiene un nome e un valore di query XPath.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- Utilità di pianificazione elemento ValueQueries
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4448693c1c1ab19b2ea13050cc9ab817bdc25e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963912"
---
# <a name="valuequeries-eventtriggertype-element"></a>Elemento ValueQueries (eventTriggerType)

Contiene una sequenza di elementi ognuno dei quali contiene un nome e un valore di query XPath. Le query vengono applicate a un evento restituito dalla sottoscrizione dell'evento specificato nell'elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) . Il nome del valore della query XPath può essere utilizzato come variabile nella sezione Action di un'attività.

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

L'elemento **ValueQueries** è definito dal tipo complesso [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                      | Derivato da                                                                 | Descrizione                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger (triggerGroup)**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**la proprietà ValueQueries di IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).

Per lo sviluppo di script, vedere [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che specifica un trigger di evento usando questo elemento, vedere [esempio di trigger di evento (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

