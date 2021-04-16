---
title: Proprietà TaskSettings. MultipleInstances
description: Per gli script, ottiene o imposta i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- Utilità di pianificazione proprietà MultipleInstances
- Utilità di pianificazione proprietà MultipleInstances, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà MultipleInstances
topic_type:
- apiref
api_name:
- TaskSettings.MultipleInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794ea07f1c01dabe957181bd327f8787f873917b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517469"
---
# <a name="tasksettingsmultipleinstances-property"></a><span data-ttu-id="889bd-106">Proprietà TaskSettings. MultipleInstances</span><span class="sxs-lookup"><span data-stu-id="889bd-106">TaskSettings.MultipleInstances property</span></span>

<span data-ttu-id="889bd-107">Per gli script, ottiene o imposta i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.</span><span class="sxs-lookup"><span data-stu-id="889bd-107">For scripting, gets or sets the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span>

<span data-ttu-id="889bd-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="889bd-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="889bd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="889bd-109">Syntax</span></span>


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a><span data-ttu-id="889bd-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="889bd-110">Property value</span></span>

<span data-ttu-id="889bd-111">[**Attività \_ Costanti dei \_ criteri delle istanze**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) .</span><span class="sxs-lookup"><span data-stu-id="889bd-111">[**TASK\_INSTANCES\_POLICY**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) constants.</span></span>



| <span data-ttu-id="889bd-112">Valore</span><span class="sxs-lookup"><span data-stu-id="889bd-112">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="889bd-113">Significato</span><span class="sxs-lookup"><span data-stu-id="889bd-113">Meaning</span></span>                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <span data-ttu-id="889bd-114"><dt>**Attività \_ ISTANZE \_ parallele**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="889bd-114"><dt>**TASK\_INSTANCES\_PARALLEL**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="889bd-115">Avvia una nuova istanza di mentre è in esecuzione un'istanza esistente dell'attività.</span><span class="sxs-lookup"><span data-stu-id="889bd-115">Starts a new instance while an existing instance of the task is running.</span></span><br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <span data-ttu-id="889bd-116"><dt>**Attività \_ \_Coda istanze**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="889bd-116"><dt>**TASK\_INSTANCES\_QUEUE**</dt> <dt>1</dt></span></span> </dl>                          | <span data-ttu-id="889bd-117">Avvia una nuova istanza dell'attività dopo il completamento di tutte le altre istanze dell'attività.</span><span class="sxs-lookup"><span data-stu-id="889bd-117">Starts a new instance of the task after all other instances of the task are complete.</span></span><br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <span data-ttu-id="889bd-118"><dt>**Attività \_ ISTANZE \_ ignorate \_ nuovo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="889bd-118"><dt>**TASK\_INSTANCES\_IGNORE\_NEW**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="889bd-119">Non avvia una nuova istanza di se è in esecuzione un'istanza esistente dell'attività.</span><span class="sxs-lookup"><span data-stu-id="889bd-119">Does not start a new instance if an existing instance of the task is running.</span></span><br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <span data-ttu-id="889bd-120"><dt>**Attività \_ Le \_ istanze \_ arrestano**</dt> <dt>3</dt> esistente</span><span class="sxs-lookup"><span data-stu-id="889bd-120"><dt>**TASK\_INSTANCES\_STOP\_EXISTING**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="889bd-121">Arresta un'istanza esistente dell'attività prima di avviare una nuova istanza.</span><span class="sxs-lookup"><span data-stu-id="889bd-121">Stops an existing instance of the task before it starts new instance.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="889bd-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="889bd-122">Remarks</span></span>

<span data-ttu-id="889bd-123">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="889bd-123">When reading or writing XML for a task, this setting is specified in the [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="889bd-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="889bd-124">Requirements</span></span>



| <span data-ttu-id="889bd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="889bd-125">Requirement</span></span> | <span data-ttu-id="889bd-126">Valore</span><span class="sxs-lookup"><span data-stu-id="889bd-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="889bd-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="889bd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="889bd-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="889bd-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="889bd-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="889bd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="889bd-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="889bd-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="889bd-131">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="889bd-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="889bd-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="889bd-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="889bd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="889bd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="889bd-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="889bd-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="889bd-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="889bd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="889bd-136">**\_criteri istanze \_ attività**</span><span class="sxs-lookup"><span data-stu-id="889bd-136">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[<span data-ttu-id="889bd-137">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="889bd-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





