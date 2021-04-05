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
# <a name="triggertype-property"></a><span data-ttu-id="b3bb0-106">Proprietà trigger. Type</span><span class="sxs-lookup"><span data-stu-id="b3bb0-106">Trigger.Type property</span></span>

<span data-ttu-id="b3bb0-107">Per lo scripting, ottiene il tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="b3bb0-107">For scripting, gets the type of the trigger.</span></span> <span data-ttu-id="b3bb0-108">Il tipo di trigger viene definito quando il trigger viene creato e non può essere modificato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="b3bb0-108">The trigger type is defined when the trigger is created and cannot be changed later.</span></span> <span data-ttu-id="b3bb0-109">Per informazioni sulla creazione di un trigger, vedere [**TriggerCollection. Create**](triggercollection-create.md).</span><span class="sxs-lookup"><span data-stu-id="b3bb0-109">For information on creating a trigger, see [**TriggerCollection.Create**](triggercollection-create.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b3bb0-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3bb0-110">Syntax</span></span>


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a><span data-ttu-id="b3bb0-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b3bb0-111">Property value</span></span>

<span data-ttu-id="b3bb0-112">Uno dei valori di [**enumerazione \_ \_ tipo2 del trigger dell'attività**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) seguente.</span><span class="sxs-lookup"><span data-stu-id="b3bb0-112">One of the following [**TASK\_TRIGGER\_TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) enumeration values.</span></span>



| <span data-ttu-id="b3bb0-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b3bb0-113">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="b3bb0-114">Significato</span><span class="sxs-lookup"><span data-stu-id="b3bb0-114">Meaning</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <span data-ttu-id="b3bb0-115"><dt>**Attività \_ \_Evento trigger**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb0-115"><dt>**TASK\_TRIGGER\_EVENT**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="b3bb0-116">Avvia l'attività quando si verifica un evento specifico.</span><span class="sxs-lookup"><span data-stu-id="b3bb0-116">Starts the task when a specific event occurs.</span></span><br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <span data-ttu-id="b3bb0-117"><dt>**Attività \_ \_Ora di attivazione**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb0-117"><dt>**TASK\_TRIGGER\_TIME**</dt> <dt>1</dt></span></span> </dl>                                                    | <span data-ttu-id="b3bb0-118">Avvia l'attività in un'ora specifica del giorno.</span><span class="sxs-lookup"><span data-stu-id="b3bb0-118">Starts the task at a specific time of day.</span></span><br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <span data-ttu-id="b3bb0-119"><dt>**Attività \_ TRIGGER \_ giornaliero**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb0-119"><dt>**TASK\_TRIGGER\_DAILY**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="b3bb0-120">Avvia l'attività ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="b3bb0-120">Starts the task daily.</span></span><br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <span data-ttu-id="b3bb0-121"><dt>**Attività \_ ATTIVA \_ settimanalmente**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb0-121"><dt>**TASK\_TRIGGER\_WEEKLY**</dt> <dt>3</dt></span></span> </dl>                                              | <span data-ttu-id="b3bb0-122">Avvia l'attività settimanalmente.</span><span class="sxs-lookup"><span data-stu-id="b3bb0-122">Starts the task weekly.</span></span><br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <span data-ttu-id="b3bb0-123"><dt>**Attività \_ TRIGGER \_ mensile**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb0-123"><dt>**TASK\_TRIGGER\_MONTHLY**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="b3bb0-124">Avvia l'attività ogni mese.</span><span class="sxs-lookup"><span data-stu-id="b3bb0-124">Starts the task monthly.</span></span><br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <span data-ttu-id="b3bb0-125"><dt>**Attività \_ ATTIVA \_ MONTHLYDOW**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb0-125"><dt>**TASK\_TRIGGER\_MONTHLYDOW**</dt> <dt>5</dt></span></span> </dl>                                  | <span data-ttu-id="b3bb0-126">Avvia l'attività ogni mese in un giorno specifico della settimana.</span><span class="sxs-lookup"><span data-stu-id="b3bb0-126">Starts the task every month on a specific day of the week.</span></span><br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <span data-ttu-id="b3bb0-127"><dt>**Attività \_ ATTIVA \_ inattività**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb0-127"><dt>**TASK\_TRIGGER\_IDLE**</dt> <dt>6</dt></span></span> </dl>                                                    | <span data-ttu-id="b3bb0-128">Avvia l'attività quando il computer entra in uno stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="b3bb0-128">Starts the task when the computer goes into an idle state.</span></span><br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <span data-ttu-id="b3bb0-129"><dt>**Attività \_ ATTIVAZIONE \_ registrazione**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb0-129"><dt>**TASK\_TRIGGER\_REGISTRATION**</dt> <dt>7</dt></span></span> </dl>                            | <span data-ttu-id="b3bb0-130">Avvia l'attività quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="b3bb0-130">Starts the task when the task is registered.</span></span><br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <span data-ttu-id="b3bb0-131"><dt>**Attività \_ ATTIVA \_ avvio**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb0-131"><dt>**TASK\_TRIGGER\_BOOT**</dt> <dt>8</dt></span></span> </dl>                                                    | <span data-ttu-id="b3bb0-132">Avvia l'attività all'avvio del computer.</span><span class="sxs-lookup"><span data-stu-id="b3bb0-132">Starts the task when the computer boots.</span></span><br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <span data-ttu-id="b3bb0-133"><dt>**Attività \_ ATTIVARE l' \_ accesso**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb0-133"><dt>**TASK\_TRIGGER\_LOGON**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="b3bb0-134">Avvia l'attività quando un utente specifico esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="b3bb0-134">Starts the task when a specific user logs on.</span></span><br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <span data-ttu-id="b3bb0-135"><dt>**Attività \_ ATTIVA \_ \_ \_ modifica stato sessione**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb0-135"><dt>**TASK\_TRIGGER\_SESSION\_STATE\_CHANGE**</dt> <dt>11</dt></span></span> </dl> | <span data-ttu-id="b3bb0-136">Attiva l'attività quando viene modificato uno specifico stato della sessione.</span><span class="sxs-lookup"><span data-stu-id="b3bb0-136">Triggers the task when a specific session state changes.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="b3bb0-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3bb0-137">Requirements</span></span>



| <span data-ttu-id="b3bb0-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3bb0-138">Requirement</span></span> | <span data-ttu-id="b3bb0-139">Valore</span><span class="sxs-lookup"><span data-stu-id="b3bb0-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3bb0-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3bb0-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b3bb0-141">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3bb0-141">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b3bb0-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3bb0-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b3bb0-143">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3bb0-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3bb0-144">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b3bb0-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="b3bb0-145"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb0-145"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b3bb0-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b3bb0-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3bb0-147"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3bb0-147"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3bb0-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3bb0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3bb0-149">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="b3bb0-149">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> <dt>

[<span data-ttu-id="b3bb0-150">**\_Trigger attività \_ tipo2**</span><span class="sxs-lookup"><span data-stu-id="b3bb0-150">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[<span data-ttu-id="b3bb0-151">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="b3bb0-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





