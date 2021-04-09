---
description: I ruoli servono due scopi diversi in Gestione autorizzazioni.
ms.assetid: 6d045ecb-432e-4ba6-b5d2-37db82ab1884
title: Ruoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65d140faa22c72d098c7a4ba2f13e952b2713f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879662"
---
# <a name="roles"></a><span data-ttu-id="36645-103">Ruoli</span><span class="sxs-lookup"><span data-stu-id="36645-103">Roles</span></span>

<span data-ttu-id="36645-104">I ruoli servono due scopi diversi in Gestione autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="36645-104">Roles serve two different purposes in Authorization Manager.</span></span> <span data-ttu-id="36645-105">Un ruolo è un set di attività o operazioni a cui una categoria di utenti richiede l'accesso ed è anche un set di utenti e gruppi che rientrano in tale categoria.</span><span class="sxs-lookup"><span data-stu-id="36645-105">A role is a set of tasks or operations to which a category of users requires access, and it is also a set of users and groups that fit into that category.</span></span>

-   [<span data-ttu-id="36645-106">Ruoli come set di attività</span><span class="sxs-lookup"><span data-stu-id="36645-106">Roles as Sets of Tasks</span></span>](#roles-as-sets-of-tasks)
-   [<span data-ttu-id="36645-107">Ruoli come set di utenti e gruppi</span><span class="sxs-lookup"><span data-stu-id="36645-107">Roles as Sets of Users and Groups</span></span>](#roles-as-sets-of-users-and-groups)
-   [<span data-ttu-id="36645-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36645-108">Related topics</span></span>](#related-topics)

## <a name="roles-as-sets-of-tasks"></a><span data-ttu-id="36645-109">Ruoli come set di attività</span><span class="sxs-lookup"><span data-stu-id="36645-109">Roles as Sets of Tasks</span></span>

<span data-ttu-id="36645-110">Un criterio di autorizzazione assegna oggetti [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) a un oggetto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) per creare set di attività.</span><span class="sxs-lookup"><span data-stu-id="36645-110">An authorization policy assigns [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) objects to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object to create sets of tasks.</span></span> <span data-ttu-id="36645-111">Tutti gli utenti e i gruppi assegnati a tale oggetto **IAzRole** dispongono quindi dell'autorizzazione per accedere a tutte le operazioni contenute negli oggetti **IAzTask** .</span><span class="sxs-lookup"><span data-stu-id="36645-111">All users and groups assigned to that **IAzRole** object then have permission to access all operations contained by those **IAzTask** objects.</span></span>

<span data-ttu-id="36645-112">Poiché un oggetto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) rappresenta un set di attività e un set di utenti e gruppi che hanno accesso a tali attività, gestione autorizzazioni fornisce un modo per creare definizioni di ruolo che possono essere assegnate a più di un oggetto **IAzRole** .</span><span class="sxs-lookup"><span data-stu-id="36645-112">Because an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object represents both a set of tasks and a set of users and groups that have access to those tasks, Authorization Manager provides a way to create role definitions that can be assigned to more than one **IAzRole** object.</span></span> <span data-ttu-id="36645-113">Un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) può contenere altri oggetti **IAzTask** .</span><span class="sxs-lookup"><span data-stu-id="36645-113">An [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object can contain other **IAzTask** objects.</span></span> <span data-ttu-id="36645-114">È quindi possibile usare l'oggetto **IAzTask** come definizione di ruolo assegnando questo oggetto a uno o più oggetti **IAzRole** .</span><span class="sxs-lookup"><span data-stu-id="36645-114">You can then use that **IAzTask** object as a role definition by assigning it to one or more **IAzRole** objects.</span></span> <span data-ttu-id="36645-115">Impostare la proprietà [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) dell'oggetto **IAzTask** su **true** per fare in modo che l'interfaccia utente dello snap-in MMC di **Gestione autorizzazioni** visualizzi l'oggetto **IAzTask** come ruolo.</span><span class="sxs-lookup"><span data-stu-id="36645-115">Set the [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property of the **IAzTask** object to **TRUE** to cause the **Authorization Manager** MMC snap-in user interface to display the **IAzTask** object as a role.</span></span>

## <a name="roles-as-sets-of-users-and-groups"></a><span data-ttu-id="36645-116">Ruoli come set di utenti e gruppi</span><span class="sxs-lookup"><span data-stu-id="36645-116">Roles as Sets of Users and Groups</span></span>

<span data-ttu-id="36645-117">Assegnare utenti e gruppi a un oggetto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) per concedere a tali utenti e gruppi l'accesso alle attività assegnate a tale oggetto **IAzRole** chiamando il metodo [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) o [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) .</span><span class="sxs-lookup"><span data-stu-id="36645-117">Assign users and groups to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object to grant those users and groups access to the tasks assigned to that **IAzRole** object by calling the [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) or [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) method.</span></span> <span data-ttu-id="36645-118">Assegnare i gruppi di applicazioni esistenti, rappresentati da oggetti [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) , a un oggetto **IAzRole** chiamando il metodo [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) .</span><span class="sxs-lookup"><span data-stu-id="36645-118">Assign existing application groups, represented by [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) objects, to an **IAzRole** object by calling the [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) method.</span></span> <span data-ttu-id="36645-119">Tutti gli utenti e i gruppi assegnati all'oggetto **IAzRole** hanno accesso alle attività e alle operazioni assegnate a tale ruolo.</span><span class="sxs-lookup"><span data-stu-id="36645-119">All users and groups assigned to the **IAzRole** object have access to the tasks and operations assigned to that role.</span></span> <span data-ttu-id="36645-120">Per ulteriori informazioni sui gruppi di applicazioni, vedere [utenti e gruppi](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="36645-120">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="36645-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36645-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36645-122">Raggruppamento di attività in ruoli in C++</span><span class="sxs-lookup"><span data-stu-id="36645-122">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[<span data-ttu-id="36645-123">Definizione di gruppi di utenti in C++</span><span class="sxs-lookup"><span data-stu-id="36645-123">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)
</dt> <dt>

[<span data-ttu-id="36645-124">Aggiunta di utenti a un gruppo di applicazioni in C++</span><span class="sxs-lookup"><span data-stu-id="36645-124">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



