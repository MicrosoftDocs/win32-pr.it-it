---
title: Esempio di trigger giornaliero (scripting)
description: Questo esempio di scripting mostra come creare un'attività che viene Blocco note alle 8.00 di ogni giorno.
ms.assetid: a13bd54d-b45a-46e5-8281-d080f50f6bef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 530d687264af9d2e7dbd4e9d05cf7dde39a449d3249c3576a35edc8a9e9f088d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139534"
---
# <a name="daily-trigger-example-scripting"></a>Esempio di trigger giornaliero (scripting)

Questo esempio di scripting mostra come creare un'attività che viene Blocco note alle 8:00 ogni giorno. L'attività contiene un trigger giornaliero che specifica un limite di inizio per attivare il trigger e per specificare l'ora del giorno in cui viene eseguita l'attività, un intervallo di trigger per specificare che l'attività viene eseguita ogni giorno e un limite finale per disattivare il trigger. L'esempio mostra anche come impostare un modello di ripetizione per il trigger per ripetere l'attività. L'attività contiene anche un'azione eseguibile che viene eseguita Blocco note.

La procedura seguente descrive come pianificare un'attività per avviare un eseguibile alle 8:00 ogni giorno. Questi passaggi corrispondono ai commenti del codice inclusi nel codice di esempio.

**Per pianificare Blocco note iniziare ogni giorno alle 8:00**

1.  Creare un [**oggetto TaskService.**](taskservice.md) Questo oggetto consente di creare l'attività in una cartella specificata.
2.  Ottenere una cartella di attività e creare un'attività. Usare il [**metodo TaskService.GetFolder**](taskservice-getfolder.md) per ottenere la cartella in cui è archiviata l'attività e il metodo [**TaskService.NewTask**](taskservice-newtask.md) per creare l'oggetto [**TaskDefinition**](taskdefinition.md) che rappresenta l'attività.
3.  Definire le informazioni sull'attività usando [**l'oggetto TaskDefinition.**](taskdefinition.md) Usare la proprietà [**TaskDefinition.Impostazioni**](taskdefinition-settings.md) per definire le impostazioni che determinano come il servizio Utilità di pianificazione esegue l'attività e la proprietà [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) per definire le informazioni che descrivono l'attività.
4.  Creare un trigger giornaliero usando la [**proprietà TaskDefinition.Triggers.**](taskdefinition-triggers.md) Questa proprietà consente di accedere [**all'oggetto TriggerCollection**](triggercollection.md) usato per creare il trigger. Usare il [**metodo TriggerCollection.Create**](triggercollection-create.md) (che specifica il tipo di trigger che si vuole creare) per creare un trigger giornaliero. Quando si crea il trigger, impostare il limite iniziale per attivare il trigger e specificare l'ora del giorno in cui viene eseguita l'attività, l'intervallo tra i giorni e il limite finale per disattivare il trigger. L'esempio seguente illustra come impostare un modello di ripetizione per il trigger per ripetere l'attività.
5.  Creare un'azione per l'attività da eseguire usando la [**proprietà TaskDefinition.Actions.**](taskdefinition-actions.md) Questa proprietà consente di accedere [**all'oggetto ActionCollection**](actioncollection.md) usato per creare l'azione. Usare il [**metodo ActionCollection.Create**](actioncollection-create.md) per specificare il tipo di azione che si vuole creare. Questo esempio usa un [**oggetto ExecAction,**](execaction.md) che rappresenta un'azione che esegue un'operazione della riga di comando.
6.  Registrare l'attività usando [**il metodo TaskFolder.RegisterTaskDefinition.**](taskfolder-registertaskdefinition.md) Per questo esempio l'attività Blocco note alle 8:00 ogni giorno.

Nell'esempio vbscript seguente viene illustrato come pianificare un'attività da eseguire Blocco note ogni giorno alle 8:00.


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

[Uso del Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




