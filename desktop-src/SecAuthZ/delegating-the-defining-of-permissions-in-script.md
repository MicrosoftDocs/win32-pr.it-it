---
description: È possibile delegare l'amministrazione degli archivi dei criteri di autorizzazione archiviati in Active Directory.
ms.assetid: a7b43dfe-f03e-4795-bbd3-746eb3449fd0
title: Delega della definizione di autorizzazioni nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a9569f82271642a610919db8246cc6389daba309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346556"
---
# <a name="delegating-the-defining-of-permissions-in-script"></a><span data-ttu-id="fe1a2-103">Delega della definizione di autorizzazioni nello script</span><span class="sxs-lookup"><span data-stu-id="fe1a2-103">Delegating the Defining of Permissions in Script</span></span>

<span data-ttu-id="fe1a2-104">È possibile delegare l'amministrazione degli archivi dei criteri di autorizzazione archiviati in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fe1a2-104">You can delegate the administration of authorization policy stores that are stored in Active Directory.</span></span> <span data-ttu-id="fe1a2-105">L'amministrazione può essere delegata a utenti e gruppi a livello di punto vendita, applicazione o ambito.</span><span class="sxs-lookup"><span data-stu-id="fe1a2-105">Administration can be delegated to users and groups at the store, application, or scope level.</span></span>

<span data-ttu-id="fe1a2-106">A ogni livello è disponibile un elenco di amministratori e lettori.</span><span class="sxs-lookup"><span data-stu-id="fe1a2-106">At each level, there is a list of administrators and readers.</span></span> <span data-ttu-id="fe1a2-107">Gli amministratori di un archivio, di un'applicazione o di un ambito possono leggere e modificare l'archivio criteri a livello delegato.</span><span class="sxs-lookup"><span data-stu-id="fe1a2-107">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="fe1a2-108">I lettori possono leggere l'archivio criteri a livello delegato, ma non modificare l'archivio.</span><span class="sxs-lookup"><span data-stu-id="fe1a2-108">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

<span data-ttu-id="fe1a2-109">Un utente o un gruppo che sia un amministratore o un lettore di un'applicazione deve essere aggiunto anche come utente delegato dell'archivio criteri che contiene tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="fe1a2-109">A user or group that is either an administrator or a reader of an application must also be added as a delegated user of the policy store that contains that application.</span></span> <span data-ttu-id="fe1a2-110">Analogamente, un utente o un gruppo che è un amministratore o un lettore di un ambito deve essere aggiunto come utente delegato dell'applicazione che contiene tale ambito.</span><span class="sxs-lookup"><span data-stu-id="fe1a2-110">Similarly, a user or group that is an administrator or a reader of a scope must be added as a delegated user of the application that contains that scope.</span></span>

<span data-ttu-id="fe1a2-111">**Per delegare l'amministrazione di un ambito**</span><span class="sxs-lookup"><span data-stu-id="fe1a2-111">**To delegate administration of a scope**</span></span>

1.  <span data-ttu-id="fe1a2-112">Aggiungere l'utente o il gruppo all'elenco di utenti delegati dell'archivio che contiene l'ambito chiamando il metodo [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) dell'oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che contiene l'ambito.</span><span class="sxs-lookup"><span data-stu-id="fe1a2-112">Add the user or group to the list of delegated users of the store that contains the scope by calling the [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) method of the [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that contains the scope.</span></span>
2.  <span data-ttu-id="fe1a2-113">Aggiungere l'utente o il gruppo all'elenco di utenti delegati dell'applicazione che contiene l'ambito chiamando il metodo [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) dell'oggetto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) che contiene l'ambito.</span><span class="sxs-lookup"><span data-stu-id="fe1a2-113">Add the user or group to the list of delegated users of the application that contains the scope by calling the [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) method of the [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object that contains the scope.</span></span>
3.  <span data-ttu-id="fe1a2-114">Aggiungere l'utente o il gruppo all'elenco di amministratori dell'ambito chiamando il metodo [**AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) dell'oggetto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .</span><span class="sxs-lookup"><span data-stu-id="fe1a2-114">Add the user or group to the list of administrators of the scope by calling the [**AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) method of the [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

> [!Note]  
> <span data-ttu-id="fe1a2-115">Gli archivi criteri basati su XML non supportano la delega a qualsiasi livello.</span><span class="sxs-lookup"><span data-stu-id="fe1a2-115">XML-based policy stores do not support delegation at any level.</span></span>

 

<span data-ttu-id="fe1a2-116">Se un ambito all'interno di un archivio autorizzazioni archiviato in Active Directory contiene definizioni di attività che includono regole di autorizzazione o definizioni di ruolo che includono regole di autorizzazione, l'ambito non può essere delegato.</span><span class="sxs-lookup"><span data-stu-id="fe1a2-116">If a scope within an authorization store that is stored in Active Directory contains task definitions that include authorization rules or role definitions that include authorization rules, the scope cannot be delegated.</span></span>

<span data-ttu-id="fe1a2-117">Nell'esempio seguente viene illustrato come delegare l'amministrazione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fe1a2-117">The following example shows how to delegate administration of an application.</span></span> <span data-ttu-id="fe1a2-118">Nell'esempio si presuppone che esista un archivio dei criteri di autorizzazione Active Directory esistente nel percorso specificato, che l'archivio dei criteri contenga un'applicazione denominata Expense e che l'applicazione non contenga attività con script delle regole business.</span><span class="sxs-lookup"><span data-stu-id="fe1a2-118">The example assumes that there is an existing Active Directory authorization policy store at the specified location, that this policy store contains an application named Expense, and that this application contains no tasks with business rule scripts.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, _
    "msldap://CN=MyStore,CN=Program Data,DC=authmanager,DC=com"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Add a delegated policy user to the store.
AzManStore.AddDelegatedPolicyUserName("ExampleDomain\\UserName")

'  Add the user as an administrator of the application.
expenseApp.AddPolicyAdministratorName("ExampleDomain\\UserName")

'  Save changes to the store.
AzManStore.Submit
```



 

 



