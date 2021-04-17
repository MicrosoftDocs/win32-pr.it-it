---
title: Oggetto TaskService
description: Per gli script, fornisce l'accesso al servizio Utilità di pianificazione per la gestione delle attività registrate.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- Utilità di pianificazione oggetto TaskService
- Oggetto TaskService Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- TaskService
- HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 762cd2445c3c6b720bba0f01ae48b787abc1fb38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478371"
---
# <a name="taskservice-object"></a><span data-ttu-id="9e8ce-105">Oggetto TaskService</span><span class="sxs-lookup"><span data-stu-id="9e8ce-105">TaskService object</span></span>

<span data-ttu-id="9e8ce-106">Per gli script, fornisce l'accesso al servizio Utilità di pianificazione per la gestione delle attività registrate.</span><span class="sxs-lookup"><span data-stu-id="9e8ce-106">For scripting, provides access to the Task Scheduler service for managing registered tasks.</span></span>

<span data-ttu-id="9e8ce-107">Prima di chiamare uno degli altri metodi **TaskService** , è necessario chiamare il metodo [**TaskService. Connect**](taskservice-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="9e8ce-107">The [**TaskService.Connect**](taskservice-connect.md) method should be called before calling any of the other **TaskService** methods.</span></span>

## <a name="members"></a><span data-ttu-id="9e8ce-108">Membri</span><span class="sxs-lookup"><span data-stu-id="9e8ce-108">Members</span></span>

<span data-ttu-id="9e8ce-109">L'oggetto **TaskService** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9e8ce-109">The **TaskService** object has these types of members:</span></span>

-   [<span data-ttu-id="9e8ce-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="9e8ce-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9e8ce-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e8ce-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9e8ce-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="9e8ce-112">Methods</span></span>

<span data-ttu-id="9e8ce-113">L'oggetto **TaskService** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9e8ce-113">The **TaskService** object has these methods.</span></span>



| <span data-ttu-id="9e8ce-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="9e8ce-114">Method</span></span>                                                 | <span data-ttu-id="9e8ce-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e8ce-115">Description</span></span>                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e8ce-116">**Connettersi**</span><span class="sxs-lookup"><span data-stu-id="9e8ce-116">**Connect**</span></span>](taskservice-connect.md)                 | <span data-ttu-id="9e8ce-117">Si connette a un computer remoto e associa tutte le chiamate successive a questa interfaccia con una sessione remota.</span><span class="sxs-lookup"><span data-stu-id="9e8ce-117">Connects to a remote machine and associates all subsequent calls on this interface with a remote session.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="9e8ce-118">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="9e8ce-118">**GetFolder**</span></span>](taskservice-getfolder.md)             | <span data-ttu-id="9e8ce-119">Ottiene il percorso di una cartella di attività registrate.</span><span class="sxs-lookup"><span data-stu-id="9e8ce-119">Gets the path to a folder of registered tasks.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="9e8ce-120">**GetRunningTasks**</span><span class="sxs-lookup"><span data-stu-id="9e8ce-120">**GetRunningTasks**</span></span>](taskservice-getrunningtasks.md) | <span data-ttu-id="9e8ce-121">Ottiene una raccolta di attività in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9e8ce-121">Gets a collection of running tasks.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="9e8ce-122">**NewTask**</span><span class="sxs-lookup"><span data-stu-id="9e8ce-122">**NewTask**</span></span>](taskservice-newtask.md)                 | <span data-ttu-id="9e8ce-123">Restituisce un oggetto definizione di attività vuoto da compilare con le impostazioni e le proprietà e quindi registrato utilizzando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="9e8ce-123">Returns an empty task definition object to be filled in with settings and properties and then registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9e8ce-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e8ce-124">Properties</span></span>

<span data-ttu-id="9e8ce-125">L'oggetto **TaskService** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9e8ce-125">The **TaskService** object has these properties.</span></span>



| <span data-ttu-id="9e8ce-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e8ce-126">Property</span></span>                                                          | <span data-ttu-id="9e8ce-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e8ce-127">Description</span></span>                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e8ce-128">**Connesso**</span><span class="sxs-lookup"><span data-stu-id="9e8ce-128">**Connected**</span></span>](taskservice-connected.md)<br/>             | <span data-ttu-id="9e8ce-129">Ottiene un valore booleano che indica se si è connessi al servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="9e8ce-129">Gets a Boolean value that indicates if you are connected to the Task Scheduler service.</span></span><br/>                          |
| [<span data-ttu-id="9e8ce-130">**ConnectedDomain**</span><span class="sxs-lookup"><span data-stu-id="9e8ce-130">**ConnectedDomain**</span></span>](taskservice-connecteddomain.md)<br/> | <span data-ttu-id="9e8ce-131">Ottiene il nome del dominio a cui è connesso il computer [**TargetServer**](taskservice-targetserver.md) .</span><span class="sxs-lookup"><span data-stu-id="9e8ce-131">Gets the name of the domain to which the [**TargetServer**](taskservice-targetserver.md) computer is connected.</span></span><br/> |
| [<span data-ttu-id="9e8ce-132">**ConnectedUser**</span><span class="sxs-lookup"><span data-stu-id="9e8ce-132">**ConnectedUser**</span></span>](taskservice-connecteduser.md)<br/>     | <span data-ttu-id="9e8ce-133">Ottiene il nome dell'utente connesso al servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="9e8ce-133">Gets the name of the user that is connected to the Task Scheduler service.</span></span><br/>                                       |
| <span data-ttu-id="9e8ce-134">HighestVersion</span><span class="sxs-lookup"><span data-stu-id="9e8ce-134">HighestVersion</span></span><br/>                                         | <span data-ttu-id="9e8ce-135">Ottiene la versione più recente di Utilità di pianificazione supportata da un computer.</span><span class="sxs-lookup"><span data-stu-id="9e8ce-135">Gets the highest version of Task Scheduler that a computer supports.</span></span><br/>                                             |
| [<span data-ttu-id="9e8ce-136">**TargetServer**</span><span class="sxs-lookup"><span data-stu-id="9e8ce-136">**TargetServer**</span></span>](taskservice-targetserver.md)<br/>       | <span data-ttu-id="9e8ce-137">Ottiene il nome del computer in cui è in esecuzione il servizio Utilità di pianificazione a cui è connesso l'utente.</span><span class="sxs-lookup"><span data-stu-id="9e8ce-137">Gets the name of the computer that is running the Task Scheduler service that the user is connected to.</span></span><br/>          |



 

## <a name="examples"></a><span data-ttu-id="9e8ce-138">Esempio</span><span class="sxs-lookup"><span data-stu-id="9e8ce-138">Examples</span></span>

<span data-ttu-id="9e8ce-139">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md), [esempio di trigger di evento (scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [esempio di trigger giornaliero (scripting)](daily-trigger-example--scripting-.md), esempio di trigger di [registrazione (script)](registration-trigger-example--scripting-.md), esempio di [trigger settimanale (scripting)](weekly-trigger-example--scripting-.md), [esempio di trigger LOGON (scripting](logon-trigger-example--scripting-.md)), [esempio di trigger di avvio (](boot-trigger-example--scripting-.md)scripting) o [visualizzazione di nomi e Stati delle attività (script)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="9e8ce-139">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md), or [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e8ce-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e8ce-140">Requirements</span></span>



| <span data-ttu-id="9e8ce-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e8ce-141">Requirement</span></span> | <span data-ttu-id="9e8ce-142">Valore</span><span class="sxs-lookup"><span data-stu-id="9e8ce-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e8ce-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e8ce-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9e8ce-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e8ce-144">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9e8ce-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e8ce-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9e8ce-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9e8ce-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9e8ce-147">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9e8ce-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="9e8ce-148"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9e8ce-148"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9e8ce-149">DLL</span><span class="sxs-lookup"><span data-stu-id="9e8ce-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e8ce-150"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e8ce-150"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e8ce-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e8ce-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e8ce-152">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="9e8ce-152">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





