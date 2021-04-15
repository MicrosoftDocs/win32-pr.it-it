---
title: Proprietà MonthlyDOWTrigger. WeeksOfMonth
description: Per gli script, ottiene o imposta le settimane del mese durante le quali viene eseguita l'attività.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- Utilità di pianificazione proprietà WeeksOfMonth
- Utilità di pianificazione proprietà WeeksOfMonth, oggetto MonthlyDOWTrigger
- Oggetto MonthlyDOWTrigger Utilità di pianificazione, proprietà WeeksOfMonth
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7efea628e6eefdef07bdc50b9719a7c404f78bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475808"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a>Proprietà MonthlyDOWTrigger. WeeksOfMonth

Per gli script, ottiene o imposta le settimane del mese durante le quali viene eseguita l'attività.

## <a name="syntax"></a>Sintassi


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a>Valore proprietà

Maschera bit per bit che indica i giorni della settimana durante i quali viene eseguita l'attività.

## <a name="remarks"></a>Commenti

Nella tabella seguente viene illustrato il mapping della maschera bit per bit utilizzata da questa proprietà.



| Settimana                     | Valore esadecimale | Valore decimale |
|--------------------------|-----------|---------------|
| Prima settimana del mese  | 0X01      | 1             |
| Seconda settimana del mese | 0x02      | 2             |
| Terza settimana del mese  | 0X04      | 4             |
| Quarta settimana del mese | 0X08      | 8             |



 

Durante la lettura o la scrittura di codice XML per un'attività, i giorni della settimana di un calendario giornaliero settimanale sono specificati dall'elemento [**weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) .

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

 

 





