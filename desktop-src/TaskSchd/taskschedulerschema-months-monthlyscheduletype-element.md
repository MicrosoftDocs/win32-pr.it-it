---
title: Months (monthlyScheduleType)-elemento
description: Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
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
ms.openlocfilehash: 0ed40fd2466f8962f839f39e7addd3b7e1bc33eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120898"
---
# <a name="months-monthlyscheduletype-element"></a><span data-ttu-id="823fb-104">Months (monthlyScheduleType)-elemento</span><span class="sxs-lookup"><span data-stu-id="823fb-104">Months (monthlyScheduleType) Element</span></span>

<span data-ttu-id="823fb-105">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="823fb-105">Specifies the months of the year during which the task runs for a monthly schedule.</span></span>

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

<span data-ttu-id="823fb-106">L'elemento **months** viene definito dal tipo complesso [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="823fb-106">The **Months** element is defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="823fb-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="823fb-107">Parent element</span></span>



| <span data-ttu-id="823fb-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="823fb-108">Element</span></span>                                                                                    | <span data-ttu-id="823fb-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="823fb-109">Derived from</span></span>                                                                       | <span data-ttu-id="823fb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="823fb-110">Description</span></span>                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="823fb-111">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="823fb-111">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [<span data-ttu-id="823fb-112">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="823fb-112">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md) | <span data-ttu-id="823fb-113">Specifica una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="823fb-113">Specifies a monthly schedule.</span></span> <br/> |



## <a name="child-elements"></a><span data-ttu-id="823fb-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="823fb-114">Child elements</span></span>



| <span data-ttu-id="823fb-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="823fb-115">Element</span></span>                                                                            | <span data-ttu-id="823fb-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="823fb-116">Type</span></span> | <span data-ttu-id="823fb-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="823fb-117">Description</span></span>                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="823fb-118">**Aprile (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="823fb-118">**April (monthsType)**</span></span>](taskschedulerschema-april-monthstype-element.md)         |      | <span data-ttu-id="823fb-119">Specifica che l'attività viene eseguita nell'aprile.</span><span class="sxs-lookup"><span data-stu-id="823fb-119">Specifies that the task runs in April.</span></span><br/>     |
| [<span data-ttu-id="823fb-120">**Agosto (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="823fb-120">**August (monthsType)**</span></span>](taskschedulerschema-august-monthstype-element.md)       |      | <span data-ttu-id="823fb-121">Specifica che l'attività viene eseguita nell'agosto.</span><span class="sxs-lookup"><span data-stu-id="823fb-121">Specifies that the task runs in August.</span></span><br/>    |
| [<span data-ttu-id="823fb-122">**Dicembre (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="823fb-122">**December (monthsType)**</span></span>](taskschedulerschema-december-monthstype-element.md)   |      | <span data-ttu-id="823fb-123">Specifica che l'attività viene eseguita nel dicembre.</span><span class="sxs-lookup"><span data-stu-id="823fb-123">Specifies that the task runs in December.</span></span><br/>  |
| [<span data-ttu-id="823fb-124">**Febbraio (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="823fb-124">**February (monthsType)**</span></span>](taskschedulerschema-february-monthstype-element.md)   |      | <span data-ttu-id="823fb-125">Specifica che l'attività viene eseguita nel febbraio.</span><span class="sxs-lookup"><span data-stu-id="823fb-125">Specifies that the task runs in February.</span></span><br/>  |
| [<span data-ttu-id="823fb-126">**Gennaio (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="823fb-126">**January (monthsType)**</span></span>](taskschedulerschema-january-monthstype-element.md)     |      | <span data-ttu-id="823fb-127">Specifica che l'attività viene eseguita nel gennaio.</span><span class="sxs-lookup"><span data-stu-id="823fb-127">Specifies that the task runs in January.</span></span><br/>   |
| [<span data-ttu-id="823fb-128">**Luglio (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="823fb-128">**July (monthsType)**</span></span>](taskschedulerschema-july-monthstype-element.md)           |      | <span data-ttu-id="823fb-129">Specifica che l'attività viene eseguita nel luglio.</span><span class="sxs-lookup"><span data-stu-id="823fb-129">Specifies that the task runs in July.</span></span><br/>      |
| [<span data-ttu-id="823fb-130">**Giugno (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="823fb-130">**June (monthsType)**</span></span>](taskschedulerschema-june-monthstype-element.md)           |      | <span data-ttu-id="823fb-131">Specifica che l'attività viene eseguita in giugno.</span><span class="sxs-lookup"><span data-stu-id="823fb-131">Specifies that the task runs in June.</span></span><br/>      |
| [<span data-ttu-id="823fb-132">**Marzo (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="823fb-132">**March (monthsType)**</span></span>](taskschedulerschema-march-monthstype-element.md)         |      | <span data-ttu-id="823fb-133">Specifica che l'attività viene eseguita nel marzo.</span><span class="sxs-lookup"><span data-stu-id="823fb-133">Specifies that the task runs in March.</span></span><br/>     |
| [<span data-ttu-id="823fb-134">**Maggio (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="823fb-134">**May (monthsType)**</span></span>](taskschedulerschema-may-monthstype-element.md)             |      | <span data-ttu-id="823fb-135">Specifica che l'attività viene eseguita in May.</span><span class="sxs-lookup"><span data-stu-id="823fb-135">Specifies that the task runs in May.</span></span><br/>       |
| [<span data-ttu-id="823fb-136">**Novembre (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="823fb-136">**November (monthsType)**</span></span>](taskschedulerschema-november-monthstype-element.md)   |      | <span data-ttu-id="823fb-137">Specifica che l'attività viene eseguita nel novembre.</span><span class="sxs-lookup"><span data-stu-id="823fb-137">Specifies that the task runs in November.</span></span><br/>  |
| [<span data-ttu-id="823fb-138">**Ottobre (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="823fb-138">**October (monthsType)**</span></span>](taskschedulerschema-october-monthstype-element.md)     |      | <span data-ttu-id="823fb-139">Specifica che l'attività viene eseguita nel ottobre.</span><span class="sxs-lookup"><span data-stu-id="823fb-139">Specifies that the task runs in October.</span></span><br/>   |
| [<span data-ttu-id="823fb-140">**Settembre (monthsType)**</span><span class="sxs-lookup"><span data-stu-id="823fb-140">**September (monthsType)**</span></span>](taskschedulerschema-september-monthstype-element.md) |      | <span data-ttu-id="823fb-141">Specifica che l'attività viene eseguita nel settembre.</span><span class="sxs-lookup"><span data-stu-id="823fb-141">Specifies that the task runs in September.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="823fb-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="823fb-142">Remarks</span></span>

<span data-ttu-id="823fb-143">Per lo sviluppo di script, i mesi della pianificazione vengono specificati utilizzando la proprietà [**MonthlyTrigger. MonthsOfYear**](monthlytrigger-monthsofyear.md) .</span><span class="sxs-lookup"><span data-stu-id="823fb-143">For script development, the months of the schedule are specified using the [**MonthlyTrigger.MonthsOfYear**](monthlytrigger-monthsofyear.md) property.</span></span>

<span data-ttu-id="823fb-144">Per lo sviluppo in C++, i mesi della pianificazione vengono specificati utilizzando la proprietà [**IMonthlyTrigger:: MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) .</span><span class="sxs-lookup"><span data-stu-id="823fb-144">For C++ development, the months of the schedule are specified using the [**IMonthlyTrigger::MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) property.</span></span>

## <a name="examples"></a><span data-ttu-id="823fb-145">Esempio</span><span class="sxs-lookup"><span data-stu-id="823fb-145">Examples</span></span>

<span data-ttu-id="823fb-146">Il codice XML seguente definisce un calendario mensile che avvia l'attività il primo e il quindicesimo giorno di ogni mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="823fb-146">The following XML defines a monthly calendar that starts the task on the 1st and 15th day of every month of the year.</span></span>


```XML
</ScheduleByMonth>
    <DaysOfMonth>
        <Day>1</Day>
        <Day>15</Day>
    </DaysOfMonth
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
```



## <a name="requirements"></a><span data-ttu-id="823fb-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="823fb-147">Requirements</span></span>



| <span data-ttu-id="823fb-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="823fb-148">Requirement</span></span> | <span data-ttu-id="823fb-149">Valore</span><span class="sxs-lookup"><span data-stu-id="823fb-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="823fb-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="823fb-150">Minimum supported client</span></span><br/> | <span data-ttu-id="823fb-151">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="823fb-151">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="823fb-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="823fb-152">Minimum supported server</span></span><br/> | <span data-ttu-id="823fb-153">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="823fb-153">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="823fb-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="823fb-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="823fb-155">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="823fb-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="823fb-156">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="823fb-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





