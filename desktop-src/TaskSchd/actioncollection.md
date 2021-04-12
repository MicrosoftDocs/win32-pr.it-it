---
title: Oggetto ActionCollection
description: Oggetto di scripting che contiene le azioni eseguite dall'attività.
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- Utilità di pianificazione azioni, oggetto Collection
- Utilità di pianificazione oggetto ActionCollection
- Utilità di pianificazione oggetto ActionCollection, descritto
topic_type:
- apiref
api_name:
- ActionCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dee7182cc79684dec1fd052f7ad67409ba513f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519142"
---
# <a name="actioncollection-object"></a><span data-ttu-id="55d24-106">Oggetto ActionCollection</span><span class="sxs-lookup"><span data-stu-id="55d24-106">ActionCollection object</span></span>

<span data-ttu-id="55d24-107">Oggetto di scripting che contiene le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="55d24-107">Scripting object that contains the actions performed by the task.</span></span>

## <a name="members"></a><span data-ttu-id="55d24-108">Membri</span><span class="sxs-lookup"><span data-stu-id="55d24-108">Members</span></span>

<span data-ttu-id="55d24-109">L'oggetto **ActionCollection** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="55d24-109">The **ActionCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="55d24-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="55d24-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="55d24-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="55d24-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="55d24-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="55d24-112">Methods</span></span>

<span data-ttu-id="55d24-113">Questi metodi sono disponibili nell'oggetto **ActionCollection** .</span><span class="sxs-lookup"><span data-stu-id="55d24-113">The **ActionCollection** object has these methods.</span></span>



| <span data-ttu-id="55d24-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="55d24-114">Method</span></span>                                    | <span data-ttu-id="55d24-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55d24-115">Description</span></span>                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="55d24-116">**Deselezionare**</span><span class="sxs-lookup"><span data-stu-id="55d24-116">**Clear**</span></span>](actioncollection-clear.md)   | <span data-ttu-id="55d24-117">Cancella tutte le azioni dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="55d24-117">Clears all the actions from the collection.</span></span><br/>      |
| [<span data-ttu-id="55d24-118">**Creare**</span><span class="sxs-lookup"><span data-stu-id="55d24-118">**Create**</span></span>](actioncollection-create.md) | <span data-ttu-id="55d24-119">Crea e aggiunge una nuova azione alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="55d24-119">Creates and adds a new action to the collection.</span></span><br/> |
| [<span data-ttu-id="55d24-120">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="55d24-120">**Remove**</span></span>](actioncollection-remove.md) | <span data-ttu-id="55d24-121">Rimuove un'azione specificata dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="55d24-121">Removes a specified action from the collection.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="55d24-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="55d24-122">Properties</span></span>

<span data-ttu-id="55d24-123">L'oggetto **ActionCollection** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="55d24-123">The **ActionCollection** object has these properties.</span></span>



| <span data-ttu-id="55d24-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="55d24-124">Property</span></span>                                               | <span data-ttu-id="55d24-125">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="55d24-125">Access type</span></span>           | <span data-ttu-id="55d24-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55d24-126">Description</span></span>                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="55d24-127">**Context**</span><span class="sxs-lookup"><span data-stu-id="55d24-127">**Context**</span></span>](actioncollection-context.md)<br/> | <span data-ttu-id="55d24-128">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="55d24-128">Read/write</span></span><br/> | <span data-ttu-id="55d24-129">Ottiene o imposta l'identificatore dell'entità per l'attività.</span><span class="sxs-lookup"><span data-stu-id="55d24-129">Gets or sets the identifier of the principal for the task.</span></span><br/> |
| [<span data-ttu-id="55d24-130">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="55d24-130">**Count**</span></span>](actioncollection-count.md)<br/>     | <span data-ttu-id="55d24-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d24-131">Read-only</span></span><br/>  | <span data-ttu-id="55d24-132">Ottiene il numero di azioni nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="55d24-132">Gets the number of actions in the collection.</span></span><br/>              |
| [<span data-ttu-id="55d24-133">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="55d24-133">**Item**</span></span>](actioncollection-item.md)<br/>       | <span data-ttu-id="55d24-134">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="55d24-134">Read-only</span></span><br/>  | <span data-ttu-id="55d24-135">Ottiene un'azione specificata dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="55d24-135">Gets a specified action from the collection.</span></span><br/>               |
| [<span data-ttu-id="55d24-136">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="55d24-136">**XmlText**</span></span>](actioncollection-xmltext.md)<br/> | <span data-ttu-id="55d24-137">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="55d24-137">Read/write</span></span><br/> | <span data-ttu-id="55d24-138">Ottiene o imposta una versione in formato XML della raccolta.</span><span class="sxs-lookup"><span data-stu-id="55d24-138">Gets or sets an XML-formatted version of the collection.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="55d24-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="55d24-139">Remarks</span></span>

<span data-ttu-id="55d24-140">Durante la lettura o la scrittura di codice XML, le azioni di un'attività vengono specificate nell'elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="55d24-140">When reading or writing XML, the actions of a task are specified in the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="55d24-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="55d24-141">Examples</span></span>

<span data-ttu-id="55d24-142">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere esempio di [trigger di ora (script)](time-trigger-example--scripting-.md), esempio di [trigger di evento (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))scripting), [esempio di trigger giornaliero (scripting)](daily-trigger-example--scripting-.md), [esempio di trigger di registrazione (scripting)](registration-trigger-example--scripting-.md), [esempio di trigger settimanale (scripting)](weekly-trigger-example--scripting-.md), esempio di trigger [Logon (](logon-trigger-example--scripting-.md)scripting) o [esempio di trigger di avvio (script](boot-trigger-example--scripting-.md)</span><span class="sxs-lookup"><span data-stu-id="55d24-142">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55d24-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55d24-143">Requirements</span></span>



| <span data-ttu-id="55d24-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="55d24-144">Requirement</span></span> | <span data-ttu-id="55d24-145">Valore</span><span class="sxs-lookup"><span data-stu-id="55d24-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55d24-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55d24-146">Minimum supported client</span></span><br/> | <span data-ttu-id="55d24-147">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55d24-147">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="55d24-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55d24-148">Minimum supported server</span></span><br/> | <span data-ttu-id="55d24-149">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="55d24-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55d24-150">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="55d24-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="55d24-151"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="55d24-151"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="55d24-152">DLL</span><span class="sxs-lookup"><span data-stu-id="55d24-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55d24-153"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55d24-153"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





