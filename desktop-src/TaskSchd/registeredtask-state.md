---
title: RegisteredTask.State - proprietà
description: Per lo scripting, ottiene lo stato operativo dell'attività registrata.
ms.assetid: 1acd4946-322f-4f24-b317-92be80e19de5
keywords:
- Proprietà state Utilità di pianificazione
- Proprietà State Utilità di pianificazione , oggetto RegisteredTask
- Proprietà State dell'Utilità di pianificazione RegisteredTask
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
ms.openlocfilehash: 6099c47590397556937b8b1cceb59bc231117aa16c92012d59964afec4f6bcf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759602"
---
# <a name="registeredtaskstate-property"></a>RegisteredTask.State - proprietà

Per lo scripting, ottiene lo stato operativo dell'attività registrata.

## <a name="syntax"></a>Sintassi


```VB
RegisteredTask.State As Integer
```



## <a name="property-value"></a>Valore proprietà

Costante [**TASK \_ STATE**](/windows/desktop/api/taskschd/ne-taskschd-task_state) che definisce lo stato operativo dell'attività.



| Valore                                                                                                                                                                                                                                   | Significato                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <dt>**ATTIVITÀ \_ STATO \_ SCONOSCIUTO**</dt> <dt>0</dt> </dl>    | Lo stato dell'attività è sconosciuto.<br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <dt>**ATTIVITÀ \_ STATO \_ DISABILITATO**</dt> <dt>1</dt> </dl> | L'attività è registrata ma è disabilitata e nessuna istanza dell'attività viene accodata o in esecuzione. L'attività non può essere eseguita finché non viene abilitata.<br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <dt>**ATTIVITÀ \_ STATO \_ IN CODA**</dt> <dt>2</dt> </dl>       | Le istanze dell'attività vengono accodati.<br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <dt>**ATTIVITÀ \_ STATE \_ READY**</dt> <dt>3</dt> </dl>          | L'attività è pronta per l'esecuzione, ma nessuna istanza viene accodata o in esecuzione.<br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <dt>**ATTIVITÀ \_ STATO \_ IN ESECUZIONE**</dt> <dt>4</dt> </dl>    | Una o più istanze dell'attività sono in esecuzione.<br/>                                                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





