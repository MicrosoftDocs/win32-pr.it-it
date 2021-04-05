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
# <a name="boot-trigger-example-scripting"></a>Esempio di trigger di avvio (scripting)

Questo esempio di scripting Mostra come creare un'attività pianificata per l'esecuzione del blocco note al momento dell'avvio del sistema. L'attività contiene un trigger di avvio che specifica un limite iniziale e un tempo di ritardo per l'avvio dell'attività dopo l'avvio del sistema. L'attività contiene anche un'azione che specifica l'attività per l'esecuzione del blocco note. L'attività viene registrata utilizzando l'account del servizio locale come contesto di sicurezza per l'esecuzione dell'attività.

Nella procedura riportata di seguito viene descritto come pianificare un eseguibile, ad esempio Blocco note, da avviare al momento dell'avvio del sistema.

**Per pianificare l'avvio del blocco note al momento dell'avvio del sistema**

1.  Creare un oggetto [**TaskService**](taskservice.md) . Questo oggetto consente di creare l'attività in una cartella specificata.
2.  Ottenere una cartella attività e creare un'attività. Usare il metodo [**TaskService. GetFolder**](taskservice-getfolder.md) per ottenere la cartella in cui è archiviata l'attività e il metodo [**TaskService. newTask**](taskservice-newtask.md) per creare l'oggetto [**TaskDefinition**](taskdefinition.md) che rappresenta l'attività.
3.  Definire le informazioni sull'attività usando l'oggetto [**TaskDefinition**](taskdefinition.md) . Utilizzare la proprietà [**TaskDefinition. Settings**](taskdefinition-settings.md) per definire le impostazioni che determinano il modo in cui il servizio Utilità di pianificazione esegue l'attività e la proprietà [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) per definire le informazioni che descrivono l'attività.
4.  Creare un trigger LOGON usando la proprietà [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Questa proprietà fornisce l'accesso all'oggetto [**TriggerCollection**](triggercollection.md) . Usare il metodo [**TriggerCollection. Create**](triggercollection-create.md) (specificando il tipo di trigger che si vuole creare) per creare un trigger di avvio. Quando si crea il trigger, impostare le proprietà [**StartBoundary**](trigger-startboundary.md) e [**EndBoundary**](trigger-endboundary.md) del trigger per attivare e disattivare il trigger. È anche possibile specificare un valore per la proprietà [**delay**](boottrigger-delay.md) del trigger di avvio.
5.  Creare un'azione per l'attività da eseguire usando la proprietà [**TaskDefinition. Actions**](taskdefinition-actions.md) . Questa proprietà consente di accedere all'oggetto [**ActionCollection**](actioncollection.md) . Utilizzare il metodo [**ActionCollection. Create**](actioncollection-create.md) per specificare il tipo di azione che si desidera creare. Questo esempio usa un oggetto [**ExecAction**](execaction.md) , che rappresenta un'azione che avvia un eseguibile.
6.  Registrare l'attività usando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) . L'attività viene registrata utilizzando l'account del servizio locale come contesto di sicurezza per l'esecuzione dell'attività.

Nell'esempio VBScript seguente viene illustrato come pianificare un'attività per eseguire il blocco note 30 secondi dopo l'avvio del sistema.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




