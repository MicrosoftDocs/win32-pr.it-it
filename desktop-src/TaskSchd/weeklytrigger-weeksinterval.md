---
title: Proprietà WeeklyTrigger. WeeksInterval
description: Per lo scripting, ottiene o imposta l'intervallo tra le settimane nella pianificazione.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- Utilità di pianificazione proprietà WeeksInterval
- Utilità di pianificazione proprietà WeeksInterval, oggetto WeeklyTrigger
- Oggetto WeeklyTrigger Utilità di pianificazione, proprietà WeeksInterval
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4668b68d0b3f83e096284db35df799a63eb677b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301137"
---
# <a name="weeklytriggerweeksinterval-property"></a><span data-ttu-id="13b15-106">Proprietà WeeklyTrigger. WeeksInterval</span><span class="sxs-lookup"><span data-stu-id="13b15-106">WeeklyTrigger.WeeksInterval property</span></span>

<span data-ttu-id="13b15-107">Per lo scripting, ottiene o imposta l'intervallo tra le settimane nella pianificazione.</span><span class="sxs-lookup"><span data-stu-id="13b15-107">For scripting, gets or sets the interval between the weeks in the schedule.</span></span>

## <a name="syntax"></a><span data-ttu-id="13b15-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13b15-108">Syntax</span></span>


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a><span data-ttu-id="13b15-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="13b15-109">Property value</span></span>

<span data-ttu-id="13b15-110">Intervallo tra le settimane nella pianificazione.</span><span class="sxs-lookup"><span data-stu-id="13b15-110">The interval between the weeks in the schedule.</span></span>

## <a name="remarks"></a><span data-ttu-id="13b15-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="13b15-111">Remarks</span></span>

<span data-ttu-id="13b15-112">Un intervallo di 1 produce una pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="13b15-112">An interval of 1 produces a weekly schedule.</span></span> <span data-ttu-id="13b15-113">Un intervallo di 2 produce una pianificazione di ogni settimana.</span><span class="sxs-lookup"><span data-stu-id="13b15-113">An interval of 2 produces an every-other week schedule.</span></span>

<span data-ttu-id="13b15-114">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, l'intervallo per una pianificazione settimanale viene specificato utilizzando l'elemento [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="13b15-114">When reading or writing your own XML for a task, the interval for a weekly schedule is specified using the [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="13b15-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13b15-115">Requirements</span></span>



| <span data-ttu-id="13b15-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="13b15-116">Requirement</span></span> | <span data-ttu-id="13b15-117">Valore</span><span class="sxs-lookup"><span data-stu-id="13b15-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13b15-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13b15-118">Minimum supported client</span></span><br/> | <span data-ttu-id="13b15-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13b15-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="13b15-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13b15-120">Minimum supported server</span></span><br/> | <span data-ttu-id="13b15-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13b15-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="13b15-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="13b15-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="13b15-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="13b15-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="13b15-124">DLL</span><span class="sxs-lookup"><span data-stu-id="13b15-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13b15-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13b15-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13b15-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13b15-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13b15-127">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="13b15-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





