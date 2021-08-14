---
title: Elemento Subscription (eventTriggerType)
description: Specifica la query XPath che identifica l'evento che attiva il trigger.
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- Elemento Subscription Utilità di pianificazione
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ec45a9c240a9dd5d30d2089f98216fc165af13fe418424f5b85feed5e022b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131556"
---
# <a name="subscription-eventtriggertype-element"></a>Elemento Subscription (eventTriggerType)

Specifica la query XPath che identifica l'evento che attiva il trigger.

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

**L'elemento Subscription** è definito dal tipo complesso [**eventTriggerType.**](taskschedulerschema-eventtriggertype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                       | Derivato da                                                                 | Descrizione                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, la sottoscrizione di eventi viene specificata dalla [**proprietà EventTrigger.Subscription.**](eventtrigger-subscription.md)

Per lo sviluppo C++, la sottoscrizione di eventi viene specificata dalla [**proprietà IEventTrigger::Subscription.**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





