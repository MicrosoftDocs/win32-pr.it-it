---
title: Esempi di recupero di proprietà di attività
description: Per recuperare le proprietà di un'attività, chiamare ITaskScheduler Activate per recuperare l'interfaccia dell'oggetto attività, quindi chiamare il Metodo ITask appropriato per recuperare la proprietà dell'attività a cui si è interessati.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- recupero delle proprietà dell'attività Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2b42bc8044171834b6d99e97c41e3f5c7048ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338694"
---
# <a name="retrieving-task-property-examples"></a><span data-ttu-id="143e7-104">Esempi di recupero di proprietà di attività</span><span class="sxs-lookup"><span data-stu-id="143e7-104">Retrieving Task Property Examples</span></span>

<span data-ttu-id="143e7-105">Per recuperare le proprietà di un'attività, chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per recuperare l'interfaccia dell'oggetto attività, quindi chiamare il metodo [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriato per recuperare la proprietà dell'attività a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="143e7-105">To retrieve the properties of a task, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get retrieve the interface of the task object, then call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to retrieve the task property that you are interested in.</span></span> <span data-ttu-id="143e7-106">Gli esempi di codice elencati nella parte inferiore della pagina mostrano come recuperare le diverse proprietà dell'attività.</span><span class="sxs-lookup"><span data-stu-id="143e7-106">The code examples listed at the bottom of the page show how to retrieve the different task properties.</span></span>

<span data-ttu-id="143e7-107">Gli esempi di codice elencati nella parte inferiore della pagina mostrano come recuperare le proprietà univoche degli oggetti attività.</span><span class="sxs-lookup"><span data-stu-id="143e7-107">The code examples listed at the bottom of the page show how to retrieve the properties that are unique to task objects.</span></span> <span data-ttu-id="143e7-108">Per altre proprietà dell' [*elemento di lavoro*](w.md) che si applicano anche alle attività, vedere recupero degli esempi di [elementi di lavoro](retrieving-work-item-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="143e7-108">For other [*work item*](w.md) properties that also apply to tasks, see [Retrieving Work Item Examples](retrieving-work-item-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="143e7-109">Nell'esempio di codice seguente tutte le interfacce vengono rilasciate dopo che non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="143e7-109">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="143e7-110">Si noti che se si sta recuperando una proprietà di stringa, ad esempio il nome dell'applicazione, i parametri o la directory di lavoro, è necessario chiamare [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria allocata per la stringa restituita.</span><span class="sxs-lookup"><span data-stu-id="143e7-110">Note that if you are retrieving a string property (such as the application name, parameters, or working directory), you must call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>

<span data-ttu-id="143e7-111">Nella procedura riportata di seguito viene descritto come recuperare una proprietà di attività.</span><span class="sxs-lookup"><span data-stu-id="143e7-111">The following procedure describes how to retrieve a task property.</span></span>

<span data-ttu-id="143e7-112">**Per recuperare una proprietà di attività**</span><span class="sxs-lookup"><span data-stu-id="143e7-112">**To retrieve a task property**</span></span>

1.  <span data-ttu-id="143e7-113">Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="143e7-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="143e7-114">In questi esempi si presuppone che il servizio Utilità di pianificazione sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="143e7-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="143e7-115">Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività.</span><span class="sxs-lookup"><span data-stu-id="143e7-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="143e7-116">Si noti che questo esempio Mostra come ottenere l'attività di test.</span><span class="sxs-lookup"><span data-stu-id="143e7-116">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="143e7-117">Chiamare il metodo [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriato per recuperare la proprietà a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="143e7-117">Call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to retrieve the property you are interested in.</span></span>
4.  <span data-ttu-id="143e7-118">Elaborare la proprietà in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="143e7-118">Process the property as needed.</span></span> <span data-ttu-id="143e7-119">In questi esempi la proprietà viene stampata sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="143e7-119">(These examples print the property to the screen.)</span></span>
5.  <span data-ttu-id="143e7-120">Se la proprietà restituita è una stringa, chiamare [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria allocata per la stringa restituita.</span><span class="sxs-lookup"><span data-stu-id="143e7-120">If the returned property is a string, call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>



| <span data-ttu-id="143e7-121">Per un esempio di codice di</span><span class="sxs-lookup"><span data-stu-id="143e7-121">For a code example of</span></span>                                                                                                                           | <span data-ttu-id="143e7-122">Vedere</span><span class="sxs-lookup"><span data-stu-id="143e7-122">See</span></span>                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="143e7-123">Recupero del nome dell'applicazione associata a una determinata attività</span><span class="sxs-lookup"><span data-stu-id="143e7-123">Retrieving the name of the application associated with a given task</span></span>                                                                             | [<span data-ttu-id="143e7-124">Esempio di codice C/C++: recupero del nome dell'applicazione dell'attività</span><span class="sxs-lookup"><span data-stu-id="143e7-124">C/C++ Code Example: Retrieving the Task Application Name</span></span>](c-c-code-example-retrieving-the-task-application-name.md)   |
| <span data-ttu-id="143e7-125">Recupero del tempo massimo di esecuzione dell'attività e visualizzazione di tale numero sullo schermo</span><span class="sxs-lookup"><span data-stu-id="143e7-125">Retrieving the maximum amount of time the task can run and displaying that number on the screen</span></span>                                                 | [<span data-ttu-id="143e7-126">Esempio di codice C/C++: recupero dell'attività MaxRunTime</span><span class="sxs-lookup"><span data-stu-id="143e7-126">C/C++ Code Example: Retrieving the Task MaxRunTime</span></span>](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| <span data-ttu-id="143e7-127">Recupero della stringa di parametro eseguita durante l'esecuzione dell'attività e visualizzazione della stringa sullo schermo</span><span class="sxs-lookup"><span data-stu-id="143e7-127">Retrieving the parameter string that is executed when the task is run and displaying that string on the screen</span></span>                                  | [<span data-ttu-id="143e7-128">Esempio di codice C/C++: recupero dei parametri delle attività</span><span class="sxs-lookup"><span data-stu-id="143e7-128">C/C++ Code Example: Retrieving Task Parameters</span></span>](c-c-code-example-retrieving-task-parameters.md)                       |
| <span data-ttu-id="143e7-129">Recupero del [*livello di priorità*](p.md) dell'attività</span><span class="sxs-lookup"><span data-stu-id="143e7-129">Retrieving the [*priority level*](p.md) of the task</span></span>                                                                    | [<span data-ttu-id="143e7-130">Esempio di codice C/C++: recupero della priorità dell'attività</span><span class="sxs-lookup"><span data-stu-id="143e7-130">C/C++ Code Example: Retrieving Task Priority</span></span>](c-c-code-example-retrieving-task-priority.md)                           |
| <span data-ttu-id="143e7-131">Recupero della [*directory di lavoro*](w.md) di un'attività e visualizzazione del percorso della directory di lavoro sullo schermo</span><span class="sxs-lookup"><span data-stu-id="143e7-131">Retrieving the [*working directory*](w.md) of a task and displaying the path to the working directory on the screen</span></span> | [<span data-ttu-id="143e7-132">Esempio di codice C/C++: recupero della directory di lavoro dell'attività</span><span class="sxs-lookup"><span data-stu-id="143e7-132">C/C++ Code Example: Retrieving the Task Working Directory</span></span>](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a><span data-ttu-id="143e7-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="143e7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="143e7-134">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="143e7-134">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 