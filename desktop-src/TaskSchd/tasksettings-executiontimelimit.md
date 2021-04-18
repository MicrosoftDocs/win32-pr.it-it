---
title: TaskSettings.Exeproprietà cutionTimeLimit
description: Per la creazione di script, ottiene o imposta la quantità di tempo consentita per completare l'attività.
ms.assetid: 5b8b8d4b-e705-4407-95c9-bf8baacb58c1
keywords:
- Utilità di pianificazione proprietà ExecutionTimeLimit
- Utilità di pianificazione proprietà ExecutionTimeLimit, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà ExecutionTimeLimit
topic_type:
- apiref
api_name:
- TaskSettings.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de01d68fa7fe6c21f022d8a21863887e57016c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302218"
---
# <a name="tasksettingsexecutiontimelimit-property"></a>TaskSettings.Exeproprietà cutionTimeLimit

Per la creazione di script, ottiene o imposta la quantità di tempo consentita per completare l'attività. Per impostazione predefinita, un'attività verrà arrestata 72 ore dopo l'avvio dell'esecuzione. È possibile modificare questa impostazione cambiando questa impostazione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.ExecutionTimeLimit As String
```



## <a name="property-value"></a>Valore proprietà

Quantità di tempo consentita per completare l'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Il valore PT0S consentirà l'esecuzione illimitata dell'attività. Quando questo parametro è impostato su Nothing, il limite di tempo di esecuzione è infinito.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) dello schema utilità di pianificazione.

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

 

 





