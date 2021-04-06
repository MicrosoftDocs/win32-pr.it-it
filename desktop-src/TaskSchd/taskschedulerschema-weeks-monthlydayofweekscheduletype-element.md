---
title: Weeks (monthlyDayOfWeekScheduleType)-elemento
description: Specifica le settimane del mese in cui viene eseguita l'attività.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Utilità di pianificazione dell'elemento weeks
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e032b936353d2c89a84b5da684f681ea3c2b6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743311"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a><span data-ttu-id="d3aea-104">Weeks (monthlyDayOfWeekScheduleType)-elemento</span><span class="sxs-lookup"><span data-stu-id="d3aea-104">Weeks (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="d3aea-105">Specifica le settimane del mese in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="d3aea-105">Specifies the weeks of the month in which the task is run.</span></span>

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

<span data-ttu-id="d3aea-106">L'elemento **weeks** viene definito dal tipo complesso [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d3aea-106">The **Weeks** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d3aea-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="d3aea-107">Parent element</span></span>



| <span data-ttu-id="d3aea-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d3aea-108">Element</span></span>                                                                                                      | <span data-ttu-id="d3aea-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="d3aea-109">Derived from</span></span>                                                                                         | <span data-ttu-id="d3aea-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3aea-110">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3aea-111">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="d3aea-111">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="d3aea-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="d3aea-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="d3aea-113">Specifica un trigger che avvia un processo in base a una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="d3aea-113">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="d3aea-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d3aea-114">Child elements</span></span>



| <span data-ttu-id="d3aea-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="d3aea-115">Element</span></span>                                                    | <span data-ttu-id="d3aea-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3aea-116">Type</span></span>                                                        | <span data-ttu-id="d3aea-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3aea-117">Description</span></span>                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="d3aea-118">**Settimana**</span><span class="sxs-lookup"><span data-stu-id="d3aea-118">**Week**</span></span>](taskschedulerschema-week-weekstype-element.md) | [<span data-ttu-id="d3aea-119">**weekType**</span><span class="sxs-lookup"><span data-stu-id="d3aea-119">**weekType**</span></span>](taskschedulerschema-weektype-simpletype.md) | <span data-ttu-id="d3aea-120">Specifica una settimana specifica del mese.</span><span class="sxs-lookup"><span data-stu-id="d3aea-120">Specifies a specific week of the month.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d3aea-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3aea-121">Remarks</span></span>

<span data-ttu-id="d3aea-122">Per lo sviluppo di script, le settimane del mese vengono specificate utilizzando la proprietà [**MonthlyDOWTrigger. WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) .</span><span class="sxs-lookup"><span data-stu-id="d3aea-122">For scripting development, the weeks of the month are specified using the [**MonthlyDOWTrigger.WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) property.</span></span>

<span data-ttu-id="d3aea-123">Per lo sviluppo in C++, le settimane del mese vengono specificate usando la proprietà [**IMonthlyDOWTrigger:: WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) .</span><span class="sxs-lookup"><span data-stu-id="d3aea-123">For C++ development, the weeks of the month are specified using the [**IMonthlyDOWTrigger::WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) property.</span></span>

<span data-ttu-id="d3aea-124">Quando si specificano le settimane del mese, utilizzare 1-4 per specificare le prime quattro settimane del mese oppure utilizzare la stringa "Last" per indicare l'ultima settimana indipendentemente dalla settimana in cui si trova.</span><span class="sxs-lookup"><span data-stu-id="d3aea-124">When specifying the weeks of the month, use 1-4 to specify the first four weeks of the month or use the string "Last" to indicate the last week regardless of which week it is.</span></span>

## <a name="examples"></a><span data-ttu-id="d3aea-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="d3aea-125">Examples</span></span>

<span data-ttu-id="d3aea-126">Il codice XML seguente definisce un calendario mensile del giorno della settimana che avvia l'attività il lunedì della prima settimana per ogni mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="d3aea-126">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d3aea-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3aea-127">Requirements</span></span>



| <span data-ttu-id="d3aea-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3aea-128">Requirement</span></span> | <span data-ttu-id="d3aea-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d3aea-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d3aea-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3aea-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d3aea-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3aea-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d3aea-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3aea-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d3aea-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d3aea-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3aea-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3aea-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3aea-135">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d3aea-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d3aea-136">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d3aea-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





