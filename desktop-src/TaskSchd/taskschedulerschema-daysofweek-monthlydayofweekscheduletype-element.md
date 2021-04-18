---
title: Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)
description: Specifica i giorni della settimana in cui viene eseguita l'attività. | Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
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
ms.openlocfilehash: 3867e08dd001a035a3ab25da056f75c1e73eeeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321845"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a><span data-ttu-id="86d61-105">Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)</span><span class="sxs-lookup"><span data-stu-id="86d61-105">DaysOfWeek (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="86d61-106">Specifica i giorni della settimana in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="86d61-106">Specifies the days of the week in which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

<span data-ttu-id="86d61-107">L'elemento **DaysOfWeek** è definito dal tipo complesso [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="86d61-107">The **DaysOfWeek** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="86d61-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="86d61-108">Parent element</span></span>



| <span data-ttu-id="86d61-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="86d61-109">Element</span></span>                                                                                                      | <span data-ttu-id="86d61-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="86d61-110">Derived from</span></span>                                                                                         | <span data-ttu-id="86d61-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86d61-111">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="86d61-112">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="86d61-112">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="86d61-113">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="86d61-113">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="86d61-114">Specifica un trigger che avvia un processo per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="86d61-114">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="86d61-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="86d61-115">Child elements</span></span>



| <span data-ttu-id="86d61-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="86d61-116">Element</span></span>                                                                   | <span data-ttu-id="86d61-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="86d61-117">Type</span></span> | <span data-ttu-id="86d61-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86d61-118">Description</span></span>                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="86d61-119">**Friday**</span><span class="sxs-lookup"><span data-stu-id="86d61-119">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       |      | <span data-ttu-id="86d61-120">Specifica che l'attività viene eseguita il venerdì.</span><span class="sxs-lookup"><span data-stu-id="86d61-120">Specifies that the task runs on Friday.</span></span><br/>    |
| [<span data-ttu-id="86d61-121">**Monday**</span><span class="sxs-lookup"><span data-stu-id="86d61-121">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       |      | <span data-ttu-id="86d61-122">Specifica che l'attività viene eseguita il lunedì.</span><span class="sxs-lookup"><span data-stu-id="86d61-122">Specifies that the task runs on Monday.</span></span><br/>    |
| [<span data-ttu-id="86d61-123">**Sabato**</span><span class="sxs-lookup"><span data-stu-id="86d61-123">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   |      | <span data-ttu-id="86d61-124">Specifica che l'attività viene eseguita il sabato.</span><span class="sxs-lookup"><span data-stu-id="86d61-124">Specifies that the task runs on Saturday.</span></span><br/>  |
| [<span data-ttu-id="86d61-125">**Sunday**</span><span class="sxs-lookup"><span data-stu-id="86d61-125">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       |      | <span data-ttu-id="86d61-126">Specifica che l'attività viene eseguita la domenica.</span><span class="sxs-lookup"><span data-stu-id="86d61-126">Specifies that the task runs on Sunday.</span></span><br/>    |
| [<span data-ttu-id="86d61-127">**Thursday**</span><span class="sxs-lookup"><span data-stu-id="86d61-127">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   |      | <span data-ttu-id="86d61-128">Specifica che l'attività viene eseguita il giovedì.</span><span class="sxs-lookup"><span data-stu-id="86d61-128">Specifies that the task runs on Thursday.</span></span><br/>  |
| [<span data-ttu-id="86d61-129">**Tuesday**</span><span class="sxs-lookup"><span data-stu-id="86d61-129">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | <span data-ttu-id="86d61-130">Specifica che l'attività viene eseguita il martedì.</span><span class="sxs-lookup"><span data-stu-id="86d61-130">Specifies that the task runs on Tuesday.</span></span><br/>   |
| [<span data-ttu-id="86d61-131">**Wednesday**</span><span class="sxs-lookup"><span data-stu-id="86d61-131">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) |      | <span data-ttu-id="86d61-132">Specifica che l'attività viene eseguita il mercoledì.</span><span class="sxs-lookup"><span data-stu-id="86d61-132">Specifies that the task runs on Wednesday.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="86d61-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="86d61-133">Remarks</span></span>

<span data-ttu-id="86d61-134">Per lo sviluppo di script, i giorni della settimana per un calendario mensile di giorno della settimana vengono specificati utilizzando la proprietà [**MonthlyDOWTrigger. DaysOfWeek**](monthlydowtrigger-daysofweek.md) .</span><span class="sxs-lookup"><span data-stu-id="86d61-134">For scripting development, the days of the week for a monthly day-of-week calendar are specified using the [**MonthlyDOWTrigger.DaysOfWeek**](monthlydowtrigger-daysofweek.md) property.</span></span>

<span data-ttu-id="86d61-135">Per lo sviluppo in C++, i giorni della settimana per un calendario mensile di giorno della settimana vengono specificati usando la proprietà [**IMonthlyDOWTrigger::D aysofweek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) .</span><span class="sxs-lookup"><span data-stu-id="86d61-135">For C++ development, the days of the week for a monthly day-of-week calendar are specified using the [**IMonthlyDOWTrigger::DaysOfWeek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) property.</span></span>

<span data-ttu-id="86d61-136">Gli elementi figlio precedenti sono definiti dal tipo complesso [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="86d61-136">The child elements above are defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="examples"></a><span data-ttu-id="86d61-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="86d61-137">Examples</span></span>

<span data-ttu-id="86d61-138">Il codice XML seguente definisce un calendario mensile del giorno della settimana che avvia l'attività il lunedì della prima settimana per ogni mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="86d61-138">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


```XML
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
```



## <a name="requirements"></a><span data-ttu-id="86d61-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86d61-139">Requirements</span></span>



| <span data-ttu-id="86d61-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="86d61-140">Requirement</span></span> | <span data-ttu-id="86d61-141">Valore</span><span class="sxs-lookup"><span data-stu-id="86d61-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="86d61-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86d61-142">Minimum supported client</span></span><br/> | <span data-ttu-id="86d61-143">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86d61-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="86d61-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86d61-144">Minimum supported server</span></span><br/> | <span data-ttu-id="86d61-145">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="86d61-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="86d61-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86d61-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86d61-147">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="86d61-147">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="86d61-148">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="86d61-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





