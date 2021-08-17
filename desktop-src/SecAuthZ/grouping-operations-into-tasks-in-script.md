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
ms.openlocfilehash: 29c7dedb9944a208e5ba128f0341a8cbde3e787056c099d527be8f79260c6f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913575"
---
# <a name="grouping-operations-into-tasks-in-script"></a>Raggruppamento di operazioni in attività nello script

In Gestione autorizzazioni un'attività è un'azione di alto livello che gli utenti di un'applicazione devono completare. Le attività sono costituito da operazioni, ovvero funzioni di basso livello e metodi dell'applicazione. Un'attività viene quindi assegnata ai ruoli che devono eseguire tale attività. Un'attività è rappresentata da un [**oggetto IAzTask.**](/windows/desktop/api/Azroles/nn-azroles-iaztask) Per altre informazioni su operazioni e attività, vedere [Operazioni e attività](operations-and-tasks.md).

Nell'esempio seguente viene illustrato come raggruppare le operazioni per creare un'attività. Nell'esempio si presuppone che sia presente un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C, che l'archivio contenga un'applicazione denominata Expense e che questa applicazione contenga operazioni definite nell'argomento Definizione delle operazioni [nello script](defining-operations-in-script.md).


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



 

 



