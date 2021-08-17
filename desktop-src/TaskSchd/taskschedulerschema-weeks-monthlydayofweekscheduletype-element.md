---
title: Elemento Weeks (monthlyDayOfWeekScheduleType)
description: Specifica le settimane del mese in cui viene eseguita l'attività.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Elemento Weeks Utilità di pianificazione
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81219236012146dac54965af471412369d5c5bb34319897d4d821bb10a730aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757978"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a>Elemento Weeks (monthlyDayOfWeekScheduleType)

Specifica le settimane del mese in cui viene eseguita l'attività.

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

**L'elemento Weeks** è definito dal [**tipo complesso monthlyDayOfWeekScheduleType.**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                      | Derivato da                                                                                         | Descrizione                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Specifica un trigger che avvia un processo in base a una pianificazione giornaliera mensile.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                    | Tipo                                                        | Descrizione                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [**Settimana**](taskschedulerschema-week-weekstype-element.md) | [**weekType**](taskschedulerschema-weektype-simpletype.md) | Specifica una settimana specifica del mese.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, le settimane del mese vengono specificate usando la [**proprietà MonthlyDOWTrigger.WeeksOfMonth.**](monthlydowtrigger-weeksofmonth.md)

Per lo sviluppo C++, le settimane del mese vengono specificate usando la [**proprietà IMonthlyDOWTrigger::WeeksOfMonth.**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth)

Quando si specificano le settimane del mese, usare da 1 a 4 per specificare le prime quattro settimane del mese o usare la stringa "Last" per indicare l'ultima settimana indipendentemente dalla settimana.

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un calendario mensile giorno della settimana che avvia l'attività il lunedì della prima settimana per ogni mese dell'anno.


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





