---
description: In Gestione autorizzazioni un ruolo rappresenta una categoria di utenti e le attività che gli utenti sono autorizzati a eseguire.
ms.assetid: a4981774-0f5c-4032-8a7d-d9ef44c76abe
title: Raggruppamento di attività in ruoli nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c84ec45bba8da9d76e2a4fe0b31324429374a74b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968290"
---
# <a name="grouping-tasks-into-roles-in-script"></a>Raggruppamento di attività in ruoli nello script

In Gestione autorizzazioni, un ruolo rappresenta una categoria di utenti e le attività che gli utenti sono autorizzati a eseguire. Le attività vengono raggruppate e assegnate a una definizione di ruolo, rappresentata da un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) con la proprietà [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) impostata su **true**. La definizione del ruolo può quindi essere assegnata a un oggetto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) e gli utenti o i gruppi di utenti vengono quindi assegnati a tale oggetto. Per ulteriori informazioni sulle attività e sui ruoli, vedere [ruoli](roles.md).

Nell'esempio seguente viene illustrato come assegnare attività a una definizione di ruolo, creare un oggetto Role e assegnare la definizione di ruolo all'oggetto Role. Nell'esempio si presuppone che esista un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C, che questo archivio contiene un'applicazione denominata Expense e che l'applicazione contenga attività denominate Invia spese e approva spese.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a task object to act as a role definition.
Dim roleTask
Set roleTask = expenseApp.CreateTask("Expense Admin")

'  Set the IsRoleDefinition property of roleTask to True.
roleTask.IsRoleDefinition = True

'  Add two tasks to the role definition.
roleTask.AddTask CStr("Submit Expense")
roleTask.AddTask CStr("Approve Expense")

'  Save the role definition to the store.
roleTask.Submit

'  Create a role object.
Dim role1
Set role1 = expenseApp.CreateRole("Expense Administrator")

'  Add the role definition to the role object.
role1.AddTask(roleTask.Name)

'  Save the role object to the store.
role1.Submit
```



 

 



