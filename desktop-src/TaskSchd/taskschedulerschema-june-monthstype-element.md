---
title: Elemento June (monthsType)
description: Specifica che l'attività viene eseguita in giugno.
ms.assetid: 15b0e8c2-4dc1-4ca3-99c5-bd9a36718904
keywords:
- Utilità di pianificazione elemento di giugno
topic_type:
- apiref
api_name:
- June
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e6c21834348a70033af69a71534c60c1b08d91a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742423"
---
# <a name="june-monthstype-element"></a><span data-ttu-id="6ff2d-104">Elemento June (monthsType)</span><span class="sxs-lookup"><span data-stu-id="6ff2d-104">June (monthsType) Element</span></span>

<span data-ttu-id="6ff2d-105">Specifica che l'attività viene eseguita in giugno.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-105">Specifies that the task runs in June.</span></span>

``` syntax
<xs:element name="June">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="6ff2d-106">L'elemento **June** è definito dal tipo complesso [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6ff2d-106">The **June** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6ff2d-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="6ff2d-107">Parent element</span></span>



| <span data-ttu-id="6ff2d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6ff2d-108">Element</span></span>                                                                                                          | <span data-ttu-id="6ff2d-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="6ff2d-109">Derived from</span></span>                                                     | <span data-ttu-id="6ff2d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ff2d-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ff2d-111">**Mesi (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="6ff2d-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="6ff2d-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="6ff2d-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="6ff2d-113">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="6ff2d-114">**Mesi (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="6ff2d-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="6ff2d-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="6ff2d-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="6ff2d-116">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="6ff2d-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="6ff2d-117">Examples</span></span>

<span data-ttu-id="6ff2d-118">Il codice XML seguente definisce un calendario dei mesi che esegue l'attività nel mese di giugno.</span><span class="sxs-lookup"><span data-stu-id="6ff2d-118">The following XML defines a months calendar that runs the task in June.</span></span>


```XML
<Months>
    <June/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="6ff2d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ff2d-119">Requirements</span></span>



| <span data-ttu-id="6ff2d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ff2d-120">Requirement</span></span> | <span data-ttu-id="6ff2d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6ff2d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6ff2d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ff2d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6ff2d-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ff2d-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6ff2d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ff2d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6ff2d-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6ff2d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ff2d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ff2d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff2d-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="6ff2d-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6ff2d-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="6ff2d-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





