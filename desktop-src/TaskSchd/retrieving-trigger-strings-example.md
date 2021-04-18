---
title: Esempio di recupero di stringhe di trigger
description: È possibile recuperare le stringhe di trigger di un trigger noto usando l'interfaccia IScheduledWorkItem o ITaskTrigger, a seconda del tipo di oggetto in uso.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- recupero delle stringhe del trigger Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44708fdbb4025f5d99409297dda65504a909aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300104"
---
# <a name="retrieving-trigger-strings-example"></a><span data-ttu-id="47d50-104">Esempio di recupero di stringhe di trigger</span><span class="sxs-lookup"><span data-stu-id="47d50-104">Retrieving Trigger Strings Example</span></span>

<span data-ttu-id="47d50-105">È possibile recuperare le stringhe di trigger di un trigger noto usando l'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) o [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) , a seconda del tipo di oggetto in uso.</span><span class="sxs-lookup"><span data-stu-id="47d50-105">You can retrieve the trigger strings of a known trigger using the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) or [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface, depending on the type of object you are working with.</span></span>

<span data-ttu-id="47d50-106">Quando si utilizza un [*oggetto attività*](t.md), utilizzare i metodi dell'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) per recuperare le stringhe di trigger di un elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="47d50-106">When working with a [*task object*](t.md), use the methods of the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface to retrieve the trigger strings of a work item.</span></span>

<span data-ttu-id="47d50-107">Quando si utilizza un [*oggetto trigger di attività*](t.md), utilizzare i metodi dell'interfaccia [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) per recuperare la stringa di trigger del trigger.</span><span class="sxs-lookup"><span data-stu-id="47d50-107">When you are working with a [*task trigger object*](t.md), use the methods of the [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface to retrieve the trigger string of the trigger.</span></span>

<span data-ttu-id="47d50-108">Nell'esempio seguente viene illustrato come utilizzare [**IScheduledWorkItem:: GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) per visualizzare le stringhe di tutti i trigger associati a un'attività nota.</span><span class="sxs-lookup"><span data-stu-id="47d50-108">The following example shows how to use [**IScheduledWorkItem::GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) to display the strings of all triggers associated with a known task.</span></span>

<span data-ttu-id="47d50-109">Nella procedura riportata di seguito viene descritto come recuperare le stringhe di trigger di un'attività.</span><span class="sxs-lookup"><span data-stu-id="47d50-109">The following procedure describes how to retrieve the trigger strings of a task.</span></span>

<span data-ttu-id="47d50-110">**Per recuperare le stringhe di trigger di un'attività**</span><span class="sxs-lookup"><span data-stu-id="47d50-110">**To retrieve the trigger strings of a task**</span></span>

1.  <span data-ttu-id="47d50-111">Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="47d50-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="47d50-112">In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="47d50-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="47d50-113">Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività.</span><span class="sxs-lookup"><span data-stu-id="47d50-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="47d50-114">Si noti che questo esempio Mostra come ottenere l'attività di test.</span><span class="sxs-lookup"><span data-stu-id="47d50-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="47d50-115">Chiamare **ITask:: GetTriggerCount** per verificare il numero di trigger associati a un'attività.</span><span class="sxs-lookup"><span data-stu-id="47d50-115">Call **ITask::GetTriggerCount** to find out how many triggers are associated with a task.</span></span> <span data-ttu-id="47d50-116">Si noti che [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) è un metodo [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ereditato da [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="47d50-116">(Note that [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
4.  <span data-ttu-id="47d50-117">Visualizzare le stringhe del trigger, chiamando **ITask:: GetTriggerString** per ogni trigger associato all'attività.</span><span class="sxs-lookup"><span data-stu-id="47d50-117">Display the trigger strings, calling **ITask::GetTriggerString** for each trigger associated with the task.</span></span> <span data-ttu-id="47d50-118">Si noti che [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) è un metodo [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ereditato da [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="47d50-118">(Note that [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
5.  <span data-ttu-id="47d50-119">Rilasciare tutte le risorse.</span><span class="sxs-lookup"><span data-stu-id="47d50-119">Release all resources.</span></span> <span data-ttu-id="47d50-120">Chiamare [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare le stringhe del trigger e **ITask:: Release** per rilasciare l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="47d50-120">Call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the trigger strings and **ITask::Release** to release the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="47d50-121">Si noti che la [**versione**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) è un metodo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da **ITask**.</span><span class="sxs-lookup"><span data-stu-id="47d50-121">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by **ITask**.)</span></span>



| <span data-ttu-id="47d50-122">Per un esempio di codice di</span><span class="sxs-lookup"><span data-stu-id="47d50-122">For a code example of</span></span>                                                         | <span data-ttu-id="47d50-123">Vedere</span><span class="sxs-lookup"><span data-stu-id="47d50-123">See</span></span>                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="47d50-124">Recupero di una stringa di trigger per tutti i trigger associati a un'attività nota</span><span class="sxs-lookup"><span data-stu-id="47d50-124">Retrieving a trigger string for all the triggers associated with a known task</span></span> | [<span data-ttu-id="47d50-125">Esempio di codice: recupero di stringhe di trigger</span><span class="sxs-lookup"><span data-stu-id="47d50-125">Code Example: Retrieving Trigger Strings</span></span>](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a><span data-ttu-id="47d50-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47d50-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47d50-127">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="47d50-127">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 