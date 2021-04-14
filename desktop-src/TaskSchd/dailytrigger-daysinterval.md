---
title: Proprietà DailyTrigger. DaysInterval
description: Per gli script, ottiene o imposta l'intervallo tra i giorni della pianificazione.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- Utilità di pianificazione proprietà DaysInterval
- Utilità di pianificazione proprietà DaysInterval, oggetto DailyTrigger
- Oggetto DailyTrigger Utilità di pianificazione, proprietà DaysInterval
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6499f3b900fe10b2a2527c2e2ee675cca3151204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517914"
---
# <a name="dailytriggerdaysinterval-property"></a><span data-ttu-id="d91e5-106">Proprietà DailyTrigger. DaysInterval</span><span class="sxs-lookup"><span data-stu-id="d91e5-106">DailyTrigger.DaysInterval property</span></span>

<span data-ttu-id="d91e5-107">Per gli script, ottiene o imposta l'intervallo tra i giorni della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d91e5-107">For scripting, gets or sets the interval between the days in the schedule.</span></span>

## <a name="syntax"></a><span data-ttu-id="d91e5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d91e5-108">Syntax</span></span>


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a><span data-ttu-id="d91e5-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d91e5-109">Property value</span></span>

<span data-ttu-id="d91e5-110">Intervallo tra i giorni della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d91e5-110">The interval between the days in the schedule.</span></span>

## <a name="remarks"></a><span data-ttu-id="d91e5-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d91e5-111">Remarks</span></span>

<span data-ttu-id="d91e5-112">Un intervallo di 1 produce una pianificazione giornaliera.</span><span class="sxs-lookup"><span data-stu-id="d91e5-112">An interval of 1 produces a daily schedule.</span></span> <span data-ttu-id="d91e5-113">Un intervallo di 2 produce una pianificazione di ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="d91e5-113">An interval of 2 produces an every-other day schedule.</span></span>

<span data-ttu-id="d91e5-114">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, l'intervallo per una pianificazione giornaliera viene specificato mediante l'elemento [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d91e5-114">When reading or writing your own XML for a task, the interval for a daily schedule is specified using the [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d91e5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d91e5-115">Requirements</span></span>



| <span data-ttu-id="d91e5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d91e5-116">Requirement</span></span> | <span data-ttu-id="d91e5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d91e5-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d91e5-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d91e5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d91e5-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d91e5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d91e5-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d91e5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d91e5-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d91e5-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d91e5-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d91e5-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="d91e5-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d91e5-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d91e5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d91e5-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d91e5-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d91e5-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d91e5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d91e5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d91e5-127">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d91e5-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d91e5-128">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="d91e5-128">**DailyTrigger**</span></span>](dailytrigger.md)
</dt> </dl>

 

 





