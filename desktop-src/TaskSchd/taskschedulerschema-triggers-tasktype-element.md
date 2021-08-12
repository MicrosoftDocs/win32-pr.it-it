---
title: Elemento Triggers (taskType)
description: Specifica i trigger che avviano l'attività.
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- Trigger dell'elemento Utilità di pianificazione
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d067c9e315006c55e07e972e5616525750d8a383d7ed8294f7d39a6acf32caff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610885"
---
# <a name="triggers-tasktype-element"></a>Elemento Triggers (taskType)

Specifica i trigger che avviano l'attività.

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

**L'elemento** Triggers è definito dal [**tipo complesso triggersType.**](taskschedulerschema-triggerstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                          | Derivato da                                                 | Descrizione                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Attività**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Definisce l'attività eseguita dal Utilità di pianificazione servizio.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                     | Tipo                                                                                       | Descrizione                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività all'avvio del sistema.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Specifica un trigger giornaliero, settimanale, mensile o mensile del giorno della settimana.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività quando il computer entra in uno stato di inattività.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando l'attività viene registrata.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività quando il trigger viene attivato.<br/>             |



## <a name="remarks"></a>Commenti

Gli elementi figlio elencati in precedenza possono essere aggiunti in qualsiasi ordine.

Per lo sviluppo in C++, i trigger di un'attività vengono specificati usando la [**proprietà Triggers di ITaskDefinition.**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers)

Per lo sviluppo di script, i trigger di un'attività vengono specificati usando la [**proprietà TaskDefinition.Triggers.**](taskdefinition-triggers.md)

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che specifica un trigger, vedere [Esempio di trigger temporale (XML).](time-trigger-example--xml-.md)

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

 

 





