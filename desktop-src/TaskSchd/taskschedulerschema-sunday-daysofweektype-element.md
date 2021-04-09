---
title: Elemento Sunday (daysOfWeekType)
description: Specifica che l'attività viene eseguita la domenica.
ms.assetid: 856db869-2273-4bb8-88c8-c126bb16c87b
keywords:
- Utilità di pianificazione dell'elemento Sunday
topic_type:
- apiref
api_name:
- Sunday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40efba31b392da5959853feeb1cae567cee25cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120886"
---
# <a name="sunday-daysofweektype-element"></a>Elemento Sunday (daysOfWeekType)

Specifica che l'attività viene eseguita la domenica.

``` syntax
<xs:element name="Sunday">
    <xs:complexType />
</xs:element>
```

L'elemento **Sunday** è definito dal tipo complesso [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                                  | Derivato da                                                             | Descrizione                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione mensile giornaliera della settimana.<br/> |
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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





