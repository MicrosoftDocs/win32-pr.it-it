---
description: Gli archivi di criteri di autorizzazione archiviati in Active Directory supportano la delega dell'amministrazione.
ms.assetid: ccad4c19-7a16-4599-9a42-23cae7084418
title: Delega della definizione delle autorizzazioni in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f79202a3f8ee21934f890d3c5a66a19be4466fa2b1ecdfe31672a4edfc2319e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782055"
---
# <a name="delegating-the-defining-of-permissions-in-c"></a>Delega della definizione delle autorizzazioni in C++

Gli archivi di criteri di autorizzazione archiviati in Active Directory supportano la delega dell'amministrazione. L'amministrazione può essere delegata a utenti e gruppi a livello di archivio, applicazione o ambito.

A ogni livello è disponibile un elenco di amministratori e lettori. Gli amministratori di un archivio, di un'applicazione o di un ambito possono leggere e modificare l'archivio criteri a livello delegato. I lettori possono leggere l'archivio criteri a livello delegato, ma non possono modificare l'archivio.

Un utente o un gruppo che sia un amministratore o un lettore di un'applicazione deve anche essere aggiunto come utente delegato dell'archivio criteri che contiene l'applicazione. Analogamente, un utente o un gruppo che è un amministratore o un lettore di un ambito deve essere aggiunto come utente delegato dell'applicazione che contiene tale ambito.

Ad esempio, per delegare l'amministrazione di un ambito, aggiungere prima di tutto l'utente o il gruppo all'elenco di utenti delegati dell'archivio che contiene l'ambito chiamando il metodo [**IAzAuthorizationStore::AddDelegatedPolicyUser.**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) Aggiungere quindi l'utente o il gruppo all'elenco di utenti delegati dell'applicazione che contiene l'ambito chiamando il [**metodo IAzApplication::AddDelegatedPolicyUser.**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) Infine, aggiungere l'utente o il gruppo all'elenco di amministratori dell'ambito chiamando il metodo [**IAzScope::AddPolicyAdministrator.**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator)

Gli archivi criteri basati su XML non supportano la delega a nessun livello.

Un ambito all'interno di un archivio autorizzazioni archiviato in Active Directory non può essere delegato se l'ambito contiene definizioni di attività che includono regole di autorizzazione o definizioni di ruolo che includono regole di autorizzazione.

Nell'esempio seguente viene illustrato come delegare l'amministrazione di un'applicazione. Nell'esempio si presuppone che sia presente un archivio criteri di autorizzazione di Active Directory esistente nel percorso specificato, che questo archivio di criteri contenga un'applicazione denominata Expense e che questa applicazione non contenga attività con script delle regole business.


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void)
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR userName = NULL;
    VARIANT myVar;
    
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
    
    //  Create null VARIANT for parameters.
    myVar.vt = VT_NULL;

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize
   (AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Add a delegated policy user to the store.
    if (!(userName = SysAllocString(L"ExampleDomain\\UserName")))
        MyHandleError("Could not allocate username string.");
    hr = pStore->AddDelegatedPolicyUserName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError
   ("Could not add user to store as delegated policy user.");

    //  Add the user as an administrator of the application.
    hr = pApp->AddPolicyAdministratorName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError
   ("Could not add user to application as administrator.");

    

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(userName);
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



 

 



