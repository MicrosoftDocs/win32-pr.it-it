---
title: Proprietà WeeklyTrigger. DaysOfWeek
description: Per gli script, ottiene o imposta i giorni della settimana in cui viene eseguita l'attività.
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- Utilità di pianificazione proprietà DaysOfWeek
- Utilità di pianificazione proprietà DaysOfWeek, oggetto WeeklyTrigger
- Oggetto WeeklyTrigger Utilità di pianificazione, proprietà DaysOfWeek
topic_type:
- apiref
api_name:
- WeeklyTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f0a27ef031e7baf46d2d3c0e33c23fb505c7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519254"
---
# <a name="weeklytriggerdaysofweek-property"></a><span data-ttu-id="de5a6-106">Proprietà WeeklyTrigger. DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="de5a6-106">WeeklyTrigger.DaysOfWeek property</span></span>

<span data-ttu-id="de5a6-107">Per gli script, ottiene o imposta i giorni della settimana in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="de5a6-107">For scripting, gets or sets the days of the week on which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="de5a6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de5a6-108">Syntax</span></span>


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a><span data-ttu-id="de5a6-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="de5a6-109">Property value</span></span>

<span data-ttu-id="de5a6-110">Maschera bit per bit che indica i giorni della settimana in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="de5a6-110">A bitwise mask that indicates the days of the week on which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="de5a6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="de5a6-111">Remarks</span></span>

<span data-ttu-id="de5a6-112">Nella tabella seguente viene illustrato il mapping della maschera bit per bit utilizzata da questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="de5a6-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="de5a6-113">Month</span><span class="sxs-lookup"><span data-stu-id="de5a6-113">Month</span></span>     | <span data-ttu-id="de5a6-114">Valore hex</span><span class="sxs-lookup"><span data-stu-id="de5a6-114">Hex value</span></span> | <span data-ttu-id="de5a6-115">Valore decimale</span><span class="sxs-lookup"><span data-stu-id="de5a6-115">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="de5a6-116">Sunday</span><span class="sxs-lookup"><span data-stu-id="de5a6-116">Sunday</span></span>    | <span data-ttu-id="de5a6-117">0X01</span><span class="sxs-lookup"><span data-stu-id="de5a6-117">0X01</span></span>      | <span data-ttu-id="de5a6-118">1</span><span class="sxs-lookup"><span data-stu-id="de5a6-118">1</span></span>             |
| <span data-ttu-id="de5a6-119">Monday</span><span class="sxs-lookup"><span data-stu-id="de5a6-119">Monday</span></span>    | <span data-ttu-id="de5a6-120">0x02</span><span class="sxs-lookup"><span data-stu-id="de5a6-120">0x02</span></span>      | <span data-ttu-id="de5a6-121">2</span><span class="sxs-lookup"><span data-stu-id="de5a6-121">2</span></span>             |
| <span data-ttu-id="de5a6-122">Tuesday</span><span class="sxs-lookup"><span data-stu-id="de5a6-122">Tuesday</span></span>   | <span data-ttu-id="de5a6-123">0X04</span><span class="sxs-lookup"><span data-stu-id="de5a6-123">0X04</span></span>      | <span data-ttu-id="de5a6-124">4</span><span class="sxs-lookup"><span data-stu-id="de5a6-124">4</span></span>             |
| <span data-ttu-id="de5a6-125">Wednesday</span><span class="sxs-lookup"><span data-stu-id="de5a6-125">Wednesday</span></span> | <span data-ttu-id="de5a6-126">0X08</span><span class="sxs-lookup"><span data-stu-id="de5a6-126">0X08</span></span>      | <span data-ttu-id="de5a6-127">8</span><span class="sxs-lookup"><span data-stu-id="de5a6-127">8</span></span>             |
| <span data-ttu-id="de5a6-128">Thursday</span><span class="sxs-lookup"><span data-stu-id="de5a6-128">Thursday</span></span>  | <span data-ttu-id="de5a6-129">0X10</span><span class="sxs-lookup"><span data-stu-id="de5a6-129">0X10</span></span>      | <span data-ttu-id="de5a6-130">16</span><span class="sxs-lookup"><span data-stu-id="de5a6-130">16</span></span>            |
| <span data-ttu-id="de5a6-131">Friday</span><span class="sxs-lookup"><span data-stu-id="de5a6-131">Friday</span></span>    | <span data-ttu-id="de5a6-132">0x20</span><span class="sxs-lookup"><span data-stu-id="de5a6-132">0x20</span></span>      | <span data-ttu-id="de5a6-133">32</span><span class="sxs-lookup"><span data-stu-id="de5a6-133">32</span></span>            |
| <span data-ttu-id="de5a6-134">Sabato</span><span class="sxs-lookup"><span data-stu-id="de5a6-134">Saturday</span></span>  | <span data-ttu-id="de5a6-135">0X40</span><span class="sxs-lookup"><span data-stu-id="de5a6-135">0X40</span></span>      | <span data-ttu-id="de5a6-136">64</span><span class="sxs-lookup"><span data-stu-id="de5a6-136">64</span></span>            |



 

<span data-ttu-id="de5a6-137">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, i giorni della settimana vengono specificati utilizzando l'elemento [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="de5a6-137">When reading or writing your own XML for a task, the days of the week are specified using the [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="de5a6-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de5a6-138">Requirements</span></span>



| <span data-ttu-id="de5a6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="de5a6-139">Requirement</span></span> | <span data-ttu-id="de5a6-140">Valore</span><span class="sxs-lookup"><span data-stu-id="de5a6-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de5a6-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de5a6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="de5a6-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de5a6-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="de5a6-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de5a6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="de5a6-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de5a6-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="de5a6-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="de5a6-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="de5a6-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="de5a6-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="de5a6-147">DLL</span><span class="sxs-lookup"><span data-stu-id="de5a6-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de5a6-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de5a6-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de5a6-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de5a6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de5a6-150">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="de5a6-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





