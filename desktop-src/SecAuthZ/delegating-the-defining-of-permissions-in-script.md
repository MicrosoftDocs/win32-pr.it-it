---
description: È possibile delegare l'amministrazione degli archivi dei criteri di autorizzazione archiviati in Active Directory.
ms.assetid: a7b43dfe-f03e-4795-bbd3-746eb3449fd0
title: Delega della definizione delle autorizzazioni nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69cf0793a48a572ec4b37cbf3634f65b04ff3565f3205bf0380c68914abb4530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782065"
---
# <a name="delegating-the-defining-of-permissions-in-script"></a>Delega della definizione delle autorizzazioni nello script

È possibile delegare l'amministrazione degli archivi dei criteri di autorizzazione archiviati in Active Directory. L'amministrazione può essere delegata a utenti e gruppi a livello di archivio, applicazione o ambito.

A ogni livello è disponibile un elenco di amministratori e lettori. Gli amministratori di un archivio, di un'applicazione o di un ambito possono leggere e modificare l'archivio criteri a livello delegato. I lettori possono leggere l'archivio criteri a livello delegato, ma non possono modificare l'archivio.

Un utente o un gruppo che sia un amministratore o un lettore di un'applicazione deve anche essere aggiunto come utente delegato dell'archivio criteri che contiene l'applicazione. Analogamente, un utente o un gruppo che è un amministratore o un lettore di un ambito deve essere aggiunto come utente delegato dell'applicazione che contiene tale ambito.

**Per delegare l'amministrazione di un ambito**

1.  Aggiungere l'utente o il gruppo all'elenco di utenti delegati dell'archivio che contiene l'ambito chiamando il metodo [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) [**dell'oggetto AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che contiene l'ambito.
2.  Aggiungere l'utente o il gruppo all'elenco di utenti delegati dell'applicazione che contiene l'ambito chiamando il [**metodo AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) dell'oggetto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) che contiene l'ambito.
3.  Aggiungere l'utente o il gruppo all'elenco di amministratori dell'ambito chiamando il [**metodo AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) dell'oggetto [**IAzScope.**](/windows/desktop/api/Azroles/nn-azroles-iazscope)

> [!Note]  
> Gli archivi criteri basati su XML non supportano la delega a nessun livello.

 

Se un ambito all'interno di un archivio autorizzazioni archiviato in Active Directory contiene definizioni di attività che includono regole di autorizzazione o definizioni di ruolo che includono regole di autorizzazione, l'ambito non può essere delegato.

Nell'esempio seguente viene illustrato come delegare l'amministrazione di un'applicazione. Nell'esempio si presuppone che sia presente un archivio criteri di autorizzazione di Active Directory esistente nel percorso specificato, che questo archivio di criteri contenga un'applicazione denominata Expense e che questa applicazione non contenga attività con script delle regole business.


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



 

 



