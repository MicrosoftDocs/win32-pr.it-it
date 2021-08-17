---
title: TaskSettings.MultipleInstances - proprietà
description: Per lo scripting, ottiene o imposta i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- Proprietà MultipleInstances Utilità di pianificazione
- Proprietà MultipleInstances Utilità di pianificazione , oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione proprietà , MultipleInstances
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
ms.openlocfilehash: 2ff0091b9051840fea4c37869b51902f0c5f4c7cfed43a47c4f3924b398fe3e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059689"
---
# <a name="tasksettingsmultipleinstances-property"></a>TaskSettings.MultipleInstances - proprietà

Per lo scripting, ottiene o imposta i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a>Valore proprietà

[**ATTIVITÀ \_ Costanti \_ DI INSTANCES POLICY.**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)



| Valore                                                                                                                                                                                                                                                               | Significato                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <dt>**ATTIVITÀ \_ ISTANZE \_ PARALLEL**</dt> <dt>0</dt> </dl>                 | Avvia una nuova istanza mentre è in esecuzione un'istanza esistente dell'attività.<br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <dt>**ATTIVITÀ \_ CODA \_ ISTANZE**</dt> <dt>1</dt> </dl>                          | Avvia una nuova istanza dell'attività al termine di tutte le altre istanze dell'attività.<br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <dt>**ATTIVITÀ \_ LE ISTANZE \_ \_ IGNORANO IL NUOVO**</dt> <dt>2</dt> </dl>          | Non avvia una nuova istanza se è in esecuzione un'istanza esistente dell'attività.<br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <dt>**ATTIVITÀ \_ LE ISTANZE \_ \_ INTERROMPINO 3**</dt> <dt></dt> </dl> | Arresta un'istanza esistente dell'attività prima di avviare la nuova istanza.<br/>                 |



 

## <a name="remarks"></a>Commenti

Quando si legge o si scrive codice XML per un'attività, questa impostazione viene specificata [**nell'elemento MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) dello schema Utilità di pianificazione schema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CRITERI \_ DELLE ISTANZE DI \_ ATTIVITÀ**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





