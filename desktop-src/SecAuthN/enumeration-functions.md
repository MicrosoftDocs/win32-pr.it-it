---
description: Se il provider di rete deve supportare l'esplorazione delle risorse di rete, deve implementare le funzioni seguenti. MPR chiama queste funzioni per enumerare le risorse.
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: Funzioni di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2670424be1540aad3e46e32c5b0606eb02e04bdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049426"
---
# <a name="enumeration-functions"></a><span data-ttu-id="1b376-104">Funzioni di enumerazione</span><span class="sxs-lookup"><span data-stu-id="1b376-104">Enumeration Functions</span></span>

<span data-ttu-id="1b376-105">Se il provider di rete deve supportare l'esplorazione delle risorse di rete, deve implementare le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="1b376-105">If your network provider needs to support browsing of its network resources, it should implement the following functions.</span></span> <span data-ttu-id="1b376-106">MPR chiama queste funzioni per enumerare le risorse.</span><span class="sxs-lookup"><span data-stu-id="1b376-106">MPR calls these functions to enumerate the resources.</span></span>

<span data-ttu-id="1b376-107">Non è necessario un provider di rete per implementare alcuna delle funzioni di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="1b376-107">A network provider is not required to implement any of the enumeration functions.</span></span> <span data-ttu-id="1b376-108">Se, tuttavia, un provider di rete implementa [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)o [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), deve implementare anche le altre due funzioni di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="1b376-108">If, however, a network provider implements either [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource), or [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), it must also implement the other two enumeration functions.</span></span>



| <span data-ttu-id="1b376-109">Funzione</span><span class="sxs-lookup"><span data-stu-id="1b376-109">Function</span></span>                                                     | <span data-ttu-id="1b376-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b376-110">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b376-111">**NPOpenEnum**</span><span class="sxs-lookup"><span data-stu-id="1b376-111">**NPOpenEnum**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | <span data-ttu-id="1b376-112">Apre un'enumerazione delle risorse di rete o delle connessioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="1b376-112">Opens an enumeration of network resources or existing connections.</span></span>                                                                                                  |
| [<span data-ttu-id="1b376-113">**NPEnumResource**</span><span class="sxs-lookup"><span data-stu-id="1b376-113">**NPEnumResource**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | <span data-ttu-id="1b376-114">Esegue un'enumerazione su un handle restituito da [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).</span><span class="sxs-lookup"><span data-stu-id="1b376-114">Performs an enumeration on a handle returned by [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).</span></span>                                                                                   |
| [<span data-ttu-id="1b376-115">**NPCloseEnum**</span><span class="sxs-lookup"><span data-stu-id="1b376-115">**NPCloseEnum**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | <span data-ttu-id="1b376-116">Chiude un'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="1b376-116">Closes an enumeration.</span></span>                                                                                                                                              |
| [<span data-ttu-id="1b376-117">**NPGetResourceInformation**</span><span class="sxs-lookup"><span data-stu-id="1b376-117">**NPGetResourceInformation**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | <span data-ttu-id="1b376-118">Determina se il provider è il provider corretto per rispondere a una richiesta per una risorsa di rete specificata e restituisce informazioni sul tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="1b376-118">Determines whether the provider is the correct provider to respond to a request for a specified network resource and returns information about the resource's type.</span></span> |
| [<span data-ttu-id="1b376-119">**NPGetResourceParent**</span><span class="sxs-lookup"><span data-stu-id="1b376-119">**NPGetResourceParent**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | <span data-ttu-id="1b376-120">Restituisce l'elemento padre di una risorsa di rete specificata nella gerarchia browse.</span><span class="sxs-lookup"><span data-stu-id="1b376-120">Returns the parent of a specified network resource in the browse hierarchy.</span></span>                                                                                         |



 

 

 



