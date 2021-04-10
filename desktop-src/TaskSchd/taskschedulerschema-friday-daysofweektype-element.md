---
title: Elemento Friday (daysOfWeekType)
description: Specifica che l'attività viene eseguita il venerdì.
ms.assetid: bff85911-d354-4954-8c69-7b6f2ca312d3
keywords:
- Utilità di pianificazione elemento Friday
topic_type:
- apiref
api_name:
- Friday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 951142e7e925ea71ef1f833be4421351aaea3b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120799"
---
# <a name="friday-daysofweektype-element"></a><span data-ttu-id="9fe5b-104">Elemento Friday (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="9fe5b-104">Friday (daysOfWeekType) Element</span></span>

<span data-ttu-id="9fe5b-105">Specifica che l'attività viene eseguita il venerdì.</span><span class="sxs-lookup"><span data-stu-id="9fe5b-105">Specifies that the task runs on Friday.</span></span>

``` syntax
<xs:element name="Friday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="9fe5b-106">L'elemento **Friday** è definito dal tipo complesso [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9fe5b-106">The **Friday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9fe5b-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="9fe5b-107">Parent element</span></span>



| <span data-ttu-id="9fe5b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9fe5b-108">Element</span></span>                                                                                                                  | <span data-ttu-id="9fe5b-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="9fe5b-109">Derived from</span></span>                                                             | <span data-ttu-id="9fe5b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fe5b-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fe5b-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="9fe5b-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="9fe5b-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="9fe5b-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="9fe5b-113">Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione mensile giornaliera della settimana.</span><span class="sxs-lookup"><span data-stu-id="9fe5b-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="9fe5b-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="9fe5b-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="9fe5b-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="9fe5b-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="9fe5b-116">Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="9fe5b-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="9fe5b-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="9fe5b-117">Examples</span></span>

<span data-ttu-id="9fe5b-118">Il codice XML seguente definisce un calendario del giorno della settimana che avvia un'attività il venerdì.</span><span class="sxs-lookup"><span data-stu-id="9fe5b-118">The following XML defines a day of week calendar that starts a task on Friday.</span></span>


```XML
<DaysOfWeek>
    <Friday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="9fe5b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fe5b-119">Requirements</span></span>



| <span data-ttu-id="9fe5b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fe5b-120">Requirement</span></span> | <span data-ttu-id="9fe5b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9fe5b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9fe5b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fe5b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9fe5b-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fe5b-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9fe5b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fe5b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9fe5b-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fe5b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9fe5b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fe5b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe5b-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="9fe5b-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9fe5b-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="9fe5b-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





