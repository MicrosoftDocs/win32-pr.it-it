---
title: Oggetto MonthlyDOWTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione mensile del giorno della settimana.
ms.assetid: 18607189-295f-4f7d-bf72-f0ac8d5067cf
keywords:
- Utilità di pianificazione trigger DOW mensile, oggetto
- Utilità di pianificazione oggetto MonthlyDOWTrigger
- Oggetto MonthlyDOWTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7e43925c6ebe27933a39fe5e25f37ffe6cf72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048154"
---
# <a name="monthlydowtrigger-object"></a><span data-ttu-id="d35ca-106">Oggetto MonthlyDOWTrigger</span><span class="sxs-lookup"><span data-stu-id="d35ca-106">MonthlyDOWTrigger object</span></span>

<span data-ttu-id="d35ca-107">Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="d35ca-107">Scripting object that represents a trigger that starts a task on a monthly day-of-week schedule.</span></span> <span data-ttu-id="d35ca-108">Ad esempio, l'attività viene avviata a ogni primo giovedì, da maggio a ottobre.</span><span class="sxs-lookup"><span data-stu-id="d35ca-108">For example, the task starts on every first Thursday, May through October.</span></span>

## <a name="members"></a><span data-ttu-id="d35ca-109">Membri</span><span class="sxs-lookup"><span data-stu-id="d35ca-109">Members</span></span>

<span data-ttu-id="d35ca-110">L'oggetto **MonthlyDOWTrigger** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d35ca-110">The **MonthlyDOWTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="d35ca-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d35ca-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d35ca-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d35ca-112">Properties</span></span>

<span data-ttu-id="d35ca-113">L'oggetto **MonthlyDOWTrigger** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d35ca-113">The **MonthlyDOWTrigger** object has these properties.</span></span>



| <span data-ttu-id="d35ca-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d35ca-114">Property</span></span>                                                                          | <span data-ttu-id="d35ca-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="d35ca-115">Access type</span></span>           | <span data-ttu-id="d35ca-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d35ca-116">Description</span></span>                                                                                                                                                                                 |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d35ca-117">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="d35ca-117">**DaysOfWeek**</span></span>](monthlydowtrigger-daysofweek.md)<br/>                     | <span data-ttu-id="d35ca-118">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="d35ca-118">Read/write</span></span><br/> | <span data-ttu-id="d35ca-119">Ottiene o imposta i giorni della settimana durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="d35ca-119">Gets or sets the days of the week during which the task runs.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="d35ca-120">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="d35ca-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                                     | <span data-ttu-id="d35ca-121">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="d35ca-121">Read/write</span></span><br/> | <span data-ttu-id="d35ca-122">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d35ca-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d35ca-123">Ottiene o imposta un valore booleano che indica se il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="d35ca-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="d35ca-124">EndBoundary</span><span class="sxs-lookup"><span data-stu-id="d35ca-124">EndBoundary</span></span>](trigger-endboundary.md)<br/>                                 | <span data-ttu-id="d35ca-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="d35ca-125">Read/write</span></span><br/> | <span data-ttu-id="d35ca-126">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d35ca-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d35ca-127">Ottiene o imposta la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="d35ca-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="d35ca-128">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="d35ca-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="d35ca-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="d35ca-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/>               | <span data-ttu-id="d35ca-130">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="d35ca-130">Read/write</span></span><br/> | <span data-ttu-id="d35ca-131">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d35ca-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d35ca-132">Ottiene o imposta il periodo di tempo massimo durante il quale l'attività avviata da questo trigger può essere eseguita.</span><span class="sxs-lookup"><span data-stu-id="d35ca-132">Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.</span></span><br/>                          |
| [<span data-ttu-id="d35ca-133">**ID**</span><span class="sxs-lookup"><span data-stu-id="d35ca-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                              | <span data-ttu-id="d35ca-134">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="d35ca-134">Read/write</span></span><br/> | <span data-ttu-id="d35ca-135">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d35ca-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d35ca-136">Ottiene o imposta l'identificatore per il trigger.</span><span class="sxs-lookup"><span data-stu-id="d35ca-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="d35ca-137">**MonthsOfYear**</span><span class="sxs-lookup"><span data-stu-id="d35ca-137">**MonthsOfYear**</span></span>](monthlydowtrigger-monthsofyear.md)<br/>                 | <span data-ttu-id="d35ca-138">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="d35ca-138">Read/write</span></span><br/> | <span data-ttu-id="d35ca-139">Ottiene o imposta i mesi dell'anno durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="d35ca-139">Gets or sets the months of the year during which the task runs.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="d35ca-140">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="d35ca-140">**RandomDelay**</span></span>](monthlydowtrigger-randomdelay.md)<br/>                   | <span data-ttu-id="d35ca-141">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="d35ca-141">Read/write</span></span><br/> | <span data-ttu-id="d35ca-142">Ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="d35ca-142">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="d35ca-143">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="d35ca-143">**Repetition**</span></span>](trigger-repetition.md)<br/>                               | <span data-ttu-id="d35ca-144">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="d35ca-144">Read/write</span></span><br/> | <span data-ttu-id="d35ca-145">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d35ca-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d35ca-146">Ottiene o imposta la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="d35ca-146">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="d35ca-147">**RunOnLastWeekOfMonth**</span><span class="sxs-lookup"><span data-stu-id="d35ca-147">**RunOnLastWeekOfMonth**</span></span>](monthlydowtrigger-runonlastweekofmonth.md)<br/> | <span data-ttu-id="d35ca-148">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="d35ca-148">Read/write</span></span><br/> | <span data-ttu-id="d35ca-149">Ottiene o imposta un valore booleano che indica che l'attività viene eseguita l'ultima settimana del mese.</span><span class="sxs-lookup"><span data-stu-id="d35ca-149">Gets or sets a Boolean value that indicates that the task runs on the last week of the month.</span></span><br/>                                                                                    |
| [<span data-ttu-id="d35ca-150">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="d35ca-150">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>                         | <span data-ttu-id="d35ca-151">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="d35ca-151">Read/write</span></span><br/> | <span data-ttu-id="d35ca-152">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d35ca-152">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d35ca-153">Ottiene o imposta la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="d35ca-153">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="d35ca-154">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d35ca-154">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                          | <span data-ttu-id="d35ca-155">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d35ca-155">Read-only</span></span><br/>  | <span data-ttu-id="d35ca-156">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="d35ca-156">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="d35ca-157">Ottiene il tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="d35ca-157">Gets the type of the trigger.</span></span><br/>                                                                                              |
| [<span data-ttu-id="d35ca-158">**WeeksOfMonth**</span><span class="sxs-lookup"><span data-stu-id="d35ca-158">**WeeksOfMonth**</span></span>](monthlydowtrigger-weeksofmonth.md)<br/>                 | <span data-ttu-id="d35ca-159">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="d35ca-159">Read/write</span></span><br/> | <span data-ttu-id="d35ca-160">Ottiene o imposta le settimane del mese durante le quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="d35ca-160">Gets or sets the weeks of the month during which the task runs.</span></span><br/>                                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="d35ca-161">Commenti</span><span class="sxs-lookup"><span data-stu-id="d35ca-161">Remarks</span></span>

<span data-ttu-id="d35ca-162">L'ora del giorno in cui l'attività viene avviata è impostata dalla proprietà [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="d35ca-162">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="d35ca-163">Durante la lettura o la scrittura di codice XML per un'attività, viene specificato un trigger di giorno della settimana mensile utilizzando l'elemento [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d35ca-163">When reading or writing XML for a task, a monthly day-of-week trigger is specified using the [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d35ca-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d35ca-164">Requirements</span></span>



| <span data-ttu-id="d35ca-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="d35ca-165">Requirement</span></span> | <span data-ttu-id="d35ca-166">Valore</span><span class="sxs-lookup"><span data-stu-id="d35ca-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d35ca-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d35ca-167">Minimum supported client</span></span><br/> | <span data-ttu-id="d35ca-168">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d35ca-168">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d35ca-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d35ca-169">Minimum supported server</span></span><br/> | <span data-ttu-id="d35ca-170">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d35ca-170">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d35ca-171">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d35ca-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="d35ca-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d35ca-172"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d35ca-173">DLL</span><span class="sxs-lookup"><span data-stu-id="d35ca-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d35ca-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d35ca-174"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d35ca-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d35ca-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d35ca-176">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="d35ca-176">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="d35ca-177">Oggetti Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d35ca-177">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="d35ca-178">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d35ca-178">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d35ca-179">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="d35ca-179">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="d35ca-180">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="d35ca-180">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





