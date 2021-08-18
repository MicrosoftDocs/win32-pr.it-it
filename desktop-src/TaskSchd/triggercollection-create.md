---
title: Metodo TriggerCollection.Create
description: Per lo scripting, crea un nuovo trigger per l'attività.
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- trigger Utilità di pianificazione , creazione
- Creare il metodo Utilità di pianificazione
- Creare il metodo Utilità di pianificazione, oggetto TriggerCollection
- Metodo TriggerCollection Utilità di pianificazione , Create
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
ms.openlocfilehash: a7cfc32ebff941af374d2c4bb64db8ffe064961c13840e50244f416bad477a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001969"
---
# <a name="triggercollectioncreate-method"></a>Metodo TriggerCollection.Create

Per lo scripting, crea un nuovo trigger per l'attività.

## <a name="syntax"></a>Sintassi


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*type* \[ Pollici\]
</dt> <dd>

Questo parametro è impostato su una delle costanti di enumerazione [**TASK \_ TRIGGER \_ TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) seguenti.



| Valore                                                                                                                                                                                                                                                                                | Significato                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**ATTIVITÀ \_ EVENTO \_ TRIGGER**</dt> <dt>0</dt> </dl>                                                 | Attiva l'attività quando si verifica un evento specifico.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**ATTIVITÀ \_ ORA \_ TRIGGER**</dt> <dt>1</dt> </dl>                                                    | Attiva l'attività a un'ora specifica del giorno.<br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ DAILY**</dt> <dt>2</dt> </dl>                                                 | Attiva l'attività in base a una pianificazione giornaliera. Ad esempio, l'attività inizia a un'ora specifica ogni giorno, ogni altro giorno, ogni terzo giorno e così via.<br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ WEEKLY**</dt> <dt>3</dt> </dl>                                              | Attiva l'attività in base a una pianificazione settimanale. Ad esempio, l'attività inizia alle 8:00 di un giorno specifico ogni settimana o altra settimana.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ MENSILE**</dt> <dt>4</dt> </dl>                                           | Attiva l'attività in base a una pianificazione mensile. Ad esempio, l'attività inizia in giorni specifici di mesi specifici.<br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Attiva l'attività in base a una pianificazione mensile del giorno della settimana. Ad esempio, l'attività inizia in giorni specifici della settimana, settimane del mese e mesi dell'anno.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ IDLE**</dt> <dt>6</dt> </dl>                                                    | Attiva l'attività quando il computer passa a uno stato di inattività.<br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**ATTIVITÀ \_ REGISTRAZIONE \_ TRIGGER**</dt> <dt>7</dt> </dl>                            | Attiva l'attività quando l'attività viene registrata.<br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ BOOT**</dt> <dt>8</dt> </dl>                                                    | Attiva l'attività all'avvio del computer.<br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**ATTIVITÀ \_ TRIGGER \_ LOGON**</dt> <dt>9</dt> </dl>                                                 | Attiva l'attività quando un utente specifico accede.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**ATTIVITÀ \_ ATTIVARE \_ LA MODIFICA DELLO STATO DELLA \_ \_ SESSIONE**</dt> <dt>11</dt> </dl> | Attiva l'attività quando viene modificato uno stato della sessione specifico.<br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**Trigger**](trigger.md) che rappresenta il nuovo trigger.

## <a name="remarks"></a>Commenti

Per informazioni su ogni tipo di trigger, vedere [Tipi di trigger](trigger-types.md).

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

[**Trigger**](trigger.md)
</dt> </dl>

 

 





