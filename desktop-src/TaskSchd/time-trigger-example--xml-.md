---
title: Esempio di trigger time (XML)
description: Il codice XML in questo esempio definisce un'attività che avvia il blocco note a un momento specifico.
ms.assetid: dde3627b-e268-45ef-9c26-08877bfe484f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c683c831aa3a07eeb3a41db9cd2768caeb6307a
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/24/2020
ms.locfileid: "104336026"
---
# <a name="time-trigger-example-xml"></a><span data-ttu-id="8e7a8-103">Esempio di trigger time (XML)</span><span class="sxs-lookup"><span data-stu-id="8e7a8-103">Time Trigger Example (XML)</span></span>

<span data-ttu-id="8e7a8-104">Il codice XML in questo esempio definisce un'attività che avvia il blocco note a un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="8e7a8-104">The XML in this example defines a task that starts Notepad at a specific time.</span></span>

<span data-ttu-id="8e7a8-105">Per registrare un'attività definita in XML, è possibile usare la funzione [**ITaskFolder:: l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) per gli script) o lo strumento da riga di comando Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8e7a8-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="8e7a8-106">Se si usa lo strumento Schtasks.exe (che si trova nella directory C: \\ Windows \\ System32), è possibile usare il comando seguente per registrare l'attività: **schtasks/create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="8e7a8-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-at-a-specific-time"></a><span data-ttu-id="8e7a8-107">Per definire un'attività per avviare il blocco note a un'ora specifica</span><span class="sxs-lookup"><span data-stu-id="8e7a8-107">To define a task to start Notepad at a specific time</span></span>

<span data-ttu-id="8e7a8-108">Nell'esempio XML seguente viene illustrato come definire un'attività con un'unica azione di esecuzione (avvio del blocco note), un singolo trigger di ora che avvia l'attività a un'ora specificata e diverse altre impostazioni di attività che influiscono sulla modalità di gestione dell'attività da parte del Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="8e7a8-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single time trigger that starts the task at a specified time, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe at a specific time.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after at a specified time.</Description>
    </RegistrationInfo>
    <Triggers>
        <TimeTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </TimeTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="8e7a8-109">Elementi dello schema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="8e7a8-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="8e7a8-110">Di seguito sono riportati alcuni elementi importanti da tenere presenti quando si utilizza questo esempio:</span><span class="sxs-lookup"><span data-stu-id="8e7a8-110">The following are some important elements to keep in mind when using this example:</span></span>

-   <span data-ttu-id="8e7a8-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contiene le informazioni di registrazione relative all'attività.</span><span class="sxs-lookup"><span data-stu-id="8e7a8-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="8e7a8-112">[**Trigger**](taskschedulerschema-triggers-tasktype-element.md): definisce il trigger che avvia l'attività.</span><span class="sxs-lookup"><span data-stu-id="8e7a8-112">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="8e7a8-113">[**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md): definisce il trigger di ora.</span><span class="sxs-lookup"><span data-stu-id="8e7a8-113">[**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md): Defines the time trigger.</span></span> <span data-ttu-id="8e7a8-114">In questo caso, vengono utilizzati tre elementi figlio: i limiti di inizio e di fine che specificano quando il trigger viene attivato e disattivato e il limite di tempo di esecuzione che specifica la quantità massima di tempo in cui l'attività può essere avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="8e7a8-114">In this case, three child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, and the execution time limit that specifies the maximum amount of time in which the task can be started by the trigger.</span></span> <span data-ttu-id="8e7a8-115">L'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) è un elemento obbligatorio per i trigger temporali.</span><span class="sxs-lookup"><span data-stu-id="8e7a8-115">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time triggers.</span></span>
-   <span data-ttu-id="8e7a8-116">[**Principal**](taskschedulerschema-principal-principaltype-element.md): definisce il contesto di sicurezza in cui viene eseguita un'attività.</span><span class="sxs-lookup"><span data-stu-id="8e7a8-116">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="8e7a8-117">[**Impostazioni**](taskschedulerschema-settings-tasktype-element.md): definisce le impostazioni dell'attività utilizzate dal utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="8e7a8-117">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="8e7a8-118">[**Actions**](taskschedulerschema-actions-tasktype-element.md): definisce le azioni eseguite dall'attività, in questo caso l'esecuzione del blocco note.</span><span class="sxs-lookup"><span data-stu-id="8e7a8-118">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions that the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e7a8-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8e7a8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e7a8-120">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="8e7a8-120">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




