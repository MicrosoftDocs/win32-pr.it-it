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
# <a name="displaying-task-names-and-states-scripting"></a><span data-ttu-id="223db-103">Visualizzazione di nomi e Stati delle attività (scripting)</span><span class="sxs-lookup"><span data-stu-id="223db-103">Displaying Task Names and States (Scripting)</span></span>

<span data-ttu-id="223db-104">Questo esempio di scripting Mostra come enumerare le attività in una cartella attività e visualizzare i valori delle proprietà da ogni attività.</span><span class="sxs-lookup"><span data-stu-id="223db-104">This scripting example shows how to enumerate tasks in a task folder and display property values from each task.</span></span>

<span data-ttu-id="223db-105">Nella procedura seguente viene descritto come visualizzare i nomi e gli Stati delle attività per tutte le attività in una cartella di attività.</span><span class="sxs-lookup"><span data-stu-id="223db-105">The following procedure describes how to display task names and states for all the tasks in a task folder.</span></span>

<span data-ttu-id="223db-106">**Per visualizzare i nomi delle attività e lo stato di tutte le attività in una cartella attività**</span><span class="sxs-lookup"><span data-stu-id="223db-106">**To display task names and state for all the tasks in a task folder**</span></span>

1.  <span data-ttu-id="223db-107">Creare l'oggetto [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="223db-107">Create the [**TaskService**](taskservice.md) object.</span></span>

    <span data-ttu-id="223db-108">Questo oggetto consente di connettersi al servizio Utilità di pianificazione e accedere a una cartella attività specifica.</span><span class="sxs-lookup"><span data-stu-id="223db-108">This object allows you to connect to the Task Scheduler service and access a specific task folder.</span></span>

2.  <span data-ttu-id="223db-109">Ottenere una cartella attività che contenga le attività per le quali si desiderano informazioni.</span><span class="sxs-lookup"><span data-stu-id="223db-109">Get a task folder that holds the tasks you want information about.</span></span>

    <span data-ttu-id="223db-110">Usare il metodo [**TaskService. GetFolder**](taskservice-getfolder.md) per ottenere la cartella.</span><span class="sxs-lookup"><span data-stu-id="223db-110">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder.</span></span>

3.  <span data-ttu-id="223db-111">Ottiene la raccolta di attività dalla cartella.</span><span class="sxs-lookup"><span data-stu-id="223db-111">Get the collection of tasks from the folder.</span></span>

    <span data-ttu-id="223db-112">Usare il metodo [**TaskFolder. GetTasks**](taskfolder-gettasks.md) per ottenere la raccolta di attività ([**RegisteredTaskCollection**](registeredtaskcollection.md)).</span><span class="sxs-lookup"><span data-stu-id="223db-112">Use the [**TaskFolder.GetTasks**](taskfolder-gettasks.md) method to get the collection of tasks ([**RegisteredTaskCollection**](registeredtaskcollection.md)).</span></span>

4.  <span data-ttu-id="223db-113">Ottenere il numero di attività nella raccolta ed enumerare tutte le attività nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="223db-113">Get the number of tasks in the collection and enumerate through each task in the collection.</span></span>

    <span data-ttu-id="223db-114">Usare la raccolta di oggetti [**RegisteredTaskCollection**](registeredtaskcollection.md) per ottenere un'istanza dell'oggetto [**RegisteredTask**](registeredtask.md) .</span><span class="sxs-lookup"><span data-stu-id="223db-114">Use the [**RegisteredTaskCollection**](registeredtaskcollection.md) collection of objects to get a [**RegisteredTask**](registeredtask.md) object instance.</span></span> <span data-ttu-id="223db-115">Ogni istanza conterrà un'attività nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="223db-115">Each instance will contain a task in the collection.</span></span> <span data-ttu-id="223db-116">È quindi possibile visualizzare le informazioni (valori di proprietà) da ogni attività registrata.</span><span class="sxs-lookup"><span data-stu-id="223db-116">You can then display the information (property values) from each registered task.</span></span>

<span data-ttu-id="223db-117">Nell'esempio VBScript riportato di seguito viene illustrato come enumerare una raccolta di attività registrate nella cartella radice dell'attività e visualizzare il nome e lo stato di ogni attività.</span><span class="sxs-lookup"><span data-stu-id="223db-117">The following VBScript example shows how to enumerate through a collection of registered tasks in the root task folder and display the name and state for each task.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="223db-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="223db-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="223db-119">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="223db-119">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




