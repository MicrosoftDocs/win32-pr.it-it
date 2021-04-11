---
title: Gruppo triggerGroup
description: Definisce il gruppo di trigger.
ms.assetid: e07e6999-d982-405b-adfd-2976707b999f
keywords:
- Utilità di pianificazione triggerGroup
topic_type:
- apiref
api_name:
- triggerGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce0203cd9515808891f93223dd7b3ebaf2642103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121546"
---
# <a name="triggergroup-group"></a><span data-ttu-id="b1577-104">Gruppo triggerGroup</span><span class="sxs-lookup"><span data-stu-id="b1577-104">triggerGroup Group</span></span>

<span data-ttu-id="b1577-105">Definisce il gruppo di trigger.</span><span class="sxs-lookup"><span data-stu-id="b1577-105">Defines the trigger group.</span></span>

``` syntax
<xs:group name="triggerGroup">
    <xs:choice>
        <xs:element name="BootTrigger"
            type="bootTriggerType"
            minOccurs="0"
         />
        <xs:element name="RegistrationTrigger"
            type="registrationTriggerType"
            minOccurs="0"
         />
        <xs:element name="IdleTrigger"
            type="idleTriggerType"
            minOccurs="0"
         />
        <xs:element name="TimeTrigger"
            type="timeTriggerType"
            minOccurs="0"
         />
        <xs:element name="EventTrigger"
            type="eventTriggerType"
            minOccurs="0"
         />
        <xs:element name="LogonTrigger"
            type="logonTriggerType"
            minOccurs="0"
         />
        <xs:element name="SessionStateChangeTrigger"
            type="sessionStateChangeTriggerType"
            minOccurs="0"
         />
        <xs:element name="CalendarTrigger"
            type="calendarTriggerType"
            minOccurs="0"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="b1577-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b1577-106">Child elements</span></span>



| <span data-ttu-id="b1577-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="b1577-107">Element</span></span>                                                                                                 | <span data-ttu-id="b1577-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1577-108">Type</span></span>                                                                                                   | <span data-ttu-id="b1577-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1577-109">Description</span></span>                                                                                                       |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1577-110">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="b1577-110">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                             | [<span data-ttu-id="b1577-111">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b1577-111">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                             | <span data-ttu-id="b1577-112">Trigger che avvia un'attività quando viene avviato il sistema.</span><span class="sxs-lookup"><span data-stu-id="b1577-112">A trigger that starts a task when the system is booted.</span></span><br/>                                                |
| [<span data-ttu-id="b1577-113">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="b1577-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)                     | [<span data-ttu-id="b1577-114">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b1577-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)                     | <span data-ttu-id="b1577-115">Trigger che avvia un'attività in base a una pianificazione giornaliera, settimanale, mensile o mensile del giorno della settimana (DOW).</span><span class="sxs-lookup"><span data-stu-id="b1577-115">A trigger that starts a task based on a daily, weekly, monthly, or monthly day-of-week (DOW) schedule.</span></span><br/> |
| [<span data-ttu-id="b1577-116">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="b1577-116">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)                           | [<span data-ttu-id="b1577-117">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b1577-117">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)                           | <span data-ttu-id="b1577-118">Trigger che avvia un'attività quando si verifica un evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="b1577-118">A trigger that starts a task when a system event occurs.</span></span><br/>                                               |
| [<span data-ttu-id="b1577-119">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="b1577-119">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                             | [<span data-ttu-id="b1577-120">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b1577-120">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                             | <span data-ttu-id="b1577-121">Trigger che avvia un'attività quando il computer entra in uno stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="b1577-121">A trigger that starts a task when the computer goes into an idle state.</span></span><br/>                                |
| [<span data-ttu-id="b1577-122">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="b1577-122">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)                           | [<span data-ttu-id="b1577-123">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b1577-123">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)                           | <span data-ttu-id="b1577-124">Trigger che avvia un'attività quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="b1577-124">A trigger that starts a task when a user logs on.</span></span><br/>                                                      |
| [<span data-ttu-id="b1577-125">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="b1577-125">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md)             | [<span data-ttu-id="b1577-126">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b1577-126">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)             | <span data-ttu-id="b1577-127">Trigger che avvia un'attività quando l'attività viene registrata.</span><span class="sxs-lookup"><span data-stu-id="b1577-127">A trigger that starts a task when the task is registered.</span></span><br/>                                              |
| [<span data-ttu-id="b1577-128">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="b1577-128">**SessionStateChangeTrigger**</span></span>](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) | [<span data-ttu-id="b1577-129">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b1577-129">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="b1577-130">Trigger che avvia un'attività quando una sessione di Terminal Server modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="b1577-130">A trigger that starts a task when a Terminal Server session changes state.</span></span><br/>                             |
| [<span data-ttu-id="b1577-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="b1577-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                             | [<span data-ttu-id="b1577-132">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b1577-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                             | <span data-ttu-id="b1577-133">Trigger che avvia un'attività quando viene attivato il trigger.</span><span class="sxs-lookup"><span data-stu-id="b1577-133">A trigger that starts a task when the trigger is activated.</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="b1577-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1577-134">Remarks</span></span>

<span data-ttu-id="b1577-135">Durante la lettura o la scrittura di codice XML, gli elementi definiti da questo gruppo sono gli elementi figlio dell'elemento [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b1577-135">When reading or writing XML, the elements that are defined by this group are the child elements of the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1577-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1577-136">Requirements</span></span>



| <span data-ttu-id="b1577-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1577-137">Requirement</span></span> | <span data-ttu-id="b1577-138">Valore</span><span class="sxs-lookup"><span data-stu-id="b1577-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b1577-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1577-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b1577-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1577-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b1577-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1577-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b1577-142">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b1577-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1577-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1577-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1577-144">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="b1577-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





