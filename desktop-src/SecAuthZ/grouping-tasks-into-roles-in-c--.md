---
description: In Gestione autorizzazioni, un ruolo rappresenta una categoria di utenti e le attività che gli utenti sono autorizzati a eseguire.
ms.assetid: d2671c52-8d34-45e2-9c49-4ed399f3c220
title: Raggruppamento di attività in ruoli in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb4952d9ece250ddfacc53d955bce3a107281a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317058"
---
# <a name="grouping-tasks-into-roles-in-c"></a>Raggruppamento di attività in ruoli in C++

In Gestione autorizzazioni, un ruolo rappresenta una categoria di utenti e le attività che gli utenti sono autorizzati a eseguire. Le attività vengono raggruppate e assegnate a una definizione di ruolo, rappresentata da un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) con la proprietà [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) impostata su **true**. La definizione del ruolo può quindi essere assegnata a un oggetto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) e gli utenti o i gruppi di utenti vengono quindi assegnati a tale oggetto. Per ulteriori informazioni sulle attività e sui ruoli, vedere [ruoli](roles.md).

Nell'esempio seguente viene illustrato come assegnare attività a una definizione di ruolo, creare un oggetto Role e assegnare la definizione di ruolo all'oggetto Role. Nell'esempio si presuppone che esista un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C, che questo archivio contiene un'applicazione denominata Expense e che l'applicazione contenga attività denominate Invia spese e approva spese.


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
    IAzTask* pTaskRoleDef = NULL;
    IAzRole* pRole = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR taskNameSubmit = NULL;
    BSTR taskNameApprove = NULL;
    BSTR roleDefName = NULL;
    BSTR roleName = NULL;
    
    
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

    //  Allocate a string for the name of the policy store.
    storeName = SysAllocString(L"msxml://c:\\myStore.xml");
    if (!storeName)
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    appName = SysAllocString(L"Expense");
    if (!appName)
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Allocate strings for the task names.
    taskNameSubmit = SysAllocString(L"Submit Expense");
    if (!taskNameSubmit)
        MyHandleError("Could not allocate first task name string.");
    
    taskNameApprove = SysAllocString(L"Approve Expense");
    if (!taskNameApprove)
        MyHandleError("Could not allocate second task name string.");

    //  Create a third task object to act as a role definition.
    roleDefName = SysAllocString(L"Expense Admin");
    if (!roleDefName)
        MyHandleError("Could not allocate role definition name.");
    hr = pApp->CreateTask(roleDefName, myVar, &pTaskRoleDef);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create role definition.");

    //  Set the IsRoleDefinition property of pTaskRoleDef to TRUE.
    hr = pTaskRoleDef->put_IsRoleDefinition(true);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not set role definition property.");

    //  Add two tasks to the role definition.
    hr = pTaskRoleDef->AddTask(taskNameSubmit, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add submit task.");
    hr = pTaskRoleDef->AddTask(taskNameApprove, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add approve task.");

    //  Save information to the store.
    hr = pTaskRoleDef->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save task data to the store.");

    //  Create an IAzRole object.
    roleName = SysAllocString(L"Expense Administrator");
    if (!roleName)
        MyHandleError("Could not allocate role name.");
    hr = pApp->CreateRole(roleName, myVar, &pRole);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create a role object.");

    //  Add the role definition to the role object.
    hr = pRole->AddTask(roleDefName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could add role definition to the role.");

    //  Save information to the store.
    hr = pRole->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save role data to the store.");

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pTaskRoleDef->Release();
    pRole->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(taskNameSubmit);
    SysFreeString(taskNameApprove);
    SysFreeString(roleDefName);
    SysFreeString(roleName);
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



 

 



