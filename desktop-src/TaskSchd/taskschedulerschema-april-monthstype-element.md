---
title: Elemento April (monthsType)
description: Specifica che l'attività viene eseguita nel mese di aprile.
ms.assetid: b642e142-0acc-4b88-a86a-5d539613ead6
keywords:
- Elemento aprile Utilità di pianificazione
topic_type:
- apiref
api_name:
- April
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f717e015c320c03b6d41e4c17d04cf3a255f85eb150a3f292933c370a516ae8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125881"
---
# <a name="april-monthstype-element"></a>Elemento April (monthsType)

Specifica che l'attività viene eseguita nel mese di aprile.

``` syntax
<xs:element name="April">
    <xs:complexType />
</xs:element>
```

**L'elemento** April è definito dal [**tipo complesso monthsType.**](taskschedulerschema-monthstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                          | Derivato da                                                     | Descrizione                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.<br/>             |
| [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Specifica i mesi dell'anno durante i quali viene eseguita l'attività per una pianificazione mensile del giorno della settimana.<br/> |



## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un calendario dei mesi che esegue l'attività nel mese di aprile.


```XML
<Months>
    <April/>
</Months>
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

 

 





