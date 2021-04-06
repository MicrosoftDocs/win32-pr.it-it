---
title: Elemento DaysInterval (dailyScheduleType)
description: Specifica l'intervallo tra i giorni della pianificazione.
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- Utilità di pianificazione elemento DaysInterval
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97b50581aa4825b31983a234a5eb47ff7b7b7e06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963863"
---
# <a name="daysinterval-dailyscheduletype-element"></a><span data-ttu-id="bc3d3-104">Elemento DaysInterval (dailyScheduleType)</span><span class="sxs-lookup"><span data-stu-id="bc3d3-104">DaysInterval (dailyScheduleType) Element</span></span>

<span data-ttu-id="bc3d3-105">Specifica l'intervallo tra i giorni della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="bc3d3-105">Specifies the interval between the days in the schedule.</span></span>

``` syntax
<xs:element name="DaysInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedInt"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="365"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="bc3d3-106">L'elemento è definito dal tipo complesso [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bc3d3-106">The element is defined by the [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bc3d3-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="bc3d3-107">Parent element</span></span>



| <span data-ttu-id="bc3d3-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="bc3d3-108">Element</span></span>                                                                                | <span data-ttu-id="bc3d3-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="bc3d3-109">Derived from</span></span>                                                                   | <span data-ttu-id="bc3d3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc3d3-110">Description</span></span>                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="bc3d3-111">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="bc3d3-111">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [<span data-ttu-id="bc3d3-112">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="bc3d3-112">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md) | <span data-ttu-id="bc3d3-113">Specifica una pianificazione giornaliera.</span><span class="sxs-lookup"><span data-stu-id="bc3d3-113">Specifies a daily schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bc3d3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc3d3-114">Remarks</span></span>

<span data-ttu-id="bc3d3-115">Per lo sviluppo di script, l'intervallo di giorni per un trigger giornaliero viene specificato dalla proprietà [**DailyTrigger. DaysInterval**](dailytrigger-daysinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="bc3d3-115">For script development, the days interval for a daily trigger is specified by the [**DailyTrigger.DaysInterval**](dailytrigger-daysinterval.md) property.</span></span>

<span data-ttu-id="bc3d3-116">Per lo sviluppo in C++, l'intervallo di giorni per un trigger giornaliero viene specificato dalla proprietà [**IDailyTrigger::D aysinterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) .</span><span class="sxs-lookup"><span data-stu-id="bc3d3-116">For C++ development, the days interval for a daily trigger is specified by the [**IDailyTrigger::DaysInterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="bc3d3-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="bc3d3-117">Examples</span></span>

<span data-ttu-id="bc3d3-118">Il codice XML seguente definisce un trigger di calendario giornaliero che avvia l'attività ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="bc3d3-118">The following XML defines a daily calendar trigger that starts the task every day.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



<span data-ttu-id="bc3d3-119">Per un esempio completo del codice XML per un'attività che specifica una pianificazione giornaliera, vedere [esempio di trigger giornalieri (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="bc3d3-119">For a complete example of the XML for a task that specifies a daily schedule, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc3d3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc3d3-120">Requirements</span></span>



| <span data-ttu-id="bc3d3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc3d3-121">Requirement</span></span> | <span data-ttu-id="bc3d3-122">Valore</span><span class="sxs-lookup"><span data-stu-id="bc3d3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bc3d3-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc3d3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bc3d3-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc3d3-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bc3d3-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc3d3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bc3d3-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bc3d3-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc3d3-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc3d3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc3d3-128">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="bc3d3-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="bc3d3-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="bc3d3-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





