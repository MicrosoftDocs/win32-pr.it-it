---
title: Elemento EndBoundary (triggerBaseType)
description: Specifica la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo la disattivazione.
ms.assetid: 84731c0b-3fb8-44dd-be1a-67547add1f9e
keywords:
- Elemento EndBoundary Utilità di pianificazione
topic_type:
- apiref
api_name:
- EndBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e26eb05b7b9fa15c0667fff7fd0d1eb85e61ed2daa90d6a238cbf9575f6c0e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010741"
---
# <a name="endboundary-triggerbasetype-element"></a>Elemento EndBoundary (triggerBaseType)

Specifica la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo la disattivazione.

``` syntax
<xs:element name="EndBoundary"
    type="dateTime"
 />
```

**L'elemento EndBoundary** è definito dal tipo complesso [**triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                     | Derivato da                                                                               | Descrizione                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività all'avvio del sistema.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Specifica un trigger giornaliero, settimanale, mensile o mensile.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività quando il computer passa a uno stato di inattività.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Specifica un trigger che avvia un'attività quando un utente accede.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando l'attività viene registrata.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Specifica un trigger che avvia un'attività quando il trigger viene attivato.<br/>             |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, il limite finale viene specificato usando la [**proprietà Trigger.EndBoundary**](trigger-endboundary.md) ereditata da tutti gli oggetti trigger.

Per lo sviluppo C++, il limite finale viene specificato usando la proprietà [**ITrigger::EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) ereditata da tutte le interfacce trigger.

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un elemento trigger di avvio che definisce un limite finale del 1° gennaio 2007: 8:00 AM.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



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

 

 





