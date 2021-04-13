---
description: Un oggetto IAzApplicationGroup rappresenta un gruppo di utenti. I ruoli possono quindi essere assegnati a questo gruppo di utenti collettivamente. Un oggetto IAzApplicationGroup può includere anche altri oggetti IAzApplicationGroup come membri.
ms.assetid: 8b445419-7316-4034-b742-a05845af1862
title: Definizione di gruppi di utenti nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f0b652530167c71fbea7bc23d27434ae458f9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348936"
---
# <a name="defining-groups-of-users-in-script"></a><span data-ttu-id="e511b-105">Definizione di gruppi di utenti nello script</span><span class="sxs-lookup"><span data-stu-id="e511b-105">Defining Groups of Users in Script</span></span>

<span data-ttu-id="e511b-106">In Gestione autorizzazioni, un oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) rappresenta un gruppo di utenti.</span><span class="sxs-lookup"><span data-stu-id="e511b-106">In Authorization Manager, an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="e511b-107">I ruoli possono quindi essere assegnati a questo gruppo di utenti collettivamente.</span><span class="sxs-lookup"><span data-stu-id="e511b-107">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="e511b-108">Un oggetto **IAzApplicationGroup** può includere anche altri oggetti **IAzApplicationGroup** come membri.</span><span class="sxs-lookup"><span data-stu-id="e511b-108">An **IAzApplicationGroup** object can also include other **IAzApplicationGroup** objects as members.</span></span> <span data-ttu-id="e511b-109">Per ulteriori informazioni sui gruppi di applicazioni, vedere [utenti e gruppi](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="e511b-109">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

<span data-ttu-id="e511b-110">Un gruppo può essere definito da elenchi espliciti di membri e non membri o da una query LDAP ( [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) ).</span><span class="sxs-lookup"><span data-stu-id="e511b-110">A group can be defined either by explicit lists of members and nonmembers or by a [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP) query.</span></span> <span data-ttu-id="e511b-111">Negli esempi seguenti viene illustrato come creare ogni tipo di gruppo di applicazioni:</span><span class="sxs-lookup"><span data-stu-id="e511b-111">The following examples show how to create each type of application group:</span></span>

-   [<span data-ttu-id="e511b-112">Creazione di un gruppo di base</span><span class="sxs-lookup"><span data-stu-id="e511b-112">Creating a Basic Group</span></span>](#creating-a-basic-group)
-   [<span data-ttu-id="e511b-113">Creazione di un gruppo di query LDAP</span><span class="sxs-lookup"><span data-stu-id="e511b-113">Creating an LDAP Query Group</span></span>](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a><span data-ttu-id="e511b-114">Creazione di un gruppo di base</span><span class="sxs-lookup"><span data-stu-id="e511b-114">Creating a Basic Group</span></span>

<span data-ttu-id="e511b-115">Un gruppo di applicazioni di base viene definito dai membri inclusi nelle proprietà [**membri**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) e non [**membri**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) dell'oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) che rappresenta il gruppo.</span><span class="sxs-lookup"><span data-stu-id="e511b-115">A basic application group is defined by the members included in the [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) and [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) properties of the [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object that represents the group.</span></span> <span data-ttu-id="e511b-116">Gli utenti e i gruppi elencati nella proprietà **membri** sono inclusi nel gruppo di applicazioni e gli utenti e i gruppi elencati nella proprietà non **membri** vengono esclusi dal gruppo di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e511b-116">Users and groups listed in the **Members** property are included in the application group, and users and groups listed in the **NonMembers** property are excluded from the application group.</span></span> <span data-ttu-id="e511b-117">L'elenco nella proprietà non **Members** sostituisce l'elenco nella proprietà **Members** .</span><span class="sxs-lookup"><span data-stu-id="e511b-117">Being listed in the **NonMembers** property supersedes being listed in the **Members** property.</span></span>

<span data-ttu-id="e511b-118">Nell'esempio seguente viene illustrato come creare un gruppo di applicazioni di base e come aggiungere tutti gli utenti locali come membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="e511b-118">The following example shows how to create a basic application group and add all local users as members of that group.</span></span> <span data-ttu-id="e511b-119">Nell'esempio si presuppone l'esistenza di un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C.</span><span class="sxs-lookup"><span data-stu-id="e511b-119">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Trusted Users")

'  Add a well-known SID for all local users to the group.
appGroup.AddMember("S-1-1-0")

'  Save the application group to the store.
appGroup.Submit
```



## <a name="creating-an-ldap-query-group"></a><span data-ttu-id="e511b-120">Creazione di un gruppo di query LDAP</span><span class="sxs-lookup"><span data-stu-id="e511b-120">Creating an LDAP Query Group</span></span>

<span data-ttu-id="e511b-121">Un gruppo di query LDAP ha un'appartenenza definita dalla query contenuta nel valore della relativa proprietà [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) .</span><span class="sxs-lookup"><span data-stu-id="e511b-121">An LDAP query group has a membership defined by the query contained in the value of its [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) property.</span></span>

<span data-ttu-id="e511b-122">Nell'esempio seguente viene illustrato come creare un gruppo di applicazioni di query LDAP e come aggiungere tutti gli utenti come membri di tale gruppo.</span><span class="sxs-lookup"><span data-stu-id="e511b-122">The following example shows how to create an LDAP query application group and add all users as members of that group.</span></span> <span data-ttu-id="e511b-123">Nell'esempio si presuppone l'esistenza di un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C.</span><span class="sxs-lookup"><span data-stu-id="e511b-123">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("LDAP Trusted Users")

'  Set the Type property of the group to two
'  (AZ_GROUPTYPE_LDAP_QUERY).
appGroup.Type = 2

'  Add LDAP query for all users.
appGroup.LdapQuery = ("&(objectCategory=person)(objectClass=user)")

'  Save the application group to the store.
appGroup.Submit

```



 

 
