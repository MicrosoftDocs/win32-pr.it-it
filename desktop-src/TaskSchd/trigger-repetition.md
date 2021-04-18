---
title: Trigger. proprietà di ripetizione
description: Per lo scripting, ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- Utilità di pianificazione della proprietà di ripetizione
- Utilità di pianificazione proprietà di ripetizione, oggetto trigger
- Trigger Utilità di pianificazione oggetto, proprietà di ripetizione
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611c7e42a14de06a8777333a6dc640781943ba06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301326"
---
# <a name="triggerrepetition-property"></a><span data-ttu-id="e8cbf-106">Trigger. proprietà di ripetizione</span><span class="sxs-lookup"><span data-stu-id="e8cbf-106">Trigger.Repetition property</span></span>

<span data-ttu-id="e8cbf-107">Per lo scripting, ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="e8cbf-107">For scripting, gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8cbf-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8cbf-108">Syntax</span></span>


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a><span data-ttu-id="e8cbf-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e8cbf-109">Property value</span></span>

<span data-ttu-id="e8cbf-110">Oggetto [**RepetitionPattern**](repetitionpattern.md) che definisce la frequenza con cui viene eseguita l'attività e per quanto tempo il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="e8cbf-110">A [**RepetitionPattern**](repetitionpattern.md) object that defines how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8cbf-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8cbf-111">Remarks</span></span>

<span data-ttu-id="e8cbf-112">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, il modello di ripetizione per un trigger viene specificato nell'elemento di [**ripetizione**](taskschedulerschema-repetition-triggerbasetype-element.md) dello schema di utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="e8cbf-112">When reading or writing your own XML for a task, the repetition pattern for a trigger is specified in the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8cbf-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8cbf-113">Requirements</span></span>



| <span data-ttu-id="e8cbf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8cbf-114">Requirement</span></span> | <span data-ttu-id="e8cbf-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e8cbf-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8cbf-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8cbf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e8cbf-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8cbf-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e8cbf-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8cbf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e8cbf-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e8cbf-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e8cbf-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e8cbf-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8cbf-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e8cbf-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e8cbf-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e8cbf-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8cbf-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8cbf-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8cbf-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8cbf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8cbf-125">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e8cbf-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e8cbf-126">**RepetitionPattern**</span><span class="sxs-lookup"><span data-stu-id="e8cbf-126">**RepetitionPattern**</span></span>](repetitionpattern.md)
</dt> </dl>

 

 





