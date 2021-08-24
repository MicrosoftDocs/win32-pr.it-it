---
title: MonthlyDOWTrigger.WeeksOfMonth - proprietà
description: Per lo scripting, ottiene o imposta le settimane del mese durante le quali viene eseguita l'attività.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- Proprietà WeeksOfMonth Utilità di pianificazione
- Proprietà WeeksOfMonth Utilità di pianificazione, oggetto MonthlyDOWTrigger
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
ms.openlocfilehash: 323ee8b93411d7ef176fa9dc2ffb3a4acfd1f902c0dc481fe48e07b82821227b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517441"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a>MonthlyDOWTrigger.WeeksOfMonth - proprietà

Per lo scripting, ottiene o imposta le settimane del mese durante le quali viene eseguita l'attività.

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



 

Durante la lettura o la scrittura di codice XML per un'attività, i giorni della settimana di un calendario mensile del giorno della settimana vengono specificati [**dall'elemento Weeks.**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)

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

 

 





