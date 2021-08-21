---
title: TimeTrigger.RandomDelay - proprietà
description: Per lo scripting, ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger. | TimeTrigger.RandomDelay - proprietà
ms.assetid: ee55dd85-9696-4872-8670-f919fca7481d
keywords:
- Proprietà RandomDelay Utilità di pianificazione
- Proprietà RandomDelay Utilità di pianificazione , oggetto TimeTrigger
- Oggetto TimeTrigger Utilità di pianificazione, proprietà RandomDelay
topic_type:
- apiref
api_name:
- TimeTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdbe297ace4fd34c2b5bf88db132e0573afd208052b50331ab571881b85831f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354763"
---
# <a name="timetriggerrandomdelay-property"></a>TimeTrigger.RandomDelay - proprietà

Per lo scripting, ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.

## <a name="syntax"></a>Sintassi


```VB
TimeTrigger.RandomDelay As String
```



## <a name="property-value"></a>Valore proprietà

Tempo di ritardo aggiunto in modo casuale all'ora di inizio del trigger. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





