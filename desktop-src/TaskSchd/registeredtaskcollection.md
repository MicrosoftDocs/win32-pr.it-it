---
title: Oggetto RegisteredTaskCollection
description: Oggetto di scripting che contiene tutte le attività registrate.
ms.assetid: 0bd2010d-af25-4316-8829-62e4ec4761e2
keywords:
- Utilità di pianificazione oggetto RegisteredTaskCollection
- Oggetto RegisteredTaskCollection Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- RegisteredTaskCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11c299bc8817cc1627c40b3c465cd182e0f4c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048041"
---
# <a name="registeredtaskcollection-object"></a><span data-ttu-id="e6b76-105">Oggetto RegisteredTaskCollection</span><span class="sxs-lookup"><span data-stu-id="e6b76-105">RegisteredTaskCollection object</span></span>

<span data-ttu-id="e6b76-106">Oggetto di scripting che contiene tutte le attività registrate.</span><span class="sxs-lookup"><span data-stu-id="e6b76-106">Scripting object that contains all the tasks that are registered.</span></span>

## <a name="members"></a><span data-ttu-id="e6b76-107">Membri</span><span class="sxs-lookup"><span data-stu-id="e6b76-107">Members</span></span>

<span data-ttu-id="e6b76-108">L'oggetto **RegisteredTaskCollection** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e6b76-108">The **RegisteredTaskCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="e6b76-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e6b76-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e6b76-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e6b76-110">Properties</span></span>

<span data-ttu-id="e6b76-111">L'oggetto **RegisteredTaskCollection** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e6b76-111">The **RegisteredTaskCollection** object has these properties.</span></span>



| <span data-ttu-id="e6b76-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e6b76-112">Property</span></span>                                                   | <span data-ttu-id="e6b76-113">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="e6b76-113">Access type</span></span>          | <span data-ttu-id="e6b76-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6b76-114">Description</span></span>                                                        |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="e6b76-115">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="e6b76-115">**Count**</span></span>](registeredtaskcollection-count.md)<br/> | <span data-ttu-id="e6b76-116">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e6b76-116">Read-only</span></span><br/> | <span data-ttu-id="e6b76-117">Ottiene il numero di attività registrate nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="e6b76-117">Gets the number of registered tasks in the collection.</span></span><br/>  |
| [<span data-ttu-id="e6b76-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e6b76-118">**Item**</span></span>](registeredtaskcollection-item.md)<br/>   | <span data-ttu-id="e6b76-119">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e6b76-119">Read-only</span></span><br/> | <span data-ttu-id="e6b76-120">Ottiene l'attività registrata specificata dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="e6b76-120">Gets the specified registered task from the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="e6b76-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="e6b76-121">Examples</span></span>

<span data-ttu-id="e6b76-122">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [visualizzazione di nomi di attività e Stati (scripting)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="e6b76-122">For more information and example code for this scripting object, see [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6b76-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6b76-123">Requirements</span></span>



| <span data-ttu-id="e6b76-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6b76-124">Requirement</span></span> | <span data-ttu-id="e6b76-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e6b76-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6b76-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6b76-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e6b76-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6b76-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e6b76-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6b76-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e6b76-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e6b76-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6b76-130">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e6b76-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6b76-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e6b76-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e6b76-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e6b76-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6b76-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6b76-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6b76-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6b76-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6b76-135">**TaskFolder. GetTasks**</span><span class="sxs-lookup"><span data-stu-id="e6b76-135">**TaskFolder.GetTasks**</span></span>](taskfolder-gettasks.md)
</dt> </dl>

 

 





