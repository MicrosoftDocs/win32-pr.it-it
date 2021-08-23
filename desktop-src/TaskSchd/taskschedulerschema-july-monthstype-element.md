---
title: Elemento July (monthsType)
description: Specifica che l'attività viene eseguita nel mese di luglio.
ms.assetid: 6fcb06f1-0806-469c-a283-ba8f2ba2c256
keywords:
- Elemento July Utilità di pianificazione
topic_type:
- apiref
api_name:
- July
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e62ad0f04dcf8ec12d31ddc5ff6372896fd49442689cae7cdc82810b19a9138
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575221"
---
# <a name="july-monthstype-element"></a>Elemento July (monthsType)

Specifica che l'attività viene eseguita nel mese di luglio.

``` syntax
<xs:element name="July">
    <xs:complexType />
</xs:element>
```

**L'elemento** july è definito dal [**tipo complesso monthsType.**](taskschedulerschema-monthstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                          | Derivato da                                                     | Descrizione                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Specifica i mesi dell'anno durante i quali viene eseguita l'attività per una pianificazione mensile del giorno della settimana.<br/> |
| [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.<br/>             |



## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un calendario dei mesi che esegue l'attività nel mese di luglio.


```XML
<Months>
    <July/>
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

 

 





