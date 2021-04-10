---
title: Esempio di trigger di registrazione (scripting)
description: Questo esempio di scripting Mostra come creare un'attività pianificata per l'esecuzione del blocco note quando un'attività viene registrata.
ms.assetid: 956b3a21-7d36-4d06-be84-690884ba653a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bce6271927e74e31f25b3ac86783b35899bbd862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332519"
---
# <a name="registration-trigger-example-scripting"></a><span data-ttu-id="62b2f-103">Esempio di trigger di registrazione (scripting)</span><span class="sxs-lookup"><span data-stu-id="62b2f-103">Registration Trigger Example (Scripting)</span></span>

<span data-ttu-id="62b2f-104">Questo esempio di scripting Mostra come creare un'attività pianificata per l'esecuzione del blocco note quando un'attività viene registrata.</span><span class="sxs-lookup"><span data-stu-id="62b2f-104">This scripting example shows how to create a task that is scheduled to execute Notepad when a task is registered.</span></span> <span data-ttu-id="62b2f-105">L'attività contiene un trigger di registrazione che specifica un limite iniziale e un limite finale per l'attività.</span><span class="sxs-lookup"><span data-stu-id="62b2f-105">The task contains a registration trigger that specifies a start boundary and an end boundary for the task.</span></span> <span data-ttu-id="62b2f-106">Il limite iniziale specifica quando viene attivato il trigger.</span><span class="sxs-lookup"><span data-stu-id="62b2f-106">The start boundary specifies when the trigger is activated.</span></span> <span data-ttu-id="62b2f-107">L'attività contiene anche un'azione che specifica l'attività per l'esecuzione del blocco note.</span><span class="sxs-lookup"><span data-stu-id="62b2f-107">The task also contains an action that specifies the task to execute Notepad.</span></span>

> [!Note]  
> <span data-ttu-id="62b2f-108">Quando si aggiorna un'attività con un trigger di registrazione, l'attività verrà eseguita dopo l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="62b2f-108">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

<span data-ttu-id="62b2f-109">Nella procedura riportata di seguito viene descritto come pianificare un eseguibile, ad esempio Blocco note, da avviare quando viene registrata un'attività.</span><span class="sxs-lookup"><span data-stu-id="62b2f-109">The following procedure describes how to schedule an executable such as Notepad to start when a task is registered.</span></span>

<span data-ttu-id="62b2f-110">**Per pianificare l'avvio del blocco note quando viene registrata un'attività**</span><span class="sxs-lookup"><span data-stu-id="62b2f-110">**To schedule Notepad to start when a task is registered**</span></span>

1.  <span data-ttu-id="62b2f-111">Creare un oggetto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="62b2f-111">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="62b2f-112">Questo oggetto consente di creare l'attività in una cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="62b2f-112">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="62b2f-113">Ottenere una cartella attività e creare un'attività.</span><span class="sxs-lookup"><span data-stu-id="62b2f-113">Get a task folder and create a task.</span></span> <span data-ttu-id="62b2f-114">Usare il metodo [**TaskService. GetFolder**](taskservice-getfolder.md) per ottenere la cartella in cui è archiviata l'attività e il metodo [**TaskService. newTask**](taskservice-newtask.md) per creare l'oggetto [**TaskDefinition**](taskdefinition.md) che rappresenta l'attività.</span><span class="sxs-lookup"><span data-stu-id="62b2f-114">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="62b2f-115">Definire le informazioni sull'attività usando l'oggetto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="62b2f-115">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="62b2f-116">Utilizzare la proprietà [**TaskDefinition. Settings**](taskdefinition-settings.md) per definire le impostazioni che determinano il modo in cui il servizio Utilità di pianificazione esegue l'attività e la proprietà [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) per definire le informazioni che descrivono l'attività.</span><span class="sxs-lookup"><span data-stu-id="62b2f-116">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="62b2f-117">Creare un trigger di registrazione usando la proprietà [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="62b2f-117">Create a registration trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="62b2f-118">Questa proprietà fornisce l'accesso all'oggetto [**TriggerCollection**](triggercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="62b2f-118">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="62b2f-119">Usare il metodo [**TriggerCollection. Create**](triggercollection-create.md) (specificando il tipo di trigger che si vuole creare) per creare un trigger di registrazione.</span><span class="sxs-lookup"><span data-stu-id="62b2f-119">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a registration trigger.</span></span>
5.  <span data-ttu-id="62b2f-120">Creare un'azione per l'attività da eseguire usando la proprietà [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="62b2f-120">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="62b2f-121">Questa proprietà consente di accedere all'oggetto [**ActionCollection**](actioncollection.md) .</span><span class="sxs-lookup"><span data-stu-id="62b2f-121">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="62b2f-122">Utilizzare il metodo [**ActionCollection. Create**](actioncollection-create.md) per specificare il tipo di azione che si desidera creare.</span><span class="sxs-lookup"><span data-stu-id="62b2f-122">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="62b2f-123">Questo esempio usa un oggetto [**ExecAction**](execaction.md) , che rappresenta un'azione che avvia un eseguibile.</span><span class="sxs-lookup"><span data-stu-id="62b2f-123">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="62b2f-124">Registrare l'attività usando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="62b2f-124">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span>

<span data-ttu-id="62b2f-125">Nell'esempio VBScript seguente viene illustrato come creare un'attività per la pianificazione del blocco note da eseguire quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="62b2f-125">The following VBScript example shows how to create a task that schedules Notepad to execute when the task is registered.</span></span>


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when
' the task is registered.
'---------------------------------------------------------

' A constant that specifies a registration trigger.
const TriggerTypeRegistration = 7
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
regInfo.Description = "Start Notepad when the task is registered."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a registration trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeRegistration)

trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "RegistrationTriggerId"   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes Notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test Registration Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a><span data-ttu-id="62b2f-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62b2f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62b2f-127">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="62b2f-127">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




