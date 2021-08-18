---
title: WeeklyTrigger.RandomDelay - proprietà
description: Per lo scripting, ottiene o imposta un tempo di ritardo aggiunto in modo casuale all'ora di inizio del trigger. | WeeklyTrigger.RandomDelay - proprietà
ms.assetid: 711b188d-b283-4c99-b43d-644f39a31cdc
keywords:
- Proprietà RandomDelay Utilità di pianificazione
- Proprietà RandomDelay Utilità di pianificazione, oggetto WeeklyTrigger
- Proprietà WeeklyTrigger Utilità di pianificazione , RandomDelay
topic_type:
- apiref
api_name:
- WeeklyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc17260b33b4f5ca833ae0f2e322a99205b690ad8d54779ea6471db246cc056b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001779"
---
# <a name="weeklytriggerrandomdelay-property"></a>WeeklyTrigger.RandomDelay - proprietà

Per lo scripting, ottiene o imposta un tempo di ritardo aggiunto in modo casuale all'ora di inizio del trigger.

## <a name="syntax"></a>Sintassi


```VB
WeeklyTrigger.RandomDelay As String
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



 

 





