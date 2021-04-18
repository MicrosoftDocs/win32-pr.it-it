---
title: Esempio di trigger di registrazione (XML)
description: Il codice XML in questo esempio definisce un'attività che avvia il blocco note quando l'attività è registrata.
ms.assetid: 976b9767-635f-42a6-84f5-7e0203478594
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09b9193f3b63f21464811609e8f5f19017539ecd
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/24/2020
ms.locfileid: "106299333"
---
# <a name="registration-trigger-example-xml"></a><span data-ttu-id="46a38-103">Esempio di trigger di registrazione (XML)</span><span class="sxs-lookup"><span data-stu-id="46a38-103">Registration Trigger Example (XML)</span></span>

<span data-ttu-id="46a38-104">Il codice XML in questo esempio definisce un'attività che avvia il blocco note quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="46a38-104">The XML in this example defines a task that starts Notepad when the task is registered.</span></span>

<span data-ttu-id="46a38-105">Per registrare un'attività definita in XML, è possibile usare la funzione [**ITaskFolder:: l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) per gli script) o lo strumento da riga di comando Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="46a38-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="46a38-106">Se si usa lo strumento Schtasks.exe (che si trova nella directory C: \\ Windows \\ System32), è possibile usare il comando seguente per registrare l'attività: **schtasks/create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="46a38-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

> [!Note]  
> <span data-ttu-id="46a38-107">Quando si aggiorna un'attività con un trigger di registrazione, l'attività verrà eseguita dopo l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="46a38-107">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

## <a name="to-define-a-task-to-start-notepad-on-registration"></a><span data-ttu-id="46a38-108">Per definire un'attività per avviare il blocco note alla registrazione</span><span class="sxs-lookup"><span data-stu-id="46a38-108">To define a task to start Notepad on registration</span></span>

<span data-ttu-id="46a38-109">Nell'esempio di codice XML riportato di seguito viene illustrato come definire un'attività con un'unica azione di esecuzione (avvio del blocco note), un singolo trigger di registrazione che avvia l'attività quando viene registrata e diverse altre impostazioni di attività che influiscono sul modo in cui l'attività viene gestita dal Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="46a38-109">The following XML example shows how to define a task with a single execution action (starting Notepad), a single registration trigger that starts the task when it is registered, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>

> [!Note]  
> <span data-ttu-id="46a38-110">Quando si aggiorna un'attività con un trigger di registrazione, l'attività verrà eseguita dopo l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="46a38-110">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the task is registered.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after registration.</Description>
    </RegistrationInfo>
    <Triggers>
        <RegistrationTrigger>
        </RegistrationTrigger>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="46a38-111">Elementi dello schema TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="46a38-111">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="46a38-112">Di seguito sono riportati alcuni elementi importanti da tenere presenti quando si usa questo esempio.</span><span class="sxs-lookup"><span data-stu-id="46a38-112">Here are some important elements to keep in mind when using this example.</span></span>

-   <span data-ttu-id="46a38-113">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contiene le informazioni di registrazione relative all'attività.</span><span class="sxs-lookup"><span data-stu-id="46a38-113">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="46a38-114">[**Trigger**](taskschedulerschema-triggers-tasktype-element.md): definisce il trigger che avvia l'attività.</span><span class="sxs-lookup"><span data-stu-id="46a38-114">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="46a38-115">[**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md): definisce il trigger di registrazione.</span><span class="sxs-lookup"><span data-stu-id="46a38-115">[**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md): Defines the registration trigger.</span></span> <span data-ttu-id="46a38-116">In questo caso vengono utilizzati solo due elementi figlio: i limiti di inizio e di fine che specificano quando il trigger viene attivato e disattivato.</span><span class="sxs-lookup"><span data-stu-id="46a38-116">In this case, only two child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated.</span></span>
-   <span data-ttu-id="46a38-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): definisce il contesto di sicurezza in cui viene eseguita un'attività.</span><span class="sxs-lookup"><span data-stu-id="46a38-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="46a38-118">[**Impostazioni**](taskschedulerschema-settings-tasktype-element.md): definisce le impostazioni dell'attività utilizzate dal utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="46a38-118">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="46a38-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): definisce le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="46a38-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="46a38-120">In questo caso, viene eseguito il blocco note.</span><span class="sxs-lookup"><span data-stu-id="46a38-120">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46a38-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46a38-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46a38-122">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="46a38-122">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




