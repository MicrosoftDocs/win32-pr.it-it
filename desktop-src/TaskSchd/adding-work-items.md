---
title: Aggiunta di elementi di lavoro
description: Esistono due modi per aggiungere elementi di lavoro alla TasksFolder pianificata. È possibile creare un nuovo elemento di lavoro all'interno della cartella oppure è possibile aggiungere un elemento di lavoro esistente alla cartella.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- elementi di lavoro Utilità di pianificazione, aggiunta
- attività Utilità di pianificazione, aggiunta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722f776fd36933995cfd9b5a85612b52dae63f7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298479"
---
# <a name="adding-work-items"></a><span data-ttu-id="9bc3b-106">Aggiunta di elementi di lavoro</span><span class="sxs-lookup"><span data-stu-id="9bc3b-106">Adding Work Items</span></span>

<span data-ttu-id="9bc3b-107">Esistono due modi per aggiungere [*elementi di lavoro*](w.md) alla [*TasksFolder pianificata*](s.md).</span><span class="sxs-lookup"><span data-stu-id="9bc3b-107">There are two ways to add [*work items*](w.md) to the [*Scheduled Tasksfolder*](s.md).</span></span> <span data-ttu-id="9bc3b-108">È possibile creare un nuovo elemento di lavoro all'interno della cartella oppure è possibile aggiungere un elemento di lavoro esistente alla cartella.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-108">You can create a new work item within the folder, or you can add an existing work item to the folder.</span></span>

> [!Note]  
> <span data-ttu-id="9bc3b-109">Attualmente, solo gli oggetti attività possono essere aggiunti alla cartella attività pianificate.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-109">Currently, only task objects can be added to the Scheduled Tasks folder.</span></span> <span data-ttu-id="9bc3b-110">Quando si aggiunge un'attività, è necessario conoscerne gli identificatori per la classe dell'attività e l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="9bc3b-110">When adding a task, you must know the identifiers for the task class and the task interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span></span>

 

<span data-ttu-id="9bc3b-111">Per creare nuovi elementi di lavoro, chiamare il metodo [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) .</span><span class="sxs-lookup"><span data-stu-id="9bc3b-111">You create new work items by calling the [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) method.</span></span> <span data-ttu-id="9bc3b-112">Questo metodo crea un nuovo oggetto elemento di lavoro usando il nome fornito e aggiunge l'elemento di lavoro alla cartella delle attività pianificate.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-112">This method creates a new work item object using the name that you provide and adds the work item to the Scheduled Tasks folder.</span></span> <span data-ttu-id="9bc3b-113">Quando si crea un nuovo elemento di lavoro, il Utilità di pianificazione alloca la memoria necessaria per il nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-113">When you create a new work item, the Task Scheduler allocates the memory that is required for the new object.</span></span>

<span data-ttu-id="9bc3b-114">Per aggiungere elementi di lavoro esistenti alla cartella delle attività pianificate, chiamare il metodo [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) .</span><span class="sxs-lookup"><span data-stu-id="9bc3b-114">To add existing work items to the Scheduled Tasks folder, call the [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) method.</span></span> <span data-ttu-id="9bc3b-115">Quando si chiama questo metodo, è necessario creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-115">When you call this method, you must create the object.</span></span>

<span data-ttu-id="9bc3b-116">I nomi forniti per gli elementi di lavoro devono essere univoci all'interno della cartella attività pianificate.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-116">The names you supply for work items must be unique within the Scheduled Tasks folder.</span></span> <span data-ttu-id="9bc3b-117">Se un elemento di lavoro con lo stesso nome esiste già quando si chiama il metodo [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) o [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) , il metodo restituisce un errore relativo al **file di errore \_ \_ esistente** .</span><span class="sxs-lookup"><span data-stu-id="9bc3b-117">If a work item with the same name already exists when you call either the [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) method or the [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) method, the method returns an **ERROR\_FILE\_EXISTS** error.</span></span> <span data-ttu-id="9bc3b-118">Per altre informazioni, vedere [creazione di un'attività con l'esempio NewWorkItem](creating-a-task-using-newworkitem-example.md).</span><span class="sxs-lookup"><span data-stu-id="9bc3b-118">For more information, see [Creating a Task Using NewWorkItem Example](creating-a-task-using-newworkitem-example.md).</span></span>

 

 




