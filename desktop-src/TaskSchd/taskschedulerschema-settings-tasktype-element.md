---
title: Settings (taskType)-elemento
description: Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Utilità di pianificazione elemento impostazioni
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9133d536aef692a5f9928e10963dff8c454f25fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400473"
---
# <a name="settings-tasktype-element"></a><span data-ttu-id="5f6ae-104">Settings (taskType)-elemento</span><span class="sxs-lookup"><span data-stu-id="5f6ae-104">Settings (taskType) Element</span></span>

<span data-ttu-id="5f6ae-105">Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-105">Specifies the settings that the Task Scheduler uses to perform the task.</span></span>

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="5f6ae-106">L'elemento **Settings** è definito dal tipo complesso [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5f6ae-106">The **Settings** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5f6ae-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="5f6ae-107">Parent element</span></span>



| <span data-ttu-id="5f6ae-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5f6ae-108">Element</span></span>                                          | <span data-ttu-id="5f6ae-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="5f6ae-109">Derived from</span></span>                                                 | <span data-ttu-id="5f6ae-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f6ae-110">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="5f6ae-111">**Attività**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="5f6ae-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="5f6ae-113">Specifica l'attività eseguita dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-113">Specifies the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="5f6ae-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5f6ae-114">Child elements</span></span>



| <span data-ttu-id="5f6ae-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="5f6ae-115">Element</span></span>                                                                                                          | <span data-ttu-id="5f6ae-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f6ae-116">Type</span></span>                                                                                              | <span data-ttu-id="5f6ae-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f6ae-117">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f6ae-118">**AllowHardTerminate**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-118">**AllowHardTerminate**</span></span>](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | <span data-ttu-id="5f6ae-119">boolean</span><span class="sxs-lookup"><span data-stu-id="5f6ae-119">boolean</span></span>                                                                                           | <span data-ttu-id="5f6ae-120">Specifica che l'attività può essere terminata utilizzando TerminateProcess.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-120">Specifies that the task may be terminated using TerminateProcess.</span></span><br/>                                         |
| [<span data-ttu-id="5f6ae-121">**AllowStartOnDemand**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-121">**AllowStartOnDemand**</span></span>](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | <span data-ttu-id="5f6ae-122">boolean</span><span class="sxs-lookup"><span data-stu-id="5f6ae-122">boolean</span></span>                                                                                           | <span data-ttu-id="5f6ae-123">Specifica che l'attività può essere avviata utilizzando il comando Esegui o il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-123">Specifies that the task can be started using either the Run command or the Context menu.</span></span><br/>                  |
| [<span data-ttu-id="5f6ae-124">**DeleteExpiredTaskAfter**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-124">**DeleteExpiredTaskAfter**</span></span>](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | <span data-ttu-id="5f6ae-125">duration</span><span class="sxs-lookup"><span data-stu-id="5f6ae-125">duration</span></span>                                                                                          | <span data-ttu-id="5f6ae-126">Specifica la quantità di tempo di attesa del Utilità di pianificazione prima di eliminare l'attività dopo la scadenza.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-126">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span><br/> |
| [<span data-ttu-id="5f6ae-127">**DisallowStartIfOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-127">**DisallowStartIfOnBatteries**</span></span>](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | <span data-ttu-id="5f6ae-128">boolean</span><span class="sxs-lookup"><span data-stu-id="5f6ae-128">boolean</span></span>                                                                                           | <span data-ttu-id="5f6ae-129">Specifica che l'attività non verrà avviata se il computer è in esecuzione sulle batterie.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-129">Specifies that the task will not be started if the computer is running on batteries.</span></span><br/>                      |
| [<span data-ttu-id="5f6ae-130">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-130">**Enabled**</span></span>](taskschedulerschema-enabled-settingstype-element.md)                                              | <span data-ttu-id="5f6ae-131">boolean</span><span class="sxs-lookup"><span data-stu-id="5f6ae-131">boolean</span></span>                                                                                           | <span data-ttu-id="5f6ae-132">Specifica che l'attività è abilitata.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-132">Specifies that the task is enabled.</span></span> <span data-ttu-id="5f6ae-133">L'attività può essere eseguita solo quando questa impostazione è true.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-133">The task can be performed only when this setting is True.</span></span><br/>             |
| [<span data-ttu-id="5f6ae-134">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-134">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | <span data-ttu-id="5f6ae-135">duration</span><span class="sxs-lookup"><span data-stu-id="5f6ae-135">duration</span></span>                                                                                          | <span data-ttu-id="5f6ae-136">Quantità di tempo consentita per completare l'attività.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-136">Amount of time allowed to complete the task.</span></span><br/>                                                              |
| [<span data-ttu-id="5f6ae-137">**Nascosto**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-137">**Hidden**</span></span>](taskschedulerschema-hidden-settingstype-element.md)                                                | <span data-ttu-id="5f6ae-138">boolean</span><span class="sxs-lookup"><span data-stu-id="5f6ae-138">boolean</span></span>                                                                                           | <span data-ttu-id="5f6ae-139">Specifica che l'attività non sarà visibile nell'interfaccia utente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-139">Specifies that the task will not be visible in the UI by default.</span></span><br/>                                         |
| [<span data-ttu-id="5f6ae-140">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-140">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [<span data-ttu-id="5f6ae-141">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-141">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)                      | <span data-ttu-id="5f6ae-142">Specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in uno stato inattivo.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-142">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/>                    |
| [<span data-ttu-id="5f6ae-143">**MaintenanceSettings**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-143">**MaintenanceSettings**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [<span data-ttu-id="5f6ae-144">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-144">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md)        | <span data-ttu-id="5f6ae-145">Specifica il modo in cui il Utilità di pianificazione esegue le attività durante la manutenzione automatica.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-145">Specifies how the Task Scheduler performs tasks during Automatic maintenance.</span></span><br/>                             |
| [<span data-ttu-id="5f6ae-146">**MultipleInstancesPolicy**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-146">**MultipleInstancesPolicy**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [<span data-ttu-id="5f6ae-147">**multipleInstancesPolicyType**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-147">**multipleInstancesPolicyType**</span></span>](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | <span data-ttu-id="5f6ae-148">Specifica i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-148">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span><br/>       |
| [<span data-ttu-id="5f6ae-149">**Priority**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-149">**Priority**</span></span>](taskschedulerschema-priority-settingstype-element.md)                                            | [<span data-ttu-id="5f6ae-150">**priorityType**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-150">**priorityType**</span></span>](taskschedulerschema-prioritytype-simpletype.md)                               | <span data-ttu-id="5f6ae-151">Specifica il livello di priorità per l'attività.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-151">Specifies the priority level for the task.</span></span><br/>                                                                |
| [<span data-ttu-id="5f6ae-152">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-152">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [<span data-ttu-id="5f6ae-153">**restartType**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-153">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)                                | <span data-ttu-id="5f6ae-154">Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se l'attività non riesce per qualsiasi motivo.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-154">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/>      |
| [<span data-ttu-id="5f6ae-155">**RunOnlyIfIdle**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-155">**RunOnlyIfIdle**</span></span>](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | <span data-ttu-id="5f6ae-156">boolean</span><span class="sxs-lookup"><span data-stu-id="5f6ae-156">boolean</span></span>                                                                                           | <span data-ttu-id="5f6ae-157">Specifica che l'attività viene eseguita solo quando il computer è in stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-157">Specifies that the task is run only when the computer is in an idle state.</span></span><br/>                                |
| [<span data-ttu-id="5f6ae-158">**RunOnlyIfNetworkAvailable**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-158">**RunOnlyIfNetworkAvailable**</span></span>](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | <span data-ttu-id="5f6ae-159">boolean</span><span class="sxs-lookup"><span data-stu-id="5f6ae-159">boolean</span></span>                                                                                           | <span data-ttu-id="5f6ae-160">Specifica che l'Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-160">Specifies that the Task Scheduler will run the task only when a network is available.</span></span><br/>                     |
| [<span data-ttu-id="5f6ae-161">**StartWhenAvailable**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-161">**StartWhenAvailable**</span></span>](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | <span data-ttu-id="5f6ae-162">boolean</span><span class="sxs-lookup"><span data-stu-id="5f6ae-162">boolean</span></span>                                                                                           | <span data-ttu-id="5f6ae-163">Specifica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorso il relativo orario pianificato.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-163">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span><br/>     |
| [<span data-ttu-id="5f6ae-164">**StopIfGoingOnBatteries (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-164">**StopIfGoingOnBatteries (settingsType)**</span></span>](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | <span data-ttu-id="5f6ae-165">boolean</span><span class="sxs-lookup"><span data-stu-id="5f6ae-165">boolean</span></span>                                                                                           | <span data-ttu-id="5f6ae-166">Specifica che l'attività verrà arrestata se il computer sta per accedere alle batterie.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-166">Specifies that the task will be stopped if the computer is going onto batteries.</span></span><br/>                          |
| [<span data-ttu-id="5f6ae-167">**Volatile**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-167">**Volatile**</span></span>](taskschedulerschema-volatile-element.md)                                                         | <span data-ttu-id="5f6ae-168">boolean</span><span class="sxs-lookup"><span data-stu-id="5f6ae-168">boolean</span></span>                                                                                           | <span data-ttu-id="5f6ae-169">Specifica se l'attività viene disabilitata automaticamente da Utilità di pianificazione all'avvio di Windows.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-169">Specifies if the task is automatically disabled by Task Scheduler at Windows startup.</span></span><br/>                     |
| [<span data-ttu-id="5f6ae-170">**WakeToRun (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="5f6ae-170">**WakeToRun (settingsType)**</span></span>](taskschedulerschema-waketorun-settingstype-element.md)                           | <span data-ttu-id="5f6ae-171">boolean</span><span class="sxs-lookup"><span data-stu-id="5f6ae-171">boolean</span></span>                                                                                           | <span data-ttu-id="5f6ae-172">Specifica che Utilità di pianificazione riattiverà il computer al momento dell'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-172">Specifies that Task Scheduler will wake the computer when it is time to run the task.</span></span><br/>                     |



## <a name="remarks"></a><span data-ttu-id="5f6ae-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f6ae-173">Remarks</span></span>

<span data-ttu-id="5f6ae-174">È possibile selezionare uno o più elementi figlio a cui si fa riferimento sopra.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-174">You can select one or more of the child elements referenced above.</span></span>

<span data-ttu-id="5f6ae-175">Per lo sviluppo in C++, le informazioni di registrazione di un'attività vengono specificate utilizzando la [**Proprietà Settings di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).</span><span class="sxs-lookup"><span data-stu-id="5f6ae-175">For C++ development, the registration information of a task is specified using the [**Settings property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).</span></span>

<span data-ttu-id="5f6ae-176">Per lo sviluppo di script, le informazioni di registrazione di un'attività vengono specificate utilizzando la proprietà [**TaskDefinition. Settings**](taskdefinition-settings.md) .</span><span class="sxs-lookup"><span data-stu-id="5f6ae-176">For scripting development, the registration information of a task is specified using the [**TaskDefinition.Settings**](taskdefinition-settings.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="5f6ae-177">Esempio</span><span class="sxs-lookup"><span data-stu-id="5f6ae-177">Examples</span></span>

<span data-ttu-id="5f6ae-178">Nell'esempio di codice XML seguente viene definito un elemento Settings che consente la terminazione rigida dell'attività.</span><span class="sxs-lookup"><span data-stu-id="5f6ae-178">The following XML code example defines a settings element that allows a hard termination of the task.</span></span>


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



<span data-ttu-id="5f6ae-179">Per ulteriori informazioni e un esempio completo del codice XML per l'impostazione delle impostazioni delle attività, vedere [esempio di trigger di ora (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="5f6ae-179">For more information and a complete example of the XML for setting task settings, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f6ae-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f6ae-180">Requirements</span></span>



| <span data-ttu-id="5f6ae-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f6ae-181">Requirement</span></span> | <span data-ttu-id="5f6ae-182">Valore</span><span class="sxs-lookup"><span data-stu-id="5f6ae-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5f6ae-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f6ae-183">Minimum supported client</span></span><br/> | <span data-ttu-id="5f6ae-184">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f6ae-184">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5f6ae-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f6ae-185">Minimum supported server</span></span><br/> | <span data-ttu-id="5f6ae-186">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5f6ae-186">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f6ae-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f6ae-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f6ae-188">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5f6ae-188">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5f6ae-189">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5f6ae-189">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





