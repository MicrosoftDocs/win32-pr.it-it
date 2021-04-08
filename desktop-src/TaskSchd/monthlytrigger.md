---
title: Oggetto MonthlyTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione mensile.
ms.assetid: d73715cb-a52e-4daf-930f-e94fbe28881e
keywords:
- Utilità di pianificazione trigger mensile, oggetto
- Utilità di pianificazione oggetto MonthlyTrigger
- Oggetto MonthlyTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- MonthlyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce433f626fbe45e209f881c00787495cc6343bc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741882"
---
# <a name="monthlytrigger-object"></a><span data-ttu-id="efeb0-106">Oggetto MonthlyTrigger</span><span class="sxs-lookup"><span data-stu-id="efeb0-106">MonthlyTrigger object</span></span>

<span data-ttu-id="efeb0-107">Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="efeb0-107">Scripting object that represents a trigger that starts a task based on a monthly schedule.</span></span> <span data-ttu-id="efeb0-108">Ad esempio, l'attività viene avviata in giorni specifici di mesi specifici.</span><span class="sxs-lookup"><span data-stu-id="efeb0-108">For example, the task starts on specific days of specific months.</span></span>

## <a name="members"></a><span data-ttu-id="efeb0-109">Membri</span><span class="sxs-lookup"><span data-stu-id="efeb0-109">Members</span></span>

<span data-ttu-id="efeb0-110">L'oggetto **MonthlyTrigger** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="efeb0-110">The **MonthlyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="efeb0-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="efeb0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efeb0-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="efeb0-112">Properties</span></span>

<span data-ttu-id="efeb0-113">L'oggetto **MonthlyTrigger** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="efeb0-113">The **MonthlyTrigger** object has these properties.</span></span>



| <span data-ttu-id="efeb0-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="efeb0-114">Property</span></span>                                                                     | <span data-ttu-id="efeb0-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="efeb0-115">Access type</span></span>           | <span data-ttu-id="efeb0-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efeb0-116">Description</span></span>                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efeb0-117">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="efeb0-117">**DaysOfMonth**</span></span>](monthlytrigger-daysofmonth.md)<br/>                 | <span data-ttu-id="efeb0-118">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="efeb0-118">Read/write</span></span><br/> | <span data-ttu-id="efeb0-119">Ottiene o imposta i giorni del mese durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="efeb0-119">Gets or sets the days of the month during which the task runs.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="efeb0-120">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="efeb0-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                                | <span data-ttu-id="efeb0-121">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="efeb0-121">Read/write</span></span><br/> | <span data-ttu-id="efeb0-122">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="efeb0-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="efeb0-123">Ottiene o imposta un valore booleano che indica se il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="efeb0-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="efeb0-124">EndBoundary</span><span class="sxs-lookup"><span data-stu-id="efeb0-124">EndBoundary</span></span>](trigger-endboundary.md)<br/>                            | <span data-ttu-id="efeb0-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="efeb0-125">Read/write</span></span><br/> | <span data-ttu-id="efeb0-126">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="efeb0-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="efeb0-127">Ottiene o imposta la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="efeb0-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="efeb0-128">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="efeb0-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="efeb0-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="efeb0-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/>          | <span data-ttu-id="efeb0-130">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="efeb0-130">Read/write</span></span><br/> | <span data-ttu-id="efeb0-131">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="efeb0-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="efeb0-132">Ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="efeb0-132">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="efeb0-133">**ID**</span><span class="sxs-lookup"><span data-stu-id="efeb0-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                         | <span data-ttu-id="efeb0-134">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="efeb0-134">Read/write</span></span><br/> | <span data-ttu-id="efeb0-135">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="efeb0-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="efeb0-136">Ottiene o imposta l'identificatore per il trigger.</span><span class="sxs-lookup"><span data-stu-id="efeb0-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="efeb0-137">**MonthsOfYear**</span><span class="sxs-lookup"><span data-stu-id="efeb0-137">**MonthsOfYear**</span></span>](monthlytrigger-monthsofyear.md)<br/>               | <span data-ttu-id="efeb0-138">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="efeb0-138">Read/write</span></span><br/> | <span data-ttu-id="efeb0-139">Ottiene o imposta i mesi dell'anno durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="efeb0-139">Gets or sets the months of the year during which the task runs.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="efeb0-140">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="efeb0-140">**RandomDelay**</span></span>](monthlytrigger-randomdelay.md)<br/>                 | <span data-ttu-id="efeb0-141">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="efeb0-141">Read/write</span></span><br/> | <span data-ttu-id="efeb0-142">Ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="efeb0-142">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="efeb0-143">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="efeb0-143">**Repetition**</span></span>](trigger-repetition.md)<br/>                          | <span data-ttu-id="efeb0-144">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="efeb0-144">Read/write</span></span><br/> | <span data-ttu-id="efeb0-145">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="efeb0-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="efeb0-146">Ottiene o imposta la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="efeb0-146">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="efeb0-147">**RunOnLastDayOfMonth**</span><span class="sxs-lookup"><span data-stu-id="efeb0-147">**RunOnLastDayOfMonth**</span></span>](monthlytrigger-runonlastdayofmonth.md)<br/> | <span data-ttu-id="efeb0-148">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="efeb0-148">Read/write</span></span><br/> | <span data-ttu-id="efeb0-149">Ottiene o imposta un valore booleano che indica che l'attività viene eseguita l'ultimo giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="efeb0-149">Gets or sets a Boolean value that indicates that the task runs on the last day of the month.</span></span><br/>                                                                                     |
| [<span data-ttu-id="efeb0-150">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="efeb0-150">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>                    | <span data-ttu-id="efeb0-151">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="efeb0-151">Read/write</span></span><br/> | <span data-ttu-id="efeb0-152">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="efeb0-152">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="efeb0-153">Ottiene o imposta la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="efeb0-153">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="efeb0-154">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="efeb0-154">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                     | <span data-ttu-id="efeb0-155">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="efeb0-155">Read-only</span></span><br/>  | <span data-ttu-id="efeb0-156">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="efeb0-156">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="efeb0-157">Ottiene il tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="efeb0-157">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="efeb0-158">Commenti</span><span class="sxs-lookup"><span data-stu-id="efeb0-158">Remarks</span></span>

<span data-ttu-id="efeb0-159">L'ora del giorno in cui l'attività viene avviata è impostata dalla proprietà [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="efeb0-159">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="efeb0-160">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificato un trigger mensile utilizzando l'elemento [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="efeb0-160">When reading or writing your own XML for a task, a monthly trigger is specified using the [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="efeb0-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efeb0-161">Requirements</span></span>



| <span data-ttu-id="efeb0-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="efeb0-162">Requirement</span></span> | <span data-ttu-id="efeb0-163">Valore</span><span class="sxs-lookup"><span data-stu-id="efeb0-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efeb0-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efeb0-164">Minimum supported client</span></span><br/> | <span data-ttu-id="efeb0-165">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efeb0-165">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="efeb0-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efeb0-166">Minimum supported server</span></span><br/> | <span data-ttu-id="efeb0-167">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="efeb0-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="efeb0-168">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="efeb0-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="efeb0-169"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="efeb0-169"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="efeb0-170">DLL</span><span class="sxs-lookup"><span data-stu-id="efeb0-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efeb0-171"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efeb0-171"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efeb0-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efeb0-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efeb0-173">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="efeb0-173">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="efeb0-174">Oggetti Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="efeb0-174">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="efeb0-175">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="efeb0-175">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="efeb0-176">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="efeb0-176">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="efeb0-177">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="efeb0-177">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





