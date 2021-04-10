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
# <a name="creating-an-authorization-policy-store-object-in-c"></a>Creazione di un oggetto archivio criteri di autorizzazione in C++

Un archivio dei criteri di autorizzazione contiene informazioni sui criteri di sicurezza di un'applicazione o di un gruppo di applicazioni. Le informazioni includono le applicazioni, le operazioni, le attività, gli utenti e i gruppi di utenti associati allo Store. Quando un'applicazione che usa Gestione autorizzazioni Inizializza, carica queste informazioni dall'archivio. L'archivio dei criteri di autorizzazione deve trovarsi in un sistema attendibile perché gli amministratori di tale sistema hanno un alto livello di accesso all'archivio.

Gestione autorizzazioni supporta l'archiviazione dei criteri di autorizzazione nel servizio directory Active Directory o in un file XML, come illustrato negli esempi seguenti. Nell'API di gestione autorizzazioni, un archivio dei criteri di autorizzazione è rappresentato da un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) . Negli esempi viene illustrato come creare un oggetto **AzAuthorizationStore** per un archivio Active Directory e un archivio XML.

-   [Creazione di un archivio Active Directory](#creating-an-active-directory-store)
-   [Creazione di un archivio SQL Server](#creating-a-sql-server-store)
-   [Creazione di un archivio XML](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Creazione di un archivio Active Directory

Per usare Active Directory per archiviare i criteri di autorizzazione, il dominio deve essere nel livello di funzionalità del dominio di **Windows Server 2003** . L'archivio dei criteri di autorizzazione non può trovarsi in un **contesto dei nomi non di dominio** (detto anche partizione applicativa). È consigliabile che l'archivio si trovi nel contenitore di **dati del programma** in una nuova unità organizzativa creata in modo specifico per l'archivio dei criteri di autorizzazione. È inoltre consigliabile che l'archivio si trovi all'interno della stessa rete locale dei server applicazioni che eseguono applicazioni che utilizzano lo Store.

Nell'esempio seguente viene illustrato come creare un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio dei criteri di autorizzazione in Active Directory. Nell'esempio si presuppone l'esistenza di un'unità organizzativa Active Directory denominata dati del programma in un dominio denominato authmanager.com.


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



## <a name="creating-a-sql-server-store"></a>Creazione di un archivio SQL Server

Gestione autorizzazioni supporta la creazione di un archivio criteri di autorizzazione basato su Microsoft SQL Server. Per creare un archivio autorizzazioni basato su SQL Server, usare un URL che inizia con il prefisso **MSSQL://**. L'URL deve contenere una stringa di connessione SQL valida, un nome di database e il nome dell'archivio dei criteri di autorizzazione: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.

Se l'istanza di SQL Server non contiene il database di gestione autorizzazioni specificato, gestione autorizzazioni Crea un nuovo database con tale nome.

> [!Note]  
> Le connessioni a un archivio SQL Server non vengono crittografate a meno che non si configurano in modo esplicito la crittografia SQL per la connessione o si configura la crittografia del traffico di rete che utilizza IPsec (Internet Protocol Security).

 

Nell'esempio seguente viene illustrato come creare un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio criteri di autorizzazione in un database SQL Server.


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



## <a name="creating-an-xml-store"></a>Creazione di un archivio XML

Gestione autorizzazioni supporta la creazione di un archivio criteri di autorizzazione in formato XML. L'archivio XML può trovarsi nello stesso computer in cui viene eseguita l'applicazione oppure può essere archiviato in remoto. La modifica diretta del file XML non è supportata. Utilizzare lo snap-in MMC Gestione autorizzazioni o l'API di gestione autorizzazioni per modificare l'archivio criteri.

Gestione autorizzazioni non supporta la delega dell'amministrazione di un archivio criteri XML. Per informazioni sulla delega, vedere delegare [la definizione delle autorizzazioni in C++](delegating-the-defining-of-permissions-in-c--.md).

Nell'esempio seguente viene illustrato come creare un oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) che rappresenta un archivio criteri di autorizzazione in un file XML.


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



 

 



