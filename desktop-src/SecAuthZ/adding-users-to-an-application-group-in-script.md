---
description: Un gruppo di applicazioni è un gruppo di utenti e gruppi di utenti. Un gruppo di applicazioni può contenere altri gruppi di applicazioni, quindi i gruppi di utenti possono essere annidati. Un gruppo di applicazioni è rappresentato da un oggetto IAzApplicationGroup.
ms.assetid: 9ec5b55e-3d66-44f6-9b59-a5e66192d8ac
title: Aggiunta di utenti a un gruppo di applicazioni nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 18c990e3140dcfc6a4cbc2d57379431075387f43af8fbb0b22f344ffd0b9a30b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784933"
---
# <a name="adding-users-to-an-application-group-in-script"></a>Aggiunta di utenti a un gruppo di applicazioni nello script

In Gestione autorizzazioni un gruppo di applicazioni è un gruppo di utenti e gruppi di utenti. Un gruppo di applicazioni può contenere altri gruppi di applicazioni, quindi i gruppi di utenti possono essere annidati. Un gruppo di applicazioni è rappresentato da un [**oggetto IAzApplicationGroup.**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup)

**Per consentire ai membri di un gruppo di applicazioni di eseguire un'attività o un set di attività**

-   Assegnare il gruppo di applicazioni a un ruolo che contiene tali attività.

    I ruoli sono rappresentati [**da oggetti IAzRole.**](/windows/desktop/api/Azroles/nn-azroles-iazrole)

Nell'esempio seguente viene illustrato come creare un gruppo di applicazioni, aggiungere un utente come membro del gruppo di applicazioni e assegnare il gruppo di applicazioni a un ruolo esistente. Nell'esempio si presuppone che sia presente un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C, che questo archivio contenga un'applicazione denominata Expense e che questa applicazione contenga un ruolo denominato Expense Administrator.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Approvers")

'  Add a member to the group.
'  Replace with valid domain and user name.
appGroup.AddMemberName("domain\\username")

'  Save information to the store.
appGroup.Submit

'  Open a role object.
Dim adminRole
Set adminRole = expenseApp.OpenRole("Expense Administrator")

'  Add the group to the role.
adminRole.AddAppMember("Approvers")

'  Save the information to the store.
adminRole.Submit
```



 

 



