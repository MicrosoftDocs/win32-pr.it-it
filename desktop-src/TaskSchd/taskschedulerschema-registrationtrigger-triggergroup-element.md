---
title: Elemento RegistrationTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando l'attività è registrata.
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- Utilità di pianificazione trigger di registrazione, elemento XML
- Utilità di pianificazione elemento RegistrationTrigger
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90960f81d252b0b0a8d1de3ab5cc1465003467a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302001"
---
# <a name="registrationtrigger-triggergroup-element"></a><span data-ttu-id="05345-105">Elemento RegistrationTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="05345-105">RegistrationTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="05345-106">Specifica un trigger che avvia un'attività quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="05345-106">Specifies a trigger that starts a task when the task is registered.</span></span>

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

<span data-ttu-id="05345-107">L'elemento **RegistrationTrigger** è definito dal tipo complesso [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="05345-107">The **RegistrationTrigger** element is defined by the [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="05345-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="05345-108">Parent element</span></span>



| <span data-ttu-id="05345-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="05345-109">Element</span></span>                                                           | <span data-ttu-id="05345-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="05345-110">Derived from</span></span>                                                         | <span data-ttu-id="05345-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05345-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="05345-112">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="05345-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="05345-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="05345-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="05345-114">Specifica i trigger che avviano l'attività.</span><span class="sxs-lookup"><span data-stu-id="05345-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="05345-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="05345-115">Child elements</span></span>



| <span data-ttu-id="05345-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="05345-116">Element</span></span>                                                                                                        | <span data-ttu-id="05345-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="05345-117">Type</span></span>                                                                     | <span data-ttu-id="05345-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05345-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05345-119">**Ritardo (registrationTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="05345-119">**Delay (registrationTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)                   | <span data-ttu-id="05345-120">duration</span><span class="sxs-lookup"><span data-stu-id="05345-120">duration</span></span>                                                                 | <span data-ttu-id="05345-121">Specifica l'intervallo di tempo tra il momento in cui l'attività viene registrata e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="05345-121">Specifies the amount of time between when the task is registered and when the task is started.</span></span><br/>                          |
| [<span data-ttu-id="05345-122">**Abilitato (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="05345-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="05345-123">boolean</span><span class="sxs-lookup"><span data-stu-id="05345-123">boolean</span></span>                                                                  | <span data-ttu-id="05345-124">Specifica che il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="05345-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="05345-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="05345-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="05345-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="05345-126">dateTime</span></span>                                                                 | <span data-ttu-id="05345-127">Specifica la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="05345-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="05345-128">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="05345-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="05345-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="05345-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="05345-130">duration</span><span class="sxs-lookup"><span data-stu-id="05345-130">duration</span></span>                                                                 | <span data-ttu-id="05345-131">Specifica l'intervallo di tempo massimo in cui l'attività può essere avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="05345-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="05345-132">**Ripetizione (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="05345-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="05345-133">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="05345-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="05345-134">Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="05345-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="05345-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="05345-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="05345-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="05345-136">dateTime</span></span>                                                                 | <span data-ttu-id="05345-137">Specifica la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="05345-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="05345-138">Attributi</span><span class="sxs-lookup"><span data-stu-id="05345-138">Attributes</span></span>



| <span data-ttu-id="05345-139">Nome</span><span class="sxs-lookup"><span data-stu-id="05345-139">Name</span></span> | <span data-ttu-id="05345-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="05345-140">Type</span></span> | <span data-ttu-id="05345-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05345-141">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="05345-142">Id</span><span class="sxs-lookup"><span data-stu-id="05345-142">Id</span></span>   | <span data-ttu-id="05345-143">ID</span><span class="sxs-lookup"><span data-stu-id="05345-143">ID</span></span>   | <span data-ttu-id="05345-144">Identificatore del trigger.</span><span class="sxs-lookup"><span data-stu-id="05345-144">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="05345-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="05345-145">Remarks</span></span>

<span data-ttu-id="05345-146">Per lo sviluppo di script, viene specificato un trigger di registrazione tramite l'oggetto [**RegistrationTrigger**](registrationtrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="05345-146">For scripting development, a registration trigger is specified using the [**RegistrationTrigger**](registrationtrigger.md) object.</span></span>

<span data-ttu-id="05345-147">Per lo sviluppo in C++, viene specificato un trigger di registrazione tramite l'interfaccia [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) .</span><span class="sxs-lookup"><span data-stu-id="05345-147">For C++ development, a registration trigger is specified using the [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) interface.</span></span>

<span data-ttu-id="05345-148">Gli elementi figlio elencati sopra sono definiti dai tipi di elemento complessi [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) e [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="05345-148">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex element types.</span></span> <span data-ttu-id="05345-149">Questi elementi devono essere aggiunti nella sequenza illustrata di seguito.</span><span class="sxs-lookup"><span data-stu-id="05345-149">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="05345-150">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="05345-150">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="05345-151">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="05345-151">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="05345-152">**Abilitato (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="05345-152">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="05345-153">**Ripetizione (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="05345-153">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="05345-154">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="05345-154">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [<span data-ttu-id="05345-155">**Ritardo (registrationTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="05345-155">**Delay (registrationTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a><span data-ttu-id="05345-156">Esempio</span><span class="sxs-lookup"><span data-stu-id="05345-156">Examples</span></span>

<span data-ttu-id="05345-157">Per un esempio completo del codice XML per un'attività che specifica un trigger di avvio, vedere [esempio di trigger di registrazione (XML)](registration-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="05345-157">For a complete example of the XML for a task that specifies a boot trigger, see [Registration Trigger Example (XML)](registration-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05345-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05345-158">Requirements</span></span>



| <span data-ttu-id="05345-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="05345-159">Requirement</span></span> | <span data-ttu-id="05345-160">Valore</span><span class="sxs-lookup"><span data-stu-id="05345-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05345-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05345-161">Minimum supported client</span></span><br/> | <span data-ttu-id="05345-162">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05345-162">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05345-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05345-163">Minimum supported server</span></span><br/> | <span data-ttu-id="05345-164">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05345-164">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05345-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05345-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05345-166">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="05345-166">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="05345-167">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="05345-167">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





