---
title: Elemento ScheduleByDay (calendarTriggerType)
description: Specifica una pianificazione giornaliera.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- trigger giornaliero Utilità di pianificazione, elemento XML
- Utilità di pianificazione elemento ScheduleByDay
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 614777ede63605dc7ed6936bda952c6071bda371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964710"
---
# <a name="schedulebyday-calendartriggertype-element"></a><span data-ttu-id="44964-105">Elemento ScheduleByDay (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="44964-105">ScheduleByDay (calendarTriggerType) Element</span></span>

<span data-ttu-id="44964-106">Specifica una pianificazione giornaliera.</span><span class="sxs-lookup"><span data-stu-id="44964-106">Specifies a daily schedule.</span></span> <span data-ttu-id="44964-107">Ad esempio, l'attività inizia alle 8:00 AM ogni giorno, ogni giorno, ogni terzo giorno e così via.</span><span class="sxs-lookup"><span data-stu-id="44964-107">For example, the task starts at 8:00 AM every day, every-other day, every third day, and so on.</span></span>

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

<span data-ttu-id="44964-108">L'elemento **ScheduleByDay** è definito dal tipo complesso [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="44964-108">The **ScheduleByDay** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="44964-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="44964-109">Parent element</span></span>



| <span data-ttu-id="44964-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="44964-110">Element</span></span>                                                                             | <span data-ttu-id="44964-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="44964-111">Derived from</span></span>                                                                       | <span data-ttu-id="44964-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44964-112">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44964-113">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="44964-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="44964-114">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="44964-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="44964-115">Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="44964-115">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="44964-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="44964-116">Child elements</span></span>



| <span data-ttu-id="44964-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="44964-117">Element</span></span>                                                                            | <span data-ttu-id="44964-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="44964-118">Type</span></span>             | <span data-ttu-id="44964-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44964-119">Description</span></span>                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="44964-120">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="44964-120">**DaysInterval**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | <span data-ttu-id="44964-121">**unsignedByte**</span><span class="sxs-lookup"><span data-stu-id="44964-121">**unsignedByte**</span></span> | <span data-ttu-id="44964-122">Specifica l'intervallo tra i giorni della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="44964-122">Specifies the interval between the days in the schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="44964-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="44964-123">Remarks</span></span>

<span data-ttu-id="44964-124">L'elemento figlio elencato in precedenza è definito dai tipi di elemento complessi [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="44964-124">The child element listed previously is defined by the [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) complex element types.</span></span>

<span data-ttu-id="44964-125">L'ora del giorno in cui l'attività viene avviata viene impostata dall'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="44964-125">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="44964-126">Per lo sviluppo di script, viene specificato un trigger giornaliero utilizzando l'oggetto [**DailyTrigger**](weeklytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="44964-126">For scripting development, a daily trigger is specified using the [**DailyTrigger**](weeklytrigger.md) object.</span></span>

<span data-ttu-id="44964-127">Per lo sviluppo in C++, viene specificato un trigger giornaliero usando l'interfaccia [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) .</span><span class="sxs-lookup"><span data-stu-id="44964-127">For C++ development, a daily trigger is specified using the [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="44964-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="44964-128">Examples</span></span>

<span data-ttu-id="44964-129">Il codice XML seguente definisce un trigger di calendario giornaliero che avvia l'attività ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="44964-129">The following XML defines a daily calendar trigger that starts the task every day.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



<span data-ttu-id="44964-130">Per un esempio completo del codice XML per un'attività che specifica una pianificazione giornaliera, vedere [esempio di trigger giornalieri (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="44964-130">For a complete example of the XML for a task that specifies a daily schedule, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44964-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44964-131">Requirements</span></span>



| <span data-ttu-id="44964-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="44964-132">Requirement</span></span> | <span data-ttu-id="44964-133">Valore</span><span class="sxs-lookup"><span data-stu-id="44964-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44964-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44964-134">Minimum supported client</span></span><br/> | <span data-ttu-id="44964-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44964-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="44964-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44964-136">Minimum supported server</span></span><br/> | <span data-ttu-id="44964-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="44964-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44964-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44964-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44964-139">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="44964-139">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="44964-140">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="44964-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





