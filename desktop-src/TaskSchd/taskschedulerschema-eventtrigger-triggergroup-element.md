---
title: Elemento EventTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- Utilità di pianificazione trigger evento, elemento
- Elemento EventTrigger Utilità di pianificazione
topic_type:
- apiref
api_name:
- EventTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3cecf46250fface0f716adbf287cda3269b86f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478179"
---
# <a name="eventtrigger-triggergroup-element"></a><span data-ttu-id="553a5-105">Elemento EventTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="553a5-105">EventTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="553a5-106">Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="553a5-106">Specifies a trigger that starts a task when a system event occurs.</span></span>

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

<span data-ttu-id="553a5-107">L'elemento **EventTrigger** è definito da [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="553a5-107">The **EventTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="553a5-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="553a5-108">Parent element</span></span>



| <span data-ttu-id="553a5-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="553a5-109">Element</span></span>                                                           | <span data-ttu-id="553a5-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="553a5-110">Derived from</span></span>                                                         | <span data-ttu-id="553a5-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="553a5-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="553a5-112">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="553a5-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="553a5-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="553a5-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="553a5-114">Specifica i trigger che avviano l'attività.</span><span class="sxs-lookup"><span data-stu-id="553a5-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="553a5-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="553a5-115">Child elements</span></span>



| <span data-ttu-id="553a5-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="553a5-116">Element</span></span>                                                                                              | <span data-ttu-id="553a5-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="553a5-117">Type</span></span>                                                                     | <span data-ttu-id="553a5-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="553a5-118">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="553a5-119">**Ritardo (eventTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="553a5-119">**Delay (eventTriggerType)**</span></span>](taskschedulerschema-delay-eventtriggertype-element.md)               | <span data-ttu-id="553a5-120">duration</span><span class="sxs-lookup"><span data-stu-id="553a5-120">duration</span></span>                                                                 | <span data-ttu-id="553a5-121">Specifica la quantità di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="553a5-121">Specifies the amount of time between when the event occurs and when the task is started.</span></span><br/>                                |
| [<span data-ttu-id="553a5-122">**Abilitato (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="553a5-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)             | <span data-ttu-id="553a5-123">boolean</span><span class="sxs-lookup"><span data-stu-id="553a5-123">boolean</span></span>                                                                  | <span data-ttu-id="553a5-124">Specifica che il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="553a5-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="553a5-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="553a5-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)     | <span data-ttu-id="553a5-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="553a5-126">dateTime</span></span>                                                                 | <span data-ttu-id="553a5-127">Specifica la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="553a5-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="553a5-128">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="553a5-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="553a5-129">**Ripetizione (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="553a5-129">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)       | [<span data-ttu-id="553a5-130">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="553a5-130">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="553a5-131">Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="553a5-131">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="553a5-132">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="553a5-132">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md) | <span data-ttu-id="553a5-133">dateTime</span><span class="sxs-lookup"><span data-stu-id="553a5-133">dateTime</span></span>                                                                 | <span data-ttu-id="553a5-134">Specifica la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="553a5-134">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="553a5-135">**Sottoscrizione (eventTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="553a5-135">**Subscription (eventTriggerType)**</span></span>](taskschedulerschema-subscription-eventtriggertype-element.md) | <span data-ttu-id="553a5-136">string</span><span class="sxs-lookup"><span data-stu-id="553a5-136">string</span></span>                                                                   | <span data-ttu-id="553a5-137">Specifica la query XPath che identifica l'evento che attiva il trigger.</span><span class="sxs-lookup"><span data-stu-id="553a5-137">Specifies the XPath query that identifies the event that fires the trigger.</span></span><br/>                                             |



## <a name="attributes"></a><span data-ttu-id="553a5-138">Attributi</span><span class="sxs-lookup"><span data-stu-id="553a5-138">Attributes</span></span>



| <span data-ttu-id="553a5-139">Nome</span><span class="sxs-lookup"><span data-stu-id="553a5-139">Name</span></span> | <span data-ttu-id="553a5-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="553a5-140">Type</span></span> | <span data-ttu-id="553a5-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="553a5-141">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="553a5-142">Id</span><span class="sxs-lookup"><span data-stu-id="553a5-142">Id</span></span>   | <span data-ttu-id="553a5-143">ID</span><span class="sxs-lookup"><span data-stu-id="553a5-143">ID</span></span>   | <span data-ttu-id="553a5-144">Identificatore del trigger.</span><span class="sxs-lookup"><span data-stu-id="553a5-144">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="553a5-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="553a5-145">Remarks</span></span>

<span data-ttu-id="553a5-146">È possibile creare un massimo di 500 attività con sottoscrizioni di eventi.</span><span class="sxs-lookup"><span data-stu-id="553a5-146">A maximum of 500 tasks with event subscriptions can be created.</span></span> <span data-ttu-id="553a5-147">Una sottoscrizione di eventi che esegue query per una varietà di eventi può essere usata per attivare un'attività che usa la stessa azione in risposta agli eventi che vengono registrati.</span><span class="sxs-lookup"><span data-stu-id="553a5-147">An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.</span></span>

<span data-ttu-id="553a5-148">Per lo sviluppo di script, un trigger di evento viene definito dall'oggetto [**EventTrigger**](eventtrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="553a5-148">For script development, an event trigger is defined by the [**EventTrigger**](eventtrigger.md) object.</span></span>

<span data-ttu-id="553a5-149">Per lo sviluppo in C++, un trigger di evento viene definito dall'interfaccia [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) .</span><span class="sxs-lookup"><span data-stu-id="553a5-149">For C++ development, an event trigger is defined by the [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="553a5-150">Esempio</span><span class="sxs-lookup"><span data-stu-id="553a5-150">Examples</span></span>

<span data-ttu-id="553a5-151">Per un esempio completo del codice XML per un'attività che usa un trigger di evento, vedere [esempio di trigger di evento (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="553a5-151">For a complete example of the XML for a task that uses an event trigger, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="553a5-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="553a5-152">Requirements</span></span>



| <span data-ttu-id="553a5-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="553a5-153">Requirement</span></span> | <span data-ttu-id="553a5-154">Valore</span><span class="sxs-lookup"><span data-stu-id="553a5-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="553a5-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="553a5-155">Minimum supported client</span></span><br/> | <span data-ttu-id="553a5-156">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="553a5-156">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="553a5-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="553a5-157">Minimum supported server</span></span><br/> | <span data-ttu-id="553a5-158">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="553a5-158">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="553a5-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="553a5-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="553a5-160">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="553a5-160">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

