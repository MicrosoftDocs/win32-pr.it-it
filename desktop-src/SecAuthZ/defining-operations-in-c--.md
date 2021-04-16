---
description: In Gestione autorizzazioni un'operazione è una funzione o un metodo di basso livello di un'applicazione.
ms.assetid: 458c5418-94c5-4977-8203-f8299387c6da
title: Definizione di operazioni in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31431390d3c95dbf4248ffeebc63f29f1fa6757d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350581"
---
# <a name="defining-operations-in-c"></a>Definizione di operazioni in C++

In Gestione autorizzazioni un'operazione è una funzione o un metodo di basso livello di un'applicazione. Queste operazioni sono raggruppate come attività. Gli utenti dell'applicazione richiedono l'autorizzazione per completare le attività. Un'operazione è rappresentata da un oggetto [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) . Per ulteriori informazioni sulle operazioni, vedere [operazioni e attività](operations-and-tasks.md).

Nell'esempio seguente viene illustrato come definire le operazioni in un archivio dei criteri di autorizzazione. Nell'esempio si presuppone l'esistenza di un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C e che l'archivio contenga un'applicazione denominata Expense.


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif
#pragma comment(lib, "duser.lib")

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzOperation* pOp = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR opName = NULL;
    
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
    VARIANT myVar; 
    VariantInit(&myVar);

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Create operations.

    //  Create first operation.
    if (!(opName = SysAllocString(L"RetrieveForm")))
        MyHandleError("Could not allocate operation name string.");
    hr = pApp->CreateOperation(opName, myVar, &pOp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create operation.");
    
    //  Set the OperationID property.
    hr = pOp->put_OperationID(1);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not set operation ID.");

    //  Save the operation to the store.
    hr = pOp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save operation.");
    SysFreeString(opName);

    //  Create second operation.
    if (!(opName = SysAllocString(L"EnqueRequest")))
        MyHandleError("Could not allocate operation name string.");
    hr = pApp->CreateOperation(opName, myVar, &pOp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create operation.");

    //  Set the OperationID property.
    hr = pOp->put_OperationID(2);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not set operation ID.");

    //  Save the operation to the store.
    hr = pOp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save operation.");
    SysFreeString(opName);

    //  Create third operation.
    if (!(opName = SysAllocString(L"DequeRequest")))
        MyHandleError("Could not allocate operation name string.");
    hr = pApp->CreateOperation(opName, myVar, &pOp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create operation.");

    //  Set the OperationID property.
    hr = pOp->put_OperationID(3);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not set operation ID.");

    //  Save the operation to the store.
    hr = pOp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save operation.");
    SysFreeString(opName);

    //  Create fourth operation.
    if (!(opName = SysAllocString(L"UseFormControl")))
        MyHandleError("Could not allocate operation name string.");
    hr = pApp->CreateOperation(opName, myVar, &pOp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create operation.");

    //  Set the OperationID property.
    hr = pOp->put_OperationID(4);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not set operation ID.");

    //  Save the operation to the store.
    hr = pOp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save operation.");
    SysFreeString(opName);

    //  Create fifth operation.
    if (!(opName = SysAllocString(L"MarkFormApproved")))
        MyHandleError("Could not allocate operation name string.");
    hr = pApp->CreateOperation(opName, myVar, &pOp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create operation.");

    //  Set the OperationID property.
    hr = pOp->put_OperationID(5);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not set operation ID.");

    //  Save the operation to the store.
    hr = pOp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save operation.");
    SysFreeString(opName);

    //  Create sixth operation.
    if (!(opName = SysAllocString(L"SendApprovalNotify")))
        MyHandleError("Could not allocate operation name string.");
    hr = pApp->CreateOperation(opName, myVar, &pOp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create operation.");

    //  Set the OperationID property.
    hr = pOp->put_OperationID(6);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not set operation ID.");

    //  Save the operation to the store.
    hr = pOp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save operation.");
    SysFreeString(opName);

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pOp->Release();
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



 

 



