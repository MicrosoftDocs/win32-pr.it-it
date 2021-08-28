---
title: Elemento StartBoundary (triggerBaseType)
description: Specifica la data e l'ora di attivazione del trigger.
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- Elemento StartBoundary Utilità di pianificazione
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46584659fbd14bc26981e220798a91c03e960e1f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886421"
---
# <a name="startboundary-triggerbasetype-element"></a>Elemento StartBoundary (triggerBaseType)

Specifica la data e l'ora di attivazione del trigger.

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

**L'elemento StartBoundary** è definito dal tipo complesso [**triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

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

**&lt; L'elemento &gt; StartBoundary** è un elemento obbligatorio per i trigger di ora e calendario ([**&lt; TimeTrigger &gt;**](taskschedulerschema-timetrigger-triggergroup-element.md) e [**&lt; CalendarTrigger &gt;**](taskschedulerschema-calendartrigger-triggergroup-element.md)).

Per lo sviluppo di script, il limite finale viene specificato usando la [**proprietà Trigger.StartBoundary**](trigger-startboundary.md) ereditata da tutti gli oggetti trigger.

Per lo sviluppo C++, il limite finale viene specificato usando la proprietà [**ITrigger::StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) ereditata da tutte le interfacce trigger.

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un elemento trigger di avvio che definisce un limite di inizio del 1° gennaio 2005: 8:00 AM.


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

 

 





