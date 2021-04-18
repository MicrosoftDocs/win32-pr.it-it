---
description: L'azione StartServices avvia i servizi di sistema. Questa azione esegue una query sulla tabella ServiceControl.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: Azione StartServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c150a8970c5852d9cfc53581290e792c00b628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310512"
---
# <a name="startservices-action"></a><span data-ttu-id="1e2f2-104">Azione StartServices</span><span class="sxs-lookup"><span data-stu-id="1e2f2-104">StartServices Action</span></span>

<span data-ttu-id="1e2f2-105">L'azione StartServices avvia i servizi di sistema.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-105">The StartServices action starts system services.</span></span> <span data-ttu-id="1e2f2-106">Questa azione esegue una query sulla [tabella ServiceControl](servicecontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="1e2f2-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1e2f2-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="1e2f2-107">Sequence Restrictions</span></span>

<span data-ttu-id="1e2f2-108">Le azioni dei servizi devono essere usate nella sequenza seguente:</span><span class="sxs-lookup"><span data-stu-id="1e2f2-108">The services actions must be used in the following sequence:</span></span>

-   [<span data-ttu-id="1e2f2-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="1e2f2-109">StopServices</span></span>](stopservices-action.md)
-   [<span data-ttu-id="1e2f2-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="1e2f2-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="1e2f2-111">Una delle azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1e2f2-111">Any of the following actions:</span></span>

-   [<span data-ttu-id="1e2f2-112">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="1e2f2-112">InstallFiles</span></span>](installfiles-action.md)
-   [<span data-ttu-id="1e2f2-113">RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="1e2f2-113">RemoveFiles</span></span>](removefiles-action.md)
-   [<span data-ttu-id="1e2f2-114">DuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="1e2f2-114">DuplicateFiles</span></span>](duplicatefiles-action.md)
-   [<span data-ttu-id="1e2f2-115">MoveFiles</span><span class="sxs-lookup"><span data-stu-id="1e2f2-115">MoveFiles</span></span>](movefiles-action.md)
-   [<span data-ttu-id="1e2f2-116">PatchFiles</span><span class="sxs-lookup"><span data-stu-id="1e2f2-116">PatchFiles</span></span>](patchfiles-action.md)
-   [<span data-ttu-id="1e2f2-117">RemoveDuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="1e2f2-117">RemoveDuplicateFiles</span></span>](removeduplicatefiles-action.md)
-   [<span data-ttu-id="1e2f2-118">InstallServices</span><span class="sxs-lookup"><span data-stu-id="1e2f2-118">InstallServices</span></span>](installservices-action.md)
-   <span data-ttu-id="1e2f2-119">StartServices</span><span class="sxs-lookup"><span data-stu-id="1e2f2-119">StartServices</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1e2f2-120">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="1e2f2-120">ActionData Messages</span></span>



| <span data-ttu-id="1e2f2-121">Campo</span><span class="sxs-lookup"><span data-stu-id="1e2f2-121">Field</span></span> | <span data-ttu-id="1e2f2-122">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="1e2f2-122">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="1e2f2-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="1e2f2-123">\[1\]</span></span> | <span data-ttu-id="1e2f2-124">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-124">Service display name.</span></span>      |
| <span data-ttu-id="1e2f2-125">\[2\]</span><span class="sxs-lookup"><span data-stu-id="1e2f2-125">\[2\]</span></span> | <span data-ttu-id="1e2f2-126">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-126">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="1e2f2-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e2f2-127">Remarks</span></span>

<span data-ttu-id="1e2f2-128">Per questa azione è necessario che l'utente sia un amministratore o disponga di privilegi elevati con l'autorizzazione per controllare i servizi o che l'applicazione faccia parte di un'installazione gestita.</span><span class="sxs-lookup"><span data-stu-id="1e2f2-128">This action requires that the user be an administrator or have elevated privileges with permission to control services or that the application be part of a managed installation.</span></span>

 

 



