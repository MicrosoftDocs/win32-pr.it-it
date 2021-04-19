---
title: Elemento week (weeksType)
description: Specifica una settimana specifica del mese.
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Utilità di pianificazione dell'elemento week
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0487aa07e1f1132c998b6cb2ba0f518a9db57ce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302483"
---
# <a name="week-weekstype-element"></a>Elemento week (weeksType)

Specifica una settimana specifica del mese.

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

L'elemento **week** è definito dal tipo complesso [**weeksType**](taskschedulerschema-weekstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                                        | Derivato da                                                   | Descrizione                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [**Settimane (monthlyDayOfWeekScheduleType)**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [**weeksType**](taskschedulerschema-weekstype-complextype.md) | Specifica le settimane del mese in cui viene eseguita l'attività.<br/> |



## <a name="remarks"></a>Commenti

Quando si specificano le settimane del mese, utilizzare i numeri 1-4 per le prime quattro settimane del mese oppure utilizzare la stringa "ultimo" per indicare l'ultima settimana del mese.

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

 

 





