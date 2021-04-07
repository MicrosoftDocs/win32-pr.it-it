---
title: Trigger.Exeproprietà cutionTimeLimit
description: Per la creazione di script, ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.
ms.assetid: 9993b362-f8f7-429b-a16a-1845d6f0f5e0
keywords:
- Utilità di pianificazione proprietà ExecutionTimeLimit
- Utilità di pianificazione proprietà ExecutionTimeLimit, oggetto trigger
- Utilità di pianificazione oggetto trigger, proprietà ExecutionTimeLimit
topic_type:
- apiref
api_name:
- Trigger.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974a9adebf8ca29fe8626c938c37580d0628771b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963979"
---
# <a name="triggerexecutiontimelimit-property"></a><span data-ttu-id="29291-106">Trigger.Exeproprietà cutionTimeLimit</span><span class="sxs-lookup"><span data-stu-id="29291-106">Trigger.ExecutionTimeLimit property</span></span>

<span data-ttu-id="29291-107">Per la creazione di script, ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="29291-107">For scripting, gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="29291-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29291-108">Syntax</span></span>


```VB
Trigger.ExecutionTimeLimit As String
```



## <a name="property-value"></a><span data-ttu-id="29291-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="29291-109">Property value</span></span>

<span data-ttu-id="29291-110">Quantità massima di tempo durante il quale l'attività avviata dal trigger può essere eseguita.</span><span class="sxs-lookup"><span data-stu-id="29291-110">The maximum amount of time that the task launched by the trigger is allowed to run.</span></span> <span data-ttu-id="29291-111">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="29291-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="29291-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="29291-112">Remarks</span></span>

<span data-ttu-id="29291-113">Durante la lettura o la scrittura di codice XML per un'attività, il limite di tempo di esecuzione viene specificato nell'elemento [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="29291-113">When reading or writing XML for a task, the execution time limit is specified in the [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="29291-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29291-114">Requirements</span></span>



| <span data-ttu-id="29291-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="29291-115">Requirement</span></span> | <span data-ttu-id="29291-116">Valore</span><span class="sxs-lookup"><span data-stu-id="29291-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29291-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29291-117">Minimum supported client</span></span><br/> | <span data-ttu-id="29291-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29291-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="29291-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29291-119">Minimum supported server</span></span><br/> | <span data-ttu-id="29291-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="29291-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="29291-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="29291-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="29291-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="29291-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="29291-123">DLL</span><span class="sxs-lookup"><span data-stu-id="29291-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29291-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29291-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29291-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29291-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29291-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="29291-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





