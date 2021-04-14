---
title: Proprietà RegisteredTask. state
description: Per lo scripting, ottiene lo stato operativo dell'attività registrata.
ms.assetid: 1acd4946-322f-4f24-b317-92be80e19de5
keywords:
- Utilità di pianificazione proprietà stato
- Utilità di pianificazione proprietà state, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, proprietà state
topic_type:
- apiref
api_name:
- RegisteredTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47af082174bc6927a16760e87566f311ec9f4a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478910"
---
# <a name="registeredtaskstate-property"></a><span data-ttu-id="c0746-106">Proprietà RegisteredTask. state</span><span class="sxs-lookup"><span data-stu-id="c0746-106">RegisteredTask.State property</span></span>

<span data-ttu-id="c0746-107">Per lo scripting, ottiene lo stato operativo dell'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="c0746-107">For scripting, gets the operational state of the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0746-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0746-108">Syntax</span></span>


```VB
RegisteredTask.State As Integer
```



## <a name="property-value"></a><span data-ttu-id="c0746-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c0746-109">Property value</span></span>

<span data-ttu-id="c0746-110">Costante [**\_ dello stato dell'attività**](/windows/desktop/api/taskschd/ne-taskschd-task_state) che definisce lo stato operativo dell'attività.</span><span class="sxs-lookup"><span data-stu-id="c0746-110">A [**TASK\_STATE**](/windows/desktop/api/taskschd/ne-taskschd-task_state) constant that defines the operational state of the task.</span></span>



| <span data-ttu-id="c0746-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c0746-111">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="c0746-112">Significato</span><span class="sxs-lookup"><span data-stu-id="c0746-112">Meaning</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <span data-ttu-id="c0746-113"><dt>**Attività \_ STATO \_ sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c0746-113"><dt>**TASK\_STATE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="c0746-114">Lo stato dell'attività è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="c0746-114">The state of the task is unknown.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <span data-ttu-id="c0746-115"><dt>**Attività \_ STATO \_ disabilitato**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c0746-115"><dt>**TASK\_STATE\_DISABLED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="c0746-116">L'attività è registrata ma è disabilitata e nessuna istanza dell'attività viene accodata o in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c0746-116">The task is registered but is disabled and no instances of the task are queued or running.</span></span> <span data-ttu-id="c0746-117">L'attività non può essere eseguita fino a quando non viene abilitata.</span><span class="sxs-lookup"><span data-stu-id="c0746-117">The task cannot be run until it is enabled.</span></span><br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <span data-ttu-id="c0746-118"><dt>**Attività \_ STATO in \_ coda**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c0746-118"><dt>**TASK\_STATE\_QUEUED**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="c0746-119">Le istanze dell'attività vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="c0746-119">Instances of the task are queued.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <span data-ttu-id="c0746-120"><dt>**Attività \_ STATO \_ pronto**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c0746-120"><dt>**TASK\_STATE\_READY**</dt> <dt>3</dt></span></span> </dl>          | <span data-ttu-id="c0746-121">L'attività è pronta per essere eseguita, ma nessuna istanza è in coda o in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c0746-121">The task is ready to be executed, but no instances are queued or running.</span></span><br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <span data-ttu-id="c0746-122"><dt>**Attività \_ STATO \_ che esegue**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c0746-122"><dt>**TASK\_STATE\_RUNNING**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="c0746-123">Una o più istanze dell'attività sono in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c0746-123">One or more instances of the task are running.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="c0746-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0746-124">Requirements</span></span>



| <span data-ttu-id="c0746-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0746-125">Requirement</span></span> | <span data-ttu-id="c0746-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c0746-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0746-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0746-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c0746-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0746-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c0746-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0746-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c0746-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0746-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0746-131">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c0746-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="c0746-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c0746-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c0746-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c0746-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0746-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0746-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0746-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0746-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0746-136">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c0746-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="c0746-137">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="c0746-137">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





