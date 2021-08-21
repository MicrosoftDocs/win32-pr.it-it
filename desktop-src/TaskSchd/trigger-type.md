---
title: Trigger.Type - proprietà
description: Per lo scripting, ottiene il tipo del trigger.
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Proprietà type Utilità di pianificazione
- Proprietà Type Utilità di pianificazione, oggetto Trigger
- Attivare l'oggetto Utilità di pianificazione proprietà , Type
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
ms.openlocfilehash: bcc44e385324d161ca051b4270096e674adbba878448667ef176a9c1c63bb24b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002039"
---
# <a name="triggertype-property"></a>Trigger.Type - proprietà

Per lo scripting, ottiene il tipo del trigger. Il tipo di trigger viene definito quando il trigger viene creato e non può essere modificato in un secondo momento. Per informazioni sulla creazione di un trigger, vedere [**TriggerCollection.Create.**](triggercollection-create.md)

## <a name="syntax"></a>Sintassi


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a>Valore proprietà

Uno dei valori di [**enumerazione TASK \_ TRIGGER \_ TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) seguenti.



| Valore                                                                                                                                                                                                                                                                                | Significato                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**ATTIVITÀ \_ ATTIVARE \_ L'EVENTO**</dt> <dt>0</dt> </dl>                                                 | Avvia l'attività quando si verifica un evento specifico.<br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ TIME**</dt> <dt>1</dt> </dl>                                                    | Avvia l'attività a un'ora specifica del giorno.<br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ DAILY**</dt> <dt>2</dt> </dl>                                                 | Avvia l'attività ogni giorno.<br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ WEEKLY**</dt> <dt>3</dt> </dl>                                              | Avvia l'attività ogni settimana.<br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ MONTHLY**</dt> <dt>4</dt> </dl>                                           | Avvia l'attività ogni mese.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Avvia l'attività ogni mese in un giorno specifico della settimana.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ IDLE**</dt> <dt>6</dt> </dl>                                                    | Avvia l'attività quando il computer entra in uno stato di inattività.<br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ REGISTRATION**</dt> <dt>7</dt> </dl>                            | Avvia l'attività quando l'attività viene registrata.<br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ BOOT**</dt> <dt>8</dt> </dl>                                                    | Avvia l'attività all'avvio del computer.<br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ LOGON**</dt> <dt>9</dt> </dl>                                                 | Avvia l'attività quando un utente specifico esegue l'accesso.<br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**ATTIVITÀ \_ ATTIVARE \_ LA MODIFICA DELLO STATO DELLA \_ \_ SESSIONE**</dt> <dt>11</dt> </dl> | Attiva l'attività quando viene modificato uno stato della sessione specifico.<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> <dt>

[**TIPO \_ DI TRIGGER \_ ATTIVITÀ2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





