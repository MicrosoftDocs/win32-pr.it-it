---
title: Flag di hop successivo
description: Flag di hop successivo
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Prossima
- Flag di hop successivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd672c9b083e47c3d0a7419d03ab890c1037ce5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045200"
---
# <a name="next-hop-flags"></a><span data-ttu-id="d0300-105">Flag di hop successivo</span><span class="sxs-lookup"><span data-stu-id="d0300-105">Next Hop Flags</span></span>

## <a name="next-hop-state-flags"></a><span data-ttu-id="d0300-106">Flag di stato hop successivo</span><span class="sxs-lookup"><span data-stu-id="d0300-106">Next Hop State Flags</span></span>



| <span data-ttu-id="d0300-107">Costante</span><span class="sxs-lookup"><span data-stu-id="d0300-107">Constant</span></span>                     | <span data-ttu-id="d0300-108">Valore</span><span class="sxs-lookup"><span data-stu-id="d0300-108">Value</span></span> | <span data-ttu-id="d0300-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0300-109">Description</span></span>                              |
|------------------------------|-------|------------------------------------------|
| <span data-ttu-id="d0300-110">\_stato NEXTHOP \_ RTM \_ creato</span><span class="sxs-lookup"><span data-stu-id="d0300-110">RTM\_NEXTHOP\_STATE\_CREATED</span></span> | <span data-ttu-id="d0300-111">0</span><span class="sxs-lookup"><span data-stu-id="d0300-111">0</span></span>     | <span data-ttu-id="d0300-112">Indica che è stato creato l'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="d0300-112">Indicates that the next hop was created.</span></span> |
| <span data-ttu-id="d0300-113">\_stato NEXTHOP \_ RTM \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="d0300-113">RTM\_NEXTHOP\_STATE\_DELETED</span></span> | <span data-ttu-id="d0300-114">1</span><span class="sxs-lookup"><span data-stu-id="d0300-114">1</span></span>     | <span data-ttu-id="d0300-115">Indica che l'hop successivo è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="d0300-115">Indicates that the next hop was deleted.</span></span> |



 

## <a name="next-hop-flags"></a><span data-ttu-id="d0300-116">Flag di hop successivo</span><span class="sxs-lookup"><span data-stu-id="d0300-116">Next Hop Flags</span></span>



| <span data-ttu-id="d0300-117">Costante</span><span class="sxs-lookup"><span data-stu-id="d0300-117">Constant</span></span>                    | <span data-ttu-id="d0300-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d0300-118">Value</span></span>  | <span data-ttu-id="d0300-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0300-119">Description</span></span>                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0300-120">\_flag NEXTHOP RTM in \_ \_ remoto</span><span class="sxs-lookup"><span data-stu-id="d0300-120">RTM\_NEXTHOP\_FLAGS\_REMOTE</span></span> | <span data-ttu-id="d0300-121">0x0001</span><span class="sxs-lookup"><span data-stu-id="d0300-121">0x0001</span></span> | <span data-ttu-id="d0300-122">L'hop successivo punta a una destinazione remota non direttamente raggiungibile.</span><span class="sxs-lookup"><span data-stu-id="d0300-122">This next hop points to a remote destination that is not directly reachable.</span></span> <span data-ttu-id="d0300-123">Per ottenere il percorso completo, il client deve eseguire una ricerca ricorsiva.</span><span class="sxs-lookup"><span data-stu-id="d0300-123">To obtain the complete path, the client must perform a recursive lookup.</span></span> |
| <span data-ttu-id="d0300-124">\_flag NEXTHOP \_ RTM \_ inattivo</span><span class="sxs-lookup"><span data-stu-id="d0300-124">RTM\_NEXTHOP\_FLAGS\_DOWN</span></span>   | <span data-ttu-id="d0300-125">0x0002</span><span class="sxs-lookup"><span data-stu-id="d0300-125">0x0002</span></span> | <span data-ttu-id="d0300-126">Questo flag è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="d0300-126">This flag is reserved for future use.</span></span>                                                                                                                 |



 

## <a name="next-hop-added"></a><span data-ttu-id="d0300-127">Hop successivo aggiunto</span><span class="sxs-lookup"><span data-stu-id="d0300-127">Next Hop Added</span></span>



| <span data-ttu-id="d0300-128">Costante</span><span class="sxs-lookup"><span data-stu-id="d0300-128">Constant</span></span>                  | <span data-ttu-id="d0300-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d0300-129">Value</span></span> | <span data-ttu-id="d0300-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0300-130">Description</span></span>                 |
|---------------------------|-------|-----------------------------|
| <span data-ttu-id="d0300-131">\_ \_ nuova modifica di NEXTHOP RTM \_</span><span class="sxs-lookup"><span data-stu-id="d0300-131">RTM\_NEXTHOP\_CHANGE\_NEW</span></span> | <span data-ttu-id="d0300-132">0x01</span><span class="sxs-lookup"><span data-stu-id="d0300-132">0x01</span></span>  | <span data-ttu-id="d0300-133">È stato creato un nuovo hop successivo.</span><span class="sxs-lookup"><span data-stu-id="d0300-133">A new next hop was created.</span></span> |



 

 

 




