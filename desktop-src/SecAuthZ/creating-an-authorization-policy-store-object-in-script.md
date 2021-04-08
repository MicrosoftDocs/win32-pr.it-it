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
# <a name="creating-an-authorization-policy-store-object-in-script"></a><span data-ttu-id="72b80-103">Creazione di un oggetto archivio criteri di autorizzazione nello script</span><span class="sxs-lookup"><span data-stu-id="72b80-103">Creating an Authorization Policy Store Object in Script</span></span>

<span data-ttu-id="72b80-104">Un archivio dei criteri di autorizzazione contiene informazioni sui criteri di sicurezza di un'applicazione o di un gruppo di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="72b80-104">An authorization policy store contains information about the security policy of an application or group of applications.</span></span> <span data-ttu-id="72b80-105">Le informazioni includono le applicazioni, le operazioni, le attività, gli utenti e i gruppi di utenti associati allo Store.</span><span class="sxs-lookup"><span data-stu-id="72b80-105">The information includes the applications, operations, tasks, users, and groups of users associated with the store.</span></span> <span data-ttu-id="72b80-106">Quando un'applicazione che usa Gestione autorizzazioni Inizializza, carica queste informazioni dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="72b80-106">When an application that uses Authorization Manager initializes, it loads this information from the store.</span></span> <span data-ttu-id="72b80-107">L'archivio dei criteri di autorizzazione deve trovarsi in un sistema attendibile perché gli amministratori di tale sistema hanno un alto livello di accesso all'archivio.</span><span class="sxs-lookup"><span data-stu-id="72b80-107">The authorization policy store must be located on a trusted system because administrators on that system have a high degree of access to the store.</span></span>

<span data-ttu-id="72b80-108">Gestione autorizzazioni supporta l'archiviazione dei criteri di autorizzazione nel servizio directory Active Directory o in un file XML, come illustrato negli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="72b80-108">Authorization Manager supports storing authorization policy either in the Active Directory directory service or in an XML file as shown in the following examples.</span></span> <span data-ttu-id="72b80-109">Nell'API di gestione autorizzazioni, un archivio dei criteri di autorizzazione è rappresentato da un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="72b80-109">In the Authorization Manager API, an authorization policy store is represented by an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="72b80-110">Negli esempi viene illustrato come creare un oggetto **AzAuthorizationStore** per un archivio Active Directory e un archivio XML.</span><span class="sxs-lookup"><span data-stu-id="72b80-110">The examples show how to create an **AzAuthorizationStore** object for an Active Directory store and an XML store.</span></span>

-   [<span data-ttu-id="72b80-111">Creazione di un archivio Active Directory</span><span class="sxs-lookup"><span data-stu-id="72b80-111">Creating an Active Directory Store</span></span>](#creating-an-active-directory-store)
-   [<span data-ttu-id="72b80-112">Creazione di un archivio SQL Server</span><span class="sxs-lookup"><span data-stu-id="72b80-112">Creating a SQL Server Store</span></span>](#creating-a-sql-server-store)
-   [<span data-ttu-id="72b80-113">Creazione di un archivio XML</span><span class="sxs-lookup"><span data-stu-id="72b80-113">Creating an XML Store</span></span>](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a><span data-ttu-id="72b80-114">Creazione di un archivio Active Directory</span><span class="sxs-lookup"><span data-stu-id="72b80-114">Creating an Active Directory Store</span></span>

<span data-ttu-id="72b80-115">Per usare Active Directory per archiviare i criteri di autorizzazione, il dominio deve essere nel livello di funzionalità del dominio di **Windows Server 2003** .</span><span class="sxs-lookup"><span data-stu-id="72b80-115">To use Active Directory to store the authorization policy, the domain must be in the **Windows Server 2003** domain functional level.</span></span> <span data-ttu-id="72b80-116">L'archivio dei criteri di autorizzazione non può trovarsi in un **contesto dei nomi non di dominio** (detto anche partizione applicativa).</span><span class="sxs-lookup"><span data-stu-id="72b80-116">The authorization policy store cannot be located in a **Non-Domain Naming Context** (also called an application partition).</span></span> <span data-ttu-id="72b80-117">È consigliabile che l'archivio si trovi nel contenitore di **dati del programma** in una nuova unità organizzativa creata in modo specifico per l'archivio dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="72b80-117">It is recommended that the store be located in the **Program Data** container under a new organizational unit created specifically for the authorization policy store.</span></span> <span data-ttu-id="72b80-118">È inoltre consigliabile che l'archivio si trovi all'interno della stessa rete locale dei server applicazioni che eseguono applicazioni che utilizzano lo Store.</span><span class="sxs-lookup"><span data-stu-id="72b80-118">It is also recommended that the store be located within the same local area network as application servers that run applications that use the store.</span></span>

<span data-ttu-id="72b80-119">Nell'esempio seguente viene illustrato come creare un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio dei criteri di autorizzazione in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="72b80-119">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in Active Directory.</span></span> <span data-ttu-id="72b80-120">Nell'esempio si presuppone l'esistenza di un'unità organizzativa Active Directory denominata dati del programma in un dominio denominato authmanager.com.</span><span class="sxs-lookup"><span data-stu-id="72b80-120">The example assumes that there is an existing Active Directory organizational unit named Program Data in a domain named authmanager.com.</span></span>


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



## <a name="creating-a-sql-server-store"></a><span data-ttu-id="72b80-121">Creazione di un archivio SQL Server</span><span class="sxs-lookup"><span data-stu-id="72b80-121">Creating a SQL Server Store</span></span>

<span data-ttu-id="72b80-122">Gestione autorizzazioni supporta la creazione di un archivio criteri di autorizzazione basato su Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="72b80-122">Authorization Manager supports creating a Microsoft SQL Server–based authorization policy store.</span></span> <span data-ttu-id="72b80-123">Per creare un archivio autorizzazioni basato su SQL Server, usare un URL che inizia con il prefisso **MSSQL://**.</span><span class="sxs-lookup"><span data-stu-id="72b80-123">To create a SQL Server–based authorization store, use a URL that begins with the prefix **MSSQL://**.</span></span> <span data-ttu-id="72b80-124">L'URL deve contenere una stringa di connessione SQL valida, un nome di database e il nome dell'archivio dei criteri di autorizzazione: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.</span><span class="sxs-lookup"><span data-stu-id="72b80-124">The URL must contain a valid SQL connection string, a database name, and the name of the authorization policy store: **MSSQL://**_ConnectionString_*_/_*_DatabaseName_*_/_*_PolicyStoreName_.</span></span>

<span data-ttu-id="72b80-125">Se l'istanza di SQL Server non contiene il database di gestione autorizzazioni specificato, gestione autorizzazioni Crea un nuovo database con tale nome.</span><span class="sxs-lookup"><span data-stu-id="72b80-125">If the instance of SQL Server does not contain the specified Authorization Manager database, Authorization Manager creates a new database with that name.</span></span>

> [!Note]  
> <span data-ttu-id="72b80-126">Le connessioni a un archivio SQL Server non vengono crittografate a meno che non si configurano in modo esplicito la crittografia SQL per la connessione o si configura la crittografia del traffico di rete che utilizza IPsec (Internet Protocol Security).</span><span class="sxs-lookup"><span data-stu-id="72b80-126">Connections to a SQL Server store are not encrypted unless you explicitly set up SQL encryption for the connection or set up encryption of the network traffic that uses Internet Protocol Security (IPsec).</span></span>

 

<span data-ttu-id="72b80-127">Nell'esempio seguente viene illustrato come creare un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio criteri di autorizzazione in un database SQL Server.</span><span class="sxs-lookup"><span data-stu-id="72b80-127">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in a SQL Server database.</span></span>


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



## <a name="creating-an-xml-store"></a><span data-ttu-id="72b80-128">Creazione di un archivio XML</span><span class="sxs-lookup"><span data-stu-id="72b80-128">Creating an XML Store</span></span>

<span data-ttu-id="72b80-129">Gestione autorizzazioni supporta la creazione di un archivio criteri di autorizzazione in formato XML.</span><span class="sxs-lookup"><span data-stu-id="72b80-129">Authorization Manager supports creating an authorization policy store in XML format.</span></span> <span data-ttu-id="72b80-130">L'archivio XML può trovarsi nello stesso computer in cui viene eseguita l'applicazione oppure può essere archiviato in remoto.</span><span class="sxs-lookup"><span data-stu-id="72b80-130">The XML store can be located on the same computer where the application runs, or it can be stored remotely.</span></span> <span data-ttu-id="72b80-131">La modifica diretta del file XML non è supportata.</span><span class="sxs-lookup"><span data-stu-id="72b80-131">Editing the XML file directly is not supported.</span></span> <span data-ttu-id="72b80-132">Utilizzare lo snap-in MMC Gestione autorizzazioni o l'API di gestione autorizzazioni per modificare l'archivio criteri.</span><span class="sxs-lookup"><span data-stu-id="72b80-132">Use the Authorization Manager MMC snap-in or the Authorization Manager API to edit the policy store.</span></span>

<span data-ttu-id="72b80-133">Gestione autorizzazioni non supporta la delega dell'amministrazione di un archivio criteri XML.</span><span class="sxs-lookup"><span data-stu-id="72b80-133">Authorization Manager does not support delegating administration of an XML policy store.</span></span> <span data-ttu-id="72b80-134">Per informazioni sulla delega, vedere [delega della definizione di autorizzazioni nello script](delegating-the-defining-of-permissions-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="72b80-134">For information about delegation, see [Delegating the Defining of Permissions in Script](delegating-the-defining-of-permissions-in-script.md).</span></span>

<span data-ttu-id="72b80-135">Nell'esempio seguente viene illustrato come creare un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio criteri di autorizzazione in un file XML.</span><span class="sxs-lookup"><span data-stu-id="72b80-135">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in an XML file.</span></span>


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 



