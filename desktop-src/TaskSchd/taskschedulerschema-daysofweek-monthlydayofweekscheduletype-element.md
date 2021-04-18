---
title: Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)
description: Specifica i giorni della settimana in cui viene eseguita l'attività. | Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
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
ms.openlocfilehash: 3867e08dd001a035a3ab25da056f75c1e73eeeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321845"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a>Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)

Specifica i giorni della settimana in cui viene eseguita l'attività.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

L'elemento **DaysOfWeek** è definito dal tipo complesso [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                      | Derivato da                                                                                         | Descrizione                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Specifica un trigger che avvia un processo per una pianificazione mensile del giorno della settimana.<br/> |



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

Per lo sviluppo di script, i giorni della settimana per un calendario mensile di giorno della settimana vengono specificati utilizzando la proprietà [**MonthlyDOWTrigger. DaysOfWeek**](monthlydowtrigger-daysofweek.md) .

Per lo sviluppo in C++, i giorni della settimana per un calendario mensile di giorno della settimana vengono specificati usando la proprietà [**IMonthlyDOWTrigger::D aysofweek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) .

Gli elementi figlio precedenti sono definiti dal tipo complesso [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un calendario mensile del giorno della settimana che avvia l'attività il lunedì della prima settimana per ogni mese dell'anno.


```XML
<ScheduleByMonthDayOfWeek>
    <Weeks>
        <Week>1</Week>
    </Weeks>
    <DaysOfWeek>
        <Monday/>
    </DaysOfWeek>
    <Months>
        <January/>
        <February/>
        <March/>
        <April/>
        <May/>
        <June/>
        <July/>
        <August/>
        <September/>
        <October/>
        <November/>
        <December/>
    <Months>
</ScheduleByMonthDayOfWeek>
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

 

 





