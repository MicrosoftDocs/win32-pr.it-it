---
title: Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)
description: Specifica una pianificazione mensile del giorno della settimana.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- Elemento ScheduleByMonthDayOfWeek Utilità di pianificazione
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 185608ea5a8805511de8430c82e6eecabd9cc5b9622fed85d71e26dd39f20cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099881"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a>Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)

Specifica una pianificazione mensile del giorno della settimana. Ad esempio, l'attività inizia in giorni specifici della settimana, settimane del mese e mesi dell'anno.

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

**L'elemento ScheduleByMonthDayOfWeek** è definito dal tipo complesso [**monthlyDayOfWeekScheduleType.**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                             | Derivato da                                                                       | Descrizione                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Specifica un trigger giornaliero, settimanale, mensile o mensile.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                   | Tipo                                                                     | Descrizione                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Specifica i giorni della settimana in cui viene eseguita l'attività.<br/>       |
| [**Mesi**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**monthsType**](taskschedulerschema-monthstype-complextype.md)         | Specifica i mesi dell'anno durante i quali viene eseguita l'attività.<br/> |
| [**Settimane**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | unsignedByte                                                             | Specifica l'intervallo tra le settimane nella pianificazione.<br/>    |



## <a name="remarks"></a>Commenti

L'ora del giorno in cui l'attività viene avviata viene impostata [**dall'elemento StartBoundary.**](taskschedulerschema-startboundary-triggerbasetype-element.md)

Per lo sviluppo di script, viene specificato un trigger mensile giorno della settimana usando [**l'oggetto MonthlyDOWTrigger.**](monthlydowtrigger.md)

Per lo sviluppo C++, viene specificato un trigger giornaliero mensile tramite [**l'interfaccia IMonthlyDOWTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

Gli elementi figlio elencati in precedenza sono definiti dai tipi di elemento complessi [**monthlyDayOfWeekScheduleType.**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un trigger di calendario mensile giorno della settimana che avvia un'attività ( alle 8:00 AM) il lunedì della prima settimana per ogni mese dell'anno.


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione elementi dello schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





