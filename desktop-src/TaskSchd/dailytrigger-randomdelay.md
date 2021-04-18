---
title: Proprietà DailyTrigger. RandomDelay
description: Per gli script, ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger. | Proprietà DailyTrigger. RandomDelay
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- Utilità di pianificazione proprietà RandomDelay
- Utilità di pianificazione proprietà RandomDelay, oggetto DailyTrigger
- Oggetto DailyTrigger Utilità di pianificazione, proprietà RandomDelay
topic_type:
- apiref
api_name:
- DailyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd24fc5bd97a51cc0276e0fdfe800c0a9baa022a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321736"
---
# <a name="dailytriggerrandomdelay-property"></a><span data-ttu-id="20c0f-107">Proprietà DailyTrigger. RandomDelay</span><span class="sxs-lookup"><span data-stu-id="20c0f-107">DailyTrigger.RandomDelay property</span></span>

<span data-ttu-id="20c0f-108">Per gli script, ottiene o imposta un tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="20c0f-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="20c0f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20c0f-109">Syntax</span></span>


```VB
DailyTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="20c0f-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="20c0f-110">Property value</span></span>

<span data-ttu-id="20c0f-111">Tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="20c0f-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="20c0f-112">Il formato di questa stringa è P <days> DT <hours> H <minutes> M <seconds> S (ad esempio, P2DT5S è un ritardo di 2 giorni e 5 secondi).</span><span class="sxs-lookup"><span data-stu-id="20c0f-112">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="20c0f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20c0f-113">Requirements</span></span>



| <span data-ttu-id="20c0f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="20c0f-114">Requirement</span></span> | <span data-ttu-id="20c0f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="20c0f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20c0f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20c0f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="20c0f-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20c0f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="20c0f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20c0f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="20c0f-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="20c0f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="20c0f-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="20c0f-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="20c0f-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="20c0f-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="20c0f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="20c0f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20c0f-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20c0f-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20c0f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20c0f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c0f-125">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="20c0f-125">**DailyTrigger**</span></span>](dailytrigger.md)
</dt> <dt>

[<span data-ttu-id="20c0f-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="20c0f-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





