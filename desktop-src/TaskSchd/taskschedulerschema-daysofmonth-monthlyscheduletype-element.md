---
title: Elemento DaysOfMonth (monthlyScheduleType)
description: Specifica i giorni del mese durante i quali viene eseguita l'attività.
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- Utilità di pianificazione elemento DaysOfMonth
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38c2106f8d612ee27dc1297023a59b531fa9548d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302698"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a><span data-ttu-id="2dbf4-104">Elemento DaysOfMonth (monthlyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="2dbf4-104">DaysOfMonth (monthlyScheduleType) Element</span></span>

<span data-ttu-id="2dbf4-105">Specifica i giorni del mese durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="2dbf4-105">Specifies the days of the month during which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

<span data-ttu-id="2dbf4-106">L'elemento **DaysOfMonth** è definito dal tipo complesso [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2dbf4-106">The **DaysOfMonth** element is defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2dbf4-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="2dbf4-107">Parent element</span></span>



| <span data-ttu-id="2dbf4-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2dbf4-108">Element</span></span>                                                                                    | <span data-ttu-id="2dbf4-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="2dbf4-109">Derived from</span></span>                                                                                         | <span data-ttu-id="2dbf4-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dbf4-110">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="2dbf4-111">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="2dbf4-111">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [<span data-ttu-id="2dbf4-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="2dbf4-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="2dbf4-113">Specifica un trigger che avvia un processo per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="2dbf4-113">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="2dbf4-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="2dbf4-114">Child elements</span></span>



| <span data-ttu-id="2dbf4-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="2dbf4-115">Element</span></span>                                                        | <span data-ttu-id="2dbf4-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="2dbf4-116">Type</span></span>                                                                    | <span data-ttu-id="2dbf4-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dbf4-117">Description</span></span>                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="2dbf4-118">**Giorno**</span><span class="sxs-lookup"><span data-stu-id="2dbf4-118">**Day**</span></span>](taskschedulerschema-day-daysofmonthtype-element.md) | [<span data-ttu-id="2dbf4-119">**dayOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="2dbf4-119">**dayOfMonthType**</span></span>](taskschedulerschema-dayofmonthtype-simpletype.md) | <span data-ttu-id="2dbf4-120">Specifica un giorno del mese durante il quale viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="2dbf4-120">Specifies a day of the month during which the task runs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2dbf4-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="2dbf4-121">Remarks</span></span>

<span data-ttu-id="2dbf4-122">Per lo sviluppo di script, i giorni del mese per la pianificazione vengono specificati utilizzando la proprietà [**MonthlyTrigger. DaysOfMonth**](monthlytrigger-daysofmonth.md) .</span><span class="sxs-lookup"><span data-stu-id="2dbf4-122">For script development, the days of the month for the schedule are specified using the [**MonthlyTrigger.DaysOfMonth**](monthlytrigger-daysofmonth.md) property.</span></span>

<span data-ttu-id="2dbf4-123">Per lo sviluppo in C++, i giorni del mese per la pianificazione vengono specificati usando la proprietà [**IMonthlyTrigger::D aysofmonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) .</span><span class="sxs-lookup"><span data-stu-id="2dbf4-123">For C++ development, the days of the month for the schedule are specified using the [**IMonthlyTrigger::DaysOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) property.</span></span>

<span data-ttu-id="2dbf4-124">L'elemento figlio deve essere ripetuto per ogni giorno del mese in cui l'attività deve essere eseguita.</span><span class="sxs-lookup"><span data-stu-id="2dbf4-124">The child element must be repeated for each day of the month the task is to run.</span></span>

## <a name="examples"></a><span data-ttu-id="2dbf4-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="2dbf4-125">Examples</span></span>

<span data-ttu-id="2dbf4-126">Il codice XML seguente definisce un trigger di calendario mensile che avvia un'attività (alle 8:30 AM) il primo giorno di ogni mese.</span><span class="sxs-lookup"><span data-stu-id="2dbf4-126">The following XML defines a monthly calendar trigger that starts a task (at 8:30 AM) on the 1st day of every month.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>  
        </DaysOfMonth>
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
    </ScheduleByMonth>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="2dbf4-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2dbf4-127">Requirements</span></span>



| <span data-ttu-id="2dbf4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dbf4-128">Requirement</span></span> | <span data-ttu-id="2dbf4-129">Valore</span><span class="sxs-lookup"><span data-stu-id="2dbf4-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2dbf4-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dbf4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2dbf4-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2dbf4-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2dbf4-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dbf4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2dbf4-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2dbf4-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2dbf4-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2dbf4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dbf4-135">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="2dbf4-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="2dbf4-136">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="2dbf4-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





