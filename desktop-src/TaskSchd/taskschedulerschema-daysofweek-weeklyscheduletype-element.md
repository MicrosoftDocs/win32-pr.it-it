---
title: Elemento DaysOfWeek (weeklyScheduleType)
description: Specifica i giorni della settimana in cui viene eseguita l'attività. | Elemento DaysOfWeek (weeklyScheduleType)
ms.assetid: 86555681-2324-4095-9eab-fdef40e0acba
keywords:
- Utilità di pianificazione elemento DaysOfWeek
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a2b310feb49f3141d1f7f08c4552305f9ffc3ea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321844"
---
# <a name="daysofweek-weeklyscheduletype-element"></a>Elemento DaysOfWeek (weeklyScheduleType)

Specifica i giorni della settimana in cui viene eseguita l'attività.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

L'elemento **DaysOfWeek** è definito dal tipo complesso [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                  | Derivato da                                                                     | Descrizione                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) | Specifica una pianificazione settimanale.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                   | Tipo | Descrizione                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Friday**](taskschedulerschema-friday-daysofweektype-element.md)       |      | Specifica che l'attività viene eseguita il venerdì.<br/>    |
| [**Monday**](taskschedulerschema-monday-daysofweektype-element.md)       |      | Specifica che l'attività viene eseguita il lunedì.<br/>    |
| [**Sabato**](taskschedulerschema-saturday-daysofweektype-element.md)   |      | Specifica che l'attività viene eseguita il sabato.<br/>  |
| [**Sunday**](taskschedulerschema-sunday-daysofweektype-element.md)       |      | Specifica che l'attività viene eseguita la domenica.<br/>    |
| [**Thursday**](taskschedulerschema-thursday-daysofweektype-element.md)   |      | Specifica che l'attività viene eseguita il giovedì.<br/>  |
| [**Tuesday**](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | Specifica che l'attività viene eseguita il martedì.<br/>   |
| [**Wednesday**](taskschedulerschema-wednesday-daysofweektype-element.md) |      | Specifica che l'attività viene eseguita il mercoledì.<br/> |



## <a name="remarks"></a>Commenti

Gli elementi figlio precedenti sono definiti dal tipo complesso [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

Per lo sviluppo di script, l'intervallo settimanale viene specificato tramite la proprietà [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) .

Per lo sviluppo in C++, l'intervallo settimanale viene specificato con la proprietà [**IWeeklyTrigger:: WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un trigger di calendario giornaliero che avvia un'attività dal lunedì al venerdì (alle 8:00 AM) ogni settimana.


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



Per un esempio completo del codice XML per un'attività che usa un trigger settimanale, vedere [esempio di trigger settimanale (XML)](weekly-trigger-example--xml-.md).

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

 

 





