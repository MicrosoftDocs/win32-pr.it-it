---
title: Triggers (taskType)-elemento
description: Specifica i trigger che avviano l'attività.
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- Triggers Utilità di pianificazione elemento
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06994c395fbfbc5b0c6244c9d17930bc4afac885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743754"
---
# <a name="triggers-tasktype-element"></a><span data-ttu-id="1af71-104">Triggers (taskType)-elemento</span><span class="sxs-lookup"><span data-stu-id="1af71-104">Triggers (taskType) Element</span></span>

<span data-ttu-id="1af71-105">Specifica i trigger che avviano l'attività.</span><span class="sxs-lookup"><span data-stu-id="1af71-105">Specifies the triggers that start the task.</span></span>

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

<span data-ttu-id="1af71-106">L'elemento **Triggers** è definito dal tipo complesso [**triggersType**](taskschedulerschema-triggerstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1af71-106">The **Triggers** element is defined by the [**triggersType**](taskschedulerschema-triggerstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1af71-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1af71-107">Parent element</span></span>



| <span data-ttu-id="1af71-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="1af71-108">Element</span></span>                                          | <span data-ttu-id="1af71-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="1af71-109">Derived from</span></span>                                                 | <span data-ttu-id="1af71-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1af71-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="1af71-111">**Attività**</span><span class="sxs-lookup"><span data-stu-id="1af71-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="1af71-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="1af71-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="1af71-113">Definisce l'attività eseguita dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1af71-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="1af71-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1af71-114">Child elements</span></span>



| <span data-ttu-id="1af71-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="1af71-115">Element</span></span>                                                                                     | <span data-ttu-id="1af71-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="1af71-116">Type</span></span>                                                                                       | <span data-ttu-id="1af71-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1af71-117">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1af71-118">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="1af71-118">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="1af71-119">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1af71-119">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="1af71-120">Specifica un trigger che avvia un'attività quando viene avviato il sistema.</span><span class="sxs-lookup"><span data-stu-id="1af71-120">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="1af71-121">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="1af71-121">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="1af71-122">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1af71-122">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="1af71-123">Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="1af71-123">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="1af71-124">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="1af71-124">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="1af71-125">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1af71-125">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="1af71-126">Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="1af71-126">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="1af71-127">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="1af71-127">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="1af71-128">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1af71-128">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="1af71-129">Specifica un trigger che avvia un'attività quando il computer entra in uno stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="1af71-129">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="1af71-130">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="1af71-130">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="1af71-131">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1af71-131">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="1af71-132">Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="1af71-132">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="1af71-133">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="1af71-133">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="1af71-134">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1af71-134">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="1af71-135">Specifica un trigger che avvia un'attività quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="1af71-135">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="1af71-136">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="1af71-136">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="1af71-137">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1af71-137">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="1af71-138">Specifica un trigger che avvia un'attività quando viene attivato il trigger.</span><span class="sxs-lookup"><span data-stu-id="1af71-138">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="1af71-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="1af71-139">Remarks</span></span>

<span data-ttu-id="1af71-140">Gli elementi figlio elencati sopra possono essere aggiunti in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="1af71-140">The child elements listed above can be added in any order.</span></span>

<span data-ttu-id="1af71-141">Per lo sviluppo in C++, i trigger di un'attività vengono specificati utilizzando la [**Proprietà Triggers di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).</span><span class="sxs-lookup"><span data-stu-id="1af71-141">For C++ development, the triggers of a task are specified using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).</span></span>

<span data-ttu-id="1af71-142">Per lo sviluppo di script, i trigger di un'attività vengono specificati utilizzando la proprietà [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="1af71-142">For scripting development, the triggers of a task are specified using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="1af71-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="1af71-143">Examples</span></span>

<span data-ttu-id="1af71-144">Per un esempio completo del codice XML per un'attività che specifica un trigger, vedere [esempio di trigger di ora (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="1af71-144">For a complete example of the XML for a task that specifies a trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1af71-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1af71-145">Requirements</span></span>



| <span data-ttu-id="1af71-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="1af71-146">Requirement</span></span> | <span data-ttu-id="1af71-147">Valore</span><span class="sxs-lookup"><span data-stu-id="1af71-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1af71-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1af71-148">Minimum supported client</span></span><br/> | <span data-ttu-id="1af71-149">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1af71-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1af71-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1af71-150">Minimum supported server</span></span><br/> | <span data-ttu-id="1af71-151">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1af71-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1af71-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1af71-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af71-153">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="1af71-153">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1af71-154">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="1af71-154">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





