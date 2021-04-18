---
title: Attività
description: Un'attività è il lavoro pianificato eseguito dal servizio Utilità di pianificazione.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- Utilità di pianificazione attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbb4ef41915ec70c98b59c9a7ba74c00f283ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298747"
---
# <a name="tasks"></a><span data-ttu-id="c73b0-104">Attività</span><span class="sxs-lookup"><span data-stu-id="c73b0-104">Tasks</span></span>

<span data-ttu-id="c73b0-105">Un'attività è il lavoro pianificato eseguito dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="c73b0-105">A task is the scheduled work that the Task Scheduler service performs.</span></span> <span data-ttu-id="c73b0-106">Un'attività è costituita da componenti diversi, ma un'attività deve contenere un trigger utilizzato dal Utilità di pianificazione per avviare l'attività e un'azione che descrive il lavoro che verrà eseguito dall'Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="c73b0-106">A task is composed of different components, but a task must contain a trigger that the Task Scheduler uses to start the task and an action that describes what work the Task Scheduler will perform.</span></span>

<span data-ttu-id="c73b0-107">Quando si crea un'attività, questa viene archiviata in una cartella attività.</span><span class="sxs-lookup"><span data-stu-id="c73b0-107">When a task is created, it is stored in a task folder.</span></span> <span data-ttu-id="c73b0-108">È possibile accedere alle cartelle delle attività tramite l'interfaccia [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) ([**TaskFolder**](taskfolder.md) per lo scripting) e accedere alle attività tramite l'interfaccia [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) ([**RegisteredTask**](registeredtask.md) per lo scripting) al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="c73b0-108">Task folders can be accessed through the [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) interface ([**TaskFolder**](taskfolder.md) for scripting), and tasks can be accessed through the [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) interface ([**RegisteredTask**](registeredtask.md) for scripting) when they are created.</span></span> <span data-ttu-id="c73b0-109">È possibile modificare gli elenchi di controllo di accesso (ACL) per le attività e le cartelle attività per concedere o negare a determinati utenti e gruppi l'accesso a una cartella attività o attività.</span><span class="sxs-lookup"><span data-stu-id="c73b0-109">You can change access control lists (ACLs) for tasks and task folders in order to grant or deny certain users and groups access to a task or task folder.</span></span> <span data-ttu-id="c73b0-110">Questa operazione può essere eseguita usando il metodo [**IRegisteredTask:: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) , il metodo [**ITaskFolder:: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) oppure specificando un descrittore di sicurezza quando un'attività viene registrata usando il metodo [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) o [**l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) .</span><span class="sxs-lookup"><span data-stu-id="c73b0-110">This can be done by using the [**IRegisteredTask::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) method, the [**ITaskFolder::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) method, or by specifying a security descriptor when a task is registered by using the [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) or [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) method.</span></span>

> [!Note]  
> <span data-ttu-id="c73b0-111">Se all'account di sistema locale viene negato l'accesso a un file attività o a una cartella attività, il servizio Utilità di pianificazione può produrre risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="c73b0-111">If the Local System account is denied access to a task file or task folder, then the Task Scheduler service can produce unexpected results.</span></span>

 

## <a name="components-of-a-task"></a><span data-ttu-id="c73b0-112">Componenti di un'attività</span><span class="sxs-lookup"><span data-stu-id="c73b0-112">Components of a Task</span></span>

<span data-ttu-id="c73b0-113">Nella figura seguente sono illustrati i componenti dell'attività.</span><span class="sxs-lookup"><span data-stu-id="c73b0-113">The following illustration shows the task components.</span></span>

![componenti attività](images/taskcomponents.png)

<span data-ttu-id="c73b0-115">L'elenco seguente contiene una breve descrizione di ogni componente attività:</span><span class="sxs-lookup"><span data-stu-id="c73b0-115">The following list contains a brief description of each task component:</span></span>

-   <span data-ttu-id="c73b0-116">Trigger: Utilità di pianificazione usa trigger basati su eventi o temporali per capire quando avviare un'attività.</span><span class="sxs-lookup"><span data-stu-id="c73b0-116">Triggers: Task Scheduler uses event or time-based triggers to know when to start a task.</span></span> <span data-ttu-id="c73b0-117">Ogni attività può specificare uno o più trigger per avviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="c73b0-117">Every task can specify one or more triggers to start the task.</span></span>

    <span data-ttu-id="c73b0-118">Per ulteriori informazioni sui trigger, vedere [trigger di attività](task-triggers.md).</span><span class="sxs-lookup"><span data-stu-id="c73b0-118">For more information about triggers, see [Task Triggers](task-triggers.md).</span></span>

-   <span data-ttu-id="c73b0-119">Azioni: queste sono le azioni, il lavoro effettivo che viene eseguito dall'attività.</span><span class="sxs-lookup"><span data-stu-id="c73b0-119">Actions: These are the actions, the actual work, that is performed by the task.</span></span> <span data-ttu-id="c73b0-120">Ogni attività può specificare una o più azioni per completare il lavoro.</span><span class="sxs-lookup"><span data-stu-id="c73b0-120">Every task can specify one or more actions to complete its work.</span></span>

    <span data-ttu-id="c73b0-121">Per altre informazioni sulle azioni, vedere [azioni attività](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c73b0-121">For more information about actions, see [Task Actions](task-actions.md).</span></span>

-   <span data-ttu-id="c73b0-122">Entità: le entità definiscono il contesto di sicurezza in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="c73b0-122">Principals: Principals define the security context in which the task is run.</span></span> <span data-ttu-id="c73b0-123">Ad esempio, un'entità potrebbe definire un utente o un gruppo di utenti specifico che può eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="c73b0-123">For example, a principal might define a specific user or user group that can run the task.</span></span>

    <span data-ttu-id="c73b0-124">Per ulteriori informazioni sulle entità, vedere [contesti di sicurezza per le attività](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="c73b0-124">For more information about principals, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

-   <span data-ttu-id="c73b0-125">Impostazioni: si tratta delle impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività in relazione alle condizioni esterne all'attività stessa.</span><span class="sxs-lookup"><span data-stu-id="c73b0-125">Settings: These are the settings that the Task Scheduler uses to run the task with respect to conditions that are external to the task itself.</span></span> <span data-ttu-id="c73b0-126">Queste impostazioni possono ad esempio specificare la priorità dell'attività in relazione ad altre attività, se è possibile eseguire più istanze dell'attività, il modo in cui l'attività viene gestita quando il computer si trova in una condizione di inattività e altre condizioni.</span><span class="sxs-lookup"><span data-stu-id="c73b0-126">For example, these settings can specify the priority of the task with respect to other tasks, whether multiple instances of the task can be run, how the task is handled when the computer is in an idle condition, and other conditions.</span></span>

    <span data-ttu-id="c73b0-127">Per ulteriori informazioni sulle impostazioni delle attività, vedere [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) per lo scripting).</span><span class="sxs-lookup"><span data-stu-id="c73b0-127">For more information about task settings, see [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) for scripting).</span></span>

    > [!Note]  
    > <span data-ttu-id="c73b0-128">Per impostazione predefinita, un'attività verrà arrestata 72 ore dopo l'avvio dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c73b0-128">By default, a task will be stopped 72 hours after it starts to run.</span></span> <span data-ttu-id="c73b0-129">È possibile modificare questa impostazione modificando l'impostazione [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) .</span><span class="sxs-lookup"><span data-stu-id="c73b0-129">You can change this by changing the [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) setting.</span></span>

     

-   <span data-ttu-id="c73b0-130">Informazioni di registrazione: informazioni amministrative raccolte quando l'attività viene registrata.</span><span class="sxs-lookup"><span data-stu-id="c73b0-130">Registration Information: This is administrative information that is gathered when the task is registered.</span></span> <span data-ttu-id="c73b0-131">Ad esempio, queste informazioni descrivono l'autore dell'attività, la data in cui l'attività è stata registrata, una descrizione XML dell'attività e altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c73b0-131">For example, this information describes the author of the task, the date when the task was registered, an XML description of the task, and other information.</span></span>

    <span data-ttu-id="c73b0-132">Per ulteriori informazioni sulle informazioni di registrazione delle attività, vedere [informazioni sulla registrazione delle attività](task-registration-information.md).</span><span class="sxs-lookup"><span data-stu-id="c73b0-132">For more information about task registration information, see [Task Registration Information](task-registration-information.md).</span></span>

-   <span data-ttu-id="c73b0-133">Data: documentazione aggiuntiva sull'attività fornita dall'autore dell'attività.</span><span class="sxs-lookup"><span data-stu-id="c73b0-133">Data: This is additional documentation about the task that is supplied by the author of the task.</span></span> <span data-ttu-id="c73b0-134">Ad esempio, questi dati possono contenere la guida XML che può essere utilizzata dagli utenti quando eseguono l'attività.</span><span class="sxs-lookup"><span data-stu-id="c73b0-134">For example, this data may contain XML Help that can be used by users when they run the task.</span></span>

## <a name="task-apis"></a><span data-ttu-id="c73b0-135">API attività</span><span class="sxs-lookup"><span data-stu-id="c73b0-135">Task APIs</span></span>

<span data-ttu-id="c73b0-136">Utilità di pianificazione 2,0 offre due set di API: un set di oggetti di script e interfacce per Utilità di pianificazione 2,0.</span><span class="sxs-lookup"><span data-stu-id="c73b0-136">Task Scheduler 2.0 provides two sets of APIs: a set of scripting objects and interfaces for Task Scheduler 2.0.</span></span> <span data-ttu-id="c73b0-137">Per ulteriori informazioni, vedere [utilità di pianificazione Reference](task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="c73b0-137">For more information, see [Task Scheduler Reference](task-scheduler-reference.md).</span></span>

<span data-ttu-id="c73b0-138">Per la compatibilità delle attività, impostata tramite la proprietà [**compatibilità**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , è consigliabile impostare solo la \_ compatibilità delle attività \_ V1 se è necessario accedere o modificare un'attività da un computer Windows XP, Windows Server 2003 o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c73b0-138">Task compatibility, which is set through the [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) property, should only be set to TASK\_COMPATIBILITY\_V1 if a task must be accessed or modified from a Windows XP, Windows Server 2003, or Windows 2000 computer.</span></span> <span data-ttu-id="c73b0-139">In caso contrario, è consigliabile usare Utilità di pianificazione compatibilità 2,0, perché include più funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c73b0-139">Otherwise, it is recommended that you use Task Scheduler 2.0 compatibility because it has more features.</span></span>

<span data-ttu-id="c73b0-140">A partire da Utilità di pianificazione 2,0, l'interfaccia [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) ([**TaskService**](taskservice.md) per lo scripting) viene usata come punto di partenza per la creazione di attività in cartelle specifiche.</span><span class="sxs-lookup"><span data-stu-id="c73b0-140">Starting with Task Scheduler 2.0, the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) interface ([**TaskService**](taskservice.md) for scripting) is used as a starting point to create tasks in specified folders.</span></span> <span data-ttu-id="c73b0-141">L'interfaccia [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) ([**TaskDefinition**](taskdefinition.md) per lo scripting) viene usata per conservare tutti i componenti di un'attività, ad esempio le impostazioni, le azioni e i trigger.</span><span class="sxs-lookup"><span data-stu-id="c73b0-141">The [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface ([**TaskDefinition**](taskdefinition.md) for scripting) is used to hold all the components of a task, such as the settings, actions, and triggers.</span></span> <span data-ttu-id="c73b0-142">Le API [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)e [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) forniscono proprietà che vengono quindi utilizzate per definire gli altri componenti dell'attività.</span><span class="sxs-lookup"><span data-stu-id="c73b0-142">The [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction), and [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) APIs provide properties that are then used to define the other components of the task.</span></span> <span data-ttu-id="c73b0-143">Utilità di pianificazione 1,0 fornisce l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , supportata solo per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="c73b0-143">Task Scheduler 1.0 provides the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface, which is supported only for backward compatibility.</span></span>

<span data-ttu-id="c73b0-144">Per gli script, le interfacce di Utilità di pianificazione vengono mappate a oggetti di script con nomi, proprietà e metodi simili.</span><span class="sxs-lookup"><span data-stu-id="c73b0-144">For scripting, the Task Scheduler interfaces map to scripting objects that have the similar names, properties, and methods.</span></span> <span data-ttu-id="c73b0-145">Ad esempio, l'oggetto di scripting [**TaskService**](taskservice.md) ha le stesse proprietà e i metodi dell'interfaccia [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="c73b0-145">For example, the [**TaskService**](taskservice.md) scripting object has the same properties and methods as the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) interface.</span></span>

<span data-ttu-id="c73b0-146">Per ulteriori informazioni ed esempi su come utilizzare le interfacce Utilità di pianificazione, gli oggetti di script e il codice XML, vedere [utilizzo del utilità di pianificazione](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="c73b0-146">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

### <a name="task-scheduler-10-tasks"></a><span data-ttu-id="c73b0-147">Attività Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="c73b0-147">Task Scheduler 1.0 Tasks</span></span>

<span data-ttu-id="c73b0-148">Un'attività Utilità di pianificazione 1,0 è qualsiasi tipo di applicazione o di file che può essere eseguito dall'Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="c73b0-148">A Task Scheduler 1.0 task is any application or file type that the Task Scheduler can execute.</span></span> <span data-ttu-id="c73b0-149">Questi possono includere uno dei seguenti (come supportato dal sistema operativo in cui verrà eseguita l'attività): applicazioni Win32, applicazioni Win16, applicazioni OS/2, applicazioni MS-DOS, file batch ( \* . bat), file di comando ( \* cmd) o qualsiasi tipo di file registrato correttamente.</span><span class="sxs-lookup"><span data-stu-id="c73b0-149">These may include any of the following (as supported by the operating system on which the task will execute): Win32 applications, Win16 applications, OS/2 applications, MS-DOS applications, batch files (\*.bat), command files (\*.cmd), or any properly registered file type.</span></span>

<span data-ttu-id="c73b0-150">I dati che descrivono un'attività vengono conservati in un file di attività archiviato nella cartella delle attività pianificate.</span><span class="sxs-lookup"><span data-stu-id="c73b0-150">Data that describes a task is kept in a task file that is stored in the Scheduled Tasks folder.</span></span> <span data-ttu-id="c73b0-151">Per ulteriori informazioni, vedere [*cartella attività pianificate*](s.md).</span><span class="sxs-lookup"><span data-stu-id="c73b0-151">For more information, see [*Scheduled Tasks folder*](s.md).</span></span> <span data-ttu-id="c73b0-152">Il nome di questi file delle attività include il nome dell'attività, seguito da un'estensione del nome di file. job.</span><span class="sxs-lookup"><span data-stu-id="c73b0-152">The name of these task files include the name of the task, followed by a .job file name extension.</span></span>

<span data-ttu-id="c73b0-153">Per ulteriori informazioni sull'aggiunta di Utilità di pianificazione attività 1,0, vedere [aggiunta di elementi di lavoro](adding-work-items.md).</span><span class="sxs-lookup"><span data-stu-id="c73b0-153">For more information about adding Task Scheduler 1.0 tasks, see [Adding Work Items](adding-work-items.md).</span></span>

<span data-ttu-id="c73b0-154">Per ulteriori informazioni sull'enumerazione tramite Utilità di pianificazione attività 1,0, vedere [enumerazione delle attività](enumerating-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="c73b0-154">For more information about enumerating through Task Scheduler 1.0 tasks, see [Enumerating Tasks](enumerating-tasks.md).</span></span>

<span data-ttu-id="c73b0-155">Per un computer Windows Server 2003, Windows XP o Windows 2000 per creare, monitorare o controllare le attività in un computer con Windows Vista, è necessario completare le operazioni seguenti nel computer con Windows Vista e l'utente che chiama il metodo [**ITaskScheduler:: SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) deve essere un membro del gruppo Administrators nel computer Windows Vista remoto.</span><span class="sxs-lookup"><span data-stu-id="c73b0-155">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, the following operations should be completed on the Windows Vista computer, and the user who is calling the [**ITaskScheduler::SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) method must be a member of the Administrators group on the remote Windows Vista computer.</span></span>

<span data-ttu-id="c73b0-156">**Per abilitare l'eccezione "condivisione di file e stampanti" in Windows Firewall**</span><span class="sxs-lookup"><span data-stu-id="c73b0-156">**To enable the "Share File and Printers" exception in Windows Firewall**</span></span>

1.  <span data-ttu-id="c73b0-157">Fare clic sul pulsante **Start** e quindi scegliere **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="c73b0-157">Click **Start**, and then click **Control Panel**.</span></span>
2.  <span data-ttu-id="c73b0-158">Nel **Pannello di controllo** fare clic su **visualizzazione classica** , quindi fare doppio clic sull'icona **Windows Firewall** .</span><span class="sxs-lookup"><span data-stu-id="c73b0-158">In **Control Panel**, click **Classic View** and then double-click the **Windows Firewall** icon.</span></span>
3.  <span data-ttu-id="c73b0-159">Nella finestra **Windows Firewall** fare clic sulla scheda **eccezioni** , quindi selezionare la casella di controllo eccezioni **condivisione file e stampanti** .</span><span class="sxs-lookup"><span data-stu-id="c73b0-159">In the **Windows Firewall** window, click the **Exceptions** tab and select **File and Printer Sharing exception** check box.</span></span>

<span data-ttu-id="c73b0-160">**Per abilitare il servizio "Registro di sistema remoto"**</span><span class="sxs-lookup"><span data-stu-id="c73b0-160">**To enable the "Remote Registry" service**</span></span>

-   <span data-ttu-id="c73b0-161">Aprire una finestra del prompt dei comandi e immettere il comando seguente: **net start "Remote Registry"**.</span><span class="sxs-lookup"><span data-stu-id="c73b0-161">Open a Command Prompt window and enter the following command: **net start "Remote Registry"**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c73b0-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c73b0-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c73b0-163">Informazioni sul Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c73b0-163">About the Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="c73b0-164">Trigger attività</span><span class="sxs-lookup"><span data-stu-id="c73b0-164">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="c73b0-165">Azioni attività</span><span class="sxs-lookup"><span data-stu-id="c73b0-165">Task Actions</span></span>](task-actions.md)
</dt> <dt>

[<span data-ttu-id="c73b0-166">**ITaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="c73b0-166">**ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[<span data-ttu-id="c73b0-167">**TaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="c73b0-167">**TaskDefinition**</span></span>](taskdefinition.md)
</dt> <dt>

[<span data-ttu-id="c73b0-168">**ITaskService**</span><span class="sxs-lookup"><span data-stu-id="c73b0-168">**ITaskService**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[<span data-ttu-id="c73b0-169">**TaskService**</span><span class="sxs-lookup"><span data-stu-id="c73b0-169">**TaskService**</span></span>](taskservice.md)
</dt> </dl>

 

 




