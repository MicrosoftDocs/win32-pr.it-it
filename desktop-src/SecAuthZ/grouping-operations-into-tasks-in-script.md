---
description: In Gestione autorizzazioni un'attività è un'azione di alto livello che gli utenti di un'applicazione devono completare.
ms.assetid: a266dde7-86f8-4537-99a5-be7142e765c6
title: Raggruppamento di operazioni in attività nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fb7fc1d4a84cd42dc0ae48af4fcbf02412b93337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884474"
---
# <a name="grouping-operations-into-tasks-in-script"></a><span data-ttu-id="7771a-103">Raggruppamento di operazioni in attività nello script</span><span class="sxs-lookup"><span data-stu-id="7771a-103">Grouping Operations into Tasks in Script</span></span>

<span data-ttu-id="7771a-104">In Gestione autorizzazioni un'attività è un'azione di alto livello che gli utenti di un'applicazione devono completare.</span><span class="sxs-lookup"><span data-stu-id="7771a-104">In Authorization Manager, a task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="7771a-105">Le attività sono costituite da operazioni, ovvero funzioni di basso livello e metodi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7771a-105">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span> <span data-ttu-id="7771a-106">Viene quindi assegnata un'attività ai ruoli che devono eseguire tale attività.</span><span class="sxs-lookup"><span data-stu-id="7771a-106">A task is then assigned to those roles that must perform that task.</span></span> <span data-ttu-id="7771a-107">Un'attività è rappresentata da un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) .</span><span class="sxs-lookup"><span data-stu-id="7771a-107">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="7771a-108">Per ulteriori informazioni sulle operazioni e sulle attività, vedere [operazioni e attività](operations-and-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="7771a-108">For more information about operations and tasks, see [Operations and Tasks](operations-and-tasks.md).</span></span>

<span data-ttu-id="7771a-109">Nell'esempio seguente viene illustrato come raggruppare le operazioni per creare un'attività.</span><span class="sxs-lookup"><span data-stu-id="7771a-109">The following example shows how to group operations to create a task.</span></span> <span data-ttu-id="7771a-110">Nell'esempio si presuppone che esista un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C, che questo archivio contiene un'applicazione denominata Expense e che l'applicazione contenga operazioni definite nell'argomento [definizione di operazioni nello script](defining-operations-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="7771a-110">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains operations defined in the topic [Defining Operations in Script](defining-operations-in-script.md).</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create a task object.
Dim Task1
Set Task1 = expenseApp.CreateTask("Submit Expense")

'  Add operations to the task.
Task1.AddOperation CStr("RetrieveForm")
Task1.AddOperation CStr("EnqueRequest")
Task1.AddOperation Cstr("UseFormControl")

'  Save the task to the store.
Task1.Submit
```



 

 



