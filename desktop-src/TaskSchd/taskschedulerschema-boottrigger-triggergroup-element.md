---
title: Elemento BootTrigger (triggerGroup)
description: Specifica un trigger che avvia un'attività quando viene avviato il sistema.
ms.assetid: c6833547-0daf-4e8a-b8c5-b422827b1d96
keywords:
- trigger di avvio Utilità di pianificazione, elemento XML
- Utilità di pianificazione elemento BootTrigger
topic_type:
- apiref
api_name:
- BootTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb6ccf590893e19340662fd4c47e4aa68047b29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340952"
---
# <a name="boottrigger-triggergroup-element"></a><span data-ttu-id="dca95-105">Elemento BootTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="dca95-105">BootTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="dca95-106">Specifica un trigger che avvia un'attività quando viene avviato il sistema.</span><span class="sxs-lookup"><span data-stu-id="dca95-106">Specifies a trigger that starts a task when the system is booted.</span></span>

``` syntax
<xs:element name="BootTrigger"
    type="bootTriggerType"
 />
```

<span data-ttu-id="dca95-107">L'elemento **BootTrigger** è definito dal tipo complesso [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="dca95-107">The **BootTrigger** element is defined by the [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="dca95-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="dca95-108">Parent element</span></span>



| <span data-ttu-id="dca95-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="dca95-109">Element</span></span>                                                           | <span data-ttu-id="dca95-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="dca95-110">Derived from</span></span>                                                         | <span data-ttu-id="dca95-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca95-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="dca95-112">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="dca95-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="dca95-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="dca95-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="dca95-114">Specifica i trigger che avviano l'attività.</span><span class="sxs-lookup"><span data-stu-id="dca95-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="dca95-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="dca95-115">Child elements</span></span>



| <span data-ttu-id="dca95-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="dca95-116">Element</span></span>                                                                                                        | <span data-ttu-id="dca95-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="dca95-117">Type</span></span>                                                                     | <span data-ttu-id="dca95-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca95-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dca95-119">**Ritardo (bootTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="dca95-119">**Delay (bootTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)                           | <span data-ttu-id="dca95-120">duration</span><span class="sxs-lookup"><span data-stu-id="dca95-120">duration</span></span>                                                                 | <span data-ttu-id="dca95-121">Specifica l'intervallo di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="dca95-121">Specifies the amount of time between when the system is booted and when the task is started.</span></span><br/>                            |
| [<span data-ttu-id="dca95-122">**Abilitato (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dca95-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="dca95-123">boolean</span><span class="sxs-lookup"><span data-stu-id="dca95-123">boolean</span></span>                                                                  | <span data-ttu-id="dca95-124">Specifica che il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="dca95-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="dca95-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dca95-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="dca95-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="dca95-126">dateTime</span></span>                                                                 | <span data-ttu-id="dca95-127">Specifica la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="dca95-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="dca95-128">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="dca95-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="dca95-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dca95-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="dca95-130">duration</span><span class="sxs-lookup"><span data-stu-id="dca95-130">duration</span></span>                                                                 | <span data-ttu-id="dca95-131">Specifica l'intervallo di tempo massimo in cui l'attività può essere avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="dca95-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="dca95-132">**Ripetizione (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dca95-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="dca95-133">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="dca95-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="dca95-134">Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="dca95-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="dca95-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dca95-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="dca95-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="dca95-136">dateTime</span></span>                                                                 | <span data-ttu-id="dca95-137">Specifica la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="dca95-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="dca95-138">Attributi</span><span class="sxs-lookup"><span data-stu-id="dca95-138">Attributes</span></span>



| <span data-ttu-id="dca95-139">Nome</span><span class="sxs-lookup"><span data-stu-id="dca95-139">Name</span></span> | <span data-ttu-id="dca95-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="dca95-140">Type</span></span>       | <span data-ttu-id="dca95-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca95-141">Description</span></span>                               |
|------|------------|-------------------------------------------|
| <span data-ttu-id="dca95-142">Id</span><span class="sxs-lookup"><span data-stu-id="dca95-142">Id</span></span>   | <span data-ttu-id="dca95-143">**string**</span><span class="sxs-lookup"><span data-stu-id="dca95-143">**string**</span></span> | <span data-ttu-id="dca95-144">Identificatore del trigger.</span><span class="sxs-lookup"><span data-stu-id="dca95-144">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dca95-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="dca95-145">Remarks</span></span>

<span data-ttu-id="dca95-146">Per lo sviluppo di script, un trigger di avvio viene definito dall'oggetto [**BootTrigger**](boottrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="dca95-146">For script development, a boot trigger is defined by the [**BootTrigger**](boottrigger.md) object.</span></span>

<span data-ttu-id="dca95-147">Per lo sviluppo in C++, un trigger di avvio viene definito dall'oggetto [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) .</span><span class="sxs-lookup"><span data-stu-id="dca95-147">For C++ development, a boot trigger is defined by the [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) object.</span></span>

## <a name="examples"></a><span data-ttu-id="dca95-148">Esempio</span><span class="sxs-lookup"><span data-stu-id="dca95-148">Examples</span></span>

<span data-ttu-id="dca95-149">Per un esempio completo del codice XML per un'attività che specifica un trigger di avvio, vedere [esempio di trigger di avvio (XML)](boot-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="dca95-149">For a complete example of the XML for a task that specifies a boot trigger, see [Boot Trigger Example (XML)](boot-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dca95-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dca95-150">Requirements</span></span>



| <span data-ttu-id="dca95-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="dca95-151">Requirement</span></span> | <span data-ttu-id="dca95-152">Valore</span><span class="sxs-lookup"><span data-stu-id="dca95-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dca95-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dca95-153">Minimum supported client</span></span><br/> | <span data-ttu-id="dca95-154">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dca95-154">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dca95-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dca95-155">Minimum supported server</span></span><br/> | <span data-ttu-id="dca95-156">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dca95-156">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dca95-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dca95-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dca95-158">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="dca95-158">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="dca95-159">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="dca95-159">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





