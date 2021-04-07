---
title: Trigger.Exeproprietà cutionTimeLimit
description: Per la creazione di script, ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.
ms.assetid: 9993b362-f8f7-429b-a16a-1845d6f0f5e0
keywords:
- Utilità di pianificazione proprietà ExecutionTimeLimit
- Utilità di pianificazione proprietà ExecutionTimeLimit, oggetto trigger
- Utilità di pianificazione oggetto trigger, proprietà ExecutionTimeLimit
topic_type:
- apiref
api_name:
- Trigger.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974a9adebf8ca29fe8626c938c37580d0628771b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963979"
---
# <a name="triggerexecutiontimelimit-property"></a>Trigger.Exeproprietà cutionTimeLimit

Per la creazione di script, ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.

## <a name="syntax"></a>Sintassi


```VB
Trigger.ExecutionTimeLimit As String
```



## <a name="property-value"></a>Valore proprietà

Quantità massima di tempo durante il quale l'attività avviata dal trigger può essere eseguita. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, il limite di tempo di esecuzione viene specificato nell'elemento [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) dello schema utilità di pianificazione.

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

 

 





