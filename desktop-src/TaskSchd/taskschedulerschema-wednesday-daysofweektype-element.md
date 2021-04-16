---
title: Elemento Wednesday (daysOfWeekType)
description: Specifica che l'attività viene eseguita il mercoledì.
ms.assetid: 6d4f52e2-4390-4f9d-bab8-813bd0851582
keywords:
- Utilità di pianificazione elemento mercoledì
topic_type:
- apiref
api_name:
- Wednesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f9d8c60cb7cea818cc0b096e99e97e8f1490d47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518483"
---
# <a name="wednesday-daysofweektype-element"></a><span data-ttu-id="c6a98-104">Elemento Wednesday (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="c6a98-104">Wednesday (daysOfWeekType) Element</span></span>

<span data-ttu-id="c6a98-105">Specifica che l'attività viene eseguita il mercoledì.</span><span class="sxs-lookup"><span data-stu-id="c6a98-105">Specifies that the task runs on Wednesday.</span></span>

``` syntax
<xs:element name="Wednesday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="c6a98-106">L'elemento **Wednesday** è definito dal tipo complesso [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c6a98-106">The **Wednesday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c6a98-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="c6a98-107">Parent element</span></span>



| <span data-ttu-id="c6a98-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c6a98-108">Element</span></span>                                                                                                                  | <span data-ttu-id="c6a98-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="c6a98-109">Derived from</span></span>                                                             | <span data-ttu-id="c6a98-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6a98-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6a98-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c6a98-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="c6a98-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="c6a98-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="c6a98-113">Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione mensile giornaliera della settimana.</span><span class="sxs-lookup"><span data-stu-id="c6a98-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="c6a98-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="c6a98-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="c6a98-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="c6a98-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="c6a98-116">Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="c6a98-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="c6a98-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="c6a98-117">Examples</span></span>

<span data-ttu-id="c6a98-118">Il codice XML seguente definisce un calendario del giorno della settimana che avvia un'attività il mercoledì.</span><span class="sxs-lookup"><span data-stu-id="c6a98-118">The following XML defines a day of week calendar that starts a task on Wednesday.</span></span>


```XML
<DaysOfWeek>
    <Wednesday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="c6a98-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6a98-119">Requirements</span></span>



| <span data-ttu-id="c6a98-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6a98-120">Requirement</span></span> | <span data-ttu-id="c6a98-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c6a98-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c6a98-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6a98-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c6a98-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6a98-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c6a98-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6a98-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c6a98-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c6a98-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6a98-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6a98-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a98-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c6a98-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c6a98-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c6a98-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





