---
title: Uso della Utilità di pianificazione
description: In questa sezione sono contenuti esempi di codice che illustrano come viene utilizzata l'API di Utilità di pianificazione e gli esempi XML in cui viene illustrata la modalità di definizione delle attività nello schema di Utilità di pianificazione.
ms.assetid: 6346cbd3-b584-47b4-8313-7830f7fd77b3
keywords:
- trigger Utilità di pianificazione, esempi
- avvio di un'attività Utilità di pianificazione
- creazione di attività Utilità di pianificazione
- Utilità di pianificazione Utilità di pianificazione utilizzando
- Esempi di Utilità di pianificazione Utilità di pianificazione
- Utilità di pianificazione Utilità di pianificazione, esempi vedere Utilità di pianificazione esempi Utilità di pianificazione
- esempi Utilità di pianificazione vedere Utilità di pianificazione esempi Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f81dda9551917b8f6345248a316bd5941de53f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297605"
---
# <a name="using-the-task-scheduler"></a><span data-ttu-id="31afb-110">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="31afb-110">Using the Task Scheduler</span></span>

<span data-ttu-id="31afb-111">In questa sezione sono contenuti esempi di codice che illustrano come viene utilizzata l'API di Utilità di pianificazione e gli esempi XML in cui viene illustrata la modalità di definizione delle attività nello schema di Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="31afb-111">This section contains code examples that illustrate how the Task Scheduler API is used and XML examples that show how tasks are defined in the Task Scheduler schema.</span></span> <span data-ttu-id="31afb-112">La maggior parte di questi esempi è un codice autonomo che può essere eseguito in modo indipendente o incollato in un'applicazione di dimensioni maggiori e modificato in base ai requisiti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="31afb-112">Most of these examples are stand-alone code that can be run independently, or pasted into a larger application and modified to the requirements of the application.</span></span>

<span data-ttu-id="31afb-113">Nella tabella seguente sono elencati Utilità di pianificazione 2,0 esempi inclusi in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="31afb-113">The following table lists Task Scheduler 2.0 examples included in this section.</span></span>



| <span data-ttu-id="31afb-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="31afb-114">Example</span></span>                                                                                                    | <span data-ttu-id="31afb-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31afb-115">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="31afb-116">Avvio di un eseguibile in un momento specifico</span><span class="sxs-lookup"><span data-stu-id="31afb-116">Starting an Executable at a Specific Time</span></span>](starting-an-executable-at-a-spcific-time.md)                  | <span data-ttu-id="31afb-117">Definisce un'attività che avvia il blocco note a un'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="31afb-117">Defines a task that starts Notepad at a specified time.</span></span>                                |
| [<span data-ttu-id="31afb-118">Avvio di un eseguibile ogni giorno</span><span class="sxs-lookup"><span data-stu-id="31afb-118">Starting an Executable Daily</span></span>](starting-an-executable-daily.md)                                           | <span data-ttu-id="31afb-119">Definisce un'attività che avvia il blocco note ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="31afb-119">Defines a task that starts Notepad daily.</span></span>                                              |
| [<span data-ttu-id="31afb-120">Avvio di un eseguibile all'avvio del sistema</span><span class="sxs-lookup"><span data-stu-id="31afb-120">Starting an Executable on System Boot</span></span>](starting-an-executable-on-system-boot.md)                         | <span data-ttu-id="31afb-121">Definisce un'attività che avvia il blocco note quando viene avviato il sistema.</span><span class="sxs-lookup"><span data-stu-id="31afb-121">Defines a task that starts Notepad when the system is booted.</span></span>                          |
| [<span data-ttu-id="31afb-122">Avvio di un eseguibile settimanalmente</span><span class="sxs-lookup"><span data-stu-id="31afb-122">Starting an Executable Weekly</span></span>](starting-an-executable-weekly.md)                                         | <span data-ttu-id="31afb-123">Definisce un'attività che avvia il blocco note su base settimanale.</span><span class="sxs-lookup"><span data-stu-id="31afb-123">Defines a task that starts Notepad on a weekly basis.</span></span>                                  |
| [<span data-ttu-id="31afb-124">Avvio di un eseguibile quando un'attività è registrata</span><span class="sxs-lookup"><span data-stu-id="31afb-124">Starting an Executable When a Task is Registered</span></span>](starting-an-executable-when-a-task-is-registered.md)   | <span data-ttu-id="31afb-125">Definisce un'attività che avvia il blocco note quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="31afb-125">Defines a task that starts Notepad when the task is registered.</span></span>                        |
| [<span data-ttu-id="31afb-126">Avvio di un eseguibile quando un utente esegue l'accesso</span><span class="sxs-lookup"><span data-stu-id="31afb-126">Starting an Executable When a User Logs On</span></span>](starting-an-executable-when-a-user-logs-on.md)               | <span data-ttu-id="31afb-127">Definisce un'attività che avvia il blocco note quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="31afb-127">Defines a task that starts Notepad when a user logs on.</span></span>                                |
| [<span data-ttu-id="31afb-128">Enumerazione delle attività e visualizzazione delle informazioni sulle attività</span><span class="sxs-lookup"><span data-stu-id="31afb-128">Enumerating Tasks and Displaying Task Information</span></span>](enumerating-tasks-and-displaying-task-information.md) | <span data-ttu-id="31afb-129">Enumera tutte le attività nel computer locale e visualizza lo stato di ogni attività.</span><span class="sxs-lookup"><span data-stu-id="31afb-129">Enumerates through all the tasks on the local computer and displays each task's state.</span></span> |



 

<span data-ttu-id="31afb-130">Nella tabella seguente sono elencati Utilità di pianificazione 1,0 esempi inclusi in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="31afb-130">The following table lists Task Scheduler 1.0 examples included in this section.</span></span> 

| <span data-ttu-id="31afb-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="31afb-131">Example</span></span>                                                                                    | <span data-ttu-id="31afb-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31afb-132">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31afb-133">Esempio di creazione di un'attività con NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="31afb-133">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) | <span data-ttu-id="31afb-134">Crea una nuova attività.</span><span class="sxs-lookup"><span data-stu-id="31afb-134">Creates a new task.</span></span>                                                                           |
| [<span data-ttu-id="31afb-135">Esempio di attività di enumerazione</span><span class="sxs-lookup"><span data-stu-id="31afb-135">Enumerating Tasks Example</span></span>](enumerating-tasks-example.md)                                 | <span data-ttu-id="31afb-136">Enumera tutte le attività nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="31afb-136">Enumerates all the tasks on the local computer.</span></span>                                               |
| [<span data-ttu-id="31afb-137">Avvio di un esempio di attività</span><span class="sxs-lookup"><span data-stu-id="31afb-137">Starting a Task Example</span></span>](starting-a-task-example.md)                                     | <span data-ttu-id="31afb-138">Avvia un'attività nota.</span><span class="sxs-lookup"><span data-stu-id="31afb-138">Starts a known task.</span></span>                                                                          |
| [<span data-ttu-id="31afb-139">Modifica di un elemento di lavoro utilizzando le pagine delle proprietà</span><span class="sxs-lookup"><span data-stu-id="31afb-139">Editing a Work Item using Property Pages</span></span>](editing-a-work-item-using-property-pages.md)   | <span data-ttu-id="31afb-140">Consente di visualizzare le pagine delle proprietà di un'attività per la modifica.</span><span class="sxs-lookup"><span data-stu-id="31afb-140">Displays the property pages of a task for editing.</span></span>                                            |
| [<span data-ttu-id="31afb-141">Recupero degli esempi di proprietà degli elementi di lavoro</span><span class="sxs-lookup"><span data-stu-id="31afb-141">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       | <span data-ttu-id="31afb-142">Set di esempi che illustrano come recuperare le proprietà che si applicano a tutti i tipi di elementi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="31afb-142">A set of examples that show how to retrieve properties that apply to all types of work items.</span></span> |
| [<span data-ttu-id="31afb-143">Impostazione degli esempi di proprietà degli elementi di lavoro</span><span class="sxs-lookup"><span data-stu-id="31afb-143">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             | <span data-ttu-id="31afb-144">Set di esempi che illustrano come impostare le proprietà che si applicano a tutti i tipi di elementi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="31afb-144">A set of examples that show how to set properties that apply to all types of work items.</span></span>      |
| [<span data-ttu-id="31afb-145">Esempi di recupero di proprietà di attività</span><span class="sxs-lookup"><span data-stu-id="31afb-145">Retrieving Task Property Examples</span></span>](retrieving-task-property-examples.md)                 | <span data-ttu-id="31afb-146">Set di esempi che illustrano come recuperare le proprietà univoche delle attività.</span><span class="sxs-lookup"><span data-stu-id="31afb-146">A set of examples that show how to retrieve properties unique to tasks.</span></span>                       |
| [<span data-ttu-id="31afb-147">Esempi di impostazione delle proprietà delle attività</span><span class="sxs-lookup"><span data-stu-id="31afb-147">Setting Task Property Examples</span></span>](setting-task-property-examples.md)                       | <span data-ttu-id="31afb-148">Set di esempi che illustrano come impostare le proprietà univoche per le attività.</span><span class="sxs-lookup"><span data-stu-id="31afb-148">A set of examples that show how to set properties unique to tasks.</span></span>                            |
| [<span data-ttu-id="31afb-149">Esempio di recupero di una pagina attività</span><span class="sxs-lookup"><span data-stu-id="31afb-149">Retrieving a Task Page Example</span></span>](retrieving-a-task-page-example.md)                       | <span data-ttu-id="31afb-150">Recupera e visualizza la pagina generale dell'attività di un'attività nota.</span><span class="sxs-lookup"><span data-stu-id="31afb-150">Retrieves and displays the general task page of a known task.</span></span>                                 |
| [<span data-ttu-id="31afb-151">Creazione di un nuovo trigger</span><span class="sxs-lookup"><span data-stu-id="31afb-151">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                       | <span data-ttu-id="31afb-152">Crea un nuovo trigger per un'attività nota.</span><span class="sxs-lookup"><span data-stu-id="31afb-152">Creates a new trigger for a known task.</span></span>                                                       |
| [<span data-ttu-id="31afb-153">Esempio di creazione di un trigger inattivo</span><span class="sxs-lookup"><span data-stu-id="31afb-153">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)                   | <span data-ttu-id="31afb-154">Crea un trigger inattivo basato su eventi per un'attività nota.</span><span class="sxs-lookup"><span data-stu-id="31afb-154">Creates an event-based idle trigger for a known task.</span></span>                                         |
| [<span data-ttu-id="31afb-155">Chiusura di un esempio di attività</span><span class="sxs-lookup"><span data-stu-id="31afb-155">Terminating a Task Example</span></span>](terminating-a-task-example.md)                               | <span data-ttu-id="31afb-156">Termina un'attività mentre è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="31afb-156">Terminates a task while it is running.</span></span>                                                        |
| [<span data-ttu-id="31afb-157">Esempio di recupero di stringhe di trigger</span><span class="sxs-lookup"><span data-stu-id="31afb-157">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)               | <span data-ttu-id="31afb-158">Recupera la stringa di trigger di tutti i trigger associati a un'attività nota.</span><span class="sxs-lookup"><span data-stu-id="31afb-158">Retrieves the trigger string of all triggers associated with a known task.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="31afb-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31afb-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31afb-160">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="31afb-160">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="31afb-161">Informazioni sul Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="31afb-161">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 




