---
title: Oggetto azione
description: Oggetto di scripting che fornisce le proprietà comuni ereditate da tutti gli oggetti azione.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- Utilità di pianificazione oggetto azione
- Utilità di pianificazione oggetto azione, descritto
topic_type:
- apiref
api_name:
- Action
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236b26cc4cfcd10f1e6e6094e4b69928343a9ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518238"
---
# <a name="action-object"></a><span data-ttu-id="a118f-105">Oggetto azione</span><span class="sxs-lookup"><span data-stu-id="a118f-105">Action object</span></span>

<span data-ttu-id="a118f-106">Oggetto di scripting che fornisce le proprietà comuni ereditate da tutti gli oggetti azione.</span><span class="sxs-lookup"><span data-stu-id="a118f-106">Scripting object that provides the common properties that are inherited by all action objects.</span></span> <span data-ttu-id="a118f-107">Un oggetto azione viene creato dal metodo [**ActionCollection. Create**](actioncollection-create.md) .</span><span class="sxs-lookup"><span data-stu-id="a118f-107">An action object is created by the [**ActionCollection.Create**](actioncollection-create.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="a118f-108">Membri</span><span class="sxs-lookup"><span data-stu-id="a118f-108">Members</span></span>

<span data-ttu-id="a118f-109">L'oggetto **azione** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a118f-109">The **Action** object has these types of members:</span></span>

-   [<span data-ttu-id="a118f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a118f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a118f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a118f-111">Properties</span></span>

<span data-ttu-id="a118f-112">L'oggetto **azione** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a118f-112">The **Action** object has these properties.</span></span>



| <span data-ttu-id="a118f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a118f-113">Property</span></span>                               | <span data-ttu-id="a118f-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="a118f-114">Access type</span></span>           | <span data-ttu-id="a118f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a118f-115">Description</span></span>                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [<span data-ttu-id="a118f-116">**ID**</span><span class="sxs-lookup"><span data-stu-id="a118f-116">**Id**</span></span>](action-id.md)<br/>     | <span data-ttu-id="a118f-117">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a118f-117">Read/write</span></span><br/> | <span data-ttu-id="a118f-118">Ottiene o imposta l'identificatore dell'azione.</span><span class="sxs-lookup"><span data-stu-id="a118f-118">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="a118f-119">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a118f-119">**Type**</span></span>](action-type.md)<br/> | <span data-ttu-id="a118f-120">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a118f-120">Read-only</span></span><br/>  | <span data-ttu-id="a118f-121">Ottiene il tipo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="a118f-121">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="a118f-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a118f-122">Remarks</span></span>

<span data-ttu-id="a118f-123">Per informazioni sul funzionamento combinato di azioni e attività, vedere [azioni attività](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="a118f-123">For information on how actions and tasks work together, see [Task Actions](task-actions.md).</span></span> <span data-ttu-id="a118f-124">Nella tabella seguente sono inclusi gli oggetti di scripting che rappresentano le azioni che è possibile eseguire:</span><span class="sxs-lookup"><span data-stu-id="a118f-124">The following table contains the scripting objects that represent the actions that can be performed:</span></span>



| <span data-ttu-id="a118f-125">API</span><span class="sxs-lookup"><span data-stu-id="a118f-125">API</span></span>                                            | <span data-ttu-id="a118f-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a118f-126">Description</span></span>                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="a118f-127">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="a118f-127">**ComHandlerAction**</span></span>](comhandleraction.md)   | <span data-ttu-id="a118f-128">Rappresenta un'azione che attiva un gestore.</span><span class="sxs-lookup"><span data-stu-id="a118f-128">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="a118f-129">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="a118f-129">**ExecAction**</span></span>](execaction.md)               | <span data-ttu-id="a118f-130">Rappresenta un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="a118f-130">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="a118f-131">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="a118f-131">**EmailAction**</span></span>](emailaction.md)             | <span data-ttu-id="a118f-132">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="a118f-132">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="a118f-133">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="a118f-133">**ShowMessageAction**</span></span>](showmessageaction.md) | <span data-ttu-id="a118f-134">Rappresenta un'azione che visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="a118f-134">Represents an action that shows a message box.</span></span>               |



 

<span data-ttu-id="a118f-135">Durante la lettura o la scrittura di codice XML, le azioni di un'attività vengono specificate nell'elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="a118f-135">When reading or writing XML, the actions of a task are specified in the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="a118f-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="a118f-136">Examples</span></span>

<span data-ttu-id="a118f-137">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere esempio di [trigger di ora (script)](time-trigger-example--scripting-.md) , esempio di [trigger di evento (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))scripting), [esempio di trigger giornaliero (scripting)](daily-trigger-example--scripting-.md), [esempio di trigger di registrazione (scripting)](registration-trigger-example--scripting-.md), [esempio di trigger settimanale (scripting)](weekly-trigger-example--scripting-.md), esempio di trigger [Logon (](logon-trigger-example--scripting-.md)scripting) o [esempio di trigger di avvio (script](boot-trigger-example--scripting-.md)</span><span class="sxs-lookup"><span data-stu-id="a118f-137">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) , [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a118f-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a118f-138">Requirements</span></span>



| <span data-ttu-id="a118f-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a118f-139">Requirement</span></span> | <span data-ttu-id="a118f-140">Valore</span><span class="sxs-lookup"><span data-stu-id="a118f-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a118f-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a118f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a118f-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a118f-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a118f-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a118f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a118f-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a118f-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a118f-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a118f-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="a118f-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a118f-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a118f-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a118f-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a118f-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a118f-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a118f-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a118f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a118f-150">Oggetti di scripting Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="a118f-150">Task Scheduler Scripting Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="a118f-151">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="a118f-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





