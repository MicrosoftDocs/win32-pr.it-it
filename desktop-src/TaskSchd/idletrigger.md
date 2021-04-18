---
title: Oggetto IdleTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività quando si verifica una condizione di inattività.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- Utilità di pianificazione Trigger inattivo, oggetto
- Utilità di pianificazione oggetto IdleTrigger
- Oggetto IdleTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- IdleTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72288827fec34257bf4f54a152031ef37068790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302495"
---
# <a name="idletrigger-object"></a><span data-ttu-id="68227-106">Oggetto IdleTrigger</span><span class="sxs-lookup"><span data-stu-id="68227-106">IdleTrigger object</span></span>

<span data-ttu-id="68227-107">Oggetto di scripting che rappresenta un trigger che avvia un'attività quando si verifica una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="68227-107">Scripting object that represents a trigger that starts a task when an idle condition occurs.</span></span> <span data-ttu-id="68227-108">Per informazioni sulle condizioni di inattività, vedere [condizioni](task-idle-conditions.md)di inattività.</span><span class="sxs-lookup"><span data-stu-id="68227-108">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

## <a name="members"></a><span data-ttu-id="68227-109">Membri</span><span class="sxs-lookup"><span data-stu-id="68227-109">Members</span></span>

<span data-ttu-id="68227-110">L'oggetto **IdleTrigger** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="68227-110">The **IdleTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="68227-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="68227-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68227-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="68227-112">Properties</span></span>

<span data-ttu-id="68227-113">L'oggetto **IdleTrigger** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="68227-113">The **IdleTrigger** object has these properties.</span></span>



| <span data-ttu-id="68227-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="68227-114">Property</span></span>                                                            | <span data-ttu-id="68227-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="68227-115">Access type</span></span>           | <span data-ttu-id="68227-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68227-116">Description</span></span>                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68227-117">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="68227-117">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="68227-118">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="68227-118">Read/write</span></span><br/> | <span data-ttu-id="68227-119">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="68227-119">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="68227-120">Ottiene o imposta un valore booleano che indica se il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="68227-120">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="68227-121">EndBoundary</span><span class="sxs-lookup"><span data-stu-id="68227-121">EndBoundary</span></span>](trigger-endboundary.md)<br/>                   | <span data-ttu-id="68227-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="68227-122">Read/write</span></span><br/> | <span data-ttu-id="68227-123">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="68227-123">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="68227-124">Ottiene o imposta la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="68227-124">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="68227-125">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="68227-125">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="68227-126">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="68227-126">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="68227-127">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="68227-127">Read/write</span></span><br/> | <span data-ttu-id="68227-128">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="68227-128">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="68227-129">Ottiene o imposta il periodo di tempo massimo in cui l'attività può essere avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="68227-129">Gets or sets the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                                 |
| [<span data-ttu-id="68227-130">**ID**</span><span class="sxs-lookup"><span data-stu-id="68227-130">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="68227-131">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="68227-131">Read/write</span></span><br/> | <span data-ttu-id="68227-132">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="68227-132">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="68227-133">Ottiene o imposta l'identificatore per il trigger.</span><span class="sxs-lookup"><span data-stu-id="68227-133">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="68227-134">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="68227-134">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="68227-135">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="68227-135">Read/write</span></span><br/> | <span data-ttu-id="68227-136">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="68227-136">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="68227-137">Ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="68227-137">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="68227-138">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="68227-138">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="68227-139">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="68227-139">Read/write</span></span><br/> | <span data-ttu-id="68227-140">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="68227-140">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="68227-141">Ottiene o imposta la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="68227-141">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="68227-142">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="68227-142">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="68227-143">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="68227-143">Read-only</span></span><br/>  | <span data-ttu-id="68227-144">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="68227-144">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="68227-145">Ottiene il tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="68227-145">Gets the type of the trigger.</span></span><br/>                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="68227-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="68227-146">Remarks</span></span>

<span data-ttu-id="68227-147">Un trigger inattivo attiverà un'azione dell'attività solo se il computer entra in uno stato di inattività dopo il limite di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="68227-147">An idle trigger will only trigger a task action if the computer goes into an idle state after the start boundary of the trigger.</span></span>

<span data-ttu-id="68227-148">Durante la lettura o la scrittura di codice XML per un'attività, viene specificato un trigger inattivo mediante l'elemento [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="68227-148">When reading or writing XML for a task, an idle trigger is specified using the [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="68227-149">Se un'attività viene attivata da un trigger inattivo, la proprietà [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="68227-149">If a task is triggered by an idle trigger, then the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property is ignored.</span></span>

<span data-ttu-id="68227-150">Se l'istanza iniziale di un'attività con un trigger inattivo è ancora in esecuzione, l'attività viene avviata una sola volta senza ripetizioni, anche se nella proprietà di [**ripetizione**](trigger-repetition.md) viene definito più ripetizioni.</span><span class="sxs-lookup"><span data-stu-id="68227-150">If the initial instance of a task with an idle trigger is still running, then the task is only launched once with no repetitions, even if multiple repetition is defined in the [**Repetition**](trigger-repetition.md) property.</span></span> <span data-ttu-id="68227-151">Questo comportamento non si verifica se l'attività si interrompe da sola.</span><span class="sxs-lookup"><span data-stu-id="68227-151">This behavior does not occur if the task stops by itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="68227-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68227-152">Requirements</span></span>



| <span data-ttu-id="68227-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="68227-153">Requirement</span></span> | <span data-ttu-id="68227-154">Valore</span><span class="sxs-lookup"><span data-stu-id="68227-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68227-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68227-155">Minimum supported client</span></span><br/> | <span data-ttu-id="68227-156">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68227-156">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="68227-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68227-157">Minimum supported server</span></span><br/> | <span data-ttu-id="68227-158">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68227-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="68227-159">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="68227-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="68227-160"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="68227-160"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="68227-161">DLL</span><span class="sxs-lookup"><span data-stu-id="68227-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68227-162"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68227-162"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68227-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68227-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68227-164">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="68227-164">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="68227-165">Oggetti Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="68227-165">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="68227-166">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="68227-166">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





