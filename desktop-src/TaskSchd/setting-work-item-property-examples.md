---
title: Impostazione degli esempi di proprietà degli elementi di lavoro
description: Per impostare le proprietà di un elemento di lavoro, chiamare ITaskScheduler Activate per recuperare l'interfaccia dell'oggetto elemento di lavoro, quindi chiamare il metodo appropriato per impostare la proprietà dell'attività a cui si è interessati. Attualmente, gli unici elementi di lavoro validi sono attività.
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- impostazione delle proprietà degli elementi di lavoro Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e026ea3d2b3f6677a3d229e9289ab9b201e02b94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963298"
---
# <a name="setting-work-item-property-examples"></a><span data-ttu-id="45115-105">Impostazione degli esempi di proprietà degli elementi di lavoro</span><span class="sxs-lookup"><span data-stu-id="45115-105">Setting Work Item Property Examples</span></span>

<span data-ttu-id="45115-106">Per impostare le proprietà di un elemento di lavoro, chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per recuperare l'interfaccia dell'oggetto elemento di lavoro, quindi chiamare il metodo appropriato per impostare la proprietà dell'attività a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="45115-106">To set the properties of a work item, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the work item object, then call the appropriate method to set the task property you are interested in.</span></span> <span data-ttu-id="45115-107">Attualmente, gli unici elementi di lavoro validi sono attività.</span><span class="sxs-lookup"><span data-stu-id="45115-107">Currently, the only valid work items are tasks.</span></span>

<span data-ttu-id="45115-108">Gli esempi di codice elencati nella parte inferiore della pagina illustrano come impostare le proprietà che si applicano a tutti gli elementi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="45115-108">The code examples listed at the bottom of the page show how to set the properties that apply to all work items.</span></span> <span data-ttu-id="45115-109">Per altre proprietà univoche per le attività, vedere [impostazione degli esempi di proprietà delle attività](setting-task-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="45115-109">For other properties that are unique to tasks, see [Setting Task Property Examples](setting-task-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="45115-110">Nell'esempio di codice seguente tutte le interfacce vengono rilasciate dopo che non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="45115-110">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="45115-111">Negli esempi seguenti, l'oggetto modificato viene sempre salvato su disco mediante una chiamata a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="45115-111">In the following examples, the modified object is always saved to disk by a call to [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="45115-112">(L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia com standard ereditata dall'oggetto attività).</span><span class="sxs-lookup"><span data-stu-id="45115-112">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface inherited by the task object.)</span></span>

<span data-ttu-id="45115-113">Nella procedura riportata di seguito viene descritto come impostare una proprietà dell'attività.</span><span class="sxs-lookup"><span data-stu-id="45115-113">The following procedure describes how to set a task property.</span></span>

<span data-ttu-id="45115-114">**Per impostare una proprietà dell'attività**</span><span class="sxs-lookup"><span data-stu-id="45115-114">**To set a task property**</span></span>

1.  <span data-ttu-id="45115-115">Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="45115-115">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="45115-116">In questi esempi si presuppone che il servizio Utilità di pianificazione sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="45115-116">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="45115-117">Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività.</span><span class="sxs-lookup"><span data-stu-id="45115-117">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="45115-118">Si noti che le attività sono attualmente l'unico tipo di elemento di lavoro valido.</span><span class="sxs-lookup"><span data-stu-id="45115-118">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="45115-119">Chiamare il metodo [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) appropriato per impostare la proprietà a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="45115-119">Call the appropriate [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method to set the property you are interested in.</span></span> <span data-ttu-id="45115-120">Si noti che i metodi **IScheduledWorkItem** vengono ereditati dall'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="45115-120">Note that **IScheduledWorkItem** methods are inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>
4.  <span data-ttu-id="45115-121">Chiamare [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) per archiviare l'oggetto attività modificato su disco.</span><span class="sxs-lookup"><span data-stu-id="45115-121">Call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to store the modified task object to disk.</span></span>



| <span data-ttu-id="45115-122">Per un esempio di codice di</span><span class="sxs-lookup"><span data-stu-id="45115-122">For a code example of</span></span>                            | <span data-ttu-id="45115-123">Vedere</span><span class="sxs-lookup"><span data-stu-id="45115-123">See</span></span>                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45115-124">Impostazione delle informazioni sull'account per un'attività nota</span><span class="sxs-lookup"><span data-stu-id="45115-124">Setting the account information for a known task</span></span> | [<span data-ttu-id="45115-125">Esempio di codice C/C++: impostazione delle informazioni sull'account attività</span><span class="sxs-lookup"><span data-stu-id="45115-125">C/C++ Code Example: Setting Task Account Information</span></span>](c-c-code-example-setting-task-account-information.md) |
| <span data-ttu-id="45115-126">Impostazione del commento di un'attività nota</span><span class="sxs-lookup"><span data-stu-id="45115-126">Setting the comment of a known task</span></span>              | [<span data-ttu-id="45115-127">Esempio di codice C/C++: impostazione del commento dell'attività</span><span class="sxs-lookup"><span data-stu-id="45115-127">C/C++ Code Example: Setting Task Comment</span></span>](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a><span data-ttu-id="45115-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="45115-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45115-129">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="45115-129">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 