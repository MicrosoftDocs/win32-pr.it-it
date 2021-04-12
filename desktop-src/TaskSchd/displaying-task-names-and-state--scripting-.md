---
title: Visualizzazione di nomi e Stati delle attività (scripting)
description: Questo esempio di scripting Mostra come enumerare le attività in una cartella attività e visualizzare i valori delle proprietà da ogni attività.
ms.assetid: 2a84a752-fbf3-4041-8b0a-304f89a49354
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7a8f22977f8cfd2d40b3c37a1cc8d7bcb5259e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396298"
---
# <a name="displaying-task-names-and-states-scripting"></a>Visualizzazione di nomi e Stati delle attività (scripting)

Questo esempio di scripting Mostra come enumerare le attività in una cartella attività e visualizzare i valori delle proprietà da ogni attività.

Nella procedura seguente viene descritto come visualizzare i nomi e gli Stati delle attività per tutte le attività in una cartella di attività.

**Per visualizzare i nomi delle attività e lo stato di tutte le attività in una cartella attività**

1.  Creare l'oggetto [**TaskService**](taskservice.md) .

    Questo oggetto consente di connettersi al servizio Utilità di pianificazione e accedere a una cartella attività specifica.

2.  Ottenere una cartella attività che contenga le attività per le quali si desiderano informazioni.

    Usare il metodo [**TaskService. GetFolder**](taskservice-getfolder.md) per ottenere la cartella.

3.  Ottiene la raccolta di attività dalla cartella.

    Usare il metodo [**TaskFolder. GetTasks**](taskfolder-gettasks.md) per ottenere la raccolta di attività ([**RegisteredTaskCollection**](registeredtaskcollection.md)).

4.  Ottenere il numero di attività nella raccolta ed enumerare tutte le attività nella raccolta.

    Usare la raccolta di oggetti [**RegisteredTaskCollection**](registeredtaskcollection.md) per ottenere un'istanza dell'oggetto [**RegisteredTask**](registeredtask.md) . Ogni istanza conterrà un'attività nella raccolta. È quindi possibile visualizzare le informazioni (valori di proprietà) da ogni attività registrata.

Nell'esempio VBScript riportato di seguito viene illustrato come enumerare una raccolta di attività registrate nella cartella radice dell'attività e visualizzare il nome e lo stato di ogni attività.


```VB
'---------------------------------------------------------
' This sample enumerates through the tasks on the local computer and
' displays their name and state.
'---------------------------------------------------------


' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

' Get the task folder that contains the tasks. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")
 
Dim taskCollection
Set taskCollection = rootFolder.GetTasks(0)

Dim numberOfTasks
numberOfTasks = taskCollection.Count

If numberOfTasks = 0 Then 
    Wscript.Echo "No tasks are registered."
Else
    WScript.Echo "Number of tasks registered: " & numberOfTasks
    
    Dim registeredTask
    For Each registeredTask In taskCollection
        WScript.Echo "Task Name: " & registeredTask.Name
    
        Dim taskState 
        Select Case registeredTask.State 
            Case "0"
                taskState = "Unknown"
            Case "1"
                taskState = "Disabled"
            Case "2"
                taskState = "Queued"
            Case "3"
                taskState = "Ready"
            Case "4"
                taskState = "Running"
        End Select

        WScript.Echo "    Task State: " & taskState
    Next
End If

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




