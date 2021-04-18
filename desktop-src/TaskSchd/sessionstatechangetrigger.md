---
title: Oggetto SessionStateChangeTrigger
description: Oggetto di script che attiva le attività per la connessione o la disconnessione della console, la connessione remota o la disconnessione o le notifiche di blocco o sblocco della workstation.
ms.assetid: ea450b8a-81cc-4d24-b850-78c967dcc5b8
keywords:
- Utilità di pianificazione oggetto SessionStateChangeTrigger
- Oggetto SessionStateChangeTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55d41f495c714fe2e1798c79cc4f24b99987a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301244"
---
# <a name="sessionstatechangetrigger-object"></a><span data-ttu-id="02e21-105">Oggetto SessionStateChangeTrigger</span><span class="sxs-lookup"><span data-stu-id="02e21-105">SessionStateChangeTrigger object</span></span>

<span data-ttu-id="02e21-106">Oggetto di script che attiva le attività per la connessione o la disconnessione della console, la connessione remota o la disconnessione o le notifiche di blocco o sblocco della workstation.</span><span class="sxs-lookup"><span data-stu-id="02e21-106">Scripting object that triggers tasks for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.</span></span>

## <a name="members"></a><span data-ttu-id="02e21-107">Membri</span><span class="sxs-lookup"><span data-stu-id="02e21-107">Members</span></span>

<span data-ttu-id="02e21-108">L'oggetto **SessionStateChangeTrigger** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="02e21-108">The **SessionStateChangeTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="02e21-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="02e21-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02e21-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="02e21-110">Properties</span></span>

<span data-ttu-id="02e21-111">L'oggetto **SessionStateChangeTrigger** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="02e21-111">The **SessionStateChangeTrigger** object has these properties.</span></span>



| <span data-ttu-id="02e21-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="02e21-112">Property</span></span>                                                                | <span data-ttu-id="02e21-113">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="02e21-113">Access type</span></span>           | <span data-ttu-id="02e21-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02e21-114">Description</span></span>                                                                                                                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02e21-115">**Ritardo**</span><span class="sxs-lookup"><span data-stu-id="02e21-115">**Delay**</span></span>](sessionstatechangetrigger-delay.md)<br/>             | <span data-ttu-id="02e21-116">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="02e21-116">Read/write</span></span><br/> | <span data-ttu-id="02e21-117">Ottiene o imposta un valore che indica per quanto tempo si verifica un ritardo prima che venga avviata un'attività dopo che è stata rilevata una modifica dello stato della sessione Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="02e21-117">Gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.</span></span><br/>                                         |
| [<span data-ttu-id="02e21-118">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="02e21-118">**Enabled**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled)<br/>                          | <span data-ttu-id="02e21-119">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="02e21-119">Read/write</span></span><br/> | <span data-ttu-id="02e21-120">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="02e21-120">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="02e21-121">Ottiene o imposta un valore booleano che indica se il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="02e21-121">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="02e21-122">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="02e21-122">**EndBoundary**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary)<br/>                  | <span data-ttu-id="02e21-123">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="02e21-123">Read/write</span></span><br/> | <span data-ttu-id="02e21-124">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="02e21-124">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="02e21-125">Ottiene o imposta la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="02e21-125">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="02e21-126">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="02e21-126">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="02e21-127">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="02e21-127">**ExecutionTimeLimit**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit)<br/>    | <span data-ttu-id="02e21-128">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="02e21-128">Read/write</span></span><br/> | <span data-ttu-id="02e21-129">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="02e21-129">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="02e21-130">Ottiene o imposta il periodo di tempo massimo in cui l'attività può essere avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="02e21-130">Gets or sets the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                                 |
| [<span data-ttu-id="02e21-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="02e21-131">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                    | <span data-ttu-id="02e21-132">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="02e21-132">Read/write</span></span><br/> | <span data-ttu-id="02e21-133">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="02e21-133">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="02e21-134">Ottiene o imposta l'identificatore per il trigger.</span><span class="sxs-lookup"><span data-stu-id="02e21-134">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="02e21-135">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="02e21-135">**Repetition**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition)<br/>                    | <span data-ttu-id="02e21-136">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="02e21-136">Read/write</span></span><br/> | <span data-ttu-id="02e21-137">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="02e21-137">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="02e21-138">Ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="02e21-138">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="02e21-139">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="02e21-139">**StartBoundary**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary)<br/>              | <span data-ttu-id="02e21-140">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="02e21-140">Read/write</span></span><br/> | <span data-ttu-id="02e21-141">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="02e21-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="02e21-142">Ottiene o imposta la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="02e21-142">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="02e21-143">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="02e21-143">**StateChange**</span></span>](sessionstatechangetrigger-statechange.md)<br/> | <span data-ttu-id="02e21-144">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="02e21-144">Read/write</span></span><br/> | <span data-ttu-id="02e21-145">Ottiene o imposta il tipo di modifica della sessione di Terminal Server che avvierà un'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="02e21-145">Gets or sets the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="02e21-146">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="02e21-146">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                | <span data-ttu-id="02e21-147">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="02e21-147">Read-only</span></span><br/>  | <span data-ttu-id="02e21-148">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="02e21-148">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="02e21-149">Ottiene il tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="02e21-149">Gets the type of the trigger.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="02e21-150">**UserId**</span><span class="sxs-lookup"><span data-stu-id="02e21-150">**UserId**</span></span>](sessionstatechangetrigger-userid.md)<br/>           | <span data-ttu-id="02e21-151">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="02e21-151">Read/write</span></span><br/> | <span data-ttu-id="02e21-152">Ottiene o imposta l'utente per la sessione di Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="02e21-152">Gets or sets the user for the Terminal Server session.</span></span> <span data-ttu-id="02e21-153">Quando viene rilevata una modifica dello stato della sessione per questo utente, viene avviata un'attività.</span><span class="sxs-lookup"><span data-stu-id="02e21-153">When a session state change is detected for this user, a task is started.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="02e21-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="02e21-154">Remarks</span></span>

<span data-ttu-id="02e21-155">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificato un trigger di modifica dello stato della sessione utilizzando l'elemento [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="02e21-155">When reading or writing your own XML for a task, a session state change trigger is specified using the [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e21-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02e21-156">Requirements</span></span>



| <span data-ttu-id="02e21-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="02e21-157">Requirement</span></span> | <span data-ttu-id="02e21-158">Valore</span><span class="sxs-lookup"><span data-stu-id="02e21-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02e21-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02e21-159">Minimum supported client</span></span><br/> | <span data-ttu-id="02e21-160">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="02e21-160">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="02e21-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02e21-161">Minimum supported server</span></span><br/> | <span data-ttu-id="02e21-162">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="02e21-162">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02e21-163">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="02e21-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="02e21-164"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="02e21-164"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="02e21-165">DLL</span><span class="sxs-lookup"><span data-stu-id="02e21-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02e21-166"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02e21-166"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02e21-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02e21-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e21-168">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="02e21-168">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="02e21-169">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="02e21-169">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





