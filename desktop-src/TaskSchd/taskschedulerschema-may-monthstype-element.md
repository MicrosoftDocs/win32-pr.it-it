---
title: Elemento May (monthsType)
description: Specifica che l'attività viene eseguita in May.
ms.assetid: 1fcc3eb7-6500-4ba3-b146-14d169d9b445
keywords:
- Utilità di pianificazione dell'elemento May
topic_type:
- apiref
api_name:
- May
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d3f0c107124aa2c87672f63a469857f3795e13c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302166"
---
# <a name="may-monthstype-element"></a><span data-ttu-id="a919a-104">Elemento May (monthsType)</span><span class="sxs-lookup"><span data-stu-id="a919a-104">May (monthsType) Element</span></span>

<span data-ttu-id="a919a-105">Specifica che l'attività viene eseguita in May.</span><span class="sxs-lookup"><span data-stu-id="a919a-105">Specifies that the task runs in May.</span></span>

``` syntax
<xs:element name="May">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="a919a-106">L'elemento **può** essere definito dal tipo complesso [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a919a-106">The **May** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a919a-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="a919a-107">Parent element</span></span>



| <span data-ttu-id="a919a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a919a-108">Element</span></span>                                                                                                          | <span data-ttu-id="a919a-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="a919a-109">Derived from</span></span>                                                     | <span data-ttu-id="a919a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a919a-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a919a-111">**Mesi (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="a919a-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="a919a-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="a919a-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="a919a-113">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="a919a-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="a919a-114">**Mesi (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="a919a-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="a919a-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="a919a-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="a919a-116">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="a919a-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="a919a-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="a919a-117">Examples</span></span>

<span data-ttu-id="a919a-118">Il codice XML seguente definisce un calendario dei mesi che esegue l'attività in May.</span><span class="sxs-lookup"><span data-stu-id="a919a-118">The following XML defines a months calendar that runs the task in May.</span></span>


```XML
<Months>
    <May/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="a919a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a919a-119">Requirements</span></span>



| <span data-ttu-id="a919a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a919a-120">Requirement</span></span> | <span data-ttu-id="a919a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a919a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a919a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a919a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a919a-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a919a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a919a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a919a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a919a-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a919a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a919a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a919a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a919a-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="a919a-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a919a-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="a919a-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





