---
description: Per stabilire un contesto client in C++, un'applicazione può creare un contesto client con un handle per un token, un dominio e un nome utente o una rappresentazione di stringa dell'ID di sicurezza del client.
ms.assetid: 765cd702-a1a8-4ff6-bea5-54de9fb62c0b
title: Creazione di un contesto client con gestione autorizzazioni in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79afa31db547b28d129c5b8e90dcf3e4ba1e91c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529388"
---
# <a name="establishing-a-client-context-with-authorization-manager-in-c"></a><span data-ttu-id="7b90a-103">Creazione di un contesto client con gestione autorizzazioni in C++</span><span class="sxs-lookup"><span data-stu-id="7b90a-103">Establishing a Client Context with Authorization Manager in C++</span></span>

<span data-ttu-id="7b90a-104">In Gestione autorizzazioni, un'applicazione determina se a un client viene concesso l'accesso a un'operazione chiamando il metodo [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) di un oggetto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) , che rappresenta un contesto client.</span><span class="sxs-lookup"><span data-stu-id="7b90a-104">In Authorization Manager, an application determines whether a client is given access to an operation by calling the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object, which represents a client context.</span></span>

<span data-ttu-id="7b90a-105">Un'applicazione può creare un contesto client con un handle per un token, un dominio e un nome utente o una rappresentazione di stringa dell' [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) del client.</span><span class="sxs-lookup"><span data-stu-id="7b90a-105">An application can create a client context with a handle to a token, a domain and user name, or a string representation of the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the client.</span></span>

<span data-ttu-id="7b90a-106">Usare i metodi [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)e [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) dell'interfaccia [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) per creare un contesto client.</span><span class="sxs-lookup"><span data-stu-id="7b90a-106">Use the [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname), and [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) methods of the [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) interface to create a client context.</span></span>

<span data-ttu-id="7b90a-107">Nell'esempio seguente viene illustrato come creare un oggetto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) da un token client.</span><span class="sxs-lookup"><span data-stu-id="7b90a-107">The following example shows how to create an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object from a client token.</span></span> <span data-ttu-id="7b90a-108">Nell'esempio si presuppone che esista un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C, che questo archivio contiene un'applicazione denominata Expense e che la variabile hToken contiene un token client valido.</span><span class="sxs-lookup"><span data-stu-id="7b90a-108">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that the variable hToken contains a valid client token.</span></span>


```C++
#include <windows.h>

void ExpenseCheck(ULONGLONG hToken)
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzClientContext* pClientContext = NULL;
    BSTR storeName = NULL;
    BSTR appName = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
 
 //  Create a null VARIANT for function parameters.
    VARIANT myVar;
    VariantInit(&myVar);

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

    //  Allocate a string for the policy store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(0, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Create a client context from a token handle.
    hr = pApp->InitializeClientContextFromToken(hToken, myVar,
                &pClientContext);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create client context.");

    //  Use the client context as needed.

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pClientContext->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    VariantClear(&myVar);
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



 

 
