---
title: Esempio di trigger giornaliero (scripting)
description: Questo esempio di scripting Mostra come creare un'attività che esegue blocco note alle 8 00 AM ogni giorno.
ms.assetid: a13bd54d-b45a-46e5-8281-d080f50f6bef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3399934786e1cd0f95ca020c92027ccafafa5272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855962"
---
# <a name="daily-trigger-example-scripting"></a><span data-ttu-id="2f0f8-103">Esempio di trigger giornaliero (scripting)</span><span class="sxs-lookup"><span data-stu-id="2f0f8-103">Daily Trigger Example (Scripting)</span></span>

<span data-ttu-id="2f0f8-104">Questo esempio di scripting Mostra come creare un'attività che esegue blocco note alle 8:00 AM ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-104">This scripting example shows how to create a task that runs Notepad at 8:00 AM every day.</span></span> <span data-ttu-id="2f0f8-105">L'attività contiene un trigger giornaliero che specifica un limite iniziale per attivare il trigger e per specificare l'ora del giorno in cui viene eseguita l'attività, un intervallo di trigger per specificare che l'attività viene eseguita ogni giorno e un limite finale per disattivare il trigger.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-105">The task contains a daily trigger that specifies a start boundary to activate the trigger and to specify the time of day that the task runs, a trigger interval to specify that the task runs every day, and an end boundary to deactivates the trigger.</span></span> <span data-ttu-id="2f0f8-106">Nell'esempio viene inoltre illustrato come impostare un criterio di ripetizione per il trigger per ripetere l'attività.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-106">The example also shows how to set a repetition pattern for the trigger to repeat the task.</span></span> <span data-ttu-id="2f0f8-107">L'attività contiene anche un'azione eseguibile che esegue il blocco note.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-107">The task also contains an executable action that runs Notepad.</span></span>

<span data-ttu-id="2f0f8-108">Nella procedura seguente viene descritto come pianificare un'attività per l'avvio di un eseguibile alle 8:00 di ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-108">The following procedure describes how to schedule a task to start an executable at 8:00 AM every day.</span></span> <span data-ttu-id="2f0f8-109">(Questi passaggi corrispondono ai commenti del codice inclusi nel codice di esempio).</span><span class="sxs-lookup"><span data-stu-id="2f0f8-109">(These steps correspond to the code comments included in the example code.)</span></span>

<span data-ttu-id="2f0f8-110">**Per pianificare l'avvio del blocco note alle 8:00 di ogni giorno**</span><span class="sxs-lookup"><span data-stu-id="2f0f8-110">**To schedule Notepad to start at 8:00 AM every day**</span></span>

1.  <span data-ttu-id="2f0f8-111">Creare un oggetto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="2f0f8-111">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="2f0f8-112">Questo oggetto consente di creare l'attività in una cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-112">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="2f0f8-113">Ottenere una cartella attività e creare un'attività.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-113">Get a task folder and create a task.</span></span> <span data-ttu-id="2f0f8-114">Usare il metodo [**TaskService. GetFolder**](taskservice-getfolder.md) per ottenere la cartella in cui è archiviata l'attività e il metodo [**TaskService. newTask**](taskservice-newtask.md) per creare l'oggetto [**TaskDefinition**](taskdefinition.md) che rappresenta l'attività.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-114">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="2f0f8-115">Definire le informazioni sull'attività usando l'oggetto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="2f0f8-115">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="2f0f8-116">Utilizzare la proprietà [**TaskDefinition. Settings**](taskdefinition-settings.md) per definire le impostazioni che determinano il modo in cui il servizio Utilità di pianificazione esegue l'attività e la proprietà [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) per definire le informazioni che descrivono l'attività.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-116">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="2f0f8-117">Creare un trigger giornaliero usando la proprietà [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="2f0f8-117">Create a daily trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="2f0f8-118">Questa proprietà consente di accedere all'oggetto [**TriggerCollection**](triggercollection.md) utilizzato per creare il trigger.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-118">This property provides access to the [**TriggerCollection**](triggercollection.md) object that is used to create the trigger.</span></span> <span data-ttu-id="2f0f8-119">Usare il metodo [**TriggerCollection. Create**](triggercollection-create.md) (specificando il tipo di trigger che si vuole creare) per creare un trigger giornaliero.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-119">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a daily trigger.</span></span> <span data-ttu-id="2f0f8-120">Quando si crea il trigger, impostare il limite iniziale per attivare il trigger e specificare l'ora del giorno in cui viene eseguita l'attività, l'intervallo tra i giorni e il limite finale per disattivare il trigger.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-120">As you create the trigger, set the start boundary to activate the trigger and specify the time of day that the task runs, the interval between the days, and the end boundary to deactivate the trigger.</span></span> <span data-ttu-id="2f0f8-121">Nell'esempio seguente viene illustrato come impostare un criterio di ripetizione per il trigger per ripetere l'attività.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-121">The example below shows how to set a repetition pattern for the trigger to repeat the task.</span></span>
5.  <span data-ttu-id="2f0f8-122">Creare un'azione per l'attività da eseguire usando la proprietà [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="2f0f8-122">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="2f0f8-123">Questa proprietà consente di accedere all'oggetto [**ActionCollection**](actioncollection.md) utilizzato per creare l'azione.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-123">This property provides access to the [**ActionCollection**](actioncollection.md) object used to create the action.</span></span> <span data-ttu-id="2f0f8-124">Utilizzare il metodo [**ActionCollection. Create**](actioncollection-create.md) per specificare il tipo di azione che si desidera creare.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-124">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="2f0f8-125">In questo esempio viene utilizzato un oggetto [**ExecAction**](execaction.md) , che rappresenta un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-125">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="2f0f8-126">Registrare l'attività usando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="2f0f8-126">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="2f0f8-127">Per questo esempio, l'attività avvierà il blocco note alle 8:00 AM ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-127">For this example the task will start Notepad at 8:00 AM every day.</span></span>

<span data-ttu-id="2f0f8-128">Nell'esempio VBScript seguente viene illustrato come pianificare un'attività per eseguire il blocco note ogni giorno alle 8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="2f0f8-128">The following VBScript example shows how to schedule a task to execute Notepad every day at 8:00 AM.</span></span>


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a daily basis.
'------------------------------------------------------------------

' A constant that specifies a daily trigger.
const TriggerTypeDaily = 2
' A constant that specifies an executable action.
const ActionTypeExec = 0

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
regInfo.Description = "Start notepad at 8:00AM daily"
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a daily trigger. Note that the start boundary 
' specifies the time of day that the task starts and the 
' interval specifies what days the task is run.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeDaily)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this time is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysInterval = 1    'Task runs every day.
trigger.Id = "DailyTriggerId"
trigger.Enabled = True

' Set the task repetition pattern for the task.
' This will repeat the task 5 times.
Dim repetitionPattern
Set repetitionPattern = trigger.Repetition
repetitionPattern.Duration = "PT4M"
repetitionPattern.Interval = "PT1M"

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task to run notepad.exe.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExec )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test Daily Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a><span data-ttu-id="2f0f8-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f0f8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f0f8-130">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="2f0f8-130">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




