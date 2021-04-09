---
title: Elemento Sunday (daysOfWeekType)
description: Specifica che l'attività viene eseguita la domenica.
ms.assetid: 856db869-2273-4bb8-88c8-c126bb16c87b
keywords:
- Utilità di pianificazione dell'elemento Sunday
topic_type:
- apiref
api_name:
- Sunday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40efba31b392da5959853feeb1cae567cee25cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120886"
---
# <a name="sunday-daysofweektype-element"></a><span data-ttu-id="cfc42-104">Elemento Sunday (daysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="cfc42-104">Sunday (daysOfWeekType) Element</span></span>

<span data-ttu-id="cfc42-105">Specifica che l'attività viene eseguita la domenica.</span><span class="sxs-lookup"><span data-stu-id="cfc42-105">Specifies that the task runs on Sunday.</span></span>

``` syntax
<xs:element name="Sunday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="cfc42-106">L'elemento **Sunday** è definito dal tipo complesso [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cfc42-106">The **Sunday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cfc42-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="cfc42-107">Parent element</span></span>



| <span data-ttu-id="cfc42-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="cfc42-108">Element</span></span>                                                                                                                  | <span data-ttu-id="cfc42-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="cfc42-109">Derived from</span></span>                                                             | <span data-ttu-id="cfc42-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfc42-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cfc42-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="cfc42-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="cfc42-112">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="cfc42-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="cfc42-113">Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione mensile giornaliera della settimana.</span><span class="sxs-lookup"><span data-stu-id="cfc42-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="cfc42-114">**DaysOfWeek (weeklyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="cfc42-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="cfc42-115">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="cfc42-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="cfc42-116">Specifica i giorni della settimana in cui viene eseguita l'attività per una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="cfc42-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="cfc42-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="cfc42-117">Examples</span></span>

<span data-ttu-id="cfc42-118">Il codice XML seguente definisce un calendario del giorno della settimana che avvia un'attività la domenica.</span><span class="sxs-lookup"><span data-stu-id="cfc42-118">The following XML defines a day of week calendar that starts a task on Sunday.</span></span>


```XML
<DaysOfWeek>
    <Sunday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="cfc42-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfc42-119">Requirements</span></span>



| <span data-ttu-id="cfc42-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfc42-120">Requirement</span></span> | <span data-ttu-id="cfc42-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cfc42-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cfc42-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfc42-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cfc42-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cfc42-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cfc42-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfc42-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cfc42-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cfc42-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cfc42-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfc42-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfc42-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="cfc42-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="cfc42-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="cfc42-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





