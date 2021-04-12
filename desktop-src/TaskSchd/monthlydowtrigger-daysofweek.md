---
title: Proprietà MonthlyDOWTrigger. DaysOfWeek
description: Per gli script, ottiene o imposta i giorni della settimana durante i quali viene eseguita l'attività.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- Utilità di pianificazione proprietà DaysOfWeek
- Utilità di pianificazione proprietà DaysOfWeek, oggetto MonthlyDOWTrigger
- Oggetto MonthlyDOWTrigger Utilità di pianificazione, proprietà DaysOfWeek
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15344650dabdec2bcbacf91397b37b97ce3f0772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478418"
---
# <a name="monthlydowtriggerdaysofweek-property"></a><span data-ttu-id="5dbc9-106">Proprietà MonthlyDOWTrigger. DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="5dbc9-106">MonthlyDOWTrigger.DaysOfWeek property</span></span>

<span data-ttu-id="5dbc9-107">Per gli script, ottiene o imposta i giorni della settimana durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="5dbc9-107">For scripting, gets or sets the days of the week during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dbc9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5dbc9-108">Syntax</span></span>


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a><span data-ttu-id="5dbc9-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5dbc9-109">Property value</span></span>

<span data-ttu-id="5dbc9-110">Maschera bit per bit che indica i giorni della settimana durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="5dbc9-110">A bitwise mask that indicates the days of the week during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dbc9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5dbc9-111">Remarks</span></span>

<span data-ttu-id="5dbc9-112">Nella tabella seguente viene illustrato il mapping della maschera bit per bit utilizzata da questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5dbc9-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="5dbc9-113">Giorno della settimana</span><span class="sxs-lookup"><span data-stu-id="5dbc9-113">Day of Week</span></span> | <span data-ttu-id="5dbc9-114">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="5dbc9-114">Hex Value</span></span> | <span data-ttu-id="5dbc9-115">Valore decimale</span><span class="sxs-lookup"><span data-stu-id="5dbc9-115">Decimal Value</span></span> |
|-------------|-----------|---------------|
| <span data-ttu-id="5dbc9-116">Sunday</span><span class="sxs-lookup"><span data-stu-id="5dbc9-116">Sunday</span></span>      | <span data-ttu-id="5dbc9-117">0x01</span><span class="sxs-lookup"><span data-stu-id="5dbc9-117">0x01</span></span>      | <span data-ttu-id="5dbc9-118">1</span><span class="sxs-lookup"><span data-stu-id="5dbc9-118">1</span></span>             |
| <span data-ttu-id="5dbc9-119">Monday</span><span class="sxs-lookup"><span data-stu-id="5dbc9-119">Monday</span></span>      | <span data-ttu-id="5dbc9-120">0x02</span><span class="sxs-lookup"><span data-stu-id="5dbc9-120">0x02</span></span>      | <span data-ttu-id="5dbc9-121">2</span><span class="sxs-lookup"><span data-stu-id="5dbc9-121">2</span></span>             |
| <span data-ttu-id="5dbc9-122">Tuesday</span><span class="sxs-lookup"><span data-stu-id="5dbc9-122">Tuesday</span></span>     | <span data-ttu-id="5dbc9-123">0x04</span><span class="sxs-lookup"><span data-stu-id="5dbc9-123">0x04</span></span>      | <span data-ttu-id="5dbc9-124">4</span><span class="sxs-lookup"><span data-stu-id="5dbc9-124">4</span></span>             |
| <span data-ttu-id="5dbc9-125">Wednesday</span><span class="sxs-lookup"><span data-stu-id="5dbc9-125">Wednesday</span></span>   | <span data-ttu-id="5dbc9-126">0x08</span><span class="sxs-lookup"><span data-stu-id="5dbc9-126">0x08</span></span>      | <span data-ttu-id="5dbc9-127">8</span><span class="sxs-lookup"><span data-stu-id="5dbc9-127">8</span></span>             |
| <span data-ttu-id="5dbc9-128">Thursday</span><span class="sxs-lookup"><span data-stu-id="5dbc9-128">Thursday</span></span>    | <span data-ttu-id="5dbc9-129">0x10</span><span class="sxs-lookup"><span data-stu-id="5dbc9-129">0x10</span></span>      | <span data-ttu-id="5dbc9-130">16</span><span class="sxs-lookup"><span data-stu-id="5dbc9-130">16</span></span>            |
| <span data-ttu-id="5dbc9-131">Friday</span><span class="sxs-lookup"><span data-stu-id="5dbc9-131">Friday</span></span>      | <span data-ttu-id="5dbc9-132">0x20</span><span class="sxs-lookup"><span data-stu-id="5dbc9-132">0x20</span></span>      | <span data-ttu-id="5dbc9-133">32</span><span class="sxs-lookup"><span data-stu-id="5dbc9-133">32</span></span>            |
| <span data-ttu-id="5dbc9-134">Sabato</span><span class="sxs-lookup"><span data-stu-id="5dbc9-134">Saturday</span></span>    | <span data-ttu-id="5dbc9-135">0x40</span><span class="sxs-lookup"><span data-stu-id="5dbc9-135">0x40</span></span>      | <span data-ttu-id="5dbc9-136">64</span><span class="sxs-lookup"><span data-stu-id="5dbc9-136">64</span></span>            |



 

<span data-ttu-id="5dbc9-137">Durante la lettura o la scrittura di codice XML per un'attività, i giorni della settimana di un calendario giornaliero settimanale sono specificati dall'elemento [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5dbc9-137">When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dbc9-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5dbc9-138">Requirements</span></span>



| <span data-ttu-id="5dbc9-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dbc9-139">Requirement</span></span> | <span data-ttu-id="5dbc9-140">Valore</span><span class="sxs-lookup"><span data-stu-id="5dbc9-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dbc9-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5dbc9-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5dbc9-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5dbc9-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5dbc9-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5dbc9-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5dbc9-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5dbc9-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5dbc9-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5dbc9-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="5dbc9-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5dbc9-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5dbc9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="5dbc9-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dbc9-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dbc9-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dbc9-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5dbc9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dbc9-150">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="5dbc9-150">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="5dbc9-151">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5dbc9-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





