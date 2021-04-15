---
title: Oggetto BootTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività quando viene avviato il sistema.
ms.assetid: 9d5a7cf6-2e1d-44ae-bb45-66424770d61b
keywords:
- Utilità di pianificazione trigger di avvio, oggetto
- Utilità di pianificazione oggetto BootTrigger
- Oggetto BootTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- BootTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 346a4bc7b20606f59c26b131590b92593d40d07e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479241"
---
# <a name="boottrigger-object"></a><span data-ttu-id="730cb-106">Oggetto BootTrigger</span><span class="sxs-lookup"><span data-stu-id="730cb-106">BootTrigger object</span></span>

<span data-ttu-id="730cb-107">Oggetto di scripting che rappresenta un trigger che avvia un'attività quando viene avviato il sistema.</span><span class="sxs-lookup"><span data-stu-id="730cb-107">Scripting object that represents a trigger that starts a task when the system is booted.</span></span>

## <a name="members"></a><span data-ttu-id="730cb-108">Membri</span><span class="sxs-lookup"><span data-stu-id="730cb-108">Members</span></span>

<span data-ttu-id="730cb-109">L'oggetto **BootTrigger** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="730cb-109">The **BootTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="730cb-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="730cb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="730cb-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="730cb-111">Properties</span></span>

<span data-ttu-id="730cb-112">L'oggetto **BootTrigger** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="730cb-112">The **BootTrigger** object has these properties.</span></span>



| <span data-ttu-id="730cb-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="730cb-113">Property</span></span>                                                            | <span data-ttu-id="730cb-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="730cb-114">Access type</span></span>           | <span data-ttu-id="730cb-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="730cb-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="730cb-116">**Ritardo**</span><span class="sxs-lookup"><span data-stu-id="730cb-116">**Delay**</span></span>](boottrigger-delay.md)<br/>                       |                       | <span data-ttu-id="730cb-117">Ottiene o imposta un valore che indica l'intervallo di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="730cb-117">Gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.</span></span><br/>                                                           |
| [<span data-ttu-id="730cb-118">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="730cb-118">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="730cb-119">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="730cb-119">Read/write</span></span><br/> | <span data-ttu-id="730cb-120">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="730cb-120">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="730cb-121">Ottiene o imposta un valore booleano che indica se il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="730cb-121">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="730cb-122">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="730cb-122">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="730cb-123">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="730cb-123">Read/write</span></span><br/> | <span data-ttu-id="730cb-124">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="730cb-124">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="730cb-125">Ottiene o imposta la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="730cb-125">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="730cb-126">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="730cb-126">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="730cb-127">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="730cb-127">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="730cb-128">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="730cb-128">Read/write</span></span><br/> | <span data-ttu-id="730cb-129">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="730cb-129">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="730cb-130">Ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="730cb-130">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="730cb-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="730cb-131">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="730cb-132">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="730cb-132">Read/write</span></span><br/> | <span data-ttu-id="730cb-133">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="730cb-133">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="730cb-134">Ottiene o imposta l'identificatore per il trigger.</span><span class="sxs-lookup"><span data-stu-id="730cb-134">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="730cb-135">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="730cb-135">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="730cb-136">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="730cb-136">Read/write</span></span><br/> | <span data-ttu-id="730cb-137">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="730cb-137">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="730cb-138">Ottiene o imposta la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="730cb-138">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="730cb-139">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="730cb-139">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="730cb-140">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="730cb-140">Read/write</span></span><br/> | <span data-ttu-id="730cb-141">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="730cb-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="730cb-142">Ottiene o imposta la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="730cb-142">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="730cb-143">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="730cb-143">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="730cb-144">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="730cb-144">Read-only</span></span><br/>  | <span data-ttu-id="730cb-145">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="730cb-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="730cb-146">Ottiene il tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="730cb-146">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="730cb-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="730cb-147">Remarks</span></span>

<span data-ttu-id="730cb-148">Il servizio Utilità di pianificazione viene avviato all'avvio del sistema operativo e le attività del trigger di avvio sono impostate per l'avvio all'avvio del servizio di Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="730cb-148">The Task Scheduler service is started when the operating system is booted, and boot trigger tasks are set to start when the Task Scheduler service starts.</span></span>

<span data-ttu-id="730cb-149">Solo un membro del gruppo Administrators può creare un'attività con un trigger di avvio.</span><span class="sxs-lookup"><span data-stu-id="730cb-149">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="730cb-150">Quando si crea un codice XML personalizzato per un'attività, viene specificato un trigger di avvio usando l'elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="730cb-150">When creating your own XML for a task, a boot trigger is specified using the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="730cb-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="730cb-151">Examples</span></span>

<span data-ttu-id="730cb-152">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di avvio (scripting)](boot-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="730cb-152">For more information and example code for this scripting object, see [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="730cb-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="730cb-153">Requirements</span></span>



| <span data-ttu-id="730cb-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="730cb-154">Requirement</span></span> | <span data-ttu-id="730cb-155">Valore</span><span class="sxs-lookup"><span data-stu-id="730cb-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="730cb-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="730cb-156">Minimum supported client</span></span><br/> | <span data-ttu-id="730cb-157">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="730cb-157">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="730cb-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="730cb-158">Minimum supported server</span></span><br/> | <span data-ttu-id="730cb-159">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="730cb-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="730cb-160">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="730cb-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="730cb-161"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="730cb-161"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="730cb-162">DLL</span><span class="sxs-lookup"><span data-stu-id="730cb-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="730cb-163"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="730cb-163"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="730cb-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="730cb-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="730cb-165">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="730cb-165">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="730cb-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="730cb-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="730cb-167">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="730cb-167">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





