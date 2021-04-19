---
title: Elemento week (weeksType)
description: Specifica una settimana specifica del mese.
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Utilità di pianificazione dell'elemento week
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0487aa07e1f1132c998b6cb2ba0f518a9db57ce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302483"
---
# <a name="week-weekstype-element"></a><span data-ttu-id="3fb90-104">Elemento week (weeksType)</span><span class="sxs-lookup"><span data-stu-id="3fb90-104">Week (weeksType) Element</span></span>

<span data-ttu-id="3fb90-105">Specifica una settimana specifica del mese.</span><span class="sxs-lookup"><span data-stu-id="3fb90-105">Specifies a specific week of the month.</span></span>

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

<span data-ttu-id="3fb90-106">L'elemento **week** è definito dal tipo complesso [**weeksType**](taskschedulerschema-weekstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3fb90-106">The **Week** element is defined by the [**weeksType**](taskschedulerschema-weekstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3fb90-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="3fb90-107">Parent element</span></span>



| <span data-ttu-id="3fb90-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3fb90-108">Element</span></span>                                                                                                        | <span data-ttu-id="3fb90-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="3fb90-109">Derived from</span></span>                                                   | <span data-ttu-id="3fb90-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fb90-110">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="3fb90-111">**Settimane (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="3fb90-111">**Weeks (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="3fb90-112">**weeksType**</span><span class="sxs-lookup"><span data-stu-id="3fb90-112">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md) | <span data-ttu-id="3fb90-113">Specifica le settimane del mese in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="3fb90-113">Specifies the weeks of the month in which the task is run.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3fb90-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fb90-114">Remarks</span></span>

<span data-ttu-id="3fb90-115">Quando si specificano le settimane del mese, utilizzare i numeri 1-4 per le prime quattro settimane del mese oppure utilizzare la stringa "ultimo" per indicare l'ultima settimana del mese.</span><span class="sxs-lookup"><span data-stu-id="3fb90-115">When specifying the weeks of the month, use the numbers 1-4 for the first four weeks of the month or use the string "Last" to indicate that last week of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb90-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fb90-116">Requirements</span></span>



| <span data-ttu-id="3fb90-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fb90-117">Requirement</span></span> | <span data-ttu-id="3fb90-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3fb90-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3fb90-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fb90-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb90-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fb90-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3fb90-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fb90-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb90-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3fb90-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3fb90-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fb90-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb90-124">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3fb90-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3fb90-125">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3fb90-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





