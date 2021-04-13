---
title: Elemento March (monthsType)
description: Specifica che l'attività viene eseguita nel marzo.
ms.assetid: 0cd82405-8e17-483d-88ba-32cae590f6b3
keywords:
- Utilità di pianificazione elemento di marzo
topic_type:
- apiref
api_name:
- March
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bf6792cf65ab3aecb74bff82282daa0d8fb2bdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340942"
---
# <a name="march-monthstype-element"></a><span data-ttu-id="4550a-104">Elemento March (monthsType)</span><span class="sxs-lookup"><span data-stu-id="4550a-104">March (monthsType) Element</span></span>

<span data-ttu-id="4550a-105">Specifica che l'attività viene eseguita nel marzo.</span><span class="sxs-lookup"><span data-stu-id="4550a-105">Specifies that the task runs in March.</span></span>

``` syntax
<xs:element name="March">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="4550a-106">L'elemento di **marzo** è definito dal tipo complesso [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4550a-106">The **March** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4550a-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="4550a-107">Parent element</span></span>



| <span data-ttu-id="4550a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4550a-108">Element</span></span>                                                                                                          | <span data-ttu-id="4550a-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="4550a-109">Derived from</span></span>                                                     | <span data-ttu-id="4550a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4550a-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4550a-111">**Mesi (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="4550a-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="4550a-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="4550a-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="4550a-113">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="4550a-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="4550a-114">**Mesi (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="4550a-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="4550a-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="4550a-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="4550a-116">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="4550a-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="4550a-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="4550a-117">Examples</span></span>

<span data-ttu-id="4550a-118">Il codice XML seguente definisce un calendario dei mesi che esegue l'attività a marzo.</span><span class="sxs-lookup"><span data-stu-id="4550a-118">The following XML defines a months calendar that runs the task in March.</span></span>


```XML
<Months>
    <March/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="4550a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4550a-119">Requirements</span></span>



| <span data-ttu-id="4550a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4550a-120">Requirement</span></span> | <span data-ttu-id="4550a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4550a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4550a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4550a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4550a-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4550a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4550a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4550a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4550a-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4550a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4550a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4550a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4550a-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="4550a-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="4550a-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="4550a-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





