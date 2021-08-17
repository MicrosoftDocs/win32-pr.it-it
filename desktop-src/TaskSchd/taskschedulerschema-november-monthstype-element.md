---
title: Elemento November (monthsType)
description: Specifica che l'attività viene eseguita nel mese di novembre.
ms.assetid: 45f8c47b-3884-4f18-8275-f29f82ee32e2
keywords:
- Elemento november Utilità di pianificazione
topic_type:
- apiref
api_name:
- November
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 170fa1cef23fb992b651ab4675fb3f782df10a347fcff52c865b7774039cac03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758407"
---
# <a name="november-monthstype-element"></a>Elemento November (monthsType)

Specifica che l'attività viene eseguita nel mese di novembre.

``` syntax
<xs:element name="November">
    <xs:complexType />
</xs:element>
```

**L'elemento** November è definito dal [**tipo complesso monthsType.**](taskschedulerschema-monthstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                          | Derivato da                                                     | Descrizione                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.<br/> |
| [**Mesi (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.<br/>             |



## <a name="examples"></a>Esempio

Il codice XML seguente definisce un calendario di mesi che esegue l'attività nel mese di novembre.


```XML
<Months>
    <November/>
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

 

 





