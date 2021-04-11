---
description: L'azione DeleteServices arresta un servizio e ne rimuove la registrazione dal sistema. Questa azione esegue una query sulla tabella ServiceControl.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Azione DeleteServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5fc22bbb0c11cd546f1ffbb9f3ad98e06efae3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346346"
---
# <a name="deleteservices-action"></a><span data-ttu-id="d829f-104">Azione DeleteServices</span><span class="sxs-lookup"><span data-stu-id="d829f-104">DeleteServices Action</span></span>

<span data-ttu-id="d829f-105">L'azione DeleteServices arresta un servizio e ne rimuove la registrazione dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d829f-105">The DeleteServices action stops a service and removes its registration from the system.</span></span> <span data-ttu-id="d829f-106">Questa azione esegue una query sulla [tabella ServiceControl](servicecontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="d829f-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d829f-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="d829f-107">Sequence Restrictions</span></span>

<span data-ttu-id="d829f-108">Le azioni dei servizi devono essere usate nella sequenza seguente:</span><span class="sxs-lookup"><span data-stu-id="d829f-108">The services actions must be used in the following sequence:</span></span>

1.  [<span data-ttu-id="d829f-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="d829f-109">StopServices</span></span>](stopservices-action.md)
2.  <span data-ttu-id="d829f-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="d829f-110">DeleteServices</span></span>
3.  <span data-ttu-id="d829f-111">Una delle azioni seguenti: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles](removeduplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="d829f-111">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>
4.  [<span data-ttu-id="d829f-112">Azione InstallServices</span><span class="sxs-lookup"><span data-stu-id="d829f-112">InstallServices action</span></span>](installservices-action.md)
5.  [<span data-ttu-id="d829f-113">StartServices</span><span class="sxs-lookup"><span data-stu-id="d829f-113">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="d829f-114">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="d829f-114">ActionData Messages</span></span>



| <span data-ttu-id="d829f-115">Campo</span><span class="sxs-lookup"><span data-stu-id="d829f-115">Field</span></span> | <span data-ttu-id="d829f-116">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="d829f-116">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="d829f-117">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d829f-117">\[1\]</span></span> | <span data-ttu-id="d829f-118">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="d829f-118">Service display name.</span></span>      |
| <span data-ttu-id="d829f-119">\[2\]</span><span class="sxs-lookup"><span data-stu-id="d829f-119">\[2\]</span></span> | <span data-ttu-id="d829f-120">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="d829f-120">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="d829f-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="d829f-121">Remarks</span></span>

<span data-ttu-id="d829f-122">Questa azione richiede che l'utente sia un amministratore o disponga di privilegi elevati con l'autorizzazione per eliminare i servizi o che l'applicazione faccia parte di un'installazione gestita.</span><span class="sxs-lookup"><span data-stu-id="d829f-122">This action requires the user be an administrator or have elevated privileges with permission to delete services or that the application be part of a managed installation.</span></span>

 

 



