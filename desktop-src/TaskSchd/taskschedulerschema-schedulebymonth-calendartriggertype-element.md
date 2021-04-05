---
title: Elemento ScheduleByMonth (calendarTriggerType)
description: Specifica una pianificazione mensile.
ms.assetid: 3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8
keywords:
- Utilità di pianificazione elemento ScheduleByMonth
topic_type:
- apiref
api_name:
- ScheduleByMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6fda84a1cd4373f7988fa66a5ad70c97dd371d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120891"
---
# <a name="schedulebymonth-calendartriggertype-element"></a><span data-ttu-id="003af-104">Elemento ScheduleByMonth (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="003af-104">ScheduleByMonth (calendarTriggerType) Element</span></span>

<span data-ttu-id="003af-105">Specifica una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="003af-105">Specifies a monthly schedule.</span></span> <span data-ttu-id="003af-106">Ad esempio, l'attività inizia alle 8:00 in giorni specifici del mese per mesi specifici.</span><span class="sxs-lookup"><span data-stu-id="003af-106">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span>

``` syntax
<xs:element name="ScheduleByMonth"
    type="monthlyScheduleType"
 />
```

<span data-ttu-id="003af-107">L'elemento **ScheduleByMonth** è definito dal tipo complesso [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="003af-107">The **ScheduleByMonth** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="003af-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="003af-108">Parent element</span></span>



| <span data-ttu-id="003af-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="003af-109">Element</span></span>                                                                             | <span data-ttu-id="003af-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="003af-110">Derived from</span></span>                                                                       | <span data-ttu-id="003af-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="003af-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="003af-112">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="003af-112">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="003af-113">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="003af-113">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="003af-114">Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="003af-114">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="003af-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="003af-115">Child elements</span></span>



| <span data-ttu-id="003af-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="003af-116">Element</span></span>                                                                                                  | <span data-ttu-id="003af-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="003af-117">Type</span></span>                                                                       | <span data-ttu-id="003af-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="003af-118">Description</span></span>                                                             |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="003af-119">**DaysOfMonth (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="003af-119">**DaysOfMonth (monthlyScheduleType)**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="003af-120">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="003af-120">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="003af-121">Specifica i giorni del mese durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="003af-121">Specifies the days of the month during which the task runs.</span></span><br/>  |
| [<span data-ttu-id="003af-122">**Mesi (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="003af-122">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)           | [<span data-ttu-id="003af-123">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="003af-123">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)           | <span data-ttu-id="003af-124">Specifica i mesi dell'anno durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="003af-124">Specifies the months of the year during which the task runs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="003af-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="003af-125">Remarks</span></span>

<span data-ttu-id="003af-126">L'ora del giorno in cui l'attività viene avviata viene impostata dall'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="003af-126">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="003af-127">Per lo sviluppo di script, viene specificato un trigger mensile usando l'oggetto [**MonthlyTrigger**](monthlytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="003af-127">For script development, a monthly trigger is specified using the [**MonthlyTrigger**](monthlytrigger.md) object.</span></span>

<span data-ttu-id="003af-128">Per lo sviluppo in C++, viene specificato un trigger mensile usando l'interfaccia [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) .</span><span class="sxs-lookup"><span data-stu-id="003af-128">For C++ development, a monthly trigger is specified using the [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) interface.</span></span>

<span data-ttu-id="003af-129">Gli elementi figlio elencati di seguito sono definiti dai tipi di elemento complessi [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="003af-129">The child elements listed below are defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex element types.</span></span>

## <a name="examples"></a><span data-ttu-id="003af-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="003af-130">Examples</span></span>

<span data-ttu-id="003af-131">Il codice XML seguente definisce un trigger di calendario mensile che avvia un'attività (alle 8:00 AM) il primo e il quindicesimo giorno di ogni mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="003af-131">The following XML defines a monthly calendar trigger that starts a task ( at 8:00 AM) on the 1st and 15th day of every month of the year.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>
            <Day>15</Day>
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
        </Months>
    </ScheduleByMonth>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="003af-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="003af-132">Requirements</span></span>



| <span data-ttu-id="003af-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="003af-133">Requirement</span></span> | <span data-ttu-id="003af-134">Valore</span><span class="sxs-lookup"><span data-stu-id="003af-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="003af-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="003af-135">Minimum supported client</span></span><br/> | <span data-ttu-id="003af-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="003af-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="003af-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="003af-137">Minimum supported server</span></span><br/> | <span data-ttu-id="003af-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="003af-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="003af-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="003af-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="003af-140">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="003af-140">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="003af-141">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="003af-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





