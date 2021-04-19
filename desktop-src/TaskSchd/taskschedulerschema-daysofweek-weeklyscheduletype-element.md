---
title: Elemento DaysOfWeek (weeklyScheduleType)
description: Specifica i giorni della settimana in cui viene eseguita l'attività. | Elemento DaysOfWeek (weeklyScheduleType)
ms.assetid: 86555681-2324-4095-9eab-fdef40e0acba
keywords:
- Utilità di pianificazione elemento DaysOfWeek
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a2b310feb49f3141d1f7f08c4552305f9ffc3ea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321844"
---
# <a name="daysofweek-weeklyscheduletype-element"></a><span data-ttu-id="523bd-105">Elemento DaysOfWeek (weeklyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="523bd-105">DaysOfWeek (weeklyScheduleType) Element</span></span>

<span data-ttu-id="523bd-106">Specifica i giorni della settimana in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="523bd-106">Specifies the days of the week in which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

<span data-ttu-id="523bd-107">L'elemento **DaysOfWeek** è definito dal tipo complesso [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="523bd-107">The **DaysOfWeek** element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="523bd-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="523bd-108">Parent element</span></span>



| <span data-ttu-id="523bd-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="523bd-109">Element</span></span>                                                                                  | <span data-ttu-id="523bd-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="523bd-110">Derived from</span></span>                                                                     | <span data-ttu-id="523bd-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="523bd-111">Description</span></span>                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="523bd-112">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="523bd-112">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [<span data-ttu-id="523bd-113">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="523bd-113">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md) | <span data-ttu-id="523bd-114">Specifica una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="523bd-114">Specifies a weekly schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="523bd-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="523bd-115">Child elements</span></span>



| <span data-ttu-id="523bd-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="523bd-116">Element</span></span>                                                                   | <span data-ttu-id="523bd-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="523bd-117">Type</span></span> | <span data-ttu-id="523bd-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="523bd-118">Description</span></span>                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="523bd-119">**Friday**</span><span class="sxs-lookup"><span data-stu-id="523bd-119">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       |      | <span data-ttu-id="523bd-120">Specifica che l'attività viene eseguita il venerdì.</span><span class="sxs-lookup"><span data-stu-id="523bd-120">Specifies that the task runs on Friday.</span></span><br/>    |
| [<span data-ttu-id="523bd-121">**Monday**</span><span class="sxs-lookup"><span data-stu-id="523bd-121">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       |      | <span data-ttu-id="523bd-122">Specifica che l'attività viene eseguita il lunedì.</span><span class="sxs-lookup"><span data-stu-id="523bd-122">Specifies that the task runs on Monday.</span></span><br/>    |
| [<span data-ttu-id="523bd-123">**Sabato**</span><span class="sxs-lookup"><span data-stu-id="523bd-123">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   |      | <span data-ttu-id="523bd-124">Specifica che l'attività viene eseguita il sabato.</span><span class="sxs-lookup"><span data-stu-id="523bd-124">Specifies that the task runs on Saturday.</span></span><br/>  |
| [<span data-ttu-id="523bd-125">**Sunday**</span><span class="sxs-lookup"><span data-stu-id="523bd-125">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       |      | <span data-ttu-id="523bd-126">Specifica che l'attività viene eseguita la domenica.</span><span class="sxs-lookup"><span data-stu-id="523bd-126">Specifies that the task runs on Sunday.</span></span><br/>    |
| [<span data-ttu-id="523bd-127">**Thursday**</span><span class="sxs-lookup"><span data-stu-id="523bd-127">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   |      | <span data-ttu-id="523bd-128">Specifica che l'attività viene eseguita il giovedì.</span><span class="sxs-lookup"><span data-stu-id="523bd-128">Specifies that the task runs on Thursday.</span></span><br/>  |
| [<span data-ttu-id="523bd-129">**Tuesday**</span><span class="sxs-lookup"><span data-stu-id="523bd-129">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | <span data-ttu-id="523bd-130">Specifica che l'attività viene eseguita il martedì.</span><span class="sxs-lookup"><span data-stu-id="523bd-130">Specifies that the task runs on Tuesday.</span></span><br/>   |
| [<span data-ttu-id="523bd-131">**Wednesday**</span><span class="sxs-lookup"><span data-stu-id="523bd-131">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) |      | <span data-ttu-id="523bd-132">Specifica che l'attività viene eseguita il mercoledì.</span><span class="sxs-lookup"><span data-stu-id="523bd-132">Specifies that the task runs on Wednesday.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="523bd-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="523bd-133">Remarks</span></span>

<span data-ttu-id="523bd-134">Gli elementi figlio precedenti sono definiti dal tipo complesso [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="523bd-134">The previous child elements are defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

<span data-ttu-id="523bd-135">Per lo sviluppo di script, l'intervallo settimanale viene specificato tramite la proprietà [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="523bd-135">For scripting development, the weekly interval is specified using the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md) property.</span></span>

<span data-ttu-id="523bd-136">Per lo sviluppo in C++, l'intervallo settimanale viene specificato con la proprietà [**IWeeklyTrigger:: WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .</span><span class="sxs-lookup"><span data-stu-id="523bd-136">For C++ development, the weekly interval is specified using the [**IWeeklyTrigger::WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="523bd-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="523bd-137">Examples</span></span>

<span data-ttu-id="523bd-138">Il codice XML seguente definisce un trigger di calendario giornaliero che avvia un'attività dal lunedì al venerdì (alle 8:00 AM) ogni settimana.</span><span class="sxs-lookup"><span data-stu-id="523bd-138">The following XML defines a daily calendar trigger that starts a task Monday through Friday ( at 8:00 AM) every week.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByWeek>
        <WeeksInterval>1</WeeksInterval>
        <DaysOfWeek>
            <Monday/>
            <Tuesday/>
            <Wednesday/>
            <Thurday/>
            <Friday/>
        </DaysOfWeek>
    </ScheduleByWeek>
</CalendarTrigger>
```



<span data-ttu-id="523bd-139">Per un esempio completo del codice XML per un'attività che usa un trigger settimanale, vedere [esempio di trigger settimanale (XML)](weekly-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="523bd-139">For a complete example of the XML for a task that uses a weekly trigger, see [Weekly Trigger Example (XML)](weekly-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="523bd-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="523bd-140">Requirements</span></span>



| <span data-ttu-id="523bd-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="523bd-141">Requirement</span></span> | <span data-ttu-id="523bd-142">Valore</span><span class="sxs-lookup"><span data-stu-id="523bd-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="523bd-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="523bd-143">Minimum supported client</span></span><br/> | <span data-ttu-id="523bd-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="523bd-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="523bd-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="523bd-145">Minimum supported server</span></span><br/> | <span data-ttu-id="523bd-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="523bd-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="523bd-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="523bd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="523bd-148">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="523bd-148">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="523bd-149">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="523bd-149">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





