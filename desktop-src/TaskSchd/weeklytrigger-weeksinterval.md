---
title: Proprietà WeeklyTrigger. WeeksInterval
description: Per lo scripting, ottiene o imposta l'intervallo tra le settimane nella pianificazione.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- Utilità di pianificazione proprietà WeeksInterval
- Utilità di pianificazione proprietà WeeksInterval, oggetto WeeklyTrigger
- Oggetto WeeklyTrigger Utilità di pianificazione, proprietà WeeksInterval
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4668b68d0b3f83e096284db35df799a63eb677b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301137"
---
# <a name="weeklytriggerweeksinterval-property"></a>Proprietà WeeklyTrigger. WeeksInterval

Per lo scripting, ottiene o imposta l'intervallo tra le settimane nella pianificazione.

## <a name="syntax"></a>Sintassi


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a>Valore proprietà

Intervallo tra le settimane nella pianificazione.

## <a name="remarks"></a>Commenti

Un intervallo di 1 produce una pianificazione settimanale. Un intervallo di 2 produce una pianificazione di ogni settimana.

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, l'intervallo per una pianificazione settimanale viene specificato utilizzando l'elemento [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) dello schema utilità di pianificazione.

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

 

 





