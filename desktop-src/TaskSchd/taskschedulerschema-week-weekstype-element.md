---
title: Elemento Week (weeksType)
description: Specifica una settimana specifica del mese.
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Elemento Week Utilità di pianificazione
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a999eaa5ec7d4ed36b86fc292f4c0d5e8c474fd1df8f5f4b9da5b90f2dcca641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758207"
---
# <a name="week-weekstype-element"></a>Elemento Week (weeksType)

Specifica una settimana specifica del mese.

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

**L'elemento Week** è definito dal [**tipo complesso weeksType.**](taskschedulerschema-weekstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                        | Derivato da                                                   | Descrizione                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [**Weeks (monthlyDayOfWeekScheduleType)**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [**weeksType**](taskschedulerschema-weekstype-complextype.md) | Specifica le settimane del mese in cui viene eseguita l'attività.<br/> |



## <a name="remarks"></a>Commenti

Quando si specificano le settimane del mese, usare i numeri da 1 a 4 per le prime quattro settimane del mese oppure usare la stringa "Last" per indicare l'ultima settimana del mese.

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

 

 





