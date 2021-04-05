---
title: Esempio di trigger di avvio (scripting)
description: Questo esempio di scripting Mostra come creare un'attività pianificata per l'esecuzione del blocco note al momento dell'avvio del sistema.
ms.assetid: 73ae9cc4-ef89-4390-ac05-8a773f45fa46
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72b7735c607dfc39b848532a70e4d24b1a14d346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044727"
---
# <a name="boot-trigger-example-scripting"></a><span data-ttu-id="91ade-103">Esempio di trigger di avvio (scripting)</span><span class="sxs-lookup"><span data-stu-id="91ade-103">Boot Trigger Example (Scripting)</span></span>

<span data-ttu-id="91ade-104">Questo esempio di scripting Mostra come creare un'attività pianificata per l'esecuzione del blocco note al momento dell'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="91ade-104">This scripting example shows how to create a task that is scheduled to execute Notepad when the system is booted.</span></span> <span data-ttu-id="91ade-105">L'attività contiene un trigger di avvio che specifica un limite iniziale e un tempo di ritardo per l'avvio dell'attività dopo l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="91ade-105">The task contains a boot trigger that specifies a start boundary and delay time for the task to start after the system is booted.</span></span> <span data-ttu-id="91ade-106">L'attività contiene anche un'azione che specifica l'attività per l'esecuzione del blocco note.</span><span class="sxs-lookup"><span data-stu-id="91ade-106">The task also contains an action that specifies the task to execute Notepad.</span></span> <span data-ttu-id="91ade-107">L'attività viene registrata utilizzando l'account del servizio locale come contesto di sicurezza per l'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="91ade-107">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="91ade-108">Nella procedura riportata di seguito viene descritto come pianificare un eseguibile, ad esempio Blocco note, da avviare al momento dell'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="91ade-108">The following procedure describes how to schedule an executable such as Notepad to start when the system is booted.</span></span>

<span data-ttu-id="91ade-109">**Per pianificare l'avvio del blocco note al momento dell'avvio del sistema**</span><span class="sxs-lookup"><span data-stu-id="91ade-109">**To schedule Notepad to start when the system is booted**</span></span>

1.  <span data-ttu-id="91ade-110">Creare un oggetto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="91ade-110">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="91ade-111">Questo oggetto consente di creare l'attività in una cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="91ade-111">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="91ade-112">Ottenere una cartella attività e creare un'attività.</span><span class="sxs-lookup"><span data-stu-id="91ade-112">Get a task folder and create a task.</span></span> <span data-ttu-id="91ade-113">Usare il metodo [**TaskService. GetFolder**](taskservice-getfolder.md) per ottenere la cartella in cui è archiviata l'attività e il metodo [**TaskService. newTask**](taskservice-newtask.md) per creare l'oggetto [**TaskDefinition**](taskdefinition.md) che rappresenta l'attività.</span><span class="sxs-lookup"><span data-stu-id="91ade-113">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="91ade-114">Definire le informazioni sull'attività usando l'oggetto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="91ade-114">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="91ade-115">Utilizzare la proprietà [**TaskDefinition. Settings**](taskdefinition-settings.md) per definire le impostazioni che determinano il modo in cui il servizio Utilità di pianificazione esegue l'attività e la proprietà [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) per definire le informazioni che descrivono l'attività.</span><span class="sxs-lookup"><span data-stu-id="91ade-115">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="91ade-116">Creare un trigger LOGON usando la proprietà [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="91ade-116">Create a logon trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="91ade-117">Questa proprietà fornisce l'accesso all'oggetto [**TriggerCollection**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="91ade-117">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="91ade-118">Usare il metodo [**TriggerCollection. Create**](triggercollection-create.md) (specificando il tipo di trigger che si vuole creare) per creare un trigger di avvio.</span><span class="sxs-lookup"><span data-stu-id="91ade-118">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a boot trigger.</span></span> <span data-ttu-id="91ade-119">Quando si crea il trigger, impostare le proprietà [**StartBoundary**](trigger-startboundary.md) e [**EndBoundary**](trigger-endboundary.md) del trigger per attivare e disattivare il trigger.</span><span class="sxs-lookup"><span data-stu-id="91ade-119">As you create the trigger, set the [**StartBoundary**](trigger-startboundary.md) and [**EndBoundary**](trigger-endboundary.md) properties of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="91ade-120">È anche possibile specificare un valore per la proprietà [**delay**](boottrigger-delay.md) del trigger di avvio.</span><span class="sxs-lookup"><span data-stu-id="91ade-120">You can also specify a value for the [**Delay**](boottrigger-delay.md) property of the boot trigger.</span></span>
5.  <span data-ttu-id="91ade-121">Creare un'azione per l'attività da eseguire usando la proprietà [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="91ade-121">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="91ade-122">Questa proprietà consente di accedere all'oggetto [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="91ade-122">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="91ade-123">Utilizzare il metodo [**ActionCollection. Create**](actioncollection-create.md) per specificare il tipo di azione che si desidera creare.</span><span class="sxs-lookup"><span data-stu-id="91ade-123">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="91ade-124">Questo esempio usa un oggetto [**ExecAction**](execaction.md) , che rappresenta un'azione che avvia un eseguibile.</span><span class="sxs-lookup"><span data-stu-id="91ade-124">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="91ade-125">Registrare l'attività usando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="91ade-125">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="91ade-126">L'attività viene registrata utilizzando l'account del servizio locale come contesto di sicurezza per l'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="91ade-126">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="91ade-127">Nell'esempio VBScript seguente viene illustrato come pianificare un'attività per eseguire il blocco note 30 secondi dopo l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="91ade-127">The following VBScript example shows how to schedule a task to execute Notepad 30 seconds after the system is booted.</span></span>


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe 30 seconds after
' the system is booted.
'---------------------------------------------------------

' A constant that specifies a boot trigger.
const TriggerTypeBoot = 8
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
regInfo.Description = "Task will execute Notepad when " & _
    "the computer is booted."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a boot trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeBoot)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "BootTriggerId"
trigger.Delay = "PT30S"                ' 30 Seconds   

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
    "Test Boot Trigger", taskDefinition, createOrUpdateTask, _
    "Local Service", , 5)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a><span data-ttu-id="91ade-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91ade-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91ade-129">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="91ade-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




