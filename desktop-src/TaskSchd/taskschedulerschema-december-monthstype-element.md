---
title: Elemento December (monthsType)
description: Specifica che l'attività viene eseguita nel dicembre.
ms.assetid: 42f3cfb2-8e82-46a0-b3ef-42e83d329124
keywords:
- Utilità di pianificazione elemento dicembre
topic_type:
- apiref
api_name:
- December
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c907262fe67a0529917d085583465eb97f94c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302697"
---
# <a name="december-monthstype-element"></a><span data-ttu-id="8a6b4-104">Elemento December (monthsType)</span><span class="sxs-lookup"><span data-stu-id="8a6b4-104">December (monthsType) Element</span></span>

<span data-ttu-id="8a6b4-105">Specifica che l'attività viene eseguita nel dicembre.</span><span class="sxs-lookup"><span data-stu-id="8a6b4-105">Specifies that the task runs in December.</span></span>

``` syntax
<xs:element name="December">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="8a6b4-106">L'elemento **December** è definito dal tipo complesso [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8a6b4-106">The **December** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8a6b4-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="8a6b4-107">Parent element</span></span>



| <span data-ttu-id="8a6b4-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8a6b4-108">Element</span></span>                                                                                                          | <span data-ttu-id="8a6b4-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="8a6b4-109">Derived from</span></span>                                                     | <span data-ttu-id="8a6b4-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a6b4-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a6b4-111">**Mesi (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="8a6b4-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="8a6b4-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="8a6b4-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="8a6b4-113">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="8a6b4-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="8a6b4-114">**Mesi (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="8a6b4-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="8a6b4-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="8a6b4-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="8a6b4-116">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="8a6b4-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="8a6b4-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="8a6b4-117">Examples</span></span>

<span data-ttu-id="8a6b4-118">Il codice XML seguente definisce un calendario dei mesi che esegue l'attività nel mese di dicembre.</span><span class="sxs-lookup"><span data-stu-id="8a6b4-118">The following XML defines a months calendar that runs the task in December.</span></span>


```XML
<Months>
    <December/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="8a6b4-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a6b4-119">Requirements</span></span>



| <span data-ttu-id="8a6b4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a6b4-120">Requirement</span></span> | <span data-ttu-id="8a6b4-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8a6b4-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8a6b4-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a6b4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8a6b4-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a6b4-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8a6b4-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a6b4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8a6b4-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a6b4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a6b4-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a6b4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a6b4-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8a6b4-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="8a6b4-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8a6b4-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





