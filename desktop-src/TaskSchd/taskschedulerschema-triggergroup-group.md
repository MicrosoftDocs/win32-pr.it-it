---
title: Gruppo triggerGroup
description: Definisce il gruppo di trigger.
ms.assetid: e07e6999-d982-405b-adfd-2976707b999f
keywords:
- TriggerGroup Utilità di pianificazione
topic_type:
- apiref
api_name:
- triggerGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74ae14f6e22245e49b2c2d0136fd297b35c9c5ed1f5126cc0914e97f42c8488f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611002"
---
# <a name="triggergroup-group"></a>Gruppo triggerGroup

Definisce il gruppo di trigger.

``` syntax
<xs:group name="triggerGroup">
    <xs:choice>
        <xs:element name="BootTrigger"
            type="bootTriggerType"
            minOccurs="0"
         />
        <xs:element name="RegistrationTrigger"
            type="registrationTriggerType"
            minOccurs="0"
         />
        <xs:element name="IdleTrigger"
            type="idleTriggerType"
            minOccurs="0"
         />
        <xs:element name="TimeTrigger"
            type="timeTriggerType"
            minOccurs="0"
         />
        <xs:element name="EventTrigger"
            type="eventTriggerType"
            minOccurs="0"
         />
        <xs:element name="LogonTrigger"
            type="logonTriggerType"
            minOccurs="0"
         />
        <xs:element name="SessionStateChangeTrigger"
            type="sessionStateChangeTriggerType"
            minOccurs="0"
         />
        <xs:element name="CalendarTrigger"
            type="calendarTriggerType"
            minOccurs="0"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                 | Tipo                                                                                                   | Descrizione                                                                                                       |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                             | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                             | Trigger che avvia un'attività all'avvio del sistema.<br/>                                                |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)                     | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)                     | Trigger che avvia un'attività in base a una pianificazione giornaliera, settimanale, mensile o mensile del giorno della settimana.<br/> |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)                           | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)                           | Trigger che avvia un'attività quando si verifica un evento di sistema.<br/>                                               |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                             | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                             | Trigger che avvia un'attività quando il computer entra in uno stato di inattività.<br/>                                |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)                           | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)                           | Trigger che avvia un'attività quando un utente esegue l'accesso.<br/>                                                      |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md)             | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md)             | Trigger che avvia un'attività quando l'attività viene registrata.<br/>                                              |
| [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Trigger che avvia un'attività quando viene modificato lo stato di una sessione di Terminal Server.<br/>                             |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                             | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                             | Trigger che avvia un'attività quando il trigger viene attivato.<br/>                                            |



## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML, gli elementi definiti da questo gruppo sono gli elementi figlio [**dell'elemento Triggers.**](taskschedulerschema-triggers-tasktype-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





