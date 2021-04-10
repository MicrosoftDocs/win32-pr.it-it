---
title: Elemento September (monthsType)
description: Specifica che l'attività viene eseguita nel settembre.
ms.assetid: b1ad2221-ca22-4808-bf20-ecf3cbb930f2
keywords:
- Utilità di pianificazione elemento di settembre
topic_type:
- apiref
api_name:
- September
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdd7e18ba9ae1cc7653589710fb9529281e84ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964822"
---
# <a name="september-monthstype-element"></a><span data-ttu-id="897f8-104">Elemento September (monthsType)</span><span class="sxs-lookup"><span data-stu-id="897f8-104">September (monthsType) Element</span></span>

<span data-ttu-id="897f8-105">Specifica che l'attività viene eseguita nel settembre.</span><span class="sxs-lookup"><span data-stu-id="897f8-105">Specifies that the task runs in September.</span></span>

``` syntax
<xs:element name="September">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="897f8-106">L'elemento di **settembre** è definito dal tipo complesso [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="897f8-106">The **September** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="897f8-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="897f8-107">Parent element</span></span>



| <span data-ttu-id="897f8-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="897f8-108">Element</span></span>                                                                                                          | <span data-ttu-id="897f8-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="897f8-109">Derived from</span></span>                                                     | <span data-ttu-id="897f8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="897f8-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="897f8-111">**Mesi (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="897f8-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="897f8-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="897f8-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="897f8-113">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="897f8-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="897f8-114">**Mesi (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="897f8-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="897f8-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="897f8-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="897f8-116">Specifica i mesi dell'anno durante i quali l'attività viene eseguita per una pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="897f8-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="897f8-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="897f8-117">Examples</span></span>

<span data-ttu-id="897f8-118">Il codice XML seguente definisce un calendario dei mesi che esegue l'attività a settembre.</span><span class="sxs-lookup"><span data-stu-id="897f8-118">The following XML defines a months calendar that runs the task in September.</span></span>


```XML
<Months>
    <September/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="897f8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="897f8-119">Requirements</span></span>



| <span data-ttu-id="897f8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="897f8-120">Requirement</span></span> | <span data-ttu-id="897f8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="897f8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="897f8-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="897f8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="897f8-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="897f8-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="897f8-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="897f8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="897f8-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="897f8-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="897f8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="897f8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="897f8-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="897f8-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="897f8-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="897f8-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





