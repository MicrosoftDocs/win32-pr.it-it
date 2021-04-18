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
# <a name="task-scheduler-error-and-success-constants"></a><span data-ttu-id="1ca64-104">Utilità di pianificazione le costanti Error e Success</span><span class="sxs-lookup"><span data-stu-id="1ca64-104">Task Scheduler Error and Success Constants</span></span>

<span data-ttu-id="1ca64-105">Se si verifica un errore, le API Utilità di pianificazione possono restituire uno dei codici di errore seguenti come valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1ca64-105">If an error occurs, the Task Scheduler APIs can return one of the following error codes as an **HRESULT** value.</span></span>

<span data-ttu-id="1ca64-106">Le costanti che iniziano con Pianifica \_ S \_ sono costanti Success e le costanti che iniziano con Pianifica \_ e \_ sono costanti di errore.</span><span class="sxs-lookup"><span data-stu-id="1ca64-106">The constants that begin with SCHED\_S\_ are success constants, and the constants that begin with SCHED\_E\_ are error constants.</span></span>

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

<span data-ttu-id="1ca64-107">Esempio di [codice C/C++ esempio: recupero dello stato dell'attività](c-c-code-example-retrieving-task-status.md).</span><span class="sxs-lookup"><span data-stu-id="1ca64-107">Example from [C/C++ Code Example: Retrieving Task Status](c-c-code-example-retrieving-task-status.md).</span></span>

> [!Note]  
> <span data-ttu-id="1ca64-108">Alcune API Utilità di pianificazione possono restituire codici di errore di sistema e di rete (ad esempio, 64).</span><span class="sxs-lookup"><span data-stu-id="1ca64-108">Some Task Scheduler APIs can return system and network error codes (64 for example).</span></span> <span data-ttu-id="1ca64-109">È possibile controllare la definizione di questi tipi di codici di errore usando il comando **net helpmsg** nella finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="1ca64-109">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="1ca64-110">Ad esempio, il comando **net helpmsg 64** restituisce il messaggio: il nome di rete specificato non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="1ca64-110">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

 

<span data-ttu-id="1ca64-111">Per ulteriori informazioni sugli eventi e i messaggi di errore, vedere [centro messaggi eventi ed errori](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).</span><span class="sxs-lookup"><span data-stu-id="1ca64-111">For more information about events and error messages, see [Events and Errors Message Center](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).</span></span>

<dl> <dt>

<span data-ttu-id="1ca64-112"><span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**\_attività pianifica \_ S \_ pronta**</span><span class="sxs-lookup"><span data-stu-id="1ca64-112"><span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**SCHED\_S\_TASK\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-113">0x00041300</span><span class="sxs-lookup"><span data-stu-id="1ca64-113">0x00041300</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-114">L'attività è pronta per essere eseguita al successivo orario pianificato.</span><span class="sxs-lookup"><span data-stu-id="1ca64-114">The task is ready to run at its next scheduled time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-115"><span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**\_attività pianifica \_ \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="1ca64-115"><span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**SCHED\_S\_TASK\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-116">0x00041301</span><span class="sxs-lookup"><span data-stu-id="1ca64-116">0x00041301</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-117">L'attività è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1ca64-117">The task is currently running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-118"><span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**\_attività pianifica \_ \_ disabilitata**</span><span class="sxs-lookup"><span data-stu-id="1ca64-118"><span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**SCHED\_S\_TASK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-119">0x00041302</span><span class="sxs-lookup"><span data-stu-id="1ca64-119">0x00041302</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-120">L'attività non verrà eseguita all'ora pianificata perché è stata disabilitata.</span><span class="sxs-lookup"><span data-stu-id="1ca64-120">The task will not run at the scheduled times because it has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-121"><span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**l' \_ attività pianifica S \_ \_ non è stata \_ \_ eseguita**</span><span class="sxs-lookup"><span data-stu-id="1ca64-121"><span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**SCHED\_S\_TASK\_HAS\_NOT\_RUN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-122">0x00041303</span><span class="sxs-lookup"><span data-stu-id="1ca64-122">0x00041303</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-123">L'attività non è ancora stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="1ca64-123">The task has not yet run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-124"><span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**\_non è \_ \_ più possibile \_ \_ eseguire l'attività pianifica**</span><span class="sxs-lookup"><span data-stu-id="1ca64-124"><span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**SCHED\_S\_TASK\_NO\_MORE\_RUNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-125">0x00041304</span><span class="sxs-lookup"><span data-stu-id="1ca64-125">0x00041304</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-126">Non sono disponibili altre esecuzioni pianificate per questa attività.</span><span class="sxs-lookup"><span data-stu-id="1ca64-126">There are no more runs scheduled for this task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-127"><span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**\_attività pianifica \_ \_ non \_ pianificata**</span><span class="sxs-lookup"><span data-stu-id="1ca64-127"><span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**SCHED\_S\_TASK\_NOT\_SCHEDULED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-128">0x00041305</span><span class="sxs-lookup"><span data-stu-id="1ca64-128">0x00041305</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-129">Una o più proprietà necessarie per eseguire questa attività in una pianificazione non sono state impostate.</span><span class="sxs-lookup"><span data-stu-id="1ca64-129">One or more of the properties that are needed to run this task on a schedule have not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-130"><span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**\_attività pianifica \_ \_ terminata**</span><span class="sxs-lookup"><span data-stu-id="1ca64-130"><span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**SCHED\_S\_TASK\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-131">0x00041306</span><span class="sxs-lookup"><span data-stu-id="1ca64-131">0x00041306</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-132">L'ultima esecuzione dell'attività è stata interrotta dall'utente.</span><span class="sxs-lookup"><span data-stu-id="1ca64-132">The last run of the task was terminated by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-133"><span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**Pianifica \_ S \_ attività \_ nessun \_ \_ trigger valido**</span><span class="sxs-lookup"><span data-stu-id="1ca64-133"><span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**SCHED\_S\_TASK\_NO\_VALID\_TRIGGERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-134">0x00041307</span><span class="sxs-lookup"><span data-stu-id="1ca64-134">0x00041307</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-135">L'attività non dispone di trigger oppure i trigger esistenti sono disabilitati o non impostati.</span><span class="sxs-lookup"><span data-stu-id="1ca64-135">Either the task has no triggers or the existing triggers are disabled or not set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-136"><span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**\_trigger di \_ evento Pianifica S \_**</span><span class="sxs-lookup"><span data-stu-id="1ca64-136"><span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**SCHED\_S\_EVENT\_TRIGGER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-137">0x00041308</span><span class="sxs-lookup"><span data-stu-id="1ca64-137">0x00041308</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-138">I trigger di evento non hanno set run times.</span><span class="sxs-lookup"><span data-stu-id="1ca64-138">Event triggers do not have set run times.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-139"><span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**\_trigger Pianifica \_ E \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="1ca64-139"><span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**SCHED\_E\_TRIGGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-140">0x80041309</span><span class="sxs-lookup"><span data-stu-id="1ca64-140">0x80041309</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-141">Il trigger di un'attività non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="1ca64-141">A task's trigger is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-142"><span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**\_attività pianifica \_ E \_ non \_ pronta**</span><span class="sxs-lookup"><span data-stu-id="1ca64-142"><span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**SCHED\_E\_TASK\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-143">0x8004130A</span><span class="sxs-lookup"><span data-stu-id="1ca64-143">0x8004130A</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-144">Una o più proprietà richieste per eseguire questa attività non sono state impostate.</span><span class="sxs-lookup"><span data-stu-id="1ca64-144">One or more of the properties required to run this task have not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-145"><span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**\_attività pianifica \_ E \_ non \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="1ca64-145"><span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**SCHED\_E\_TASK\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-146">0x8004130B</span><span class="sxs-lookup"><span data-stu-id="1ca64-146">0x8004130B</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-147">Nessuna istanza in esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="1ca64-147">There is no running instance of the task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-148"><span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**il \_ servizio Pianifica E \_ \_ non è \_ installato**</span><span class="sxs-lookup"><span data-stu-id="1ca64-148"><span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**SCHED\_E\_SERVICE\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-149">0x8004130C</span><span class="sxs-lookup"><span data-stu-id="1ca64-149">0x8004130C</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-150">Il servizio Utilità di pianificazione non è installato in questo computer.</span><span class="sxs-lookup"><span data-stu-id="1ca64-150">The Task Scheduler service is not installed on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-151"><span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**Pianifica \_ E \_ non è possibile \_ aprire l' \_ attività**</span><span class="sxs-lookup"><span data-stu-id="1ca64-151"><span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**SCHED\_E\_CANNOT\_OPEN\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-152">0x8004130D</span><span class="sxs-lookup"><span data-stu-id="1ca64-152">0x8004130D</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-153">Non è stato possibile aprire l'oggetto attività.</span><span class="sxs-lookup"><span data-stu-id="1ca64-153">The task object could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-154"><span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**\_attività pianifica E \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="1ca64-154"><span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**SCHED\_E\_INVALID\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-155">0x8004130E</span><span class="sxs-lookup"><span data-stu-id="1ca64-155">0x8004130E</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-156">L'oggetto è un oggetto attività non valido o non è un oggetto attività.</span><span class="sxs-lookup"><span data-stu-id="1ca64-156">The object is either an invalid task object or is not a task object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-157"><span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**\_ \_ informazioni sull'account Pianifica E \_ \_ non \_ impostate**</span><span class="sxs-lookup"><span data-stu-id="1ca64-157"><span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**SCHED\_E\_ACCOUNT\_INFORMATION\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-158">0x8004130F</span><span class="sxs-lookup"><span data-stu-id="1ca64-158">0x8004130F</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-159">Non sono state trovate informazioni sull'account nel database di Utilità di pianificazione Security per l'attività indicata.</span><span class="sxs-lookup"><span data-stu-id="1ca64-159">No account information could be found in the Task Scheduler security database for the task indicated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-160"><span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**il \_ nome dell'account Pianifica E non è stato \_ \_ \_ \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="1ca64-160"><span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**SCHED\_E\_ACCOUNT\_NAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-161">0x80041310</span><span class="sxs-lookup"><span data-stu-id="1ca64-161">0x80041310</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-162">Impossibile stabilire l'esistenza dell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="1ca64-162">Unable to establish existence of the account specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-163"><span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**Pianifica \_ E \_ account \_ dBASE \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="1ca64-163"><span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**SCHED\_E\_ACCOUNT\_DBASE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-164">0x80041311</span><span class="sxs-lookup"><span data-stu-id="1ca64-164">0x80041311</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-165">È stato rilevato un danneggiamento nel database di Utilità di pianificazione Security; il database è stato reimpostato.</span><span class="sxs-lookup"><span data-stu-id="1ca64-165">Corruption was detected in the Task Scheduler security database; the database has been reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-166"><span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**Pianifica \_ E \_ nessun \_ servizio di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="1ca64-166"><span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHED\_E\_NO\_SECURITY\_SERVICES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-167">0x80041312</span><span class="sxs-lookup"><span data-stu-id="1ca64-167">0x80041312</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-168">I servizi di sicurezza Utilità di pianificazione sono disponibili solo in Windows NT.</span><span class="sxs-lookup"><span data-stu-id="1ca64-168">Task Scheduler security services are available only on Windows NT.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-169"><span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**Pianifica \_ E \_ \_ versione oggetto \_ sconosciuta**</span><span class="sxs-lookup"><span data-stu-id="1ca64-169"><span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**SCHED\_E\_UNKNOWN\_OBJECT\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-170">0x80041313</span><span class="sxs-lookup"><span data-stu-id="1ca64-170">0x80041313</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-171">La versione dell'oggetto attività non è supportata o non è valida.</span><span class="sxs-lookup"><span data-stu-id="1ca64-171">The task object version is either unsupported or invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-172"><span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**\_opzione account Pianifica E non \_ supportata \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1ca64-172"><span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**SCHED\_E\_UNSUPPORTED\_ACCOUNT\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-173">0x80041314</span><span class="sxs-lookup"><span data-stu-id="1ca64-173">0x80041314</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-174">L'attività è stata configurata con una combinazione non supportata di impostazioni dell'account e di opzioni di run-time.</span><span class="sxs-lookup"><span data-stu-id="1ca64-174">The task has been configured with an unsupported combination of account settings and run time options.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-175"><span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**Pianifica \_ E \_ servizio \_ non \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="1ca64-175"><span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**SCHED\_E\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-176">0x80041315</span><span class="sxs-lookup"><span data-stu-id="1ca64-176">0x80041315</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-177">Il servizio Utilità di pianificazione non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1ca64-177">The Task Scheduler Service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-178"><span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**Pianifica \_ E \_ UNEXPECTEDNODE**</span><span class="sxs-lookup"><span data-stu-id="1ca64-178"><span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**SCHED\_E\_UNEXPECTEDNODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-179">0x80041316</span><span class="sxs-lookup"><span data-stu-id="1ca64-179">0x80041316</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-180">Il codice XML dell'attività contiene un nodo imprevisto.</span><span class="sxs-lookup"><span data-stu-id="1ca64-180">The task XML contains an unexpected node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-181"><span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**\_ \_ spazio dei nomi Pianifica E**</span><span class="sxs-lookup"><span data-stu-id="1ca64-181"><span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**SCHED\_E\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-182">0x80041317</span><span class="sxs-lookup"><span data-stu-id="1ca64-182">0x80041317</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-183">Il codice XML dell'attività contiene un elemento o un attributo da uno spazio dei nomi imprevisto.</span><span class="sxs-lookup"><span data-stu-id="1ca64-183">The task XML contains an element or attribute from an unexpected namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-184"><span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**Pianifica \_ E \_ INVALIDVALUE**</span><span class="sxs-lookup"><span data-stu-id="1ca64-184"><span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**SCHED\_E\_INVALIDVALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-185">0x80041318</span><span class="sxs-lookup"><span data-stu-id="1ca64-185">0x80041318</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-186">Il codice XML dell'attività contiene un valore che non è formattato correttamente o non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="1ca64-186">The task XML contains a value which is incorrectly formatted or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-187"><span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**Pianifica \_ E \_ MISSINGNODE**</span><span class="sxs-lookup"><span data-stu-id="1ca64-187"><span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**SCHED\_E\_MISSINGNODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-188">0x80041319</span><span class="sxs-lookup"><span data-stu-id="1ca64-188">0x80041319</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-189">Nell'XML dell'attività manca un elemento o un attributo obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1ca64-189">The task XML is missing a required element or attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-190"><span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**Pianifica \_ E \_ MALFORMEDXML**</span><span class="sxs-lookup"><span data-stu-id="1ca64-190"><span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**SCHED\_E\_MALFORMEDXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-191">0x8004131A</span><span class="sxs-lookup"><span data-stu-id="1ca64-191">0x8004131A</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-192">Il formato del codice XML dell'attività non è valido.</span><span class="sxs-lookup"><span data-stu-id="1ca64-192">The task XML is malformed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-193"><span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**Pianifica \_ \_ alcuni \_ trigger \_ non riusciti**</span><span class="sxs-lookup"><span data-stu-id="1ca64-193"><span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**SCHED\_S\_SOME\_TRIGGERS\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-194">0x0004131B</span><span class="sxs-lookup"><span data-stu-id="1ca64-194">0x0004131B</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-195">L'attività è registrata, ma non tutti i trigger specificati avvierà l'attività.</span><span class="sxs-lookup"><span data-stu-id="1ca64-195">The task is registered, but not all specified triggers will start the task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-196"><span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**\_problema di \_ \_ accesso batch Pianifica S \_**</span><span class="sxs-lookup"><span data-stu-id="1ca64-196"><span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**SCHED\_S\_BATCH\_LOGON\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-197">0x0004131C</span><span class="sxs-lookup"><span data-stu-id="1ca64-197">0x0004131C</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-198">L'attività è registrata, ma potrebbe non essere avviata.</span><span class="sxs-lookup"><span data-stu-id="1ca64-198">The task is registered, but may fail to start.</span></span> <span data-ttu-id="1ca64-199">Il privilegio di accesso batch deve essere abilitato per l'entità attività.</span><span class="sxs-lookup"><span data-stu-id="1ca64-199">Batch logon privilege needs to be enabled for the task principal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-200"><span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**Pianifica \_ E \_ troppi \_ \_ nodi**</span><span class="sxs-lookup"><span data-stu-id="1ca64-200"><span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**SCHED\_E\_TOO\_MANY\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-201">0x8004131D</span><span class="sxs-lookup"><span data-stu-id="1ca64-201">0x8004131D</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-202">Il codice XML dell'attività contiene troppi nodi dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="1ca64-202">The task XML contains too many nodes of the same type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-203"><span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**Pianifica \_ E \_ \_ limite finale finale \_**</span><span class="sxs-lookup"><span data-stu-id="1ca64-203"><span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**SCHED\_E\_PAST\_END\_BOUNDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-204">0x8004131E</span><span class="sxs-lookup"><span data-stu-id="1ca64-204">0x8004131E</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-205">Non è possibile avviare l'attività dopo il limite finale del trigger.</span><span class="sxs-lookup"><span data-stu-id="1ca64-205">The task cannot be started after the trigger end boundary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-206"><span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**Pianifica \_ E \_ già \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="1ca64-206"><span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHED\_E\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-207">0x8004131F</span><span class="sxs-lookup"><span data-stu-id="1ca64-207">0x8004131F</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-208">Un'istanza di questa attività è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1ca64-208">An instance of this task is already running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-209"><span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**\_ \_ utente di Pianifica E \_ non \_ connesso \_**</span><span class="sxs-lookup"><span data-stu-id="1ca64-209"><span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**SCHED\_E\_USER\_NOT\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-210">0x80041320</span><span class="sxs-lookup"><span data-stu-id="1ca64-210">0x80041320</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-211">L'attività non verrà eseguita perché l'utente non è connesso.</span><span class="sxs-lookup"><span data-stu-id="1ca64-211">The task will not run because the user is not logged on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-212"><span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**Pianifica \_ E \_ \_ hash attività non valido \_**</span><span class="sxs-lookup"><span data-stu-id="1ca64-212"><span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**SCHED\_E\_INVALID\_TASK\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-213">0x80041321</span><span class="sxs-lookup"><span data-stu-id="1ca64-213">0x80041321</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-214">L'immagine dell'attività è danneggiata o è stata manomessa.</span><span class="sxs-lookup"><span data-stu-id="1ca64-214">The task image is corrupt or has been tampered with.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-215"><span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**Pianifica \_ E \_ servizio \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="1ca64-215"><span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**SCHED\_E\_SERVICE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-216">0x80041322</span><span class="sxs-lookup"><span data-stu-id="1ca64-216">0x80041322</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-217">Il servizio Utilità di pianificazione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="1ca64-217">The Task Scheduler service is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-218"><span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**Pianifica \_ E \_ servizio \_ troppo \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="1ca64-218"><span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**SCHED\_E\_SERVICE\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-219">0x80041323</span><span class="sxs-lookup"><span data-stu-id="1ca64-219">0x80041323</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-220">Il servizio Utilità di pianificazione è troppo occupato per gestire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="1ca64-220">The Task Scheduler service is too busy to handle your request.</span></span> <span data-ttu-id="1ca64-221">Riprova più tardi.</span><span class="sxs-lookup"><span data-stu-id="1ca64-221">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-222"><span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**tentativo di Pianifica \_ E \_ attività \_**</span><span class="sxs-lookup"><span data-stu-id="1ca64-222"><span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**SCHED\_E\_TASK\_ATTEMPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-223">0x80041324</span><span class="sxs-lookup"><span data-stu-id="1ca64-223">0x80041324</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-224">Il servizio Utilità di pianificazione ha tentato di eseguire l'attività, ma l'attività non è stata eseguita a causa di uno dei vincoli nella definizione di attività.</span><span class="sxs-lookup"><span data-stu-id="1ca64-224">The Task Scheduler service attempted to run the task, but the task did not run due to one of the constraints in the task definition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-225"><span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**\_attività pianifica \_ in \_ coda**</span><span class="sxs-lookup"><span data-stu-id="1ca64-225"><span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**SCHED\_S\_TASK\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-226">0x00041325</span><span class="sxs-lookup"><span data-stu-id="1ca64-226">0x00041325</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-227">Il servizio Utilità di pianificazione ha richiesto l'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="1ca64-227">The Task Scheduler service has asked the task to run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-228"><span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**\_attività pianifica \_ E \_ disabilitata**</span><span class="sxs-lookup"><span data-stu-id="1ca64-228"><span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**SCHED\_E\_TASK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-229">0x80041326</span><span class="sxs-lookup"><span data-stu-id="1ca64-229">0x80041326</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-230">L'attività è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="1ca64-230">The task is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-231"><span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**Pianifica \_ E \_ attività \_ non \_ v1 v1 \_**</span><span class="sxs-lookup"><span data-stu-id="1ca64-231"><span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**SCHED\_E\_TASK\_NOT\_V1\_COMPAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-232">0x80041327</span><span class="sxs-lookup"><span data-stu-id="1ca64-232">0x80041327</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-233">L'attività dispone di proprietà che non sono compatibili con le versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="1ca64-233">The task has properties that are not compatible with earlier versions of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1ca64-234"><span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**Pianifica \_ E \_ avvio \_ su \_ richiesta**</span><span class="sxs-lookup"><span data-stu-id="1ca64-234"><span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**SCHED\_E\_START\_ON\_DEMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca64-235">0x80041328</span><span class="sxs-lookup"><span data-stu-id="1ca64-235">0x80041328</span></span>
</dt> <dt>



<span data-ttu-id="1ca64-236">Le impostazioni dell'attività non consentono l'avvio su richiesta dell'attività.</span><span class="sxs-lookup"><span data-stu-id="1ca64-236">The task settings do not allow the task to start on demand.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ca64-237">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ca64-237">Requirements</span></span>



| <span data-ttu-id="1ca64-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ca64-238">Requirement</span></span> | <span data-ttu-id="1ca64-239">Valore</span><span class="sxs-lookup"><span data-stu-id="1ca64-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ca64-240">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ca64-240">Minimum supported client</span></span><br/> | <span data-ttu-id="1ca64-241">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ca64-241">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ca64-242">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ca64-242">Minimum supported server</span></span><br/> | <span data-ttu-id="1ca64-243">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1ca64-243">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ca64-244">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ca64-244">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ca64-245"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ca64-245"><dt>WinError.h</dt></span></span> </dl> |



 

 





