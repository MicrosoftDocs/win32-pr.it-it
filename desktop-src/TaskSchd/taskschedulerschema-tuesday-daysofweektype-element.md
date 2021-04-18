---
title: Elemento Tuesday (daysOfWeekType)
description: Specifica che l'attività viene eseguita il martedì.
ms.assetid: 588608e9-33f9-405d-8b4b-35f11ab403db
keywords:
- Utilità di pianificazione dell'elemento Tuesday
topic_type:
- apiref
api_name:
- Tuesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ed48803d0cad5dae409202869c600e7e7a60643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302675"
---
# <a name="tuesday-daysofweektype-element"></a><span data-ttu-id="2ed73-104">Elemento Tuesday (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="2ed73-104">Tuesday (daysOfWeekType) Element</span></span>

<span data-ttu-id="2ed73-105">Specifica che l'attività viene eseguita il martedì.</span><span class="sxs-lookup"><span data-stu-id="2ed73-105">Specifies that the task runs on Tuesday.</span></span>

``` syntax
<xs:element name="Tuesday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="2ed73-106">L'elemento **Tuesday** viene definito dal tipo complesso [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2ed73-106">The **Tuesday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2ed73-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="2ed73-107">Parent element</span></span>



| <span data-ttu-id="2ed73-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2ed73-108">Element</span></span>                                                                                                                  | <span data-ttu-id="2ed73-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="2ed73-109">Derived from</span></span>                                                             | <span data-ttu-id="2ed73-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ed73-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ed73-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="2ed73-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="2ed73-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="2ed73-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="2ed73-113">Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione mensile giornaliera della settimana.</span><span class="sxs-lookup"><span data-stu-id="2ed73-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="2ed73-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="2ed73-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="2ed73-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="2ed73-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="2ed73-116">Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="2ed73-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="2ed73-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="2ed73-117">Examples</span></span>

<span data-ttu-id="2ed73-118">Il codice XML seguente definisce un calendario del giorno della settimana che avvia un'attività il martedì.</span><span class="sxs-lookup"><span data-stu-id="2ed73-118">The following XML defines a day of week calendar that starts a task on Tuesday.</span></span>


```XML
<DaysOfWeek>
    <Tuesday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="2ed73-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ed73-119">Requirements</span></span>



| <span data-ttu-id="2ed73-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ed73-120">Requirement</span></span> | <span data-ttu-id="2ed73-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2ed73-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2ed73-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ed73-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2ed73-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ed73-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2ed73-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ed73-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2ed73-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2ed73-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ed73-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ed73-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ed73-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="2ed73-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="2ed73-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="2ed73-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





