---
description: Chiamare il metodo AccessCheck dell'interfaccia IAzClientContext per verificare se il client ha accesso a una o più operazioni.
ms.assetid: 7c8a63c5-2eab-4414-9a3d-c99a92b67a62
title: Verifica dell'accesso client a una risorsa richiesta in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeffe9cb3312e33a283c1701b58356cdf5ea9b3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234010"
---
# <a name="verifying-client-access-to-a-requested-resource-in-c"></a><span data-ttu-id="42f76-103">Verifica dell'accesso client a una risorsa richiesta in C++</span><span class="sxs-lookup"><span data-stu-id="42f76-103">Verifying Client Access to a Requested Resource in C++</span></span>

<span data-ttu-id="42f76-104">Chiamare il metodo [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) dell'interfaccia [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) per verificare se il client ha accesso a una o più operazioni.</span><span class="sxs-lookup"><span data-stu-id="42f76-104">Call the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of the [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) interface to check if the client has access to one or more operations.</span></span> <span data-ttu-id="42f76-105">Un client potrebbe appartenere a più di un ruolo e un'operazione potrebbe essere assegnata a più di un'attività, in modo che Gestione autorizzazioni verifichi tutti i ruoli e le attività.</span><span class="sxs-lookup"><span data-stu-id="42f76-105">A client might have membership in more than one role, and an operation might be assigned to more than one task, so Authorization Manager checks for all roles and tasks.</span></span> <span data-ttu-id="42f76-106">Se un ruolo a cui appartiene il client contiene un'attività che contiene un'operazione, viene concesso l'accesso a tale operazione.</span><span class="sxs-lookup"><span data-stu-id="42f76-106">If any role to which the client belongs contains any task that contains an operation, access to that operation is granted.</span></span>

<span data-ttu-id="42f76-107">Per controllare l'accesso solo a un singolo ruolo a cui appartiene il client, impostare la proprietà [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) dell'interfaccia [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="42f76-107">To check access for only a single role to which the client belongs, set the [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) property of the [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) interface.</span></span>

<span data-ttu-id="42f76-108">Quando si inizializza l'archivio dei criteri di autorizzazione per il controllo dell'accesso, è necessario passare zero come valore del parametro *è* del metodo [**IAzAuthorizationStore:: Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) .</span><span class="sxs-lookup"><span data-stu-id="42f76-108">When initializing the authorization policy store for access check, you must pass zero as the value of the *lFlags* parameter of the [**IAzAuthorizationStore::Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) method.</span></span>

<span data-ttu-id="42f76-109">Nell'esempio seguente viene illustrato come controllare l'accesso di un client a un'operazione.</span><span class="sxs-lookup"><span data-stu-id="42f76-109">The following example shows how to check a client's access to an operation.</span></span> <span data-ttu-id="42f76-110">Nell'esempio si presuppone che esista un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C, che questo archivio contiene un'applicazione denominata Expense e un'operazione denominata UseFormControl e che la variabile hToken contiene un token client valido.</span><span class="sxs-lookup"><span data-stu-id="42f76-110">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense and an operation named UseFormControl, and that the variable hToken contains a valid client token.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <azroles.h>

void CheckAccess(ULONGLONG hToken)
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzClientContext* pClientContext = NULL;
    IAzOperation* pOperation = NULL;
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR operationName = NULL;
    BSTR objectName = NULL;
    LONG operationID;
    HRESULT hr;
    VARIANT varOperationIdArray;
    VARIANT varOperationId;
    VARIANT varResultsArray;
    VARIANT varResult;
    void MyHandleError(char *s);

    VARIANT myVar;
    VariantInit(&myVar);//.vt) = VT_NULL;

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

    //  Allocate a string for the  policy store.
    if(!(storeName = SysAllocString(L"msxml://c:\\myStore.xml")))
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

    //  Set up parameters for access check.

    //  Set up the object name.
    if (!(operationName = SysAllocString(L"UseFormControl")))
        MyHandleError("Could not allocate operation name string.");

    //  Get the ID of the operation to check.
    hr = pApp->OpenOperation(operationName, myVar, &pOperation);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open operation.");

    hr = pOperation->get_OperationID(&operationID);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not get operation ID.");

    //  Create a SAFEARRAY for the operation ID.
    varOperationIdArray.parray = SafeArrayCreateVector(VT_VARIANT, 0, 1);

    //  Set SAFEARRAY type.
    varOperationIdArray.vt = VT_ARRAY | VT_VARIANT;

    //  Create an array of indexes.
    LONG* index = new LONG[1];
    index[0] = 0;

    //  Populate a SAFEARRAY with the operation ID.
    varOperationId.vt = VT_I4;
    varOperationId.lVal = operationID;

    hr = SafeArrayPutElement(varOperationIdArray.parray, index,
   &varOperationId);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not put operation ID in array.");

    if(!(objectName = SysAllocString(L"UseFormControl")))//used for audit
        MyHandleError("Could not allocate object name string.");

    //  Check access.
    hr = pClientContext->AccessCheck(
        objectName,
        myVar,
        varOperationIdArray,
        myVar,               // use default application scope
        myVar,
        myVar,
        myVar,
        myVar,
        &varResultsArray);

    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not complete access check.");

    hr = SafeArrayGetElement(varResultsArray.parray, index, &varResult);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not get result from array.");

    if (varResult.lVal == 0)
        printf("Access granted.\n");
    else
        printf("Access denied.\n");
    

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pClientContext->Release();
    pOperation->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(operationName);
    SysFreeString(objectName);
    VariantClear(&myVar);
    VariantClear(&varOperationIdArray);
    VariantClear(&varOperationId);
    VariantClear(&varResultsArray);
    VariantClear(&varResult); 
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



 

 



