---
title: Oggetto RunningTask
description: Oggetto di scripting che fornisce i metodi per ottenere informazioni da e controllare un'attività in esecuzione.
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- Utilità di pianificazione oggetto RunningTask
- Oggetto RunningTask Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- RunningTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261be07f71d0d35f5d3140de1b39574b635a531e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518208"
---
# <a name="runningtask-object"></a><span data-ttu-id="12e9d-105">Oggetto RunningTask</span><span class="sxs-lookup"><span data-stu-id="12e9d-105">RunningTask object</span></span>

<span data-ttu-id="12e9d-106">Oggetto di scripting che fornisce i metodi per ottenere informazioni da e controllare un'attività in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="12e9d-106">Scripting object that provides the methods to get information from and control a running task.</span></span>

## <a name="members"></a><span data-ttu-id="12e9d-107">Membri</span><span class="sxs-lookup"><span data-stu-id="12e9d-107">Members</span></span>

<span data-ttu-id="12e9d-108">L'oggetto **RunningTask** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="12e9d-108">The **RunningTask** object has these types of members:</span></span>

-   [<span data-ttu-id="12e9d-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="12e9d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="12e9d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12e9d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="12e9d-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="12e9d-111">Methods</span></span>

<span data-ttu-id="12e9d-112">L'oggetto **RunningTask** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="12e9d-112">The **RunningTask** object has these methods.</span></span>



| <span data-ttu-id="12e9d-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="12e9d-113">Method</span></span>                                 | <span data-ttu-id="12e9d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12e9d-114">Description</span></span>                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="12e9d-115">**Aggiorna**</span><span class="sxs-lookup"><span data-stu-id="12e9d-115">**Refresh**</span></span>](runningtask-refresh.md) | <span data-ttu-id="12e9d-116">Aggiorna tutte le variabili di istanza locale dell'attività.</span><span class="sxs-lookup"><span data-stu-id="12e9d-116">Refreshes all of the local instance variables of the task.</span></span><br/> |
| [<span data-ttu-id="12e9d-117">**Interrompere**</span><span class="sxs-lookup"><span data-stu-id="12e9d-117">**Stop**</span></span>](runningtask-stop.md)       | <span data-ttu-id="12e9d-118">Arresta questa istanza dell'attività.</span><span class="sxs-lookup"><span data-stu-id="12e9d-118">Stops this instance of the task.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="12e9d-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12e9d-119">Properties</span></span>

<span data-ttu-id="12e9d-120">L'oggetto **RunningTask** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="12e9d-120">The **RunningTask** object has these properties.</span></span>



| <span data-ttu-id="12e9d-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12e9d-121">Property</span></span>                                                      | <span data-ttu-id="12e9d-122">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="12e9d-122">Access type</span></span>          | <span data-ttu-id="12e9d-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12e9d-123">Description</span></span>                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="12e9d-124">**CurrentAction**</span><span class="sxs-lookup"><span data-stu-id="12e9d-124">**CurrentAction**</span></span>](runningtask-currentaction.md)<br/> | <span data-ttu-id="12e9d-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="12e9d-125">Read-only</span></span><br/> | <span data-ttu-id="12e9d-126">Ottiene il nome dell'azione corrente eseguita dall'attività in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="12e9d-126">Gets the name of the current action that the running task is performing.</span></span><br/> |
| [<span data-ttu-id="12e9d-127">**EnginePID**</span><span class="sxs-lookup"><span data-stu-id="12e9d-127">**EnginePID**</span></span>](runningtask-enginepid.md)<br/>         | <span data-ttu-id="12e9d-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="12e9d-128">Read-only</span></span><br/> | <span data-ttu-id="12e9d-129">Ottiene l'ID di processo per il motore (processo) che esegue l'attività.</span><span class="sxs-lookup"><span data-stu-id="12e9d-129">Gets the process ID for the engine (process) which is running the task.</span></span><br/>  |
| [<span data-ttu-id="12e9d-130">**: InstanceGuid**</span><span class="sxs-lookup"><span data-stu-id="12e9d-130">**InstanceGuid**</span></span>](runningtask-instanceguid.md)<br/>   | <span data-ttu-id="12e9d-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="12e9d-131">Read-only</span></span><br/> | <span data-ttu-id="12e9d-132">Ottiene l'identificatore GUID per questa istanza dell'attività.</span><span class="sxs-lookup"><span data-stu-id="12e9d-132">Gets the GUID identifier for this instance of the task.</span></span><br/>                  |
| [<span data-ttu-id="12e9d-133">**Nome**</span><span class="sxs-lookup"><span data-stu-id="12e9d-133">**Name**</span></span>](runningtask-name.md)<br/>                   | <span data-ttu-id="12e9d-134">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="12e9d-134">Read-only</span></span><br/> | <span data-ttu-id="12e9d-135">Ottiene il nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="12e9d-135">Gets the name of the task.</span></span><br/>                                               |
| [<span data-ttu-id="12e9d-136">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="12e9d-136">**Path**</span></span>](runningtask-path.md)<br/>                   | <span data-ttu-id="12e9d-137">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="12e9d-137">Read-only</span></span><br/> | <span data-ttu-id="12e9d-138">Ottiene il percorso in cui è archiviata l'attività.</span><span class="sxs-lookup"><span data-stu-id="12e9d-138">Gets the path to where the task is stored.</span></span><br/>                               |
| [<span data-ttu-id="12e9d-139">**State**</span><span class="sxs-lookup"><span data-stu-id="12e9d-139">**State**</span></span>](runningtask-state.md)<br/>                 | <span data-ttu-id="12e9d-140">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="12e9d-140">Read-only</span></span><br/> | <span data-ttu-id="12e9d-141">Ottiene lo stato dell'attività in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="12e9d-141">Gets the state of the running task.</span></span> <br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="12e9d-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12e9d-142">Requirements</span></span>



| <span data-ttu-id="12e9d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="12e9d-143">Requirement</span></span> | <span data-ttu-id="12e9d-144">Valore</span><span class="sxs-lookup"><span data-stu-id="12e9d-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12e9d-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12e9d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="12e9d-146">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12e9d-146">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="12e9d-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12e9d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="12e9d-148">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="12e9d-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="12e9d-149">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="12e9d-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="12e9d-150"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="12e9d-150"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="12e9d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="12e9d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12e9d-152"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12e9d-152"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12e9d-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12e9d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e9d-154">Oggetti Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="12e9d-154">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="12e9d-155">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="12e9d-155">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="12e9d-156">**RunningTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="12e9d-156">**RunningTaskCollection**</span></span>](runningtaskcollection.md)
</dt> <dt>

[<span data-ttu-id="12e9d-157">**RegisteredTask. Run**</span><span class="sxs-lookup"><span data-stu-id="12e9d-157">**RegisteredTask.Run**</span></span>](registeredtask-run.md)
</dt> <dt>

[<span data-ttu-id="12e9d-158">**RegisteredTask.RunEx**</span><span class="sxs-lookup"><span data-stu-id="12e9d-158">**RegisteredTask.RunEx**</span></span>](registeredtask-runex.md)
</dt> </dl>

 

 





