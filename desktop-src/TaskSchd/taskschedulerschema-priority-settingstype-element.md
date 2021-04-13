---
title: Elemento Priority (settingsType)
description: Specifica il livello di priorità per l'attività.
ms.assetid: 4885fffa-b7d9-4f5e-b6e8-6f18b01c2427
keywords:
- Elemento Priority Utilità di pianificazione
topic_type:
- apiref
api_name:
- Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecda59ecbbe23550363fb30706d73bca54fcd925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400344"
---
# <a name="priority-settingstype-element"></a><span data-ttu-id="3b247-104">Elemento Priority (settingsType)</span><span class="sxs-lookup"><span data-stu-id="3b247-104">Priority (settingsType) Element</span></span>

<span data-ttu-id="3b247-105">Specifica il livello di priorità per l'attività.</span><span class="sxs-lookup"><span data-stu-id="3b247-105">Specifies the priority level for the task.</span></span>

``` syntax
<xs:element name="Priority"
    type="priorityType"
    default="7"
    minOccurs="0"
 />
```

<span data-ttu-id="3b247-106">L'elemento **Priority** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3b247-106">The **Priority** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3b247-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="3b247-107">Parent element</span></span>



| <span data-ttu-id="3b247-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3b247-108">Element</span></span>                                                           | <span data-ttu-id="3b247-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="3b247-109">Derived from</span></span>                                                         | <span data-ttu-id="3b247-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b247-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b247-111">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="3b247-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="3b247-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="3b247-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="3b247-113">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="3b247-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3b247-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b247-114">Remarks</span></span>

<span data-ttu-id="3b247-115">Il livello di priorità 0 è la priorità più alta e il livello di priorità 10 è la priorità più bassa.</span><span class="sxs-lookup"><span data-stu-id="3b247-115">Priority level 0 is the highest priority, and priority level 10 is the lowest priority.</span></span> <span data-ttu-id="3b247-116">Il valore predefinito è 7.</span><span class="sxs-lookup"><span data-stu-id="3b247-116">The default value is 7.</span></span> <span data-ttu-id="3b247-117">I valori minimo e massimo vengono impostati dal tipo semplice [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="3b247-117">The minimum and maximum values are set by the [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) simple type.</span></span> <span data-ttu-id="3b247-118">I livelli di priorità 7 e 8 vengono usati per le attività in background e i livelli di priorità 4, 5 e 6 vengono usati per le attività interattive.</span><span class="sxs-lookup"><span data-stu-id="3b247-118">Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.</span></span>

<span data-ttu-id="3b247-119">L'azione dell'attività viene avviata in un processo con una priorità basata su un valore della classe di priorità.</span><span class="sxs-lookup"><span data-stu-id="3b247-119">The task's action is started in a process with a priority that is based on a Priority Class value.</span></span> <span data-ttu-id="3b247-120">Un valore del livello di priorità (priorità thread) viene usato per le azioni del gestore COM, della finestra di messaggio e dell'attività di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3b247-120">A Priority Level value (thread priority) is used for COM handler, message box, and email task actions.</span></span> <span data-ttu-id="3b247-121">Per ulteriori informazioni sui valori della classe di priorità e del livello di priorità, vedere [priorità di pianificazione](/windows/desktop/ProcThread/scheduling-priorities).</span><span class="sxs-lookup"><span data-stu-id="3b247-121">For more information about the Priority Class and Priority Level values, see [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities).</span></span> <span data-ttu-id="3b247-122">Nella tabella seguente sono elencati i valori possibili per l'elemento **Priority** e i valori della classe di priorità e del livello di priorità corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="3b247-122">The following table lists the possible values for the **Priority** element, and the corresponding Priority Class and Priority Level values.</span></span>



| <span data-ttu-id="3b247-123">Priorità attività</span><span class="sxs-lookup"><span data-stu-id="3b247-123">Task Priority</span></span> | <span data-ttu-id="3b247-124">Classe Priority</span><span class="sxs-lookup"><span data-stu-id="3b247-124">Priority Class</span></span>                 | <span data-ttu-id="3b247-125">Livello di priorità</span><span class="sxs-lookup"><span data-stu-id="3b247-125">Priority Level</span></span>                   |
|---------------|--------------------------------|----------------------------------|
| <span data-ttu-id="3b247-126">0</span><span class="sxs-lookup"><span data-stu-id="3b247-126">0</span></span>             | <span data-ttu-id="3b247-127">\_classe priorità in tempo reale \_</span><span class="sxs-lookup"><span data-stu-id="3b247-127">REALTIME\_PRIORITY\_CLASS</span></span>      | <span data-ttu-id="3b247-128">\_tempo di priorità thread \_ \_ critico</span><span class="sxs-lookup"><span data-stu-id="3b247-128">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span> |
| <span data-ttu-id="3b247-129">1</span><span class="sxs-lookup"><span data-stu-id="3b247-129">1</span></span>             | <span data-ttu-id="3b247-130">\_classe con priorità alta \_</span><span class="sxs-lookup"><span data-stu-id="3b247-130">HIGH\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="3b247-131">\_priorità thread \_ più elevata</span><span class="sxs-lookup"><span data-stu-id="3b247-131">THREAD\_PRIORITY\_HIGHEST</span></span>        |
| <span data-ttu-id="3b247-132">2</span><span class="sxs-lookup"><span data-stu-id="3b247-132">2</span></span>             | <span data-ttu-id="3b247-133">\_classe di \_ priorità \_ normale sopra</span><span class="sxs-lookup"><span data-stu-id="3b247-133">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="3b247-134">\_priorità thread \_ superiore al \_ normale</span><span class="sxs-lookup"><span data-stu-id="3b247-134">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="3b247-135">3</span><span class="sxs-lookup"><span data-stu-id="3b247-135">3</span></span>             | <span data-ttu-id="3b247-136">\_classe di \_ priorità \_ normale sopra</span><span class="sxs-lookup"><span data-stu-id="3b247-136">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="3b247-137">\_priorità thread \_ superiore al \_ normale</span><span class="sxs-lookup"><span data-stu-id="3b247-137">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="3b247-138">4</span><span class="sxs-lookup"><span data-stu-id="3b247-138">4</span></span>             | <span data-ttu-id="3b247-139">\_classe di priorità normale \_</span><span class="sxs-lookup"><span data-stu-id="3b247-139">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="3b247-140">priorità THREAD- \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="3b247-140">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="3b247-141">5</span><span class="sxs-lookup"><span data-stu-id="3b247-141">5</span></span>             | <span data-ttu-id="3b247-142">\_classe di priorità normale \_</span><span class="sxs-lookup"><span data-stu-id="3b247-142">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="3b247-143">priorità THREAD- \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="3b247-143">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="3b247-144">6</span><span class="sxs-lookup"><span data-stu-id="3b247-144">6</span></span>             | <span data-ttu-id="3b247-145">\_classe di priorità normale \_</span><span class="sxs-lookup"><span data-stu-id="3b247-145">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="3b247-146">priorità THREAD- \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="3b247-146">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="3b247-147">7</span><span class="sxs-lookup"><span data-stu-id="3b247-147">7</span></span>             | <span data-ttu-id="3b247-148">classe di priorità inferiore al \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="3b247-148">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="3b247-149">priorità THREAD al di \_ \_ sotto del \_ normale</span><span class="sxs-lookup"><span data-stu-id="3b247-149">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="3b247-150">8</span><span class="sxs-lookup"><span data-stu-id="3b247-150">8</span></span>             | <span data-ttu-id="3b247-151">classe di priorità inferiore al \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="3b247-151">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="3b247-152">priorità THREAD al di \_ \_ sotto del \_ normale</span><span class="sxs-lookup"><span data-stu-id="3b247-152">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="3b247-153">9</span><span class="sxs-lookup"><span data-stu-id="3b247-153">9</span></span>             | <span data-ttu-id="3b247-154">\_classe priorità INattiva \_</span><span class="sxs-lookup"><span data-stu-id="3b247-154">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="3b247-155">\_priorità thread \_ più bassa</span><span class="sxs-lookup"><span data-stu-id="3b247-155">THREAD\_PRIORITY\_LOWEST</span></span>         |
| <span data-ttu-id="3b247-156">10</span><span class="sxs-lookup"><span data-stu-id="3b247-156">10</span></span>            | <span data-ttu-id="3b247-157">\_classe priorità INattiva \_</span><span class="sxs-lookup"><span data-stu-id="3b247-157">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="3b247-158">\_priorità thread \_ inattiva</span><span class="sxs-lookup"><span data-stu-id="3b247-158">THREAD\_PRIORITY\_IDLE</span></span>           |



 

<span data-ttu-id="3b247-159">Per lo sviluppo in C++, vedere [**proprietà Priority di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).</span><span class="sxs-lookup"><span data-stu-id="3b247-159">For C++ development, see [**Priority Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).</span></span>

<span data-ttu-id="3b247-160">Per lo sviluppo di script, vedere [**TaskSettings. Priority**](tasksettings-priority.md).</span><span class="sxs-lookup"><span data-stu-id="3b247-160">For script development, see [**TaskSettings.Priority**](tasksettings-priority.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b247-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b247-161">Requirements</span></span>



| <span data-ttu-id="3b247-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b247-162">Requirement</span></span> | <span data-ttu-id="3b247-163">Valore</span><span class="sxs-lookup"><span data-stu-id="3b247-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3b247-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b247-164">Minimum supported client</span></span><br/> | <span data-ttu-id="3b247-165">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b247-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3b247-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b247-166">Minimum supported server</span></span><br/> | <span data-ttu-id="3b247-167">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3b247-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b247-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b247-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b247-169">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3b247-169">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

