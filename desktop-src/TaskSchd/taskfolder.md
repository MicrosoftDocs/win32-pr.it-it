---
title: Oggetto TaskFolder
description: Oggetto di scripting che fornisce i metodi utilizzati per registrare (creare) attività nella cartella, rimuovere attività dalla cartella e creare o rimuovere sottocartelle dalla cartella.
ms.assetid: f6fd09ec-2777-4903-83b5-e3ac1aa472a0
keywords:
- Utilità di pianificazione oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- TaskFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ccad9331cf3df12ea5752fdd7e5ac94bfbeba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518598"
---
# <a name="taskfolder-object"></a><span data-ttu-id="c7850-105">Oggetto TaskFolder</span><span class="sxs-lookup"><span data-stu-id="c7850-105">TaskFolder object</span></span>

<span data-ttu-id="c7850-106">Oggetto di scripting che fornisce i metodi utilizzati per registrare (creare) attività nella cartella, rimuovere attività dalla cartella e creare o rimuovere sottocartelle dalla cartella.</span><span class="sxs-lookup"><span data-stu-id="c7850-106">Scripting object that provides the methods that are used to register (create) tasks in the folder, remove tasks from the folder, and create or remove subfolders from the folder.</span></span>

## <a name="members"></a><span data-ttu-id="c7850-107">Membri</span><span class="sxs-lookup"><span data-stu-id="c7850-107">Members</span></span>

<span data-ttu-id="c7850-108">L'oggetto **TaskFolder** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c7850-108">The **TaskFolder** object has these types of members:</span></span>

-   [<span data-ttu-id="c7850-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="c7850-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c7850-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c7850-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c7850-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="c7850-111">Methods</span></span>

<span data-ttu-id="c7850-112">L'oggetto **TaskFolder** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c7850-112">The **TaskFolder** object has these methods.</span></span>



| <span data-ttu-id="c7850-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="c7850-113">Method</span></span>                                                              | <span data-ttu-id="c7850-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7850-114">Description</span></span>                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7850-115">**CreateFolder**</span><span class="sxs-lookup"><span data-stu-id="c7850-115">**CreateFolder**</span></span>](taskfolder-createfolder.md)                     | <span data-ttu-id="c7850-116">Crea una cartella per le attività correlate.</span><span class="sxs-lookup"><span data-stu-id="c7850-116">Creates a folder for related tasks.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="c7850-117">**DeleteFolder**</span><span class="sxs-lookup"><span data-stu-id="c7850-117">**DeleteFolder**</span></span>](taskfolder-deletefolder.md)                     | <span data-ttu-id="c7850-118">Elimina una sottocartella dalla cartella padre.</span><span class="sxs-lookup"><span data-stu-id="c7850-118">Deletes a subfolder from the parent folder.</span></span><br/>                                                                                         |
| [<span data-ttu-id="c7850-119">**DeleteTask**</span><span class="sxs-lookup"><span data-stu-id="c7850-119">**DeleteTask**</span></span>](taskfolder-deletetask.md)                         | <span data-ttu-id="c7850-120">Elimina un'attività dalla cartella.</span><span class="sxs-lookup"><span data-stu-id="c7850-120">Deletes a task from the folder.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="c7850-121">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="c7850-121">**GetFolder**</span></span>](taskfolder-getfolder.md)                           | <span data-ttu-id="c7850-122">Ottiene una cartella che contiene le attività in una posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="c7850-122">Gets a folder that contains tasks at a specified location.</span></span><br/>                                                                          |
| [<span data-ttu-id="c7850-123">**GetFolders**</span><span class="sxs-lookup"><span data-stu-id="c7850-123">**GetFolders**</span></span>](taskfolder-getfolders.md)                         | <span data-ttu-id="c7850-124">Ottiene tutte le sottocartelle nella cartella.</span><span class="sxs-lookup"><span data-stu-id="c7850-124">Gets all the subfolders in the folder.</span></span><br/>                                                                                              |
| [<span data-ttu-id="c7850-125">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c7850-125">**GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)   | <span data-ttu-id="c7850-126">Ottiene il descrittore di sicurezza per la cartella.</span><span class="sxs-lookup"><span data-stu-id="c7850-126">Gets the security descriptor for the folder.</span></span><br/>                                                                                        |
| [<span data-ttu-id="c7850-127">**GetTask**</span><span class="sxs-lookup"><span data-stu-id="c7850-127">**GetTask**</span></span>](taskfolder-gettask.md)                               | <span data-ttu-id="c7850-128">Ottiene un'attività in una posizione specificata in una cartella.</span><span class="sxs-lookup"><span data-stu-id="c7850-128">Gets a task at a specified location in a folder.</span></span><br/>                                                                                    |
| [<span data-ttu-id="c7850-129">**GetTasks**</span><span class="sxs-lookup"><span data-stu-id="c7850-129">**GetTasks**</span></span>](taskfolder-gettasks.md)                             | <span data-ttu-id="c7850-130">Ottiene tutte le attività nella cartella.</span><span class="sxs-lookup"><span data-stu-id="c7850-130">Gets all the tasks in the folder.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="c7850-131">**L'RegisterTask**</span><span class="sxs-lookup"><span data-stu-id="c7850-131">**RegisterTask**</span></span>](taskfolder-registertask.md)                     | <span data-ttu-id="c7850-132">Registra (Crea) una nuova attività nella cartella usando XML per definire l'attività.</span><span class="sxs-lookup"><span data-stu-id="c7850-132">Registers (creates) a new task in the folder using XML to define the task.</span></span><br/>                                                          |
| [<span data-ttu-id="c7850-133">**RegisterTaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="c7850-133">**RegisterTaskDefinition**</span></span>](taskfolder-registertaskdefinition.md) | <span data-ttu-id="c7850-134">Registra (Crea) un'attività in una posizione specificata usando l'interfaccia [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) per definire un'attività.</span><span class="sxs-lookup"><span data-stu-id="c7850-134">Registers (creates) a task in a specified location using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define a task.</span></span><br/> |
| [<span data-ttu-id="c7850-135">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c7850-135">**SetSecurityDescriptor**</span></span>](taskfolder-setsecuritydescriptor.md)   | <span data-ttu-id="c7850-136">Imposta il descrittore di sicurezza per la cartella.</span><span class="sxs-lookup"><span data-stu-id="c7850-136">Sets the security descriptor for the folder.</span></span><br/>                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="c7850-137">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c7850-137">Properties</span></span>

<span data-ttu-id="c7850-138">L'oggetto **TaskFolder** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c7850-138">The **TaskFolder** object has these properties.</span></span>



| <span data-ttu-id="c7850-139">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c7850-139">Property</span></span>                                   | <span data-ttu-id="c7850-140">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="c7850-140">Access type</span></span>          | <span data-ttu-id="c7850-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7850-141">Description</span></span>                                                                        |
|:-------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="c7850-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c7850-142">**Name**</span></span>](taskfolder-name.md)<br/> | <span data-ttu-id="c7850-143">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="c7850-143">Read-only</span></span><br/> | <span data-ttu-id="c7850-144">Ottiene il nome utilizzato per identificare la cartella che contiene un'attività.</span><span class="sxs-lookup"><span data-stu-id="c7850-144">Gets the name that is used to identify the folder that contains a task.</span></span><br/> |
| [<span data-ttu-id="c7850-145">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="c7850-145">**Path**</span></span>](taskfolder-path.md)<br/> | <span data-ttu-id="c7850-146">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="c7850-146">Read-only</span></span><br/> | <span data-ttu-id="c7850-147">Ottiene il percorso in cui è archiviata la cartella.</span><span class="sxs-lookup"><span data-stu-id="c7850-147">Gets the path to where the folder is stored.</span></span><br/>                            |



 

## <a name="examples"></a><span data-ttu-id="c7850-148">Esempio</span><span class="sxs-lookup"><span data-stu-id="c7850-148">Examples</span></span>

<span data-ttu-id="c7850-149">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md), [esempio di trigger di evento (scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [esempio di trigger giornaliero (scripting)](daily-trigger-example--scripting-.md), esempio di trigger di [registrazione (script)](registration-trigger-example--scripting-.md), esempio di [trigger settimanale (scripting)](weekly-trigger-example--scripting-.md), [esempio di trigger LOGON (scripting](logon-trigger-example--scripting-.md)), [esempio di trigger di avvio (](boot-trigger-example--scripting-.md)scripting) o [visualizzazione di nomi e Stati delle attività (script)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="c7850-149">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md), or [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7850-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7850-150">Requirements</span></span>



| <span data-ttu-id="c7850-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7850-151">Requirement</span></span> | <span data-ttu-id="c7850-152">Valore</span><span class="sxs-lookup"><span data-stu-id="c7850-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7850-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7850-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c7850-154">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7850-154">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c7850-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7850-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c7850-156">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c7850-156">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c7850-157">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c7850-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="c7850-158"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c7850-158"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c7850-159">DLL</span><span class="sxs-lookup"><span data-stu-id="c7850-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7850-160"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7850-160"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7850-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7850-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7850-162">Oggetti Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c7850-162">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="c7850-163">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c7850-163">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





