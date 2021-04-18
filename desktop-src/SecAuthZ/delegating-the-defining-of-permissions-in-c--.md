---
description: Gli archivi dei criteri di autorizzazione archiviati in Active Directory supportano la delega dell'amministrazione.
ms.assetid: ccad4c19-7a16-4599-9a42-23cae7084418
title: Delega della definizione di autorizzazioni in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc299e3506300da1f0db2b4a9bacfce60def1c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315839"
---
# <a name="delegating-the-defining-of-permissions-in-c"></a><span data-ttu-id="4d5ec-103">Delega della definizione di autorizzazioni in C++</span><span class="sxs-lookup"><span data-stu-id="4d5ec-103">Delegating the Defining of Permissions in C++</span></span>

<span data-ttu-id="4d5ec-104">Gli archivi dei criteri di autorizzazione archiviati in Active Directory supportano la delega dell'amministrazione.</span><span class="sxs-lookup"><span data-stu-id="4d5ec-104">Authorization policy stores that are stored in Active Directory support delegation of administration.</span></span> <span data-ttu-id="4d5ec-105">L'amministrazione può essere delegata a utenti e gruppi a livello di punto vendita, applicazione o ambito.</span><span class="sxs-lookup"><span data-stu-id="4d5ec-105">Administration can be delegated to users and groups at the store, application, or scope level.</span></span>

<span data-ttu-id="4d5ec-106">A ogni livello è disponibile un elenco di amministratori e lettori.</span><span class="sxs-lookup"><span data-stu-id="4d5ec-106">At each level, there is a list of administrators and readers.</span></span> <span data-ttu-id="4d5ec-107">Gli amministratori di un archivio, di un'applicazione o di un ambito possono leggere e modificare l'archivio criteri a livello delegato.</span><span class="sxs-lookup"><span data-stu-id="4d5ec-107">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="4d5ec-108">I lettori possono leggere l'archivio criteri a livello delegato, ma non modificare l'archivio.</span><span class="sxs-lookup"><span data-stu-id="4d5ec-108">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

<span data-ttu-id="4d5ec-109">Un utente o un gruppo che sia un amministratore o un lettore di un'applicazione deve essere aggiunto anche come utente delegato dell'archivio criteri che contiene tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="4d5ec-109">A user or group that is either an administrator or a reader of an application must also be added as a delegated user of the policy store that contains that application.</span></span> <span data-ttu-id="4d5ec-110">Analogamente, un utente o un gruppo che è un amministratore o un lettore di un ambito deve essere aggiunto come utente delegato dell'applicazione che contiene tale ambito.</span><span class="sxs-lookup"><span data-stu-id="4d5ec-110">Similarly, a user or group that is an administrator or a reader of a scope must be added as a delegated user of the application that contains that scope.</span></span>

<span data-ttu-id="4d5ec-111">Per delegare l'amministrazione di un ambito, ad esempio, aggiungere innanzitutto l'utente o il gruppo all'elenco di utenti delegati dell'archivio che contiene l'ambito chiamando il metodo [**IAzAuthorizationStore:: AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) .</span><span class="sxs-lookup"><span data-stu-id="4d5ec-111">For example, to delegate administration of a scope, first add the user or group to the list of delegated users of the store that contains the scope by calling the [**IAzAuthorizationStore::AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) method.</span></span> <span data-ttu-id="4d5ec-112">Aggiungere quindi l'utente o il gruppo all'elenco di utenti delegati dell'applicazione che contiene l'ambito chiamando il metodo [**IAzApplication:: AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) .</span><span class="sxs-lookup"><span data-stu-id="4d5ec-112">Then add the user or group to the list of delegated users of the application that contains the scope by calling the [**IAzApplication::AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) method.</span></span> <span data-ttu-id="4d5ec-113">Infine, aggiungere l'utente o il gruppo all'elenco di amministratori dell'ambito chiamando il metodo [**IAzScope:: AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) .</span><span class="sxs-lookup"><span data-stu-id="4d5ec-113">Finally, add the user or group to the list of administrators of the scope by calling the [**IAzScope::AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) method.</span></span>

<span data-ttu-id="4d5ec-114">Gli archivi criteri basati su XML non supportano la delega a qualsiasi livello.</span><span class="sxs-lookup"><span data-stu-id="4d5ec-114">XML-based policy stores do not support delegation at any level.</span></span>

<span data-ttu-id="4d5ec-115">Non è possibile delegare un ambito all'interno di un archivio autorizzazioni archiviato in Active Directory se l'ambito contiene definizioni di attività che includono regole di autorizzazione o definizioni di ruolo che includono regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="4d5ec-115">A scope within an authorization store that is stored in Active Directory cannot be delegated if the scope contains task definitions that include authorization rules or role definitions that include authorization rules.</span></span>

<span data-ttu-id="4d5ec-116">Nell'esempio seguente viene illustrato come delegare l'amministrazione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4d5ec-116">The following example shows how to delegate administration of an application.</span></span> <span data-ttu-id="4d5ec-117">Nell'esempio si presuppone che esista un archivio dei criteri di autorizzazione Active Directory esistente nel percorso specificato, che l'archivio dei criteri contenga un'applicazione denominata Expense e che l'applicazione non contenga attività con script delle regole business.</span><span class="sxs-lookup"><span data-stu-id="4d5ec-117">The example assumes that there is an existing Active Directory authorization policy store at the specified location, that this policy store contains an application named Expense, and that this application contains no tasks with business rule scripts.</span></span>


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



 

 



