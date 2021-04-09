---
title: Oggetto RegisteredTask
description: Oggetto di scripting che fornisce i metodi utilizzati per eseguire immediatamente l'attività, ottenere tutte le istanze in esecuzione dell'attività, ottenere o impostare le credenziali utilizzate per registrare l'attività e le proprietà che descrivono l'attività.
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- Utilità di pianificazione oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- RegisteredTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ce300375e5122a7b63266c0cd21cdddf34606b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740471"
---
# <a name="registeredtask-object"></a><span data-ttu-id="9e183-105">Oggetto RegisteredTask</span><span class="sxs-lookup"><span data-stu-id="9e183-105">RegisteredTask object</span></span>

<span data-ttu-id="9e183-106">Oggetto di scripting che fornisce i metodi utilizzati per eseguire immediatamente l'attività, ottenere tutte le istanze in esecuzione dell'attività, ottenere o impostare le credenziali utilizzate per registrare l'attività e le proprietà che descrivono l'attività.</span><span class="sxs-lookup"><span data-stu-id="9e183-106">Scripting object that provides the methods that are used to run the task immediately, get any running instances of the task, get or set the credentials that are used to register the task, and the properties that describe the task.</span></span>

## <a name="members"></a><span data-ttu-id="9e183-107">Membri</span><span class="sxs-lookup"><span data-stu-id="9e183-107">Members</span></span>

<span data-ttu-id="9e183-108">L'oggetto **RegisteredTask** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9e183-108">The **RegisteredTask** object has these types of members:</span></span>

-   [<span data-ttu-id="9e183-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="9e183-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="9e183-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e183-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9e183-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="9e183-111">Methods</span></span>

<span data-ttu-id="9e183-112">L'oggetto **RegisteredTask** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9e183-112">The **RegisteredTask** object has these methods.</span></span>



| <span data-ttu-id="9e183-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="9e183-113">Method</span></span>                                                                | <span data-ttu-id="9e183-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e183-114">Description</span></span>                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e183-115">**GetInstances**</span><span class="sxs-lookup"><span data-stu-id="9e183-115">**GetInstances**</span></span>](registeredtask-getinstances.md)                   | <span data-ttu-id="9e183-116">Restituisce tutte le istanze dell'attività registrata attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9e183-116">Returns all instances of the registered task that are currently running.</span></span><br/>             |
| [<span data-ttu-id="9e183-117">**Getruntimes**</span><span class="sxs-lookup"><span data-stu-id="9e183-117">**GetRunTimes**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | <span data-ttu-id="9e183-118">Ottiene le ore pianificate per l'esecuzione dell'attività registrata durante un periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="9e183-118">Gets the times that the registered task is scheduled to run during a specified time.</span></span><br/> |
| [<span data-ttu-id="9e183-119">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="9e183-119">**GetSecurityDescriptor**</span></span>](registeredtask-getsecuritydescriptor.md) | <span data-ttu-id="9e183-120">Ottiene il descrittore di sicurezza utilizzato come credenziali per l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="9e183-120">Gets the security descriptor that is used as credentials for the registered task.</span></span><br/>    |
| [<span data-ttu-id="9e183-121">**Correre**</span><span class="sxs-lookup"><span data-stu-id="9e183-121">**Run**</span></span>](registeredtask-run.md)                                     | <span data-ttu-id="9e183-122">Esegue immediatamente l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="9e183-122">Runs the registered task immediately.</span></span><br/>                                                |
| [<span data-ttu-id="9e183-123">**RunEx**</span><span class="sxs-lookup"><span data-stu-id="9e183-123">**RunEx**</span></span>](registeredtask-runex.md)                                 | <span data-ttu-id="9e183-124">Esegue immediatamente l'attività registrata utilizzando i flag specificati e un identificatore di sessione.</span><span class="sxs-lookup"><span data-stu-id="9e183-124">Runs the registered task immediately using specified flags and a session identifier.</span></span><br/> |
| [<span data-ttu-id="9e183-125">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="9e183-125">**SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md) | <span data-ttu-id="9e183-126">Imposta il descrittore di sicurezza utilizzato come credenziali per l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="9e183-126">Sets the security descriptor that is used as credentials for the registered task.</span></span><br/>    |
| [<span data-ttu-id="9e183-127">**Interrompere**</span><span class="sxs-lookup"><span data-stu-id="9e183-127">**Stop**</span></span>](registeredtask-stop.md)                                   | <span data-ttu-id="9e183-128">Arresta immediatamente l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="9e183-128">Stops the registered task immediately.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="9e183-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e183-129">Properties</span></span>

<span data-ttu-id="9e183-130">L'oggetto **RegisteredTask** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9e183-130">The **RegisteredTask** object has these properties.</span></span>



| <span data-ttu-id="9e183-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e183-131">Property</span></span>                                                                   | <span data-ttu-id="9e183-132">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="9e183-132">Access type</span></span>           | <span data-ttu-id="9e183-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e183-133">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e183-134">**Definizione**</span><span class="sxs-lookup"><span data-stu-id="9e183-134">**Definition**</span></span>](registeredtask-definition.md)<br/>                 | <span data-ttu-id="9e183-135">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e183-135">Read-only</span></span><br/>  | <span data-ttu-id="9e183-136">Ottiene la definizione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="9e183-136">Gets the definition of the task.</span></span><br/>                                               |
| [<span data-ttu-id="9e183-137">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="9e183-137">**Enabled**</span></span>](registeredtask-enabled.md)<br/>                       | <span data-ttu-id="9e183-138">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="9e183-138">Read/write</span></span><br/> | <span data-ttu-id="9e183-139">Ottiene o imposta un valore booleano che indica se l'attività registrata è abilitata.</span><span class="sxs-lookup"><span data-stu-id="9e183-139">Gets or set a Boolean value that indicates if the registered task is enabled.</span></span><br/>  |
| [<span data-ttu-id="9e183-140">**LastRunTime**</span><span class="sxs-lookup"><span data-stu-id="9e183-140">**LastRunTime**</span></span>](registeredtask-lastruntime.md)<br/>               | <span data-ttu-id="9e183-141">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e183-141">Read-only</span></span><br/>  | <span data-ttu-id="9e183-142">Ottiene l'ora dell'ultima esecuzione dell'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="9e183-142">Gets the time the registered task was last run.</span></span><br/>                                |
| [<span data-ttu-id="9e183-143">**LastTaskResult**</span><span class="sxs-lookup"><span data-stu-id="9e183-143">**LastTaskResult**</span></span>](registeredtask-lasttaskresult.md)<br/>         | <span data-ttu-id="9e183-144">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e183-144">Read-only</span></span><br/>  | <span data-ttu-id="9e183-145">Ottiene i risultati restituiti l'ultima volta in cui è stata eseguita l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="9e183-145">Gets the results that were returned the last time the registered task was run.</span></span><br/> |
| [<span data-ttu-id="9e183-146">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9e183-146">**Name**</span></span>](registeredtask-name.md)<br/>                             | <span data-ttu-id="9e183-147">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e183-147">Read-only</span></span><br/>  | <span data-ttu-id="9e183-148">Ottiene il nome dell'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="9e183-148">Gets the name of the registered task.</span></span><br/>                                          |
| [<span data-ttu-id="9e183-149">**NextRunTime**</span><span class="sxs-lookup"><span data-stu-id="9e183-149">**NextRunTime**</span></span>](registeredtask-nextruntime.md)<br/>               | <span data-ttu-id="9e183-150">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e183-150">Read-only</span></span><br/>  | <span data-ttu-id="9e183-151">Ottiene l'ora in cui è pianificata l'esecuzione successiva dell'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="9e183-151">Gets the time when the registered task is next scheduled to run.</span></span><br/>               |
| [<span data-ttu-id="9e183-152">**NumberOfMissedRuns**</span><span class="sxs-lookup"><span data-stu-id="9e183-152">**NumberOfMissedRuns**</span></span>](registeredtask-numberofmissedruns.md)<br/> | <span data-ttu-id="9e183-153">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e183-153">Read-only</span></span><br/>  | <span data-ttu-id="9e183-154">Ottiene il numero di volte in cui l'attività registrata ha perso un'esecuzione pianificata.</span><span class="sxs-lookup"><span data-stu-id="9e183-154">Gets the number of times the registered task has missed a scheduled run.</span></span><br/>       |
| [<span data-ttu-id="9e183-155">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="9e183-155">**Path**</span></span>](registeredtask-path.md)<br/>                             | <span data-ttu-id="9e183-156">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e183-156">Read-only</span></span><br/>  | <span data-ttu-id="9e183-157">Ottiene il percorso in cui è archiviata l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="9e183-157">Gets the path to where the registered task is stored.</span></span><br/>                          |
| [<span data-ttu-id="9e183-158">**State**</span><span class="sxs-lookup"><span data-stu-id="9e183-158">**State**</span></span>](registeredtask-state.md)<br/>                           | <span data-ttu-id="9e183-159">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e183-159">Read-only</span></span><br/>  | <span data-ttu-id="9e183-160">Ottiene lo stato operativo dell'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="9e183-160">Gets the operational state of the registered task.</span></span><br/>                             |
| [<span data-ttu-id="9e183-161">**XML**</span><span class="sxs-lookup"><span data-stu-id="9e183-161">**XML**</span></span>](registeredtask-xml.md)<br/>                               | <span data-ttu-id="9e183-162">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e183-162">Read-only</span></span><br/>  | <span data-ttu-id="9e183-163">Ottiene le informazioni di registrazione in formato XML per l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="9e183-163">Gets the XML-formatted registration information for the registered task.</span></span><br/>       |



 

## <a name="examples"></a><span data-ttu-id="9e183-164">Esempio</span><span class="sxs-lookup"><span data-stu-id="9e183-164">Examples</span></span>

<span data-ttu-id="9e183-165">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere l' [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md) e la [visualizzazione di nomi e Stati delle attività (scripting)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="9e183-165">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) and [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e183-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e183-166">Requirements</span></span>



| <span data-ttu-id="9e183-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e183-167">Requirement</span></span> | <span data-ttu-id="9e183-168">Valore</span><span class="sxs-lookup"><span data-stu-id="9e183-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e183-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e183-169">Minimum supported client</span></span><br/> | <span data-ttu-id="9e183-170">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e183-170">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9e183-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e183-171">Minimum supported server</span></span><br/> | <span data-ttu-id="9e183-172">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9e183-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9e183-173">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9e183-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="9e183-174"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9e183-174"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9e183-175">DLL</span><span class="sxs-lookup"><span data-stu-id="9e183-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e183-176"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e183-176"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





