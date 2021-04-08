---
title: Flag di query tabella di routing
description: Utilizzare queste costanti per le query di tabella router.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Flag di query tabella di routing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37ab647efb192e29aae421e02bef1dec065e3b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103857026"
---
# <a name="routing-table-query-flags"></a><span data-ttu-id="abf62-104">Flag di query tabella di routing</span><span class="sxs-lookup"><span data-stu-id="abf62-104">Routing Table Query Flags</span></span>

<span data-ttu-id="abf62-105">Utilizzare queste costanti per le query di tabella router.</span><span class="sxs-lookup"><span data-stu-id="abf62-105">Use these constants for router table queries.</span></span>



| <span data-ttu-id="abf62-106">Costante</span><span class="sxs-lookup"><span data-stu-id="abf62-106">Constant</span></span>              | <span data-ttu-id="abf62-107">Valore</span><span class="sxs-lookup"><span data-stu-id="abf62-107">Value</span></span>      | <span data-ttu-id="abf62-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abf62-108">Description</span></span>                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="abf62-109">\_Nessuna corrispondenza \_ RTM</span><span class="sxs-lookup"><span data-stu-id="abf62-109">RTM\_MATCH\_NONE</span></span>      | <span data-ttu-id="abf62-110">0x00000000</span><span class="sxs-lookup"><span data-stu-id="abf62-110">0x00000000</span></span> | <span data-ttu-id="abf62-111">Corrisponde a nessuno dei criteri. vengono restituite tutte le route per la destinazione.</span><span class="sxs-lookup"><span data-stu-id="abf62-111">Matches none of the criteria; all routes for the destination are returned.</span></span> |
| <span data-ttu-id="abf62-112">\_proprietario corrispondenza \_ RTM</span><span class="sxs-lookup"><span data-stu-id="abf62-112">RTM\_MATCH\_OWNER</span></span>     | <span data-ttu-id="abf62-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="abf62-113">0x00000001</span></span> | <span data-ttu-id="abf62-114">Corrisponde alle route con lo stesso proprietario.</span><span class="sxs-lookup"><span data-stu-id="abf62-114">Matches routes with same owner.</span></span>                                            |
| <span data-ttu-id="abf62-115">\_corrispondenza RTM corrispondente \_</span><span class="sxs-lookup"><span data-stu-id="abf62-115">RTM\_MATCH\_NEIGHBOUR</span></span> | <span data-ttu-id="abf62-116">0x00000002</span><span class="sxs-lookup"><span data-stu-id="abf62-116">0x00000002</span></span> | <span data-ttu-id="abf62-117">Corrisponde alle route con lo stesso adiacente.</span><span class="sxs-lookup"><span data-stu-id="abf62-117">Matches routes with the same neighbor.</span></span>                                     |
| <span data-ttu-id="abf62-118">\_corrispondenze \_ RTM</span><span class="sxs-lookup"><span data-stu-id="abf62-118">RTM\_MATCH\_PREF</span></span>      | <span data-ttu-id="abf62-119">0x00000004</span><span class="sxs-lookup"><span data-stu-id="abf62-119">0x00000004</span></span> | <span data-ttu-id="abf62-120">Corrisponde alle route con la stessa preferenza.</span><span class="sxs-lookup"><span data-stu-id="abf62-120">Matches routes that have the same preference.</span></span>                              |
| <span data-ttu-id="abf62-121">\_NEXTHOP corrispondenza \_ RTM</span><span class="sxs-lookup"><span data-stu-id="abf62-121">RTM\_MATCH\_NEXTHOP</span></span>   | <span data-ttu-id="abf62-122">0x00000008</span><span class="sxs-lookup"><span data-stu-id="abf62-122">0x00000008</span></span> | <span data-ttu-id="abf62-123">Corrisponde alle route con lo stesso hop successivo.</span><span class="sxs-lookup"><span data-stu-id="abf62-123">Matches routes that have the same next hop.</span></span>                                |
| <span data-ttu-id="abf62-124">\_interfaccia di corrispondenza RTM \_</span><span class="sxs-lookup"><span data-stu-id="abf62-124">RTM\_MATCH\_INTERFACE</span></span> | <span data-ttu-id="abf62-125">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abf62-125">0x00000010</span></span> | <span data-ttu-id="abf62-126">Corrisponde alle route che si trovano nella stessa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="abf62-126">Matches routes that are on the same interface.</span></span>                             |
| <span data-ttu-id="abf62-127">\_corrispondenza RTM \_ completa</span><span class="sxs-lookup"><span data-stu-id="abf62-127">RTM\_MATCH\_FULL</span></span>      | <span data-ttu-id="abf62-128">0x0000FFFF</span><span class="sxs-lookup"><span data-stu-id="abf62-128">0x0000FFFF</span></span> | <span data-ttu-id="abf62-129">Corrisponde alle route con tutti i criteri.</span><span class="sxs-lookup"><span data-stu-id="abf62-129">Matches routes with all criteria.</span></span>                                          |
| <span data-ttu-id="abf62-130">\_protocollo migliore \_ RTM</span><span class="sxs-lookup"><span data-stu-id="abf62-130">RTM\_BEST\_PROTOCOL</span></span>   | <span data-ttu-id="abf62-131">0</span><span class="sxs-lookup"><span data-stu-id="abf62-131">0</span></span>          | <span data-ttu-id="abf62-132">Restituisce una route indipendentemente dal protocollo di cui è proprietario.</span><span class="sxs-lookup"><span data-stu-id="abf62-132">Returns a route regardless of which protocol owns it.</span></span>                      |
| <span data-ttu-id="abf62-133">\_il \_ protocollo RTM</span><span class="sxs-lookup"><span data-stu-id="abf62-133">RTM\_THIS\_PROTOCOL</span></span>   | <span data-ttu-id="abf62-134">~0</span><span class="sxs-lookup"><span data-stu-id="abf62-134">~0</span></span>         | <span data-ttu-id="abf62-135">Restituisce la route migliore per il protocollo chiamante.</span><span class="sxs-lookup"><span data-stu-id="abf62-135">Returns the best route for the calling protocol.</span></span>                           |



 

 

 




