---
title: Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)
description: Specifica una pianificazione mensile giornaliera della settimana.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- Utilità di pianificazione elemento ScheduleByMonthDayOfWeek
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e92d6ad530466a2238c8239c9e262f85ae361d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742890"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a>Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)

Specifica una pianificazione mensile giornaliera della settimana. Ad esempio, l'attività viene avviata in giorni specifici della settimana, settimane del mese e mesi dell'anno.

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

L'elemento **ScheduleByMonthDayOfWeek** è definito dal tipo complesso [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                             | Derivato da                                                                       | Descrizione                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                   | Tipo                                                                     | Descrizione                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Specifica i giorni della settimana in cui viene eseguita l'attività.<br/>       |
| [**Mesi**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**monthsType**](taskschedulerschema-monthstype-complextype.md)         | Specifica i mesi dell'anno durante i quali viene eseguita l'attività.<br/> |
| [**Settimane**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | unsignedByte                                                             | Specifica l'intervallo tra le settimane nella pianificazione.<br/>    |



## <a name="remarks"></a>Commenti

L'ora del giorno in cui l'attività viene avviata viene impostata dall'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .

Per lo sviluppo di script, viene specificato un trigger di giorno della settimana mensile utilizzando l'oggetto [**MonthlyDOWTrigger**](monthlydowtrigger.md) .

Per lo sviluppo in C++, viene specificato un trigger di giorno della settimana mensile usando l'interfaccia [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) .

Gli elementi figlio elencati sopra sono definiti dai tipi di elemento complessi [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un trigger di calendario mensile del giorno della settimana che avvia un'attività (alle 8:00 AM) il lunedì della prima settimana per ogni mese dell'anno.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
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

 

 





