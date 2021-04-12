---
title: Elemento ScheduleByWeek (calendarTriggerType)
description: Specifica una pianificazione settimanale.
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- Utilità di pianificazione trigger settimanale, elemento XML
- Utilità di pianificazione elemento ScheduleByWeek
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d5ab62a0c39c4c1d0102edcdb96d310e9315820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400886"
---
# <a name="schedulebyweek-calendartriggertype-element"></a>Elemento ScheduleByWeek (calendarTriggerType)

Specifica una pianificazione settimanale. Ad esempio, l'attività inizia alle 8:00 in un giorno specifico della settimana ogni settimana o in un giorno specifico della settimana ogni altra settimana.

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

L'elemento **ScheduleByWeek** è definito dal tipo complesso [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                             | Derivato da                                                                       | Descrizione                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                               | Tipo                                                                     | Descrizione                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Specifica i giorni della settimana in cui viene eseguita l'attività.<br/>    |
| [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | unsignedByte                                                             | Specifica l'intervallo tra le settimane nella pianificazione.<br/> |



## <a name="remarks"></a>Commenti

Gli elementi figlio elencati sopra sono definiti dai tipi di elemento complessi [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .

L'ora del giorno in cui l'attività viene avviata viene impostata dall'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .

Per lo sviluppo di script, viene specificato un trigger settimanale usando l'oggetto [**WeeklyTrigger**](weeklytrigger.md) .

Per lo sviluppo in C++, viene specificato un trigger settimanale usando l'interfaccia [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) .

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un trigger di calendario settimanale che avvia un'attività dal lunedì al venerdì (alle 8:00 AM) ogni settimana.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByWeek>
        <WeeksInterval>1</WeeksInterval>
        <DaysOfWeek>
            <Monday/>
            <Tuesday/>
            <Wednesday/>
            <Thurday/>
            <Friday/>
        </DaysOfWeek>
    </ScheduleByWeek>
</CalendarTrigger>
```



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

 

 





