---
title: Months (monthlyDayOfWeekScheduleType)-elemento
description: Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Utilità di pianificazione dell'elemento months
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76f13a5823e0154519dbdb093dd03ea36bbe77b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400406"
---
# <a name="months-monthlydayofweekscheduletype-element"></a>Months (monthlyDayOfWeekScheduleType)-elemento

Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

L'elemento **months** viene definito dal tipo complesso [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                                            | Derivato da                                                                                         | Descrizione                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek (calendarTriggerType)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Specifica un trigger che avvia un processo per una pianificazione mensile del giorno della settimana.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                               | Tipo | Descrizione                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Aprile**](taskschedulerschema-april-monthstype-element.md)         |      | Specifica che l'attività viene eseguita nell'aprile.<br/>     |
| [**Agosto**](taskschedulerschema-august-monthstype-element.md)       |      | Specifica che l'attività viene eseguita nell'agosto.<br/>    |
| [**Dicembre**](taskschedulerschema-december-monthstype-element.md)   |      | Specifica che l'attività viene eseguita nel dicembre.<br/>  |
| [**Febbraio**](taskschedulerschema-february-monthstype-element.md)   |      | Specifica che l'attività viene eseguita nel febbraio.<br/>  |
| [**Gennaio**](taskschedulerschema-january-monthstype-element.md)     |      | Specifica che l'attività viene eseguita nel gennaio.<br/>   |
| [**Luglio**](taskschedulerschema-july-monthstype-element.md)           |      | Specifica che l'attività viene eseguita nel luglio.<br/>      |
| [**Giugno**](taskschedulerschema-june-monthstype-element.md)           |      | Specifica che l'attività viene eseguita in giugno.<br/>      |
| [**Marzo**](taskschedulerschema-march-monthstype-element.md)         |      | Specifica che l'attività viene eseguita nel marzo.<br/>     |
| [**Mag**](taskschedulerschema-may-monthstype-element.md)             |      | Specifica che l'attività viene eseguita in May.<br/>       |
| [**Novembre**](taskschedulerschema-november-monthstype-element.md)   |      | Specifica che l'attività viene eseguita nel novembre.<br/>  |
| [**Ottobre**](taskschedulerschema-october-monthstype-element.md)     |      | Specifica che l'attività viene eseguita nel ottobre.<br/>   |
| [**Settembre**](taskschedulerschema-september-monthstype-element.md) |      | Specifica che l'attività viene eseguita nel settembre.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, i mesi di un anno per una pianificazione giornaliera giornaliera della settimana vengono specificati utilizzando la proprietà [**MonthlyDOWTrigger. MonthsOfYear**](monthlydowtrigger-monthsofyear.md) .

Per lo sviluppo in C++, i mesi di un anno per una pianificazione giornaliera giornaliera della settimana vengono specificati utilizzando la proprietà [**IMonthlyDOWTrigger:: MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) .

Gli elementi figlio precedenti sono definiti dal tipo complesso [**monthsType**](taskschedulerschema-monthstype-complextype.md) .

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

 

 





