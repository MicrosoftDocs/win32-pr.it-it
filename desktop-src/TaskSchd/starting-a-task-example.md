---
title: Avvio di un esempio di attività
description: Per avviare un'attività, chiamare il metodo Run dell'interfaccia ITask. Run è un metodo asincrono che tenta di eseguire l'attività e viene restituito non appena l'attività è stata avviata. Per la riuscita di questo metodo, è necessario che il servizio Utilità di pianificazione sia in esecuzione.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325d8d990367a810351ec4eea8b03b7dc0240cd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300201"
---
# <a name="starting-a-task-example"></a><span data-ttu-id="7ea41-105">Avvio di un esempio di attività</span><span class="sxs-lookup"><span data-stu-id="7ea41-105">Starting a Task Example</span></span>

<span data-ttu-id="7ea41-106">Per avviare un'attività, chiamare il metodo [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) dell'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="7ea41-106">To start a task, call the [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) method of the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="7ea41-107">**Run** è un metodo asincrono che tenta di eseguire l'attività e viene restituito non appena l'attività è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="7ea41-107">**Run** is an asynchronous method that attempts to execute the task and returns as soon as the task has started.</span></span> <span data-ttu-id="7ea41-108">Per la riuscita di questo metodo, è necessario che il servizio Utilità di pianificazione sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7ea41-108">The Task Scheduler service must be running for this method to succeed.</span></span>

<span data-ttu-id="7ea41-109">Nella procedura riportata di seguito viene descritto come avviare un'attività.</span><span class="sxs-lookup"><span data-stu-id="7ea41-109">The following procedure describes how to start a task.</span></span>

<span data-ttu-id="7ea41-110">**Per avviare un'attività**</span><span class="sxs-lookup"><span data-stu-id="7ea41-110">**To start a task**</span></span>

1.  <span data-ttu-id="7ea41-111">Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7ea41-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="7ea41-112">In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7ea41-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="7ea41-113">Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività.</span><span class="sxs-lookup"><span data-stu-id="7ea41-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="7ea41-114">Si noti che questo esempio Mostra come ottenere l'attività di test.</span><span class="sxs-lookup"><span data-stu-id="7ea41-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="7ea41-115">Chiamare [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) per avviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="7ea41-115">Call [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) to start the task.</span></span> <span data-ttu-id="7ea41-116">Si noti che questo metodo viene ereditato dall'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="7ea41-116">Note that this method is inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>
4.  <span data-ttu-id="7ea41-117">Continuare l'elaborazione in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="7ea41-117">Continue processing as needed.</span></span>
5.  <span data-ttu-id="7ea41-118">Chiamare **ITask:: Release** per liberare risorse e [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) per annullare l'inizializzazione di com.</span><span class="sxs-lookup"><span data-stu-id="7ea41-118">Call **ITask::Release** to free resources and [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) to uninitialize COM.</span></span> <span data-ttu-id="7ea41-119">In questo esempio viene chiamata la [**versione**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per liberare il puntatore all'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="7ea41-119">This example calls [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to free the pointer to the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="7ea41-120">Si noti che la **versione** è un metodo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da **ITask**.</span><span class="sxs-lookup"><span data-stu-id="7ea41-120">(Note that **Release** is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by **ITask**.)</span></span>



| <span data-ttu-id="7ea41-121">Per un esempio di codice di</span><span class="sxs-lookup"><span data-stu-id="7ea41-121">For a code example of</span></span>    | <span data-ttu-id="7ea41-122">Vedere</span><span class="sxs-lookup"><span data-stu-id="7ea41-122">See</span></span>                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="7ea41-123">Esecuzione di un'attività esistente</span><span class="sxs-lookup"><span data-stu-id="7ea41-123">Running an existing task</span></span> | [<span data-ttu-id="7ea41-124">Esempio di codice C/C++: avvio di un'attività</span><span class="sxs-lookup"><span data-stu-id="7ea41-124">C/C++ Code Example: Starting a Task</span></span>](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a><span data-ttu-id="7ea41-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ea41-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ea41-126">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="7ea41-126">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 