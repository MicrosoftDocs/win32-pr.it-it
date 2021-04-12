---
title: Elemento Monday (daysOfWeekType)
description: Specifica che l'attività viene eseguita il lunedì.
ms.assetid: 2b7ce0c1-c635-47d0-b482-5c93c0028c92
keywords:
- Utilità di pianificazione elemento Monday
topic_type:
- apiref
api_name:
- Monday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3967db32a6ccd536e2e389e84de4eec05b333634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478166"
---
# <a name="monday-daysofweektype-element"></a><span data-ttu-id="60374-104">Elemento Monday (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="60374-104">Monday (daysOfWeekType) Element</span></span>

<span data-ttu-id="60374-105">Specifica che l'attività viene eseguita il lunedì.</span><span class="sxs-lookup"><span data-stu-id="60374-105">Specifies that the task runs on Monday.</span></span>

``` syntax
<xs:element name="Monday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="60374-106">L'elemento **Monday** è definito dal tipo complesso [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="60374-106">The **Monday** element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="60374-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="60374-107">Parent element</span></span>



| <span data-ttu-id="60374-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="60374-108">Element</span></span>                                                                                                                  | <span data-ttu-id="60374-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="60374-109">Derived from</span></span>                                                             | <span data-ttu-id="60374-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60374-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60374-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="60374-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="60374-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="60374-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="60374-113">Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione mensile giornaliera della settimana.</span><span class="sxs-lookup"><span data-stu-id="60374-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="60374-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="60374-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="60374-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="60374-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="60374-116">Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="60374-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="60374-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="60374-117">Examples</span></span>

<span data-ttu-id="60374-118">Il codice XML seguente definisce un calendario del giorno della settimana che avvia un'attività il lunedì.</span><span class="sxs-lookup"><span data-stu-id="60374-118">The following XML defines a day of week calendar that starts a task on Monday.</span></span>


```XML
<DaysOfWeek>
    <Monday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="60374-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60374-119">Requirements</span></span>



| <span data-ttu-id="60374-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="60374-120">Requirement</span></span> | <span data-ttu-id="60374-121">Valore</span><span class="sxs-lookup"><span data-stu-id="60374-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="60374-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60374-122">Minimum supported client</span></span><br/> | <span data-ttu-id="60374-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60374-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="60374-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60374-124">Minimum supported server</span></span><br/> | <span data-ttu-id="60374-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="60374-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60374-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60374-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60374-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="60374-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="60374-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="60374-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





