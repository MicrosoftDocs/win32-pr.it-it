---
title: Elemento Tuesday (daysOfWeekType)
description: Specifica che l'attività viene eseguita il martedì.
ms.assetid: 588608e9-33f9-405d-8b4b-35f11ab403db
keywords:
- Elemento Tuesday Utilità di pianificazione
topic_type:
- apiref
api_name:
- Tuesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524d5dbe6b0deb1636fd06281d81b641665609310ad10a8b407da2dc570876ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355614"
---
# <a name="tuesday-daysofweektype-element"></a>Elemento Tuesday (daysOfWeekType)

Specifica che l'attività viene eseguita il martedì.

``` syntax
<xs:element name="Tuesday">
    <xs:complexType />
</xs:element>
```

**L'elemento** Tuesday è definito dal [**tipo complesso daysOfWeekType.**](taskschedulerschema-daysofweektype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                                  | Derivato da                                                             | Descrizione                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione mensile del giorno della settimana.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione settimanale.<br/>              |



## <a name="examples"></a>Esempio

Il codice XML seguente definisce un calendario del giorno della settimana che avvia un'attività il martedì.


```XML
<DaysOfWeek>
    <Tuesday/>
</DaysOfWeek>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





