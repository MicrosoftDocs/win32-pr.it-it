---
title: Creazione di un nuovo trigger
description: Per creare un trigger è necessario usare tre interfacce.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48ecb7b06e5bade6d5ad80e4c9a82794f6a17e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399387"
---
# <a name="creating-a-new-trigger"></a><span data-ttu-id="53a9d-103">Creazione di un nuovo trigger</span><span class="sxs-lookup"><span data-stu-id="53a9d-103">Creating a New Trigger</span></span>

<span data-ttu-id="53a9d-104">Per creare un trigger è necessario usare tre interfacce.</span><span class="sxs-lookup"><span data-stu-id="53a9d-104">To create a trigger you must use three interfaces.</span></span> <span data-ttu-id="53a9d-105">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornisce il metodo [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) per la creazione dell'oggetto trigger, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) fornisce il metodo [**ITaskTrigger:: setrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) per l'impostazione dei criteri per il trigger e l'interfaccia com [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) fornisce un metodo **Save** per salvare il nuovo trigger su disco.</span><span class="sxs-lookup"><span data-stu-id="53a9d-105">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) provides the [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) method for creating the trigger object, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) provides the [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) method for setting the criteria for the trigger, and the COM interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) provides a **Save** method for saving the new trigger to disk.</span></span>

<span data-ttu-id="53a9d-106">Nella procedura riportata di seguito viene descritto come creare un nuovo trigger.</span><span class="sxs-lookup"><span data-stu-id="53a9d-106">The following procedure describes how to create a new trigger.</span></span>

<span data-ttu-id="53a9d-107">**Per creare un nuovo trigger**</span><span class="sxs-lookup"><span data-stu-id="53a9d-107">**To create a new trigger**</span></span>

1.  <span data-ttu-id="53a9d-108">Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="53a9d-108">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="53a9d-109">In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="53a9d-109">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="53a9d-110">Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività.</span><span class="sxs-lookup"><span data-stu-id="53a9d-110">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="53a9d-111">Si noti che questo esempio Mostra come ottenere l'attività di test.</span><span class="sxs-lookup"><span data-stu-id="53a9d-111">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="53a9d-112">Chiamare [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) per creare un oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="53a9d-112">Call [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) to create a trigger object.</span></span> <span data-ttu-id="53a9d-113">(Si noti che [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) viene ereditato da [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)).</span><span class="sxs-lookup"><span data-stu-id="53a9d-113">(Note that [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
4.  <span data-ttu-id="53a9d-114">Definire una struttura di [**\_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="53a9d-114">Define a [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="53a9d-115">Si noti che i membri wBeginDay, wBeginMonth e wBeginYear **del \_ trigger di attività** devono essere impostati rispettivamente su un giorno, un mese e un anno validi.</span><span class="sxs-lookup"><span data-stu-id="53a9d-115">Note that wBeginDay, wBeginMonth, and wBeginYear members of **TASK\_TRIGGER** must be set to a valid day, month, and year respectively.</span></span>
5.  <span data-ttu-id="53a9d-116">Chiamare [**ITaskTrigger:: setrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) per impostare i criteri del trigger.</span><span class="sxs-lookup"><span data-stu-id="53a9d-116">Call [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) to set the trigger criteria.</span></span>
6.  <span data-ttu-id="53a9d-117">Salvare l'attività con il nuovo trigger su disco usando [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="53a9d-117">Save the task with the new trigger to disk using [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="53a9d-118">L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia com standard supportata dall'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="53a9d-118">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
7.  <span data-ttu-id="53a9d-119">Chiamare [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per rilasciare tutte le risorse.</span><span class="sxs-lookup"><span data-stu-id="53a9d-119">Call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release all resources.</span></span> <span data-ttu-id="53a9d-120">Si noti che la **versione** è un metodo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="53a9d-120">(Note that **Release** is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="53a9d-121">Per un esempio di codice di</span><span class="sxs-lookup"><span data-stu-id="53a9d-121">For a code example of</span></span>                       | <span data-ttu-id="53a9d-122">Vedere</span><span class="sxs-lookup"><span data-stu-id="53a9d-122">See</span></span>                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="53a9d-123">Creazione di un nuovo trigger per un'attività esistente</span><span class="sxs-lookup"><span data-stu-id="53a9d-123">Creating a new trigger for an existing task</span></span> | [<span data-ttu-id="53a9d-124">Esempio di codice C/C++: creazione di un trigger di attività</span><span class="sxs-lookup"><span data-stu-id="53a9d-124">C/C++ Code Example: Creating a Task Trigger</span></span>](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a><span data-ttu-id="53a9d-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53a9d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53a9d-126">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="53a9d-126">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 