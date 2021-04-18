---
description: L'azione StopServices interrompe i servizi di sistema. Questa azione esegue una query sulla tabella ServiceControl.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Azione StopServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb271b99c434a1ac54ab9744697b991e9e1fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308680"
---
# <a name="stopservices-action"></a><span data-ttu-id="46157-104">Azione StopServices</span><span class="sxs-lookup"><span data-stu-id="46157-104">StopServices Action</span></span>

<span data-ttu-id="46157-105">L'azione StopServices interrompe i servizi di sistema.</span><span class="sxs-lookup"><span data-stu-id="46157-105">The StopServices action stops system services.</span></span> <span data-ttu-id="46157-106">Questa azione esegue una query sulla [tabella ServiceControl](servicecontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="46157-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="46157-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="46157-107">Sequence Restrictions</span></span>

<span data-ttu-id="46157-108">Le azioni dei servizi devono essere usate nella sequenza seguente:</span><span class="sxs-lookup"><span data-stu-id="46157-108">The services actions must be used in the following sequence:</span></span>

-   <span data-ttu-id="46157-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="46157-109">StopServices</span></span>
-   [<span data-ttu-id="46157-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="46157-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="46157-111">Una delle azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="46157-111">Any of the following actions:</span></span>

-   [<span data-ttu-id="46157-112">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="46157-112">InstallFiles</span></span>](installfiles-action.md)
-   [<span data-ttu-id="46157-113">RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="46157-113">RemoveFiles</span></span>](removefiles-action.md)
-   [<span data-ttu-id="46157-114">DuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="46157-114">DuplicateFiles</span></span>](duplicatefiles-action.md)
-   [<span data-ttu-id="46157-115">MoveFiles</span><span class="sxs-lookup"><span data-stu-id="46157-115">MoveFiles</span></span>](movefiles-action.md)
-   [<span data-ttu-id="46157-116">PatchFiles</span><span class="sxs-lookup"><span data-stu-id="46157-116">PatchFiles</span></span>](patchfiles-action.md)
-   [<span data-ttu-id="46157-117">RemoveDuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="46157-117">RemoveDuplicateFiles</span></span>](removeduplicatefiles-action.md)
-   [<span data-ttu-id="46157-118">InstallServices</span><span class="sxs-lookup"><span data-stu-id="46157-118">InstallServices</span></span>](installservices-action.md)
-   [<span data-ttu-id="46157-119">StartServices</span><span class="sxs-lookup"><span data-stu-id="46157-119">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="46157-120">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="46157-120">ActionData Messages</span></span>



| <span data-ttu-id="46157-121">Campo</span><span class="sxs-lookup"><span data-stu-id="46157-121">Field</span></span> | <span data-ttu-id="46157-122">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="46157-122">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="46157-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="46157-123">\[1\]</span></span> | <span data-ttu-id="46157-124">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="46157-124">Service display name.</span></span>      |
| <span data-ttu-id="46157-125">\[2\]</span><span class="sxs-lookup"><span data-stu-id="46157-125">\[2\]</span></span> | <span data-ttu-id="46157-126">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="46157-126">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="46157-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="46157-127">Remarks</span></span>

<span data-ttu-id="46157-128">Per questa azione è necessario che l'utente sia un amministratore o disponga di privilegi elevati con l'autorizzazione per controllare i servizi o che l'applicazione faccia parte di un'installazione gestita.</span><span class="sxs-lookup"><span data-stu-id="46157-128">This action requires that the user be an administrator or have elevated privileges with permission to control services or that the application be part of a managed installation.</span></span>

 

 



