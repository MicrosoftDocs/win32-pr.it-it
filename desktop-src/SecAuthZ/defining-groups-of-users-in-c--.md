---
description: In Gestione autorizzazioni un oggetto IAzApplicationGroup rappresenta un gruppo di utenti. I ruoli possono quindi essere assegnati collettivamente a questo gruppo di utenti.
ms.assetid: 13950da1-b04f-4346-b216-9713cbdcd5b5
title: Definizione di gruppi di utenti in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fde349dcf5a877490d85917247cf7fba3480143d87d92afb1b8eb2017030e71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914037"
---
# <a name="defining-groups-of-users-in-c"></a>Definizione di gruppi di utenti in C++

In Gestione autorizzazioni un [**oggetto IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) rappresenta un gruppo di utenti. I ruoli possono quindi essere assegnati collettivamente a questo gruppo di utenti. Un [**oggetto IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) può includere anche altri **oggetti IAzApplicationGroup** come membri. Per altre informazioni sui gruppi di applicazioni, vedere [Utenti e gruppi.](users-and-groups.md)

Un gruppo può essere definito da elenchi espliciti di membri e non membri o da una query [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP). Gli esempi seguenti illustrano come creare ogni tipo di gruppo di applicazioni:

-   [Creazione di un gruppo di base](#creating-a-basic-group)
-   [Creazione di un gruppo di query LDAP](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a>Creazione di un gruppo di base

Un gruppo di applicazioni di base viene definito dai membri inclusi nelle proprietà [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) e [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) dell'oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) che rappresenta il gruppo. Gli utenti e  i gruppi elencati nella proprietà Membri sono inclusi nel gruppo di applicazioni e gli utenti e i gruppi elencati nella proprietà **NonMembers** vengono esclusi dal gruppo di applicazioni. L'elenco nella **proprietà NonMembers** sostituisce l'elenco nella **proprietà Members.**

Nell'esempio seguente viene illustrato come creare un gruppo di applicazioni di base e aggiungere tutti gli utenti locali come membri di tale gruppo. Nell'esempio si presuppone che sia presente un archivio criteri XML esistente denominato MyStore.xml nella directory radice dell'unità C.


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
    IAzApplicationGroup* pAppGroup = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR groupName = NULL;
    BSTR sidString = NULL;

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

    //  Create an application group object.
    if (!(groupName = SysAllocString(L"Trusted Users")))
        MyHandleError("Could not allocate group name string");
    hr = pStore->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Add well-known SID for all local users to the group.
    if (!(sidString = SysAllocString(L"S-1-2-0")))
        MyHandleError("Could not allocate SID string name");
    hr = pAppGroup->AddMember(sidString, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add member to group");

    //  Save changes to the store.
    pAppGroup->Submit(0, myVar);

    //  Clean up resources.
    pStore->Release();
    pAppGroup->Release();
    SysFreeString(storeName);
    SysFreeString(groupName);
    SysFreeString(sidString);
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



## <a name="creating-an-ldap-query-group"></a>Creazione di un gruppo di query LDAP

Un gruppo di query LDAP ha un'appartenenza definita dalla query contenuta nel valore della [**relativa proprietà LdapQuery.**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery)

L'esempio seguente illustra come creare un gruppo di applicazioni di query LDAP e aggiungere tutti gli utenti come membri di tale gruppo. Nell'esempio si presuppone che sia presente un archivio criteri XML esistente denominato MyStore.xml nella directory radice dell'unità C.


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
    IAzApplicationGroup* pAppGroup = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR groupName = NULL;
    BSTR ldapString = NULL;

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

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application group object.
    if (!(groupName = SysAllocString(L"Trusted Users3")))
        MyHandleError("Could not allocate group name string");
    hr = pStore->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Set the Type property to AZ_GROUPTYPE_LDAP_QUERY.
    hr = pAppGroup->put_Type(AZ_GROUPTYPE_LDAP_QUERY);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Error changing type to LDAP query");

    //  Add LDAP query for all users.
    if (!(ldapString =
   SysAllocString(L"(&(objectCategory=person)(objectClass=user))")))
        MyHandleError("Could not allocate LDAP query string");
    hr = pAppGroup->put_LdapQuery(ldapString);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add query to group");

    //  Save changes to the store.
    hr = pAppGroup->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save changes to store.");

    //  Clean up resources.
    pStore->Release();
    pAppGroup->Release();
    SysFreeString(storeName);
    SysFreeString(groupName);
    SysFreeString(ldapString);
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



 

 
