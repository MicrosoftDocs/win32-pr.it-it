---
title: Proprietà MonthlyDOWTrigger. MonthsOfYear
description: Per gli script, ottiene o imposta i mesi dell'anno durante i quali viene eseguita l'attività. | Proprietà MonthlyDOWTrigger. MonthsOfYear
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- Utilità di pianificazione Proprietà MonthsOfYear
- Utilità di pianificazione Proprietà MonthsOfYear, oggetto MonthlyDOWTrigger
- Oggetto MonthlyDOWTrigger Utilità di pianificazione, Proprietà MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c345cd3de12d7dba3450f62bdb18bfdcee496b13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886217"
---
# <a name="monthlydowtriggermonthsofyear-property"></a>Proprietà MonthlyDOWTrigger. MonthsOfYear

Per gli script, ottiene o imposta i mesi dell'anno durante i quali viene eseguita l'attività.

## <a name="syntax"></a>Sintassi


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a>Valore proprietà

Maschera bit per bit che indica i mesi dell'anno durante i quali viene eseguita l'attività.

## <a name="remarks"></a>Commenti

Nella tabella seguente viene illustrato il mapping della maschera bit per bit utilizzata da questa proprietà.



| Month     | Valore hex | Valore decimale |
|-----------|-----------|---------------|
| January   | 0X01      | 1             |
| Febbraio  | 0x02      | 2             |
| Marzo     | 0X04      | 4             |
| April     | 0X08      | 8             |
| Mag       | 0X10      | 16            |
| Giugno      | 0X20      | 32            |
| Luglio      | 0x40      | 64            |
| Agosto    | 0X80      | 128           |
| Settembre | 0X100     | 256           |
| Ottobre   | 0X200     | 512           |
| Novembre  | 0X400     | 1024          |
| Dicembre  | 0X800     | 2048          |



 

Durante la lettura o la scrittura di codice XML per un'attività, i mesi dell'anno di un calendario giornaliero settimanale sono specificati dall'elemento [**months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) dello schema utilità di pianificazione.

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

 

 





