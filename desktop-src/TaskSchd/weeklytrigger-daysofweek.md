---
title: WeeklyTrigger.DaysOfWeek - proprietà
description: Per lo scripting, ottiene o imposta i giorni della settimana in cui viene eseguita l'attività.
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- Proprietà DaysOfWeek Utilità di pianificazione
- Proprietà DaysOfWeek Utilità di pianificazione, oggetto WeeklyTrigger
- Proprietà WeeklyTrigger Utilità di pianificazione , DaysOfWeek
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
ms.openlocfilehash: 7298982dcd10078d9e8460459d38cfa77140d15607341460f0e0edec998306f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001794"
---
# <a name="weeklytriggerdaysofweek-property"></a>WeeklyTrigger.DaysOfWeek - proprietà

Per lo scripting, ottiene o imposta i giorni della settimana in cui viene eseguita l'attività.

## <a name="syntax"></a>Sintassi


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Valore proprietà

Maschera bit per bit che indica i giorni della settimana in cui viene eseguita l'attività.

## <a name="remarks"></a>Commenti

Nella tabella seguente viene illustrato il mapping della maschera bit per bit usata da questa proprietà.



| Month     | Valore hex | Valore decimale |
|-----------|-----------|---------------|
| Sunday    | 0X01      | 1             |
| Monday    | 0x02      | 2             |
| Tuesday   | 0X04      | 4             |
| Wednesday | 0X08      | 8             |
| Thursday  | 0X10      | 16            |
| Friday    | 0x20      | 32            |
| Sabato  | 0X40      | 64            |



 

Quando si legge o si scrive codice XML personalizzato per un'attività, i giorni della settimana vengono specificati usando l'elemento [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) dello schema Utilità di pianificazione dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





