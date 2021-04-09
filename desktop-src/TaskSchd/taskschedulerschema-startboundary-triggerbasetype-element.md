---
title: Elemento StartBoundary (triggerBaseType)
description: Specifica la data e l'ora di attivazione del trigger.
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- Utilità di pianificazione elemento StartBoundary
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d6adf90de2f3b199f98737996fe732f342787b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119287"
---
# <a name="startboundary-triggerbasetype-element"></a><span data-ttu-id="73069-104">Elemento StartBoundary (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="73069-104">StartBoundary (triggerBaseType) Element</span></span>

<span data-ttu-id="73069-105">Specifica la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="73069-105">Specifies the date and time when the trigger is activated.</span></span>

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

<span data-ttu-id="73069-106">L'elemento **StartBoundary** è definito dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="73069-106">The **StartBoundary** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="73069-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="73069-107">Parent element</span></span>



| <span data-ttu-id="73069-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="73069-108">Element</span></span>                                                                                     | <span data-ttu-id="73069-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="73069-109">Derived from</span></span>                                                                               | <span data-ttu-id="73069-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73069-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73069-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="73069-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="73069-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="73069-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="73069-113">Specifica un trigger che avvia un'attività quando viene avviato il sistema.</span><span class="sxs-lookup"><span data-stu-id="73069-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="73069-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="73069-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="73069-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="73069-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="73069-116">Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="73069-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="73069-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="73069-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="73069-118">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="73069-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="73069-119">Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="73069-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="73069-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="73069-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="73069-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="73069-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="73069-122">Specifica un trigger che avvia un'attività quando il computer entra in uno stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="73069-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="73069-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="73069-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="73069-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="73069-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="73069-125">Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="73069-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="73069-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="73069-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="73069-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="73069-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="73069-128">Specifica un trigger che avvia un'attività quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="73069-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="73069-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="73069-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="73069-130">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="73069-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="73069-131">Specifica un trigger che avvia un'attività quando viene attivato il trigger.</span><span class="sxs-lookup"><span data-stu-id="73069-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="73069-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="73069-132">Remarks</span></span>

<span data-ttu-id="73069-133">L' **<StartBoundary>** elemento è un elemento obbligatorio per i trigger Time e Calendar ( [**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) e [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md) ).</span><span class="sxs-lookup"><span data-stu-id="73069-133">The **<StartBoundary>** element is a required element for time and calendar triggers ([**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) and [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="73069-134">Per lo sviluppo di script, il limite finale viene specificato utilizzando la proprietà [**trigger. StartBoundary**](trigger-startboundary.md) ereditata dagli oggetti trigger all.</span><span class="sxs-lookup"><span data-stu-id="73069-134">For scripting development, the end boundary is specified using the [**Trigger.StartBoundary**](trigger-startboundary.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="73069-135">Per lo sviluppo in C++, il limite finale viene specificato usando la proprietà [**ITrigger:: StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) ereditata dalle interfacce di trigger all.</span><span class="sxs-lookup"><span data-stu-id="73069-135">For C++ development, the end boundary is specified using the [**ITrigger::StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) property that is inherited by the all trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="73069-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="73069-136">Examples</span></span>

<span data-ttu-id="73069-137">Il codice XML seguente definisce un elemento trigger di avvio che definisce un limite iniziale del 1 gennaio 2005:8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="73069-137">The following XML defines a boot trigger element that defines a start boundary of January 1, 2005: 8:00 AM.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="73069-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73069-138">Requirements</span></span>



| <span data-ttu-id="73069-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="73069-139">Requirement</span></span> | <span data-ttu-id="73069-140">Valore</span><span class="sxs-lookup"><span data-stu-id="73069-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="73069-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73069-141">Minimum supported client</span></span><br/> | <span data-ttu-id="73069-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73069-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="73069-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73069-143">Minimum supported server</span></span><br/> | <span data-ttu-id="73069-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="73069-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73069-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73069-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73069-146">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="73069-146">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="73069-147">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="73069-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





