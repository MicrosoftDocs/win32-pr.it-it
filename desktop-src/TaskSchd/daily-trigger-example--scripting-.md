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
# <a name="daily-trigger-example-scripting"></a>Esempio di trigger giornaliero (scripting)

Questo esempio di scripting Mostra come creare un'attività che esegue blocco note alle 8:00 AM ogni giorno. L'attività contiene un trigger giornaliero che specifica un limite iniziale per attivare il trigger e per specificare l'ora del giorno in cui viene eseguita l'attività, un intervallo di trigger per specificare che l'attività viene eseguita ogni giorno e un limite finale per disattivare il trigger. Nell'esempio viene inoltre illustrato come impostare un criterio di ripetizione per il trigger per ripetere l'attività. L'attività contiene anche un'azione eseguibile che esegue il blocco note.

Nella procedura seguente viene descritto come pianificare un'attività per l'avvio di un eseguibile alle 8:00 di ogni giorno. (Questi passaggi corrispondono ai commenti del codice inclusi nel codice di esempio).

**Per pianificare l'avvio del blocco note alle 8:00 di ogni giorno**

1.  Creare un oggetto [**TaskService**](taskservice.md) . Questo oggetto consente di creare l'attività in una cartella specificata.
2.  Ottenere una cartella attività e creare un'attività. Usare il metodo [**TaskService. GetFolder**](taskservice-getfolder.md) per ottenere la cartella in cui è archiviata l'attività e il metodo [**TaskService. newTask**](taskservice-newtask.md) per creare l'oggetto [**TaskDefinition**](taskdefinition.md) che rappresenta l'attività.
3.  Definire le informazioni sull'attività usando l'oggetto [**TaskDefinition**](taskdefinition.md) . Utilizzare la proprietà [**TaskDefinition. Settings**](taskdefinition-settings.md) per definire le impostazioni che determinano il modo in cui il servizio Utilità di pianificazione esegue l'attività e la proprietà [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) per definire le informazioni che descrivono l'attività.
4.  Creare un trigger giornaliero usando la proprietà [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Questa proprietà consente di accedere all'oggetto [**TriggerCollection**](triggercollection.md) utilizzato per creare il trigger. Usare il metodo [**TriggerCollection. Create**](triggercollection-create.md) (specificando il tipo di trigger che si vuole creare) per creare un trigger giornaliero. Quando si crea il trigger, impostare il limite iniziale per attivare il trigger e specificare l'ora del giorno in cui viene eseguita l'attività, l'intervallo tra i giorni e il limite finale per disattivare il trigger. Nell'esempio seguente viene illustrato come impostare un criterio di ripetizione per il trigger per ripetere l'attività.
5.  Creare un'azione per l'attività da eseguire usando la proprietà [**TaskDefinition. Actions**](taskdefinition-actions.md) . Questa proprietà consente di accedere all'oggetto [**ActionCollection**](actioncollection.md) utilizzato per creare l'azione. Utilizzare il metodo [**ActionCollection. Create**](actioncollection-create.md) per specificare il tipo di azione che si desidera creare. In questo esempio viene utilizzato un oggetto [**ExecAction**](execaction.md) , che rappresenta un'azione che esegue un'operazione della riga di comando.
6.  Registrare l'attività usando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . Per questo esempio, l'attività avvierà il blocco note alle 8:00 AM ogni giorno.

Nell'esempio VBScript seguente viene illustrato come pianificare un'attività per eseguire il blocco note ogni giorno alle 8:00 AM.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




