---
title: Elemento June (monthsType)
description: Specifica che l'attività viene eseguita nel mese di giugno.
ms.assetid: 15b0e8c2-4dc1-4ca3-99c5-bd9a36718904
keywords:
- Elemento June Utilità di pianificazione
topic_type:
- apiref
api_name:
- June
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0675c0fb7c399b5d3decadf651a10793c163aeb75cad752e9e2fc0fdc251ba9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072471"
---
# <a name="june-monthstype-element"></a>Elemento June (monthsType)

Specifica che l'attività viene eseguita nel mese di giugno.

``` syntax
<xs:element name="June">
    <xs:complexType />
</xs:element>
```

**L'elemento** June è definito dal [**tipo complesso monthsType.**](taskschedulerschema-monthstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                          | Derivato da                                                     | Descrizione                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Specifica i mesi dell'anno durante i quali viene eseguita l'attività per una pianificazione mensile del giorno della settimana.<br/> |
| [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.<br/>             |



## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un calendario dei mesi che esegue l'attività nel mese di giugno.


```XML
<Months>
    <June/>
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

 

 





