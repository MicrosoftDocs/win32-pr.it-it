---
title: Triggers (taskType)-elemento
description: Specifica i trigger che avviano l'attività.
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- Triggers Utilità di pianificazione elemento
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06994c395fbfbc5b0c6244c9d17930bc4afac885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743754"
---
# <a name="triggers-tasktype-element"></a>Triggers (taskType)-elemento

Specifica i trigger che avviano l'attività.

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

L'elemento **Triggers** è definito dal tipo complesso [**triggersType**](taskschedulerschema-triggerstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                          | Derivato da                                                 | Descrizione                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Attività**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Definisce l'attività eseguita dal servizio Utilità di pianificazione.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                     | Tipo                                                                                       | Descrizione                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività quando viene avviato il sistema.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività quando il computer entra in uno stato di inattività.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando l'attività è registrata.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività quando viene attivato il trigger.<br/>             |



## <a name="remarks"></a>Commenti

Gli elementi figlio elencati sopra possono essere aggiunti in qualsiasi ordine.

Per lo sviluppo in C++, i trigger di un'attività vengono specificati utilizzando la [**Proprietà Triggers di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).

Per lo sviluppo di script, i trigger di un'attività vengono specificati utilizzando la proprietà [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che specifica un trigger, vedere [esempio di trigger di ora (XML)](time-trigger-example--xml-.md).

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

 

 





