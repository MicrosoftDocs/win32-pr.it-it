---
title: Oggetto TriggerCollection (Windows. UI. XAML. h)
description: Oggetto di scripting utilizzato per aggiungere, rimuovere e recuperare i trigger di un'attività.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- Triggers Utilità di pianificazione, trigger Collection (oggetto)
- Utilità di pianificazione oggetto TriggerCollection
- Utilità di pianificazione oggetto TriggerCollection, descritto
topic_type:
- apiref
api_name:
- TriggerCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29f7288d8db0b56fc9cc8b3de7ace8c10c13959a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119379"
---
# <a name="triggercollection-object"></a><span data-ttu-id="5c1f2-106">TriggerCollection (oggetto)</span><span class="sxs-lookup"><span data-stu-id="5c1f2-106">TriggerCollection object</span></span>

<span data-ttu-id="5c1f2-107">Oggetto di scripting utilizzato per aggiungere, rimuovere e recuperare i trigger di un'attività.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-107">Scripting object that is used to add to, remove from, and retrieve the triggers of a task.</span></span>

## <a name="members"></a><span data-ttu-id="5c1f2-108">Membri</span><span class="sxs-lookup"><span data-stu-id="5c1f2-108">Members</span></span>

<span data-ttu-id="5c1f2-109">L'oggetto **TriggerCollection** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5c1f2-109">The **TriggerCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="5c1f2-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="5c1f2-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5c1f2-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c1f2-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5c1f2-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="5c1f2-112">Methods</span></span>

<span data-ttu-id="5c1f2-113">Questi metodi sono disponibili nell'oggetto **TriggerCollection** .</span><span class="sxs-lookup"><span data-stu-id="5c1f2-113">The **TriggerCollection** object has these methods.</span></span>



| <span data-ttu-id="5c1f2-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="5c1f2-114">Method</span></span>                                     | <span data-ttu-id="5c1f2-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c1f2-115">Description</span></span>                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c1f2-116">**Deselezionare**</span><span class="sxs-lookup"><span data-stu-id="5c1f2-116">**Clear**</span></span>](triggercollection-clear.md)   | <span data-ttu-id="5c1f2-117">Cancella tutti i trigger dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-117">Clears all triggers from the collection.</span></span><br/>                                        |
| [<span data-ttu-id="5c1f2-118">**Creare**</span><span class="sxs-lookup"><span data-stu-id="5c1f2-118">**Create**</span></span>](triggercollection-create.md) | <span data-ttu-id="5c1f2-119">Crea un nuovo trigger per l'attività.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-119">Creates a new trigger for the task.</span></span><br/>                                             |
| [<span data-ttu-id="5c1f2-120">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="5c1f2-120">**Remove**</span></span>](triggercollection-remove.md) | <span data-ttu-id="5c1f2-121">Rimuove il trigger specificato dalla raccolta di trigger utilizzati dall'attività.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-121">Removes the specified trigger from the collection of triggers used by the task.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5c1f2-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c1f2-122">Properties</span></span>

<span data-ttu-id="5c1f2-123">Queste proprietà sono impostate dall'oggetto **TriggerCollection** .</span><span class="sxs-lookup"><span data-stu-id="5c1f2-123">The **TriggerCollection** object has these properties.</span></span>



| <span data-ttu-id="5c1f2-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c1f2-124">Property</span></span>                                            | <span data-ttu-id="5c1f2-125">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="5c1f2-125">Access type</span></span>          | <span data-ttu-id="5c1f2-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c1f2-126">Description</span></span>                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="5c1f2-127">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="5c1f2-127">**Count**</span></span>](triggercollection-count.md)<br/> | <span data-ttu-id="5c1f2-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c1f2-128">Read-only</span></span><br/> | <span data-ttu-id="5c1f2-129">Ottiene il numero di trigger nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-129">Gets the number of triggers in the collection.</span></span><br/>  |
| [<span data-ttu-id="5c1f2-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5c1f2-130">**Item**</span></span>](triggercollection-item.md)<br/>   | <span data-ttu-id="5c1f2-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c1f2-131">Read-only</span></span><br/> | <span data-ttu-id="5c1f2-132">Ottiene il trigger specificato dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-132">Gets the specified trigger from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c1f2-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c1f2-133">Remarks</span></span>

<span data-ttu-id="5c1f2-134">Durante la lettura o la scrittura di codice XML per un'attività, i trigger per l'attività vengono specificati nell'elemento [**trigger**](taskschedulerschema-triggers-tasktype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-134">When reading or writing XML for a task, the triggers for the task are specified in the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="5c1f2-135">Per informazioni su ogni tipo di trigger, vedere [tipi di trigger](trigger-types.md).</span><span class="sxs-lookup"><span data-stu-id="5c1f2-135">For information about each trigger type see [Trigger Types](trigger-types.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5c1f2-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c1f2-136">Examples</span></span>

<span data-ttu-id="5c1f2-137">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="5c1f2-137">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c1f2-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c1f2-138">Requirements</span></span>



| <span data-ttu-id="5c1f2-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c1f2-139">Requirement</span></span> | <span data-ttu-id="5c1f2-140">Valore</span><span class="sxs-lookup"><span data-stu-id="5c1f2-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c1f2-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c1f2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5c1f2-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c1f2-142">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5c1f2-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c1f2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5c1f2-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c1f2-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5c1f2-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c1f2-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c1f2-146"><dt>Windows. UI. XAML. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c1f2-146"><dt>Windows.ui.xaml.h</dt></span></span> </dl> |
| <span data-ttu-id="5c1f2-147">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5c1f2-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c1f2-148"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5c1f2-148"><dt>Taskschd.tlb</dt></span></span> </dl>      |
| <span data-ttu-id="5c1f2-149">DLL</span><span class="sxs-lookup"><span data-stu-id="5c1f2-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c1f2-150"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c1f2-150"><dt>Taskschd.dll</dt></span></span> </dl>      |



## <a name="see-also"></a><span data-ttu-id="5c1f2-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c1f2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c1f2-152">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="5c1f2-152">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





