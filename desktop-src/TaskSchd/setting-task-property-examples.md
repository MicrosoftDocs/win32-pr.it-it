---
title: Esempi di impostazione delle proprietà delle attività
description: Per impostare le proprietà di un'attività, chiamare ITaskScheduler Activate per recuperare l'interfaccia dell'oggetto attività, quindi chiamare il Metodo ITask appropriato per impostare la proprietà dell'attività a cui si è interessati.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- impostazione delle proprietà dell'attività Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb05031961e38314cbc7cd12c20c1d863f54af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300144"
---
# <a name="setting-task-property-examples"></a><span data-ttu-id="6d256-104">Esempi di impostazione delle proprietà delle attività</span><span class="sxs-lookup"><span data-stu-id="6d256-104">Setting Task Property Examples</span></span>

<span data-ttu-id="6d256-105">Per impostare le proprietà di un'attività, chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per recuperare l'interfaccia dell'oggetto attività, quindi chiamare il metodo [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriato per impostare la proprietà dell'attività a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="6d256-105">To set the properties of a task, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the task object, then call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to set the task property you are interested in.</span></span>

<span data-ttu-id="6d256-106">Gli esempi di codice elencati nella parte inferiore della pagina illustrano come impostare le proprietà univoche per gli oggetti attività.</span><span class="sxs-lookup"><span data-stu-id="6d256-106">The code examples listed at the bottom of the page show how to set the properties that are unique to task objects.</span></span> <span data-ttu-id="6d256-107">Per altre proprietà dell' [*elemento di lavoro*](w.md) che si applicano anche alle attività, vedere Impostazione degli esempi di proprietà degli [elementi di lavoro](setting-work-item-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="6d256-107">For other [*work item*](w.md) properties that also apply to tasks, see [Setting Work Item Property Examples](setting-work-item-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="6d256-108">Nell'esempio di codice seguente tutte le interfacce vengono rilasciate dopo che non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="6d256-108">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="6d256-109">Negli esempi seguenti, l'oggetto attività modificato viene sempre salvato su disco mediante una chiamata a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="6d256-109">In the following examples, the modified task object is always saved to disk by a call to [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="6d256-110">(L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia com standard ereditata dall'oggetto attività).</span><span class="sxs-lookup"><span data-stu-id="6d256-110">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface inherited by the task object.)</span></span>

<span data-ttu-id="6d256-111">Nella procedura riportata di seguito viene descritto come impostare una proprietà dell'attività.</span><span class="sxs-lookup"><span data-stu-id="6d256-111">The following procedure describes how to set a task property.</span></span>

<span data-ttu-id="6d256-112">**Per impostare una proprietà dell'attività**</span><span class="sxs-lookup"><span data-stu-id="6d256-112">**To set a task property**</span></span>

1.  <span data-ttu-id="6d256-113">Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="6d256-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="6d256-114">In questi esempi si presuppone che il servizio Utilità di pianificazione sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6d256-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="6d256-115">Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività.</span><span class="sxs-lookup"><span data-stu-id="6d256-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="6d256-116">Si noti che questo esempio Mostra come ottenere l'attività di test.</span><span class="sxs-lookup"><span data-stu-id="6d256-116">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="6d256-117">Chiamare il metodo [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriato per impostare la proprietà a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="6d256-117">Call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to set the property you are interested in.</span></span>
4.  <span data-ttu-id="6d256-118">Chiamare [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) per archiviare l'oggetto attività modificato su disco.</span><span class="sxs-lookup"><span data-stu-id="6d256-118">Call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to store the modified task object to disk.</span></span>



| <span data-ttu-id="6d256-119">Per un esempio di codice di</span><span class="sxs-lookup"><span data-stu-id="6d256-119">For a code example of</span></span>                                                                                                                                | <span data-ttu-id="6d256-120">Vedere</span><span class="sxs-lookup"><span data-stu-id="6d256-120">See</span></span>                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d256-121">Impostazione del nome dell'applicazione associata a un'attività nota</span><span class="sxs-lookup"><span data-stu-id="6d256-121">Setting the name of the application associated with a known task</span></span>                                                                                     | [<span data-ttu-id="6d256-122">Esempio di codice C/C++: impostazione del nome dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="6d256-122">C/C++ Code Example: Setting Application Name</span></span>](c-c-code-example-setting-application-name.md)   |
| <span data-ttu-id="6d256-123">Impostazione del tempo di esecuzione massimo di un'attività nota</span><span class="sxs-lookup"><span data-stu-id="6d256-123">Setting the maximum run time of a known task</span></span>                                                                                                         | [<span data-ttu-id="6d256-124">Esempio di codice C/C++: impostazione di MaxRunTime</span><span class="sxs-lookup"><span data-stu-id="6d256-124">C/C++ Code Example: Setting MaxRunTime</span></span>](c-c-code-example-setting-maxruntime.md)               |
| <span data-ttu-id="6d256-125">Cancellazione di tutti i parametri della riga di comando associati a un'attività nota</span><span class="sxs-lookup"><span data-stu-id="6d256-125">Clearing all command-line parameters associated with a known task</span></span>                                                                                    | [<span data-ttu-id="6d256-126">Esempio di codice C/C++: impostazione dei parametri delle attività</span><span class="sxs-lookup"><span data-stu-id="6d256-126">C/C++ Code Example: Setting Task Parameters</span></span>](c-c-code-example-setting-task-parameters.md)     |
| <span data-ttu-id="6d256-127">In questo esempio viene impostata la priorità di un'attività di test e quindi viene salvata l'attività.</span><span class="sxs-lookup"><span data-stu-id="6d256-127">This example sets the priority of a test task and then saves the task.</span></span> <span data-ttu-id="6d256-128">In questo esempio si presuppone che l'attività di test esista già nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="6d256-128">This example assumes that the test task already exists on the local computer.</span></span> | [<span data-ttu-id="6d256-129">Esempio di codice C/C++: impostazione della priorità delle attività</span><span class="sxs-lookup"><span data-stu-id="6d256-129">C/C++ Code Example: Setting Task Priority</span></span>](c-c-code-example-setting-task-priority.md)         |
| <span data-ttu-id="6d256-130">Impostazione della [*directory di lavoro*](w.md) di un'attività nota</span><span class="sxs-lookup"><span data-stu-id="6d256-130">Setting the [*working directory*](w.md) of a known task</span></span>                                                                  | [<span data-ttu-id="6d256-131">Esempio di codice C/C++: impostazione della directory di lavoro</span><span class="sxs-lookup"><span data-stu-id="6d256-131">C/C++ Code Example: Setting Working Directory</span></span>](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a><span data-ttu-id="6d256-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d256-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d256-133">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="6d256-133">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 