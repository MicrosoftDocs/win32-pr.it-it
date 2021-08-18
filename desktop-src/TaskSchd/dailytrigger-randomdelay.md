---
title: DailyTrigger.RandomDelay - proprietà
description: Per lo scripting, ottiene o imposta un tempo di ritardo aggiunto in modo casuale all'ora di inizio del trigger. | DailyTrigger.RandomDelay - proprietà
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- Proprietà RandomDelay Utilità di pianificazione
- Proprietà RandomDelay Utilità di pianificazione , oggetto DailyTrigger
- Proprietà DailyTrigger Utilità di pianificazione , RandomDelay
topic_type:
- apiref
api_name:
- DailyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc3bfec997b50a1f9d802191387a2186576532ca027e1086fc311b31f0da5d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139474"
---
# <a name="dailytriggerrandomdelay-property"></a>DailyTrigger.RandomDelay - proprietà

Per lo scripting, ottiene o imposta un tempo di ritardo aggiunto in modo casuale all'ora di inizio del trigger.

## <a name="syntax"></a>Sintassi


```VB
DailyTrigger.RandomDelay As String
```



## <a name="property-value"></a>Valore proprietà

Tempo di ritardo aggiunto in modo casuale all'ora di inizio del trigger. Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, P2DT5S è un ritardo di 2 giorni e 5 secondi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DailyTrigger**](dailytrigger.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





