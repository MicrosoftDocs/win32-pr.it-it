---
title: Weeks (monthlyDayOfWeekScheduleType)-elemento
description: Specifica le settimane del mese in cui viene eseguita l'attività.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Utilità di pianificazione dell'elemento weeks
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e032b936353d2c89a84b5da684f681ea3c2b6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743311"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a>Weeks (monthlyDayOfWeekScheduleType)-elemento

Specifica le settimane del mese in cui viene eseguita l'attività.

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

L'elemento **weeks** viene definito dal tipo complesso [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                      | Derivato da                                                                                         | Descrizione                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Specifica un trigger che avvia un processo in base a una pianificazione mensile del giorno della settimana.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                    | Tipo                                                        | Descrizione                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [**Settimana**](taskschedulerschema-week-weekstype-element.md) | [**weekType**](taskschedulerschema-weektype-simpletype.md) | Specifica una settimana specifica del mese.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, le settimane del mese vengono specificate utilizzando la proprietà [**MonthlyDOWTrigger. WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) .

Per lo sviluppo in C++, le settimane del mese vengono specificate usando la proprietà [**IMonthlyDOWTrigger:: WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) .

Quando si specificano le settimane del mese, utilizzare 1-4 per specificare le prime quattro settimane del mese oppure utilizzare la stringa "Last" per indicare l'ultima settimana indipendentemente dalla settimana in cui si trova.

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

 

 





