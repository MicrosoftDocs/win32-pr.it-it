---
title: Months (monthlyDayOfWeekScheduleType)-elemento
description: Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Utilità di pianificazione dell'elemento months
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76f13a5823e0154519dbdb093dd03ea36bbe77b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400406"
---
# <a name="months-monthlydayofweekscheduletype-element"></a><span data-ttu-id="f43ed-104">Months (monthlyDayOfWeekScheduleType)-elemento</span><span class="sxs-lookup"><span data-stu-id="f43ed-104">Months (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="f43ed-105">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="f43ed-105">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span>

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

<span data-ttu-id="f43ed-106">L'elemento **months** viene definito dal tipo complesso [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f43ed-106">The **Months** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f43ed-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="f43ed-107">Parent element</span></span>



| <span data-ttu-id="f43ed-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f43ed-108">Element</span></span>                                                                                                                            | <span data-ttu-id="f43ed-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="f43ed-109">Derived from</span></span>                                                                                         | <span data-ttu-id="f43ed-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f43ed-110">Description</span></span>                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="f43ed-111">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="f43ed-111">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="f43ed-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="f43ed-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="f43ed-113">Specifica un trigger che avvia un processo per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="f43ed-113">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f43ed-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f43ed-114">Child elements</span></span>



| <span data-ttu-id="f43ed-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="f43ed-115">Element</span></span>                                                               | <span data-ttu-id="f43ed-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="f43ed-116">Type</span></span> | <span data-ttu-id="f43ed-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f43ed-117">Description</span></span>                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="f43ed-118">**Aprile**</span><span class="sxs-lookup"><span data-stu-id="f43ed-118">**April**</span></span>](taskschedulerschema-april-monthstype-element.md)         |      | <span data-ttu-id="f43ed-119">Specifica che l'attività viene eseguita nell'aprile.</span><span class="sxs-lookup"><span data-stu-id="f43ed-119">Specifies that the task runs in April.</span></span><br/>     |
| [<span data-ttu-id="f43ed-120">**Agosto**</span><span class="sxs-lookup"><span data-stu-id="f43ed-120">**August**</span></span>](taskschedulerschema-august-monthstype-element.md)       |      | <span data-ttu-id="f43ed-121">Specifica che l'attività viene eseguita nell'agosto.</span><span class="sxs-lookup"><span data-stu-id="f43ed-121">Specifies that the task runs in August.</span></span><br/>    |
| [<span data-ttu-id="f43ed-122">**Dicembre**</span><span class="sxs-lookup"><span data-stu-id="f43ed-122">**December**</span></span>](taskschedulerschema-december-monthstype-element.md)   |      | <span data-ttu-id="f43ed-123">Specifica che l'attività viene eseguita nel dicembre.</span><span class="sxs-lookup"><span data-stu-id="f43ed-123">Specifies that the task runs in December.</span></span><br/>  |
| [<span data-ttu-id="f43ed-124">**Febbraio**</span><span class="sxs-lookup"><span data-stu-id="f43ed-124">**February**</span></span>](taskschedulerschema-february-monthstype-element.md)   |      | <span data-ttu-id="f43ed-125">Specifica che l'attività viene eseguita nel febbraio.</span><span class="sxs-lookup"><span data-stu-id="f43ed-125">Specifies that the task runs in February.</span></span><br/>  |
| [<span data-ttu-id="f43ed-126">**Gennaio**</span><span class="sxs-lookup"><span data-stu-id="f43ed-126">**January**</span></span>](taskschedulerschema-january-monthstype-element.md)     |      | <span data-ttu-id="f43ed-127">Specifica che l'attività viene eseguita nel gennaio.</span><span class="sxs-lookup"><span data-stu-id="f43ed-127">Specifies that the task runs in January.</span></span><br/>   |
| [<span data-ttu-id="f43ed-128">**Luglio**</span><span class="sxs-lookup"><span data-stu-id="f43ed-128">**July**</span></span>](taskschedulerschema-july-monthstype-element.md)           |      | <span data-ttu-id="f43ed-129">Specifica che l'attività viene eseguita nel luglio.</span><span class="sxs-lookup"><span data-stu-id="f43ed-129">Specifies that the task runs in July.</span></span><br/>      |
| [<span data-ttu-id="f43ed-130">**Giugno**</span><span class="sxs-lookup"><span data-stu-id="f43ed-130">**June**</span></span>](taskschedulerschema-june-monthstype-element.md)           |      | <span data-ttu-id="f43ed-131">Specifica che l'attività viene eseguita in giugno.</span><span class="sxs-lookup"><span data-stu-id="f43ed-131">Specifies that the task runs in June.</span></span><br/>      |
| [<span data-ttu-id="f43ed-132">**Marzo**</span><span class="sxs-lookup"><span data-stu-id="f43ed-132">**March**</span></span>](taskschedulerschema-march-monthstype-element.md)         |      | <span data-ttu-id="f43ed-133">Specifica che l'attività viene eseguita nel marzo.</span><span class="sxs-lookup"><span data-stu-id="f43ed-133">Specifies that the task runs in March.</span></span><br/>     |
| [<span data-ttu-id="f43ed-134">**Mag**</span><span class="sxs-lookup"><span data-stu-id="f43ed-134">**May**</span></span>](taskschedulerschema-may-monthstype-element.md)             |      | <span data-ttu-id="f43ed-135">Specifica che l'attività viene eseguita in May.</span><span class="sxs-lookup"><span data-stu-id="f43ed-135">Specifies that the task runs in May.</span></span><br/>       |
| [<span data-ttu-id="f43ed-136">**Novembre**</span><span class="sxs-lookup"><span data-stu-id="f43ed-136">**November**</span></span>](taskschedulerschema-november-monthstype-element.md)   |      | <span data-ttu-id="f43ed-137">Specifica che l'attività viene eseguita nel novembre.</span><span class="sxs-lookup"><span data-stu-id="f43ed-137">Specifies that the task runs in November.</span></span><br/>  |
| [<span data-ttu-id="f43ed-138">**Ottobre**</span><span class="sxs-lookup"><span data-stu-id="f43ed-138">**October**</span></span>](taskschedulerschema-october-monthstype-element.md)     |      | <span data-ttu-id="f43ed-139">Specifica che l'attività viene eseguita nel ottobre.</span><span class="sxs-lookup"><span data-stu-id="f43ed-139">Specifies that the task runs in October.</span></span><br/>   |
| [<span data-ttu-id="f43ed-140">**Settembre**</span><span class="sxs-lookup"><span data-stu-id="f43ed-140">**September**</span></span>](taskschedulerschema-september-monthstype-element.md) |      | <span data-ttu-id="f43ed-141">Specifica che l'attività viene eseguita nel settembre.</span><span class="sxs-lookup"><span data-stu-id="f43ed-141">Specifies that the task runs in September.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f43ed-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="f43ed-142">Remarks</span></span>

<span data-ttu-id="f43ed-143">Per lo sviluppo di script, i mesi di un anno per una pianificazione giornaliera giornaliera della settimana vengono specificati utilizzando la proprietà [**MonthlyDOWTrigger. MonthsOfYear**](monthlydowtrigger-monthsofyear.md) .</span><span class="sxs-lookup"><span data-stu-id="f43ed-143">For scripting development, the months of a year for a monthly day-of-week schedule are specified using the [**MonthlyDOWTrigger.MonthsOfYear**](monthlydowtrigger-monthsofyear.md) property.</span></span>

<span data-ttu-id="f43ed-144">Per lo sviluppo in C++, i mesi di un anno per una pianificazione giornaliera giornaliera della settimana vengono specificati utilizzando la proprietà [**IMonthlyDOWTrigger:: MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) .</span><span class="sxs-lookup"><span data-stu-id="f43ed-144">For C++ development, the months of a year for a monthly day-of-week schedule are specified using the [**IMonthlyDOWTrigger::MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) property.</span></span>

<span data-ttu-id="f43ed-145">Gli elementi figlio precedenti sono definiti dal tipo complesso [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f43ed-145">The child elements above are defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="examples"></a><span data-ttu-id="f43ed-146">Esempio</span><span class="sxs-lookup"><span data-stu-id="f43ed-146">Examples</span></span>

<span data-ttu-id="f43ed-147">Il codice XML seguente definisce un calendario mensile del giorno della settimana che avvia l'attività il lunedì della prima settimana per ogni mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="f43ed-147">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f43ed-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f43ed-148">Requirements</span></span>



| <span data-ttu-id="f43ed-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="f43ed-149">Requirement</span></span> | <span data-ttu-id="f43ed-150">Valore</span><span class="sxs-lookup"><span data-stu-id="f43ed-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f43ed-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f43ed-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f43ed-152">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f43ed-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f43ed-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f43ed-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f43ed-154">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f43ed-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f43ed-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f43ed-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f43ed-156">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f43ed-156">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f43ed-157">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f43ed-157">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





