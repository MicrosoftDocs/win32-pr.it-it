---
title: Elemento ScheduleByWeek (calendarTriggerType)
description: Specifica una pianificazione settimanale.
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- Utilità di pianificazione trigger settimanale, elemento XML
- Utilità di pianificazione elemento ScheduleByWeek
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d5ab62a0c39c4c1d0102edcdb96d310e9315820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400886"
---
# <a name="schedulebyweek-calendartriggertype-element"></a><span data-ttu-id="003e7-105">Elemento ScheduleByWeek (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="003e7-105">ScheduleByWeek (calendarTriggerType) Element</span></span>

<span data-ttu-id="003e7-106">Specifica una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="003e7-106">Specifies a weekly schedule.</span></span> <span data-ttu-id="003e7-107">Ad esempio, l'attività inizia alle 8:00 in un giorno specifico della settimana ogni settimana o in un giorno specifico della settimana ogni altra settimana.</span><span class="sxs-lookup"><span data-stu-id="003e7-107">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span>

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

<span data-ttu-id="003e7-108">L'elemento **ScheduleByWeek** è definito dal tipo complesso [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="003e7-108">The **ScheduleByWeek** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="003e7-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="003e7-109">Parent element</span></span>



| <span data-ttu-id="003e7-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="003e7-110">Element</span></span>                                                                             | <span data-ttu-id="003e7-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="003e7-111">Derived from</span></span>                                                                       | <span data-ttu-id="003e7-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="003e7-112">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="003e7-113">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="003e7-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="003e7-114">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="003e7-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="003e7-115">Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="003e7-115">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="003e7-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="003e7-116">Child elements</span></span>



| <span data-ttu-id="003e7-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="003e7-117">Element</span></span>                                                                               | <span data-ttu-id="003e7-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="003e7-118">Type</span></span>                                                                     | <span data-ttu-id="003e7-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="003e7-119">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="003e7-120">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="003e7-120">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [<span data-ttu-id="003e7-121">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="003e7-121">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="003e7-122">Specifica i giorni della settimana in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="003e7-122">Specifies the days of the week in which the task runs.</span></span><br/>    |
| [<span data-ttu-id="003e7-123">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="003e7-123">**WeeksInterval**</span></span>](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | <span data-ttu-id="003e7-124">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="003e7-124">unsignedByte</span></span>                                                             | <span data-ttu-id="003e7-125">Specifica l'intervallo tra le settimane nella pianificazione.</span><span class="sxs-lookup"><span data-stu-id="003e7-125">Specifies the interval between the weeks in the schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="003e7-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="003e7-126">Remarks</span></span>

<span data-ttu-id="003e7-127">Gli elementi figlio elencati sopra sono definiti dai tipi di elemento complessi [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="003e7-127">The child elements listed above are defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex element types.</span></span>

<span data-ttu-id="003e7-128">L'ora del giorno in cui l'attività viene avviata viene impostata dall'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="003e7-128">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="003e7-129">Per lo sviluppo di script, viene specificato un trigger settimanale usando l'oggetto [**WeeklyTrigger**](weeklytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="003e7-129">For scripting development, a weekly trigger is specified using the [**WeeklyTrigger**](weeklytrigger.md) object.</span></span>

<span data-ttu-id="003e7-130">Per lo sviluppo in C++, viene specificato un trigger settimanale usando l'interfaccia [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) .</span><span class="sxs-lookup"><span data-stu-id="003e7-130">For C++ development, a weekly trigger is specified using the [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="003e7-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="003e7-131">Examples</span></span>

<span data-ttu-id="003e7-132">Il codice XML seguente definisce un trigger di calendario settimanale che avvia un'attività dal lunedì al venerdì (alle 8:00 AM) ogni settimana.</span><span class="sxs-lookup"><span data-stu-id="003e7-132">The following XML defines a weekly calendar trigger that starts a task Monday through Friday (at 8:00 AM) every week.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="003e7-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="003e7-133">Requirements</span></span>



| <span data-ttu-id="003e7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="003e7-134">Requirement</span></span> | <span data-ttu-id="003e7-135">Valore</span><span class="sxs-lookup"><span data-stu-id="003e7-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="003e7-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="003e7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="003e7-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="003e7-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="003e7-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="003e7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="003e7-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="003e7-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="003e7-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="003e7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="003e7-141">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="003e7-141">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="003e7-142">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="003e7-142">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





