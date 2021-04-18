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
# <a name="triggercollectioncreate-method"></a><span data-ttu-id="abb08-107">TriggerCollection. Create (metodo)</span><span class="sxs-lookup"><span data-stu-id="abb08-107">TriggerCollection.Create method</span></span>

<span data-ttu-id="abb08-108">Per lo scripting crea un nuovo trigger per l'attività.</span><span class="sxs-lookup"><span data-stu-id="abb08-108">For scripting, creates a new trigger for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="abb08-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abb08-109">Syntax</span></span>


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a><span data-ttu-id="abb08-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="abb08-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abb08-111">*tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="abb08-111">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abb08-112">Questo parametro è impostato su una delle seguenti costanti di enumerazione [**\_ \_ tipo2 del trigger di attività**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) .</span><span class="sxs-lookup"><span data-stu-id="abb08-112">This parameter is set to one of the following [**TASK\_TRIGGER\_TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) enumeration constants.</span></span>



| <span data-ttu-id="abb08-113">Valore</span><span class="sxs-lookup"><span data-stu-id="abb08-113">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="abb08-114">Significato</span><span class="sxs-lookup"><span data-stu-id="abb08-114">Meaning</span></span>                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <span data-ttu-id="abb08-115"><dt>**Attività \_ \_Evento trigger**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="abb08-115"><dt>**TASK\_TRIGGER\_EVENT**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="abb08-116">Attiva l'attività quando si verifica un evento specifico.</span><span class="sxs-lookup"><span data-stu-id="abb08-116">Triggers the task when a specific event occurs.</span></span><br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <span data-ttu-id="abb08-117"><dt>**Attività \_ \_Ora di attivazione**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="abb08-117"><dt>**TASK\_TRIGGER\_TIME**</dt> <dt>1</dt></span></span> </dl>                                                    | <span data-ttu-id="abb08-118">Attiva l'attività in un'ora specifica del giorno.</span><span class="sxs-lookup"><span data-stu-id="abb08-118">Triggers the task at a specific time of day.</span></span><br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <span data-ttu-id="abb08-119"><dt>**Attività \_ TRIGGER \_ giornaliero**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="abb08-119"><dt>**TASK\_TRIGGER\_DAILY**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="abb08-120">Attiva l'attività in base a una pianificazione giornaliera.</span><span class="sxs-lookup"><span data-stu-id="abb08-120">Triggers the task on a daily schedule.</span></span> <span data-ttu-id="abb08-121">Ad esempio, l'attività viene avviata a un'ora specifica ogni giorno, ogni giorno, ogni tre giorni e così via.</span><span class="sxs-lookup"><span data-stu-id="abb08-121">For example, the task starts at a specific time every day, every-other day, every third day, and so on.</span></span><br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <span data-ttu-id="abb08-122"><dt>**Attività \_ ATTIVA \_ settimanalmente**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="abb08-122"><dt>**TASK\_TRIGGER\_WEEKLY**</dt> <dt>3</dt></span></span> </dl>                                              | <span data-ttu-id="abb08-123">Attiva l'attività in base a una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="abb08-123">Triggers the task on a weekly schedule.</span></span> <span data-ttu-id="abb08-124">Ad esempio, l'attività inizia alle 8:00 di un giorno specifico ogni settimana o altra settimana.</span><span class="sxs-lookup"><span data-stu-id="abb08-124">For example, the task starts at 8:00 AM on a specific day every week or other week.</span></span><br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <span data-ttu-id="abb08-125"><dt>**Attività \_ TRIGGER \_ mensile**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="abb08-125"><dt>**TASK\_TRIGGER\_MONTHLY**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="abb08-126">Attiva l'attività in base a una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="abb08-126">Triggers the task on a monthly schedule.</span></span> <span data-ttu-id="abb08-127">Ad esempio, l'attività viene avviata in giorni specifici di mesi specifici.</span><span class="sxs-lookup"><span data-stu-id="abb08-127">For example, the task starts on specific days of specific months.</span></span><br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <span data-ttu-id="abb08-128"><dt>**Attività \_ ATTIVA \_ MONTHLYDOW**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="abb08-128"><dt>**TASK\_TRIGGER\_MONTHLYDOW**</dt> <dt>5</dt></span></span> </dl>                                  | <span data-ttu-id="abb08-129">Attiva l'attività in base a una pianificazione mensile giornaliera della settimana.</span><span class="sxs-lookup"><span data-stu-id="abb08-129">Triggers the task on a monthly day-of-week schedule.</span></span> <span data-ttu-id="abb08-130">Ad esempio, l'attività viene avviata in base a giorni specifici della settimana, settimane del mese e mesi dell'anno.</span><span class="sxs-lookup"><span data-stu-id="abb08-130">For example, the task starts on a specific days of the week, weeks of the month, and months of the year.</span></span><br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <span data-ttu-id="abb08-131"><dt>**Attività \_ ATTIVA \_ inattività**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="abb08-131"><dt>**TASK\_TRIGGER\_IDLE**</dt> <dt>6</dt></span></span> </dl>                                                    | <span data-ttu-id="abb08-132">Attiva l'attività quando il computer entra in uno stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="abb08-132">Triggers the task when the computer goes into an idle state.</span></span><br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <span data-ttu-id="abb08-133"><dt>**Attività \_ ATTIVAZIONE \_ registrazione**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="abb08-133"><dt>**TASK\_TRIGGER\_REGISTRATION**</dt> <dt>7</dt></span></span> </dl>                            | <span data-ttu-id="abb08-134">Attiva l'attività quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="abb08-134">Triggers the task when the task is registered.</span></span><br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <span data-ttu-id="abb08-135"><dt>**Attività \_ ATTIVA \_ avvio**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="abb08-135"><dt>**TASK\_TRIGGER\_BOOT**</dt> <dt>8</dt></span></span> </dl>                                                    | <span data-ttu-id="abb08-136">Attiva l'attività all'avvio del computer.</span><span class="sxs-lookup"><span data-stu-id="abb08-136">Triggers the task when the computer boots.</span></span><br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <span data-ttu-id="abb08-137"><dt>**Attività \_ ATTIVARE l' \_ accesso**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="abb08-137"><dt>**TASK\_TRIGGER\_LOGON**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="abb08-138">Attiva l'attività quando un utente specifico esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="abb08-138">Triggers the task when a specific user logs on.</span></span><br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <span data-ttu-id="abb08-139"><dt>**Attività \_ ATTIVA \_ \_ \_ modifica stato sessione**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="abb08-139"><dt>**TASK\_TRIGGER\_SESSION\_STATE\_CHANGE**</dt> <dt>11</dt></span></span> </dl> | <span data-ttu-id="abb08-140">Attiva l'attività quando viene modificato uno specifico stato della sessione.</span><span class="sxs-lookup"><span data-stu-id="abb08-140">Triggers the task when a specific session state changes.</span></span><br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abb08-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="abb08-141">Return value</span></span>

<span data-ttu-id="abb08-142">Oggetto [**trigger**](trigger.md) che rappresenta il nuovo trigger.</span><span class="sxs-lookup"><span data-stu-id="abb08-142">A [**Trigger**](trigger.md) object that represents the new trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="abb08-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="abb08-143">Remarks</span></span>

<span data-ttu-id="abb08-144">Per informazioni su ogni tipo di trigger, vedere [tipi di trigger](trigger-types.md).</span><span class="sxs-lookup"><span data-stu-id="abb08-144">For information about each trigger type see [Trigger Types](trigger-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abb08-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abb08-145">Requirements</span></span>



| <span data-ttu-id="abb08-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="abb08-146">Requirement</span></span> | <span data-ttu-id="abb08-147">Valore</span><span class="sxs-lookup"><span data-stu-id="abb08-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abb08-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abb08-148">Minimum supported client</span></span><br/> | <span data-ttu-id="abb08-149">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="abb08-149">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="abb08-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abb08-150">Minimum supported server</span></span><br/> | <span data-ttu-id="abb08-151">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="abb08-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="abb08-152">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="abb08-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="abb08-153"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="abb08-153"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="abb08-154">DLL</span><span class="sxs-lookup"><span data-stu-id="abb08-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abb08-155"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abb08-155"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abb08-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="abb08-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abb08-157">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="abb08-157">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="abb08-158">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="abb08-158">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





