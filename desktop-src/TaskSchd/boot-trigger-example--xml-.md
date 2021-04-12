---
title: Esempio di trigger di avvio (XML)
description: Il codice XML in questo esempio definisce un'attività che avvia il blocco note quando il sistema viene avviato.
ms.assetid: 6dd7155c-6163-4408-9cef-c313134beeb0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8f9f5ea10f92979b0798b12a6225f8ba74a38ee
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/24/2020
ms.locfileid: "104336037"
---
# <a name="boot-trigger-example-xml"></a><span data-ttu-id="fe990-103">Esempio di trigger di avvio (XML)</span><span class="sxs-lookup"><span data-stu-id="fe990-103">Boot Trigger Example (XML)</span></span>

<span data-ttu-id="fe990-104">Il codice XML in questo esempio definisce un'attività che avvia il blocco note quando il sistema viene avviato.</span><span class="sxs-lookup"><span data-stu-id="fe990-104">The XML in this example defines a task that starts Notepad when the system is booted.</span></span>

<span data-ttu-id="fe990-105">Per registrare un'attività definita in XML, è possibile usare la funzione [**ITaskFolder:: l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) per gli script) o lo strumento da riga di comando Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="fe990-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="fe990-106">Se si usa lo strumento Schtasks.exe (che si trova nella directory C: \\ Windows \\ System32), è possibile usare il comando seguente per registrare l'attività: **schtasks/create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="fe990-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a><span data-ttu-id="fe990-107">Per definire un'attività per avviare il blocco note all'avvio del sistema</span><span class="sxs-lookup"><span data-stu-id="fe990-107">To define a task to start Notepad on system boot</span></span>

<span data-ttu-id="fe990-108">Nell'esempio XML seguente viene illustrato come definire un'attività con un'unica azione di esecuzione (avvio del blocco note), un singolo trigger di avvio che avvia l'attività quando viene avviato il sistema e diverse altre impostazioni di attività che influiscono sulla modalità di gestione dell'attività da parte del Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="fe990-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single boot trigger that starts the task when the system is booted, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the system is booted.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad on system boot.</Description>
    </RegistrationInfo>
    <Triggers>
        <BootTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </BootTrigger>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="fe990-109">Elementi dello schema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="fe990-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="fe990-110">Di seguito sono riportati alcuni elementi importanti da tenere presenti quando si usa questo esempio.</span><span class="sxs-lookup"><span data-stu-id="fe990-110">Here are some important elements to keep in mind when using this example.</span></span>

-   <span data-ttu-id="fe990-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contiene le informazioni di registrazione relative all'attività.</span><span class="sxs-lookup"><span data-stu-id="fe990-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="fe990-112">[**Trigger**](taskschedulerschema-triggers-tasktype-element.md): definisce il trigger che avvia l'attività.</span><span class="sxs-lookup"><span data-stu-id="fe990-112">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="fe990-113">[**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): definisce il trigger di avvio.</span><span class="sxs-lookup"><span data-stu-id="fe990-113">[**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): Defines the boot trigger.</span></span> <span data-ttu-id="fe990-114">In questo caso vengono utilizzati solo due elementi figlio: i limiti di inizio e di fine che specificano quando il trigger viene attivato e disattivato.</span><span class="sxs-lookup"><span data-stu-id="fe990-114">In this case only two child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated.</span></span>
-   <span data-ttu-id="fe990-115">[**Principal**](taskschedulerschema-principal-principaltype-element.md): definisce il contesto di sicurezza in cui viene eseguita un'attività.</span><span class="sxs-lookup"><span data-stu-id="fe990-115">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="fe990-116">[**Impostazioni**](taskschedulerschema-settings-tasktype-element.md): definisce le impostazioni dell'attività utilizzate dal utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="fe990-116">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="fe990-117">[**Actions**](taskschedulerschema-actions-tasktype-element.md): definisce le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="fe990-117">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="fe990-118">In questo caso, viene eseguito il blocco note.</span><span class="sxs-lookup"><span data-stu-id="fe990-118">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe990-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe990-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe990-120">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="fe990-120">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




