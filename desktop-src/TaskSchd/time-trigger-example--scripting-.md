---
title: Esempio di trigger di ora (scripting)
description: Questo esempio di scripting Mostra come creare un'attività che esegue blocco note a un'ora specifica.
ms.assetid: 8511ffcd-166f-4c63-9cd2-ead53dde9ed8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77cbf9eab12f5ca027fbb6c48ade37a9f57d9beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297949"
---
# <a name="time-trigger-example-scripting"></a>Esempio di trigger di ora (scripting)

Questo esempio di scripting Mostra come creare un'attività che esegue blocco note a un'ora specifica. L'attività contiene un trigger basato sul tempo che specifica un limite iniziale per l'attivazione dell'attività, un'azione eseguibile che esegue blocco note e un limite finale che disattiva l'attività.

Nella procedura seguente viene descritto come pianificare un'attività per avviare un eseguibile in un momento specifico.

**Per pianificare l'avvio del blocco note a un'ora specifica**

1.  Creare un oggetto [**TaskService**](taskservice.md) . Questo oggetto consente di creare l'attività in una cartella specificata.
2.  Ottenere una cartella attività e creare un'attività. Usare il metodo [**TaskService. GetFolder**](taskservice-getfolder.md) per ottenere la cartella in cui è archiviata l'attività e il metodo [**TaskService. newTask**](taskservice-newtask.md) per creare l'oggetto [**TaskDefinition**](taskdefinition.md) che rappresenta l'attività.
3.  Definire le informazioni sull'attività usando l'oggetto [**TaskDefinition**](taskdefinition.md) . Utilizzare la proprietà [**TaskDefinition. Settings**](taskdefinition-settings.md) per definire le impostazioni che determinano il modo in cui il servizio Utilità di pianificazione esegue l'attività e la proprietà [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) per definire le informazioni che descrivono l'attività.
4.  Creare un trigger basato sul tempo usando la proprietà [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Questa proprietà fornisce l'accesso all'oggetto [**TriggerCollection**](triggercollection.md) . Usare il metodo [**TriggerCollection. Create**](triggercollection-create.md) (specificando il tipo di trigger che si vuole creare) per creare un trigger basato sul tempo. Quando si crea il trigger, impostare i limiti iniziale e finale del trigger per attivare e disattivare il trigger. Il limite iniziale specifica quando verrà eseguita l'azione dell'attività.
5.  Creare un'azione per l'attività da eseguire usando la proprietà [**TaskDefinition. Actions**](taskdefinition-actions.md) . Questa proprietà consente di accedere all'oggetto [**ActionCollection**](actioncollection.md) . Utilizzare il metodo [**ActionCollection. Create**](actioncollection-create.md) per specificare il tipo di azione che si desidera creare. In questo esempio viene utilizzato un oggetto [**ExecAction**](execaction.md) , che rappresenta un'azione che esegue un'operazione della riga di comando.
6.  Registrare l'attività usando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . Per questo esempio, l'attività avvierà il blocco note all'ora corrente più 30 secondi.

Nell'esempio VBScript seguente viene illustrato come pianificare un'attività per eseguire il blocco note 30 secondi dopo la registrazione dell'attività.


```VB
'------------------------------------------------------------------
' This sample schedules a task to start notepad.exe 30 seconds
' from the time the task is registered.
'------------------------------------------------------------------

' A constant that specifies a time-based trigger.
const TriggerTypeTime = 1
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
regInfo.Description = "Start notepad at a certain time"
regInfo.Author = "Author Name"

'********************************************************
' Set the principal for the task
Dim principal
Set principal = taskDefinition.Principal

' Set the logon type to interactive logon
principal.LogonType = 3


' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a time-based trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeTime)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime

Dim time
time = DateAdd("s", 30, Now)  'start time = 30 seconds from now
startTime = XmlTime(time)

time = DateAdd("n", 5, Now) 'end time = 5 minutes from now
endTime = XmlTime(time)

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "TimeTriggerId"
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
    "Test TimeTrigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."



'------------------------------------------------------------------
' Used to get the time for the trigger 
' startBoundary and endBoundary.
' Return the time in the correct format: 
' YYYY-MM-DDTHH:MM:SS. 
'------------------------------------------------------------------
Function XmlTime(t)
    Dim cSecond, cMinute, CHour, cDay, cMonth, cYear
    Dim tTime, tDate

    cSecond = "0" & Second(t)
    cMinute = "0" & Minute(t)
    cHour = "0" & Hour(t)
    cDay = "0" & Day(t)
    cMonth = "0" & Month(t)
    cYear = Year(t)

    tTime = Right(cHour, 2) & ":" & Right(cMinute, 2) & _
        ":" & Right(cSecond, 2)
    tDate = cYear & "-" & Right(cMonth, 2) & "-" & Right(cDay, 2)
    XmlTime = tDate & "T" & tTime 
End Function

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




