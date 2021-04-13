---
title: Elemento TimeTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando viene attivato il trigger.
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- Utilità di pianificazione elemento TimeTrigger
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83d3b0a63a8be70af7eba4edb90e49db71892f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478161"
---
# <a name="timetrigger-triggergroup-element"></a><span data-ttu-id="46be1-104">Elemento TimeTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="46be1-104">TimeTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="46be1-105">Specifica un trigger che avvia un'attività quando viene attivato il trigger.</span><span class="sxs-lookup"><span data-stu-id="46be1-105">Specifies a trigger that starts a task when the trigger is activated.</span></span>

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

<span data-ttu-id="46be1-106">L'elemento **TimeTrigger** è definito da [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="46be1-106">The **TimeTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="46be1-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="46be1-107">Parent element</span></span>



| <span data-ttu-id="46be1-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="46be1-108">Element</span></span>                                                           | <span data-ttu-id="46be1-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="46be1-109">Derived from</span></span>                                                         | <span data-ttu-id="46be1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46be1-110">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="46be1-111">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="46be1-111">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="46be1-112">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="46be1-112">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="46be1-113">Specifica i trigger che avviano l'attività.</span><span class="sxs-lookup"><span data-stu-id="46be1-113">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="46be1-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="46be1-114">Child elements</span></span>



| <span data-ttu-id="46be1-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="46be1-115">Element</span></span>                                                                                                        | <span data-ttu-id="46be1-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="46be1-116">Type</span></span>                                                                     | <span data-ttu-id="46be1-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46be1-117">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46be1-118">**Abilitato (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="46be1-118">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="46be1-119">boolean</span><span class="sxs-lookup"><span data-stu-id="46be1-119">boolean</span></span>                                                                  | <span data-ttu-id="46be1-120">Specifica che il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="46be1-120">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="46be1-121">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="46be1-121">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="46be1-122">dateTime</span><span class="sxs-lookup"><span data-stu-id="46be1-122">dateTime</span></span>                                                                 | <span data-ttu-id="46be1-123">Specifica la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="46be1-123">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="46be1-124">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="46be1-124">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="46be1-125">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="46be1-125">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="46be1-126">duration</span><span class="sxs-lookup"><span data-stu-id="46be1-126">duration</span></span>                                                                 | <span data-ttu-id="46be1-127">Specifica l'intervallo di tempo massimo in cui l'attività può essere avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="46be1-127">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="46be1-128">**Ripetizione (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="46be1-128">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="46be1-129">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="46be1-129">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="46be1-130">Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="46be1-130">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="46be1-131">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="46be1-131">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="46be1-132">dateTime</span><span class="sxs-lookup"><span data-stu-id="46be1-132">dateTime</span></span>                                                                 | <span data-ttu-id="46be1-133">Specifica la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="46be1-133">Specifies the date and time when the trigger is activated.</span></span> <span data-ttu-id="46be1-134">Questo elemento è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="46be1-134">This element is required.</span></span><br/>                                    |



## <a name="attributes"></a><span data-ttu-id="46be1-135">Attributi</span><span class="sxs-lookup"><span data-stu-id="46be1-135">Attributes</span></span>



| <span data-ttu-id="46be1-136">Nome</span><span class="sxs-lookup"><span data-stu-id="46be1-136">Name</span></span> | <span data-ttu-id="46be1-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="46be1-137">Type</span></span>       | <span data-ttu-id="46be1-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46be1-138">Description</span></span>                               |
|------|------------|-------------------------------------------|
| <span data-ttu-id="46be1-139">Id</span><span class="sxs-lookup"><span data-stu-id="46be1-139">Id</span></span>   | <span data-ttu-id="46be1-140">**string**</span><span class="sxs-lookup"><span data-stu-id="46be1-140">**string**</span></span> | <span data-ttu-id="46be1-141">Identificatore del trigger.</span><span class="sxs-lookup"><span data-stu-id="46be1-141">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="46be1-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="46be1-142">Remarks</span></span>

<span data-ttu-id="46be1-143">L'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) è un elemento obbligatorio per i trigger Time e Calendar (**TimeTrigger** e [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span><span class="sxs-lookup"><span data-stu-id="46be1-143">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers (**TimeTrigger** and [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="46be1-144">Per lo sviluppo di script, viene specificato un trigger time utilizzando l'oggetto [**TimeTrigger**](timetrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="46be1-144">For scripting development, a time trigger is specified using the [**TimeTrigger**](timetrigger.md) object.</span></span>

<span data-ttu-id="46be1-145">Per lo sviluppo in C++, viene specificato un trigger Time usando l'interfaccia [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) .</span><span class="sxs-lookup"><span data-stu-id="46be1-145">For C++ development, a time trigger is specified using the [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) interface.</span></span>

<span data-ttu-id="46be1-146">Gli elementi figlio elencati sopra sono definiti dai tipi di elemento complessi [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="46be1-146">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span> <span data-ttu-id="46be1-147">Questi elementi devono essere aggiunti nella sequenza illustrata di seguito.</span><span class="sxs-lookup"><span data-stu-id="46be1-147">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="46be1-148">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="46be1-148">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="46be1-149">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="46be1-149">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="46be1-150">**Abilitato (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="46be1-150">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="46be1-151">**Ripetizione (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="46be1-151">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="46be1-152">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="46be1-152">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a><span data-ttu-id="46be1-153">Esempio</span><span class="sxs-lookup"><span data-stu-id="46be1-153">Examples</span></span>

<span data-ttu-id="46be1-154">Per un esempio completo del codice XML per un'attività che specifica un trigger di ora, vedere [esempio di trigger di ora (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="46be1-154">For a complete example of the XML for a task that specifies a time trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46be1-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46be1-155">Requirements</span></span>



| <span data-ttu-id="46be1-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="46be1-156">Requirement</span></span> | <span data-ttu-id="46be1-157">Valore</span><span class="sxs-lookup"><span data-stu-id="46be1-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46be1-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46be1-158">Minimum supported client</span></span><br/> | <span data-ttu-id="46be1-159">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46be1-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="46be1-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46be1-160">Minimum supported server</span></span><br/> | <span data-ttu-id="46be1-161">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46be1-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46be1-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46be1-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46be1-163">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="46be1-163">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





