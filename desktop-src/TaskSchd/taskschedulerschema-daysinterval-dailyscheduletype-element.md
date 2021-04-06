---
title: Elemento DaysInterval (dailyScheduleType)
description: Specifica l'intervallo tra i giorni della pianificazione.
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- Utilità di pianificazione elemento DaysInterval
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97b50581aa4825b31983a234a5eb47ff7b7b7e06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963863"
---
# <a name="daysinterval-dailyscheduletype-element"></a>Elemento DaysInterval (dailyScheduleType)

Specifica l'intervallo tra i giorni della pianificazione.

``` syntax
<xs:element name="DaysInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedInt"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="365"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento è definito dal tipo complesso [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                | Derivato da                                                                   | Descrizione                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) | Specifica una pianificazione giornaliera.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, l'intervallo di giorni per un trigger giornaliero viene specificato dalla proprietà [**DailyTrigger. DaysInterval**](dailytrigger-daysinterval.md) .

Per lo sviluppo in C++, l'intervallo di giorni per un trigger giornaliero viene specificato dalla proprietà [**IDailyTrigger::D aysinterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) .

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un trigger di calendario giornaliero che avvia l'attività ogni giorno.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



Per un esempio completo del codice XML per un'attività che specifica una pianificazione giornaliera, vedere [esempio di trigger giornalieri (XML)](daily-trigger-example--xml-.md).

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

 

 





