---
description: Istruzioni per l'utilizzo dell'API di gestione autorizzazioni per definire le autorizzazioni nello script mediante la creazione di un archivio dei criteri di autorizzazione.
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: Definizione delle autorizzazioni nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e16f377ffa669da0b686ac28783e9a370efec94d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968080"
---
# <a name="defining-permissions-in-script"></a><span data-ttu-id="f6f42-103">Definizione delle autorizzazioni nello script</span><span class="sxs-lookup"><span data-stu-id="f6f42-103">Defining Permissions in Script</span></span>

<span data-ttu-id="f6f42-104">In Gestione autorizzazioni è possibile definire quali utenti hanno accesso alle risorse dell'applicazione creando un archivio criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="f6f42-104">In Authorization Manager, you define which users have access to which application resources by creating an authorization policy store.</span></span>

<span data-ttu-id="f6f42-105">**Per definire le autorizzazioni di accesso**</span><span class="sxs-lookup"><span data-stu-id="f6f42-105">**To define access permissions**</span></span>

1.  <span data-ttu-id="f6f42-106">Creare l'archivio in cui sono definiti i criteri di autorizzazione:</span><span class="sxs-lookup"><span data-stu-id="f6f42-106">Create the store where the authorization policy is defined:</span></span><dl>

[<span data-ttu-id="f6f42-107">Creazione di un archivio criteri di autorizzazione nello script</span><span class="sxs-lookup"><span data-stu-id="f6f42-107">Creating an Authorization Policy Store in Script</span></span>](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  <span data-ttu-id="f6f42-108">Creare una sezione nell'archivio dei criteri di autorizzazione per un'applicazione specifica:</span><span class="sxs-lookup"><span data-stu-id="f6f42-108">Create a section in the authorization policy store for a specific application:</span></span><dl>

[<span data-ttu-id="f6f42-109">Creazione di un oggetto applicazione nello script</span><span class="sxs-lookup"><span data-stu-id="f6f42-109">Creating an Application Object in Script</span></span>](creating-an-application-object-in-script.md)  
    </dl>
3.  <span data-ttu-id="f6f42-110">Definire le operazioni implementate dall'applicazione per accedere alle risorse e modificarle:</span><span class="sxs-lookup"><span data-stu-id="f6f42-110">Define operations that the application implements to access and modify resources:</span></span><dl>

[<span data-ttu-id="f6f42-111">Definizione di operazioni nello script</span><span class="sxs-lookup"><span data-stu-id="f6f42-111">Defining Operations in Script</span></span>](defining-operations-in-script.md)  
    </dl>
4.  <span data-ttu-id="f6f42-112">Raggruppare le operazioni in attività di alto livello che gli utenti desiderano eseguire:</span><span class="sxs-lookup"><span data-stu-id="f6f42-112">Group operations into high-level tasks that users want to perform:</span></span><dl>

[<span data-ttu-id="f6f42-113">Raggruppamento di operazioni in attività nello script</span><span class="sxs-lookup"><span data-stu-id="f6f42-113">Grouping Operations into Tasks in Script</span></span>](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  <span data-ttu-id="f6f42-114">Definire i ruoli che sono costituiti da gruppi di attività:</span><span class="sxs-lookup"><span data-stu-id="f6f42-114">Define roles that consist of groups of tasks:</span></span><dl>

[<span data-ttu-id="f6f42-115">Raggruppamento di attività in ruoli nello script</span><span class="sxs-lookup"><span data-stu-id="f6f42-115">Grouping Tasks into Roles in Script</span></span>](grouping-tasks-into-roles-in-script.md)  
    </dl><span data-ttu-id="f6f42-116">Un utente assegnato a un ruolo dispone dell'autorizzazione per eseguire tutte le attività assegnate a tale ruolo.</span><span class="sxs-lookup"><span data-stu-id="f6f42-116">A user that is assigned to a role has permission to perform any task assigned to that role.</span></span>
6.  <span data-ttu-id="f6f42-117">Creare script per qualificare l'accesso alle attività in fase di esecuzione:</span><span class="sxs-lookup"><span data-stu-id="f6f42-117">Create scripts to qualify access to tasks at run time:</span></span><dl>

[<span data-ttu-id="f6f42-118">Qualificazione dell'accesso con la logica di business nello script</span><span class="sxs-lookup"><span data-stu-id="f6f42-118">Qualifying Access with Business Logic in Script</span></span>](qualifying-access-with-business-logic-in-script.md)  
    </dl><span data-ttu-id="f6f42-119">Questo passaggio è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f6f42-119">This step is optional.</span></span>
7.  <span data-ttu-id="f6f42-120">Definire gruppi di utenti:</span><span class="sxs-lookup"><span data-stu-id="f6f42-120">Define groups of users:</span></span><dl>

[<span data-ttu-id="f6f42-121">Definizione di gruppi di utenti nello script</span><span class="sxs-lookup"><span data-stu-id="f6f42-121">Defining Groups of Users in Script</span></span>](defining-groups-of-users-in-script.md)  
    </dl><span data-ttu-id="f6f42-122">Questi gruppi possono quindi essere assegnati ai ruoli per determinare quali attività possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="f6f42-122">These groups can then be assigned to roles to determine which tasks they can perform.</span></span>
8.  <span data-ttu-id="f6f42-123">Aggiungere utenti ai gruppi di utenti:</span><span class="sxs-lookup"><span data-stu-id="f6f42-123">Add users to user groups:</span></span><dl>

[<span data-ttu-id="f6f42-124">Aggiunta di utenti a un gruppo di applicazioni nello script</span><span class="sxs-lookup"><span data-stu-id="f6f42-124">Adding Users to an Application Group in Script</span></span>](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 



