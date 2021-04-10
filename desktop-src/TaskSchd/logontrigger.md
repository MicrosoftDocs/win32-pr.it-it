---
title: Oggetto LogonTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività quando un utente esegue l'accesso.
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- Utilità di pianificazione trigger LOGON, oggetto
- Utilità di pianificazione oggetto LogonTrigger
- Oggetto LogonTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- LogonTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9c4b2031b39a6dfd483b039023ad9114271b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964518"
---
# <a name="logontrigger-object"></a><span data-ttu-id="73dc3-106">Oggetto LogonTrigger</span><span class="sxs-lookup"><span data-stu-id="73dc3-106">LogonTrigger object</span></span>

<span data-ttu-id="73dc3-107">Oggetto di scripting che rappresenta un trigger che avvia un'attività quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="73dc3-107">Scripting object that represents a trigger that starts a task when a user logs on.</span></span> <span data-ttu-id="73dc3-108">All'avvio del servizio Utilità di pianificazione, vengono enumerati tutti gli utenti connessi e vengono eseguite tutte le attività registrate con i trigger LOGON corrispondenti all'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="73dc3-108">When the Task Scheduler service starts, all logged-on users are enumerated and any tasks registered with logon triggers that match the logged on user are run.</span></span>

## <a name="members"></a><span data-ttu-id="73dc3-109">Membri</span><span class="sxs-lookup"><span data-stu-id="73dc3-109">Members</span></span>

<span data-ttu-id="73dc3-110">L'oggetto **LogonTrigger** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="73dc3-110">The **LogonTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="73dc3-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73dc3-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73dc3-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73dc3-112">Properties</span></span>

<span data-ttu-id="73dc3-113">L'oggetto **LogonTrigger** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="73dc3-113">The **LogonTrigger** object has these properties.</span></span>



| <span data-ttu-id="73dc3-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73dc3-114">Property</span></span>                                                            | <span data-ttu-id="73dc3-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="73dc3-115">Access type</span></span>           | <span data-ttu-id="73dc3-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73dc3-116">Description</span></span>                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73dc3-117">**Ritardo**</span><span class="sxs-lookup"><span data-stu-id="73dc3-117">**Delay**</span></span>](logontrigger-delay.md)<br/>                      | <span data-ttu-id="73dc3-118">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73dc3-118">Read/write</span></span><br/> | <span data-ttu-id="73dc3-119">Ottiene o imposta un valore che indica l'intervallo di tempo tra il momento in cui l'utente esegue l'accesso e il momento in cui il processo viene avviato.</span><span class="sxs-lookup"><span data-stu-id="73dc3-119">Gets or sets a value that indicates the amount of time between when the user logs on and when the job is started.</span></span><br/>                                                                              |
| [<span data-ttu-id="73dc3-120">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="73dc3-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="73dc3-121">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73dc3-121">Read/write</span></span><br/> | <span data-ttu-id="73dc3-122">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="73dc3-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="73dc3-123">Ottiene o imposta un valore booleano che indica se il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="73dc3-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="73dc3-124">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="73dc3-124">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="73dc3-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73dc3-125">Read/write</span></span><br/> | <span data-ttu-id="73dc3-126">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="73dc3-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="73dc3-127">Ottiene o imposta la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="73dc3-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="73dc3-128">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="73dc3-128">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="73dc3-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="73dc3-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="73dc3-130">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73dc3-130">Read/write</span></span><br/> | <span data-ttu-id="73dc3-131">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="73dc3-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="73dc3-132">Ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="73dc3-132">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                                         |
| [<span data-ttu-id="73dc3-133">**ID**</span><span class="sxs-lookup"><span data-stu-id="73dc3-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="73dc3-134">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73dc3-134">Read/write</span></span><br/> | <span data-ttu-id="73dc3-135">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="73dc3-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="73dc3-136">Ottiene o imposta l'identificatore per il trigger.</span><span class="sxs-lookup"><span data-stu-id="73dc3-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="73dc3-137">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="73dc3-137">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="73dc3-138">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73dc3-138">Read/write</span></span><br/> | <span data-ttu-id="73dc3-139">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="73dc3-139">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="73dc3-140">Ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="73dc3-140">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="73dc3-141">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="73dc3-141">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="73dc3-142">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73dc3-142">Read/write</span></span><br/> | <span data-ttu-id="73dc3-143">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="73dc3-143">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="73dc3-144">Ottiene o imposta la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="73dc3-144">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="73dc3-145">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="73dc3-145">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="73dc3-146">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="73dc3-146">Read-only</span></span><br/>  | <span data-ttu-id="73dc3-147">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="73dc3-147">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="73dc3-148">Ottiene il tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="73dc3-148">Gets the type of the trigger.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="73dc3-149">**UserId**</span><span class="sxs-lookup"><span data-stu-id="73dc3-149">**UserId**</span></span>](logontrigger-userid.md)<br/>                    | <span data-ttu-id="73dc3-150">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="73dc3-150">Read/write</span></span><br/> | <span data-ttu-id="73dc3-151">Ottiene o imposta l'identificatore dell'utente.</span><span class="sxs-lookup"><span data-stu-id="73dc3-151">Gets or sets the identifier of the user.</span></span><br/>                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="73dc3-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="73dc3-152">Remarks</span></span>

<span data-ttu-id="73dc3-153">Se si desidera che un'attività venga attivata quando un membro di un gruppo accede al computer anziché quando un utente specifico esegue l'accesso, non assegnare un valore alla proprietà [**LogonTrigger. UserID**](logontrigger-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="73dc3-153">If you want a task to be triggered when any member of a group logs on to the computer rather than when a specific user logs on, then do not assign a value to the [**LogonTrigger.UserId**](logontrigger-userid.md) property.</span></span> <span data-ttu-id="73dc3-154">In alternativa, creare un trigger LOGON con una proprietà **LogonTrigger. UserID** vuota e assegnare un valore all'entità per l'attività usando la proprietà [**Principal. GroupID**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="73dc3-154">Instead, create a logon trigger with an empty **LogonTrigger.UserId** property and assign a value to the principal for the task using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="73dc3-155">Durante la lettura o la scrittura di codice XML per un'attività, viene specificato un trigger LOGON utilizzando l'elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="73dc3-155">When reading or writing XML for a task, a logon trigger is specified using the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="73dc3-156">Esempio</span><span class="sxs-lookup"><span data-stu-id="73dc3-156">Examples</span></span>

<span data-ttu-id="73dc3-157">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger LOGON (scripting)](logon-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="73dc3-157">For more information and example code for this scripting object, see [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73dc3-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73dc3-158">Requirements</span></span>



| <span data-ttu-id="73dc3-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="73dc3-159">Requirement</span></span> | <span data-ttu-id="73dc3-160">Valore</span><span class="sxs-lookup"><span data-stu-id="73dc3-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73dc3-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73dc3-161">Minimum supported client</span></span><br/> | <span data-ttu-id="73dc3-162">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73dc3-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="73dc3-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73dc3-163">Minimum supported server</span></span><br/> | <span data-ttu-id="73dc3-164">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="73dc3-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73dc3-165">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="73dc3-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="73dc3-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="73dc3-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="73dc3-167">DLL</span><span class="sxs-lookup"><span data-stu-id="73dc3-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73dc3-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73dc3-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73dc3-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73dc3-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73dc3-170">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="73dc3-170">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





