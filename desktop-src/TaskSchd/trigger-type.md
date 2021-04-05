---
title: Proprietà trigger. Type
description: Per lo scripting, ottiene il tipo del trigger.
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Utilità di pianificazione proprietà di tipo
- Utilità di pianificazione proprietà di tipo, oggetto trigger
- Trigger Utilità di pianificazione oggetto, proprietà Type
topic_type:
- apiref
api_name:
- Trigger.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2cef2d6ae33ceeac028e10a0f545afbc0a0ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740791"
---
# <a name="triggertype-property"></a>Proprietà trigger. Type

Per lo scripting, ottiene il tipo del trigger. Il tipo di trigger viene definito quando il trigger viene creato e non può essere modificato in un secondo momento. Per informazioni sulla creazione di un trigger, vedere [**TriggerCollection. Create**](triggercollection-create.md).

## <a name="syntax"></a>Sintassi


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a>Valore proprietà

Uno dei valori di [**enumerazione \_ \_ tipo2 del trigger dell'attività**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) seguente.



| Valore                                                                                                                                                                                                                                                                                | Significato                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**Attività \_ \_Evento trigger**</dt> <dt>0</dt> </dl>                                                 | Avvia l'attività quando si verifica un evento specifico.<br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**Attività \_ \_Ora di attivazione**</dt> <dt>1</dt> </dl>                                                    | Avvia l'attività in un'ora specifica del giorno.<br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**Attività \_ TRIGGER \_ giornaliero**</dt> <dt>2</dt> </dl>                                                 | Avvia l'attività ogni giorno.<br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**Attività \_ ATTIVA \_ settimanalmente**</dt> <dt>3</dt> </dl>                                              | Avvia l'attività settimanalmente.<br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**Attività \_ TRIGGER \_ mensile**</dt> <dt>4</dt> </dl>                                           | Avvia l'attività ogni mese.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**Attività \_ ATTIVA \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Avvia l'attività ogni mese in un giorno specifico della settimana.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**Attività \_ ATTIVA \_ inattività**</dt> <dt>6</dt> </dl>                                                    | Avvia l'attività quando il computer entra in uno stato di inattività.<br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**Attività \_ ATTIVAZIONE \_ registrazione**</dt> <dt>7</dt> </dl>                            | Avvia l'attività quando l'attività è registrata.<br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**Attività \_ ATTIVA \_ avvio**</dt> <dt>8</dt> </dl>                                                    | Avvia l'attività all'avvio del computer.<br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**Attività \_ ATTIVARE l' \_ accesso**</dt> <dt>9</dt> </dl>                                                 | Avvia l'attività quando un utente specifico esegue l'accesso.<br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**Attività \_ ATTIVA \_ \_ \_ modifica stato sessione**</dt> <dt>11</dt> </dl> | Attiva l'attività quando viene modificato uno specifico stato della sessione.<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> <dt>

[**\_Trigger attività \_ tipo2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





