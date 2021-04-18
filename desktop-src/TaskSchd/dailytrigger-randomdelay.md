---
title: Proprietà DailyTrigger. RandomDelay
description: Per gli script, ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger. | Proprietà DailyTrigger. RandomDelay
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- Utilità di pianificazione proprietà RandomDelay
- Utilità di pianificazione proprietà RandomDelay, oggetto DailyTrigger
- Oggetto DailyTrigger Utilità di pianificazione, proprietà RandomDelay
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
ms.openlocfilehash: bd24fc5bd97a51cc0276e0fdfe800c0a9baa022a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321736"
---
# <a name="dailytriggerrandomdelay-property"></a>Proprietà DailyTrigger. RandomDelay

Per gli script, ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.

## <a name="syntax"></a>Sintassi


```VB
DailyTrigger.RandomDelay As String
```



## <a name="property-value"></a>Valore proprietà

Tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger. Il formato di questa stringa è P <days> DT <hours> H <minutes> M <seconds> S (ad esempio, P2DT5S è un ritardo di 2 giorni e 5 secondi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DailyTrigger**](dailytrigger.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





