---
title: Elemento Enabled (triggerBaseType)
description: Specifica che il trigger è abilitato.
ms.assetid: 14c98f40-0ec5-4dc1-978e-b02c08ee2384
keywords:
- Elemento Enabled Utilità di pianificazione
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc7ecfb58425533234637708e6c5610f3a84cdaf8e2058d088a68e3c0c707384
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072501"
---
# <a name="enabled-triggerbasetype-element"></a>Elemento Enabled (triggerBaseType)

Specifica che il trigger è abilitato.

``` syntax
<xs:element name="Enabled"
    type="boolean"
 />
```

**L'elemento Enabled** è definito dal [**tipo complesso triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                     | Derivato da                                                                               | Descrizione                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività all'avvio del sistema.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Specifica un trigger giornaliero, settimanale, mensile o mensile del giorno della settimana.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività quando il computer entra in uno stato di inattività.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando l'attività viene registrata.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività quando il trigger viene attivato.<br/>             |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, è possibile accedere a queste informazioni tramite la [**proprietà Trigger.Enabled**](trigger-enabled.md) ereditata da tutti gli oggetti trigger.

Per lo sviluppo in C++, è possibile accedere a queste informazioni tramite la proprietà [**ITrigger::Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) ereditata da tutte le interfacce trigger.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





