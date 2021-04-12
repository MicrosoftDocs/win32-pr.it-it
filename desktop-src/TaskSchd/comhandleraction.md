---
title: Oggetto ComHandlerAction
description: Oggetto di scripting che rappresenta un'azione che attiva un gestore.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- Utilità di pianificazione azione gestore COM, oggetto
- Utilità di pianificazione oggetto ComHandlerAction
- Oggetto ComHandlerAction Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- ComHandlerAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d7e8371deda260c407682181fd31e29886b777
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475046"
---
# <a name="comhandleraction-object"></a><span data-ttu-id="4b714-106">Oggetto ComHandlerAction</span><span class="sxs-lookup"><span data-stu-id="4b714-106">ComHandlerAction object</span></span>

<span data-ttu-id="4b714-107">Oggetto di scripting che rappresenta un'azione che attiva un gestore.</span><span class="sxs-lookup"><span data-stu-id="4b714-107">Scripting object that represents an action that fires a handler.</span></span>

## <a name="members"></a><span data-ttu-id="4b714-108">Membri</span><span class="sxs-lookup"><span data-stu-id="4b714-108">Members</span></span>

<span data-ttu-id="4b714-109">L'oggetto **ComHandlerAction** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4b714-109">The **ComHandlerAction** object has these types of members:</span></span>

-   [<span data-ttu-id="4b714-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b714-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b714-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b714-111">Properties</span></span>

<span data-ttu-id="4b714-112">L'oggetto **ComHandlerAction** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4b714-112">The **ComHandlerAction** object has these properties.</span></span>



| <span data-ttu-id="4b714-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b714-113">Property</span></span>                                               | <span data-ttu-id="4b714-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="4b714-114">Access type</span></span>           | <span data-ttu-id="4b714-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b714-115">Description</span></span>                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b714-116">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="4b714-116">**ClassId**</span></span>](comhandleraction-classid.md)<br/> | <span data-ttu-id="4b714-117">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4b714-117">Read/write</span></span><br/> | <span data-ttu-id="4b714-118">Ottiene o imposta l'identificatore della classe del gestore.</span><span class="sxs-lookup"><span data-stu-id="4b714-118">Gets or sets the identifier of the handler class.</span></span><br/>                                              |
| [<span data-ttu-id="4b714-119">**Data**</span><span class="sxs-lookup"><span data-stu-id="4b714-119">**Data**</span></span>](comhandleraction-data.md)<br/>       | <span data-ttu-id="4b714-120">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4b714-120">Read/write</span></span><br/> | <span data-ttu-id="4b714-121">Ottiene o imposta dati aggiuntivi associati al gestore.</span><span class="sxs-lookup"><span data-stu-id="4b714-121">Gets or sets additional data that is associated with the handler.</span></span><br/>                              |
| [<span data-ttu-id="4b714-122">**ID**</span><span class="sxs-lookup"><span data-stu-id="4b714-122">**Id**</span></span>](action-id.md)<br/>                     | <span data-ttu-id="4b714-123">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4b714-123">Read/write</span></span><br/> | <span data-ttu-id="4b714-124">Ereditato dall'oggetto [**azione**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="4b714-124">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="4b714-125">Ottiene o imposta l'identificatore dell'azione.</span><span class="sxs-lookup"><span data-stu-id="4b714-125">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="4b714-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4b714-126">**Type**</span></span>](action-type.md)<br/>                 | <span data-ttu-id="4b714-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b714-127">Read-only</span></span><br/>  | <span data-ttu-id="4b714-128">Ereditato dall'oggetto [**azione**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="4b714-128">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="4b714-129">Ottiene il tipo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="4b714-129">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="4b714-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b714-130">Remarks</span></span>

<span data-ttu-id="4b714-131">I gestori COM devono implementare l'interfaccia [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) per l'utilità di pianificazione per avviare e arrestare il gestore.</span><span class="sxs-lookup"><span data-stu-id="4b714-131">COM handlers must implement the [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) interface for the Task Scheduler to start and stop the handler.</span></span> <span data-ttu-id="4b714-132">Il gestore COM utilizza a sua volta i metodi dell'oggetto [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) per comunicare lo stato al utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="4b714-132">In turn, the COM handler uses the methods of the [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) object to communicate the status back to the Task Scheduler.</span></span>

<span data-ttu-id="4b714-133">Durante la lettura o la scrittura di codice XML, un'azione del gestore COM viene specificata nell'elemento [**Comhandler**](taskschedulerschema-comhandler-actiongroup-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="4b714-133">When reading or writing XML, a COM handler action is specified in the [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b714-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b714-134">Requirements</span></span>



| <span data-ttu-id="4b714-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b714-135">Requirement</span></span> | <span data-ttu-id="4b714-136">Valore</span><span class="sxs-lookup"><span data-stu-id="4b714-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b714-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b714-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4b714-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b714-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4b714-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b714-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4b714-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4b714-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b714-141">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4b714-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="4b714-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4b714-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4b714-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4b714-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b714-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b714-144"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b714-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b714-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b714-146">**TaskHandlerStatus**</span><span class="sxs-lookup"><span data-stu-id="4b714-146">**TaskHandlerStatus**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[<span data-ttu-id="4b714-147">Oggetti Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="4b714-147">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="4b714-148">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="4b714-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





