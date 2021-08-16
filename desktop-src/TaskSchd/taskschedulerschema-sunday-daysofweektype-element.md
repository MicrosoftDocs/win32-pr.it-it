---
title: Elemento Sunday (daysOfWeekType)
description: Specifica che l'attività viene eseguita la domenica.
ms.assetid: 856db869-2273-4bb8-88c8-c126bb16c87b
keywords:
- Elemento Sunday Utilità di pianificazione
topic_type:
- apiref
api_name:
- Sunday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25a184d16d5239f2294f02ddb6144fa4b886d1f83e11cbbd6e481f7fda77e1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356262"
---
# <a name="sunday-daysofweektype-element"></a>Elemento Sunday (daysOfWeekType)

Specifica che l'attività viene eseguita la domenica.

``` syntax
<xs:element name="Sunday">
    <xs:complexType />
</xs:element>
```

**L'elemento** Sunday è definito dal [**tipo complesso daysOfWeekType.**](taskschedulerschema-daysofweektype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                                  | Derivato da                                                             | Descrizione                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione mensile del giorno della settimana.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione settimanale.<br/>              |



## <a name="examples"></a>Esempio

Il codice XML seguente definisce un calendario del giorno della settimana che avvia un'attività la domenica.


```XML
<DaysOfWeek>
    <Sunday/>
</DaysOfWeek>
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

 

 





