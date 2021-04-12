---
title: Proprietà MonthlyDOWTrigger. DaysOfWeek
description: Per gli script, ottiene o imposta i giorni della settimana durante i quali viene eseguita l'attività.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- Utilità di pianificazione proprietà DaysOfWeek
- Utilità di pianificazione proprietà DaysOfWeek, oggetto MonthlyDOWTrigger
- Oggetto MonthlyDOWTrigger Utilità di pianificazione, proprietà DaysOfWeek
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
ms.openlocfilehash: 15344650dabdec2bcbacf91397b37b97ce3f0772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478418"
---
# <a name="monthlydowtriggerdaysofweek-property"></a>Proprietà MonthlyDOWTrigger. DaysOfWeek

Per gli script, ottiene o imposta i giorni della settimana durante i quali viene eseguita l'attività.

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



 

Durante la lettura o la scrittura di codice XML per un'attività, i giorni della settimana di un calendario giornaliero settimanale sono specificati dall'elemento [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





