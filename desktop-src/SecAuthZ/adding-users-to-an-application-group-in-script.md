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
ms.openlocfilehash: 6fd92a69a236e6b4d04d5bb0a1a8b961c699d434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315844"
---
# <a name="adding-users-to-an-application-group-in-script"></a><span data-ttu-id="29c38-105">Aggiunta di utenti a un gruppo di applicazioni nello script</span><span class="sxs-lookup"><span data-stu-id="29c38-105">Adding Users to an Application Group in Script</span></span>

<span data-ttu-id="29c38-106">In Gestione autorizzazioni, un gruppo di applicazioni è costituito da un gruppo di utenti e gruppi di utenti.</span><span class="sxs-lookup"><span data-stu-id="29c38-106">In Authorization Manager, an application group is a group of users and user groups.</span></span> <span data-ttu-id="29c38-107">Un gruppo di applicazioni può contenere altri gruppi di applicazioni, quindi i gruppi di utenti possono essere annidati.</span><span class="sxs-lookup"><span data-stu-id="29c38-107">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="29c38-108">Un gruppo di applicazioni è rappresentato da un oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="29c38-108">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>

<span data-ttu-id="29c38-109">**Per consentire ai membri di un gruppo di applicazioni di eseguire un'attività o un set di attività**</span><span class="sxs-lookup"><span data-stu-id="29c38-109">**To allow members of an application group to perform a task or set of tasks**</span></span>

-   <span data-ttu-id="29c38-110">Assegnare il gruppo di applicazioni a un ruolo che contiene tali attività.</span><span class="sxs-lookup"><span data-stu-id="29c38-110">Assign that application group to a role that contains those tasks.</span></span>

    <span data-ttu-id="29c38-111">I ruoli sono rappresentati da oggetti [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) .</span><span class="sxs-lookup"><span data-stu-id="29c38-111">Roles are represented by [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) objects.</span></span>

<span data-ttu-id="29c38-112">Nell'esempio seguente viene illustrato come creare un gruppo di applicazioni, aggiungere un utente come membro del gruppo di applicazioni e assegnare il gruppo di applicazioni a un ruolo esistente.</span><span class="sxs-lookup"><span data-stu-id="29c38-112">The following example shows how to create an application group, add a user as a member of the application group, and assign the application group to an existing role.</span></span> <span data-ttu-id="29c38-113">Nell'esempio si presuppone che esista un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C, che questo archivio contiene un'applicazione denominata Expense e che l'applicazione contenga un ruolo denominato Expense Administrator.</span><span class="sxs-lookup"><span data-stu-id="29c38-113">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains a role named Expense Administrator.</span></span>


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



 

 



