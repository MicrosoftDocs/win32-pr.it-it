---
title: Esempio di creazione di un trigger inattivo
description: Per creare un trigger inattivo, è necessario specificare un trigger inattivo quando si crea il trigger ed è necessario impostare il tempo di inattività per l'attività. Per informazioni sulle condizioni di inattività, vedere condizioni di inattività.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a7f8333c79d05dfade609f028f93a816e61adf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338527"
---
# <a name="creating-an-idle-trigger-example"></a><span data-ttu-id="7c258-104">Esempio di creazione di un trigger inattivo</span><span class="sxs-lookup"><span data-stu-id="7c258-104">Creating an Idle Trigger Example</span></span>

<span data-ttu-id="7c258-105">Per creare un trigger inattivo, è necessario specificare un trigger inattivo quando si crea il trigger ed è necessario impostare il tempo di inattività per l'attività.</span><span class="sxs-lookup"><span data-stu-id="7c258-105">To create an idle trigger, you must specify an idle trigger when you create the trigger, and you must set the idle time for the task.</span></span> <span data-ttu-id="7c258-106">Per informazioni sulle condizioni di inattività, vedere [condizioni](task-idle-conditions.md)di inattività.</span><span class="sxs-lookup"><span data-stu-id="7c258-106">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

<span data-ttu-id="7c258-107">Dopo aver creato il trigger inattivo, chiamare [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) per salvare il nuovo trigger su disco.</span><span class="sxs-lookup"><span data-stu-id="7c258-107">After creating the idle trigger, call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to save the new trigger to disk.</span></span>

<span data-ttu-id="7c258-108">Nella procedura riportata di seguito viene descritto come creare un trigger inattivo per un'attività nota.</span><span class="sxs-lookup"><span data-stu-id="7c258-108">The following procedure describes how to create an idle trigger for a known task.</span></span>

<span data-ttu-id="7c258-109">**Per creare un trigger inattivo per un'attività nota**</span><span class="sxs-lookup"><span data-stu-id="7c258-109">**To create an idle trigger for a known task**</span></span>

1.  <span data-ttu-id="7c258-110">Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7c258-110">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="7c258-111">In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7c258-111">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="7c258-112">Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività.</span><span class="sxs-lookup"><span data-stu-id="7c258-112">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="7c258-113">Si noti che questo esempio Mostra come ottenere l'attività di test.</span><span class="sxs-lookup"><span data-stu-id="7c258-113">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="7c258-114">Chiamare [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) per impostare per quanto tempo il sistema deve rimanere inattivo prima che il trigger venga attivato.</span><span class="sxs-lookup"><span data-stu-id="7c258-114">Call [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) to set how long the system must remain idle before the trigger will fire.</span></span> <span data-ttu-id="7c258-115">(Si noti che **SetIdleWait** viene ereditato da [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)).</span><span class="sxs-lookup"><span data-stu-id="7c258-115">(Note that **SetIdleWait** is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
4.  <span data-ttu-id="7c258-116">Definire la struttura del [**\_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) e chiamare [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) per creare il trigger inattivo.</span><span class="sxs-lookup"><span data-stu-id="7c258-116">Define the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure and call [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) to create the idle trigger.</span></span> <span data-ttu-id="7c258-117">(Si noti che **CreateTrigger** viene ereditato da [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)).</span><span class="sxs-lookup"><span data-stu-id="7c258-117">(Note that **CreateTrigger** is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
5.  <span data-ttu-id="7c258-118">Salvare l'attività con il nuovo trigger di inattività su disco con [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="7c258-118">Save the task with the new idle trigger to disk using [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="7c258-119">L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia com standard supportata dall'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="7c258-119">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
6.  <span data-ttu-id="7c258-120">Chiamare **ITask:: Release** per rilasciare tutte le risorse.</span><span class="sxs-lookup"><span data-stu-id="7c258-120">Call **ITask::Release** to release all resources.</span></span> <span data-ttu-id="7c258-121">Si noti che la [**versione**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) è un metodo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="7c258-121">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="7c258-122">Per un esempio di codice di</span><span class="sxs-lookup"><span data-stu-id="7c258-122">For a code example of</span></span>                         | <span data-ttu-id="7c258-123">Vedere</span><span class="sxs-lookup"><span data-stu-id="7c258-123">See</span></span>                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c258-124">Creazione di un trigger inattivo per un'attività esistente</span><span class="sxs-lookup"><span data-stu-id="7c258-124">Creating an idle trigger for an existing task</span></span> | [<span data-ttu-id="7c258-125">Esempio di codice C/C++: creazione di un trigger inattivo</span><span class="sxs-lookup"><span data-stu-id="7c258-125">C/C++ Code Example: Creating an Idle Trigger</span></span>](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a><span data-ttu-id="7c258-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c258-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c258-127">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="7c258-127">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 