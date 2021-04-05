---
title: Proprietà TaskSettings. Compatibility
description: Per lo scripting, ottiene o imposta un valore integer che indica la versione di Utilità di pianificazione un'attività è compatibile con.
ms.assetid: bbe21177-e010-4770-9068-9c5b41974ee5
keywords:
- Utilità di pianificazione proprietà di compatibilità
- Utilità di pianificazione proprietà di compatibilità, oggetto TaskSettings
- Utilità di pianificazione oggetto TaskSettings, proprietà di compatibilità
topic_type:
- apiref
api_name:
- TaskSettings.Compatibility
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ba93d3716a8fb0e701cc783ec83abba40190d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740815"
---
# <a name="tasksettingscompatibility-property"></a><span data-ttu-id="3ecd5-106">Proprietà TaskSettings. Compatibility</span><span class="sxs-lookup"><span data-stu-id="3ecd5-106">TaskSettings.Compatibility property</span></span>

<span data-ttu-id="3ecd5-107">Per lo scripting, ottiene o imposta un valore integer che indica la versione di Utilità di pianificazione un'attività è compatibile con.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-107">For scripting, gets or sets an integer value that indicates which version of Task Scheduler a task is compatible with.</span></span>

<span data-ttu-id="3ecd5-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ecd5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ecd5-109">Syntax</span></span>


```VB
TaskSettings.Compatibility As Integer
```



## <a name="property-value"></a><span data-ttu-id="3ecd5-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3ecd5-110">Property value</span></span>



| <span data-ttu-id="3ecd5-111">Valore</span><span class="sxs-lookup"><span data-stu-id="3ecd5-111">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="3ecd5-112">Significato</span><span class="sxs-lookup"><span data-stu-id="3ecd5-112">Meaning</span></span>                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="TASK_COMPATIBILITY_AT"></span><span id="task_compatibility_at"></span><dl> <span data-ttu-id="3ecd5-113"><dt>**Attività \_ COMPATIBILITÀ \_ con**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3ecd5-113"><dt>**TASK\_COMPATIBILITY\_AT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="3ecd5-114">L'attività è compatibile con il comando AT.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-114">The task is compatible with the AT command.</span></span><br/>     |
| <span id="TASK_COMPATIBILITY_V1"></span><span id="task_compatibility_v1"></span><dl> <span data-ttu-id="3ecd5-115"><dt>**Attività \_ COMPATIBILITÀ \_ V1**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3ecd5-115"><dt>**TASK\_COMPATIBILITY\_V1**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="3ecd5-116">L'attività è compatibile con Utilità di pianificazione 1,0.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-116">The task is compatible with Task Scheduler 1.0.</span></span><br/> |
| <span id="TASK_COMPATIBILITY_V2"></span><span id="task_compatibility_v2"></span><dl> <span data-ttu-id="3ecd5-117"><dt>**Attività \_ COMPATIBILITÀ \_ v2**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3ecd5-117"><dt>**TASK\_COMPATIBILITY\_V2**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="3ecd5-118">L'attività è compatibile con Utilità di pianificazione 2,0.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-118">The task is compatible with Task Scheduler 2.0.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3ecd5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ecd5-119">Remarks</span></span>

<span data-ttu-id="3ecd5-120">Per la compatibilità delle attività, impostata tramite la proprietà [**compatibilità**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , è consigliabile impostare solo la \_ compatibilità delle attività \_ V1 se un'attività deve essere accessibile o modificata da un computer Windows XP, Windows Server 2003 o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-120">Task compatibility, which is set through the [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) property, should only be set to TASK\_COMPATIBILITY\_V1 if a task needs to be accessed or modified from a Windows XP, Windows Server 2003, or Windows 2000 computer.</span></span> <span data-ttu-id="3ecd5-121">In caso contrario, è consigliabile usare Utilità di pianificazione compatibilità 2,0 perché l'attività avrà più funzionalità.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-121">Otherwise, it is recommended that Task Scheduler 2.0 compatibility be used because the task will have more features.</span></span>

<span data-ttu-id="3ecd5-122">Le attività compatibili con il comando AT possono avere un solo trigger di tempo.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-122">Tasks compatible with the AT command can only have one time trigger.</span></span>

<span data-ttu-id="3ecd5-123">Le attività compatibili con Utilità di pianificazione 1,0 possono avere solo un trigger di ora, un trigger LOGON o un trigger di avvio e l'attività può avere solo un'azione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-123">Tasks compatible with Task Scheduler 1.0 can only have a time trigger, a logon trigger, or a boot trigger, and the task can only have an executable action.</span></span>

<span data-ttu-id="3ecd5-124">Per ulteriori informazioni sulla compatibilità delle attività, vedere Novità [di utilità di pianificazione](what-s-new-in-task-scheduler.md) e [attività](tasks.md).</span><span class="sxs-lookup"><span data-stu-id="3ecd5-124">For more information about task compatibility, see [What's New in Task Scheduler](what-s-new-in-task-scheduler.md) and [Tasks](tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ecd5-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ecd5-125">Requirements</span></span>



| <span data-ttu-id="3ecd5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ecd5-126">Requirement</span></span> | <span data-ttu-id="3ecd5-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3ecd5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ecd5-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ecd5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3ecd5-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ecd5-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3ecd5-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ecd5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3ecd5-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ecd5-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ecd5-132">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3ecd5-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="3ecd5-133"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3ecd5-133"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3ecd5-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3ecd5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ecd5-135"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ecd5-135"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ecd5-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ecd5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ecd5-137">**compatibilità delle attività \_**</span><span class="sxs-lookup"><span data-stu-id="3ecd5-137">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)
</dt> <dt>

[<span data-ttu-id="3ecd5-138">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3ecd5-138">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





