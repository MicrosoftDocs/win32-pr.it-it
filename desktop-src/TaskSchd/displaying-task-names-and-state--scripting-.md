---
title: Visualizzazione dei nomi e degli stati delle attività (scripting)
description: Questo esempio di scripting illustra come enumerare le attività in una cartella di attività e visualizzare i valori delle proprietà di ogni attività.
ms.assetid: 2a84a752-fbf3-4041-8b0a-304f89a49354
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6f3ec036b1d9d61c387495b48874bf742a9479ae0608f0e5c728a029df24709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002489"
---
# <a name="displaying-task-names-and-states-scripting"></a>Visualizzazione dei nomi e degli stati delle attività (scripting)

Questo esempio di scripting illustra come enumerare le attività in una cartella di attività e visualizzare i valori delle proprietà di ogni attività.

La procedura seguente descrive come visualizzare i nomi e gli stati delle attività per tutte le attività in una cartella di attività.

**Per visualizzare i nomi e lo stato delle attività per tutte le attività in una cartella di attività**

1.  Creare [**l'oggetto TaskService.**](taskservice.md)

    Questo oggetto consente di connettersi al servizio Utilità di pianificazione e accedere a una cartella di attività specifica.

2.  Ottenere una cartella di attività che contiene le attività su cui si vogliono ottenere informazioni.

    Usare il [**metodo TaskService.GetFolder**](taskservice-getfolder.md) per ottenere la cartella.

3.  Ottenere la raccolta di attività dalla cartella.

    Usare il [**metodo TaskFolder.GetTasks**](taskfolder-gettasks.md) per ottenere la raccolta di attività ([**RegisteredTaskCollection**](registeredtaskcollection.md)).

4.  Ottenere il numero di attività nella raccolta ed enumerare ogni attività nella raccolta.

    Usare la [**raccolta RegisteredTaskCollection**](registeredtaskcollection.md) di oggetti per ottenere un'istanza [**dell'oggetto RegisteredTask.**](registeredtask.md) Ogni istanza conterrà un'attività nella raccolta. È quindi possibile visualizzare le informazioni (valori delle proprietà) di ogni attività registrata.

L'esempio VBScript seguente illustra come enumerare tramite una raccolta di attività registrate nella cartella delle attività radice e visualizzare il nome e lo stato per ogni attività.


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

[Uso del Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




