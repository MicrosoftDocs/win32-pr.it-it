---
title: Manipolazione degli elementi di lavoro
description: L'interfaccia IScheduledWorkItem fornisce metodi per il recupero e l'impostazione delle proprietà degli elementi di lavoro. creazione, recupero ed eliminazione di trigger per gli elementi di lavoro (l'impostazione del trigger deve essere eseguita con il metodo setrigger ITaskTrigger); e per l'esecuzione, la terminazione e l'eliminazione dell'elemento di lavoro. Nota per le proprietà di un tipo specifico di elemento di lavoro, fare riferimento all'interfaccia per quel tipo di oggetto. Ad esempio, non è possibile impostare il livello di priorità di un elemento di lavoro; Tuttavia, è possibile utilizzare i metodi dell'interfaccia ITask per recuperare e impostare la priorità di un'attività.
ms.assetid: 8aedf96d-e43d-4aac-ad8c-860379209f95
keywords:
- elementi di lavoro Utilità di pianificazione, gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33680d04da9d34f54085d182ed61edda9e8b232f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728546"
---
# <a name="manipulating-work-items"></a><span data-ttu-id="f1e63-105">Manipolazione degli elementi di lavoro</span><span class="sxs-lookup"><span data-stu-id="f1e63-105">Manipulating Work Items</span></span>

<span data-ttu-id="f1e63-106">L'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornisce metodi per il recupero e l'impostazione delle proprietà degli elementi di lavoro. creazione, recupero ed eliminazione di trigger per gli elementi di lavoro (l'impostazione del trigger deve essere eseguita con il metodo [**ITaskTrigger:: setrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) ); e per l'esecuzione, la terminazione e l'eliminazione dell'elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f1e63-106">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface provides methods for retrieving and setting work item properties; creating, retrieving, and deleting triggers for work items (setting the trigger must be done with the [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) method); and for running, terminating, and deleting the work item.</span></span>

> [!Note]  
> <span data-ttu-id="f1e63-107">Per le proprietà di un tipo specifico di elemento di lavoro, fare riferimento all'interfaccia per quel tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1e63-107">For the properties of a specific type of work item, refer to the interface for that type of object.</span></span> <span data-ttu-id="f1e63-108">Ad esempio, non è possibile impostare il livello di priorità di un elemento di lavoro; Tuttavia, è possibile utilizzare i metodi dell'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) per recuperare e impostare la priorità di un'attività.</span><span class="sxs-lookup"><span data-stu-id="f1e63-108">For example, you cannot set the priority level of a work item; however, you can use the methods of the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface to retrieve and set the priority of a task.</span></span>

 

<span data-ttu-id="f1e63-109">Ogni volta che si modifica un elemento di lavoro, è necessario chiamare l'oggetto [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) per salvare l'elemento di lavoro modificato su disco.</span><span class="sxs-lookup"><span data-stu-id="f1e63-109">Whenever you modify a work item, you must call the [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) object to save the modified work item to disk.</span></span> <span data-ttu-id="f1e63-110">L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia com standard supportata dall'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="f1e63-110">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface that is supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>

| <span data-ttu-id="f1e63-111">Per esempi di</span><span class="sxs-lookup"><span data-stu-id="f1e63-111">For examples of</span></span>                                                            | <span data-ttu-id="f1e63-112">Vedere</span><span class="sxs-lookup"><span data-stu-id="f1e63-112">See</span></span>                                                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e63-113">Recupero di proprietà che si applicano a tutti i tipi di elementi di lavoro</span><span class="sxs-lookup"><span data-stu-id="f1e63-113">Retrieving properties that apply to all types of work items</span></span>                | [<span data-ttu-id="f1e63-114">Recupero degli esempi di proprietà degli elementi di lavoro</span><span class="sxs-lookup"><span data-stu-id="f1e63-114">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md) |
| <span data-ttu-id="f1e63-115">Impostazione delle proprietà che si applicano a tutti i tipi di elementi di lavoro</span><span class="sxs-lookup"><span data-stu-id="f1e63-115">Setting properties that apply to all types of work items</span></span>                   | [<span data-ttu-id="f1e63-116">Impostazione degli esempi di proprietà degli elementi di lavoro</span><span class="sxs-lookup"><span data-stu-id="f1e63-116">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)       |
| <span data-ttu-id="f1e63-117">Esecuzione di un'attività nota</span><span class="sxs-lookup"><span data-stu-id="f1e63-117">Running a known task</span></span>                                                       | [<span data-ttu-id="f1e63-118">Avvio di un esempio di attività</span><span class="sxs-lookup"><span data-stu-id="f1e63-118">Starting a Task Example</span></span>](starting-a-task-example.md)                               |
| <span data-ttu-id="f1e63-119">Terminazione di un'attività in esecuzione</span><span class="sxs-lookup"><span data-stu-id="f1e63-119">Terminating a running task</span></span>                                                 | [<span data-ttu-id="f1e63-120">Chiusura di un esempio di attività</span><span class="sxs-lookup"><span data-stu-id="f1e63-120">Terminating a Task Example</span></span>](terminating-a-task-example.md)                         |
| <span data-ttu-id="f1e63-121">Creazione di un nuovo trigger per un'attività nota</span><span class="sxs-lookup"><span data-stu-id="f1e63-121">Creating a new trigger for a known task</span></span>                                    | [<span data-ttu-id="f1e63-122">Creazione di un nuovo trigger</span><span class="sxs-lookup"><span data-stu-id="f1e63-122">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                 |
| <span data-ttu-id="f1e63-123">Creazione di un trigger inattivo basato su eventi per un'attività nota</span><span class="sxs-lookup"><span data-stu-id="f1e63-123">Creating an event-based idle trigger for a known task</span></span>                      | [<span data-ttu-id="f1e63-124">Esempio di creazione di un trigger inattivo</span><span class="sxs-lookup"><span data-stu-id="f1e63-124">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)             |
| <span data-ttu-id="f1e63-125">Recupero della stringa di trigger di tutti i trigger associati a un'attività nota</span><span class="sxs-lookup"><span data-stu-id="f1e63-125">Retrieving the trigger string of all triggers associated with a known task</span></span> | [<span data-ttu-id="f1e63-126">Esempio di recupero di stringhe di trigger</span><span class="sxs-lookup"><span data-stu-id="f1e63-126">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)         |



 

 

 