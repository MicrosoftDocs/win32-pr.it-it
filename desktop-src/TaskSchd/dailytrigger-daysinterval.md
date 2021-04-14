---
title: Proprietà DailyTrigger. DaysInterval
description: Per gli script, ottiene o imposta l'intervallo tra i giorni della pianificazione.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- Utilità di pianificazione proprietà DaysInterval
- Utilità di pianificazione proprietà DaysInterval, oggetto DailyTrigger
- Oggetto DailyTrigger Utilità di pianificazione, proprietà DaysInterval
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6499f3b900fe10b2a2527c2e2ee675cca3151204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517914"
---
# <a name="dailytriggerdaysinterval-property"></a>Proprietà DailyTrigger. DaysInterval

Per gli script, ottiene o imposta l'intervallo tra i giorni della pianificazione.

## <a name="syntax"></a>Sintassi


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a>Valore proprietà

Intervallo tra i giorni della pianificazione.

## <a name="remarks"></a>Commenti

Un intervallo di 1 produce una pianificazione giornaliera. Un intervallo di 2 produce una pianificazione di ogni giorno.

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, l'intervallo per una pianificazione giornaliera viene specificato mediante l'elemento [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) dello schema utilità di pianificazione.

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

[**DailyTrigger**](dailytrigger.md)
</dt> </dl>

 

 





