---
description: Un archivio dei criteri di autorizzazione contiene informazioni sui criteri di sicurezza di un'applicazione o di un gruppo di applicazioni. Le informazioni includono le applicazioni, le operazioni, le attività, gli utenti e i gruppi di utenti associati allo Store.
ms.assetid: 6fc84944-8050-4000-8856-36558d94e2fd
title: Creazione di un oggetto archivio criteri di autorizzazione in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b50bfa4234f5adaf162b1499f85785a7d65f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966967"
---
# <a name="creating-an-authorization-policy-store-object-in-c"></a><span data-ttu-id="2a771-104">Creazione di un oggetto archivio criteri di autorizzazione in C++</span><span class="sxs-lookup"><span data-stu-id="2a771-104">Creating an Authorization Policy Store Object in C++</span></span>

<span data-ttu-id="2a771-105">Un archivio dei criteri di autorizzazione contiene informazioni sui criteri di sicurezza di un'applicazione o di un gruppo di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2a771-105">An authorization policy store contains information about the security policy of an application or group of applications.</span></span> <span data-ttu-id="2a771-106">Le informazioni includono le applicazioni, le operazioni, le attività, gli utenti e i gruppi di utenti associati allo Store.</span><span class="sxs-lookup"><span data-stu-id="2a771-106">The information includes the applications, operations, tasks, users, and groups of users associated with the store.</span></span> <span data-ttu-id="2a771-107">Quando un'applicazione che usa Gestione autorizzazioni Inizializza, carica queste informazioni dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="2a771-107">When an application that uses Authorization Manager initializes, it loads this information from the store.</span></span> <span data-ttu-id="2a771-108">L'archivio dei criteri di autorizzazione deve trovarsi in un sistema attendibile perché gli amministratori di tale sistema hanno un alto livello di accesso all'archivio.</span><span class="sxs-lookup"><span data-stu-id="2a771-108">The authorization policy store must be located on a trusted system because administrators on that system have a high degree of access to the store.</span></span>

<span data-ttu-id="2a771-109">Gestione autorizzazioni supporta l'archiviazione dei criteri di autorizzazione nel servizio directory Active Directory o in un file XML, come illustrato negli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a771-109">Authorization Manager supports storing authorization policy either in the Active Directory directory service or in an XML file as shown in the following examples.</span></span> <span data-ttu-id="2a771-110">Nell'API di gestione autorizzazioni, un archivio dei criteri di autorizzazione è rappresentato da un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="2a771-110">In the Authorization Manager API, an authorization policy store is represented by an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="2a771-111">Negli esempi viene illustrato come creare un oggetto **AzAuthorizationStore** per un archivio Active Directory e un archivio XML.</span><span class="sxs-lookup"><span data-stu-id="2a771-111">The examples show how to create an **AzAuthorizationStore** object for an Active Directory store and an XML store.</span></span>

-   [<span data-ttu-id="2a771-112">Creazione di un archivio Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a771-112">Creating an Active Directory Store</span></span>](#creating-an-active-directory-store)
-   [<span data-ttu-id="2a771-113">Creazione di un archivio SQL Server</span><span class="sxs-lookup"><span data-stu-id="2a771-113">Creating a SQL Server Store</span></span>](#creating-a-sql-server-store)
-   [<span data-ttu-id="2a771-114">Creazione di un archivio XML</span><span class="sxs-lookup"><span data-stu-id="2a771-114">Creating an XML Store</span></span>](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a><span data-ttu-id="2a771-115">Creazione di un archivio Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a771-115">Creating an Active Directory Store</span></span>

<span data-ttu-id="2a771-116">Per usare Active Directory per archiviare i criteri di autorizzazione, il dominio deve essere nel livello di funzionalità del dominio di **Windows Server 2003** .</span><span class="sxs-lookup"><span data-stu-id="2a771-116">To use Active Directory to store the authorization policy, the domain must be in the **Windows Server 2003** domain functional level.</span></span> <span data-ttu-id="2a771-117">L'archivio dei criteri di autorizzazione non può trovarsi in un **contesto dei nomi non di dominio** (detto anche partizione applicativa).</span><span class="sxs-lookup"><span data-stu-id="2a771-117">The authorization policy store cannot be located in a **Non-Domain Naming Context** (also called an application partition).</span></span> <span data-ttu-id="2a771-118">È consigliabile che l'archivio si trovi nel contenitore di **dati del programma** in una nuova unità organizzativa creata in modo specifico per l'archivio dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="2a771-118">It is recommended that the store be located in the **Program Data** container under a new organizational unit created specifically for the authorization policy store.</span></span> <span data-ttu-id="2a771-119">È inoltre consigliabile che l'archivio si trovi all'interno della stessa rete locale dei server applicazioni che eseguono applicazioni che utilizzano lo Store.</span><span class="sxs-lookup"><span data-stu-id="2a771-119">It is also recommended that the store be located within the same local area network as application servers that run applications that use the store.</span></span>

<span data-ttu-id="2a771-120">Nell'esempio seguente viene illustrato come creare un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio dei criteri di autorizzazione in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2a771-120">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in Active Directory.</span></span> <span data-ttu-id="2a771-121">Nell'esempio si presuppone l'esistenza di un'unità organizzativa Active Directory denominata dati del programma in un dominio denominato authmanager.com.</span><span class="sxs-lookup"><span data-stu-id="2a771-121">The example assumes that there is an existing Active Directory organizational unit named Program Data in a domain named authmanager.com.</span></span>


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    //  Create a null VARIANT for function parameters.
    VARIANT myVar;
    VariantInit(&myVar);

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in Active Directory. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    VariantClear(&myVar);
    SysFreeString(storeName);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



## <a name="creating-a-sql-server-store"></a><span data-ttu-id="2a771-122">Creazione di un archivio SQL Server</span><span class="sxs-lookup"><span data-stu-id="2a771-122">Creating a SQL Server Store</span></span>

<span data-ttu-id="2a771-123">Gestione autorizzazioni supporta la creazione di un archivio criteri di autorizzazione basato su Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2a771-123">Authorization Manager supports creating a Microsoft SQL Server–based authorization policy store.</span></span> <span data-ttu-id="2a771-124">Per creare un archivio autorizzazioni basato su SQL Server, usare un URL che inizia con il prefisso **MSSQL://**.</span><span class="sxs-lookup"><span data-stu-id="2a771-124">To create a SQL Server–based authorization store, use a URL that begins with the prefix **MSSQL://**.</span></span> <span data-ttu-id="2a771-125">L'URL deve contenere una stringa di connessione SQL valida, un nome di database e il nome dell'archivio dei criteri di autorizzazione: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.</span><span class="sxs-lookup"><span data-stu-id="2a771-125">The URL must contain a valid SQL connection string, a database name, and the name of the authorization policy store: **MSSQL://**_ConnectionString_*_/_*_DatabaseName_*_/_*_PolicyStoreName_.</span></span>

<span data-ttu-id="2a771-126">Se l'istanza di SQL Server non contiene il database di gestione autorizzazioni specificato, gestione autorizzazioni Crea un nuovo database con tale nome.</span><span class="sxs-lookup"><span data-stu-id="2a771-126">If the instance of SQL Server does not contain the specified Authorization Manager database, Authorization Manager creates a new database with that name.</span></span>

> [!Note]  
> <span data-ttu-id="2a771-127">Le connessioni a un archivio SQL Server non vengono crittografate a meno che non si configurano in modo esplicito la crittografia SQL per la connessione o si configura la crittografia del traffico di rete che utilizza IPsec (Internet Protocol Security).</span><span class="sxs-lookup"><span data-stu-id="2a771-127">Connections to a SQL Server store are not encrypted unless you explicitly set up SQL encryption for the connection or set up encryption of the network traffic that uses Internet Protocol Security (IPsec).</span></span>

 

<span data-ttu-id="2a771-128">Nell'esempio seguente viene illustrato come creare un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio criteri di autorizzazione in un database SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2a771-128">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in a SQL Server database.</span></span>


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    VARIANT myVar; 
    myVar.vt = VT_NULL;

    //  Allocate a string for the SQL Server store.
    if(!(storeName = SysAllocString
   (L"MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



## <a name="creating-an-xml-store"></a><span data-ttu-id="2a771-129">Creazione di un archivio XML</span><span class="sxs-lookup"><span data-stu-id="2a771-129">Creating an XML Store</span></span>

<span data-ttu-id="2a771-130">Gestione autorizzazioni supporta la creazione di un archivio criteri di autorizzazione in formato XML.</span><span class="sxs-lookup"><span data-stu-id="2a771-130">Authorization Manager supports creating an authorization policy store in XML format.</span></span> <span data-ttu-id="2a771-131">L'archivio XML può trovarsi nello stesso computer in cui viene eseguita l'applicazione oppure può essere archiviato in remoto.</span><span class="sxs-lookup"><span data-stu-id="2a771-131">The XML store can be located on the same computer where the application runs, or it can be stored remotely.</span></span> <span data-ttu-id="2a771-132">La modifica diretta del file XML non è supportata.</span><span class="sxs-lookup"><span data-stu-id="2a771-132">Editing the XML file directly is not supported.</span></span> <span data-ttu-id="2a771-133">Utilizzare lo snap-in MMC Gestione autorizzazioni o l'API di gestione autorizzazioni per modificare l'archivio criteri.</span><span class="sxs-lookup"><span data-stu-id="2a771-133">Use the Authorization Manager MMC snap-in or the Authorization Manager API to edit the policy store.</span></span>

<span data-ttu-id="2a771-134">Gestione autorizzazioni non supporta la delega dell'amministrazione di un archivio criteri XML.</span><span class="sxs-lookup"><span data-stu-id="2a771-134">Authorization Manager does not support delegating administration of an XML policy store.</span></span> <span data-ttu-id="2a771-135">Per informazioni sulla delega, vedere delegare [la definizione delle autorizzazioni in C++](delegating-the-defining-of-permissions-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="2a771-135">For information about delegation, see [Delegating the Defining of Permissions in C++](delegating-the-defining-of-permissions-in-c--.md).</span></span>

<span data-ttu-id="2a771-136">Nell'esempio seguente viene illustrato come creare un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio criteri di autorizzazione in un file XML.</span><span class="sxs-lookup"><span data-stu-id="2a771-136">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in an XML file.</span></span>


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    VARIANT myVar; 
    myVar.vt = VT_NULL;

    //  Allocate a string for the distinguished name of the XML store.
    if(!(storeName = SysAllocString(L"msxml://C:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in an XML file. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 



