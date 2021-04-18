---
title: Utilità di pianificazione le costanti Error e Success (WinError. h)
description: Se si verifica un errore, le API Utilità di pianificazione possono restituire uno dei codici di errore seguenti come valore HRESULT.
ms.assetid: 54278bbd-7dca-438e-a771-5fcb08c4aa68
keywords:
- Costanti Utilità di pianificazione Utilità di pianificazione, Reference, Error e Success
topic_type:
- apiref
api_name:
- SCHED_S_TASK_READY
- SCHED_S_TASK_RUNNING
- SCHED_S_TASK_DISABLED
- SCHED_S_TASK_HAS_NOT_RUN
- SCHED_S_TASK_NO_MORE_RUNS
- SCHED_S_TASK_NOT_SCHEDULED
- SCHED_S_TASK_TERMINATED
- SCHED_S_TASK_NO_VALID_TRIGGERS
- SCHED_S_EVENT_TRIGGER
- SCHED_E_TRIGGER_NOT_FOUND
- SCHED_E_TASK_NOT_READY
- SCHED_E_TASK_NOT_RUNNING
- SCHED_E_SERVICE_NOT_INSTALLED
- SCHED_E_CANNOT_OPEN_TASK
- SCHED_E_INVALID_TASK
- SCHED_E_ACCOUNT_INFORMATION_NOT_SET
- SCHED_E_ACCOUNT_NAME_NOT_FOUND
- SCHED_E_ACCOUNT_DBASE_CORRUPT
- SCHED_E_NO_SECURITY_SERVICES
- SCHED_E_UNKNOWN_OBJECT_VERSION
- SCHED_E_UNSUPPORTED_ACCOUNT_OPTION
- SCHED_E_SERVICE_NOT_RUNNING
- SCHED_E_UNEXPECTEDNODE
- SCHED_E_NAMESPACE
- SCHED_E_INVALIDVALUE
- SCHED_E_MISSINGNODE
- SCHED_E_MALFORMEDXML
- SCHED_S_SOME_TRIGGERS_FAILED
- SCHED_S_BATCH_LOGON_PROBLEM
- SCHED_E_TOO_MANY_NODES
- SCHED_E_PAST_END_BOUNDARY
- SCHED_E_ALREADY_RUNNING
- SCHED_E_USER_NOT_LOGGED_ON
- SCHED_E_INVALID_TASK_HASH
- SCHED_E_SERVICE_NOT_AVAILABLE
- SCHED_E_SERVICE_TOO_BUSY
- SCHED_E_TASK_ATTEMPTED
- SCHED_S_TASK_QUEUED
- SCHED_E_TASK_DISABLED
- SCHED_E_TASK_NOT_V1_COMPAT
- SCHED_E_START_ON_DEMAND
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: a1d0347938020ca8937f2764e3b2c62a38fc9273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325277"
---
# <a name="task-scheduler-error-and-success-constants"></a>Utilità di pianificazione le costanti Error e Success

Se si verifica un errore, le API Utilità di pianificazione possono restituire uno dei codici di errore seguenti come valore **HRESULT** .

Le costanti che iniziano con Pianifica \_ S \_ sono costanti Success e le costanti che iniziano con Pianifica \_ e \_ sono costanti di errore.

```cpp
  HRESULT phrStatus;
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
    
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;

  //...
  }
```

Esempio di [codice C/C++ esempio: recupero dello stato dell'attività](c-c-code-example-retrieving-task-status.md).

> [!Note]  
> Alcune API Utilità di pianificazione possono restituire codici di errore di sistema e di rete (ad esempio, 64). È possibile controllare la definizione di questi tipi di codici di errore usando il comando **net helpmsg** nella finestra del prompt dei comandi. Ad esempio, il comando **net helpmsg 64** restituisce il messaggio: il nome di rete specificato non è più disponibile.

 

Per ulteriori informazioni sugli eventi e i messaggi di errore, vedere [centro messaggi eventi ed errori](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).

<dl> <dt>

<span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**\_attività pianifica \_ S \_ pronta**
</dt> <dd> <dl> <dt>

0x00041300
</dt> <dt>



L'attività è pronta per essere eseguita al successivo orario pianificato.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**\_attività pianifica \_ \_ in esecuzione**
</dt> <dd> <dl> <dt>

0x00041301
</dt> <dt>



L'attività è attualmente in esecuzione.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**\_attività pianifica \_ \_ disabilitata**
</dt> <dd> <dl> <dt>

0x00041302
</dt> <dt>



L'attività non verrà eseguita all'ora pianificata perché è stata disabilitata.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**l' \_ attività pianifica S \_ \_ non è stata \_ \_ eseguita**
</dt> <dd> <dl> <dt>

0x00041303
</dt> <dt>



L'attività non è ancora stata eseguita.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**\_non è \_ \_ più possibile \_ \_ eseguire l'attività pianifica**
</dt> <dd> <dl> <dt>

0x00041304
</dt> <dt>



Non sono disponibili altre esecuzioni pianificate per questa attività.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**\_attività pianifica \_ \_ non \_ pianificata**
</dt> <dd> <dl> <dt>

0x00041305
</dt> <dt>



Una o più proprietà necessarie per eseguire questa attività in una pianificazione non sono state impostate.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**\_attività pianifica \_ \_ terminata**
</dt> <dd> <dl> <dt>

0x00041306
</dt> <dt>



L'ultima esecuzione dell'attività è stata interrotta dall'utente.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**Pianifica \_ S \_ attività \_ nessun \_ \_ trigger valido**
</dt> <dd> <dl> <dt>

0x00041307
</dt> <dt>



L'attività non dispone di trigger oppure i trigger esistenti sono disabilitati o non impostati.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**\_trigger di \_ evento Pianifica S \_**
</dt> <dd> <dl> <dt>

0x00041308
</dt> <dt>



I trigger di evento non hanno set run times.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**\_trigger Pianifica \_ E \_ non \_ trovato**
</dt> <dd> <dl> <dt>

0x80041309
</dt> <dt>



Il trigger di un'attività non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**\_attività pianifica \_ E \_ non \_ pronta**
</dt> <dd> <dl> <dt>

0x8004130A
</dt> <dt>



Una o più proprietà richieste per eseguire questa attività non sono state impostate.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**\_attività pianifica \_ E \_ non \_ in esecuzione**
</dt> <dd> <dl> <dt>

0x8004130B
</dt> <dt>



Nessuna istanza in esecuzione dell'attività.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**il \_ servizio Pianifica E \_ \_ non è \_ installato**
</dt> <dd> <dl> <dt>

0x8004130C
</dt> <dt>



Il servizio Utilità di pianificazione non è installato in questo computer.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**Pianifica \_ E \_ non è possibile \_ aprire l' \_ attività**
</dt> <dd> <dl> <dt>

0x8004130D
</dt> <dt>



Non è stato possibile aprire l'oggetto attività.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**\_attività pianifica E \_ non valida \_**
</dt> <dd> <dl> <dt>

0x8004130E
</dt> <dt>



L'oggetto è un oggetto attività non valido o non è un oggetto attività.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**\_ \_ informazioni sull'account Pianifica E \_ \_ non \_ impostate**
</dt> <dd> <dl> <dt>

0x8004130F
</dt> <dt>



Non sono state trovate informazioni sull'account nel database di Utilità di pianificazione Security per l'attività indicata.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**il \_ nome dell'account Pianifica E non è stato \_ \_ \_ \_ trovato**
</dt> <dd> <dl> <dt>

0x80041310
</dt> <dt>



Impossibile stabilire l'esistenza dell'account specificato.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**Pianifica \_ E \_ account \_ dBASE \_ danneggiato**
</dt> <dd> <dl> <dt>

0x80041311
</dt> <dt>



È stato rilevato un danneggiamento nel database di Utilità di pianificazione Security; il database è stato reimpostato.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**Pianifica \_ E \_ nessun \_ servizio di sicurezza \_**
</dt> <dd> <dl> <dt>

0x80041312
</dt> <dt>



I servizi di sicurezza Utilità di pianificazione sono disponibili solo in Windows NT.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**Pianifica \_ E \_ \_ versione oggetto \_ sconosciuta**
</dt> <dd> <dl> <dt>

0x80041313
</dt> <dt>



La versione dell'oggetto attività non è supportata o non è valida.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**\_opzione account Pianifica E non \_ supportata \_ \_**
</dt> <dd> <dl> <dt>

0x80041314
</dt> <dt>



L'attività è stata configurata con una combinazione non supportata di impostazioni dell'account e di opzioni di run-time.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**Pianifica \_ E \_ servizio \_ non \_ in esecuzione**
</dt> <dd> <dl> <dt>

0x80041315
</dt> <dt>



Il servizio Utilità di pianificazione non è in esecuzione.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**Pianifica \_ E \_ UNEXPECTEDNODE**
</dt> <dd> <dl> <dt>

0x80041316
</dt> <dt>



Il codice XML dell'attività contiene un nodo imprevisto.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**\_ \_ spazio dei nomi Pianifica E**
</dt> <dd> <dl> <dt>

0x80041317
</dt> <dt>



Il codice XML dell'attività contiene un elemento o un attributo da uno spazio dei nomi imprevisto.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**Pianifica \_ E \_ INVALIDVALUE**
</dt> <dd> <dl> <dt>

0x80041318
</dt> <dt>



Il codice XML dell'attività contiene un valore che non è formattato correttamente o non è compreso nell'intervallo.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**Pianifica \_ E \_ MISSINGNODE**
</dt> <dd> <dl> <dt>

0x80041319
</dt> <dt>



Nell'XML dell'attività manca un elemento o un attributo obbligatorio.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**Pianifica \_ E \_ MALFORMEDXML**
</dt> <dd> <dl> <dt>

0x8004131A
</dt> <dt>



Il formato del codice XML dell'attività non è valido.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**Pianifica \_ \_ alcuni \_ trigger \_ non riusciti**
</dt> <dd> <dl> <dt>

0x0004131B
</dt> <dt>



L'attività è registrata, ma non tutti i trigger specificati avvierà l'attività.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**\_problema di \_ \_ accesso batch Pianifica S \_**
</dt> <dd> <dl> <dt>

0x0004131C
</dt> <dt>



L'attività è registrata, ma potrebbe non essere avviata. Il privilegio di accesso batch deve essere abilitato per l'entità attività.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**Pianifica \_ E \_ troppi \_ \_ nodi**
</dt> <dd> <dl> <dt>

0x8004131D
</dt> <dt>



Il codice XML dell'attività contiene troppi nodi dello stesso tipo.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**Pianifica \_ E \_ \_ limite finale finale \_**
</dt> <dd> <dl> <dt>

0x8004131E
</dt> <dt>



Non è possibile avviare l'attività dopo il limite finale del trigger.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**Pianifica \_ E \_ già \_ in esecuzione**
</dt> <dd> <dl> <dt>

0x8004131F
</dt> <dt>



Un'istanza di questa attività è già in esecuzione.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**\_ \_ utente di Pianifica E \_ non \_ connesso \_**
</dt> <dd> <dl> <dt>

0x80041320
</dt> <dt>



L'attività non verrà eseguita perché l'utente non è connesso.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**Pianifica \_ E \_ \_ hash attività non valido \_**
</dt> <dd> <dl> <dt>

0x80041321
</dt> <dt>



L'immagine dell'attività è danneggiata o è stata manomessa.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**Pianifica \_ E \_ servizio \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

0x80041322
</dt> <dt>



Il servizio Utilità di pianificazione non è disponibile.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**Pianifica \_ E \_ servizio \_ troppo \_ occupato**
</dt> <dd> <dl> <dt>

0x80041323
</dt> <dt>



Il servizio Utilità di pianificazione è troppo occupato per gestire la richiesta. Riprova più tardi.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**tentativo di Pianifica \_ E \_ attività \_**
</dt> <dd> <dl> <dt>

0x80041324
</dt> <dt>



Il servizio Utilità di pianificazione ha tentato di eseguire l'attività, ma l'attività non è stata eseguita a causa di uno dei vincoli nella definizione di attività.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**\_attività pianifica \_ in \_ coda**
</dt> <dd> <dl> <dt>

0x00041325
</dt> <dt>



Il servizio Utilità di pianificazione ha richiesto l'esecuzione dell'attività.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**\_attività pianifica \_ E \_ disabilitata**
</dt> <dd> <dl> <dt>

0x80041326
</dt> <dt>



L'attività è disabilitata.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**Pianifica \_ E \_ attività \_ non \_ v1 v1 \_**
</dt> <dd> <dl> <dt>

0x80041327
</dt> <dt>



L'attività dispone di proprietà che non sono compatibili con le versioni precedenti di Windows.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**Pianifica \_ E \_ avvio \_ su \_ richiesta**
</dt> <dd> <dl> <dt>

0x80041328
</dt> <dt>



Le impostazioni dell'attività non consentono l'avvio su richiesta dell'attività.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



 

 





