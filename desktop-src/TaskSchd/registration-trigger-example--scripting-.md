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
# <a name="registration-trigger-example-scripting"></a>Esempio di trigger di registrazione (scripting)

Questo esempio di scripting Mostra come creare un'attività pianificata per l'esecuzione del blocco note quando un'attività viene registrata. L'attività contiene un trigger di registrazione che specifica un limite iniziale e un limite finale per l'attività. Il limite iniziale specifica quando viene attivato il trigger. L'attività contiene anche un'azione che specifica l'attività per l'esecuzione del blocco note.

> [!Note]  
> Quando si aggiorna un'attività con un trigger di registrazione, l'attività verrà eseguita dopo l'aggiornamento.

 

Nella procedura riportata di seguito viene descritto come pianificare un eseguibile, ad esempio Blocco note, da avviare quando viene registrata un'attività.

**Per pianificare l'avvio del blocco note quando viene registrata un'attività**

1.  Creare un oggetto [**TaskService**](taskservice.md) . Questo oggetto consente di creare l'attività in una cartella specificata.
2.  Ottenere una cartella attività e creare un'attività. Usare il metodo [**TaskService. GetFolder**](taskservice-getfolder.md) per ottenere la cartella in cui è archiviata l'attività e il metodo [**TaskService. newTask**](taskservice-newtask.md) per creare l'oggetto [**TaskDefinition**](taskdefinition.md) che rappresenta l'attività.
3.  Definire le informazioni sull'attività usando l'oggetto [**TaskDefinition**](taskdefinition.md) . Utilizzare la proprietà [**TaskDefinition. Settings**](taskdefinition-settings.md) per definire le impostazioni che determinano il modo in cui il servizio Utilità di pianificazione esegue l'attività e la proprietà [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) per definire le informazioni che descrivono l'attività.
4.  Creare un trigger di registrazione usando la proprietà [**TaskDefinition. Triggers**](taskdefinition-triggers.md) . Questa proprietà fornisce l'accesso all'oggetto [**TriggerCollection**](triggercollection.md) . Usare il metodo [**TriggerCollection. Create**](triggercollection-create.md) (specificando il tipo di trigger che si vuole creare) per creare un trigger di registrazione.
5.  Creare un'azione per l'attività da eseguire usando la proprietà [**TaskDefinition. Actions**](taskdefinition-actions.md) . Questa proprietà consente di accedere all'oggetto [**ActionCollection**](actioncollection.md) . Utilizzare il metodo [**ActionCollection. Create**](actioncollection-create.md) per specificare il tipo di azione che si desidera creare. Questo esempio usa un oggetto [**ExecAction**](execaction.md) , che rappresenta un'azione che avvia un eseguibile.
6.  Registrare l'attività usando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .

Nell'esempio VBScript seguente viene illustrato come creare un'attività per la pianificazione del blocco note da eseguire quando l'attività è registrata.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




