---
title: Tipo complesso monthsType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per gli elementi months (monthlyDayOfWeekScheduleType) e months (monthlyScheduleType).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- Utilità di pianificazione di tipo complesso monthsType
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6a19000073fd12e05aa915921850264979a0541
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740439"
---
# <a name="monthstype-complex-type"></a><span data-ttu-id="f6b28-104">Tipo complesso monthsType</span><span class="sxs-lookup"><span data-stu-id="f6b28-104">monthsType Complex Type</span></span>

<span data-ttu-id="f6b28-105">Definisce gli elementi figlio e le informazioni di sequenziazione per gli elementi [**months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) e [**months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f6b28-105">Defines the child elements and sequencing information for the [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) and [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) elements.</span></span>

``` syntax
<xs:complexType name="monthsType">
    <xs:all>
        <xs:element name="January"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="February"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="March"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="April"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="May"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="June"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="July"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="August"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="September"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="October"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="November"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="December"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f6b28-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f6b28-106">Child elements</span></span>



| <span data-ttu-id="f6b28-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f6b28-107">Element</span></span>                                                               | <span data-ttu-id="f6b28-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6b28-108">Type</span></span> | <span data-ttu-id="f6b28-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6b28-109">Description</span></span>                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [<span data-ttu-id="f6b28-110">**Aprile**</span><span class="sxs-lookup"><span data-stu-id="f6b28-110">**April**</span></span>](taskschedulerschema-april-monthstype-element.md)         | <span data-ttu-id="f6b28-111">N/D</span><span class="sxs-lookup"><span data-stu-id="f6b28-111">N/A</span></span>  | <span data-ttu-id="f6b28-112">Specifica che l'attività viene eseguita nell'aprile.</span><span class="sxs-lookup"><span data-stu-id="f6b28-112">Specifies that the task runs in April.</span></span> <br/>     |
| [<span data-ttu-id="f6b28-113">**Agosto**</span><span class="sxs-lookup"><span data-stu-id="f6b28-113">**August**</span></span>](taskschedulerschema-august-monthstype-element.md)       | <span data-ttu-id="f6b28-114">N/D</span><span class="sxs-lookup"><span data-stu-id="f6b28-114">N/A</span></span>  | <span data-ttu-id="f6b28-115">Specifica che l'attività viene eseguita nell'agosto.</span><span class="sxs-lookup"><span data-stu-id="f6b28-115">Specifies that the task runs in August.</span></span> <br/>    |
| [<span data-ttu-id="f6b28-116">**Dicembre**</span><span class="sxs-lookup"><span data-stu-id="f6b28-116">**December**</span></span>](taskschedulerschema-december-monthstype-element.md)   | <span data-ttu-id="f6b28-117">N/D</span><span class="sxs-lookup"><span data-stu-id="f6b28-117">N/A</span></span>  | <span data-ttu-id="f6b28-118">Specifica che l'attività viene eseguita nel dicembre.</span><span class="sxs-lookup"><span data-stu-id="f6b28-118">Specifies that the task runs in December.</span></span> <br/>  |
| [<span data-ttu-id="f6b28-119">**Febbraio**</span><span class="sxs-lookup"><span data-stu-id="f6b28-119">**February**</span></span>](taskschedulerschema-february-monthstype-element.md)   | <span data-ttu-id="f6b28-120">N/D</span><span class="sxs-lookup"><span data-stu-id="f6b28-120">N/A</span></span>  | <span data-ttu-id="f6b28-121">Specifica che l'attività viene eseguita nel febbraio.</span><span class="sxs-lookup"><span data-stu-id="f6b28-121">Specifies that the task runs in February.</span></span> <br/>  |
| [<span data-ttu-id="f6b28-122">**Gennaio**</span><span class="sxs-lookup"><span data-stu-id="f6b28-122">**January**</span></span>](taskschedulerschema-january-monthstype-element.md)     | <span data-ttu-id="f6b28-123">N/D</span><span class="sxs-lookup"><span data-stu-id="f6b28-123">N/A</span></span>  | <span data-ttu-id="f6b28-124">Specifica che l'attività viene eseguita nel gennaio.</span><span class="sxs-lookup"><span data-stu-id="f6b28-124">Specifies that the task runs in January.</span></span> <br/>   |
| [<span data-ttu-id="f6b28-125">**Luglio**</span><span class="sxs-lookup"><span data-stu-id="f6b28-125">**July**</span></span>](taskschedulerschema-july-monthstype-element.md)           | <span data-ttu-id="f6b28-126">N/D</span><span class="sxs-lookup"><span data-stu-id="f6b28-126">N/A</span></span>  | <span data-ttu-id="f6b28-127">Specifica che l'attività viene eseguita nel luglio.</span><span class="sxs-lookup"><span data-stu-id="f6b28-127">Specifies that the task runs in July.</span></span> <br/>      |
| [<span data-ttu-id="f6b28-128">**Giugno**</span><span class="sxs-lookup"><span data-stu-id="f6b28-128">**June**</span></span>](taskschedulerschema-june-monthstype-element.md)           | <span data-ttu-id="f6b28-129">N/D</span><span class="sxs-lookup"><span data-stu-id="f6b28-129">N/A</span></span>  | <span data-ttu-id="f6b28-130">Specifica che l'attività viene eseguita in giugno.</span><span class="sxs-lookup"><span data-stu-id="f6b28-130">Specifies that the task runs in June.</span></span> <br/>      |
| [<span data-ttu-id="f6b28-131">**Marzo**</span><span class="sxs-lookup"><span data-stu-id="f6b28-131">**March**</span></span>](taskschedulerschema-march-monthstype-element.md)         | <span data-ttu-id="f6b28-132">N/D</span><span class="sxs-lookup"><span data-stu-id="f6b28-132">N/A</span></span>  | <span data-ttu-id="f6b28-133">Specifica che l'attività viene eseguita nel marzo.</span><span class="sxs-lookup"><span data-stu-id="f6b28-133">Specifies that the task runs in March.</span></span> <br/>     |
| [<span data-ttu-id="f6b28-134">**Mag**</span><span class="sxs-lookup"><span data-stu-id="f6b28-134">**May**</span></span>](taskschedulerschema-may-monthstype-element.md)             | <span data-ttu-id="f6b28-135">N/D</span><span class="sxs-lookup"><span data-stu-id="f6b28-135">N/A</span></span>  | <span data-ttu-id="f6b28-136">Specifica che l'attività viene eseguita in May.</span><span class="sxs-lookup"><span data-stu-id="f6b28-136">Specifies that the task runs in May.</span></span> <br/>       |
| [<span data-ttu-id="f6b28-137">**Novembre**</span><span class="sxs-lookup"><span data-stu-id="f6b28-137">**November**</span></span>](taskschedulerschema-november-monthstype-element.md)   | <span data-ttu-id="f6b28-138">N/D</span><span class="sxs-lookup"><span data-stu-id="f6b28-138">N/A</span></span>  | <span data-ttu-id="f6b28-139">Specifica che l'attività viene eseguita nel novembre.</span><span class="sxs-lookup"><span data-stu-id="f6b28-139">Specifies that the task runs in November.</span></span> <br/>  |
| [<span data-ttu-id="f6b28-140">**Ottobre**</span><span class="sxs-lookup"><span data-stu-id="f6b28-140">**October**</span></span>](taskschedulerschema-october-monthstype-element.md)     | <span data-ttu-id="f6b28-141">N/D</span><span class="sxs-lookup"><span data-stu-id="f6b28-141">N/A</span></span>  | <span data-ttu-id="f6b28-142">Specifica che l'attività viene eseguita nel ottobre.</span><span class="sxs-lookup"><span data-stu-id="f6b28-142">Specifies that the task runs in October.</span></span> <br/>   |
| [<span data-ttu-id="f6b28-143">**Settembre**</span><span class="sxs-lookup"><span data-stu-id="f6b28-143">**September**</span></span>](taskschedulerschema-september-monthstype-element.md) | <span data-ttu-id="f6b28-144">N/D</span><span class="sxs-lookup"><span data-stu-id="f6b28-144">N/A</span></span>  | <span data-ttu-id="f6b28-145">Specifica che l'attività viene eseguita nel settembre.</span><span class="sxs-lookup"><span data-stu-id="f6b28-145">Specifies that the task runs in September.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="f6b28-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6b28-146">Requirements</span></span>



| <span data-ttu-id="f6b28-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6b28-147">Requirement</span></span> | <span data-ttu-id="f6b28-148">Valore</span><span class="sxs-lookup"><span data-stu-id="f6b28-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f6b28-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6b28-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f6b28-150">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6b28-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f6b28-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6b28-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f6b28-152">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f6b28-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6b28-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6b28-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6b28-154">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f6b28-154">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="f6b28-155">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f6b28-155">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





