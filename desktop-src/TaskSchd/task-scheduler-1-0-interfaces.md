---
title: Interfacce di Utilità di pianificazione 1,0
description: Le interfacce descritte negli argomenti seguenti forniscono l'accesso a livello di codice alle funzionalità disponibili all'interno del Utilità di pianificazione usato nei sistemi operativi Windows 2000, Windows XP e Windows Server 2003.
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bab12b59d4b4561ecbe46c09a76c69209574c9d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104224576"
---
# <a name="task-scheduler-10-interfaces"></a><span data-ttu-id="87296-103">Interfacce di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="87296-103">Task Scheduler 1.0 Interfaces</span></span>

<span data-ttu-id="87296-104">\[\[Questa API può essere modificata o non disponibile nelle versioni successive del sistema operativo o del prodotto.</span><span class="sxs-lookup"><span data-stu-id="87296-104">\[\[This API may be altered or unavailable in subsequent versions of the operating system or product.</span></span> <span data-ttu-id="87296-105">Usare invece le [interfacce Utilità di pianificazione 2,0](task-scheduler-2-0-interfaces.md) o [utilità di pianificazione 2,0 tipi enumerati](task-scheduler-2-0-enumerated-types.md) . \]\]</span><span class="sxs-lookup"><span data-stu-id="87296-105">Please use the [Task Scheduler 2.0 Interfaces](task-scheduler-2-0-interfaces.md) or [Task Scheduler 2.0 Enumerated Types](task-scheduler-2-0-enumerated-types.md) instead.\] \]</span></span>

<span data-ttu-id="87296-106">Le interfacce descritte negli argomenti seguenti forniscono l'accesso a livello di codice alle funzionalità disponibili all'interno del Utilità di pianificazione usato nei sistemi operativi Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="87296-106">The interfaces that are described in the following topics provide programmatic access to the functionality that is available within the Task Scheduler that is used in the Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="87296-107">Questi argomenti contengono una descrizione dell'interfaccia, un elenco delle proprietà e dei metodi definiti dall'interfaccia e commenti sulle circostanze speciali che devono essere annotate quando si usa l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="87296-107">These topics contain a description of the interface, a list of the properties and methods defined by the interface, and remarks about any special circumstances that should be noted when using the interface.</span></span>


<span data-ttu-id="87296-108">Le interfacce seguenti sono introdotte da Utilità di pianificazione 1,0.</span><span class="sxs-lookup"><span data-stu-id="87296-108">The following interfaces are introduced by Task Scheduler 1.0.</span></span>



| <span data-ttu-id="87296-109">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="87296-109">Interface</span></span>                                        | <span data-ttu-id="87296-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87296-110">Description</span></span>                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87296-111">**IEnumWorkItems**</span><span class="sxs-lookup"><span data-stu-id="87296-111">**IEnumWorkItems**</span></span>](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | <span data-ttu-id="87296-112">Fornisce i metodi per enumerare le attività nella [*cartella delle attività pianificate*](s.md).</span><span class="sxs-lookup"><span data-stu-id="87296-112">Provides the methods for enumerating the tasks in the [*Scheduled Tasks folder*](s.md).</span></span>                                                                                                              |
| [<span data-ttu-id="87296-113">**IProvideTaskPage**</span><span class="sxs-lookup"><span data-stu-id="87296-113">**IProvideTaskPage**</span></span>](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | <span data-ttu-id="87296-114">Fornisce i metodi per accedere alle impostazioni della finestra delle proprietà di un'attività.</span><span class="sxs-lookup"><span data-stu-id="87296-114">Provides the methods to access the property sheet settings of a task.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="87296-115">**IScheduledWorkItem**</span><span class="sxs-lookup"><span data-stu-id="87296-115">**IScheduledWorkItem**</span></span>](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | <span data-ttu-id="87296-116">Fornisce i metodi per la gestione di [*elementi di lavoro*](w.md)specifici.</span><span class="sxs-lookup"><span data-stu-id="87296-116">Provides the methods for managing specific [*work items*](w.md).</span></span>                                                                                                                                                 |
| [<span data-ttu-id="87296-117">**ITask**</span><span class="sxs-lookup"><span data-stu-id="87296-117">**ITask**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itask)                           | <span data-ttu-id="87296-118">Fornisce i metodi per eseguire attività, ottenere o impostare informazioni sulle attività e terminare le attività.</span><span class="sxs-lookup"><span data-stu-id="87296-118">Provides the methods for running tasks, getting or setting task information, and terminating tasks.</span></span> <span data-ttu-id="87296-119">Viene derivato dall'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ed eredita tutti i metodi di tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="87296-119">It is derived from the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface and inherits all the methods of that interface.</span></span> |
| [<span data-ttu-id="87296-120">**ITaskScheduler**</span><span class="sxs-lookup"><span data-stu-id="87296-120">**ITaskScheduler**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | <span data-ttu-id="87296-121">Fornisce i metodi per la pianificazione delle attività.</span><span class="sxs-lookup"><span data-stu-id="87296-121">Provides the methods for scheduling tasks.</span></span>                                                                                                                                                                                            |
| [<span data-ttu-id="87296-122">**ITaskTrigger**</span><span class="sxs-lookup"><span data-stu-id="87296-122">**ITaskTrigger**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | <span data-ttu-id="87296-123">Fornisce i metodi per accedere ai trigger e impostarli per un'attività.</span><span class="sxs-lookup"><span data-stu-id="87296-123">Provides the methods for accessing and setting triggers for a task.</span></span> <span data-ttu-id="87296-124">I trigger specificano l'ora di inizio, i criteri di ripetizione e altri parametri di attività che controllano quando viene eseguita un'attività.</span><span class="sxs-lookup"><span data-stu-id="87296-124">Triggers specify task start times, repetition criteria, and other parameters that control when a task is run.</span></span>                                                     |



 

 

 




