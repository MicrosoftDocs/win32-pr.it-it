---
title: Elemento CalendarTrigger (triggerGroup)
description: Specifica un trigger giornaliero, settimanale, mensile o mensile.
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- trigger di calendario Utilità di pianificazione, elemento XML
- Elemento CalendarTrigger Utilità di pianificazione
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d02b14fa056940a8139e87d9b471f6eaef84c311eb095073f274a9b4adf3c6dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516971"
---
# <a name="calendartrigger-triggergroup-element"></a>Elemento CalendarTrigger (triggerGroup)

Specifica un trigger giornaliero, settimanale, mensile o mensile.

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

**L'elemento CalendarTrigger** è definito dal tipo complesso [**calendarTriggerType.**](taskschedulerschema-calendartriggertype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Specifica i trigger che avviano l'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                                            | Tipo                                                                                                 | Descrizione                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Abilitato (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | boolean                                                                                              | Specifica che il trigger è abilitato.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | dateTime                                                                                             | Specifica la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo la disattivazione.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | duration                                                                                             | Specifica la quantità massima di tempo durante la quale l'attività può essere avviata dal trigger.<br/>                                   |
| [**Ripetizione (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md)                             | Specifica la frequenza di esecuzione dell'attività e la durata della ripetizione del criterio di ripetizione dopo l'avvio dell'attività.<br/>          |
| [**ScheduleByDay (calendarTriggerType)**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md)                       | Specifica una pianificazione giornaliera.<br/>                                                                                             |
| [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | Specifica una pianificazione mensile.<br/>                                                                                           |
| [**ScheduleByMonthDayOfWeek (calendarTriggerType)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Specifica un trigger che avvia un processo in base a una pianificazione giornaliera mensile.<br/>                                                |
| [**ScheduleByWeek (calendarTriggerType)**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | Specifica una pianificazione settimanale.<br/>                                                                                            |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | dateTime                                                                                             | Specifica la data e l'ora di attivazione del trigger. Questo elemento è obbligatorio.<br/>                                    |



## <a name="attributes"></a>Attributi



| Nome | Tipo | Descrizione                               |
|------|------|-------------------------------------------|
| Id   | ID   | Identificatore del trigger.<br/> |



## <a name="remarks"></a>Commenti

[**L'elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) è un elemento obbligatorio per i trigger di ora e calendario ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) e **CalendarTrigger**).

Gli elementi figlio elencati in precedenza sono definiti dai tipi di elemento complessi [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) e [**calendarTriggerType.**](taskschedulerschema-calendartriggertype-complextype.md)

Per lo sviluppo di script, i trigger di calendario vengono specificati usando uno degli oggetti seguenti.

-   [**DailyTrigger**](dailytrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)

Per lo sviluppo C++, i trigger di calendario vengono specificati usando una delle interfacce seguenti.

-   [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che specifica un trigger di calendario, vedere [Daily Trigger Example (XML) ( Esempio di trigger giornaliero (XML)](daily-trigger-example--xml-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione elementi dello schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





