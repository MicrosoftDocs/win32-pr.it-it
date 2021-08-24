---
title: MonthlyDOWTrigger.DaysOfWeek - proprietà
description: Per lo scripting, ottiene o imposta i giorni della settimana durante i quali viene eseguita l'attività.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- Proprietà DaysOfWeek Utilità di pianificazione
- Proprietà DaysOfWeek Utilità di pianificazione, oggetto MonthlyDOWTrigger
- Oggetto MonthlyDOWTrigger Utilità di pianificazione proprietà DaysOfWeek
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b9abf5dcd33c92d402f8ed6047a2fd80a0d5905bae075110931cfb8f83aa10a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517461"
---
# <a name="monthlydowtriggerdaysofweek-property"></a>MonthlyDOWTrigger.DaysOfWeek - proprietà

Per lo scripting, ottiene o imposta i giorni della settimana durante i quali viene eseguita l'attività.

## <a name="syntax"></a>Sintassi


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Valore proprietà

Maschera bit per bit che indica i giorni della settimana durante i quali viene eseguita l'attività.

## <a name="remarks"></a>Commenti

Nella tabella seguente viene illustrato il mapping della maschera bit per bit utilizzata da questa proprietà.



| Giorno della settimana | Valore esadecimale | Valore decimale |
|-------------|-----------|---------------|
| Sunday      | 0x01      | 1             |
| Monday      | 0x02      | 2             |
| Tuesday     | 0x04      | 4             |
| Wednesday   | 0x08      | 8             |
| Thursday    | 0x10      | 16            |
| Friday      | 0x20      | 32            |
| Sabato    | 0x40      | 64            |



 

Durante la lettura o la scrittura di codice XML per un'attività, i giorni della settimana di un calendario mensile del giorno della settimana vengono specificati [**dall'elemento DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





