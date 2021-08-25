---
title: Elemento Months (monthlyDayOfWeekScheduleType)
description: Specifica i mesi dell'anno durante i quali viene eseguita l'attività per una pianificazione mensile del giorno della settimana.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Mesi - elemento Utilità di pianificazione
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a963032a2d33f13158af249f2b867037cf50082be005efa579148031c8e30585
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959601"
---
# <a name="months-monthlydayofweekscheduletype-element"></a>Elemento Months (monthlyDayOfWeekScheduleType)

Specifica i mesi dell'anno durante i quali viene eseguita l'attività per una pianificazione mensile del giorno della settimana.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

**L'elemento Months** è definito dal [**tipo complesso monthlyDayOfWeekScheduleType.**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                                            | Derivato da                                                                                         | Descrizione                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek (calendarTriggerType)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Specifica un trigger che avvia un processo per una pianificazione mensile del giorno della settimana.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                               | Tipo | Descrizione                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Aprile**](taskschedulerschema-april-monthstype-element.md)         |      | Specifica che l'attività viene eseguita nel mese di aprile.<br/>     |
| [**Agosto**](taskschedulerschema-august-monthstype-element.md)       |      | Specifica che l'attività viene eseguita nel mese di agosto.<br/>    |
| [**Dicembre**](taskschedulerschema-december-monthstype-element.md)   |      | Specifica che l'attività viene eseguita nel mese di dicembre.<br/>  |
| [**Febbraio**](taskschedulerschema-february-monthstype-element.md)   |      | Specifica che l'attività viene eseguita nel mese di febbraio.<br/>  |
| [**Gennaio**](taskschedulerschema-january-monthstype-element.md)     |      | Specifica che l'attività viene eseguita nel mese di gennaio.<br/>   |
| [**Luglio**](taskschedulerschema-july-monthstype-element.md)           |      | Specifica che l'attività viene eseguita nel mese di luglio.<br/>      |
| [**Giugno**](taskschedulerschema-june-monthstype-element.md)           |      | Specifica che l'attività viene eseguita nel mese di giugno.<br/>      |
| [**Marzo**](taskschedulerschema-march-monthstype-element.md)         |      | Specifica che l'attività viene eseguita nel mese di marzo.<br/>     |
| [**Maggio**](taskschedulerschema-may-monthstype-element.md)             |      | Specifica che l'attività viene eseguita nel maggio.<br/>       |
| [**Novembre**](taskschedulerschema-november-monthstype-element.md)   |      | Specifica che l'attività viene eseguita nel mese di novembre.<br/>  |
| [**Ottobre**](taskschedulerschema-october-monthstype-element.md)     |      | Specifica che l'attività viene eseguita nel mese di ottobre.<br/>   |
| [**Settembre**](taskschedulerschema-september-monthstype-element.md) |      | Specifica che l'attività viene eseguita nel mese di settembre.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, i mesi di un anno per una pianificazione mensile del giorno della settimana vengono specificati usando la [**proprietà MonthlyDOWTrigger.MonthsOfYear.**](monthlydowtrigger-monthsofyear.md)

Per lo sviluppo in C++, i mesi di un anno per una pianificazione mensile del giorno della settimana vengono specificati usando la proprietà [**IMonthlyDOWTrigger::MonthsOfYear.**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear)

Gli elementi figlio precedenti sono definiti dal [**tipo complesso monthsType.**](taskschedulerschema-monthstype-complextype.md)

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un calendario mensile del giorno della settimana che avvia l'attività il lunedì della prima settimana per ogni mese dell'anno.


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
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





