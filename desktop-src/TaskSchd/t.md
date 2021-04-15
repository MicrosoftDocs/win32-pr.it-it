---
title: T (Utilità di pianificazione)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d4c6d7ba-7bca-420d-a4dc-4daea816f99c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2730cdbe3a13456aed0e613a614d43a0e56e6673
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517283"
---
# <a name="t-task-scheduler"></a><span data-ttu-id="749e1-103">T (Utilità di pianificazione)</span><span class="sxs-lookup"><span data-stu-id="749e1-103">T (Task Scheduler)</span></span>

<span data-ttu-id="749e1-104">A B C D [E](e.md) F G H [i](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="749e1-104">A B C D [E](e.md) F G H [I](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="749e1-105"><span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**oggetti attività**</span><span class="sxs-lookup"><span data-stu-id="749e1-105"><span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**task objects**</span></span>
</dt> <dd>

<span data-ttu-id="749e1-106">Istanze di un oggetto che fornisce i metodi per la gestione delle attività.</span><span class="sxs-lookup"><span data-stu-id="749e1-106">Instances of an object that provides methods for managing tasks.</span></span> <span data-ttu-id="749e1-107">Sono inclusi i metodi per l'impostazione e il recupero delle proprietà. esecuzione, terminazione ed eliminazione di attività; e la creazione di nuovi trigger e il recupero di trigger obsoleti.</span><span class="sxs-lookup"><span data-stu-id="749e1-107">This includes methods for setting and retrieving properties; running, terminating, and deleting tasks; and creating new triggers and retrieving old triggers.</span></span>

<span data-ttu-id="749e1-108">L'oggetto attività viene creato da chiamate a [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) e [**IScheduledWorkItem:: GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span><span class="sxs-lookup"><span data-stu-id="749e1-108">The task object is created by calls to [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) and [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span></span>

</dd> <dt>

<span data-ttu-id="749e1-109"><span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**oggetti utilità di pianificazione**</span><span class="sxs-lookup"><span data-stu-id="749e1-109"><span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**task scheduler objects**</span></span>
</dt> <dd>

<span data-ttu-id="749e1-110">Istanze di un oggetto che rappresenta il servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="749e1-110">Instances of an object the represents the Task Scheduler service.</span></span> <span data-ttu-id="749e1-111">Questo oggetto supporta due interfacce: **IUnknown** e [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (attualmente le attività sono l'unico tipo di elementi di lavoro supportati dal servizio Utilità di pianificazione).</span><span class="sxs-lookup"><span data-stu-id="749e1-111">This object supports two interfaces: **IUnknown** and [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (currently tasks are the only type of work items supported by the Task Scheduler service).</span></span>

<span data-ttu-id="749e1-112">Gli oggetti utilità di pianificazione vengono creati tramite chiamate a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="749e1-112">Task scheduler objects are created by calls to **CoCreateInstance**.</span></span>

</dd> <dt>

<span data-ttu-id="749e1-113"><span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**oggetti trigger attività**</span><span class="sxs-lookup"><span data-stu-id="749e1-113"><span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**task trigger objects**</span></span>
</dt> <dd>

<span data-ttu-id="749e1-114">Istanze di un oggetto che fornisce i metodi per l'impostazione e il recupero di trigger di attività.</span><span class="sxs-lookup"><span data-stu-id="749e1-114">Instances of an object the provides methods for setting and retrieving task triggers.</span></span> <span data-ttu-id="749e1-115">Questo oggetto supporta due interfacce: **IUnknown** e [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).</span><span class="sxs-lookup"><span data-stu-id="749e1-115">This object supports two interfaces: **IUnknown** and [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).</span></span>

<span data-ttu-id="749e1-116">Gli oggetti trigger di attività vengono creati tramite chiamate a [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) e [**IScheduledWorkItem:: GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span><span class="sxs-lookup"><span data-stu-id="749e1-116">Task trigger objects are created by calls to [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) and [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span></span>

<span data-ttu-id="749e1-117">Vedere anche: *trigger*.</span><span class="sxs-lookup"><span data-stu-id="749e1-117">See also: *triggers*.</span></span>

</dd> <dt>

<span data-ttu-id="749e1-118"><span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**attività**</span><span class="sxs-lookup"><span data-stu-id="749e1-118"><span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**tasks**</span></span>
</dt> <dd>

<span data-ttu-id="749e1-119">Qualsiasi elemento che può essere eseguito dal Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="749e1-119">Any item that the Task Scheduler can execute.</span></span> <span data-ttu-id="749e1-120">Questi elementi possono includere uno degli elementi seguenti (come supportato dal sistema operativo in cui verrà eseguita l'attività): Win32® applicazioni, applicazioni Win16, applicazioni OS/2, MS-DOS® applicazioni, file batch ( \* . bat), file di comando ( \* cmd) o qualsiasi tipo di file registrato correttamente.</span><span class="sxs-lookup"><span data-stu-id="749e1-120">These items may include any of the following (as supported by the operating system on which the task will execute): Win32® applications, Win16 applications, OS/2 applications, MS-DOS® applications, batch files (\*.bat), command files (\*.cmd), or any properly registered file type.</span></span>

</dd> <dt>

<span data-ttu-id="749e1-121"><span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Cartella attività**</span><span class="sxs-lookup"><span data-stu-id="749e1-121"><span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Tasks folder**</span></span>
</dt> <dd>

<span data-ttu-id="749e1-122">La cartella in cui sono elencati tutti i file delle attività (attualmente, le attività sono gli unici elementi di lavoro disponibili).</span><span class="sxs-lookup"><span data-stu-id="749e1-122">The folder that lists all task files (currently, tasks are the only work items available).</span></span> <span data-ttu-id="749e1-123">Questi file contengono le informazioni sull'attività.</span><span class="sxs-lookup"><span data-stu-id="749e1-123">These files contain the information about the task.</span></span> <span data-ttu-id="749e1-124">Il nome di questi file riflette il nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="749e1-124">The name of these files reflects the name of the task.</span></span>

<span data-ttu-id="749e1-125">È possibile recuperare il percorso della cartella attività dal registro di sistema ottenendo i dati per il valore seguente:</span><span class="sxs-lookup"><span data-stu-id="749e1-125">You can retrieve the location of the Tasks folder from the registry by getting data for the following value:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span data-ttu-id="749e1-126"><span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**trigger**</span><span class="sxs-lookup"><span data-stu-id="749e1-126"><span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**triggers**</span></span>
</dt> <dd>

<span data-ttu-id="749e1-127">Set di criteri che, se soddisfatti, comporterà l'esecuzione di un'attività.</span><span class="sxs-lookup"><span data-stu-id="749e1-127">A set of criteria that, when met, will cause a task to be executed.</span></span> <span data-ttu-id="749e1-128">Utilità di pianificazione fornisce trigger basati sul tempo e sugli eventi che possono specificare gli orari di inizio, i criteri di ripetizione e altri parametri dell'attività.</span><span class="sxs-lookup"><span data-stu-id="749e1-128">Task Scheduler provides time-based and event-based triggers that can specify task start times, repetition criteria, and other parameters.</span></span>

</dd> <dt>

<span data-ttu-id="749e1-129"><span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**stringhe di trigger**</span><span class="sxs-lookup"><span data-stu-id="749e1-129"><span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**trigger strings**</span></span>
</dt> <dd>

<span data-ttu-id="749e1-130">Stringa che descrive il trigger.</span><span class="sxs-lookup"><span data-stu-id="749e1-130">A string that describes the trigger.</span></span> <span data-ttu-id="749e1-131">Questa stringa viene creata dal servizio Utilità di pianificazione e viene visualizzata nell'interfaccia utente Utilità di pianificazione in un formato simile a "alle 14:00 ogni giorno, a partire dal 5/11/97".</span><span class="sxs-lookup"><span data-stu-id="749e1-131">This string is created by the Task Scheduler service, and appears in the Task Scheduler user interface in a form similar to "At 2PM every day, starting 5/11/97."</span></span>

</dd> <dt>

<span data-ttu-id="749e1-132"><span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**strutture trigger**</span><span class="sxs-lookup"><span data-stu-id="749e1-132"><span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**trigger structures**</span></span>
</dt> <dd>

<span data-ttu-id="749e1-133">Struttura [**del \_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) utilizzata durante l'impostazione o il recupero dei criteri che definiscono il trigger.</span><span class="sxs-lookup"><span data-stu-id="749e1-133">The [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure used when setting or retrieving the criteria that defines the trigger.</span></span> <span data-ttu-id="749e1-134">I criteri includono quando il trigger viene attivato e il tipo del trigger.</span><span class="sxs-lookup"><span data-stu-id="749e1-134">The criteria includes when the trigger will fire, and the type of the trigger.</span></span>

</dd> </dl>

 

 




