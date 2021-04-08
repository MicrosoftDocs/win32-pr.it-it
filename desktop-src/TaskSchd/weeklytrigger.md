---
title: Oggetto WeeklyTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione settimanale.
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- Utilità di pianificazione trigger settimanale, oggetto
- Utilità di pianificazione oggetto WeeklyTrigger
- Oggetto WeeklyTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- WeeklyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58dec9172d38b53f779f44a048b39bc709dbd54f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743850"
---
# <a name="weeklytrigger-object"></a><span data-ttu-id="b85f0-106">Oggetto WeeklyTrigger</span><span class="sxs-lookup"><span data-stu-id="b85f0-106">WeeklyTrigger object</span></span>

<span data-ttu-id="b85f0-107">Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="b85f0-107">Scripting object that represents a trigger that starts a task based on a weekly schedule.</span></span> <span data-ttu-id="b85f0-108">Ad esempio, l'attività inizia alle ore 8:00.</span><span class="sxs-lookup"><span data-stu-id="b85f0-108">For example, the task starts at 8:00 A.M.</span></span> <span data-ttu-id="b85f0-109">in un giorno specifico della settimana o ogni settimana.</span><span class="sxs-lookup"><span data-stu-id="b85f0-109">on a specific day of the week every week or every other week.</span></span>

## <a name="members"></a><span data-ttu-id="b85f0-110">Membri</span><span class="sxs-lookup"><span data-stu-id="b85f0-110">Members</span></span>

<span data-ttu-id="b85f0-111">L'oggetto **WeeklyTrigger** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b85f0-111">The **WeeklyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="b85f0-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b85f0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b85f0-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b85f0-113">Properties</span></span>

<span data-ttu-id="b85f0-114">L'oggetto **WeeklyTrigger** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b85f0-114">The **WeeklyTrigger** object has these properties.</span></span>



| <span data-ttu-id="b85f0-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b85f0-115">Property</span></span>                                                            | <span data-ttu-id="b85f0-116">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="b85f0-116">Access type</span></span>           | <span data-ttu-id="b85f0-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b85f0-117">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b85f0-118">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="b85f0-118">**DaysOfWeek**</span></span>](weeklytrigger-daysofweek.md)<br/>           | <span data-ttu-id="b85f0-119">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b85f0-119">Read/write</span></span><br/> | <span data-ttu-id="b85f0-120">Ottiene o imposta i giorni della settimana in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="b85f0-120">Gets or sets the days of the week on which the task runs.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="b85f0-121">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="b85f0-121">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="b85f0-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b85f0-122">Read/write</span></span><br/> | <span data-ttu-id="b85f0-123">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="b85f0-123">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b85f0-124">Ottiene o imposta un valore booleano che indica se il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b85f0-124">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="b85f0-125">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="b85f0-125">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="b85f0-126">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b85f0-126">Read/write</span></span><br/> | <span data-ttu-id="b85f0-127">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="b85f0-127">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b85f0-128">Ottiene o imposta la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="b85f0-128">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="b85f0-129">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="b85f0-129">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="b85f0-130">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="b85f0-130">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="b85f0-131">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b85f0-131">Read/write</span></span><br/> | <span data-ttu-id="b85f0-132">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="b85f0-132">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b85f0-133">Ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="b85f0-133">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="b85f0-134">**ID**</span><span class="sxs-lookup"><span data-stu-id="b85f0-134">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="b85f0-135">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b85f0-135">Read/write</span></span><br/> | <span data-ttu-id="b85f0-136">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="b85f0-136">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b85f0-137">Ottiene o imposta l'identificatore per il trigger.</span><span class="sxs-lookup"><span data-stu-id="b85f0-137">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="b85f0-138">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="b85f0-138">**RandomDelay**</span></span>](weeklytrigger-randomdelay.md)<br/>         | <span data-ttu-id="b85f0-139">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b85f0-139">Read/write</span></span><br/> | <span data-ttu-id="b85f0-140">Ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="b85f0-140">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="b85f0-141">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="b85f0-141">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="b85f0-142">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b85f0-142">Read/write</span></span><br/> | <span data-ttu-id="b85f0-143">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="b85f0-143">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b85f0-144">Ottiene o imposta la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="b85f0-144">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="b85f0-145">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="b85f0-145">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="b85f0-146">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b85f0-146">Read/write</span></span><br/> | <span data-ttu-id="b85f0-147">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="b85f0-147">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b85f0-148">Ottiene o imposta la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="b85f0-148">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="b85f0-149">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b85f0-149">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="b85f0-150">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b85f0-150">Read-only</span></span><br/>  | <span data-ttu-id="b85f0-151">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="b85f0-151">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b85f0-152">Ottiene il tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="b85f0-152">Gets the type of the trigger.</span></span><br/>                                                                                              |
| [<span data-ttu-id="b85f0-153">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="b85f0-153">**WeeksInterval**</span></span>](weeklytrigger-weeksinterval.md)<br/>     | <span data-ttu-id="b85f0-154">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b85f0-154">Read/write</span></span><br/> | <span data-ttu-id="b85f0-155">Ottiene o imposta l'intervallo tra le settimane nella pianificazione.</span><span class="sxs-lookup"><span data-stu-id="b85f0-155">Gets or sets the interval between the weeks in the schedule.</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="b85f0-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="b85f0-156">Remarks</span></span>

<span data-ttu-id="b85f0-157">L'ora del giorno in cui l'attività viene avviata è impostata dalla proprietà [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="b85f0-157">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="b85f0-158">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificato un trigger settimanale usando l'elemento [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="b85f0-158">When reading or writing your own XML for a task, a weekly trigger is specified using the [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="b85f0-159">Esempio</span><span class="sxs-lookup"><span data-stu-id="b85f0-159">Examples</span></span>

<span data-ttu-id="b85f0-160">Per ulteriori informazioni e un esempio di codice per questo oggetto di scripting, vedere l' [esempio di trigger settimanale (scripting)](weekly-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="b85f0-160">For more information and a code example for this scripting object, see [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b85f0-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b85f0-161">Requirements</span></span>



| <span data-ttu-id="b85f0-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="b85f0-162">Requirement</span></span> | <span data-ttu-id="b85f0-163">Valore</span><span class="sxs-lookup"><span data-stu-id="b85f0-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b85f0-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b85f0-164">Minimum supported client</span></span><br/> | <span data-ttu-id="b85f0-165">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b85f0-165">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b85f0-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b85f0-166">Minimum supported server</span></span><br/> | <span data-ttu-id="b85f0-167">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b85f0-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b85f0-168">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b85f0-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="b85f0-169"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b85f0-169"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b85f0-170">DLL</span><span class="sxs-lookup"><span data-stu-id="b85f0-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b85f0-171"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b85f0-171"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b85f0-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b85f0-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b85f0-173">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="b85f0-173">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="b85f0-174">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="b85f0-174">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="b85f0-175">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="b85f0-175">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





