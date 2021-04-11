---
title: Proprietà MonthlyTrigger. DaysOfMonth
description: Per gli script, ottiene o imposta i giorni del mese durante i quali viene eseguita l'attività.
ms.assetid: 4da80d0f-ae0c-4e56-b51b-6ee6ab309d7c
keywords:
- Utilità di pianificazione proprietà DaysOfMonth
- Utilità di pianificazione proprietà DaysOfMonth, oggetto MonthlyTrigger
- Oggetto MonthlyTrigger Utilità di pianificazione, proprietà DaysOfMonth
topic_type:
- apiref
api_name:
- MonthlyTrigger.DaysOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a3bd671266cfbe459218367fadf20fd52f94a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120223"
---
# <a name="monthlytriggerdaysofmonth-property"></a>Proprietà MonthlyTrigger. DaysOfMonth

Per gli script, ottiene o imposta i giorni del mese durante i quali viene eseguita l'attività.

## <a name="syntax"></a>Sintassi


```VB
MonthlyTrigger.DaysOfMonth As long
```



## <a name="property-value"></a>Valore proprietà

Maschera bit per bit che indica i giorni del mese durante i quali viene eseguita l'attività.

## <a name="remarks"></a>Commenti



| Giorno del mese | Valore hex  | Valore decimale |
|--------------|------------|---------------|
| 1            | 0x01       | 1             |
| 2            | 0x02       | 2             |
| 3            | 0x04       | 4             |
| 4            | 0x08       | 8             |
| 5            | 0x10       | 16            |
| 6            | 0x20       | 32            |
| 7            | 0x40       | 64            |
| 8            | 0x80       | 128           |
| 9            | 0x100      | 256           |
| 10           | 0x200      | 512           |
| 11           | 0x400      | 1024          |
| 12           | 0x800      | 2048          |
| 13           | 0x1000     | 4096          |
| 14           | 0x2000     | 8192          |
| 15           | 0x4000     | 16384         |
| 16           | 0x8000     | 32768         |
| 17           | 0x10000    | 65536         |
| 18           | 0x20000    | 131072        |
| 19           | 0x40000    | 262144        |
| 20           | 0x80000    | 524288        |
| 21           | 0x100000   | 1048576       |
| 22           | 0x200000   | 2097152       |
| 23           | 0x400000   | 4194304       |
| 24           | 0x800000   | 8388608       |
| 25           | 0x1000000  | 16777216      |
| 26           | 0x2000000  | 33554432      |
| 27           | 0x4000000  | 67108864      |
| 28           | 0x8000000  | 134217728     |
| 29           | 0x10000000 | 268435456     |
| 30           | 0x20000000 | 536870912     |
| 31           | 0x40000000 | 1073741824    |
| Last (Ultimo)         | 0x80000000 | 2147483648    |



 

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, i giorni del mese vengono specificati utilizzando l'elemento [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**MonthlyTrigger**](monthlytrigger.md)
</dt> </dl>

 

 





