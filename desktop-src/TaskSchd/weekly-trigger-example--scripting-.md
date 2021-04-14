---
title: Esempio di trigger settimanale (scripting)
description: Questo esempio di scripting Mostra come creare un'attività che esegue il blocco note alle 8 00 del lunedì di ogni settimana.
ms.assetid: 68ef73b0-3780-480e-90fe-940b6e8a5340
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d9cf627591250c341008ba3a5129c4cc10cad6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395627"
---
# <a name="weekly-trigger-example-scripting"></a><span data-ttu-id="0f18b-103">Esempio di trigger settimanale (scripting)</span><span class="sxs-lookup"><span data-stu-id="0f18b-103">Weekly Trigger Example (Scripting)</span></span>

<span data-ttu-id="0f18b-104">Questo esempio di scripting Mostra come creare un'attività che esegue il blocco note alle 8:00 del lunedì di ogni settimana.</span><span class="sxs-lookup"><span data-stu-id="0f18b-104">This scripting example shows how to create a task that runs Notepad at 8:00 AM on Monday of every week.</span></span> <span data-ttu-id="0f18b-105">L'attività contiene un trigger giornaliero che specifica quando viene eseguita l'attività e un'azione eseguibile che esegue il blocco note.</span><span class="sxs-lookup"><span data-stu-id="0f18b-105">The task contains a daily trigger that specifies when the task runs and an executable action that runs Notepad.</span></span>

<span data-ttu-id="0f18b-106">Nella procedura seguente viene descritto come pianificare un'attività per l'avvio di un eseguibile alle 8:00 del lunedì di ogni settimana.</span><span class="sxs-lookup"><span data-stu-id="0f18b-106">The following procedure describes how to schedule a task to start an executable at 8:00 AM on Monday of every week.</span></span>

<span data-ttu-id="0f18b-107">**Per pianificare l'avvio del blocco note alle 8:00 del lunedì di ogni settimana**</span><span class="sxs-lookup"><span data-stu-id="0f18b-107">**To schedule Notepad to start at 8:00 AM on Monday of every week**</span></span>

1.  <span data-ttu-id="0f18b-108">Creare un oggetto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0f18b-108">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="0f18b-109">Questo oggetto consente di creare l'attività in una cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="0f18b-109">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="0f18b-110">Ottenere una cartella attività e creare un'attività.</span><span class="sxs-lookup"><span data-stu-id="0f18b-110">Get a task folder and create a task.</span></span> <span data-ttu-id="0f18b-111">Usare il metodo [**TaskService. GetFolder**](taskservice-getfolder.md) per ottenere la cartella in cui è archiviata l'attività e il metodo [**TaskService. newTask**](taskservice-newtask.md) per creare l'oggetto [**TaskDefinition**](taskdefinition.md) che rappresenta l'attività.</span><span class="sxs-lookup"><span data-stu-id="0f18b-111">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="0f18b-112">Definire le informazioni sull'attività usando l'oggetto [**TaskDefinition**](taskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="0f18b-112">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="0f18b-113">Utilizzare la proprietà [**TaskDefinition. Settings**](taskdefinition-settings.md) per definire le impostazioni che determinano il modo in cui il servizio Utilità di pianificazione esegue l'attività e la proprietà [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) per definire le informazioni che descrivono l'attività.</span><span class="sxs-lookup"><span data-stu-id="0f18b-113">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="0f18b-114">Creare un trigger settimanale usando la proprietà [**TaskDefinition. Triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="0f18b-114">Create a weekly trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="0f18b-115">Questa proprietà consente di accedere all'oggetto [**TriggerCollection**](triggercollection.md) utilizzato per creare il trigger.</span><span class="sxs-lookup"><span data-stu-id="0f18b-115">This property provides access to the [**TriggerCollection**](triggercollection.md) object that is used to create the trigger.</span></span>

    <span data-ttu-id="0f18b-116">Usare il metodo [**TriggerCollection. Create**](triggercollection-create.md) (specificando il tipo di trigger che si vuole creare) per creare un trigger settimanale.</span><span class="sxs-lookup"><span data-stu-id="0f18b-116">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a weekly trigger.</span></span>

    <span data-ttu-id="0f18b-117">Impostare la proprietà [**WeeklyTrigger. StartBoundary**](trigger-startboundary.md) per specificare quando il trigger è attivato e l'ora del giorno in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="0f18b-117">Set the [**WeeklyTrigger.StartBoundary**](trigger-startboundary.md) property to specify when the trigger is activated and the time of the day when the task is run.</span></span> <span data-ttu-id="0f18b-118">In questo esempio il trigger viene attivato il 1 ° gennaio 2005 e l'attività viene eseguita alle 8:00.</span><span class="sxs-lookup"><span data-stu-id="0f18b-118">In this example the trigger is activated on January 1, 2005 and the task runs at 8:00 AM.</span></span>

    <span data-ttu-id="0f18b-119">Impostare la proprietà [**WeeklyTrigger. EndBoundary**](trigger-endboundary.md)per specificare quando il trigger viene disattivato.</span><span class="sxs-lookup"><span data-stu-id="0f18b-119">Set the [**WeeklyTrigger.EndBoundary**](trigger-endboundary.md)property to specify when the trigger is deactivated.</span></span> <span data-ttu-id="0f18b-120">In questo esempio il trigger viene disattivato il 1 ° gennaio 2015.</span><span class="sxs-lookup"><span data-stu-id="0f18b-120">In this example the trigger is deactivated on January 1, 2015.</span></span>

    <span data-ttu-id="0f18b-121">Impostare la proprietà [**WeeklyTrigger. DaysOfWeek**](weeklytrigger-daysofweek.md) per specificare i giorni della settimana in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="0f18b-121">Set the [**WeeklyTrigger.DaysOfWeek**](weeklytrigger-daysofweek.md) property to specify the days of the week on which the task runs.</span></span> <span data-ttu-id="0f18b-122">In questo esempio l'attività viene eseguita il lunedì.</span><span class="sxs-lookup"><span data-stu-id="0f18b-122">In this example the task is run on Monday.</span></span>

    <span data-ttu-id="0f18b-123">Impostare la proprietà [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md)per specificare l'intervallo tra le settimane nella pianificazione.</span><span class="sxs-lookup"><span data-stu-id="0f18b-123">Set the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md)property to specify the interval between the weeks in the schedule.</span></span> <span data-ttu-id="0f18b-124">In questo esempio l'attività viene eseguita ogni settimana.</span><span class="sxs-lookup"><span data-stu-id="0f18b-124">In this example the task runs every week.</span></span>

5.  <span data-ttu-id="0f18b-125">Creare un'azione per l'attività da eseguire usando la proprietà [**TaskDefinition. Actions**](taskdefinition-actions.md) .</span><span class="sxs-lookup"><span data-stu-id="0f18b-125">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="0f18b-126">Questa proprietà consente di accedere all'oggetto [**ActionCollection**](actioncollection.md) utilizzato per creare l'azione.</span><span class="sxs-lookup"><span data-stu-id="0f18b-126">This property provides access to the [**ActionCollection**](actioncollection.md) object used to create the action.</span></span> <span data-ttu-id="0f18b-127">Utilizzare il metodo [**ActionCollection. Create**](actioncollection-create.md) per specificare il tipo di azione che si desidera creare.</span><span class="sxs-lookup"><span data-stu-id="0f18b-127">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="0f18b-128">In questo esempio viene utilizzato un oggetto [**ExecAction**](execaction.md) , che rappresenta un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="0f18b-128">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="0f18b-129">Registrare l'attività usando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="0f18b-129">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="0f18b-130">Per questo esempio, l'attività avvierà il blocco note alle 8:00 del lunedì di ogni settimana.</span><span class="sxs-lookup"><span data-stu-id="0f18b-130">For this example the task will start Notepad at 8:00 AM on Monday of every week.</span></span>

<span data-ttu-id="0f18b-131">Nell'esempio VBScript seguente viene illustrato come pianificare un'attività per eseguire il blocco note ogni giorno alle 8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="0f18b-131">The following VBScript example shows how to schedule a task to execute Notepad every day at 8:00 AM.</span></span>


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a weekly basis.
'------------------------------------------------------------------

' A constant that specifies a weekly trigger.
const TriggerTypeWeekly = 3
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
regInfo.Description = "Start Notepad weekly."
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a weekly trigger. Note that the start boundary 
' specifies the time of day that the task starts, the 
' day-of-week specfies on what day of the week the task 
' runs, and the interval specifies what weeks the task runs.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeWeekly)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this tims is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysOfWeek = 1
trigger.WeeksInterval = 1    'Task runs every week.
trigger.Id = "WeeklyTriggerId"
trigger.Enabled = True

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
    "Test Weekly Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a><span data-ttu-id="0f18b-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f18b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f18b-133">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0f18b-133">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




