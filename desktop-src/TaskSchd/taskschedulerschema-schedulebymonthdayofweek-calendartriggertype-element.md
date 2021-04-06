---
title: Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)
description: Specifica una pianificazione mensile giornaliera della settimana.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- Utilità di pianificazione elemento ScheduleByMonthDayOfWeek
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e92d6ad530466a2238c8239c9e262f85ae361d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742890"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a><span data-ttu-id="f3650-104">Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="f3650-104">ScheduleByMonthDayOfWeek (calendarTriggerType) Element</span></span>

<span data-ttu-id="f3650-105">Specifica una pianificazione mensile giornaliera della settimana.</span><span class="sxs-lookup"><span data-stu-id="f3650-105">Specifies a monthly day-of-week schedule.</span></span> <span data-ttu-id="f3650-106">Ad esempio, l'attività viene avviata in giorni specifici della settimana, settimane del mese e mesi dell'anno.</span><span class="sxs-lookup"><span data-stu-id="f3650-106">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span>

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

<span data-ttu-id="f3650-107">L'elemento **ScheduleByMonthDayOfWeek** è definito dal tipo complesso [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f3650-107">The **ScheduleByMonthDayOfWeek** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f3650-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="f3650-108">Parent element</span></span>



| <span data-ttu-id="f3650-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="f3650-109">Element</span></span>                                                                             | <span data-ttu-id="f3650-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="f3650-110">Derived from</span></span>                                                                       | <span data-ttu-id="f3650-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3650-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3650-112">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="f3650-112">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="f3650-113">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="f3650-113">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="f3650-114">Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="f3650-114">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f3650-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f3650-115">Child elements</span></span>



| <span data-ttu-id="f3650-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="f3650-116">Element</span></span>                                                                                   | <span data-ttu-id="f3650-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3650-117">Type</span></span>                                                                     | <span data-ttu-id="f3650-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3650-118">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="f3650-119">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="f3650-119">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="f3650-120">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="f3650-120">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="f3650-121">Specifica i giorni della settimana in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="f3650-121">Specifies the days of the week in which the task runs.</span></span><br/>       |
| [<span data-ttu-id="f3650-122">**Mesi**</span><span class="sxs-lookup"><span data-stu-id="f3650-122">**Months**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [<span data-ttu-id="f3650-123">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="f3650-123">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)         | <span data-ttu-id="f3650-124">Specifica i mesi dell'anno durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="f3650-124">Specifies the months of the year during which the task runs.</span></span><br/> |
| [<span data-ttu-id="f3650-125">**Settimane**</span><span class="sxs-lookup"><span data-stu-id="f3650-125">**Weeks**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | <span data-ttu-id="f3650-126">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="f3650-126">unsignedByte</span></span>                                                             | <span data-ttu-id="f3650-127">Specifica l'intervallo tra le settimane nella pianificazione.</span><span class="sxs-lookup"><span data-stu-id="f3650-127">Specifies the interval between the weeks in the schedule.</span></span><br/>    |



## <a name="remarks"></a><span data-ttu-id="f3650-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3650-128">Remarks</span></span>

<span data-ttu-id="f3650-129">L'ora del giorno in cui l'attività viene avviata viene impostata dall'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f3650-129">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="f3650-130">Per lo sviluppo di script, viene specificato un trigger di giorno della settimana mensile utilizzando l'oggetto [**MonthlyDOWTrigger**](monthlydowtrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f3650-130">For scripting development, a monthly day-of-week trigger is specified using the [**MonthlyDOWTrigger**](monthlydowtrigger.md) object.</span></span>

<span data-ttu-id="f3650-131">Per lo sviluppo in C++, viene specificato un trigger di giorno della settimana mensile usando l'interfaccia [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) .</span><span class="sxs-lookup"><span data-stu-id="f3650-131">For C++ development, a monthly day-of-week trigger is specified using the [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) interface.</span></span>

<span data-ttu-id="f3650-132">Gli elementi figlio elencati sopra sono definiti dai tipi di elemento complessi [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f3650-132">The child elements listed above are defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex element types.</span></span>

## <a name="examples"></a><span data-ttu-id="f3650-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="f3650-133">Examples</span></span>

<span data-ttu-id="f3650-134">Il codice XML seguente definisce un trigger di calendario mensile del giorno della settimana che avvia un'attività (alle 8:00 AM) il lunedì della prima settimana per ogni mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="f3650-134">The following XML defines a monthly day of week calendar trigger that starts a task ( at 8:00 AM) on Monday of the first week for each month of the year.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonthDayOfWeek>
        <Weeks>
            <Week>1</Week>
        </Weeks>
        <DaysOfWeek>
            <Monday/>
        </DaysOfWeek>
        <Months>
            <January/>
            <February/>
            <March/>
            <April/>
            <May/>
            <June/>
            <July/>
            <August/>
            <September/>
            <October/>
            <November/>
            <December/>
        <Months>
    </ScheduleByMonthDayOfWeek>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="f3650-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3650-135">Requirements</span></span>



| <span data-ttu-id="f3650-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3650-136">Requirement</span></span> | <span data-ttu-id="f3650-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f3650-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3650-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3650-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f3650-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3650-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f3650-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3650-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f3650-141">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f3650-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3650-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3650-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3650-143">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f3650-143">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f3650-144">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f3650-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





