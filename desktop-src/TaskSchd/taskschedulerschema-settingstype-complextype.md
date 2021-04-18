---
title: Tipo complesso settingsType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento Settings (taskType).
ms.assetid: dba6b82d-aaa4-4f77-aeb1-c5a8f81aec25
keywords:
- Utilità di pianificazione di tipo complesso settingsType
topic_type:
- apiref
api_name:
- settingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3c2b3128a35ee0e46c56d19badd431400d4d862
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302000"
---
# <a name="settingstype-complex-type"></a><span data-ttu-id="3c83c-104">Tipo complesso settingsType</span><span class="sxs-lookup"><span data-stu-id="3c83c-104">settingsType Complex Type</span></span>

<span data-ttu-id="3c83c-105">Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**Settings (TaskType)**](taskschedulerschema-settings-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3c83c-105">Defines the child elements and sequencing information for the [**Settings (taskType)**](taskschedulerschema-settings-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="settingsType">
    <xs:all>
        <xs:element name="AllowStartOnDemand"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnFailure"
            type="restartType"
            minOccurs="0"
         />
        <xs:element name="MultipleInstancesPolicy"
            type="multipleInstancesPolicyType"
            default="IgnoreNew"
            minOccurs="0"
         />
        <xs:element name="DisallowStartIfOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StopIfGoingOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="AllowHardTerminate"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartWhenAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="NetworkProfileName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfNetworkAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="WakeToRun"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="Hidden"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DeleteExpiredTaskAfter"
            type="duration"
            default="PT0S"
            minOccurs="0"
         />
        <xs:element name="IdleSettings"
            type="idleSettingsType"
            minOccurs="0"
         />
        <xs:element name="NetworkSettings"
            type="networkSettingsType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
        <xs:element name="Priority"
            type="priorityType"
            default="7"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="UseUnifiedSchedulingEngine"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DisallowStartOnRemoteAppSession"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3c83c-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3c83c-106">Child elements</span></span>



| <span data-ttu-id="3c83c-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="3c83c-107">Element</span></span>                                                                                                             | <span data-ttu-id="3c83c-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c83c-108">Type</span></span>                                                                                              | <span data-ttu-id="3c83c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c83c-109">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c83c-110">**AllowHardTerminate**</span><span class="sxs-lookup"><span data-stu-id="3c83c-110">**AllowHardTerminate**</span></span>](taskschedulerschema-allowhardterminate-settingstype-element.md)                           | <span data-ttu-id="3c83c-111">boolean</span><span class="sxs-lookup"><span data-stu-id="3c83c-111">boolean</span></span>                                                                                           | <span data-ttu-id="3c83c-112">Specifica se il servizio Utilità di pianificazione consente la terminazione rigida dell'attività.</span><span class="sxs-lookup"><span data-stu-id="3c83c-112">Specifies if the Task Scheduler service allows hard termination of the task.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="3c83c-113">**AllowStartOnDemand**</span><span class="sxs-lookup"><span data-stu-id="3c83c-113">**AllowStartOnDemand**</span></span>](taskschedulerschema-allowstartondemand-settingstype-element.md)                           | <span data-ttu-id="3c83c-114">boolean</span><span class="sxs-lookup"><span data-stu-id="3c83c-114">boolean</span></span>                                                                                           | <span data-ttu-id="3c83c-115">Specifica che l'attività può essere avviata tramite il comando Esegui o il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="3c83c-115">Specifies that the task can be started by using either the Run command or the Context menu.</span></span> <br/>                                                                                                                                                                                                             |
| [<span data-ttu-id="3c83c-116">**DeleteExpiredTaskAfter**</span><span class="sxs-lookup"><span data-stu-id="3c83c-116">**DeleteExpiredTaskAfter**</span></span>](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                   | <span data-ttu-id="3c83c-117">duration</span><span class="sxs-lookup"><span data-stu-id="3c83c-117">duration</span></span>                                                                                          | <span data-ttu-id="3c83c-118">Specifica la quantità di tempo di attesa del Utilità di pianificazione prima di eliminare l'attività dopo la scadenza.</span><span class="sxs-lookup"><span data-stu-id="3c83c-118">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="3c83c-119">Se per questo elemento non viene specificato alcun valore, il servizio Utilità di pianificazione non eliminerà l'attività.</span><span class="sxs-lookup"><span data-stu-id="3c83c-119">If no value is specified for this element, then the Task Scheduler service will not delete the task.</span></span><br/>                                                                                           |
| [<span data-ttu-id="3c83c-120">**DisallowStartIfOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="3c83c-120">**DisallowStartIfOnBatteries**</span></span>](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)           | <span data-ttu-id="3c83c-121">boolean</span><span class="sxs-lookup"><span data-stu-id="3c83c-121">boolean</span></span>                                                                                           | <span data-ttu-id="3c83c-122">Specifica che l'attività non verrà avviata se il computer è alimentato a batteria.</span><span class="sxs-lookup"><span data-stu-id="3c83c-122">Specifies that the task will not be started if the computer is running on battery power.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="3c83c-123">**DisallowStartOnRemoteAppSession**</span><span class="sxs-lookup"><span data-stu-id="3c83c-123">**DisallowStartOnRemoteAppSession**</span></span>](taskschedulerschema-disallowstartonremoteappsession-settingstype-element.md) | <span data-ttu-id="3c83c-124">boolean</span><span class="sxs-lookup"><span data-stu-id="3c83c-124">boolean</span></span>                                                                                           | <span data-ttu-id="3c83c-125">Specifica che l'attività non deve essere avviata se l'attività viene attivata per l'esecuzione in una sessione di applicazioni remote integrata localmente (RAIL).</span><span class="sxs-lookup"><span data-stu-id="3c83c-125">Specifies that the task should not start if the task is triggered to run in a Remote Applications Integrated Locally (RAIL) session.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="3c83c-126">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="3c83c-126">**Enabled**</span></span>](taskschedulerschema-enabled-settingstype-element.md)                                                 | <span data-ttu-id="3c83c-127">boolean</span><span class="sxs-lookup"><span data-stu-id="3c83c-127">boolean</span></span>                                                                                           | <span data-ttu-id="3c83c-128">Specifica che l'attività è abilitata.</span><span class="sxs-lookup"><span data-stu-id="3c83c-128">Specifies that the task is enabled.</span></span> <span data-ttu-id="3c83c-129">L'attività può essere eseguita solo quando questa impostazione è **true**.</span><span class="sxs-lookup"><span data-stu-id="3c83c-129">The task can be performed only when this setting is **True**.</span></span><br/>                                                                                                                                                                                                        |
| [<span data-ttu-id="3c83c-130">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="3c83c-130">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-settingstype-element.md)                           | <span data-ttu-id="3c83c-131">duration</span><span class="sxs-lookup"><span data-stu-id="3c83c-131">duration</span></span>                                                                                          | <span data-ttu-id="3c83c-132">Specifica la quantità di tempo consentita per completare l'attività.</span><span class="sxs-lookup"><span data-stu-id="3c83c-132">Specifies the amount of time allowed to complete the task.</span></span><br/>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="3c83c-133">**Nascosto**</span><span class="sxs-lookup"><span data-stu-id="3c83c-133">**Hidden**</span></span>](taskschedulerschema-hidden-settingstype-element.md)                                                   | <span data-ttu-id="3c83c-134">boolean</span><span class="sxs-lookup"><span data-stu-id="3c83c-134">boolean</span></span>                                                                                           | <span data-ttu-id="3c83c-135">Specifica che, per impostazione predefinita, l'attività non sarà visibile nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="3c83c-135">Specifies, by default, that the task will not be visible in the user interface (UI).</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="3c83c-136">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="3c83c-136">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md)                                       | [<span data-ttu-id="3c83c-137">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="3c83c-137">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)                      | <span data-ttu-id="3c83c-138">Specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in uno stato inattivo.</span><span class="sxs-lookup"><span data-stu-id="3c83c-138">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/>                                                                                                                                                                                                                   |
| [<span data-ttu-id="3c83c-139">**MultipleInstancesPolicy**</span><span class="sxs-lookup"><span data-stu-id="3c83c-139">**MultipleInstancesPolicy**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)                 | [<span data-ttu-id="3c83c-140">**multipleInstancesPolicyType**</span><span class="sxs-lookup"><span data-stu-id="3c83c-140">**multipleInstancesPolicyType**</span></span>](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | <span data-ttu-id="3c83c-141">Specifica i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.</span><span class="sxs-lookup"><span data-stu-id="3c83c-141">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span> <br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="3c83c-142">**NetworkProfileName**</span><span class="sxs-lookup"><span data-stu-id="3c83c-142">**NetworkProfileName**</span></span>](taskschedulerschema-networkprofilename-settingstype-element.md)                           | <span data-ttu-id="3c83c-143">string</span><span class="sxs-lookup"><span data-stu-id="3c83c-143">string</span></span>                                                                                            | <span data-ttu-id="3c83c-144">Specifica il nome di un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="3c83c-144">Specifies the name of a network profile.</span></span> <span data-ttu-id="3c83c-145">Il servizio Utilità di pianificazione verifica la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="3c83c-145">The Task Scheduler service verifies the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span> <span data-ttu-id="3c83c-146">Il nome viene usato a scopo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3c83c-146">The name is used for display purposes.</span></span><br/>        |
| [<span data-ttu-id="3c83c-147">**NetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="3c83c-147">**NetworkSettings**</span></span>](taskschedulerschema-networksettings-settingstype-element.md)                                 | [<span data-ttu-id="3c83c-148">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="3c83c-148">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md)                | <span data-ttu-id="3c83c-149">Specifica le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="3c83c-149">Specifies the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="3c83c-150">Il servizio Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="3c83c-150">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |
| [<span data-ttu-id="3c83c-151">**Priority**</span><span class="sxs-lookup"><span data-stu-id="3c83c-151">**Priority**</span></span>](taskschedulerschema-priority-settingstype-element.md)                                               | [<span data-ttu-id="3c83c-152">**priorityType**</span><span class="sxs-lookup"><span data-stu-id="3c83c-152">**priorityType**</span></span>](taskschedulerschema-prioritytype-simpletype.md)                               | <span data-ttu-id="3c83c-153">Specifica il livello di priorità per l'attività.</span><span class="sxs-lookup"><span data-stu-id="3c83c-153">Specifies the priority level for the task.</span></span><br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="3c83c-154">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="3c83c-154">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md)                               | [<span data-ttu-id="3c83c-155">**restartType**</span><span class="sxs-lookup"><span data-stu-id="3c83c-155">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)                                | <span data-ttu-id="3c83c-156">Specifica che il Utilità di pianificazione tenterà di riavviare l'attività in caso di esito negativo per qualsiasi motivo.</span><span class="sxs-lookup"><span data-stu-id="3c83c-156">Specifies that the Task Scheduler will attempt to restart the task if it fails for any reason.</span></span> <br/>                                                                                                                                                                                                          |
| [<span data-ttu-id="3c83c-157">**RunOnlyIfIdle**</span><span class="sxs-lookup"><span data-stu-id="3c83c-157">**RunOnlyIfIdle**</span></span>](taskschedulerschema-runonlyifidle-settingstype-element.md)                                     | <span data-ttu-id="3c83c-158">boolean</span><span class="sxs-lookup"><span data-stu-id="3c83c-158">boolean</span></span>                                                                                           | <span data-ttu-id="3c83c-159">Specifica che l'attività viene eseguita solo quando il computer è in stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="3c83c-159">Specifies that the task is run only when the computer is in an idle state.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="3c83c-160">**RunOnlyIfNetworkAvailable**</span><span class="sxs-lookup"><span data-stu-id="3c83c-160">**RunOnlyIfNetworkAvailable**</span></span>](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)             | <span data-ttu-id="3c83c-161">boolean</span><span class="sxs-lookup"><span data-stu-id="3c83c-161">boolean</span></span>                                                                                           | <span data-ttu-id="3c83c-162">Specifica che l'Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.</span><span class="sxs-lookup"><span data-stu-id="3c83c-162">Specifies that the Task Scheduler will run the task only when a network is available.</span></span><br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="3c83c-163">**StartWhenAvailable**</span><span class="sxs-lookup"><span data-stu-id="3c83c-163">**StartWhenAvailable**</span></span>](taskschedulerschema-startwhenavailable-settingstype-element.md)                           | <span data-ttu-id="3c83c-164">boolean</span><span class="sxs-lookup"><span data-stu-id="3c83c-164">boolean</span></span>                                                                                           | <span data-ttu-id="3c83c-165">Specifica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorso il relativo orario pianificato.</span><span class="sxs-lookup"><span data-stu-id="3c83c-165">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="3c83c-166">**StopIfGoingOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="3c83c-166">**StopIfGoingOnBatteries**</span></span>](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md)                   | <span data-ttu-id="3c83c-167">boolean</span><span class="sxs-lookup"><span data-stu-id="3c83c-167">boolean</span></span>                                                                                           | <span data-ttu-id="3c83c-168">Specifica che l'attività verrà arrestata se il computer passa all'alimentazione a batteria.</span><span class="sxs-lookup"><span data-stu-id="3c83c-168">Specifies that the task will be stopped if the computer switches to battery power.</span></span> <br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="3c83c-169">**UseUnifiedSchedulingEngine**</span><span class="sxs-lookup"><span data-stu-id="3c83c-169">**UseUnifiedSchedulingEngine**</span></span>](taskschedulerschema-useunifiedschedulingengine-settingstype-element.md)           | <span data-ttu-id="3c83c-170">boolean</span><span class="sxs-lookup"><span data-stu-id="3c83c-170">boolean</span></span>                                                                                           | <span data-ttu-id="3c83c-171">Specifica che l'attività viene eseguita utilizzando il motore di pianificazione unificato.</span><span class="sxs-lookup"><span data-stu-id="3c83c-171">Specifies that the task is run by using the Unified Scheduling Engine.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="3c83c-172">**WakeToRun**</span><span class="sxs-lookup"><span data-stu-id="3c83c-172">**WakeToRun**</span></span>](taskschedulerschema-waketorun-settingstype-element.md)                                             | <span data-ttu-id="3c83c-173">boolean</span><span class="sxs-lookup"><span data-stu-id="3c83c-173">boolean</span></span>                                                                                           | <span data-ttu-id="3c83c-174">Specifica che Utilità di pianificazione riattiverà il computer prima di eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="3c83c-174">Specifies that Task Scheduler will wake the computer before it runs the task.</span></span><br/>                                                                                                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="3c83c-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c83c-175">Requirements</span></span>



| <span data-ttu-id="3c83c-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c83c-176">Requirement</span></span> | <span data-ttu-id="3c83c-177">Valore</span><span class="sxs-lookup"><span data-stu-id="3c83c-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3c83c-178">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c83c-178">Minimum supported client</span></span><br/> | <span data-ttu-id="3c83c-179">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c83c-179">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3c83c-180">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c83c-180">Minimum supported server</span></span><br/> | <span data-ttu-id="3c83c-181">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3c83c-181">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c83c-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c83c-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c83c-183">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3c83c-183">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="3c83c-184">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3c83c-184">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





