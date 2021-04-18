---
title: TriggerCollection. Create (metodo)
description: Per lo scripting crea un nuovo trigger per l'attività.
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- attiva Utilità di pianificazione, creazione
- Utilità di pianificazione Crea metodo
- Metodo Create Utilità di pianificazione, oggetto TriggerCollection
- TriggerCollection, oggetto Utilità di pianificazione, metodo create
topic_type:
- apiref
api_name:
- TriggerCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0f1c5dd8bef3d81a8e9b5859bc2bbd8c969bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301324"
---
# <a name="triggercollectioncreate-method"></a>TriggerCollection. Create (metodo)

Per lo scripting crea un nuovo trigger per l'attività.

## <a name="syntax"></a>Sintassi


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo* \[ di in\]
</dt> <dd>

Questo parametro è impostato su una delle seguenti costanti di enumerazione [**\_ \_ tipo2 del trigger di attività**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) .



| Valore                                                                                                                                                                                                                                                                                | Significato                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**Attività \_ \_Evento trigger**</dt> <dt>0</dt> </dl>                                                 | Attiva l'attività quando si verifica un evento specifico.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**Attività \_ \_Ora di attivazione**</dt> <dt>1</dt> </dl>                                                    | Attiva l'attività in un'ora specifica del giorno.<br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**Attività \_ TRIGGER \_ giornaliero**</dt> <dt>2</dt> </dl>                                                 | Attiva l'attività in base a una pianificazione giornaliera. Ad esempio, l'attività viene avviata a un'ora specifica ogni giorno, ogni giorno, ogni tre giorni e così via.<br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**Attività \_ ATTIVA \_ settimanalmente**</dt> <dt>3</dt> </dl>                                              | Attiva l'attività in base a una pianificazione settimanale. Ad esempio, l'attività inizia alle 8:00 di un giorno specifico ogni settimana o altra settimana.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**Attività \_ TRIGGER \_ mensile**</dt> <dt>4</dt> </dl>                                           | Attiva l'attività in base a una pianificazione mensile. Ad esempio, l'attività viene avviata in giorni specifici di mesi specifici.<br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**Attività \_ ATTIVA \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Attiva l'attività in base a una pianificazione mensile giornaliera della settimana. Ad esempio, l'attività viene avviata in base a giorni specifici della settimana, settimane del mese e mesi dell'anno.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**Attività \_ ATTIVA \_ inattività**</dt> <dt>6</dt> </dl>                                                    | Attiva l'attività quando il computer entra in uno stato di inattività.<br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**Attività \_ ATTIVAZIONE \_ registrazione**</dt> <dt>7</dt> </dl>                            | Attiva l'attività quando l'attività è registrata.<br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**Attività \_ ATTIVA \_ avvio**</dt> <dt>8</dt> </dl>                                                    | Attiva l'attività all'avvio del computer.<br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**Attività \_ ATTIVARE l' \_ accesso**</dt> <dt>9</dt> </dl>                                                 | Attiva l'attività quando un utente specifico esegue l'accesso.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**Attività \_ ATTIVA \_ \_ \_ modifica stato sessione**</dt> <dt>11</dt> </dl> | Attiva l'attività quando viene modificato uno specifico stato della sessione.<br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**trigger**](trigger.md) che rappresenta il nuovo trigger.

## <a name="remarks"></a>Commenti

Per informazioni su ogni tipo di trigger, vedere [tipi di trigger](trigger-types.md).

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

[**Trigger**](trigger.md)
</dt> </dl>

 

 





