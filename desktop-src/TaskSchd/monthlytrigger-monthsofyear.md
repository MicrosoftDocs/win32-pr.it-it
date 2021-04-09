---
title: Proprietà MonthlyTrigger. MonthsOfYear
description: Per gli script, ottiene o imposta i mesi dell'anno durante i quali viene eseguita l'attività. | Proprietà MonthlyTrigger. MonthsOfYear
ms.assetid: cf26a815-7f4f-4b7a-8db8-a4bd9b77cf49
keywords:
- Utilità di pianificazione Proprietà MonthsOfYear
- Utilità di pianificazione Proprietà MonthsOfYear, oggetto MonthlyTrigger
- Oggetto MonthlyTrigger Utilità di pianificazione, Proprietà MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5683fb1c85e470ca7c82b069929de0351ea7cffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886167"
---
# <a name="monthlytriggermonthsofyear-property"></a><span data-ttu-id="06f54-107">Proprietà MonthlyTrigger. MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="06f54-107">MonthlyTrigger.MonthsOfYear property</span></span>

<span data-ttu-id="06f54-108">Per gli script, ottiene o imposta i mesi dell'anno durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="06f54-108">For scripting, gets or sets the months of the year during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="06f54-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06f54-109">Syntax</span></span>


```VB
MonthlyTrigger.MonthsOfYear As short
```



## <a name="property-value"></a><span data-ttu-id="06f54-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="06f54-110">Property value</span></span>

<span data-ttu-id="06f54-111">Maschera bit per bit che indica i mesi dell'anno durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="06f54-111">A bitwise mask that indicates the months of the year during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="06f54-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="06f54-112">Remarks</span></span>

<span data-ttu-id="06f54-113">Nella tabella seguente viene illustrato il mapping della maschera bit per bit utilizzata da questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="06f54-113">The following table shows the mapping of the bitwise mask that is used by this property.</span></span>



| <span data-ttu-id="06f54-114">Month</span><span class="sxs-lookup"><span data-stu-id="06f54-114">Month</span></span>     | <span data-ttu-id="06f54-115">Valore hex</span><span class="sxs-lookup"><span data-stu-id="06f54-115">Hex value</span></span> | <span data-ttu-id="06f54-116">Valore decimale</span><span class="sxs-lookup"><span data-stu-id="06f54-116">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="06f54-117">January</span><span class="sxs-lookup"><span data-stu-id="06f54-117">January</span></span>   | <span data-ttu-id="06f54-118">0X01</span><span class="sxs-lookup"><span data-stu-id="06f54-118">0X01</span></span>      | <span data-ttu-id="06f54-119">1</span><span class="sxs-lookup"><span data-stu-id="06f54-119">1</span></span>             |
| <span data-ttu-id="06f54-120">Febbraio</span><span class="sxs-lookup"><span data-stu-id="06f54-120">February</span></span>  | <span data-ttu-id="06f54-121">0x02</span><span class="sxs-lookup"><span data-stu-id="06f54-121">0x02</span></span>      | <span data-ttu-id="06f54-122">2</span><span class="sxs-lookup"><span data-stu-id="06f54-122">2</span></span>             |
| <span data-ttu-id="06f54-123">Marzo</span><span class="sxs-lookup"><span data-stu-id="06f54-123">March</span></span>     | <span data-ttu-id="06f54-124">0X04</span><span class="sxs-lookup"><span data-stu-id="06f54-124">0X04</span></span>      | <span data-ttu-id="06f54-125">4</span><span class="sxs-lookup"><span data-stu-id="06f54-125">4</span></span>             |
| <span data-ttu-id="06f54-126">April</span><span class="sxs-lookup"><span data-stu-id="06f54-126">April</span></span>     | <span data-ttu-id="06f54-127">0X08</span><span class="sxs-lookup"><span data-stu-id="06f54-127">0X08</span></span>      | <span data-ttu-id="06f54-128">8</span><span class="sxs-lookup"><span data-stu-id="06f54-128">8</span></span>             |
| <span data-ttu-id="06f54-129">Mag</span><span class="sxs-lookup"><span data-stu-id="06f54-129">May</span></span>       | <span data-ttu-id="06f54-130">0X10</span><span class="sxs-lookup"><span data-stu-id="06f54-130">0X10</span></span>      | <span data-ttu-id="06f54-131">16</span><span class="sxs-lookup"><span data-stu-id="06f54-131">16</span></span>            |
| <span data-ttu-id="06f54-132">Giugno</span><span class="sxs-lookup"><span data-stu-id="06f54-132">June</span></span>      | <span data-ttu-id="06f54-133">0X20</span><span class="sxs-lookup"><span data-stu-id="06f54-133">0X20</span></span>      | <span data-ttu-id="06f54-134">32</span><span class="sxs-lookup"><span data-stu-id="06f54-134">32</span></span>            |
| <span data-ttu-id="06f54-135">Luglio</span><span class="sxs-lookup"><span data-stu-id="06f54-135">July</span></span>      | <span data-ttu-id="06f54-136">0x40</span><span class="sxs-lookup"><span data-stu-id="06f54-136">0x40</span></span>      | <span data-ttu-id="06f54-137">64</span><span class="sxs-lookup"><span data-stu-id="06f54-137">64</span></span>            |
| <span data-ttu-id="06f54-138">Agosto</span><span class="sxs-lookup"><span data-stu-id="06f54-138">August</span></span>    | <span data-ttu-id="06f54-139">0X80</span><span class="sxs-lookup"><span data-stu-id="06f54-139">0X80</span></span>      | <span data-ttu-id="06f54-140">128</span><span class="sxs-lookup"><span data-stu-id="06f54-140">128</span></span>           |
| <span data-ttu-id="06f54-141">Settembre</span><span class="sxs-lookup"><span data-stu-id="06f54-141">September</span></span> | <span data-ttu-id="06f54-142">0X100</span><span class="sxs-lookup"><span data-stu-id="06f54-142">0X100</span></span>     | <span data-ttu-id="06f54-143">256</span><span class="sxs-lookup"><span data-stu-id="06f54-143">256</span></span>           |
| <span data-ttu-id="06f54-144">Ottobre</span><span class="sxs-lookup"><span data-stu-id="06f54-144">October</span></span>   | <span data-ttu-id="06f54-145">0X200</span><span class="sxs-lookup"><span data-stu-id="06f54-145">0X200</span></span>     | <span data-ttu-id="06f54-146">512</span><span class="sxs-lookup"><span data-stu-id="06f54-146">512</span></span>           |
| <span data-ttu-id="06f54-147">Novembre</span><span class="sxs-lookup"><span data-stu-id="06f54-147">November</span></span>  | <span data-ttu-id="06f54-148">0X400</span><span class="sxs-lookup"><span data-stu-id="06f54-148">0X400</span></span>     | <span data-ttu-id="06f54-149">1024</span><span class="sxs-lookup"><span data-stu-id="06f54-149">1024</span></span>          |
| <span data-ttu-id="06f54-150">Dicembre</span><span class="sxs-lookup"><span data-stu-id="06f54-150">December</span></span>  | <span data-ttu-id="06f54-151">0X800</span><span class="sxs-lookup"><span data-stu-id="06f54-151">0X800</span></span>     | <span data-ttu-id="06f54-152">2048</span><span class="sxs-lookup"><span data-stu-id="06f54-152">2048</span></span>          |



 

<span data-ttu-id="06f54-153">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, i mesi dell'anno vengono specificati utilizzando l'elemento [**months**](taskschedulerschema-months-monthlyscheduletype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="06f54-153">When reading or writing your own XML for a task, the months of the year are specified using the [**Months**](taskschedulerschema-months-monthlyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="06f54-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06f54-154">Requirements</span></span>



| <span data-ttu-id="06f54-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="06f54-155">Requirement</span></span> | <span data-ttu-id="06f54-156">Valore</span><span class="sxs-lookup"><span data-stu-id="06f54-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06f54-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06f54-157">Minimum supported client</span></span><br/> | <span data-ttu-id="06f54-158">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06f54-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="06f54-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06f54-159">Minimum supported server</span></span><br/> | <span data-ttu-id="06f54-160">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06f54-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="06f54-161">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="06f54-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="06f54-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="06f54-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="06f54-163">DLL</span><span class="sxs-lookup"><span data-stu-id="06f54-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06f54-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06f54-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06f54-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06f54-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06f54-166">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="06f54-166">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="06f54-167">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="06f54-167">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





