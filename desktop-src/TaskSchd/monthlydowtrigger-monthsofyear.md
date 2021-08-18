---
title: MonthlyDOWTrigger.MonthsOfYear - proprietà
description: Per lo scripting, ottiene o imposta i mesi dell'anno durante i quali viene eseguita l'attività. | MonthlyDOWTrigger.MonthsOfYear - proprietà
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- Proprietà MonthsOfYear Utilità di pianificazione
- Proprietà MonthsOfYear Utilità di pianificazione , oggetto MonthlyDOWTrigger
- Oggetto MonthlyDOWTrigger Utilità di pianificazione proprietà , MonthsOfYear
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
ms.openlocfilehash: 7f8dc9752cf241218a95a9816824bc6ccf560f47c3445df9e5f40406381de3b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253821"
---
# <a name="monthlydowtriggermonthsofyear-property"></a>MonthlyDOWTrigger.MonthsOfYear - proprietà

Per lo scripting, ottiene o imposta i mesi dell'anno durante i quali viene eseguita l'attività.

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



 

Durante la lettura o la scrittura di codice XML per un'attività, i mesi dell'anno di un calendario mensile del giorno della settimana vengono specificati dall'elemento [**Months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) dello schema Utilità di pianificazione dati.

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

 

 





