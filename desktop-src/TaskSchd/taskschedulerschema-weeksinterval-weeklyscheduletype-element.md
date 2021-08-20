---
title: Elemento WeeksInterval (weeklyScheduleType)
description: Specifica l'intervallo tra le settimane nella pianificazione.
ms.assetid: 6cbf1e7e-a695-4012-97fd-fe3360c362c4
keywords:
- Elemento WeeksInterval Utilità di pianificazione
topic_type:
- apiref
api_name:
- WeeksInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c59e4f4b163e5e96418c84bf2925e45cf3a54da1bbb50e17ad9282409438ff3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059759"
---
# <a name="weeksinterval-weeklyscheduletype-element"></a>Elemento WeeksInterval (weeklyScheduleType)

Specifica l'intervallo tra le settimane nella pianificazione.

``` syntax
<xs:element name="WeeksInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="52"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento è definito dal tipo complesso [**weeklyScheduleType.**](taskschedulerschema-weeklyscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                  | Derivato da                                                                     | Descrizione                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) | Specifica una pianificazione settimanale.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, l'intervallo settimanale viene specificato usando la [**proprietà WeeklyTrigger.WeeksInterval.**](weeklytrigger-weeksinterval.md)

Per lo sviluppo C++, l'intervallo settimanale viene specificato usando la [**proprietà IWeeklyTrigger::WeeksInterval.**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval)

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un trigger di calendario settimanale che avvia un'attività dal lunedì al venerdì (alle 8:00) ogni settimana.


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

 

 





