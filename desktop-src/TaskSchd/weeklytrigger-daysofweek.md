---
title: Proprietà WeeklyTrigger. DaysOfWeek
description: Per gli script, ottiene o imposta i giorni della settimana in cui viene eseguita l'attività.
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- Utilità di pianificazione proprietà DaysOfWeek
- Utilità di pianificazione proprietà DaysOfWeek, oggetto WeeklyTrigger
- Oggetto WeeklyTrigger Utilità di pianificazione, proprietà DaysOfWeek
topic_type:
- apiref
api_name:
- WeeklyTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f0a27ef031e7baf46d2d3c0e33c23fb505c7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519254"
---
# <a name="weeklytriggerdaysofweek-property"></a>Proprietà WeeklyTrigger. DaysOfWeek

Per gli script, ottiene o imposta i giorni della settimana in cui viene eseguita l'attività.

## <a name="syntax"></a>Sintassi


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Valore proprietà

Maschera bit per bit che indica i giorni della settimana in cui viene eseguita l'attività.

## <a name="remarks"></a>Commenti

Nella tabella seguente viene illustrato il mapping della maschera bit per bit utilizzata da questa proprietà.



| Month     | Valore hex | Valore decimale |
|-----------|-----------|---------------|
| Sunday    | 0X01      | 1             |
| Monday    | 0x02      | 2             |
| Tuesday   | 0X04      | 4             |
| Wednesday | 0X08      | 8             |
| Thursday  | 0X10      | 16            |
| Friday    | 0x20      | 32            |
| Sabato  | 0X40      | 64            |



 

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, i giorni della settimana vengono specificati utilizzando l'elemento [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) dello schema utilità di pianificazione.

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
</dt> </dl>

 

 





