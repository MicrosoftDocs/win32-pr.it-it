---
title: Actions (taskType)-elemento
description: Contiene le azioni eseguite dall'attività.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Actions (taskType)-elemento Utilità di pianificazione
- Utilità di pianificazione azioni, XML
- Elemento Actions Utilità di pianificazione
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21af0f8a06faa9cdc61917dcb3b3b0672c47e0e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400407"
---
# <a name="actions-tasktype-element"></a><span data-ttu-id="439ec-106">Actions (taskType)-elemento</span><span class="sxs-lookup"><span data-stu-id="439ec-106">Actions (taskType) Element</span></span>

<span data-ttu-id="439ec-107">Contiene le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="439ec-107">Contains the actions performed by the task.</span></span>

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

<span data-ttu-id="439ec-108">L'elemento **Actions** viene definito dal tipo complesso [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="439ec-108">The **Actions** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="439ec-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="439ec-109">Parent element</span></span>



| <span data-ttu-id="439ec-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="439ec-110">Element</span></span>                                          | <span data-ttu-id="439ec-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="439ec-111">Derived from</span></span>                                                 | <span data-ttu-id="439ec-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="439ec-112">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="439ec-113">**Attività**</span><span class="sxs-lookup"><span data-stu-id="439ec-113">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="439ec-114">**taskType**</span><span class="sxs-lookup"><span data-stu-id="439ec-114">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="439ec-115">Descrive l'attività eseguita dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="439ec-115">Describes the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="439ec-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="439ec-116">Child elements</span></span>



| <span data-ttu-id="439ec-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="439ec-117">Element</span></span>                                                                    | <span data-ttu-id="439ec-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="439ec-118">Type</span></span>                                                                       | <span data-ttu-id="439ec-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="439ec-119">Description</span></span>                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="439ec-120">**Comgestore**</span><span class="sxs-lookup"><span data-stu-id="439ec-120">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | [<span data-ttu-id="439ec-121">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="439ec-121">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)   | <span data-ttu-id="439ec-122">Specifica un'azione che attiva un gestore.</span><span class="sxs-lookup"><span data-stu-id="439ec-122">Specifies an action that fires a handler.</span></span><br/>                   |
| [<span data-ttu-id="439ec-123">**Exec**</span><span class="sxs-lookup"><span data-stu-id="439ec-123">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | [<span data-ttu-id="439ec-124">**execType**</span><span class="sxs-lookup"><span data-stu-id="439ec-124">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)               | <span data-ttu-id="439ec-125">Specifica un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="439ec-125">Specifies an action that executes a command-line operation.</span></span><br/> |
| [<span data-ttu-id="439ec-126">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="439ec-126">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | [<span data-ttu-id="439ec-127">**sendEmailType**</span><span class="sxs-lookup"><span data-stu-id="439ec-127">**sendEmailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)     | <span data-ttu-id="439ec-128">Specifica un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="439ec-128">Specifies an action that sends an email message.</span></span><br/>            |
| [<span data-ttu-id="439ec-129">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="439ec-129">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="439ec-130">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="439ec-130">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="439ec-131">Specifica un'azione che visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="439ec-131">Specifies an action that shows a message box.</span></span><br/>               |



## <a name="attributes"></a><span data-ttu-id="439ec-132">Attributi</span><span class="sxs-lookup"><span data-stu-id="439ec-132">Attributes</span></span>



| <span data-ttu-id="439ec-133">Nome</span><span class="sxs-lookup"><span data-stu-id="439ec-133">Name</span></span>    | <span data-ttu-id="439ec-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="439ec-134">Type</span></span> | <span data-ttu-id="439ec-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="439ec-135">Description</span></span>                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="439ec-136">Context</span><span class="sxs-lookup"><span data-stu-id="439ec-136">Context</span></span> |      | <span data-ttu-id="439ec-137">Identificatore principale dell'utente che rappresenta il contesto di sicurezza per le azioni dell'attività.</span><span class="sxs-lookup"><span data-stu-id="439ec-137">Principal identifier of the user who is the security context for the actions of the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="439ec-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="439ec-138">Remarks</span></span>

<span data-ttu-id="439ec-139">Gli elementi figlio elencati in precedenza (massimo 32) sono definiti dal gruppo [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="439ec-139">The child elements listed previously (maximum 32) are defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) group.</span></span> <span data-ttu-id="439ec-140">Questi elementi possono essere aggiunti in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="439ec-140">These elements can be added in any order.</span></span>

<span data-ttu-id="439ec-141">Per lo sviluppo in C++, le azioni di un'attività sono definite nell'interfaccia [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) .</span><span class="sxs-lookup"><span data-stu-id="439ec-141">For C++ development, the actions of a task are defined in the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface.</span></span>

<span data-ttu-id="439ec-142">Per lo sviluppo di script, le azioni di un'attività sono definite nell'oggetto [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="439ec-142">For script development, the actions of a task are defined in the [**ActionCollection**](actioncollection.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="439ec-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="439ec-143">Examples</span></span>

<span data-ttu-id="439ec-144">Per ulteriori informazioni e un esempio completo del codice XML per un'attività che contiene una singola azione di esecuzione, vedere l'esempio relativo al [trigger temporale (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="439ec-144">For more information and a complete example of the XML for a task that contains a single execution action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="439ec-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="439ec-145">Requirements</span></span>



| <span data-ttu-id="439ec-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="439ec-146">Requirement</span></span> | <span data-ttu-id="439ec-147">Valore</span><span class="sxs-lookup"><span data-stu-id="439ec-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="439ec-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="439ec-148">Minimum supported client</span></span><br/> | <span data-ttu-id="439ec-149">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="439ec-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="439ec-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="439ec-150">Minimum supported server</span></span><br/> | <span data-ttu-id="439ec-151">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="439ec-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="439ec-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="439ec-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="439ec-153">**taskType**</span><span class="sxs-lookup"><span data-stu-id="439ec-153">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[<span data-ttu-id="439ec-154">**actionGroup**</span><span class="sxs-lookup"><span data-stu-id="439ec-154">**actionGroup**</span></span>](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[<span data-ttu-id="439ec-155">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="439ec-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="439ec-156">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="439ec-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





