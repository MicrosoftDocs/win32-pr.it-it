---
title: Proprietà MonthlyDOWTrigger. MonthsOfYear
description: Per gli script, ottiene o imposta i mesi dell'anno durante i quali viene eseguita l'attività. | Proprietà MonthlyDOWTrigger. MonthsOfYear
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- Utilità di pianificazione Proprietà MonthsOfYear
- Utilità di pianificazione Proprietà MonthsOfYear, oggetto MonthlyDOWTrigger
- Oggetto MonthlyDOWTrigger Utilità di pianificazione, Proprietà MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c345cd3de12d7dba3450f62bdb18bfdcee496b13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886217"
---
# <a name="monthlydowtriggermonthsofyear-property"></a><span data-ttu-id="2f85e-107">Proprietà MonthlyDOWTrigger. MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="2f85e-107">MonthlyDOWTrigger.MonthsOfYear property</span></span>

<span data-ttu-id="2f85e-108">Per gli script, ottiene o imposta i mesi dell'anno durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="2f85e-108">For scripting, gets or sets the months of the year during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f85e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f85e-109">Syntax</span></span>


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a><span data-ttu-id="2f85e-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2f85e-110">Property value</span></span>

<span data-ttu-id="2f85e-111">Maschera bit per bit che indica i mesi dell'anno durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="2f85e-111">A bitwise mask that indicates the months of the year during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f85e-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f85e-112">Remarks</span></span>

<span data-ttu-id="2f85e-113">Nella tabella seguente viene illustrato il mapping della maschera bit per bit utilizzata da questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="2f85e-113">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="2f85e-114">Month</span><span class="sxs-lookup"><span data-stu-id="2f85e-114">Month</span></span>     | <span data-ttu-id="2f85e-115">Valore hex</span><span class="sxs-lookup"><span data-stu-id="2f85e-115">Hex value</span></span> | <span data-ttu-id="2f85e-116">Valore decimale</span><span class="sxs-lookup"><span data-stu-id="2f85e-116">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="2f85e-117">January</span><span class="sxs-lookup"><span data-stu-id="2f85e-117">January</span></span>   | <span data-ttu-id="2f85e-118">0X01</span><span class="sxs-lookup"><span data-stu-id="2f85e-118">0X01</span></span>      | <span data-ttu-id="2f85e-119">1</span><span class="sxs-lookup"><span data-stu-id="2f85e-119">1</span></span>             |
| <span data-ttu-id="2f85e-120">Febbraio</span><span class="sxs-lookup"><span data-stu-id="2f85e-120">February</span></span>  | <span data-ttu-id="2f85e-121">0x02</span><span class="sxs-lookup"><span data-stu-id="2f85e-121">0x02</span></span>      | <span data-ttu-id="2f85e-122">2</span><span class="sxs-lookup"><span data-stu-id="2f85e-122">2</span></span>             |
| <span data-ttu-id="2f85e-123">Marzo</span><span class="sxs-lookup"><span data-stu-id="2f85e-123">March</span></span>     | <span data-ttu-id="2f85e-124">0X04</span><span class="sxs-lookup"><span data-stu-id="2f85e-124">0X04</span></span>      | <span data-ttu-id="2f85e-125">4</span><span class="sxs-lookup"><span data-stu-id="2f85e-125">4</span></span>             |
| <span data-ttu-id="2f85e-126">April</span><span class="sxs-lookup"><span data-stu-id="2f85e-126">April</span></span>     | <span data-ttu-id="2f85e-127">0X08</span><span class="sxs-lookup"><span data-stu-id="2f85e-127">0X08</span></span>      | <span data-ttu-id="2f85e-128">8</span><span class="sxs-lookup"><span data-stu-id="2f85e-128">8</span></span>             |
| <span data-ttu-id="2f85e-129">Mag</span><span class="sxs-lookup"><span data-stu-id="2f85e-129">May</span></span>       | <span data-ttu-id="2f85e-130">0X10</span><span class="sxs-lookup"><span data-stu-id="2f85e-130">0X10</span></span>      | <span data-ttu-id="2f85e-131">16</span><span class="sxs-lookup"><span data-stu-id="2f85e-131">16</span></span>            |
| <span data-ttu-id="2f85e-132">Giugno</span><span class="sxs-lookup"><span data-stu-id="2f85e-132">June</span></span>      | <span data-ttu-id="2f85e-133">0X20</span><span class="sxs-lookup"><span data-stu-id="2f85e-133">0X20</span></span>      | <span data-ttu-id="2f85e-134">32</span><span class="sxs-lookup"><span data-stu-id="2f85e-134">32</span></span>            |
| <span data-ttu-id="2f85e-135">Luglio</span><span class="sxs-lookup"><span data-stu-id="2f85e-135">July</span></span>      | <span data-ttu-id="2f85e-136">0x40</span><span class="sxs-lookup"><span data-stu-id="2f85e-136">0x40</span></span>      | <span data-ttu-id="2f85e-137">64</span><span class="sxs-lookup"><span data-stu-id="2f85e-137">64</span></span>            |
| <span data-ttu-id="2f85e-138">Agosto</span><span class="sxs-lookup"><span data-stu-id="2f85e-138">August</span></span>    | <span data-ttu-id="2f85e-139">0X80</span><span class="sxs-lookup"><span data-stu-id="2f85e-139">0X80</span></span>      | <span data-ttu-id="2f85e-140">128</span><span class="sxs-lookup"><span data-stu-id="2f85e-140">128</span></span>           |
| <span data-ttu-id="2f85e-141">Settembre</span><span class="sxs-lookup"><span data-stu-id="2f85e-141">September</span></span> | <span data-ttu-id="2f85e-142">0X100</span><span class="sxs-lookup"><span data-stu-id="2f85e-142">0X100</span></span>     | <span data-ttu-id="2f85e-143">256</span><span class="sxs-lookup"><span data-stu-id="2f85e-143">256</span></span>           |
| <span data-ttu-id="2f85e-144">Ottobre</span><span class="sxs-lookup"><span data-stu-id="2f85e-144">October</span></span>   | <span data-ttu-id="2f85e-145">0X200</span><span class="sxs-lookup"><span data-stu-id="2f85e-145">0X200</span></span>     | <span data-ttu-id="2f85e-146">512</span><span class="sxs-lookup"><span data-stu-id="2f85e-146">512</span></span>           |
| <span data-ttu-id="2f85e-147">Novembre</span><span class="sxs-lookup"><span data-stu-id="2f85e-147">November</span></span>  | <span data-ttu-id="2f85e-148">0X400</span><span class="sxs-lookup"><span data-stu-id="2f85e-148">0X400</span></span>     | <span data-ttu-id="2f85e-149">1024</span><span class="sxs-lookup"><span data-stu-id="2f85e-149">1024</span></span>          |
| <span data-ttu-id="2f85e-150">Dicembre</span><span class="sxs-lookup"><span data-stu-id="2f85e-150">December</span></span>  | <span data-ttu-id="2f85e-151">0X800</span><span class="sxs-lookup"><span data-stu-id="2f85e-151">0X800</span></span>     | <span data-ttu-id="2f85e-152">2048</span><span class="sxs-lookup"><span data-stu-id="2f85e-152">2048</span></span>          |



 

<span data-ttu-id="2f85e-153">Durante la lettura o la scrittura di codice XML per un'attività, i mesi dell'anno di un calendario giornaliero settimanale sono specificati dall'elemento [**months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="2f85e-153">When reading or writing XML for a task, the months of the year of a monthly day-of-week calendar are specified by the [**Months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f85e-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f85e-154">Requirements</span></span>



| <span data-ttu-id="2f85e-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f85e-155">Requirement</span></span> | <span data-ttu-id="2f85e-156">Valore</span><span class="sxs-lookup"><span data-stu-id="2f85e-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f85e-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f85e-157">Minimum supported client</span></span><br/> | <span data-ttu-id="2f85e-158">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2f85e-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2f85e-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f85e-159">Minimum supported server</span></span><br/> | <span data-ttu-id="2f85e-160">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2f85e-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f85e-161">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2f85e-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f85e-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2f85e-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2f85e-163">DLL</span><span class="sxs-lookup"><span data-stu-id="2f85e-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f85e-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f85e-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f85e-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f85e-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f85e-166">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="2f85e-166">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="2f85e-167">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="2f85e-167">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





