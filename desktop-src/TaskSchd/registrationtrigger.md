---
title: Oggetto RegistrationTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività quando l'attività viene registrata o aggiornata.
ms.assetid: 430ef3e0-9409-49ff-8ffb-31833938d8b2
keywords:
- Utilità di pianificazione trigger di registrazione, oggetto
- Utilità di pianificazione oggetto RegistrationTrigger
- Oggetto RegistrationTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08bf84fa92b1736b2989c1920abb8f0af2c0b97c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518081"
---
# <a name="registrationtrigger-object"></a><span data-ttu-id="c99e1-106">Oggetto RegistrationTrigger</span><span class="sxs-lookup"><span data-stu-id="c99e1-106">RegistrationTrigger object</span></span>

<span data-ttu-id="c99e1-107">Oggetto di scripting che rappresenta un trigger che avvia un'attività quando l'attività viene registrata o aggiornata.</span><span class="sxs-lookup"><span data-stu-id="c99e1-107">Scripting object that represents a trigger that starts a task when the task is registered or updated.</span></span>

## <a name="members"></a><span data-ttu-id="c99e1-108">Membri</span><span class="sxs-lookup"><span data-stu-id="c99e1-108">Members</span></span>

<span data-ttu-id="c99e1-109">L'oggetto **RegistrationTrigger** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c99e1-109">The **RegistrationTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="c99e1-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c99e1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c99e1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c99e1-111">Properties</span></span>

<span data-ttu-id="c99e1-112">L'oggetto **RegistrationTrigger** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c99e1-112">The **RegistrationTrigger** object has these properties.</span></span>



| <span data-ttu-id="c99e1-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c99e1-113">Property</span></span>                                                            | <span data-ttu-id="c99e1-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="c99e1-114">Access type</span></span>           | <span data-ttu-id="c99e1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c99e1-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c99e1-116">**Ritardo**</span><span class="sxs-lookup"><span data-stu-id="c99e1-116">**Delay**</span></span>](registrationtrigger-delay.md)<br/>               | <span data-ttu-id="c99e1-117">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="c99e1-117">Read/write</span></span><br/> | <span data-ttu-id="c99e1-118">Ottiene o imposta la quantità di tempo tra il momento in cui l'attività viene registrata e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="c99e1-118">Gets or sets the amount of time between when the task is registered and when the task is started.</span></span><br/>                                                                                |
| [<span data-ttu-id="c99e1-119">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="c99e1-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="c99e1-120">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="c99e1-120">Read/write</span></span><br/> | <span data-ttu-id="c99e1-121">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c99e1-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="c99e1-122">Ottiene o imposta un valore booleano che indica se il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="c99e1-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="c99e1-123">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="c99e1-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="c99e1-124">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="c99e1-124">Read/write</span></span><br/> | <span data-ttu-id="c99e1-125">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c99e1-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="c99e1-126">Ottiene o imposta la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="c99e1-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="c99e1-127">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="c99e1-127">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="c99e1-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="c99e1-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="c99e1-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="c99e1-129">Read/write</span></span><br/> | <span data-ttu-id="c99e1-130">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c99e1-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="c99e1-131">Ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="c99e1-131">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="c99e1-132">**ID**</span><span class="sxs-lookup"><span data-stu-id="c99e1-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="c99e1-133">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="c99e1-133">Read/write</span></span><br/> | <span data-ttu-id="c99e1-134">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c99e1-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="c99e1-135">Ottiene o imposta l'identificatore per il trigger.</span><span class="sxs-lookup"><span data-stu-id="c99e1-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="c99e1-136">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="c99e1-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="c99e1-137">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="c99e1-137">Read/write</span></span><br/> | <span data-ttu-id="c99e1-138">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c99e1-138">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="c99e1-139">Ottiene o imposta la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="c99e1-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="c99e1-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="c99e1-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="c99e1-141">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="c99e1-141">Read/write</span></span><br/> | <span data-ttu-id="c99e1-142">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c99e1-142">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="c99e1-143">Ottiene o imposta la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="c99e1-143">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="c99e1-144">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c99e1-144">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="c99e1-145">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="c99e1-145">Read-only</span></span><br/>  | <span data-ttu-id="c99e1-146">Ereditato dall'oggetto [**trigger**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c99e1-146">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="c99e1-147">Ottiene il tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="c99e1-147">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="c99e1-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="c99e1-148">Remarks</span></span>

<span data-ttu-id="c99e1-149">Quando si crea un codice XML personalizzato per un'attività, viene specificato un trigger di registrazione usando l'elemento [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="c99e1-149">When creating your own XML for a task, a registration trigger is specified using the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="c99e1-150">Se un'attività con un trigger di registrazione ritardata viene registrata e il computer in cui è registrata l'attività viene arrestato o riavviato durante il ritardo, prima dell'esecuzione dell'attività, l'attività non verrà eseguita e il ritardo andrà perso.</span><span class="sxs-lookup"><span data-stu-id="c99e1-150">If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during the delay, before the task runs, then the task will not run and the delay will be lost.</span></span>

## <a name="examples"></a><span data-ttu-id="c99e1-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="c99e1-151">Examples</span></span>

<span data-ttu-id="c99e1-152">Per ulteriori informazioni e un esempio di codice per questo oggetto di scripting, vedere [esempio di trigger di registrazione (scripting)](registration-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="c99e1-152">For more information and a code example for this scripting object, see [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c99e1-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c99e1-153">Requirements</span></span>



| <span data-ttu-id="c99e1-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="c99e1-154">Requirement</span></span> | <span data-ttu-id="c99e1-155">Valore</span><span class="sxs-lookup"><span data-stu-id="c99e1-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c99e1-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c99e1-156">Minimum supported client</span></span><br/> | <span data-ttu-id="c99e1-157">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c99e1-157">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c99e1-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c99e1-158">Minimum supported server</span></span><br/> | <span data-ttu-id="c99e1-159">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c99e1-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c99e1-160">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c99e1-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="c99e1-161"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c99e1-161"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c99e1-162">DLL</span><span class="sxs-lookup"><span data-stu-id="c99e1-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c99e1-163"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c99e1-163"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c99e1-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c99e1-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c99e1-165">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="c99e1-165">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="c99e1-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="c99e1-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="c99e1-167">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="c99e1-167">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





