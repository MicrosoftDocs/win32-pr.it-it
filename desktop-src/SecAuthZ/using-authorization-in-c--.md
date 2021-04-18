---
description: Usare l'API di gestione autorizzazioni per controllare l'accesso alle risorse dell'applicazione.
ms.assetid: 2485056c-b860-4247-9e7b-0157ca85d05d
title: Utilizzo dell'autorizzazione in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6771d16748d3c04680b545a83e382fa3d5ce78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315424"
---
# <a name="using-authorization-in-c"></a><span data-ttu-id="c1afb-103">Utilizzo dell'autorizzazione in C++</span><span class="sxs-lookup"><span data-stu-id="c1afb-103">Using Authorization in C++</span></span>

<span data-ttu-id="c1afb-104">È possibile utilizzare l'API di gestione autorizzazioni per controllare l'accesso alle risorse dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c1afb-104">You can use the Authorization Manager API to control access to application resources.</span></span>

<span data-ttu-id="c1afb-105">Se si dispone di una soluzione di controllo degli accessi esistente basata sugli [*elenchi di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) e si vuole evitare di convertire questa soluzione per l'uso di gestione autorizzazioni, è possibile continuare a usare gli ACL per controllare l'accesso alle risorse.</span><span class="sxs-lookup"><span data-stu-id="c1afb-105">If you have an existing access control solution based on [*access control lists*](/windows/desktop/SecGloss/a-gly) (ACLs) and want to avoid converting this solution to use Authorization Manager, you can continue to use ACLs to control access to resources.</span></span> <span data-ttu-id="c1afb-106">Per informazioni sul controllo dell'accesso alle risorse tramite gli ACL, vedere [definizione delle autorizzazioni con ACL in c++](defining-permissions-with-acls-in-c--.md), [creazione di un contesto client da un SID in c++](establishing-a-client-context-from-a-sid-in-c--.md)e [Verifica dell'accesso client con ACL in c++](verifying-client-access-with-acls-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="c1afb-106">For information about controlling access to resources using ACLs, see [Defining Permissions with ACLs in C++](defining-permissions-with-acls-in-c--.md), [Establishing a Client Context from a SID in C++](establishing-a-client-context-from-a-sid-in-c--.md), and [Verifying Client Access with ACLs in C++](verifying-client-access-with-acls-in-c--.md).</span></span>

> [!Note]  
> <span data-ttu-id="c1afb-107">Per le aziende di grandi dimensioni, esiste un compromesso tra il sovraccarico amministrativo e le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="c1afb-107">For large enterprises, there is a trade-off between administrative overhead and performance.</span></span> <span data-ttu-id="c1afb-108">Con l'aumentare del numero di risorse e utenti protetti, l'amministrazione degli ACL diventa più complessa.</span><span class="sxs-lookup"><span data-stu-id="c1afb-108">As the number of secured resources and users increases, the administration of ACLs becomes more complicated.</span></span> <span data-ttu-id="c1afb-109">Le prestazioni non vengono compromesse perché tutte le informazioni necessarie sui diritti di accesso vengono distribuite alle risorse protette.</span><span class="sxs-lookup"><span data-stu-id="c1afb-109">Performance is not affected because all required information about access rights is distributed to the secured resources.</span></span> <span data-ttu-id="c1afb-110">Le prestazioni di gestione autorizzazioni sono influenzate dalla scalabilità.</span><span class="sxs-lookup"><span data-stu-id="c1afb-110">The performance of Authorization Manager is affected by scaling.</span></span>

 

<span data-ttu-id="c1afb-111">Per informazioni sulle altre attività di autorizzazione, vedere [supporto di attività per l'autorizzazione in C++](supporting-tasks-for-authorization-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="c1afb-111">For information about other authorization tasks, see [Supporting Tasks for Authorization in C++](supporting-tasks-for-authorization-in-c--.md).</span></span>



| <span data-ttu-id="c1afb-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="c1afb-112">Topic</span></span>                                                                                                                | <span data-ttu-id="c1afb-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1afb-113">Description</span></span>                                                                                              |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1afb-114">Definizione delle autorizzazioni in C++</span><span class="sxs-lookup"><span data-stu-id="c1afb-114">Defining Permissions in C++</span></span>](defining-permissions-in-c--.md)                                                       | <span data-ttu-id="c1afb-115">Definire gli utenti che possono accedere alle risorse dell'applicazione creando un archivio dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="c1afb-115">Define which users have access to which application resources by creating an authorization policy store.</span></span> |
| [<span data-ttu-id="c1afb-116">Verifica dell'accesso client a una risorsa richiesta in C++</span><span class="sxs-lookup"><span data-stu-id="c1afb-116">Verifying Client Access to a Requested Resource in C++</span></span>](verifying-client-access-to-a-requested-resource-in-c--.md) | <span data-ttu-id="c1afb-117">Controllare se il client ha accesso a una o più operazioni.</span><span class="sxs-lookup"><span data-stu-id="c1afb-117">Check whether the client has access to one or more operations.</span></span>                                           |
| [<span data-ttu-id="c1afb-118">Delega della definizione di autorizzazioni in C++</span><span class="sxs-lookup"><span data-stu-id="c1afb-118">Delegating the Defining of Permissions in C++</span></span>](delegating-the-defining-of-permissions-in-c--.md)                   | <span data-ttu-id="c1afb-119">Delegare l'amministrazione degli archivi dei criteri di autorizzazione archiviati in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c1afb-119">Delegate the administration of authorization policy stores that are stored in Active Directory.</span></span>          |



 

 

 
