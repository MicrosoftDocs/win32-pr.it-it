---
title: Elemento DaysOfMonth (monthlyScheduleType)
description: Specifica i giorni del mese durante i quali viene eseguita l'attività.
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- Utilità di pianificazione elemento DaysOfMonth
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38c2106f8d612ee27dc1297023a59b531fa9548d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302698"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a>Elemento DaysOfMonth (monthlyScheduleType)

Specifica i giorni del mese durante i quali viene eseguita l'attività.

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

L'elemento **DaysOfMonth** è definito dal tipo complesso [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                    | Derivato da                                                                                         | Descrizione                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Specifica un trigger che avvia un processo per una pianificazione mensile del giorno della settimana.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                        | Tipo                                                                    | Descrizione                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**Giorno**](taskschedulerschema-day-daysofmonthtype-element.md) | [**dayOfMonthType**](taskschedulerschema-dayofmonthtype-simpletype.md) | Specifica un giorno del mese durante il quale viene eseguita l'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, i giorni del mese per la pianificazione vengono specificati utilizzando la proprietà [**MonthlyTrigger. DaysOfMonth**](monthlytrigger-daysofmonth.md) .

Per lo sviluppo in C++, i giorni del mese per la pianificazione vengono specificati usando la proprietà [**IMonthlyTrigger::D aysofmonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) .

L'elemento figlio deve essere ripetuto per ogni giorno del mese in cui l'attività deve essere eseguita.

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un trigger di calendario mensile che avvia un'attività (alle 8:30 AM) il primo giorno di ogni mese.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>  
        </DaysOfMonth>
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
    </ScheduleByMonth>
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

 

 





