---
description: Un archivio dei criteri di autorizzazione contiene informazioni sui criteri di sicurezza di un'applicazione o di un gruppo di applicazioni.
ms.assetid: bce85da8-11de-4bc1-b097-d8efdbd28abf
title: Creazione di un oggetto archivio criteri di autorizzazione nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 409a22df52d2914cd205700afccfc7a59f19031d924a921b5f2e5101621a895a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782196"
---
# <a name="creating-an-authorization-policy-store-object-in-script"></a>Creazione di un oggetto archivio criteri di autorizzazione nello script

Un archivio dei criteri di autorizzazione contiene informazioni sui criteri di sicurezza di un'applicazione o di un gruppo di applicazioni. Le informazioni includono le applicazioni, le operazioni, le attività, gli utenti e i gruppi di utenti associati all'archivio. Quando un'applicazione che usa Gestione autorizzazioni viene inizializzata, carica queste informazioni dall'archivio. L'archivio dei criteri di autorizzazione deve trovarsi in un sistema attendibile perché gli amministratori di tale sistema dispongono di un elevato livello di accesso all'archivio.

Gestione autorizzazioni supporta l'archiviazione dei criteri di autorizzazione nel servizio directory Active Directory o in un file XML, come illustrato negli esempi seguenti. Nell'API di Gestione autorizzazioni un archivio dei criteri di autorizzazione è rappresentato da un [**oggetto AzAuthorizationStore.**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) Gli esempi illustrano come creare un **oggetto AzAuthorizationStore** per un archivio di Active Directory e un archivio XML.

-   [Creazione di un archivio di Active Directory](#creating-an-active-directory-store)
-   [Creazione di un SQL Server Store](#creating-a-sql-server-store)
-   [Creazione di un archivio XML](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Creazione di un archivio di Active Directory

Per utilizzare Active Directory per archiviare i criteri di autorizzazione, il dominio deve essere nel Windows di funzionalità del dominio di **Server 2003.** L'archivio dei criteri di autorizzazione non può trovarsi in **un contesto di denominazione non** di dominio (detto anche partizione applicativa). È consigliabile che l'archivio si trovi nel contenitore **Program Data** in una nuova unità organizzativa creata in modo specifico per l'archivio dei criteri di autorizzazione. È inoltre consigliabile che l'archivio si trovi nella stessa rete locale dei server applicazioni che eseguono applicazioni che usano l'archivio.

L'esempio seguente illustra come creare un [**oggetto AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio criteri di autorizzazione in Active Directory. Nell'esempio si presuppone che sia presente un'unità organizzativa di Active Directory denominata Program Data in un dominio denominato authmanager.com.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _
    "msldap://CN=MyStore, CN=Program Data,DC=authmanager,DC=com"

'  Save the information to the store.
authStore.Submit
```



## <a name="creating-a-sql-server-store"></a>Creazione di un SQL Server Store

Gestione autorizzazioni supporta la creazione di un Microsoft SQL Server di criteri di autorizzazione basato su criteri. Per creare un archivio SQL Server autorizzazioni basato su , usare un URL che inizia con il **prefisso MSSQL://**. L'URL deve contenere SQL stringa di connessione, un nome di database e il nome dell'archivio dei criteri di autorizzazione: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.

Se l'istanza SQL Server non contiene il database di Gestione autorizzazioni specificato, Gestione autorizzazioni crea un nuovo database con tale nome.

> [!Note]  
> Le connessioni a un archivio SQL Server non vengono crittografate a meno che non si sia impostata in modo esplicito la crittografia SQL per la connessione o non si sia impostata la crittografia del traffico di rete che usa IPsec (Internet Protocol Security).

 

L'esempio seguente illustra come creare un [**oggetto AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio criteri di autorizzazione in un database SQL Server.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _ 
  "MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore"

'  Save information to the store.
authStore.Submit
```



## <a name="creating-an-xml-store"></a>Creazione di un archivio XML

Gestione autorizzazioni supporta la creazione di un archivio criteri di autorizzazione in formato XML. L'archivio XML può trovarsi nello stesso computer in cui viene eseguita l'applicazione oppure può essere archiviato in modalità remota. La modifica diretta del file XML non è supportata. Usare lo snap-in MMC Gestione autorizzazioni o l'API di Gestione autorizzazioni per modificare l'archivio criteri.

Gestione autorizzazioni non supporta la delega dell'amministrazione di un archivio criteri XML. Per informazioni sulla delega, vedere [Delega della definizione delle autorizzazioni nello script](delegating-the-defining-of-permissions-in-script.md).

L'esempio seguente illustra come creare un [**oggetto AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio dei criteri di autorizzazione in un file XML.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 



