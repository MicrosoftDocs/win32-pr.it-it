---
title: Chiusura di un esempio di attività
description: È possibile terminare un'attività mentre è in esecuzione chiamando IScheduledWorkItem terminate.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e632b00a9e957849a5735d31018e3444113190
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223971"
---
# <a name="terminating-a-task-example"></a><span data-ttu-id="df9fc-103">Chiusura di un esempio di attività</span><span class="sxs-lookup"><span data-stu-id="df9fc-103">Terminating a Task Example</span></span>

<span data-ttu-id="df9fc-104">È possibile terminare un'attività mentre è in esecuzione chiamando [**IScheduledWorkItem:: terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).</span><span class="sxs-lookup"><span data-stu-id="df9fc-104">You can terminate a task while it is running by calling [**IScheduledWorkItem::Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).</span></span>

<span data-ttu-id="df9fc-105">Nella procedura riportata di seguito viene descritto come terminare un'attività se è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="df9fc-105">The following procedure describes how to terminate a task if it is running.</span></span>

<span data-ttu-id="df9fc-106">**Per terminare un'attività se è in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="df9fc-106">**To terminate a task if it is running**</span></span>

1.  <span data-ttu-id="df9fc-107">Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="df9fc-107">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="df9fc-108">In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="df9fc-108">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="df9fc-109">Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività.</span><span class="sxs-lookup"><span data-stu-id="df9fc-109">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="df9fc-110">Si noti che questo esempio Mostra come ottenere l'attività di test.</span><span class="sxs-lookup"><span data-stu-id="df9fc-110">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="df9fc-111">Chiamare **ITask:: GetStatus** per verificare se l'attività è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="df9fc-111">Call **ITask::GetStatus** to find out if the task is running.</span></span> <span data-ttu-id="df9fc-112">(Si noti che [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) è un metodo [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ereditato da [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).</span><span class="sxs-lookup"><span data-stu-id="df9fc-112">(Note that [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
4.  <span data-ttu-id="df9fc-113">Verificare lo stato dell'attività e quindi chiamare **ITask:: terminate** se l'attività è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="df9fc-113">Check the status of the task and then call **ITask::Terminate** if the task is running.</span></span> <span data-ttu-id="df9fc-114">(Si noti che [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) è un metodo [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ereditato da [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).</span><span class="sxs-lookup"><span data-stu-id="df9fc-114">(Note that [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="df9fc-115">Per un esempio di codice di</span><span class="sxs-lookup"><span data-stu-id="df9fc-115">For a code example of</span></span>                | <span data-ttu-id="df9fc-116">Vedere</span><span class="sxs-lookup"><span data-stu-id="df9fc-116">See</span></span>                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="df9fc-117">Verifica dello stato di un'attività nota</span><span class="sxs-lookup"><span data-stu-id="df9fc-117">Verifying the status of a known task</span></span> | [<span data-ttu-id="df9fc-118">Esempio di codice C/C++: terminazione di un'attività</span><span class="sxs-lookup"><span data-stu-id="df9fc-118">C/C++ Code Example: Terminating a Task</span></span>](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a><span data-ttu-id="df9fc-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="df9fc-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df9fc-120">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="df9fc-120">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 