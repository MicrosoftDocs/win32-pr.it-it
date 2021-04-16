---
title: Proprietà TaskSettings. MultipleInstances
description: Per gli script, ottiene o imposta i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- Utilità di pianificazione proprietà MultipleInstances
- Utilità di pianificazione proprietà MultipleInstances, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà MultipleInstances
topic_type:
- apiref
api_name:
- TaskSettings.MultipleInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794ea07f1c01dabe957181bd327f8787f873917b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517469"
---
# <a name="tasksettingsmultipleinstances-property"></a>Proprietà TaskSettings. MultipleInstances

Per gli script, ottiene o imposta i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a>Valore proprietà

[**Attività \_ Costanti dei \_ criteri delle istanze**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) .



| Valore                                                                                                                                                                                                                                                               | Significato                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <dt>**Attività \_ ISTANZE \_ parallele**</dt> <dt>0</dt> </dl>                 | Avvia una nuova istanza di mentre è in esecuzione un'istanza esistente dell'attività.<br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <dt>**Attività \_ \_Coda istanze**</dt> <dt>1</dt> </dl>                          | Avvia una nuova istanza dell'attività dopo il completamento di tutte le altre istanze dell'attività.<br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <dt>**Attività \_ ISTANZE \_ ignorate \_ nuovo**</dt> <dt>2</dt> </dl>          | Non avvia una nuova istanza di se è in esecuzione un'istanza esistente dell'attività.<br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <dt>**Attività \_ Le \_ istanze \_ arrestano**</dt> <dt>3</dt> esistente </dl> | Arresta un'istanza esistente dell'attività prima di avviare una nuova istanza.<br/>                 |



 

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_criteri istanze \_ attività**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





