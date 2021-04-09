---
description: In Gestione autorizzazioni, un oggetto IAzApplicationGroup rappresenta un gruppo di utenti. I ruoli possono quindi essere assegnati a questo gruppo di utenti collettivamente.
ms.assetid: 13950da1-b04f-4346-b216-9713cbdcd5b5
title: Definizione di gruppi di utenti in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b4931d3b35658539284305e98096d7ecfc891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885085"
---
# <a name="defining-groups-of-users-in-c"></a><span data-ttu-id="775c8-104">Definizione di gruppi di utenti in C++</span><span class="sxs-lookup"><span data-stu-id="775c8-104">Defining Groups of Users in C++</span></span>

<span data-ttu-id="775c8-105">In Gestione autorizzazioni, un oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) rappresenta un gruppo di utenti.</span><span class="sxs-lookup"><span data-stu-id="775c8-105">In Authorization Manager, an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="775c8-106">I ruoli possono quindi essere assegnati a questo gruppo di utenti collettivamente.</span><span class="sxs-lookup"><span data-stu-id="775c8-106">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="775c8-107">Un oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) può includere anche altri oggetti **IAzApplicationGroup** come membri.</span><span class="sxs-lookup"><span data-stu-id="775c8-107">An [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object can also include other **IAzApplicationGroup** objects as members.</span></span> <span data-ttu-id="775c8-108">Per ulteriori informazioni sui gruppi di applicazioni, vedere [utenti e gruppi](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="775c8-108">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

<span data-ttu-id="775c8-109">Un gruppo può essere definito da elenchi espliciti di membri e non membri oppure da una query LDAP ( [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) ).</span><span class="sxs-lookup"><span data-stu-id="775c8-109">A group can be defined either by explicit lists of members and nonmembers, or by a [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP) query.</span></span> <span data-ttu-id="775c8-110">Negli esempi seguenti viene illustrato come creare ogni tipo di gruppo di applicazioni:</span><span class="sxs-lookup"><span data-stu-id="775c8-110">The following examples show how to create each type of application group:</span></span>

-   [<span data-ttu-id="775c8-111">Creazione di un gruppo di base</span><span class="sxs-lookup"><span data-stu-id="775c8-111">Creating a Basic Group</span></span>](#creating-a-basic-group)
-   [<span data-ttu-id="775c8-112">Creazione di un gruppo di query LDAP</span><span class="sxs-lookup"><span data-stu-id="775c8-112">Creating an LDAP Query Group</span></span>](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a><span data-ttu-id="775c8-113">Creazione di un gruppo di base</span><span class="sxs-lookup"><span data-stu-id="775c8-113">Creating a Basic Group</span></span>

<span data-ttu-id="775c8-114">Un gruppo di applicazioni di base viene definito dai membri inclusi nelle proprietà [**membri**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) e non [**membri**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) dell'oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) che rappresenta il gruppo.</span><span class="sxs-lookup"><span data-stu-id="775c8-114">A basic application group is defined by the members included in the [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) and [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) properties of the [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object that represents the group.</span></span> <span data-ttu-id="775c8-115">Gli utenti e i gruppi elencati nella proprietà **membri** sono inclusi nel gruppo di applicazioni e gli utenti e i gruppi elencati nella proprietà non **membri** vengono esclusi dal gruppo di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="775c8-115">Users and groups listed in the **Members** property are included in the application group, and users and groups listed in the **NonMembers** property are excluded from the application group.</span></span> <span data-ttu-id="775c8-116">L'elenco nella proprietà non **Members** sostituisce l'elenco nella proprietà **Members** .</span><span class="sxs-lookup"><span data-stu-id="775c8-116">Being listed in the **NonMembers** property supersedes being listed in the **Members** property.</span></span>

<span data-ttu-id="775c8-117">Nell'esempio seguente viene illustrato come creare un gruppo di applicazioni di base e come aggiungere tutti gli utenti locali come membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="775c8-117">The following example shows how to create a basic application group and add all local users as members of that group.</span></span> <span data-ttu-id="775c8-118">Nell'esempio si presuppone l'esistenza di un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C.</span><span class="sxs-lookup"><span data-stu-id="775c8-118">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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



## <a name="creating-an-ldap-query-group"></a><span data-ttu-id="775c8-119">Creazione di un gruppo di query LDAP</span><span class="sxs-lookup"><span data-stu-id="775c8-119">Creating an LDAP Query Group</span></span>

<span data-ttu-id="775c8-120">Un gruppo di query LDAP ha un'appartenenza definita dalla query contenuta nel valore della relativa proprietà [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) .</span><span class="sxs-lookup"><span data-stu-id="775c8-120">An LDAP query group has a membership defined by the query contained in the value of its [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) property.</span></span>

<span data-ttu-id="775c8-121">Nell'esempio seguente viene illustrato come creare un gruppo di applicazioni di query LDAP e come aggiungere tutti gli utenti come membri di tale gruppo.</span><span class="sxs-lookup"><span data-stu-id="775c8-121">The following example shows how to create an LDAP query application group and add all users as members of that group.</span></span> <span data-ttu-id="775c8-122">Nell'esempio si presuppone l'esistenza di un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C.</span><span class="sxs-lookup"><span data-stu-id="775c8-122">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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



 

 
