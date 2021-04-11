---
title: Proprietà MonthlyTrigger. DaysOfMonth
description: Per gli script, ottiene o imposta i giorni del mese durante i quali viene eseguita l'attività.
ms.assetid: 4da80d0f-ae0c-4e56-b51b-6ee6ab309d7c
keywords:
- Utilità di pianificazione proprietà DaysOfMonth
- Utilità di pianificazione proprietà DaysOfMonth, oggetto MonthlyTrigger
- Oggetto MonthlyTrigger Utilità di pianificazione, proprietà DaysOfMonth
topic_type:
- apiref
api_name:
- MonthlyTrigger.DaysOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a3bd671266cfbe459218367fadf20fd52f94a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120223"
---
# <a name="monthlytriggerdaysofmonth-property"></a><span data-ttu-id="f4c38-106">Proprietà MonthlyTrigger. DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="f4c38-106">MonthlyTrigger.DaysOfMonth property</span></span>

<span data-ttu-id="f4c38-107">Per gli script, ottiene o imposta i giorni del mese durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="f4c38-107">For scripting, gets or sets the days of the month during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c38-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4c38-108">Syntax</span></span>


```VB
MonthlyTrigger.DaysOfMonth As long
```



## <a name="property-value"></a><span data-ttu-id="f4c38-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f4c38-109">Property value</span></span>

<span data-ttu-id="f4c38-110">Maschera bit per bit che indica i giorni del mese durante i quali viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="f4c38-110">A bitwise mask that indicates the days of the month during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4c38-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4c38-111">Remarks</span></span>



| <span data-ttu-id="f4c38-112">Giorno del mese</span><span class="sxs-lookup"><span data-stu-id="f4c38-112">Day of month</span></span> | <span data-ttu-id="f4c38-113">Valore hex</span><span class="sxs-lookup"><span data-stu-id="f4c38-113">Hex value</span></span>  | <span data-ttu-id="f4c38-114">Valore decimale</span><span class="sxs-lookup"><span data-stu-id="f4c38-114">Decimal value</span></span> |
|--------------|------------|---------------|
| <span data-ttu-id="f4c38-115">1</span><span class="sxs-lookup"><span data-stu-id="f4c38-115">1</span></span>            | <span data-ttu-id="f4c38-116">0x01</span><span class="sxs-lookup"><span data-stu-id="f4c38-116">0x01</span></span>       | <span data-ttu-id="f4c38-117">1</span><span class="sxs-lookup"><span data-stu-id="f4c38-117">1</span></span>             |
| <span data-ttu-id="f4c38-118">2</span><span class="sxs-lookup"><span data-stu-id="f4c38-118">2</span></span>            | <span data-ttu-id="f4c38-119">0x02</span><span class="sxs-lookup"><span data-stu-id="f4c38-119">0x02</span></span>       | <span data-ttu-id="f4c38-120">2</span><span class="sxs-lookup"><span data-stu-id="f4c38-120">2</span></span>             |
| <span data-ttu-id="f4c38-121">3</span><span class="sxs-lookup"><span data-stu-id="f4c38-121">3</span></span>            | <span data-ttu-id="f4c38-122">0x04</span><span class="sxs-lookup"><span data-stu-id="f4c38-122">0x04</span></span>       | <span data-ttu-id="f4c38-123">4</span><span class="sxs-lookup"><span data-stu-id="f4c38-123">4</span></span>             |
| <span data-ttu-id="f4c38-124">4</span><span class="sxs-lookup"><span data-stu-id="f4c38-124">4</span></span>            | <span data-ttu-id="f4c38-125">0x08</span><span class="sxs-lookup"><span data-stu-id="f4c38-125">0x08</span></span>       | <span data-ttu-id="f4c38-126">8</span><span class="sxs-lookup"><span data-stu-id="f4c38-126">8</span></span>             |
| <span data-ttu-id="f4c38-127">5</span><span class="sxs-lookup"><span data-stu-id="f4c38-127">5</span></span>            | <span data-ttu-id="f4c38-128">0x10</span><span class="sxs-lookup"><span data-stu-id="f4c38-128">0x10</span></span>       | <span data-ttu-id="f4c38-129">16</span><span class="sxs-lookup"><span data-stu-id="f4c38-129">16</span></span>            |
| <span data-ttu-id="f4c38-130">6</span><span class="sxs-lookup"><span data-stu-id="f4c38-130">6</span></span>            | <span data-ttu-id="f4c38-131">0x20</span><span class="sxs-lookup"><span data-stu-id="f4c38-131">0x20</span></span>       | <span data-ttu-id="f4c38-132">32</span><span class="sxs-lookup"><span data-stu-id="f4c38-132">32</span></span>            |
| <span data-ttu-id="f4c38-133">7</span><span class="sxs-lookup"><span data-stu-id="f4c38-133">7</span></span>            | <span data-ttu-id="f4c38-134">0x40</span><span class="sxs-lookup"><span data-stu-id="f4c38-134">0x40</span></span>       | <span data-ttu-id="f4c38-135">64</span><span class="sxs-lookup"><span data-stu-id="f4c38-135">64</span></span>            |
| <span data-ttu-id="f4c38-136">8</span><span class="sxs-lookup"><span data-stu-id="f4c38-136">8</span></span>            | <span data-ttu-id="f4c38-137">0x80</span><span class="sxs-lookup"><span data-stu-id="f4c38-137">0x80</span></span>       | <span data-ttu-id="f4c38-138">128</span><span class="sxs-lookup"><span data-stu-id="f4c38-138">128</span></span>           |
| <span data-ttu-id="f4c38-139">9</span><span class="sxs-lookup"><span data-stu-id="f4c38-139">9</span></span>            | <span data-ttu-id="f4c38-140">0x100</span><span class="sxs-lookup"><span data-stu-id="f4c38-140">0x100</span></span>      | <span data-ttu-id="f4c38-141">256</span><span class="sxs-lookup"><span data-stu-id="f4c38-141">256</span></span>           |
| <span data-ttu-id="f4c38-142">10</span><span class="sxs-lookup"><span data-stu-id="f4c38-142">10</span></span>           | <span data-ttu-id="f4c38-143">0x200</span><span class="sxs-lookup"><span data-stu-id="f4c38-143">0x200</span></span>      | <span data-ttu-id="f4c38-144">512</span><span class="sxs-lookup"><span data-stu-id="f4c38-144">512</span></span>           |
| <span data-ttu-id="f4c38-145">11</span><span class="sxs-lookup"><span data-stu-id="f4c38-145">11</span></span>           | <span data-ttu-id="f4c38-146">0x400</span><span class="sxs-lookup"><span data-stu-id="f4c38-146">0x400</span></span>      | <span data-ttu-id="f4c38-147">1024</span><span class="sxs-lookup"><span data-stu-id="f4c38-147">1024</span></span>          |
| <span data-ttu-id="f4c38-148">12</span><span class="sxs-lookup"><span data-stu-id="f4c38-148">12</span></span>           | <span data-ttu-id="f4c38-149">0x800</span><span class="sxs-lookup"><span data-stu-id="f4c38-149">0x800</span></span>      | <span data-ttu-id="f4c38-150">2048</span><span class="sxs-lookup"><span data-stu-id="f4c38-150">2048</span></span>          |
| <span data-ttu-id="f4c38-151">13</span><span class="sxs-lookup"><span data-stu-id="f4c38-151">13</span></span>           | <span data-ttu-id="f4c38-152">0x1000</span><span class="sxs-lookup"><span data-stu-id="f4c38-152">0x1000</span></span>     | <span data-ttu-id="f4c38-153">4096</span><span class="sxs-lookup"><span data-stu-id="f4c38-153">4096</span></span>          |
| <span data-ttu-id="f4c38-154">14</span><span class="sxs-lookup"><span data-stu-id="f4c38-154">14</span></span>           | <span data-ttu-id="f4c38-155">0x2000</span><span class="sxs-lookup"><span data-stu-id="f4c38-155">0x2000</span></span>     | <span data-ttu-id="f4c38-156">8192</span><span class="sxs-lookup"><span data-stu-id="f4c38-156">8192</span></span>          |
| <span data-ttu-id="f4c38-157">15</span><span class="sxs-lookup"><span data-stu-id="f4c38-157">15</span></span>           | <span data-ttu-id="f4c38-158">0x4000</span><span class="sxs-lookup"><span data-stu-id="f4c38-158">0x4000</span></span>     | <span data-ttu-id="f4c38-159">16384</span><span class="sxs-lookup"><span data-stu-id="f4c38-159">16384</span></span>         |
| <span data-ttu-id="f4c38-160">16</span><span class="sxs-lookup"><span data-stu-id="f4c38-160">16</span></span>           | <span data-ttu-id="f4c38-161">0x8000</span><span class="sxs-lookup"><span data-stu-id="f4c38-161">0x8000</span></span>     | <span data-ttu-id="f4c38-162">32768</span><span class="sxs-lookup"><span data-stu-id="f4c38-162">32768</span></span>         |
| <span data-ttu-id="f4c38-163">17</span><span class="sxs-lookup"><span data-stu-id="f4c38-163">17</span></span>           | <span data-ttu-id="f4c38-164">0x10000</span><span class="sxs-lookup"><span data-stu-id="f4c38-164">0x10000</span></span>    | <span data-ttu-id="f4c38-165">65536</span><span class="sxs-lookup"><span data-stu-id="f4c38-165">65536</span></span>         |
| <span data-ttu-id="f4c38-166">18</span><span class="sxs-lookup"><span data-stu-id="f4c38-166">18</span></span>           | <span data-ttu-id="f4c38-167">0x20000</span><span class="sxs-lookup"><span data-stu-id="f4c38-167">0x20000</span></span>    | <span data-ttu-id="f4c38-168">131072</span><span class="sxs-lookup"><span data-stu-id="f4c38-168">131072</span></span>        |
| <span data-ttu-id="f4c38-169">19</span><span class="sxs-lookup"><span data-stu-id="f4c38-169">19</span></span>           | <span data-ttu-id="f4c38-170">0x40000</span><span class="sxs-lookup"><span data-stu-id="f4c38-170">0x40000</span></span>    | <span data-ttu-id="f4c38-171">262144</span><span class="sxs-lookup"><span data-stu-id="f4c38-171">262144</span></span>        |
| <span data-ttu-id="f4c38-172">20</span><span class="sxs-lookup"><span data-stu-id="f4c38-172">20</span></span>           | <span data-ttu-id="f4c38-173">0x80000</span><span class="sxs-lookup"><span data-stu-id="f4c38-173">0x80000</span></span>    | <span data-ttu-id="f4c38-174">524288</span><span class="sxs-lookup"><span data-stu-id="f4c38-174">524288</span></span>        |
| <span data-ttu-id="f4c38-175">21</span><span class="sxs-lookup"><span data-stu-id="f4c38-175">21</span></span>           | <span data-ttu-id="f4c38-176">0x100000</span><span class="sxs-lookup"><span data-stu-id="f4c38-176">0x100000</span></span>   | <span data-ttu-id="f4c38-177">1048576</span><span class="sxs-lookup"><span data-stu-id="f4c38-177">1048576</span></span>       |
| <span data-ttu-id="f4c38-178">22</span><span class="sxs-lookup"><span data-stu-id="f4c38-178">22</span></span>           | <span data-ttu-id="f4c38-179">0x200000</span><span class="sxs-lookup"><span data-stu-id="f4c38-179">0x200000</span></span>   | <span data-ttu-id="f4c38-180">2097152</span><span class="sxs-lookup"><span data-stu-id="f4c38-180">2097152</span></span>       |
| <span data-ttu-id="f4c38-181">23</span><span class="sxs-lookup"><span data-stu-id="f4c38-181">23</span></span>           | <span data-ttu-id="f4c38-182">0x400000</span><span class="sxs-lookup"><span data-stu-id="f4c38-182">0x400000</span></span>   | <span data-ttu-id="f4c38-183">4194304</span><span class="sxs-lookup"><span data-stu-id="f4c38-183">4194304</span></span>       |
| <span data-ttu-id="f4c38-184">24</span><span class="sxs-lookup"><span data-stu-id="f4c38-184">24</span></span>           | <span data-ttu-id="f4c38-185">0x800000</span><span class="sxs-lookup"><span data-stu-id="f4c38-185">0x800000</span></span>   | <span data-ttu-id="f4c38-186">8388608</span><span class="sxs-lookup"><span data-stu-id="f4c38-186">8388608</span></span>       |
| <span data-ttu-id="f4c38-187">25</span><span class="sxs-lookup"><span data-stu-id="f4c38-187">25</span></span>           | <span data-ttu-id="f4c38-188">0x1000000</span><span class="sxs-lookup"><span data-stu-id="f4c38-188">0x1000000</span></span>  | <span data-ttu-id="f4c38-189">16777216</span><span class="sxs-lookup"><span data-stu-id="f4c38-189">16777216</span></span>      |
| <span data-ttu-id="f4c38-190">26</span><span class="sxs-lookup"><span data-stu-id="f4c38-190">26</span></span>           | <span data-ttu-id="f4c38-191">0x2000000</span><span class="sxs-lookup"><span data-stu-id="f4c38-191">0x2000000</span></span>  | <span data-ttu-id="f4c38-192">33554432</span><span class="sxs-lookup"><span data-stu-id="f4c38-192">33554432</span></span>      |
| <span data-ttu-id="f4c38-193">27</span><span class="sxs-lookup"><span data-stu-id="f4c38-193">27</span></span>           | <span data-ttu-id="f4c38-194">0x4000000</span><span class="sxs-lookup"><span data-stu-id="f4c38-194">0x4000000</span></span>  | <span data-ttu-id="f4c38-195">67108864</span><span class="sxs-lookup"><span data-stu-id="f4c38-195">67108864</span></span>      |
| <span data-ttu-id="f4c38-196">28</span><span class="sxs-lookup"><span data-stu-id="f4c38-196">28</span></span>           | <span data-ttu-id="f4c38-197">0x8000000</span><span class="sxs-lookup"><span data-stu-id="f4c38-197">0x8000000</span></span>  | <span data-ttu-id="f4c38-198">134217728</span><span class="sxs-lookup"><span data-stu-id="f4c38-198">134217728</span></span>     |
| <span data-ttu-id="f4c38-199">29</span><span class="sxs-lookup"><span data-stu-id="f4c38-199">29</span></span>           | <span data-ttu-id="f4c38-200">0x10000000</span><span class="sxs-lookup"><span data-stu-id="f4c38-200">0x10000000</span></span> | <span data-ttu-id="f4c38-201">268435456</span><span class="sxs-lookup"><span data-stu-id="f4c38-201">268435456</span></span>     |
| <span data-ttu-id="f4c38-202">30</span><span class="sxs-lookup"><span data-stu-id="f4c38-202">30</span></span>           | <span data-ttu-id="f4c38-203">0x20000000</span><span class="sxs-lookup"><span data-stu-id="f4c38-203">0x20000000</span></span> | <span data-ttu-id="f4c38-204">536870912</span><span class="sxs-lookup"><span data-stu-id="f4c38-204">536870912</span></span>     |
| <span data-ttu-id="f4c38-205">31</span><span class="sxs-lookup"><span data-stu-id="f4c38-205">31</span></span>           | <span data-ttu-id="f4c38-206">0x40000000</span><span class="sxs-lookup"><span data-stu-id="f4c38-206">0x40000000</span></span> | <span data-ttu-id="f4c38-207">1073741824</span><span class="sxs-lookup"><span data-stu-id="f4c38-207">1073741824</span></span>    |
| <span data-ttu-id="f4c38-208">Last (Ultimo)</span><span class="sxs-lookup"><span data-stu-id="f4c38-208">Last</span></span>         | <span data-ttu-id="f4c38-209">0x80000000</span><span class="sxs-lookup"><span data-stu-id="f4c38-209">0x80000000</span></span> | <span data-ttu-id="f4c38-210">2147483648</span><span class="sxs-lookup"><span data-stu-id="f4c38-210">2147483648</span></span>    |



 

<span data-ttu-id="f4c38-211">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, i giorni del mese vengono specificati utilizzando l'elemento [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="f4c38-211">When reading or writing your own XML for a task, the days of the month are specified using the [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4c38-212">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4c38-212">Requirements</span></span>



| <span data-ttu-id="f4c38-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4c38-213">Requirement</span></span> | <span data-ttu-id="f4c38-214">Valore</span><span class="sxs-lookup"><span data-stu-id="f4c38-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c38-215">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4c38-215">Minimum supported client</span></span><br/> | <span data-ttu-id="f4c38-216">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4c38-216">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f4c38-217">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4c38-217">Minimum supported server</span></span><br/> | <span data-ttu-id="f4c38-218">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4c38-218">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f4c38-219">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f4c38-219">Type library</span></span><br/>             | <dl> <span data-ttu-id="f4c38-220"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f4c38-220"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f4c38-221">DLL</span><span class="sxs-lookup"><span data-stu-id="f4c38-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4c38-222"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4c38-222"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4c38-223">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4c38-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4c38-224">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f4c38-224">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="f4c38-225">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="f4c38-225">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





