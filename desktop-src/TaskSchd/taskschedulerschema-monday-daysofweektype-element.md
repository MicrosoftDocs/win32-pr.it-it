---
title: Elemento Monday (daysOfWeekType)
description: Specifica che l'attività viene eseguita il lunedì.
ms.assetid: 2b7ce0c1-c635-47d0-b482-5c93c0028c92
keywords:
- Elemento Monday Utilità di pianificazione
topic_type:
- apiref
api_name:
- Monday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 22bd1028a36efa6e2fe96a300b221073dbf87f14e77621d8b1591f85c7f6fd6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513931"
---
# <a name="monday-daysofweektype-element"></a>Elemento Monday (daysOfWeekType)

Specifica che l'attività viene eseguita il lunedì.

``` syntax
<xs:element name="Monday">
    <xs:complexType />
</xs:element>
```

**L'elemento** Monday è definito dal [**tipo complesso weeklyScheduleType.**](taskschedulerschema-weeklyscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                                  | Derivato da                                                             | Descrizione                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione mensile del giorno della settimana.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione settimanale.<br/>              |



## <a name="examples"></a>Esempio

Il codice XML seguente definisce un calendario del giorno della settimana che avvia un'attività il lunedì.


```XML
<DaysOfWeek>
    <Monday/>
</DaysOfWeek>
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

 

 





