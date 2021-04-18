---
title: Elemento CalendarTrigger (triggerGroup)
description: Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- trigger del calendario Utilità di pianificazione, elemento XML
- Utilità di pianificazione elemento CalendarTrigger
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02c061d8821dffa82eca8756ab26acadc6bb9281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302006"
---
# <a name="calendartrigger-triggergroup-element"></a><span data-ttu-id="29d51-105">Elemento CalendarTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="29d51-105">CalendarTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="29d51-106">Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="29d51-106">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span>

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

<span data-ttu-id="29d51-107">L'elemento **CalendarTrigger** è definito dal tipo complesso [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="29d51-107">The **CalendarTrigger** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="29d51-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="29d51-108">Parent element</span></span>



| <span data-ttu-id="29d51-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="29d51-109">Element</span></span>                                                           | <span data-ttu-id="29d51-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="29d51-110">Derived from</span></span>                                                         | <span data-ttu-id="29d51-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29d51-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="29d51-112">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="29d51-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="29d51-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="29d51-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="29d51-114">Specifica i trigger che avviano l'attività.</span><span class="sxs-lookup"><span data-stu-id="29d51-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="29d51-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="29d51-115">Child elements</span></span>



| <span data-ttu-id="29d51-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="29d51-116">Element</span></span>                                                                                                                            | <span data-ttu-id="29d51-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="29d51-117">Type</span></span>                                                                                                 | <span data-ttu-id="29d51-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29d51-118">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29d51-119">**Abilitato (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="29d51-119">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | <span data-ttu-id="29d51-120">boolean</span><span class="sxs-lookup"><span data-stu-id="29d51-120">boolean</span></span>                                                                                              | <span data-ttu-id="29d51-121">Specifica che il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="29d51-121">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="29d51-122">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="29d51-122">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | <span data-ttu-id="29d51-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="29d51-123">dateTime</span></span>                                                                                             | <span data-ttu-id="29d51-124">Specifica la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="29d51-124">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="29d51-125">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="29d51-125">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="29d51-126">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="29d51-126">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | <span data-ttu-id="29d51-127">duration</span><span class="sxs-lookup"><span data-stu-id="29d51-127">duration</span></span>                                                                                             | <span data-ttu-id="29d51-128">Specifica l'intervallo di tempo massimo in cui l'attività può essere avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="29d51-128">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="29d51-129">**Ripetizione (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="29d51-129">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [<span data-ttu-id="29d51-130">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="29d51-130">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md)                             | <span data-ttu-id="29d51-131">Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="29d51-131">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="29d51-132">**ScheduleByDay (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="29d51-132">**ScheduleByDay (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="29d51-133">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="29d51-133">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="29d51-134">Specifica una pianificazione giornaliera.</span><span class="sxs-lookup"><span data-stu-id="29d51-134">Specifies a daily schedule.</span></span><br/>                                                                                             |
| [<span data-ttu-id="29d51-135">**ScheduleByMonth (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="29d51-135">**ScheduleByMonth (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="29d51-136">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="29d51-136">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="29d51-137">Specifica una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="29d51-137">Specifies a monthly schedule.</span></span><br/>                                                                                           |
| [<span data-ttu-id="29d51-138">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="29d51-138">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="29d51-139">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="29d51-139">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="29d51-140">Specifica un trigger che avvia un processo in base a una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="29d51-140">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span><br/>                                                |
| [<span data-ttu-id="29d51-141">**ScheduleByWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="29d51-141">**ScheduleByWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="29d51-142">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="29d51-142">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="29d51-143">Specifica una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="29d51-143">Specifies a weekly schedule.</span></span><br/>                                                                                            |
| [<span data-ttu-id="29d51-144">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="29d51-144">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | <span data-ttu-id="29d51-145">dateTime</span><span class="sxs-lookup"><span data-stu-id="29d51-145">dateTime</span></span>                                                                                             | <span data-ttu-id="29d51-146">Specifica la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="29d51-146">Specifies the date and time when the trigger is activated.</span></span> <span data-ttu-id="29d51-147">Questo elemento è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="29d51-147">This element is required.</span></span><br/>                                    |



## <a name="attributes"></a><span data-ttu-id="29d51-148">Attributi</span><span class="sxs-lookup"><span data-stu-id="29d51-148">Attributes</span></span>



| <span data-ttu-id="29d51-149">Nome</span><span class="sxs-lookup"><span data-stu-id="29d51-149">Name</span></span> | <span data-ttu-id="29d51-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="29d51-150">Type</span></span> | <span data-ttu-id="29d51-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29d51-151">Description</span></span>                               |
|------|------|-------------------------------------------|
| <span data-ttu-id="29d51-152">Id</span><span class="sxs-lookup"><span data-stu-id="29d51-152">Id</span></span>   | <span data-ttu-id="29d51-153">ID</span><span class="sxs-lookup"><span data-stu-id="29d51-153">ID</span></span>   | <span data-ttu-id="29d51-154">Identificatore del trigger.</span><span class="sxs-lookup"><span data-stu-id="29d51-154">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="29d51-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="29d51-155">Remarks</span></span>

<span data-ttu-id="29d51-156">L'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) è un elemento obbligatorio per i trigger Time e Calendar ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) e **CalendarTrigger**).</span><span class="sxs-lookup"><span data-stu-id="29d51-156">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) and **CalendarTrigger**).</span></span>

<span data-ttu-id="29d51-157">Gli elementi figlio elencati sopra sono definiti dai tipi di elemento complessi [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) e [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="29d51-157">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex element types.</span></span>

<span data-ttu-id="29d51-158">Per lo sviluppo di script, i trigger Calendar vengono specificati utilizzando uno degli oggetti seguenti.</span><span class="sxs-lookup"><span data-stu-id="29d51-158">For script development, calendar triggers are specified using one of the following objects.</span></span>

-   [<span data-ttu-id="29d51-159">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="29d51-159">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="29d51-160">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="29d51-160">**WeeklyTrigger**</span></span>](weeklytrigger.md)
-   [<span data-ttu-id="29d51-161">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="29d51-161">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="29d51-162">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="29d51-162">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)

<span data-ttu-id="29d51-163">Per lo sviluppo in C++, i trigger Calendar vengono specificati utilizzando una delle interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="29d51-163">For C++ development, calendar triggers are specified using one of the following interfaces.</span></span>

-   [<span data-ttu-id="29d51-164">**IDailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="29d51-164">**IDailyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [<span data-ttu-id="29d51-165">**IWeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="29d51-165">**IWeeklyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [<span data-ttu-id="29d51-166">**IMonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="29d51-166">**IMonthlyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [<span data-ttu-id="29d51-167">**IMonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="29d51-167">**IMonthlyDOWTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a><span data-ttu-id="29d51-168">Esempio</span><span class="sxs-lookup"><span data-stu-id="29d51-168">Examples</span></span>

<span data-ttu-id="29d51-169">Per un esempio completo del codice XML per un'attività che specifica un trigger di calendario, vedere [esempio di trigger giornalieri (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="29d51-169">For a complete example of the XML for a task that specifies a calendar trigger, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29d51-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29d51-170">Requirements</span></span>



| <span data-ttu-id="29d51-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="29d51-171">Requirement</span></span> | <span data-ttu-id="29d51-172">Valore</span><span class="sxs-lookup"><span data-stu-id="29d51-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="29d51-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29d51-173">Minimum supported client</span></span><br/> | <span data-ttu-id="29d51-174">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29d51-174">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="29d51-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29d51-175">Minimum supported server</span></span><br/> | <span data-ttu-id="29d51-176">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="29d51-176">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29d51-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29d51-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d51-178">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="29d51-178">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="29d51-179">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="29d51-179">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





