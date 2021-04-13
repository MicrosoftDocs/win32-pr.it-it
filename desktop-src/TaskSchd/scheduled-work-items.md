---
title: Elementi di lavoro pianificati
description: Il Utilità di pianificazione usa due termini per descrivere ciò che può pianificare gli elementi di lavoro e le attività.
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- elementi di lavoro Utilità di pianificazione
- elementi di lavoro Utilità di pianificazione, rispetto alle attività
- Utilità di pianificazione attività
- Utilità di pianificazione attività, rispetto agli elementi di lavoro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586747e4049529dcfe747959aae994360a7b1485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329327"
---
# <a name="scheduled-work-items"></a><span data-ttu-id="0f48c-107">Elementi di lavoro pianificati</span><span class="sxs-lookup"><span data-stu-id="0f48c-107">Scheduled Work Items</span></span>

<span data-ttu-id="0f48c-108">Il Utilità di pianificazione usa due termini per descrivere ciò che può pianificare: elementi di lavoro e attività.</span><span class="sxs-lookup"><span data-stu-id="0f48c-108">The Task Scheduler uses two terms to describe what it can schedule: work items and tasks.</span></span> <span data-ttu-id="0f48c-109">Di questi due termini, [*elemento di lavoro*](w.md) è un termine più generale che descrive qualsiasi tipo di elemento che è possibile pianificare.</span><span class="sxs-lookup"><span data-stu-id="0f48c-109">Of these two terms, [*work item*](w.md) is a more general term that describes any type of item that can be scheduled.</span></span> <span data-ttu-id="0f48c-110">Un *elemento di lavoro* può essere qualsiasi elemento eseguito dal servizio Utilità di pianificazione in un momento specificato dal trigger o dai trigger dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0f48c-110">A *work item* can be any item that the Task Scheduler service runs at a time that is specified by the item's trigger(s).</span></span>

<span data-ttu-id="0f48c-111">Al contrario, un' [*attività*](t.md) è un tipo specifico di elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0f48c-111">In contrast, a [*task*](t.md) is a specific type of work item.</span></span> <span data-ttu-id="0f48c-112">Attualmente, l'unico tipo di elemento di lavoro pianificato supportato è un'attività.</span><span class="sxs-lookup"><span data-stu-id="0f48c-112">Currently, the only type of scheduled work item that is supported is a task.</span></span>

<span data-ttu-id="0f48c-113">L'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) contiene metodi supportati da tutti i tipi di elementi di lavoro pianificati.</span><span class="sxs-lookup"><span data-stu-id="0f48c-113">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface contains methods that are supported by all types of scheduled work items.</span></span> <span data-ttu-id="0f48c-114">Ad esempio, le informazioni sull'account, le esecuzioni e i commenti definiti dall'applicazione sono proprietà che possono essere valide per tutti i tipi di elementi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0f48c-114">For example, account information, run times, and application-defined comments are properties that may apply to all types of work items.</span></span> <span data-ttu-id="0f48c-115">È possibile impostare e recuperare queste proprietà tramite l'interfaccia **IScheduledWorkItem** .</span><span class="sxs-lookup"><span data-stu-id="0f48c-115">These properties can be set and retrieved through the **IScheduledWorkItem** interface.</span></span>

<span data-ttu-id="0f48c-116">L'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) contiene metodi supportati solo dalle attività.</span><span class="sxs-lookup"><span data-stu-id="0f48c-116">The [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface contains methods that are supported only by tasks.</span></span>

<span data-ttu-id="0f48c-117">I metodi dell'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) sono attualmente ereditati dall'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) e in futuro verranno ereditati da altre interfacce di elementi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0f48c-117">The methods of the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface are currently inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface and in the future will be inherited by other work item interfaces.</span></span>

| <span data-ttu-id="0f48c-118">Per esempi di</span><span class="sxs-lookup"><span data-stu-id="0f48c-118">For examples of</span></span>                                              | <span data-ttu-id="0f48c-119">Vedere</span><span class="sxs-lookup"><span data-stu-id="0f48c-119">See</span></span>                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f48c-120">Creazione di una nuova attività.</span><span class="sxs-lookup"><span data-stu-id="0f48c-120">Creating a new task.</span></span>                                         | [<span data-ttu-id="0f48c-121">Esempio di creazione di un'attività con NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="0f48c-121">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) |
| <span data-ttu-id="0f48c-122">Esecuzione di un'attività esistente.</span><span class="sxs-lookup"><span data-stu-id="0f48c-122">Running an existing task.</span></span>                                    | [<span data-ttu-id="0f48c-123">Avvio di un esempio di attività</span><span class="sxs-lookup"><span data-stu-id="0f48c-123">Starting a Task Example</span></span>](starting-a-task-example.md)                                     |
| <span data-ttu-id="0f48c-124">Recupero di proprietà che si applicano a tutti i tipi di elementi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0f48c-124">Retrieving properties that apply to all types of work items.</span></span> | [<span data-ttu-id="0f48c-125">Recupero degli esempi di proprietà degli elementi di lavoro</span><span class="sxs-lookup"><span data-stu-id="0f48c-125">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       |
| <span data-ttu-id="0f48c-126">Impostazione delle proprietà che si applicano a tutti i tipi di elementi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0f48c-126">Setting properties that apply to all types of work items.</span></span>    | [<span data-ttu-id="0f48c-127">Impostazione degli esempi di proprietà degli elementi di lavoro</span><span class="sxs-lookup"><span data-stu-id="0f48c-127">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             |



 

 

 




