---
title: Elemento IdleTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando il computer entra in uno stato di inattività.
ms.assetid: c3e317b5-d1a7-46de-ace5-e066452583d3
keywords:
- Trigger inattivo, elemento XML
- Utilità di pianificazione elemento IdleTrigger
topic_type:
- apiref
api_name:
- IdleTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 221d272145670b9514cde5ffbe8b02e5ddcd6e0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048038"
---
# <a name="idletrigger-triggergroup-element"></a><span data-ttu-id="75d1a-105">Elemento IdleTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="75d1a-105">IdleTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="75d1a-106">Specifica un trigger che avvia un'attività quando il computer entra in uno stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="75d1a-106">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span> <span data-ttu-id="75d1a-107">Per informazioni sulle condizioni di inattività, vedere [condizioni](task-idle-conditions.md)di inattività.</span><span class="sxs-lookup"><span data-stu-id="75d1a-107">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

``` syntax
<xs:element name="IdleTrigger"
    type="idleTriggerType"
 />
```

<span data-ttu-id="75d1a-108">L'elemento **IdleTrigger** è definito da [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="75d1a-108">The **IdleTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="75d1a-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="75d1a-109">Parent element</span></span>



| <span data-ttu-id="75d1a-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="75d1a-110">Element</span></span>                                                           | <span data-ttu-id="75d1a-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="75d1a-111">Derived from</span></span>                                                         | <span data-ttu-id="75d1a-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75d1a-112">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="75d1a-113">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="75d1a-113">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="75d1a-114">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="75d1a-114">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="75d1a-115">Specifica i trigger che avviano l'attività.</span><span class="sxs-lookup"><span data-stu-id="75d1a-115">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="75d1a-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="75d1a-116">Child elements</span></span>



| <span data-ttu-id="75d1a-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="75d1a-117">Element</span></span>                                                                                                        | <span data-ttu-id="75d1a-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="75d1a-118">Type</span></span>                                                                     | <span data-ttu-id="75d1a-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75d1a-119">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75d1a-120">**Abilitato (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="75d1a-120">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="75d1a-121">boolean</span><span class="sxs-lookup"><span data-stu-id="75d1a-121">boolean</span></span>                                                                  | <span data-ttu-id="75d1a-122">Specifica che il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="75d1a-122">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="75d1a-123">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="75d1a-123">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="75d1a-124">dateTime</span><span class="sxs-lookup"><span data-stu-id="75d1a-124">dateTime</span></span>                                                                 | <span data-ttu-id="75d1a-125">Specifica la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="75d1a-125">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="75d1a-126">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="75d1a-126">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="75d1a-127">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="75d1a-127">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="75d1a-128">duration</span><span class="sxs-lookup"><span data-stu-id="75d1a-128">duration</span></span>                                                                 | <span data-ttu-id="75d1a-129">Specifica l'intervallo di tempo massimo in cui l'attività può essere avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="75d1a-129">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="75d1a-130">**Ripetizione (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="75d1a-130">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="75d1a-131">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="75d1a-131">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="75d1a-132">Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="75d1a-132">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="75d1a-133">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="75d1a-133">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="75d1a-134">dateTime</span><span class="sxs-lookup"><span data-stu-id="75d1a-134">dateTime</span></span>                                                                 | <span data-ttu-id="75d1a-135">Specifica la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="75d1a-135">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="75d1a-136">Attributi</span><span class="sxs-lookup"><span data-stu-id="75d1a-136">Attributes</span></span>



| <span data-ttu-id="75d1a-137">Nome</span><span class="sxs-lookup"><span data-stu-id="75d1a-137">Name</span></span> | <span data-ttu-id="75d1a-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="75d1a-138">Type</span></span>   | <span data-ttu-id="75d1a-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75d1a-139">Description</span></span>                               |
|------|--------|-------------------------------------------|
| <span data-ttu-id="75d1a-140">Id</span><span class="sxs-lookup"><span data-stu-id="75d1a-140">Id</span></span>   | <span data-ttu-id="75d1a-141">string</span><span class="sxs-lookup"><span data-stu-id="75d1a-141">string</span></span> | <span data-ttu-id="75d1a-142">Identificatore del trigger.</span><span class="sxs-lookup"><span data-stu-id="75d1a-142">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="75d1a-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="75d1a-143">Remarks</span></span>

<span data-ttu-id="75d1a-144">Per lo sviluppo di script, viene specificato un trigger inattivo tramite l'oggetto [**IdleTrigger**](idletrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="75d1a-144">For scripting development, an idle trigger is specified using the [**IdleTrigger**](idletrigger.md) object.</span></span>

<span data-ttu-id="75d1a-145">Per lo sviluppo in C++, un trigger inattivo viene specificato tramite l'interfaccia [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) .</span><span class="sxs-lookup"><span data-stu-id="75d1a-145">For C++ development, an idle trigger is specified using the [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) interface.</span></span>

<span data-ttu-id="75d1a-146">Gli elementi figlio elencati sopra sono definiti dai tipi di elemento complessi [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="75d1a-146">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span> <span data-ttu-id="75d1a-147">Questi elementi devono essere aggiunti nella sequenza illustrata di seguito.</span><span class="sxs-lookup"><span data-stu-id="75d1a-147">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="75d1a-148">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="75d1a-148">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="75d1a-149">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="75d1a-149">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="75d1a-150">**Abilitato (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="75d1a-150">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="75d1a-151">**Ripetizione (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="75d1a-151">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="75d1a-152">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="75d1a-152">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a><span data-ttu-id="75d1a-153">Esempio</span><span class="sxs-lookup"><span data-stu-id="75d1a-153">Examples</span></span>

<span data-ttu-id="75d1a-154">Il codice XML seguente definisce un trigger inattivo.</span><span class="sxs-lookup"><span data-stu-id="75d1a-154">The following XML defines an idle trigger.</span></span>


```XML
<IdleTrigger>
    <StartBoundary>2005-01-01T00:08:00</StartBoundary>
    <EndBounadry>2007-01-01T00:08:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
</IdleTrigger>
```



## <a name="requirements"></a><span data-ttu-id="75d1a-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75d1a-155">Requirements</span></span>



| <span data-ttu-id="75d1a-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="75d1a-156">Requirement</span></span> | <span data-ttu-id="75d1a-157">Valore</span><span class="sxs-lookup"><span data-stu-id="75d1a-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="75d1a-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75d1a-158">Minimum supported client</span></span><br/> | <span data-ttu-id="75d1a-159">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75d1a-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="75d1a-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75d1a-160">Minimum supported server</span></span><br/> | <span data-ttu-id="75d1a-161">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75d1a-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75d1a-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75d1a-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d1a-163">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="75d1a-163">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="75d1a-164">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="75d1a-164">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

