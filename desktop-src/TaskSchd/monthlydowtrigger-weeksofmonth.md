---
title: Proprietà MonthlyDOWTrigger. WeeksOfMonth
description: Per gli script, ottiene o imposta le settimane del mese durante le quali viene eseguita l'attività.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- Utilità di pianificazione proprietà WeeksOfMonth
- Utilità di pianificazione proprietà WeeksOfMonth, oggetto MonthlyDOWTrigger
- Oggetto MonthlyDOWTrigger Utilità di pianificazione, proprietà WeeksOfMonth
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7efea628e6eefdef07bdc50b9719a7c404f78bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475808"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a><span data-ttu-id="3f2ee-106">Proprietà MonthlyDOWTrigger. WeeksOfMonth</span><span class="sxs-lookup"><span data-stu-id="3f2ee-106">MonthlyDOWTrigger.WeeksOfMonth property</span></span>

<span data-ttu-id="3f2ee-107">Per gli script, ottiene o imposta le settimane del mese durante le quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="3f2ee-107">For scripting, gets or sets the weeks of the month during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f2ee-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f2ee-108">Syntax</span></span>


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a><span data-ttu-id="3f2ee-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3f2ee-109">Property value</span></span>

<span data-ttu-id="3f2ee-110">Maschera bit per bit che indica i giorni della settimana durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="3f2ee-110">A bitwise mask that indicates the days of the week during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f2ee-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f2ee-111">Remarks</span></span>

<span data-ttu-id="3f2ee-112">Nella tabella seguente viene illustrato il mapping della maschera bit per bit utilizzata da questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="3f2ee-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="3f2ee-113">Settimana</span><span class="sxs-lookup"><span data-stu-id="3f2ee-113">Week</span></span>                     | <span data-ttu-id="3f2ee-114">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="3f2ee-114">Hex Value</span></span> | <span data-ttu-id="3f2ee-115">Valore decimale</span><span class="sxs-lookup"><span data-stu-id="3f2ee-115">Decimal Value</span></span> |
|--------------------------|-----------|---------------|
| <span data-ttu-id="3f2ee-116">Prima settimana del mese</span><span class="sxs-lookup"><span data-stu-id="3f2ee-116">First week of the month</span></span>  | <span data-ttu-id="3f2ee-117">0X01</span><span class="sxs-lookup"><span data-stu-id="3f2ee-117">0X01</span></span>      | <span data-ttu-id="3f2ee-118">1</span><span class="sxs-lookup"><span data-stu-id="3f2ee-118">1</span></span>             |
| <span data-ttu-id="3f2ee-119">Seconda settimana del mese</span><span class="sxs-lookup"><span data-stu-id="3f2ee-119">Second week of the month</span></span> | <span data-ttu-id="3f2ee-120">0x02</span><span class="sxs-lookup"><span data-stu-id="3f2ee-120">0x02</span></span>      | <span data-ttu-id="3f2ee-121">2</span><span class="sxs-lookup"><span data-stu-id="3f2ee-121">2</span></span>             |
| <span data-ttu-id="3f2ee-122">Terza settimana del mese</span><span class="sxs-lookup"><span data-stu-id="3f2ee-122">Third week of the month</span></span>  | <span data-ttu-id="3f2ee-123">0X04</span><span class="sxs-lookup"><span data-stu-id="3f2ee-123">0X04</span></span>      | <span data-ttu-id="3f2ee-124">4</span><span class="sxs-lookup"><span data-stu-id="3f2ee-124">4</span></span>             |
| <span data-ttu-id="3f2ee-125">Quarta settimana del mese</span><span class="sxs-lookup"><span data-stu-id="3f2ee-125">Fourth week of the month</span></span> | <span data-ttu-id="3f2ee-126">0X08</span><span class="sxs-lookup"><span data-stu-id="3f2ee-126">0X08</span></span>      | <span data-ttu-id="3f2ee-127">8</span><span class="sxs-lookup"><span data-stu-id="3f2ee-127">8</span></span>             |



 

<span data-ttu-id="3f2ee-128">Durante la lettura o la scrittura di codice XML per un'attività, i giorni della settimana di un calendario giornaliero settimanale sono specificati dall'elemento [**weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3f2ee-128">When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**Weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f2ee-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f2ee-129">Requirements</span></span>



| <span data-ttu-id="3f2ee-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f2ee-130">Requirement</span></span> | <span data-ttu-id="3f2ee-131">Valore</span><span class="sxs-lookup"><span data-stu-id="3f2ee-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f2ee-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f2ee-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3f2ee-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f2ee-133">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3f2ee-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f2ee-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3f2ee-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f2ee-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f2ee-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3f2ee-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="3f2ee-137"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3f2ee-137"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3f2ee-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3f2ee-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f2ee-139"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f2ee-139"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f2ee-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f2ee-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f2ee-141">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="3f2ee-141">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="3f2ee-142">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3f2ee-142">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





