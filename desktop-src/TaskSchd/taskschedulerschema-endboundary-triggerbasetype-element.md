---
title: Elemento EndBoundary (triggerBaseType)
description: Specifica la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.
ms.assetid: 84731c0b-3fb8-44dd-be1a-67547add1f9e
keywords:
- Utilità di pianificazione elemento EndBoundary
topic_type:
- apiref
api_name:
- EndBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d687655498301595c1ab888fcc179ec0694f0aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301153"
---
# <a name="endboundary-triggerbasetype-element"></a><span data-ttu-id="02c2f-105">Elemento EndBoundary (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="02c2f-105">EndBoundary (triggerBaseType) Element</span></span>

<span data-ttu-id="02c2f-106">Specifica la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="02c2f-106">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="02c2f-107">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="02c2f-107">The trigger cannot start the task after it is deactivated.</span></span>

``` syntax
<xs:element name="EndBoundary"
    type="dateTime"
 />
```

<span data-ttu-id="02c2f-108">L'elemento **EndBoundary** è definito dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="02c2f-108">The **EndBoundary** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="02c2f-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="02c2f-109">Parent element</span></span>



| <span data-ttu-id="02c2f-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="02c2f-110">Element</span></span>                                                                                     | <span data-ttu-id="02c2f-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="02c2f-111">Derived from</span></span>                                                                               | <span data-ttu-id="02c2f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02c2f-112">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02c2f-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="02c2f-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="02c2f-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="02c2f-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="02c2f-115">Specifica un trigger che avvia un'attività quando viene avviato il sistema.</span><span class="sxs-lookup"><span data-stu-id="02c2f-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="02c2f-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="02c2f-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="02c2f-117">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="02c2f-117">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="02c2f-118">Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="02c2f-118">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="02c2f-119">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="02c2f-119">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="02c2f-120">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="02c2f-120">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="02c2f-121">Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="02c2f-121">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="02c2f-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="02c2f-122">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="02c2f-123">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="02c2f-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="02c2f-124">Specifica un trigger che avvia un'attività quando il computer entra in uno stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="02c2f-124">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="02c2f-125">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="02c2f-125">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="02c2f-126">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="02c2f-126">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="02c2f-127">Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="02c2f-127">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="02c2f-128">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="02c2f-128">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="02c2f-129">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="02c2f-129">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="02c2f-130">Specifica un trigger che avvia un'attività quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="02c2f-130">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="02c2f-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="02c2f-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="02c2f-132">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="02c2f-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="02c2f-133">Specifica un trigger che avvia un'attività quando viene attivato il trigger.</span><span class="sxs-lookup"><span data-stu-id="02c2f-133">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="02c2f-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="02c2f-134">Remarks</span></span>

<span data-ttu-id="02c2f-135">Per lo sviluppo di script, il limite finale viene specificato utilizzando la proprietà [**trigger. EndBoundary**](trigger-endboundary.md) ereditata dagli oggetti trigger all.</span><span class="sxs-lookup"><span data-stu-id="02c2f-135">For scripting development, the end boundary is specified using the [**Trigger.EndBoundary**](trigger-endboundary.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="02c2f-136">Per lo sviluppo in C++, il limite finale viene specificato usando la proprietà [**ITrigger:: EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) ereditata dalle interfacce di trigger all.</span><span class="sxs-lookup"><span data-stu-id="02c2f-136">For C++ development, the end boundary is specified using the [**ITrigger::EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) property that is inherited by the all trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="02c2f-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="02c2f-137">Examples</span></span>

<span data-ttu-id="02c2f-138">Il codice XML seguente definisce un elemento trigger di avvio che definisce un limite finale del 1 gennaio 2007:8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="02c2f-138">The following XML defines a boot trigger element that defines an end boundary of January 1, 2007: 8:00 AM.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="02c2f-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02c2f-139">Requirements</span></span>



| <span data-ttu-id="02c2f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="02c2f-140">Requirement</span></span> | <span data-ttu-id="02c2f-141">Valore</span><span class="sxs-lookup"><span data-stu-id="02c2f-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="02c2f-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02c2f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="02c2f-143">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="02c2f-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="02c2f-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02c2f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="02c2f-145">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="02c2f-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02c2f-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02c2f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c2f-147">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="02c2f-147">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="02c2f-148">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="02c2f-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





