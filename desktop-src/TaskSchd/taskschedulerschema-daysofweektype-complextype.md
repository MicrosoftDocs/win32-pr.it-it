---
title: Tipo complesso daysOfWeekType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per gli elementi DaysOfWeek (weeklyScheduleType) e DaysOfWeek (monthlyDayOfWeekScheduleType).
ms.assetid: b3315582-af7a-4d4c-8f6f-61de12a85f46
keywords:
- Utilità di pianificazione di tipo complesso daysOfWeekType
topic_type:
- apiref
api_name:
- daysOfWeekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4a1b5e6aeaa77c0bdfe12b1d5b68fde018f236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341333"
---
# <a name="daysofweektype-complex-type"></a><span data-ttu-id="8dabc-104">Tipo complesso daysOfWeekType</span><span class="sxs-lookup"><span data-stu-id="8dabc-104">daysOfWeekType Complex Type</span></span>

<span data-ttu-id="8dabc-105">Definisce gli elementi figlio e le informazioni di sequenziazione per gli elementi [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) e [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8dabc-105">Defines the child elements and sequencing information for the [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) and [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) elements.</span></span>

``` syntax
<xs:complexType name="daysOfWeekType">
    <xs:all>
        <xs:element name="Monday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Tuesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Wednesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Thursday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Friday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Saturday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Sunday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8dabc-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8dabc-106">Child elements</span></span>



| <span data-ttu-id="8dabc-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="8dabc-107">Element</span></span>                                                                   | <span data-ttu-id="8dabc-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8dabc-108">Type</span></span> | <span data-ttu-id="8dabc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dabc-109">Description</span></span>                         |
|---------------------------------------------------------------------------|------|-------------------------------------|
| [<span data-ttu-id="8dabc-110">**Friday**</span><span class="sxs-lookup"><span data-stu-id="8dabc-110">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       | <span data-ttu-id="8dabc-111">N/D</span><span class="sxs-lookup"><span data-stu-id="8dabc-111">N/A</span></span>  | <span data-ttu-id="8dabc-112">L'attività viene eseguita il venerdì.</span><span class="sxs-lookup"><span data-stu-id="8dabc-112">Task runs on Friday.</span></span> <br/>    |
| [<span data-ttu-id="8dabc-113">**Monday**</span><span class="sxs-lookup"><span data-stu-id="8dabc-113">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       | <span data-ttu-id="8dabc-114">N/D</span><span class="sxs-lookup"><span data-stu-id="8dabc-114">N/A</span></span>  | <span data-ttu-id="8dabc-115">L'attività viene eseguita il lunedì.</span><span class="sxs-lookup"><span data-stu-id="8dabc-115">Task runs on Monday.</span></span><br/>     |
| [<span data-ttu-id="8dabc-116">**Sabato**</span><span class="sxs-lookup"><span data-stu-id="8dabc-116">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   | <span data-ttu-id="8dabc-117">N/D</span><span class="sxs-lookup"><span data-stu-id="8dabc-117">N/A</span></span>  | <span data-ttu-id="8dabc-118">L'attività viene eseguita il sabato.</span><span class="sxs-lookup"><span data-stu-id="8dabc-118">Task runs on Saturday.</span></span> <br/>  |
| [<span data-ttu-id="8dabc-119">**Sunday**</span><span class="sxs-lookup"><span data-stu-id="8dabc-119">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       | <span data-ttu-id="8dabc-120">N/D</span><span class="sxs-lookup"><span data-stu-id="8dabc-120">N/A</span></span>  | <span data-ttu-id="8dabc-121">L'attività viene eseguita la domenica.</span><span class="sxs-lookup"><span data-stu-id="8dabc-121">Task runs on Sunday.</span></span> <br/>    |
| [<span data-ttu-id="8dabc-122">**Thursday**</span><span class="sxs-lookup"><span data-stu-id="8dabc-122">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   | <span data-ttu-id="8dabc-123">N/D</span><span class="sxs-lookup"><span data-stu-id="8dabc-123">N/A</span></span>  | <span data-ttu-id="8dabc-124">Attività eseguita il giovedì</span><span class="sxs-lookup"><span data-stu-id="8dabc-124">Task runs on Thursday</span></span> <br/>   |
| [<span data-ttu-id="8dabc-125">**Tuesday**</span><span class="sxs-lookup"><span data-stu-id="8dabc-125">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     | <span data-ttu-id="8dabc-126">N/D</span><span class="sxs-lookup"><span data-stu-id="8dabc-126">N/A</span></span>  | <span data-ttu-id="8dabc-127">L'attività viene eseguita il martedì.</span><span class="sxs-lookup"><span data-stu-id="8dabc-127">Task runs on Tuesday.</span></span> <br/>   |
| [<span data-ttu-id="8dabc-128">**Wednesday**</span><span class="sxs-lookup"><span data-stu-id="8dabc-128">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) | <span data-ttu-id="8dabc-129">N/D</span><span class="sxs-lookup"><span data-stu-id="8dabc-129">N/A</span></span>  | <span data-ttu-id="8dabc-130">L'attività viene eseguita il mercoledì.</span><span class="sxs-lookup"><span data-stu-id="8dabc-130">Task runs on Wednesday.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="8dabc-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8dabc-131">Requirements</span></span>



| <span data-ttu-id="8dabc-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dabc-132">Requirement</span></span> | <span data-ttu-id="8dabc-133">Valore</span><span class="sxs-lookup"><span data-stu-id="8dabc-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8dabc-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8dabc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8dabc-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8dabc-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8dabc-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8dabc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8dabc-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8dabc-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8dabc-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8dabc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dabc-139">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8dabc-139">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="8dabc-140">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8dabc-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





