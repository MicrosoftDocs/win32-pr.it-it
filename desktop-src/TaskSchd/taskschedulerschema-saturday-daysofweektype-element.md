---
title: Elemento Saturday (daysOfWeekType)
description: Specifica che l'attività viene eseguita il sabato.
ms.assetid: def26a72-c143-466a-b5b0-6105078afffa
keywords:
- Elemento Saturday Utilità di pianificazione
topic_type:
- apiref
api_name:
- Saturday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0592d4f5f005afa1136d06261b05d4d4a942ac490140d384bb9174555b49c253
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099901"
---
# <a name="saturday-daysofweektype-element"></a>Elemento Saturday (daysOfWeekType)

Specifica che l'attività viene eseguita il sabato.

``` syntax
<xs:element name="Saturday">
    <xs:complexType />
</xs:element>
```

**L'elemento Saturday** è definito dal [**tipo complesso daysOfWeekType.**](taskschedulerschema-daysofweektype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                                  | Derivato da                                                             | Descrizione                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione mensile del giorno della settimana.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione settimanale.<br/>              |



## <a name="examples"></a>Esempio

Il codice XML seguente definisce un calendario del giorno della settimana che avvia un'attività il sabato.


```XML
<DaysOfWeek>
    <Saturday/>
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

 

 





