---
title: SessionStateChangeTrigger.StateChange - proprietà
description: Per lo scripting, ottiene o imposta il tipo di modifica della sessione di Terminal Server che attiverebbe l'avvio di un'attività.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- Proprietà StateChange Utilità di pianificazione
- Proprietà StateChange Utilità di pianificazione , oggetto SessionStateChangeTrigger
- Oggetto SessionStateChangeTrigger Utilità di pianificazione proprietà , StateChange
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
ms.openlocfilehash: cfbd2037f19ca2d9fe8ec5d0ba046e69894f431b81d623b61b9474515bcef3a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100161"
---
# <a name="sessionstatechangetriggerstatechange-property"></a>SessionStateChangeTrigger.StateChange - proprietà

Per lo scripting, ottiene o imposta il tipo di modifica della sessione di Terminal Server che attiverebbe l'avvio di un'attività.

## <a name="syntax"></a>Sintassi


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a>Valore proprietà

Tipo di modifica della sessione di Terminal Server che attiva l'avvio di un'attività.

I valori possibili derivano [**dall'enumerazione TASK SESSION STATE CHANGE \_ \_ \_ \_ TYPE.**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type)



| Valore                                                                                                                                                                                                                                               | Significato                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <dt>**ATTIVITÀ \_ CONSOLE \_ CONNECT**</dt> <dt>1</dt> </dl>          | Modifica dello stato di connessione della console di Terminal Server. Ad esempio, quando ci si connette a una sessione utente nel computer locale scambiando utenti nel computer. <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <dt>**ATTIVITÀ \_ CONSOLE \_ DISCONNECT**</dt> <dt>2</dt> </dl> | Modifica dello stato di disconnessione della console di Terminal Server. Ad esempio, quando ci si disconnette da una sessione utente nel computer locale scambiando gli utenti nel computer.<br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <dt>**ATTIVITÀ \_ CONNESSIONE \_ REMOTA**</dt> <dt>3</dt> </dl>             | Modifica dello stato della connessione remota di Terminal Server. Ad esempio, quando un utente si connette a una sessione utente usando il Connessione Desktop remoto da un computer remoto.<br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <dt>**ATTIVITÀ \_ REMOTE \_ DISCONNECT**</dt> <dt>4</dt> </dl>    | Modifica dello stato di disconnessione remota di Terminal Server. Ad esempio, quando un utente si disconnette da una sessione utente durante l'Connessione Desktop remoto programma da un computer remoto.<br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <dt>**ATTIVITÀ \_ BLOCCO \_ SESSIONE**</dt> <dt>7</dt> </dl>                   | Modifica dello stato di blocco della sessione di Terminal Server. Ad esempio, questa modifica dello stato determina l'esecuzione dell'attività quando il computer è bloccato. <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <dt>**ATTIVITÀ \_ SBLOCCO \_ SESSIONE**</dt> <dt>8</dt> </dl>             | Modifica dello stato della sessione di Terminal Server sbloccata. Ad esempio, questa modifica dello stato determina l'esecuzione dell'attività quando il computer viene sbloccato.<br/>                                                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





