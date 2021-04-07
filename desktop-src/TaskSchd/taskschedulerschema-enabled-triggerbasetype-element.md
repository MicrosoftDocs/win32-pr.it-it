---
title: Elemento Enabled (triggerBaseType)
description: Specifica che il trigger è abilitato.
ms.assetid: 14c98f40-0ec5-4dc1-978e-b02c08ee2384
keywords:
- Elemento Enabled Utilità di pianificazione
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42b495ba1af5f3b9b99034b0d6ca9d02040460c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048757"
---
# <a name="enabled-triggerbasetype-element"></a><span data-ttu-id="dddaa-104">Elemento Enabled (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="dddaa-104">Enabled (triggerBaseType) Element</span></span>

<span data-ttu-id="dddaa-105">Specifica che il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="dddaa-105">Specifies that the trigger is enabled.</span></span>

``` syntax
<xs:element name="Enabled"
    type="boolean"
 />
```

<span data-ttu-id="dddaa-106">L'elemento **Enabled** è definito dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="dddaa-106">The **Enabled** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="dddaa-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="dddaa-107">Parent element</span></span>



| <span data-ttu-id="dddaa-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="dddaa-108">Element</span></span>                                                                                     | <span data-ttu-id="dddaa-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="dddaa-109">Derived from</span></span>                                                                               | <span data-ttu-id="dddaa-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dddaa-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dddaa-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="dddaa-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="dddaa-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="dddaa-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="dddaa-113">Specifica un trigger che avvia un'attività quando viene avviato il sistema.</span><span class="sxs-lookup"><span data-stu-id="dddaa-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="dddaa-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="dddaa-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="dddaa-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="dddaa-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="dddaa-116">Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="dddaa-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="dddaa-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="dddaa-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="dddaa-118">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="dddaa-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="dddaa-119">Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="dddaa-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="dddaa-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="dddaa-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="dddaa-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="dddaa-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="dddaa-122">Specifica un trigger che avvia un'attività quando il computer entra in uno stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="dddaa-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="dddaa-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="dddaa-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="dddaa-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="dddaa-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="dddaa-125">Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="dddaa-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="dddaa-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="dddaa-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="dddaa-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="dddaa-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="dddaa-128">Specifica un trigger che avvia un'attività quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="dddaa-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="dddaa-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="dddaa-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="dddaa-130">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="dddaa-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="dddaa-131">Specifica un trigger che avvia un'attività quando viene attivato il trigger.</span><span class="sxs-lookup"><span data-stu-id="dddaa-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="dddaa-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="dddaa-132">Remarks</span></span>

<span data-ttu-id="dddaa-133">Per lo sviluppo di script, è possibile accedere a queste informazioni tramite la proprietà [**trigger. Enabled**](trigger-enabled.md) ereditata dagli oggetti trigger all.</span><span class="sxs-lookup"><span data-stu-id="dddaa-133">For scripting development, this information is accessed through the [**Trigger.Enabled**](trigger-enabled.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="dddaa-134">Per lo sviluppo in C++, queste informazioni sono accessibili tramite la proprietà [**ITrigger:: Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) ereditata dalle interfacce di trigger all.</span><span class="sxs-lookup"><span data-stu-id="dddaa-134">For C++ development, this information is accessed through the [**ITrigger::Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) property that is inherited by the all trigger interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="dddaa-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dddaa-135">Requirements</span></span>



| <span data-ttu-id="dddaa-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="dddaa-136">Requirement</span></span> | <span data-ttu-id="dddaa-137">Valore</span><span class="sxs-lookup"><span data-stu-id="dddaa-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dddaa-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dddaa-138">Minimum supported client</span></span><br/> | <span data-ttu-id="dddaa-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dddaa-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dddaa-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dddaa-140">Minimum supported server</span></span><br/> | <span data-ttu-id="dddaa-141">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dddaa-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dddaa-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dddaa-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dddaa-143">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="dddaa-143">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="dddaa-144">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="dddaa-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





