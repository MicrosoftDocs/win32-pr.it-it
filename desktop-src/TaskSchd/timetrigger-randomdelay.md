---
title: Proprietà TimeTrigger. RandomDelay
description: Per gli script, ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger. | Proprietà TimeTrigger. RandomDelay
ms.assetid: ee55dd85-9696-4872-8670-f919fca7481d
keywords:
- Utilità di pianificazione proprietà RandomDelay
- Utilità di pianificazione proprietà RandomDelay, oggetto TimeTrigger
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
ms.openlocfilehash: 39c4acf4f38670332e723ac0824276695919cb1d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321508"
---
# <a name="timetriggerrandomdelay-property"></a>Proprietà TimeTrigger. RandomDelay

Per gli script, ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.

## <a name="syntax"></a>Sintassi


```VB
TimeTrigger.RandomDelay As String
```



## <a name="property-value"></a>Valore proprietà

Tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





