---
title: Tipo complesso monthlyDayOfWeekScheduleType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento ScheduleByMonthDayOfWeek.
ms.assetid: fb4e5ba3-592b-47a4-bedf-5181d2b7a50f
keywords:
- Utilità di pianificazione di tipo complesso monthlyDayOfWeekScheduleType
topic_type:
- apiref
api_name:
- monthlyDayOfWeekScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 782715aed5cbf59a98e996bfa18fdd7c1022227a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302221"
---
# <a name="monthlydayofweekscheduletype-complex-type"></a><span data-ttu-id="0617a-104">Tipo complesso monthlyDayOfWeekScheduleType</span><span class="sxs-lookup"><span data-stu-id="0617a-104">monthlyDayOfWeekScheduleType Complex Type</span></span>

<span data-ttu-id="0617a-105">Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0617a-105">Defines the child elements and sequencing information for the [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="monthlyDayOfWeekScheduleType">
    <xs:all>
        <xs:element name="Weeks"
            type="weeksType"
            minOccurs="0"
         />
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0617a-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0617a-106">Child elements</span></span>



| <span data-ttu-id="0617a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="0617a-107">Element</span></span>                                                                                   | <span data-ttu-id="0617a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0617a-108">Type</span></span>                                                                     | <span data-ttu-id="0617a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0617a-109">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="0617a-110">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="0617a-110">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="0617a-111">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="0617a-111">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="0617a-112">Specifica i giorni della settimana durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="0617a-112">Specifies the days of the week during which the task runs.</span></span><br/>   |
| [<span data-ttu-id="0617a-113">**Mesi**</span><span class="sxs-lookup"><span data-stu-id="0617a-113">**Months**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [<span data-ttu-id="0617a-114">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="0617a-114">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)         | <span data-ttu-id="0617a-115">Specifica i mesi dell'anno durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="0617a-115">Specifies the months of the year during which the task runs.</span></span><br/> |
| [<span data-ttu-id="0617a-116">**Settimane**</span><span class="sxs-lookup"><span data-stu-id="0617a-116">**Weeks**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | [<span data-ttu-id="0617a-117">**weeksType**</span><span class="sxs-lookup"><span data-stu-id="0617a-117">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md)           | <span data-ttu-id="0617a-118">Specifica le settimane del mese durante le quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="0617a-118">Specifies the weeks of the month during which the task runs.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0617a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0617a-119">Requirements</span></span>



| <span data-ttu-id="0617a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0617a-120">Requirement</span></span> | <span data-ttu-id="0617a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0617a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0617a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0617a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0617a-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0617a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0617a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0617a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0617a-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0617a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0617a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0617a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0617a-127">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0617a-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="0617a-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0617a-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





