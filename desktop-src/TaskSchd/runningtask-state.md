---
title: RunningTask.State - proprietà
description: Per lo scripting, ottiene un identificatore per lo stato dell'attività in esecuzione.
ms.assetid: 048863f4-b80b-42ab-bd74-ec761a8f03aa
keywords:
- Proprietà state Utilità di pianificazione
- Proprietà State Utilità di pianificazione , oggetto RunningTask
- Oggetto RunningTask Utilità di pianificazione proprietà , State
topic_type:
- apiref
api_name:
- RunningTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e3c83b35c348e3ab86eb04c03ef4c5d25a76ef3fe5040603ce32da54ec4e217
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975041"
---
# <a name="runningtaskstate-property"></a>RunningTask.State - proprietà

Per lo scripting, ottiene un identificatore per lo stato dell'attività in esecuzione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
RunningTask.State As String
```



## <a name="property-value"></a>Valore proprietà

Identificatore dello stato dell'attività in esecuzione.



| Valore                                                                                                                                                                                                                                   | Significato                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <dt>**ATTIVITÀ \_ STATO \_ SCONOSCIUTO**</dt> <dt>0</dt> </dl>    | Lo stato dell'attività è sconosciuto.<br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <dt>**ATTIVITÀ \_ STATO \_ DISABILITATO**</dt> <dt>1</dt> </dl> | L'attività è registrata ma è disabilitata e nessuna istanza dell'attività viene accodata o in esecuzione. L'attività non può essere eseguita finché non viene abilitata.<br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <dt>**ATTIVITÀ \_ STATO \_ IN CODA**</dt> <dt>2</dt> </dl>       | Le istanze dell'attività vengono accodati.<br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <dt>**ATTIVITÀ \_ STATE \_ READY**</dt> <dt>3</dt> </dl>          | L'attività è pronta per l'esecuzione, ma nessuna istanza viene accodata o in esecuzione.<br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <dt>**ATTIVITÀ \_ STATO \_ IN ESECUZIONE**</dt> <dt>4</dt> </dl>    | Una o più istanze dell'attività sono in esecuzione.<br/>                                                                                         |



 

## <a name="remarks"></a>Commenti

Il [**metodo RunningTask.Refresh**](runningtask-refresh.md) viene chiamato prima che venga restituito il valore della proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





