---
title: Elemento ScheduleByMonth (calendarTriggerType)
description: Specifica una pianificazione mensile.
ms.assetid: 3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8
keywords:
- Utilità di pianificazione elemento ScheduleByMonth
topic_type:
- apiref
api_name:
- ScheduleByMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6fda84a1cd4373f7988fa66a5ad70c97dd371d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120891"
---
# <a name="schedulebymonth-calendartriggertype-element"></a>Elemento ScheduleByMonth (calendarTriggerType)

Specifica una pianificazione mensile. Ad esempio, l'attività inizia alle 8:00 in giorni specifici del mese per mesi specifici.

``` syntax
<xs:element name="ScheduleByMonth"
    type="monthlyScheduleType"
 />
```

L'elemento **ScheduleByMonth** è definito dal tipo complesso [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                             | Derivato da                                                                       | Descrizione                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                  | Tipo                                                                       | Descrizione                                                             |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | Specifica i giorni del mese durante i quali viene eseguita l'attività.<br/>  |
| [**Mesi (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)           | [**monthsType**](taskschedulerschema-monthstype-complextype.md)           | Specifica i mesi dell'anno durante i quali viene eseguita l'attività.<br/> |



## <a name="remarks"></a>Commenti

L'ora del giorno in cui l'attività viene avviata viene impostata dall'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .

Per lo sviluppo di script, viene specificato un trigger mensile usando l'oggetto [**MonthlyTrigger**](monthlytrigger.md) .

Per lo sviluppo in C++, viene specificato un trigger mensile usando l'interfaccia [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) .

Gli elementi figlio elencati di seguito sono definiti dai tipi di elemento complessi [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un trigger di calendario mensile che avvia un'attività (alle 8:00 AM) il primo e il quindicesimo giorno di ogni mese dell'anno.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>
            <Day>15</Day>
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
        </Months>
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

 

 





