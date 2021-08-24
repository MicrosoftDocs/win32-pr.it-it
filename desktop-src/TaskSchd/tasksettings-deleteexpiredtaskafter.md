---
title: TaskSettings.DeleteExpiredTaskAfter - proprietà
description: Per lo scripting, ottiene o imposta la quantità di tempo di attesa del Utilità di pianificazione prima di eliminare l'attività dopo la scadenza.
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- Proprietà DeleteExpiredTaskAfter Utilità di pianificazione
- DeleteExpiredTaskAfter - proprietà Utilità di pianificazione , oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione proprietà , DeleteExpiredTaskAfter
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
ms.openlocfilehash: 521f07a5712165c282a36bbfe2c3b66769239c53d652ae49a03fa6a50c19cb05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658451"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a>TaskSettings.DeleteExpiredTaskAfter - proprietà

Per lo scripting, ottiene o imposta la quantità di tempo di attesa del Utilità di pianificazione prima di eliminare l'attività dopo la scadenza. Se non viene specificato alcun valore per questa proprietà, il Utilità di pianificazione non eliminerà l'attività.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a>Valore proprietà

Stringa che ottiene o imposta la quantità di tempo di attesa del Utilità di pianificazione prima di eliminare l'attività dopo la scadenza. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).

## <a name="remarks"></a>Commenti

Un'attività scade dopo il superamento del limite finale per tutti i trigger associati all'attività. Il limite finale per un trigger viene specificato dalla [proprietà EndBoundary](trigger-endboundary.md) ereditata da tutti gli oggetti trigger.

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) dello schema Utilità di pianificazione dati.

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
</dt> </dl>

 

 





