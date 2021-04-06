---
title: Proprietà TaskSettings. Priority
description: Per lo scripting, ottiene o imposta il livello di priorità dell'attività.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Proprietà Priority Utilità di pianificazione
- Utilità di pianificazione proprietà priorità, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà Priority
topic_type:
- apiref
api_name:
- TaskSettings.Priority
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282c688d63bb21f2dc0bab43acde7f089fa960b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963855"
---
# <a name="tasksettingspriority-property"></a><span data-ttu-id="17fbd-106">Proprietà TaskSettings. Priority</span><span class="sxs-lookup"><span data-stu-id="17fbd-106">TaskSettings.Priority property</span></span>

<span data-ttu-id="17fbd-107">Per lo scripting, ottiene o imposta il livello di priorità dell'attività.</span><span class="sxs-lookup"><span data-stu-id="17fbd-107">For scripting, gets or sets the priority level of the task.</span></span>

<span data-ttu-id="17fbd-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="17fbd-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="17fbd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17fbd-109">Syntax</span></span>


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a><span data-ttu-id="17fbd-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="17fbd-110">Property value</span></span>

<span data-ttu-id="17fbd-111">Livello di priorità (0-10) dell'attività.</span><span class="sxs-lookup"><span data-stu-id="17fbd-111">The priority level (0-10) of the task.</span></span> <span data-ttu-id="17fbd-112">Il valore predefinito è 7.</span><span class="sxs-lookup"><span data-stu-id="17fbd-112">The default is 7.</span></span>

## <a name="remarks"></a><span data-ttu-id="17fbd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="17fbd-113">Remarks</span></span>

<span data-ttu-id="17fbd-114">Il livello di priorità 0 è la priorità più alta e il livello di priorità 10 è la priorità più bassa.</span><span class="sxs-lookup"><span data-stu-id="17fbd-114">Priority level 0 is the highest priority, and priority level 10 is the lowest priority.</span></span> <span data-ttu-id="17fbd-115">Il valore predefinito è 7.</span><span class="sxs-lookup"><span data-stu-id="17fbd-115">The default value is 7.</span></span> <span data-ttu-id="17fbd-116">I livelli di priorità 7 e 8 vengono usati per le attività in background e i livelli di priorità 4, 5 e 6 vengono usati per le attività interattive.</span><span class="sxs-lookup"><span data-stu-id="17fbd-116">Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.</span></span>

<span data-ttu-id="17fbd-117">L'azione dell'attività viene avviata in un processo con una priorità basata su un valore della classe di priorità.</span><span class="sxs-lookup"><span data-stu-id="17fbd-117">The task's action is started in a process with a priority that is based on a Priority Class value.</span></span> <span data-ttu-id="17fbd-118">Un valore del livello di priorità (priorità thread) viene usato per le azioni del gestore COM, della finestra di messaggio e dell'attività di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="17fbd-118">A Priority Level value (thread priority) is used for COM handler, message box, and email task actions.</span></span> <span data-ttu-id="17fbd-119">Per ulteriori informazioni sui valori della classe di priorità e del livello di priorità, vedere [priorità di pianificazione](/windows/desktop/ProcThread/scheduling-priorities).</span><span class="sxs-lookup"><span data-stu-id="17fbd-119">For more information about the Priority Class and Priority Level values, see [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities).</span></span> <span data-ttu-id="17fbd-120">Nella tabella seguente sono elencati i valori possibili per il parametro *Priority* e i valori della classe di priorità e del livello di priorità corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="17fbd-120">The following table lists the possible values for the *priority* parameter, and the corresponding Priority Class and Priority Level values.</span></span>



| <span data-ttu-id="17fbd-121">*Priorità* attività</span><span class="sxs-lookup"><span data-stu-id="17fbd-121">Task *priority*</span></span> | <span data-ttu-id="17fbd-122">Classe Priority</span><span class="sxs-lookup"><span data-stu-id="17fbd-122">Priority Class</span></span>                 | <span data-ttu-id="17fbd-123">Livello di priorità</span><span class="sxs-lookup"><span data-stu-id="17fbd-123">Priority Level</span></span>                   |
|-----------------|--------------------------------|----------------------------------|
| <span data-ttu-id="17fbd-124">0</span><span class="sxs-lookup"><span data-stu-id="17fbd-124">0</span></span>               | <span data-ttu-id="17fbd-125">\_classe priorità in tempo reale \_</span><span class="sxs-lookup"><span data-stu-id="17fbd-125">REALTIME\_PRIORITY\_CLASS</span></span>      | <span data-ttu-id="17fbd-126">\_tempo di priorità thread \_ \_ critico</span><span class="sxs-lookup"><span data-stu-id="17fbd-126">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span> |
| <span data-ttu-id="17fbd-127">1</span><span class="sxs-lookup"><span data-stu-id="17fbd-127">1</span></span>               | <span data-ttu-id="17fbd-128">\_classe con priorità alta \_</span><span class="sxs-lookup"><span data-stu-id="17fbd-128">HIGH\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="17fbd-129">\_priorità thread \_ più elevata</span><span class="sxs-lookup"><span data-stu-id="17fbd-129">THREAD\_PRIORITY\_HIGHEST</span></span>        |
| <span data-ttu-id="17fbd-130">2</span><span class="sxs-lookup"><span data-stu-id="17fbd-130">2</span></span>               | <span data-ttu-id="17fbd-131">\_classe di \_ priorità \_ normale sopra</span><span class="sxs-lookup"><span data-stu-id="17fbd-131">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="17fbd-132">\_priorità thread \_ superiore al \_ normale</span><span class="sxs-lookup"><span data-stu-id="17fbd-132">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="17fbd-133">3</span><span class="sxs-lookup"><span data-stu-id="17fbd-133">3</span></span>               | <span data-ttu-id="17fbd-134">\_classe di \_ priorità \_ normale sopra</span><span class="sxs-lookup"><span data-stu-id="17fbd-134">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="17fbd-135">\_priorità thread \_ superiore al \_ normale</span><span class="sxs-lookup"><span data-stu-id="17fbd-135">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="17fbd-136">4</span><span class="sxs-lookup"><span data-stu-id="17fbd-136">4</span></span>               | <span data-ttu-id="17fbd-137">\_classe di priorità normale \_</span><span class="sxs-lookup"><span data-stu-id="17fbd-137">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="17fbd-138">priorità THREAD- \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="17fbd-138">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="17fbd-139">5</span><span class="sxs-lookup"><span data-stu-id="17fbd-139">5</span></span>               | <span data-ttu-id="17fbd-140">\_classe di priorità normale \_</span><span class="sxs-lookup"><span data-stu-id="17fbd-140">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="17fbd-141">priorità THREAD- \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="17fbd-141">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="17fbd-142">6</span><span class="sxs-lookup"><span data-stu-id="17fbd-142">6</span></span>               | <span data-ttu-id="17fbd-143">\_classe di priorità normale \_</span><span class="sxs-lookup"><span data-stu-id="17fbd-143">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="17fbd-144">priorità THREAD- \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="17fbd-144">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="17fbd-145">7</span><span class="sxs-lookup"><span data-stu-id="17fbd-145">7</span></span>               | <span data-ttu-id="17fbd-146">classe di priorità inferiore al \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="17fbd-146">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="17fbd-147">priorità THREAD al di \_ \_ sotto del \_ normale</span><span class="sxs-lookup"><span data-stu-id="17fbd-147">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="17fbd-148">8</span><span class="sxs-lookup"><span data-stu-id="17fbd-148">8</span></span>               | <span data-ttu-id="17fbd-149">classe di priorità inferiore al \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="17fbd-149">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="17fbd-150">priorità THREAD al di \_ \_ sotto del \_ normale</span><span class="sxs-lookup"><span data-stu-id="17fbd-150">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="17fbd-151">9</span><span class="sxs-lookup"><span data-stu-id="17fbd-151">9</span></span>               | <span data-ttu-id="17fbd-152">\_classe priorità INattiva \_</span><span class="sxs-lookup"><span data-stu-id="17fbd-152">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="17fbd-153">\_priorità thread \_ più bassa</span><span class="sxs-lookup"><span data-stu-id="17fbd-153">THREAD\_PRIORITY\_LOWEST</span></span>         |
| <span data-ttu-id="17fbd-154">10</span><span class="sxs-lookup"><span data-stu-id="17fbd-154">10</span></span>              | <span data-ttu-id="17fbd-155">\_classe priorità INattiva \_</span><span class="sxs-lookup"><span data-stu-id="17fbd-155">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="17fbd-156">\_priorità thread \_ inattiva</span><span class="sxs-lookup"><span data-stu-id="17fbd-156">THREAD\_PRIORITY\_IDLE</span></span>           |



 

<span data-ttu-id="17fbd-157">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="17fbd-157">When reading or writing XML for a task, this setting is specified in the [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="17fbd-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17fbd-158">Requirements</span></span>



| <span data-ttu-id="17fbd-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="17fbd-159">Requirement</span></span> | <span data-ttu-id="17fbd-160">Valore</span><span class="sxs-lookup"><span data-stu-id="17fbd-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17fbd-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17fbd-161">Minimum supported client</span></span><br/> | <span data-ttu-id="17fbd-162">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17fbd-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="17fbd-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17fbd-163">Minimum supported server</span></span><br/> | <span data-ttu-id="17fbd-164">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17fbd-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="17fbd-165">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="17fbd-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="17fbd-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="17fbd-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="17fbd-167">DLL</span><span class="sxs-lookup"><span data-stu-id="17fbd-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17fbd-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17fbd-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17fbd-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17fbd-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17fbd-170">**TaskSettings**</span><span class="sxs-lookup"><span data-stu-id="17fbd-170">**TaskSettings**</span></span>](tasksettings.md)
</dt> </dl>

 

