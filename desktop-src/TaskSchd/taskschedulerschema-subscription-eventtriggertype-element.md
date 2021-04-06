---
title: Elemento Subscription (eventTriggerType)
description: Specifica la query XPath che identifica l'evento che attiva il trigger.
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- Utilità di pianificazione dell'elemento subscription
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efe38f2e825e2de566391a7b1707ce1f8cfbbc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743767"
---
# <a name="subscription-eventtriggertype-element"></a>Elemento Subscription (eventTriggerType)

Specifica la query XPath che identifica l'evento che attiva il trigger.

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

L'elemento **Subscription** è definito dal tipo complesso [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                       | Derivato da                                                                 | Descrizione                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, la sottoscrizione dell'evento viene specificata dalla proprietà [**EventTrigger. Subscription**](eventtrigger-subscription.md) .

Per lo sviluppo in C++, la sottoscrizione dell'evento viene specificata dalla proprietà [**IEventTrigger:: Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





