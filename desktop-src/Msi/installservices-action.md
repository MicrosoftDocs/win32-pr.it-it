---
description: L'azione InstallServices registra un servizio per il sistema. Questa azione esegue una query sulla tabella ServiceInstall.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Azione InstallServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5964deb08f811e391418211efc6f774261bd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317758"
---
# <a name="installservices-action"></a><span data-ttu-id="0d9d6-104">Azione InstallServices</span><span class="sxs-lookup"><span data-stu-id="0d9d6-104">InstallServices Action</span></span>

<span data-ttu-id="0d9d6-105">L'azione InstallServices registra un servizio per il sistema.</span><span class="sxs-lookup"><span data-stu-id="0d9d6-105">The InstallServices action registers a service for the system.</span></span> <span data-ttu-id="0d9d6-106">Questa azione esegue una query sulla [tabella ServiceInstall](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="0d9d6-106">This action queries the [ServiceInstall table](serviceinstall-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0d9d6-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="0d9d6-107">Sequence Restrictions</span></span>

<span data-ttu-id="0d9d6-108">L'azione servizi deve essere utilizzata nella sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="0d9d6-108">The services action must be used in the following sequence.</span></span>

[<span data-ttu-id="0d9d6-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="0d9d6-109">StopServices</span></span>](stopservices-action.md)

[<span data-ttu-id="0d9d6-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="0d9d6-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="0d9d6-111">Una delle azioni seguenti: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles](removeduplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="0d9d6-111">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>

<span data-ttu-id="0d9d6-112">InstallServices</span><span class="sxs-lookup"><span data-stu-id="0d9d6-112">InstallServices</span></span>

[<span data-ttu-id="0d9d6-113">StartServices</span><span class="sxs-lookup"><span data-stu-id="0d9d6-113">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="0d9d6-114">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="0d9d6-114">ActionData Messages</span></span>

<span data-ttu-id="0d9d6-115">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="0d9d6-115">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d9d6-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d9d6-116">Remarks</span></span>

<span data-ttu-id="0d9d6-117">Per questa azione è necessario che l'utente sia un amministratore o disponga di privilegi elevati con l'autorizzazione per installare i servizi o che l'applicazione faccia parte di un'installazione gestita.</span><span class="sxs-lookup"><span data-stu-id="0d9d6-117">This action requires that the user be an administrator or have elevated privileges with permission to install services or that the application be part of a managed installation.</span></span>

 

 



