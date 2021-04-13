---
title: Oggetto TimeTrigger (Windows. ApplicationModel. background. h)
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività in una data e a un'ora specifiche.
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- Utilità di pianificazione trigger di ora, oggetto
- Utilità di pianificazione oggetto TimeTrigger
- Oggetto TimeTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- TimeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8403b93e1c5292ade9f6f402b7e41994339140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340882"
---
# <a name="timetrigger-object"></a><span data-ttu-id="a5bb0-106">Oggetto TimeTrigger</span><span class="sxs-lookup"><span data-stu-id="a5bb0-106">TimeTrigger object</span></span>

<span data-ttu-id="a5bb0-107">Oggetto di scripting che rappresenta un trigger che avvia un'attività in una data e a un'ora specifiche.</span><span class="sxs-lookup"><span data-stu-id="a5bb0-107">Scripting object that represents a trigger that starts a task at a specific date and time.</span></span>

## <a name="members"></a><span data-ttu-id="a5bb0-108">Membri</span><span class="sxs-lookup"><span data-stu-id="a5bb0-108">Members</span></span>

<span data-ttu-id="a5bb0-109">L'oggetto **TimeTrigger** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a5bb0-109">The **TimeTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="a5bb0-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a5bb0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5bb0-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a5bb0-111">Properties</span></span>

<span data-ttu-id="a5bb0-112">L'oggetto **TimeTrigger** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a5bb0-112">The **TimeTrigger** object has these properties.</span></span>



| <span data-ttu-id="a5bb0-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a5bb0-113">Property</span></span>                                                            | <span data-ttu-id="a5bb0-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="a5bb0-114">Access type</span></span>           | <span data-ttu-id="a5bb0-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5bb0-115">Description</span></span>                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5bb0-116">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="a5bb0-116">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="a5bb0-117">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a5bb0-117">Read/write</span></span><br/> | <span data-ttu-id="a5bb0-118">Ereditato da [**trigger**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="a5bb0-118">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="a5bb0-119">Ottiene o imposta un valore booleano che indica se il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="a5bb0-119">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="a5bb0-120">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="a5bb0-120">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="a5bb0-121">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a5bb0-121">Read/write</span></span><br/> | <span data-ttu-id="a5bb0-122">Ereditato da [**trigger**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="a5bb0-122">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="a5bb0-123">Ottiene o imposta la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="a5bb0-123">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="a5bb0-124">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="a5bb0-124">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="a5bb0-125">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="a5bb0-125">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="a5bb0-126">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a5bb0-126">Read/write</span></span><br/> | <span data-ttu-id="a5bb0-127">Ereditato da [**trigger**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="a5bb0-127">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="a5bb0-128">Ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="a5bb0-128">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="a5bb0-129">**ID**</span><span class="sxs-lookup"><span data-stu-id="a5bb0-129">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="a5bb0-130">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a5bb0-130">Read/write</span></span><br/> | <span data-ttu-id="a5bb0-131">Ereditato da [**trigger**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="a5bb0-131">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="a5bb0-132">Ottiene o imposta l'identificatore per il trigger.</span><span class="sxs-lookup"><span data-stu-id="a5bb0-132">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="a5bb0-133">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="a5bb0-133">**RandomDelay**</span></span>](dailytrigger-randomdelay.md)<br/>          | <span data-ttu-id="a5bb0-134">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a5bb0-134">Read/write</span></span><br/> | <span data-ttu-id="a5bb0-135">Ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="a5bb0-135">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                    |
| [<span data-ttu-id="a5bb0-136">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="a5bb0-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="a5bb0-137">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a5bb0-137">Read/write</span></span><br/> | <span data-ttu-id="a5bb0-138">Ereditato da [**trigger**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="a5bb0-138">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="a5bb0-139">Ottiene o imposta la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="a5bb0-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="a5bb0-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="a5bb0-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="a5bb0-141">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a5bb0-141">Read/write</span></span><br/> | <span data-ttu-id="a5bb0-142">Ereditato da [**trigger**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="a5bb0-142">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="a5bb0-143">Ottiene o imposta la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="a5bb0-143">Gets or sets the date and time when the trigger is activated.</span></span> <span data-ttu-id="a5bb0-144">Questo elemento è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a5bb0-144">This element is required.</span></span><br/>                                    |
| [<span data-ttu-id="a5bb0-145">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a5bb0-145">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="a5bb0-146">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5bb0-146">Read-only</span></span><br/>  | <span data-ttu-id="a5bb0-147">Ereditato da [**trigger**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="a5bb0-147">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="a5bb0-148">Ottiene il tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="a5bb0-148">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="a5bb0-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5bb0-149">Remarks</span></span>

<span data-ttu-id="a5bb0-150">L'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) è un elemento obbligatorio per i trigger Time e Calendar ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) e [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span><span class="sxs-lookup"><span data-stu-id="a5bb0-150">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) and [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="a5bb0-151">Durante la lettura o la scrittura di codice XML per un'attività, viene specificato un trigger inattivo mediante l'elemento [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="a5bb0-151">When reading or writing XML for a task, an idle trigger is specified using the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="a5bb0-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="a5bb0-152">Examples</span></span>

<span data-ttu-id="a5bb0-153">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="a5bb0-153">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5bb0-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5bb0-154">Requirements</span></span>



| <span data-ttu-id="a5bb0-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5bb0-155">Requirement</span></span> | <span data-ttu-id="a5bb0-156">Valore</span><span class="sxs-lookup"><span data-stu-id="a5bb0-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5bb0-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5bb0-157">Minimum supported client</span></span><br/> | <span data-ttu-id="a5bb0-158">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a5bb0-158">Windows Vista \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="a5bb0-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5bb0-159">Minimum supported server</span></span><br/> | <span data-ttu-id="a5bb0-160">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a5bb0-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a5bb0-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5bb0-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5bb0-162"><dt>Windows. ApplicationModel. background. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5bb0-162"><dt>Windows.applicationmodel.background.h</dt></span></span> </dl> |
| <span data-ttu-id="a5bb0-163">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a5bb0-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="a5bb0-164"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a5bb0-164"><dt>Taskschd.tlb</dt></span></span> </dl>                          |
| <span data-ttu-id="a5bb0-165">DLL</span><span class="sxs-lookup"><span data-stu-id="a5bb0-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5bb0-166"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5bb0-166"><dt>Taskschd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a5bb0-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5bb0-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5bb0-168">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="a5bb0-168">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="a5bb0-169">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="a5bb0-169">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="a5bb0-170">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="a5bb0-170">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





