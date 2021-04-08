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
ms.openlocfilehash: feb02c80408210b663524e2aa914852a853e80ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879893"
---
# <a name="creating-an-authorization-policy-store-object-in-script"></a>Creazione di un oggetto archivio criteri di autorizzazione nello script

Un archivio dei criteri di autorizzazione contiene informazioni sui criteri di sicurezza di un'applicazione o di un gruppo di applicazioni. Le informazioni includono le applicazioni, le operazioni, le attività, gli utenti e i gruppi di utenti associati allo Store. Quando un'applicazione che usa Gestione autorizzazioni Inizializza, carica queste informazioni dall'archivio. L'archivio dei criteri di autorizzazione deve trovarsi in un sistema attendibile perché gli amministratori di tale sistema hanno un alto livello di accesso all'archivio.

Gestione autorizzazioni supporta l'archiviazione dei criteri di autorizzazione nel servizio directory Active Directory o in un file XML, come illustrato negli esempi seguenti. Nell'API di gestione autorizzazioni, un archivio dei criteri di autorizzazione è rappresentato da un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) . Negli esempi viene illustrato come creare un oggetto **AzAuthorizationStore** per un archivio Active Directory e un archivio XML.

-   [Creazione di un archivio Active Directory](#creating-an-active-directory-store)
-   [Creazione di un archivio SQL Server](#creating-a-sql-server-store)
-   [Creazione di un archivio XML](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Creazione di un archivio Active Directory

Per usare Active Directory per archiviare i criteri di autorizzazione, il dominio deve essere nel livello di funzionalità del dominio di **Windows Server 2003** . L'archivio dei criteri di autorizzazione non può trovarsi in un **contesto dei nomi non di dominio** (detto anche partizione applicativa). È consigliabile che l'archivio si trovi nel contenitore di **dati del programma** in una nuova unità organizzativa creata in modo specifico per l'archivio dei criteri di autorizzazione. È inoltre consigliabile che l'archivio si trovi all'interno della stessa rete locale dei server applicazioni che eseguono applicazioni che utilizzano lo Store.

Nell'esempio seguente viene illustrato come creare un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio dei criteri di autorizzazione in Active Directory. Nell'esempio si presuppone l'esistenza di un'unità organizzativa Active Directory denominata dati del programma in un dominio denominato authmanager.com.


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



## <a name="creating-a-sql-server-store"></a>Creazione di un archivio SQL Server

Gestione autorizzazioni supporta la creazione di un archivio criteri di autorizzazione basato su Microsoft SQL Server. Per creare un archivio autorizzazioni basato su SQL Server, usare un URL che inizia con il prefisso **MSSQL://**. L'URL deve contenere una stringa di connessione SQL valida, un nome di database e il nome dell'archivio dei criteri di autorizzazione: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.

Se l'istanza di SQL Server non contiene il database di gestione autorizzazioni specificato, gestione autorizzazioni Crea un nuovo database con tale nome.

> [!Note]  
> Le connessioni a un archivio SQL Server non vengono crittografate a meno che non si configurano in modo esplicito la crittografia SQL per la connessione o si configura la crittografia del traffico di rete che utilizza IPsec (Internet Protocol Security).

 

Nell'esempio seguente viene illustrato come creare un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio criteri di autorizzazione in un database SQL Server.


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

Gestione autorizzazioni supporta la creazione di un archivio criteri di autorizzazione in formato XML. L'archivio XML può trovarsi nello stesso computer in cui viene eseguita l'applicazione oppure può essere archiviato in remoto. La modifica diretta del file XML non è supportata. Utilizzare lo snap-in MMC Gestione autorizzazioni o l'API di gestione autorizzazioni per modificare l'archivio criteri.

Gestione autorizzazioni non supporta la delega dell'amministrazione di un archivio criteri XML. Per informazioni sulla delega, vedere [delega della definizione di autorizzazioni nello script](delegating-the-defining-of-permissions-in-script.md).

Nell'esempio seguente viene illustrato come creare un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio criteri di autorizzazione in un file XML.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 



