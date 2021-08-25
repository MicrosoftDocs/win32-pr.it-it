---
description: Chiamare il metodo AccessCheck dell'interfaccia IAzClientContext per verificare se il client ha accesso a una o più operazioni.
ms.assetid: 7c8a63c5-2eab-4414-9a3d-c99a92b67a62
title: Verifica dell'accesso client a una risorsa richiesta in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363490e3636f5ad5229dd4234eba3bf38b9dfc54a4564bda775b143a249fe640
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906731"
---
# <a name="verifying-client-access-to-a-requested-resource-in-c"></a>Verifica dell'accesso client a una risorsa richiesta in C++

Chiamare il [**metodo AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) dell'interfaccia [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) per verificare se il client ha accesso a una o più operazioni. Un client potrebbe essere membro di più di un ruolo e un'operazione potrebbe essere assegnata a più di un'attività, quindi Gestione autorizzazioni controlla tutti i ruoli e le attività. Se un ruolo a cui appartiene il client contiene un'attività che contiene un'operazione, viene concesso l'accesso a tale operazione.

Per controllare l'accesso per un solo ruolo a cui appartiene il client, impostare la [**proprietà RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) [**dell'interfaccia IAzClientContext.**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext)

Quando si inizializza l'archivio dei criteri di autorizzazione per il controllo di accesso, è necessario passare zero come valore del parametro *lFlags* del [**metodo IAzAuthorizationStore::Initialize.**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize)

Nell'esempio seguente viene illustrato come controllare l'accesso di un client a un'operazione. Nell'esempio si presuppone che nella directory radice dell'unità C sia presente un archivio criteri XML denominato MyStore.xml, che questo archivio contenga un'applicazione denominata Expense e un'operazione denominata UseFormControl e che la variabile hToken contenga un token client valido.


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



 

 



