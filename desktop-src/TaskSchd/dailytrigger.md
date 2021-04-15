---
title: Oggetto DailyTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione giornaliera.
ms.assetid: f03f53a0-0060-4793-96c1-b47a96852579
keywords:
- Utilità di pianificazione trigger giornaliero, oggetto
- Utilità di pianificazione oggetto DailyTrigger
- Oggetto DailyTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- DailyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22203ecf7a421f07ccb823745e6619e05f84f550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475982"
---
# <a name="dailytrigger-object"></a><span data-ttu-id="73ce3-106">Oggetto DailyTrigger</span><span class="sxs-lookup"><span data-stu-id="73ce3-106">DailyTrigger object</span></span>

<span data-ttu-id="73ce3-107">Oggetto di scripting che rappresenta un trigger che avvia un'attività in base a una pianificazione giornaliera.</span><span class="sxs-lookup"><span data-stu-id="73ce3-107">Scripting object that represents a trigger that starts a task based on a daily schedule.</span></span>

## <a name="members"></a><span data-ttu-id="73ce3-108">Membri</span><span class="sxs-lookup"><span data-stu-id="73ce3-108">Members</span></span>

<span data-ttu-id="73ce3-109">L'oggetto **DailyTrigger** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="73ce3-109">The **DailyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="73ce3-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73ce3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73ce3-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73ce3-111">Properties</span></span>

<span data-ttu-id="73ce3-112">L'oggetto **DailyTrigger** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="73ce3-112">The **DailyTrigger** object has these properties.</span></span>



| <span data-ttu-id="73ce3-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73ce3-113">Property</span></span>                                                            | <span data-ttu-id="73ce3-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="73ce3-114">Access type</span></span>           | <span data-ttu-id="73ce3-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73ce3-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73ce3-116">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="73ce3-116">**DaysInterval**</span></span>](dailytrigger-daysinterval.md)<br/>        | <span data-ttu-id="73ce3-117">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73ce3-117">Read/write</span></span><br/> | <span data-ttu-id="73ce3-118">Ottiene o imposta l'intervallo tra i giorni della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="73ce3-118">Gets or sets the interval between the days in the schedule.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="73ce3-119">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="73ce3-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="73ce3-120">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73ce3-120">Read/write</span></span><br/> | <span data-ttu-id="73ce3-121">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="73ce3-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="73ce3-122">Ottiene o imposta un valore booleano che indica se il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="73ce3-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="73ce3-123">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="73ce3-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="73ce3-124">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73ce3-124">Read/write</span></span><br/> | <span data-ttu-id="73ce3-125">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="73ce3-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="73ce3-126">Ottiene o imposta la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="73ce3-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="73ce3-127">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="73ce3-127">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="73ce3-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="73ce3-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="73ce3-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73ce3-129">Read/write</span></span><br/> | <span data-ttu-id="73ce3-130">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="73ce3-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="73ce3-131">Ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="73ce3-131">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="73ce3-132">**ID**</span><span class="sxs-lookup"><span data-stu-id="73ce3-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="73ce3-133">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73ce3-133">Read/write</span></span><br/> | <span data-ttu-id="73ce3-134">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="73ce3-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="73ce3-135">Ottiene o imposta l'identificatore per il trigger.</span><span class="sxs-lookup"><span data-stu-id="73ce3-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="73ce3-136">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="73ce3-136">**RandomDelay**</span></span>](dailytrigger-randomdelay.md)<br/>          | <span data-ttu-id="73ce3-137">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73ce3-137">Read/write</span></span><br/> | <span data-ttu-id="73ce3-138">Ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="73ce3-138">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="73ce3-139">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="73ce3-139">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="73ce3-140">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73ce3-140">Read/write</span></span><br/> | <span data-ttu-id="73ce3-141">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="73ce3-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="73ce3-142">Ottiene o imposta la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="73ce3-142">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="73ce3-143">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="73ce3-143">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="73ce3-144">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73ce3-144">Read/write</span></span><br/> | <span data-ttu-id="73ce3-145">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="73ce3-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="73ce3-146">Ottiene o imposta la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="73ce3-146">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="73ce3-147">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="73ce3-147">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="73ce3-148">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="73ce3-148">Read-only</span></span><br/>  | <span data-ttu-id="73ce3-149">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="73ce3-149">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="73ce3-150">Ottiene il tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="73ce3-150">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="73ce3-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="73ce3-151">Remarks</span></span>

<span data-ttu-id="73ce3-152">L'ora del giorno in cui l'attività viene avviata è impostata dalla proprietà [**StartBoundary**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="73ce3-152">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="73ce3-153">Un intervallo di 1 produce una pianificazione giornaliera.</span><span class="sxs-lookup"><span data-stu-id="73ce3-153">An interval of 1 produces a daily schedule.</span></span> <span data-ttu-id="73ce3-154">Un intervallo di 2 produce una pianificazione di ogni giorno e così via.</span><span class="sxs-lookup"><span data-stu-id="73ce3-154">An interval of 2 produces an every other day schedule and so on.</span></span>

<span data-ttu-id="73ce3-155">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificato un trigger giornaliero utilizzando l'elemento [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="73ce3-155">When reading or writing your own XML for a task, a daily trigger is specified using the [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="73ce3-156">Esempio</span><span class="sxs-lookup"><span data-stu-id="73ce3-156">Examples</span></span>

<span data-ttu-id="73ce3-157">Per ulteriori informazioni e un esempio di codice per questo oggetto di scripting, vedere [esempio di trigger giornalieri (scripting)](daily-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="73ce3-157">For more information and a code example for this scripting object, see [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73ce3-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73ce3-158">Requirements</span></span>



| <span data-ttu-id="73ce3-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="73ce3-159">Requirement</span></span> | <span data-ttu-id="73ce3-160">Valore</span><span class="sxs-lookup"><span data-stu-id="73ce3-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73ce3-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73ce3-161">Minimum supported client</span></span><br/> | <span data-ttu-id="73ce3-162">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73ce3-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="73ce3-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73ce3-163">Minimum supported server</span></span><br/> | <span data-ttu-id="73ce3-164">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="73ce3-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73ce3-165">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="73ce3-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="73ce3-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="73ce3-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="73ce3-167">DLL</span><span class="sxs-lookup"><span data-stu-id="73ce3-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73ce3-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73ce3-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73ce3-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73ce3-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ce3-170">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="73ce3-170">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="73ce3-171">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="73ce3-171">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="73ce3-172">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="73ce3-172">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





