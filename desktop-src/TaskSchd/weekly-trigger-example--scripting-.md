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
# <a name="weekly-trigger-example-scripting"></a>Esempio di trigger settimanale (scripting)

Questo esempio di scripting Mostra come creare un'attività che esegue il blocco note alle 8:00 del lunedì di ogni settimana. L'attività contiene un trigger giornaliero che specifica quando viene eseguita l'attività e un'azione eseguibile che esegue il blocco note.

Nella procedura seguente viene descritto come pianificare un'attività per l'avvio di un eseguibile alle 8:00 del lunedì di ogni settimana.

**Per pianificare l'avvio del blocco note alle 8:00 del lunedì di ogni settimana**

1.  Creare un oggetto [**TaskService**](taskservice.md) . Questo oggetto consente di creare l'attività in una cartella specificata.
2.  Ottenere una cartella attività e creare un'attività. Usare il metodo [**TaskService. GetFolder**](taskservice-getfolder.md) per ottenere la cartella in cui è archiviata l'attività e il metodo [**TaskService. newTask**](taskservice-newtask.md) per creare l'oggetto [**TaskDefinition**](taskdefinition.md) che rappresenta l'attività.
3.  Definire le informazioni sull'attività usando l'oggetto [**TaskDefinition**](taskdefinition.md) . Utilizzare la proprietà [**TaskDefinition. Settings**](taskdefinition-settings.md) per definire le impostazioni che determinano il modo in cui il servizio Utilità di pianificazione esegue l'attività e la proprietà [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) per definire le informazioni che descrivono l'attività.
4.  Creare un trigger settimanale usando la proprietà [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Questa proprietà consente di accedere all'oggetto [**TriggerCollection**](triggercollection.md) utilizzato per creare il trigger.

    Usare il metodo [**TriggerCollection. Create**](triggercollection-create.md) (specificando il tipo di trigger che si vuole creare) per creare un trigger settimanale.

    Impostare la proprietà [**WeeklyTrigger. StartBoundary**](trigger-startboundary.md) per specificare quando il trigger è attivato e l'ora del giorno in cui viene eseguita l'attività. In questo esempio il trigger viene attivato il 1 ° gennaio 2005 e l'attività viene eseguita alle 8:00.

    Impostare la proprietà [**WeeklyTrigger. EndBoundary**](trigger-endboundary.md)per specificare quando il trigger viene disattivato. In questo esempio il trigger viene disattivato il 1 ° gennaio 2015.

    Impostare la proprietà [**WeeklyTrigger. DaysOfWeek**](weeklytrigger-daysofweek.md) per specificare i giorni della settimana in cui viene eseguita l'attività. In questo esempio l'attività viene eseguita il lunedì.

    Impostare la proprietà [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md)per specificare l'intervallo tra le settimane nella pianificazione. In questo esempio l'attività viene eseguita ogni settimana.

5.  Creare un'azione per l'attività da eseguire usando la proprietà [**TaskDefinition. Actions**](taskdefinition-actions.md) . Questa proprietà consente di accedere all'oggetto [**ActionCollection**](actioncollection.md) utilizzato per creare l'azione. Utilizzare il metodo [**ActionCollection. Create**](actioncollection-create.md) per specificare il tipo di azione che si desidera creare. In questo esempio viene utilizzato un oggetto [**ExecAction**](execaction.md) , che rappresenta un'azione che esegue un'operazione della riga di comando.
6.  Registrare l'attività usando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . Per questo esempio, l'attività avvierà il blocco note alle 8:00 del lunedì di ogni settimana.

Nell'esempio VBScript seguente viene illustrato come pianificare un'attività per eseguire il blocco note ogni giorno alle 8:00 AM.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




