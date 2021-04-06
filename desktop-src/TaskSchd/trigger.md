---
title: Oggetto trigger
description: Oggetto di scripting che fornisce le proprietà comuni ereditate da tutti gli oggetti trigger.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- trigger Utilità di pianificazione, oggetto trigger
- Utilità di pianificazione oggetto trigger
- Utilità di pianificazione oggetto trigger, descritto
topic_type:
- apiref
api_name:
- Trigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4a7edc6eff0bb04c81ba3bff3bb86ec0455b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873545"
---
# <a name="trigger-object"></a><span data-ttu-id="14ae3-106">Oggetto trigger</span><span class="sxs-lookup"><span data-stu-id="14ae3-106">Trigger object</span></span>

<span data-ttu-id="14ae3-107">Oggetto di scripting che fornisce le proprietà comuni ereditate da tutti gli oggetti trigger.</span><span class="sxs-lookup"><span data-stu-id="14ae3-107">Scripting object that provides the common properties that are inherited by all trigger objects.</span></span>

## <a name="members"></a><span data-ttu-id="14ae3-108">Membri</span><span class="sxs-lookup"><span data-stu-id="14ae3-108">Members</span></span>

<span data-ttu-id="14ae3-109">L'oggetto **trigger** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="14ae3-109">The **Trigger** object has these types of members:</span></span>

-   [<span data-ttu-id="14ae3-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="14ae3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14ae3-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="14ae3-111">Properties</span></span>

<span data-ttu-id="14ae3-112">L'oggetto **trigger** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="14ae3-112">The **Trigger** object has these properties.</span></span>



| <span data-ttu-id="14ae3-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="14ae3-113">Property</span></span>                                                            | <span data-ttu-id="14ae3-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="14ae3-114">Access type</span></span>           | <span data-ttu-id="14ae3-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14ae3-115">Description</span></span>                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14ae3-116">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="14ae3-116">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="14ae3-117">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="14ae3-117">Read/write</span></span><br/> | <span data-ttu-id="14ae3-118">Ottiene o imposta un valore booleano che indica se il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="14ae3-118">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="14ae3-119">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="14ae3-119">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="14ae3-120">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="14ae3-120">Read/write</span></span><br/> | <span data-ttu-id="14ae3-121">Ottiene o imposta la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="14ae3-121">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="14ae3-122">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="14ae3-122">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="14ae3-123">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="14ae3-123">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="14ae3-124">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="14ae3-124">Read/write</span></span><br/> | <span data-ttu-id="14ae3-125">Ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="14ae3-125">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                                         |
| [<span data-ttu-id="14ae3-126">**ID**</span><span class="sxs-lookup"><span data-stu-id="14ae3-126">**Id**</span></span>](trigger-id.md)<br/>                                 | <span data-ttu-id="14ae3-127">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="14ae3-127">Read/write</span></span><br/> | <span data-ttu-id="14ae3-128">Ottiene o imposta l'identificatore per il trigger.</span><span class="sxs-lookup"><span data-stu-id="14ae3-128">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="14ae3-129">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="14ae3-129">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="14ae3-130">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="14ae3-130">Read/write</span></span><br/> | <span data-ttu-id="14ae3-131">Ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="14ae3-131">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="14ae3-132">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="14ae3-132">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="14ae3-133">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="14ae3-133">Read/write</span></span><br/> | <span data-ttu-id="14ae3-134">Ottiene o imposta la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="14ae3-134">Gets or sets the date and time when the trigger is activated.</span></span> <span data-ttu-id="14ae3-135">Il trigger può avviare l'attività dopo che il trigger è stato attivato.</span><span class="sxs-lookup"><span data-stu-id="14ae3-135">The trigger can start the task after the trigger is activated.</span></span><br/>             |
| [<span data-ttu-id="14ae3-136">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="14ae3-136">**Type**</span></span>](trigger-type.md)<br/>                             |                       | <span data-ttu-id="14ae3-137">Ottiene il tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="14ae3-137">Gets the type of the trigger.</span></span><br/>                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="14ae3-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="14ae3-138">Remarks</span></span>

<span data-ttu-id="14ae3-139">Il Utilità di pianificazione fornisce i singoli oggetti seguenti per i diversi trigger che possono essere utilizzati da un'attività:</span><span class="sxs-lookup"><span data-stu-id="14ae3-139">The Task Scheduler provides the following individual objects for the different triggers that a task can use:</span></span>

-   [<span data-ttu-id="14ae3-140">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="14ae3-140">**BootTrigger**</span></span>](boottrigger.md)
-   [<span data-ttu-id="14ae3-141">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="14ae3-141">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="14ae3-142">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="14ae3-142">**EventTrigger**</span></span>](eventtrigger.md)
-   [<span data-ttu-id="14ae3-143">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="14ae3-143">**IdleTrigger**</span></span>](idletrigger.md)
-   [<span data-ttu-id="14ae3-144">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="14ae3-144">**LogonTrigger**</span></span>](logontrigger.md)
-   [<span data-ttu-id="14ae3-145">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="14ae3-145">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
-   [<span data-ttu-id="14ae3-146">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="14ae3-146">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="14ae3-147">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="14ae3-147">**RegistrationTrigger**</span></span>](registrationtrigger.md)
-   [<span data-ttu-id="14ae3-148">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="14ae3-148">**TimeTrigger**</span></span>](timetrigger.md)
-   [<span data-ttu-id="14ae3-149">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="14ae3-149">**WeeklyTrigger**</span></span>](weeklytrigger.md)
-   [<span data-ttu-id="14ae3-150">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="14ae3-150">**SessionStateChangeTrigger**</span></span>](sessionstatechangetrigger.md)

<span data-ttu-id="14ae3-151">Durante la lettura o la scrittura di codice XML, i trigger di un'attività vengono specificati nell'elemento [**trigger**](taskschedulerschema-triggers-tasktype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="14ae3-151">When reading or writing XML, the triggers of a task are specified in the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="14ae3-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="14ae3-152">Examples</span></span>

<span data-ttu-id="14ae3-153">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="14ae3-153">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14ae3-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14ae3-154">Requirements</span></span>



| <span data-ttu-id="14ae3-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="14ae3-155">Requirement</span></span> | <span data-ttu-id="14ae3-156">Valore</span><span class="sxs-lookup"><span data-stu-id="14ae3-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14ae3-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14ae3-157">Minimum supported client</span></span><br/> | <span data-ttu-id="14ae3-158">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14ae3-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="14ae3-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14ae3-159">Minimum supported server</span></span><br/> | <span data-ttu-id="14ae3-160">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14ae3-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14ae3-161">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="14ae3-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="14ae3-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="14ae3-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="14ae3-163">DLL</span><span class="sxs-lookup"><span data-stu-id="14ae3-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14ae3-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14ae3-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14ae3-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14ae3-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14ae3-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="14ae3-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> </dl>

 

 





