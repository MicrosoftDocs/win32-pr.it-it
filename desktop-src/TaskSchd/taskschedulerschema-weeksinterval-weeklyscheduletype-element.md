---
title: Elemento WeeksInterval (weeklyScheduleType)
description: Specifica l'intervallo tra le settimane nella pianificazione.
ms.assetid: 6cbf1e7e-a695-4012-97fd-fe3360c362c4
keywords:
- Utilità di pianificazione elemento WeeksInterval
topic_type:
- apiref
api_name:
- WeeksInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747ca4b73ff18bdb3e29d8b909d72b8d2367d89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400845"
---
# <a name="weeksinterval-weeklyscheduletype-element"></a><span data-ttu-id="56646-104">Elemento WeeksInterval (weeklyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="56646-104">WeeksInterval (weeklyScheduleType) Element</span></span>

<span data-ttu-id="56646-105">Specifica l'intervallo tra le settimane nella pianificazione.</span><span class="sxs-lookup"><span data-stu-id="56646-105">Specifies the interval between the weeks in the schedule.</span></span>

``` syntax
<xs:element name="WeeksInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="52"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="56646-106">L'elemento è definito dal tipo complesso [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="56646-106">The element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="56646-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="56646-107">Parent element</span></span>



| <span data-ttu-id="56646-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="56646-108">Element</span></span>                                                                                  | <span data-ttu-id="56646-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="56646-109">Derived from</span></span>                                                                     | <span data-ttu-id="56646-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56646-110">Description</span></span>                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="56646-111">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="56646-111">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [<span data-ttu-id="56646-112">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="56646-112">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md) | <span data-ttu-id="56646-113">Specifica una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="56646-113">Specifies a weekly schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="56646-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="56646-114">Remarks</span></span>

<span data-ttu-id="56646-115">Per lo sviluppo di script, l'intervallo settimanale viene specificato tramite la proprietà [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="56646-115">For scripting development, the weekly interval is specified using the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md) property.</span></span>

<span data-ttu-id="56646-116">Per lo sviluppo in C++, l'intervallo settimanale viene specificato con la proprietà [**IWeeklyTrigger:: WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .</span><span class="sxs-lookup"><span data-stu-id="56646-116">For C++ development, the weekly interval is specified using the [**IWeeklyTrigger::WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="56646-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="56646-117">Examples</span></span>

<span data-ttu-id="56646-118">Il codice XML seguente definisce un trigger di calendario settimanale che avvia un'attività dal lunedì al venerdì (alle 8:00 AM) ogni settimana.</span><span class="sxs-lookup"><span data-stu-id="56646-118">The following XML defines a weekly calendar trigger that starts a task Monday through Friday ( at 8:00 AM) every week.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="56646-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56646-119">Requirements</span></span>



| <span data-ttu-id="56646-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="56646-120">Requirement</span></span> | <span data-ttu-id="56646-121">Valore</span><span class="sxs-lookup"><span data-stu-id="56646-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="56646-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56646-122">Minimum supported client</span></span><br/> | <span data-ttu-id="56646-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56646-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="56646-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56646-124">Minimum supported server</span></span><br/> | <span data-ttu-id="56646-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="56646-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="56646-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56646-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56646-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="56646-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="56646-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="56646-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





