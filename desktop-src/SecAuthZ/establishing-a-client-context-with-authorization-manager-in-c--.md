---
description: Per stabilire un contesto client in C++, un'applicazione può creare un contesto client con un handle per un token, un dominio e un nome utente o una rappresentazione di stringa dell'identificatore di sicurezza del client.
ms.assetid: 765cd702-a1a8-4ff6-bea5-54de9fb62c0b
title: Definizione di un contesto client con Gestione autorizzazioni in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1b74cab7d6c113f5120a682250f85dca772e1764acf432317049da27ec091d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672121"
---
# <a name="establishing-a-client-context-with-authorization-manager-in-c"></a>Definizione di un contesto client con Gestione autorizzazioni in C++

In Gestione autorizzazioni un'applicazione determina se a un client viene assegnato l'accesso a un'operazione chiamando il metodo [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) di un [**oggetto IAzClientContext,**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) che rappresenta un contesto client.

Un'applicazione può creare un contesto client con un handle per un token, un dominio e un nome utente o una rappresentazione di stringa dell'identificatore [*di*](/windows/desktop/SecGloss/s-gly) sicurezza (SID) del client.

Usare i [**metodi InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)e [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) dell'interfaccia [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) per creare un contesto client.

L'esempio seguente illustra come creare un [**oggetto IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) da un token client. L'esempio presuppone che nella directory radice dell'unità C sia presente un archivio criteri XML denominato MyStore.xml, che l'archivio contenga un'applicazione denominata Expense e che la variabile hToken contenga un token client valido.


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



 

 
