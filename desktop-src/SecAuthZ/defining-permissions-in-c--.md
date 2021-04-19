---
description: Istruzioni per l'uso dell'API di gestione autorizzazioni per definire le autorizzazioni in C++ creando un archivio dei criteri di autorizzazione.
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: Definizione delle autorizzazioni in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc398d811f44b69dbde8d30f135fd4f30a552bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319918"
---
# <a name="defining-permissions-in-c"></a><span data-ttu-id="6d967-103">Definizione delle autorizzazioni in C++</span><span class="sxs-lookup"><span data-stu-id="6d967-103">Defining Permissions in C++</span></span>

<span data-ttu-id="6d967-104">In Gestione autorizzazioni è possibile definire quali utenti hanno accesso alle risorse dell'applicazione creando un archivio criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="6d967-104">In Authorization Manager, you define which users have access to which application resources by creating an authorization policy store.</span></span>

<span data-ttu-id="6d967-105">Per informazioni sulla definizione delle autorizzazioni con ACL, vedere [definizione delle autorizzazioni con ACL in C++](defining-permissions-with-acls-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="6d967-105">For information about defining permissions with ACLs, see [Defining Permissions with ACLs in C++](defining-permissions-with-acls-in-c--.md).</span></span>

<span data-ttu-id="6d967-106">**Per definire le autorizzazioni di accesso**</span><span class="sxs-lookup"><span data-stu-id="6d967-106">**To define access permissions**</span></span>

1.  <span data-ttu-id="6d967-107">Creare l'archivio in cui sono definiti i criteri di autorizzazione:</span><span class="sxs-lookup"><span data-stu-id="6d967-107">Create the store where the authorization policy is defined:</span></span><dl>

[<span data-ttu-id="6d967-108">Creazione di un oggetto archivio criteri di autorizzazione in C++</span><span class="sxs-lookup"><span data-stu-id="6d967-108">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  <span data-ttu-id="6d967-109">Creare una sezione nell'archivio dei criteri di autorizzazione per un'applicazione specifica:</span><span class="sxs-lookup"><span data-stu-id="6d967-109">Create a section in the authorization policy store for a specific application:</span></span><dl>

[<span data-ttu-id="6d967-110">Creazione di un oggetto applicazione in C++</span><span class="sxs-lookup"><span data-stu-id="6d967-110">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)  
    </dl>
3.  <span data-ttu-id="6d967-111">Definire le operazioni implementate dall'applicazione per accedere alle risorse e modificarle:</span><span class="sxs-lookup"><span data-stu-id="6d967-111">Define operations that the application implements to access and modify resources:</span></span><dl>

[<span data-ttu-id="6d967-112">Definizione di operazioni in C++</span><span class="sxs-lookup"><span data-stu-id="6d967-112">Defining Operations in C++</span></span>](defining-operations-in-c--.md)  
    </dl>
4.  <span data-ttu-id="6d967-113">Raggruppare le operazioni in attività di alto livello che gli utenti desiderano eseguire:</span><span class="sxs-lookup"><span data-stu-id="6d967-113">Group operations into high-level tasks that users want to perform:</span></span><dl>

[<span data-ttu-id="6d967-114">Raggruppamento di operazioni in attività in C++</span><span class="sxs-lookup"><span data-stu-id="6d967-114">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  <span data-ttu-id="6d967-115">Definire i ruoli che sono costituiti da gruppi di attività:</span><span class="sxs-lookup"><span data-stu-id="6d967-115">Define roles that consist of groups of tasks:</span></span><dl>

[<span data-ttu-id="6d967-116">Raggruppamento di attività in ruoli in C++</span><span class="sxs-lookup"><span data-stu-id="6d967-116">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)  
    </dl><span data-ttu-id="6d967-117">Un utente assegnato a un ruolo dispone dell'autorizzazione per eseguire tutte le attività assegnate a tale ruolo.</span><span class="sxs-lookup"><span data-stu-id="6d967-117">A user that is assigned to a role has permission to perform any task assigned to that role.</span></span>
6.  <span data-ttu-id="6d967-118">Creare script per qualificare l'accesso alle attività in fase di esecuzione:</span><span class="sxs-lookup"><span data-stu-id="6d967-118">Create scripts to qualify access to tasks at run time:</span></span><dl>

[<span data-ttu-id="6d967-119">Qualificazione dell'accesso con la logica di business in C++</span><span class="sxs-lookup"><span data-stu-id="6d967-119">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)  
    </dl><span data-ttu-id="6d967-120">Questo passaggio è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6d967-120">This step is optional.</span></span>
7.  <span data-ttu-id="6d967-121">Definire gruppi di utenti:</span><span class="sxs-lookup"><span data-stu-id="6d967-121">Define groups of users:</span></span><dl>

[<span data-ttu-id="6d967-122">Definizione di gruppi di utenti in C++</span><span class="sxs-lookup"><span data-stu-id="6d967-122">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)  
    </dl><span data-ttu-id="6d967-123">Questi gruppi possono quindi essere assegnati ai ruoli per determinare quali attività possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="6d967-123">These groups can then be assigned to roles to determine which tasks they can perform.</span></span>
8.  <span data-ttu-id="6d967-124">Aggiungere utenti ai gruppi di utenti:</span><span class="sxs-lookup"><span data-stu-id="6d967-124">Add users to user groups:</span></span><dl>

[<span data-ttu-id="6d967-125">Aggiunta di utenti a un gruppo di applicazioni in C++</span><span class="sxs-lookup"><span data-stu-id="6d967-125">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 



