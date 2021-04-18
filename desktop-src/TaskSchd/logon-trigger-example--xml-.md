---
title: Esempio di trigger LOGON (XML)
description: Il codice XML in questo esempio definisce un'attività che avvia il blocco note quando un utente esegue l'accesso.
ms.assetid: c1cce95f-7558-489e-b092-c82d55b42165
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d66766ce4cae33c3526ac9d30071ff2082ddc1f2
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/24/2020
ms.locfileid: "104398441"
---
# <a name="logon-trigger-example-xml"></a><span data-ttu-id="171fa-103">Esempio di trigger LOGON (XML)</span><span class="sxs-lookup"><span data-stu-id="171fa-103">Logon Trigger Example (XML)</span></span>

<span data-ttu-id="171fa-104">Il codice XML in questo esempio definisce un'attività che avvia il blocco note quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="171fa-104">The XML in this example defines a task that starts Notepad when a user logs on.</span></span>

<span data-ttu-id="171fa-105">Per registrare un'attività definita in XML, è possibile usare la funzione [**ITaskFolder:: l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) per gli script) o lo strumento da riga di comando Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="171fa-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="171fa-106">Se si usa lo strumento Schtasks.exe (che si trova nella directory C: \\ Windows \\ System32), è possibile usare il comando seguente per registrare l'attività: **schtasks/create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="171fa-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a><span data-ttu-id="171fa-107">Per definire un'attività per avviare il blocco note all'avvio del sistema</span><span class="sxs-lookup"><span data-stu-id="171fa-107">To define a task to start Notepad on system boot</span></span>

<span data-ttu-id="171fa-108">Nell'esempio XML seguente viene illustrato come definire un'attività con un'unica azione di esecuzione (avvio del blocco note), un singolo trigger LOGON che avvia l'attività quando un utente esegue l'accesso e diverse altre impostazioni di attività che influiscono sul modo in cui l'attività viene gestita da Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="171fa-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single logon trigger that starts the task when a user logs on, and several other task settings that affect how the task is handled by Task Scheduler.</span></span>

> [!Note]  
> <span data-ttu-id="171fa-109">Impostare il valore dell'elemento **userid** su un nome utente nel computer in cui è registrata l'attività.</span><span class="sxs-lookup"><span data-stu-id="171fa-109">Set the value of the **UserId** element to a user name on the computer on which the task is registered.</span></span>

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when a user logs on.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad when a specified user logs on.</Description>
    </RegistrationInfo>
    <Triggers>
        <LogonTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <UserId>DOMAIN_NAME\UserName</UserId>
        </LogonTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <GroupId>Builtin\Administrators</GroupId>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="171fa-110">Elementi dello schema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="171fa-110">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="171fa-111">Di seguito sono riportati alcuni elementi importanti da tenere presenti quando si utilizza questo esempio:</span><span class="sxs-lookup"><span data-stu-id="171fa-111">The following are some important elements to keep in mind when using this example:</span></span>

-   <span data-ttu-id="171fa-112">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contiene le informazioni di registrazione relative all'attività.</span><span class="sxs-lookup"><span data-stu-id="171fa-112">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="171fa-113">[**Trigger**](taskschedulerschema-triggers-tasktype-element.md): definisce il trigger che avvia l'attività.</span><span class="sxs-lookup"><span data-stu-id="171fa-113">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="171fa-114">[**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md): definisce il trigger LOGON.</span><span class="sxs-lookup"><span data-stu-id="171fa-114">[**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md): Defines the logon trigger.</span></span> <span data-ttu-id="171fa-115">In questo caso vengono usati tre elementi figlio: i limiti di inizio e di fine che specificano quando il trigger viene attivato e disattivato e l'elemento [**userid**](taskschedulerschema-userid-logontriggertype-element.md) che identifica l'utente.</span><span class="sxs-lookup"><span data-stu-id="171fa-115">In this case, three child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, and the [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) element that identifier of the user.</span></span> <span data-ttu-id="171fa-116">L'attività viene avviata quando l'utente accede al computer.</span><span class="sxs-lookup"><span data-stu-id="171fa-116">The task is started when this user logs on to the computer..</span></span>
-   <span data-ttu-id="171fa-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): definisce il contesto di sicurezza in cui viene eseguita un'attività.</span><span class="sxs-lookup"><span data-stu-id="171fa-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="171fa-118">[**Impostazioni**](taskschedulerschema-settings-tasktype-element.md): definisce le impostazioni dell'attività utilizzate dal utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="171fa-118">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="171fa-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): definisce le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="171fa-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="171fa-120">In questo caso, viene eseguito il blocco note.</span><span class="sxs-lookup"><span data-stu-id="171fa-120">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="171fa-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="171fa-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="171fa-122">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="171fa-122">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




