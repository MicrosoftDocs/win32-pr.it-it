---
title: DailyTrigger.DaysInterval - proprietà
description: Per lo scripting, ottiene o imposta l'intervallo tra i giorni nella pianificazione.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- Proprietà DaysInterval Utilità di pianificazione
- Proprietà DaysInterval Utilità di pianificazione , oggetto DailyTrigger
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
ms.openlocfilehash: d4355e6c2a26b197224141018fa5a1d85e7d31e211ac47dc84a9e8c9ef3750fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139494"
---
# <a name="dailytriggerdaysinterval-property"></a>DailyTrigger.DaysInterval - proprietà

Per lo scripting, ottiene o imposta l'intervallo tra i giorni nella pianificazione.

## <a name="syntax"></a>Sintassi


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a>Valore proprietà

Intervallo tra i giorni nella pianificazione.

## <a name="remarks"></a>Commenti

Un intervallo di 1 produce una pianificazione giornaliera. Un intervallo di 2 produce una pianificazione ogni due giorni.

Durante la lettura o la scrittura di codice XML personalizzato per un'attività, l'intervallo per una pianificazione giornaliera viene specificato usando [**l'elemento DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) dello schema Utilità di pianificazione dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**DailyTrigger**](dailytrigger.md)
</dt> </dl>

 

 





