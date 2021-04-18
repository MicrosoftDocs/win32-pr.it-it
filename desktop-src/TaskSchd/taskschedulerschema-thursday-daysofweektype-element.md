---
title: Elemento Thursday (daysOfWeekType)
description: Specifica che l'attività viene eseguita il giovedì.
ms.assetid: 01d0e7e8-7135-4f43-9d8f-b50c002b93bc
keywords:
- Utilità di pianificazione elemento di giovedì
topic_type:
- apiref
api_name:
- Thursday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12b1fb602411a9e4562a044b044e43de4800f239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302164"
---
# <a name="thursday-daysofweektype-element"></a><span data-ttu-id="819bb-104">Elemento Thursday (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="819bb-104">Thursday (daysOfWeekType) Element</span></span>

<span data-ttu-id="819bb-105">Specifica che l'attività viene eseguita il giovedì.</span><span class="sxs-lookup"><span data-stu-id="819bb-105">Specifies that the task runs on Thursday.</span></span>

``` syntax
<xs:element name="Thursday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="819bb-106">L'elemento **Thursday** è definito dal tipo complesso [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="819bb-106">The **Thursday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="819bb-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="819bb-107">Parent element</span></span>



| <span data-ttu-id="819bb-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="819bb-108">Element</span></span>                                                                                                                  | <span data-ttu-id="819bb-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="819bb-109">Derived from</span></span>                                                             | <span data-ttu-id="819bb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="819bb-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="819bb-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="819bb-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="819bb-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="819bb-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="819bb-113">Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione mensile giornaliera della settimana.</span><span class="sxs-lookup"><span data-stu-id="819bb-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="819bb-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="819bb-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="819bb-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="819bb-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="819bb-116">Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="819bb-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="819bb-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="819bb-117">Examples</span></span>

<span data-ttu-id="819bb-118">Il codice XML seguente definisce un calendario del giorno della settimana che avvia un'attività giovedì.</span><span class="sxs-lookup"><span data-stu-id="819bb-118">The following XML defines a day of week calendar that starts a task on Thursday.</span></span>


```XML
<DaysOfWeek>
    <Thursday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="819bb-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="819bb-119">Requirements</span></span>



| <span data-ttu-id="819bb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="819bb-120">Requirement</span></span> | <span data-ttu-id="819bb-121">Valore</span><span class="sxs-lookup"><span data-stu-id="819bb-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="819bb-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="819bb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="819bb-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="819bb-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="819bb-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="819bb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="819bb-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="819bb-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="819bb-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="819bb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="819bb-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="819bb-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="819bb-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="819bb-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





