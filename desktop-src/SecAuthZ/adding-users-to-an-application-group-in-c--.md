---
description: In Gestione autorizzazioni, un gruppo di applicazioni è costituito da un gruppo di utenti e gruppi di utenti. Un gruppo di applicazioni può contenere altri gruppi di applicazioni, quindi i gruppi di utenti possono essere annidati.
ms.assetid: b01883d6-eae6-4f3a-b269-90c22827f116
title: Aggiunta di utenti a un gruppo di applicazioni in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7fa08ddd93ba1743a20e3eb14a5f62344741c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130423"
---
# <a name="adding-users-to-an-application-group-in-c"></a>Aggiunta di utenti a un gruppo di applicazioni in C++

In Gestione autorizzazioni, un gruppo di applicazioni è costituito da un gruppo di utenti e gruppi di utenti. Un gruppo di applicazioni può contenere altri gruppi di applicazioni, quindi i gruppi di utenti possono essere annidati. Un gruppo di applicazioni è rappresentato da un oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .

Per consentire ai membri di un gruppo di applicazioni di eseguire un'attività o un set di attività, assegnare tale gruppo di applicazioni a un ruolo che contiene tali attività. I ruoli sono rappresentati da oggetti [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) .

Nell'esempio seguente viene illustrato come creare un gruppo di applicazioni, aggiungere un utente come membro del gruppo di applicazioni e assegnare il gruppo di applicazioni a un ruolo esistente. Nell'esempio si presuppone che esista un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C, che questo archivio contiene un'applicazione denominata Expense e che l'applicazione contenga un ruolo denominato Expense Administrator.


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
    IAzApplicationGroup* pAppGroup = NULL;
    IAzRole* pRole = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR groupName = NULL;
    BSTR userName = NULL;
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

    //  Allocate a string for the group name.
    if (!(groupName = SysAllocString(L"Approvers")))
        MyHandleError("Could not allocate group name string.");

    //  Create an IAzApplicationGroup object.
    hr = pApp->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Add a member to the group.
 //  Replace with valid domain and user name.
    if (!(userName = SysAllocString(L"domain\\username")))
        MyHandleError("Could not allocate user name string.");

    hr = pAppGroup->AddMemberName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add user to application group.");

    //  Save information to the store.
    hr = pAppGroup->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save group information.");

    //  Open an IAzRole object.
    if (!(roleName = SysAllocString(L"Expense Administrator")))
        MyHandleError("Could not allocate role name string.");

    hr = pApp->OpenRole(roleName, myVar, &pRole);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open role object.");

    //  Add the group to the role.
    hr = pRole->AddAppMember(groupName, myVar);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not add the application group to the role.");


    //  Save information to the store.
    hr = pRole->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save role data to the store.");

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pAppGroup->Release();
    pRole->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(groupName);
    SysFreeString(roleName);
    SysFreeString(userName);
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



 

 



