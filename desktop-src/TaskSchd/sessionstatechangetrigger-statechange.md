---
title: Proprietà SessionStateChangeTrigger. StateChange
description: Per la creazione di script, ottiene o imposta il tipo di modifica della sessione di Terminal Server che attiverà l'avvio di un'attività.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- Utilità di pianificazione proprietà StateChange
- Utilità di pianificazione proprietà StateChange, oggetto SessionStateChangeTrigger
- Oggetto SessionStateChangeTrigger Utilità di pianificazione, proprietà StateChange
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.StateChange
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4be561482917788f6afb9b8eb7394cdcce7985
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740615"
---
# <a name="sessionstatechangetriggerstatechange-property"></a>Proprietà SessionStateChangeTrigger. StateChange

Per la creazione di script, ottiene o imposta il tipo di modifica della sessione di Terminal Server che attiverà l'avvio di un'attività.

## <a name="syntax"></a>Sintassi


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a>Valore proprietà

Tipo di modifica della sessione di Terminal Server che attiva un'attività da avviare.

I valori possibili sono dall'enumerazione [**del \_ \_ tipo di \_ modifica \_ dello stato della sessione di attività**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) .



| Valore                                                                                                                                                                                                                                               | Significato                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <dt>**Attività \_ \_Connessione console**</dt> <dt>1</dt> </dl>          | Modifica dello stato di connessione della console Terminal Server. Ad esempio, quando si esegue la connessione a una sessione utente nel computer locale cambiando gli utenti del computer. <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <dt>**Attività \_ \_Disconnessione console**</dt> <dt>2</dt> </dl> | Modifica dello stato di disconnessione della console Terminal Server. Ad esempio, quando si esegue la disconnessione a una sessione utente nel computer locale cambiando gli utenti del computer.<br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <dt>**Attività \_ \_Connessione remota**</dt> <dt>3</dt> </dl>             | Terminal Server modifica dello stato della connessione remota. Ad esempio, quando un utente si connette a una sessione utente utilizzando il programma Connessione Desktop remoto da un computer remoto.<br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <dt>**Attività \_ \_Disconnessione remota**</dt> <dt>4</dt> </dl>    | Terminal Server modifica dello stato di disconnessione remota. Ad esempio, quando un utente si disconnette da una sessione utente durante l'utilizzo del programma Connessione Desktop remoto da un computer remoto.<br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <dt>**Attività \_ \_Blocco sessione**</dt> <dt>7</dt> </dl>                   | Modifica dello stato di blocco della sessione Terminal Server. Ad esempio, questa modifica di stato comporta l'esecuzione dell'attività quando il computer è bloccato. <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <dt>**Attività \_ \_Sblocco sessione**</dt> <dt>8</dt> </dl>             | Modifica dello stato di Terminal Server sessione sbloccata. Ad esempio, questa modifica di stato comporta l'esecuzione dell'attività quando il computer è sbloccato.<br/>                                                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





