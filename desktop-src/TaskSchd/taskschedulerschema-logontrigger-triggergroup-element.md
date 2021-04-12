---
title: Elemento LogonTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.
ms.assetid: c3edee50-e053-4813-a1b2-bf1e7b575ff7
keywords:
- trigger LOGON, elemento XML
- Utilità di pianificazione elemento LogonTrigger
topic_type:
- apiref
api_name:
- LogonTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89d0e593277f1c854850017412b49c22d8ac436
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340543"
---
# <a name="logontrigger-triggergroup-element"></a><span data-ttu-id="767ef-105">Elemento LogonTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="767ef-105">LogonTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="767ef-106">Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="767ef-106">Specifies a trigger that starts a task when a user logs on.</span></span>

``` syntax
<xs:element name="LogonTrigger"
    type="logonTriggerType"
 />
```

<span data-ttu-id="767ef-107">L'elemento **LogonTrigger** è definito da [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="767ef-107">The **LogonTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="767ef-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="767ef-108">Parent element</span></span>



| <span data-ttu-id="767ef-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="767ef-109">Element</span></span>                                                           | <span data-ttu-id="767ef-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="767ef-110">Derived from</span></span>                                                         | <span data-ttu-id="767ef-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="767ef-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="767ef-112">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="767ef-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="767ef-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="767ef-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="767ef-114">Specifica i trigger che avviano l'attività.</span><span class="sxs-lookup"><span data-stu-id="767ef-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="767ef-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="767ef-115">Child elements</span></span>



| <span data-ttu-id="767ef-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="767ef-116">Element</span></span>                                                                                                        | <span data-ttu-id="767ef-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="767ef-117">Type</span></span>                                                                     | <span data-ttu-id="767ef-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="767ef-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="767ef-119">**Ritardo (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="767ef-119">**Delay (logonTriggerType)**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)                         | <span data-ttu-id="767ef-120">duration</span><span class="sxs-lookup"><span data-stu-id="767ef-120">duration</span></span>                                                                 | <span data-ttu-id="767ef-121">Intervallo di tempo tra il momento in cui l'utente esegue l'accesso e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="767ef-121">Amount of time between when the user logs on and when the task is started.</span></span><br/>                                              |
| [<span data-ttu-id="767ef-122">**Abilitato (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="767ef-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="767ef-123">boolean</span><span class="sxs-lookup"><span data-stu-id="767ef-123">boolean</span></span>                                                                  | <span data-ttu-id="767ef-124">Specifica che il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="767ef-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="767ef-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="767ef-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="767ef-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="767ef-126">dateTime</span></span>                                                                 | <span data-ttu-id="767ef-127">Specifica la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="767ef-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="767ef-128">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="767ef-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="767ef-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="767ef-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="767ef-130">duration</span><span class="sxs-lookup"><span data-stu-id="767ef-130">duration</span></span>                                                                 | <span data-ttu-id="767ef-131">Specifica l'intervallo di tempo massimo in cui l'attività può essere avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="767ef-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="767ef-132">**Ripetizione (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="767ef-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="767ef-133">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="767ef-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="767ef-134">Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="767ef-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="767ef-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="767ef-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="767ef-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="767ef-136">dateTime</span></span>                                                                 | <span data-ttu-id="767ef-137">Specifica la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="767ef-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="767ef-138">**UserId (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="767ef-138">**UserId (logonTriggerType)**</span></span>](taskschedulerschema-userid-logontriggertype-element.md)                       | <span data-ttu-id="767ef-139">string</span><span class="sxs-lookup"><span data-stu-id="767ef-139">string</span></span>                                                                   | <span data-ttu-id="767ef-140">Identificatore dell'utente.</span><span class="sxs-lookup"><span data-stu-id="767ef-140">Identifier of the user.</span></span> <span data-ttu-id="767ef-141">L'attività viene avviata quando l'utente accede al computer.</span><span class="sxs-lookup"><span data-stu-id="767ef-141">The task is started when this user logs onto the computer.</span></span><br/>                                      |



## <a name="remarks"></a><span data-ttu-id="767ef-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="767ef-142">Remarks</span></span>

<span data-ttu-id="767ef-143">Per lo sviluppo di script, viene specificato un trigger LOGON utilizzando l'oggetto [**LogonTrigger**](logontrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="767ef-143">For scripting development, a logon trigger is specified using the [**LogonTrigger**](logontrigger.md) object.</span></span>

<span data-ttu-id="767ef-144">Per lo sviluppo in C++, viene specificato un trigger LOGON usando l'interfaccia [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) .</span><span class="sxs-lookup"><span data-stu-id="767ef-144">For C++ development, a logon trigger is specified using the [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) interface.</span></span>

<span data-ttu-id="767ef-145">Gli elementi figlio elencati sopra sono definiti dai tipi di elemento complessi [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) e [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="767ef-145">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex element types.</span></span> <span data-ttu-id="767ef-146">Questi elementi devono essere aggiunti nella sequenza illustrata di seguito.</span><span class="sxs-lookup"><span data-stu-id="767ef-146">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="767ef-147">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="767ef-147">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="767ef-148">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="767ef-148">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="767ef-149">**Abilitato (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="767ef-149">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="767ef-150">**Ripetizione (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="767ef-150">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="767ef-151">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="767ef-151">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [<span data-ttu-id="767ef-152">**UserId (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="767ef-152">**UserId (logonTriggerType)**</span></span>](taskschedulerschema-userid-logontriggertype-element.md)
-   [<span data-ttu-id="767ef-153">**Ritardo (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="767ef-153">**Delay (logonTriggerType)**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)

### <a name="attributes"></a><span data-ttu-id="767ef-154">Attributi</span><span class="sxs-lookup"><span data-stu-id="767ef-154">Attributes</span></span>

<span data-ttu-id="767ef-155">L'attributo riportato di seguito è definito dai tipi di elemento complessi [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="767ef-155">The attribute listed below is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span>

-   <span data-ttu-id="767ef-156">ID: identificatore del trigger.</span><span class="sxs-lookup"><span data-stu-id="767ef-156">Id: Identifier of the trigger.</span></span>

## <a name="examples"></a><span data-ttu-id="767ef-157">Esempio</span><span class="sxs-lookup"><span data-stu-id="767ef-157">Examples</span></span>

<span data-ttu-id="767ef-158">Per un esempio completo del codice XML per un'attività che usa un trigger LOGON, vedere [esempio di trigger LOGON (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="767ef-158">For a complete example of the XML for a task that uses a logon trigger, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="767ef-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="767ef-159">Requirements</span></span>



| <span data-ttu-id="767ef-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="767ef-160">Requirement</span></span> | <span data-ttu-id="767ef-161">Valore</span><span class="sxs-lookup"><span data-stu-id="767ef-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="767ef-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="767ef-162">Minimum supported client</span></span><br/> | <span data-ttu-id="767ef-163">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="767ef-163">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="767ef-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="767ef-164">Minimum supported server</span></span><br/> | <span data-ttu-id="767ef-165">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="767ef-165">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="767ef-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="767ef-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="767ef-167">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="767ef-167">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





