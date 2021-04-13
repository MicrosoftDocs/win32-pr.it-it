---
title: Proprietà TaskSettings. DeleteExpiredTaskAfter
description: Per gli script, ottiene o imposta il periodo di tempo durante il quale il Utilità di pianificazione resterà in attesa prima di eliminare l'attività dopo la scadenza.
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- Utilità di pianificazione proprietà DeleteExpiredTaskAfter
- Utilità di pianificazione proprietà DeleteExpiredTaskAfter, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà DeleteExpiredTaskAfter
topic_type:
- apiref
api_name:
- TaskSettings.DeleteExpiredTaskAfter
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9005ff7988353daa902b1bc3151c539713bb94ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475958"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a>Proprietà TaskSettings. DeleteExpiredTaskAfter

Per gli script, ottiene o imposta il periodo di tempo durante il quale il Utilità di pianificazione resterà in attesa prima di eliminare l'attività dopo la scadenza. Se per questa proprietà non viene specificato alcun valore, il servizio Utilità di pianificazione non eliminerà l'attività.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a>Valore proprietà

Stringa che ottiene o imposta il periodo di tempo durante il quale il Utilità di pianificazione resterà in attesa prima di eliminare l'attività dopo la scadenza. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).

## <a name="remarks"></a>Commenti

Un'attività scade dopo il superamento del limite finale per tutti i trigger associati all'attività. Il limite finale per un trigger viene specificato dalla proprietà [EndBoundary](trigger-endboundary.md) ereditata da tutti gli oggetti trigger.

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) dello schema utilità di pianificazione.

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

 

 





