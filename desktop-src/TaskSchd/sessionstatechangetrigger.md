---
title: Oggetto SessionStateChangeTrigger
description: Oggetto di script che attiva le attività per la connessione o la disconnessione della console, la connessione remota o la disconnessione o le notifiche di blocco o sblocco della workstation.
ms.assetid: ea450b8a-81cc-4d24-b850-78c967dcc5b8
keywords:
- Utilità di pianificazione oggetto SessionStateChangeTrigger
- Oggetto SessionStateChangeTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55d41f495c714fe2e1798c79cc4f24b99987a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301244"
---
# <a name="sessionstatechangetrigger-object"></a>Oggetto SessionStateChangeTrigger

Oggetto di script che attiva le attività per la connessione o la disconnessione della console, la connessione remota o la disconnessione o le notifiche di blocco o sblocco della workstation.

## <a name="members"></a>Membri

L'oggetto **SessionStateChangeTrigger** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **SessionStateChangeTrigger** dispone di queste proprietà.



| Proprietà                                                                | Tipo di accesso           | Descrizione                                                                                                                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ritardo**](sessionstatechangetrigger-delay.md)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica per quanto tempo si verifica un ritardo prima che venga avviata un'attività dopo che è stata rilevata una modifica dello stato della sessione Terminal Server.<br/>                                         |
| [**Abilitato**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled)<br/>                          | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                              |
| [**EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary)<br/>                  | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/>               |
| [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit)<br/>    | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta il periodo di tempo massimo in cui l'attività può essere avviata dal trigger.<br/>                                                 |
| [**ID**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                    | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta l'identificatore per il trigger.<br/>                                                                                             |
| [**Ripetizione**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition)<br/>                    | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/> |
| [**StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary)<br/>              | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di attivazione del trigger.<br/>                                                                            |
| [**StateChange**](sessionstatechangetrigger-statechange.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il tipo di modifica della sessione di Terminal Server che avvierà un'esecuzione dell'attività.<br/>                                                                                                      |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                | Sola lettura<br/>  | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene il tipo del trigger.<br/>                                                                                                            |
| [**UserId**](sessionstatechangetrigger-userid.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta l'utente per la sessione di Terminal Server. Quando viene rilevata una modifica dello stato della sessione per questo utente, viene avviata un'attività.<br/>                                                               |



 

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificato un trigger di modifica dello stato della sessione utilizzando l'elemento [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





