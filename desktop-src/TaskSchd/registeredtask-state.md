---
title: Proprietà RegisteredTask. state
description: Per lo scripting, ottiene lo stato operativo dell'attività registrata.
ms.assetid: 1acd4946-322f-4f24-b317-92be80e19de5
keywords:
- Utilità di pianificazione proprietà stato
- Utilità di pianificazione proprietà state, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, proprietà state
topic_type:
- apiref
api_name:
- RegisteredTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47af082174bc6927a16760e87566f311ec9f4a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478910"
---
# <a name="registeredtaskstate-property"></a>Proprietà RegisteredTask. state

Per lo scripting, ottiene lo stato operativo dell'attività registrata.

## <a name="syntax"></a>Sintassi


```VB
RegisteredTask.State As Integer
```



## <a name="property-value"></a>Valore proprietà

Costante [**\_ dello stato dell'attività**](/windows/desktop/api/taskschd/ne-taskschd-task_state) che definisce lo stato operativo dell'attività.



| Valore                                                                                                                                                                                                                                   | Significato                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <dt>**Attività \_ STATO \_ sconosciuto**</dt> <dt>0</dt> </dl>    | Lo stato dell'attività è sconosciuto.<br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <dt>**Attività \_ STATO \_ disabilitato**</dt> <dt>1</dt> </dl> | L'attività è registrata ma è disabilitata e nessuna istanza dell'attività viene accodata o in esecuzione. L'attività non può essere eseguita fino a quando non viene abilitata.<br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <dt>**Attività \_ STATO in \_ coda**</dt> <dt>2</dt> </dl>       | Le istanze dell'attività vengono accodate.<br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <dt>**Attività \_ STATO \_ pronto**</dt> <dt>3</dt> </dl>          | L'attività è pronta per essere eseguita, ma nessuna istanza è in coda o in esecuzione.<br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <dt>**Attività \_ STATO \_ che esegue**</dt> <dt>4</dt> </dl>    | Una o più istanze dell'attività sono in esecuzione.<br/>                                                                                         |



 

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
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





