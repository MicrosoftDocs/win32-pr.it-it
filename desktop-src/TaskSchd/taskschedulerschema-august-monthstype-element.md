---
title: Elemento August (monthsType)
description: Specifica che l'attività viene eseguita nell'agosto.
ms.assetid: cd7e528c-d482-4bb4-a31f-fccdb19a441b
keywords:
- Utilità di pianificazione elemento di agosto
topic_type:
- apiref
api_name:
- August
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4978ebd8f22da6e157461791c4c2000fce9db6ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874085"
---
# <a name="august-monthstype-element"></a><span data-ttu-id="d8a70-104">Elemento August (monthsType)</span><span class="sxs-lookup"><span data-stu-id="d8a70-104">August (monthsType) Element</span></span>

<span data-ttu-id="d8a70-105">Specifica che l'attività viene eseguita nell'agosto.</span><span class="sxs-lookup"><span data-stu-id="d8a70-105">Specifies that the task runs in August.</span></span>

``` syntax
<xs:element name="August">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="d8a70-106">L'elemento **agosto** è definito dal tipo complesso [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d8a70-106">The **August** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d8a70-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="d8a70-107">Parent element</span></span>



| <span data-ttu-id="d8a70-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d8a70-108">Element</span></span>                                                                                                          | <span data-ttu-id="d8a70-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="d8a70-109">Derived from</span></span>                                                     | <span data-ttu-id="d8a70-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8a70-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8a70-111">**Mesi (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="d8a70-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="d8a70-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="d8a70-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="d8a70-113">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="d8a70-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="d8a70-114">**Mesi (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="d8a70-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="d8a70-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="d8a70-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="d8a70-116">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="d8a70-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="d8a70-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="d8a70-117">Examples</span></span>

<span data-ttu-id="d8a70-118">Il codice XML seguente definisce un calendario dei mesi che esegue l'attività ad agosto.</span><span class="sxs-lookup"><span data-stu-id="d8a70-118">The following XML defines a months calendar that runs the task in August.</span></span>


```XML
<Months>
    <August/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="d8a70-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8a70-119">Requirements</span></span>



| <span data-ttu-id="d8a70-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8a70-120">Requirement</span></span> | <span data-ttu-id="d8a70-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d8a70-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d8a70-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8a70-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d8a70-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8a70-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d8a70-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8a70-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d8a70-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d8a70-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8a70-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8a70-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a70-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d8a70-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d8a70-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d8a70-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





