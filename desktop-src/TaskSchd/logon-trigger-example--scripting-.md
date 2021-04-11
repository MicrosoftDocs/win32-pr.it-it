---
title: Esempio di trigger LOGON (scripting)
description: Questo esempio di scripting Mostra come creare un'attività pianificata per l'esecuzione del blocco note quando un utente esegue l'accesso.
ms.assetid: f25e105f-9439-4646-bdfd-609ee99a5d55
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72a8c4b5d0d67b59160eb3ed0b13885ee7e0eb51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221206"
---
# <a name="logon-trigger-example-scripting"></a><span data-ttu-id="0da5d-103">Esempio di trigger LOGON (scripting)</span><span class="sxs-lookup"><span data-stu-id="0da5d-103">Logon Trigger Example (Scripting)</span></span>

<span data-ttu-id="0da5d-104">Questo esempio di scripting Mostra come creare un'attività pianificata per l'esecuzione del blocco note quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="0da5d-104">This scripting example shows how to create a task that is scheduled to execute Notepad when a user logs on.</span></span> <span data-ttu-id="0da5d-105">L'attività contiene un trigger LOGON che specifica un limite iniziale per l'avvio dell'attività e un identificatore utente che specifica l'utente.</span><span class="sxs-lookup"><span data-stu-id="0da5d-105">The task contains a logon trigger that specifies a start boundary for the task to start and a user identifier that specifies the user.</span></span> <span data-ttu-id="0da5d-106">L'attività viene registrata utilizzando il gruppo Administrators come contesto di sicurezza per l'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0da5d-106">The task is registered using the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="0da5d-107">Nella procedura riportata di seguito viene descritto come pianificare un eseguibile, ad esempio Blocco note, da avviare quando un utente specificato esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="0da5d-107">The following procedure describes how to schedule an executable such as Notepad to start when a specified user logs on.</span></span>

<span data-ttu-id="0da5d-108">**Per pianificare l'avvio del blocco note quando un utente esegue l'accesso**</span><span class="sxs-lookup"><span data-stu-id="0da5d-108">**To schedule Notepad to start when a user logs on**</span></span>

1.  <span data-ttu-id="0da5d-109">Creare un oggetto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0da5d-109">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="0da5d-110">Questo oggetto consente di creare l'attività in una cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="0da5d-110">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="0da5d-111">Ottenere una cartella attività e creare un'attività.</span><span class="sxs-lookup"><span data-stu-id="0da5d-111">Get a task folder and create a task.</span></span> <span data-ttu-id="0da5d-112">Usare il metodo [**TaskService. GetFolder**](taskservice-getfolder.md) per ottenere la cartella in cui è archiviata l'attività e il metodo [**TaskService. newTask**](taskservice-newtask.md) per creare l'oggetto [**TaskDefinition**](taskdefinition.md) che rappresenta l'attività.</span><span class="sxs-lookup"><span data-stu-id="0da5d-112">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="0da5d-113">Definire le informazioni sull'attività usando l'oggetto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="0da5d-113">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="0da5d-114">Utilizzare la proprietà [**TaskDefinition. Settings**](taskdefinition-settings.md) per definire le impostazioni che determinano il modo in cui il servizio Utilità di pianificazione esegue l'attività e la proprietà [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) per definire le informazioni che descrivono l'attività.</span><span class="sxs-lookup"><span data-stu-id="0da5d-114">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="0da5d-115">Creare un trigger LOGON usando la proprietà [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="0da5d-115">Create a logon trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="0da5d-116">Questa proprietà fornisce l'accesso all'oggetto [**TriggerCollection**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="0da5d-116">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="0da5d-117">Usare il metodo [**TriggerCollection. Create**](triggercollection-create.md) (specificando il tipo di trigger che si vuole creare) per creare un trigger LOGON.</span><span class="sxs-lookup"><span data-stu-id="0da5d-117">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a logon trigger.</span></span> <span data-ttu-id="0da5d-118">Quando si crea il trigger, impostare i limiti iniziale e finale del trigger per attivare e disattivare il trigger.</span><span class="sxs-lookup"><span data-stu-id="0da5d-118">As you create the trigger, set the start boundary and end boundary of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="0da5d-119">È necessario impostare la proprietà [**userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) per il trigger in modo che le azioni dell'attività vengano pianificate per l'esecuzione quando l'utente specificato si connette dopo il limite iniziale.</span><span class="sxs-lookup"><span data-stu-id="0da5d-119">You must set the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property for the trigger so that the task's actions will be scheduled to execute when the specified user logs on after the start boundary.</span></span>
5.  <span data-ttu-id="0da5d-120">Creare un'azione per l'attività da eseguire usando la proprietà [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="0da5d-120">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="0da5d-121">Questa proprietà consente di accedere all'oggetto [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="0da5d-121">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="0da5d-122">Utilizzare il metodo [**ActionCollection. Create**](actioncollection-create.md) per specificare il tipo di azione che si desidera creare.</span><span class="sxs-lookup"><span data-stu-id="0da5d-122">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="0da5d-123">Questo esempio usa un oggetto [**ExecAction**](execaction.md) , che rappresenta un'azione che avvia un eseguibile.</span><span class="sxs-lookup"><span data-stu-id="0da5d-123">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="0da5d-124">Registrare l'attività usando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="0da5d-124">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="0da5d-125">In questo esempio viene registrata l'attività in modo da utilizzare il gruppo Administrators come contesto di sicurezza per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="0da5d-125">This example registers the task so that it uses the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="0da5d-126">Nell'esempio VBScript seguente viene illustrato come pianificare un'attività per eseguire il blocco note quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="0da5d-126">The following VBScript example shows how to schedule a task to execute Notepad when a user logs on.</span></span>


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when a user logs on.
'---------------------------------------------------------

' A constant that specifies a logon trigger.
const TriggerTypeLogon = 9
' A constant that specifies an executable action.
const ActionTypeExecutable = 0   

'********************************************************
' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

'********************************************************
' Get a folder to create a task definition in. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")

' The taskDefinition variable is the TaskDefinition object.
Dim taskDefinition
' The flags parameter is 0 because it is not supported.
Set taskDefinition = service.NewTask(0) 

'********************************************************
' Define information about the task.

' Set the registration info for the task by 
' creating the RegistrationInfo object.
Dim regInfo
Set regInfo = taskDefinition.RegistrationInfo
regInfo.Description = "Task will execute Notepad when a " & _
    "specified user logs on."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a logon trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeLogon)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "LogonTriggerId"
trigger.UserId = "DOMAIN\UserName"   ' Must be a valid user account   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.
const createOrUpdateTask = 6
call rootFolder.RegisterTaskDefinition( _
    "Test Logon Trigger", taskDefinition, createOrUpdateTask, _
    "Builtin\Administrators", , 4)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a><span data-ttu-id="0da5d-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0da5d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0da5d-128">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0da5d-128">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




