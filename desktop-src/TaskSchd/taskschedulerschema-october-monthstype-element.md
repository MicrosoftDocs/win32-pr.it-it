---
title: Elemento ottobre (monthsType)
description: Specifica che l'attività viene eseguita nel ottobre.
ms.assetid: 62c8bb3e-a70f-45b8-8d80-7a7eef9dfaeb
keywords:
- Utilità di pianificazione elemento di ottobre
topic_type:
- apiref
api_name:
- October
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79bf2a2dde46341f48808342ab6aefb78863524b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121558"
---
# <a name="october-monthstype-element"></a><span data-ttu-id="9dc49-104">Elemento ottobre (monthsType)</span><span class="sxs-lookup"><span data-stu-id="9dc49-104">October (monthsType) Element</span></span>

<span data-ttu-id="9dc49-105">Specifica che l'attività viene eseguita nel ottobre.</span><span class="sxs-lookup"><span data-stu-id="9dc49-105">Specifies that the task runs in October.</span></span>

``` syntax
<xs:element name="October">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="9dc49-106">L'elemento **ottobre** è definito dal tipo complesso [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9dc49-106">The **October** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9dc49-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="9dc49-107">Parent element</span></span>



| <span data-ttu-id="9dc49-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9dc49-108">Element</span></span>                                                                                                          | <span data-ttu-id="9dc49-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="9dc49-109">Derived from</span></span>                                                     | <span data-ttu-id="9dc49-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9dc49-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9dc49-111">**Mesi (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="9dc49-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="9dc49-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="9dc49-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="9dc49-113">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="9dc49-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="9dc49-114">**Mesi (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="9dc49-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="9dc49-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="9dc49-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="9dc49-116">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="9dc49-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="9dc49-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="9dc49-117">Examples</span></span>

<span data-ttu-id="9dc49-118">Nel codice XML seguente viene definito un calendario dei mesi che esegue l'attività nel mese di ottobre.</span><span class="sxs-lookup"><span data-stu-id="9dc49-118">The following XML defines a months calendar that runs the task in October.</span></span>


```XML
<Months>
    <October/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="9dc49-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9dc49-119">Requirements</span></span>



| <span data-ttu-id="9dc49-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dc49-120">Requirement</span></span> | <span data-ttu-id="9dc49-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9dc49-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9dc49-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dc49-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9dc49-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9dc49-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9dc49-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dc49-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9dc49-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9dc49-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9dc49-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9dc49-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dc49-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="9dc49-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9dc49-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="9dc49-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





