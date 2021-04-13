---
title: Oggetto EventTrigger (Windows. UI. XAML. h)
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività quando si verifica un evento di sistema.
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- Utilità di pianificazione trigger evento, oggetto
- Utilità di pianificazione oggetto EventTrigger
- Utilità di pianificazione oggetto EventTrigger, descritto
topic_type:
- apiref
api_name:
- EventTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b80bc8336c4756dfedc041aea40f79fd5f868e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518604"
---
# <a name="eventtrigger-object"></a><span data-ttu-id="27c99-106">EventTrigger (oggetto)</span><span class="sxs-lookup"><span data-stu-id="27c99-106">EventTrigger object</span></span>

<span data-ttu-id="27c99-107">Oggetto di scripting che rappresenta un trigger che avvia un'attività quando si verifica un evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="27c99-107">Scripting object that represents a trigger that starts a task when a system event occurs.</span></span>

## <a name="members"></a><span data-ttu-id="27c99-108">Membri</span><span class="sxs-lookup"><span data-stu-id="27c99-108">Members</span></span>

<span data-ttu-id="27c99-109">L'oggetto **EventTrigger** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="27c99-109">The **EventTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="27c99-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="27c99-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27c99-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="27c99-111">Properties</span></span>

<span data-ttu-id="27c99-112">L'oggetto **EventTrigger** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="27c99-112">The **EventTrigger** object has these properties.</span></span>



| <span data-ttu-id="27c99-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="27c99-113">Property</span></span>                                                            | <span data-ttu-id="27c99-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="27c99-114">Access type</span></span>           | <span data-ttu-id="27c99-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27c99-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27c99-116">**Ritardo**</span><span class="sxs-lookup"><span data-stu-id="27c99-116">**Delay**</span></span>](eventtrigger-delay.md)<br/>                      | <span data-ttu-id="27c99-117">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="27c99-117">Read/write</span></span><br/> | <span data-ttu-id="27c99-118">Ottiene o imposta un valore che indica la quantità di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="27c99-118">Gets or sets a value that indicates the amount of time between when the event occurs and when the task is started.</span></span><br/>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="27c99-119">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="27c99-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="27c99-120">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="27c99-120">Read/write</span></span><br/> | <span data-ttu-id="27c99-121">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="27c99-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="27c99-122">Ottiene o imposta un valore booleano che indica se il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="27c99-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="27c99-123">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="27c99-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="27c99-124">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="27c99-124">Read/write</span></span><br/> | <span data-ttu-id="27c99-125">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="27c99-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="27c99-126">Ottiene o imposta la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="27c99-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="27c99-127">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="27c99-127">The trigger cannot start the task after it is deactivated.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="27c99-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="27c99-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="27c99-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="27c99-129">Read/write</span></span><br/> | <span data-ttu-id="27c99-130">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="27c99-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="27c99-131">Ottiene o imposta il periodo di tempo massimo durante il quale l'attività avviata da questo trigger può essere eseguita.</span><span class="sxs-lookup"><span data-stu-id="27c99-131">Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.</span></span><br/>                                                                                                                                                                                                                       |
| [<span data-ttu-id="27c99-132">**ID**</span><span class="sxs-lookup"><span data-stu-id="27c99-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="27c99-133">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="27c99-133">Read/write</span></span><br/> | <span data-ttu-id="27c99-134">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="27c99-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="27c99-135">Ottiene o imposta l'identificatore per il trigger.</span><span class="sxs-lookup"><span data-stu-id="27c99-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="27c99-136">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="27c99-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="27c99-137">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="27c99-137">Read/write</span></span><br/> | <span data-ttu-id="27c99-138">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="27c99-138">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="27c99-139">Ottiene o imposta la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="27c99-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>                                                                                                                                                                                                       |
| [<span data-ttu-id="27c99-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="27c99-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="27c99-141">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="27c99-141">Read/write</span></span><br/> | <span data-ttu-id="27c99-142">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="27c99-142">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="27c99-143">Ottiene o imposta la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="27c99-143">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="27c99-144">**Abbonamento**</span><span class="sxs-lookup"><span data-stu-id="27c99-144">**Subscription**</span></span>](eventtrigger-subscription.md)<br/>        | <span data-ttu-id="27c99-145">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="27c99-145">Read/write</span></span><br/> | <span data-ttu-id="27c99-146">Ottiene o imposta la stringa di query XPath che identifica l'evento che attiva il trigger.</span><span class="sxs-lookup"><span data-stu-id="27c99-146">Gets or sets the XPath query string that identifies the event that fires the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="27c99-147">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="27c99-147">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="27c99-148">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="27c99-148">Read-only</span></span><br/>  | <span data-ttu-id="27c99-149">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="27c99-149">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="27c99-150">Ottiene il tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="27c99-150">Gets the type of the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="27c99-151">**ValueQueries**</span><span class="sxs-lookup"><span data-stu-id="27c99-151">**ValueQueries**</span></span>](eventtrigger-valuequeries.md)<br/>        | <span data-ttu-id="27c99-152">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="27c99-152">Read/write</span></span><br/> | <span data-ttu-id="27c99-153">Ottiene o imposta una raccolta di query XPath denominate.</span><span class="sxs-lookup"><span data-stu-id="27c99-153">Gets or sets a collection of named XPath queries.</span></span> <span data-ttu-id="27c99-154">Ogni query della raccolta viene applicata all'ultimo XML dell'evento corrispondente restituito dalla query di sottoscrizione specificata nella proprietà di [**sottoscrizione**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="27c99-154">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](eventtrigger-subscription.md) property.</span></span> <span data-ttu-id="27c99-155">Il nome della query può essere utilizzato come variabile nel messaggio di un'azione [**ShowMessageAction**](showmessageaction.md) .</span><span class="sxs-lookup"><span data-stu-id="27c99-155">The name of the query can be used as a variable in the message of a [**ShowMessageAction**](showmessageaction.md) action.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="27c99-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="27c99-156">Remarks</span></span>

<span data-ttu-id="27c99-157">È possibile creare un massimo di 500 attività con sottoscrizioni di eventi.</span><span class="sxs-lookup"><span data-stu-id="27c99-157">A maximum of 500 tasks with event subscriptions can be created.</span></span> <span data-ttu-id="27c99-158">Una sottoscrizione di eventi che esegue query per una varietà di eventi può essere usata per attivare un'attività che usa la stessa azione in risposta agli eventi che vengono registrati.</span><span class="sxs-lookup"><span data-stu-id="27c99-158">An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.</span></span>

<span data-ttu-id="27c99-159">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificato un trigger di evento usando l'elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="27c99-159">When reading or writing your own XML for a task, an event trigger is specified using the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="27c99-160">Esempio</span><span class="sxs-lookup"><span data-stu-id="27c99-160">Examples</span></span>

<span data-ttu-id="27c99-161">Per ulteriori informazioni e un esempio di codice per questo oggetto di scripting, vedere [esempio di trigger di evento (scripting)](/previous-versions//aa446887(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="27c99-161">For more information and a code example for this scripting object, see [Event Trigger Example (Scripting)](/previous-versions//aa446887(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="27c99-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27c99-162">Requirements</span></span>



| <span data-ttu-id="27c99-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="27c99-163">Requirement</span></span> | <span data-ttu-id="27c99-164">Valore</span><span class="sxs-lookup"><span data-stu-id="27c99-164">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="27c99-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27c99-165">Minimum supported client</span></span><br/> | <span data-ttu-id="27c99-166">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27c99-166">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="27c99-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27c99-167">Minimum supported server</span></span><br/> | <span data-ttu-id="27c99-168">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27c99-168">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="27c99-169">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27c99-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="27c99-170"><dt>Windows. UI. XAML. h</dt></span><span class="sxs-lookup"><span data-stu-id="27c99-170"><dt>Windows.ui.xaml.h</dt></span></span> </dl> |
| <span data-ttu-id="27c99-171">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="27c99-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="27c99-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="27c99-172"><dt>Taskschd.tlb</dt></span></span> </dl>      |
| <span data-ttu-id="27c99-173">DLL</span><span class="sxs-lookup"><span data-stu-id="27c99-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27c99-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27c99-174"><dt>Taskschd.dll</dt></span></span> </dl>      |



## <a name="see-also"></a><span data-ttu-id="27c99-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27c99-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c99-176">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="27c99-176">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="27c99-177">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="27c99-177">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="27c99-178">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="27c99-178">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

