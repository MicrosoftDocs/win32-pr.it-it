---
title: Route e migliore route
description: Una route è un \ 0034; percorso di rete \ 0034; a una destinazione a cui è associato un determinato costo. Il costo è rappresentato dalle relative preferenze amministrative e dalla metrica specifica del protocollo. Le route con costi inferiori sono preferite rispetto a tutte le altre route.
ms.assetid: c5a75308-42da-4ef9-a712-9987c87eef84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd55ec1188383f4cdef55511aae7a9c2cf59303
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298990"
---
# <a name="routes-and-the-best-route"></a><span data-ttu-id="f9837-105">Route e migliore route</span><span class="sxs-lookup"><span data-stu-id="f9837-105">Routes and the Best Route</span></span>

<span data-ttu-id="f9837-106">Una route è un "percorso di rete" per una destinazione a cui è associato un determinato costo.</span><span class="sxs-lookup"><span data-stu-id="f9837-106">A route is a "network path" to a destination that has a certain cost associated with it.</span></span> <span data-ttu-id="f9837-107">Il costo è rappresentato dalle relative preferenze amministrative e dalla metrica specifica del protocollo.</span><span class="sxs-lookup"><span data-stu-id="f9837-107">The cost is represented by its administrative preference and its protocol-specific metric.</span></span> <span data-ttu-id="f9837-108">Le route con costi inferiori sono preferite rispetto a tutte le altre route.</span><span class="sxs-lookup"><span data-stu-id="f9837-108">Routes with lower costs are preferred over all other routes.</span></span>

<span data-ttu-id="f9837-109">Una voce di route nella tabella di routing include:</span><span class="sxs-lookup"><span data-stu-id="f9837-109">A route entry in the routing table includes:</span></span>

-   <span data-ttu-id="f9837-110">Handle per la destinazione</span><span class="sxs-lookup"><span data-stu-id="f9837-110">A handle to the destination</span></span>
-   <span data-ttu-id="f9837-111">Proprietario della route</span><span class="sxs-lookup"><span data-stu-id="f9837-111">The owner of this route</span></span>
-   <span data-ttu-id="f9837-112">Neighbor (peer) che ha fornito le informazioni sulla Route</span><span class="sxs-lookup"><span data-stu-id="f9837-112">The neighbor (peer) that provided the route information</span></span>
-   <span data-ttu-id="f9837-113">Flag associati allo stato della route</span><span class="sxs-lookup"><span data-stu-id="f9837-113">Flags associated with the state of the route</span></span>
-   <span data-ttu-id="f9837-114">Flag associati alla route</span><span class="sxs-lookup"><span data-stu-id="f9837-114">Flags associated with the route</span></span>
-   <span data-ttu-id="f9837-115">Preferenza e metrica per la route</span><span class="sxs-lookup"><span data-stu-id="f9837-115">The preference and metric for the route</span></span>
-   <span data-ttu-id="f9837-116">Elenco di visualizzazioni a cui appartiene la route</span><span class="sxs-lookup"><span data-stu-id="f9837-116">The list of views to which the route belongs</span></span>
-   <span data-ttu-id="f9837-117">Informazioni private del proprietario della route</span><span class="sxs-lookup"><span data-stu-id="f9837-117">Information that is private to the owner of the route</span></span>
-   <span data-ttu-id="f9837-118">Elenco di hop successivi utilizzati per raggiungere la destinazione</span><span class="sxs-lookup"><span data-stu-id="f9837-118">A list of next hops used to reach the destination</span></span>

<span data-ttu-id="f9837-119">I valori seguenti, insieme, identificano in modo univoco una route nella tabella di routing:</span><span class="sxs-lookup"><span data-stu-id="f9837-119">The following values, taken together, uniquely identify a route in the routing table:</span></span>

-   <span data-ttu-id="f9837-120">Rete di destinazione</span><span class="sxs-lookup"><span data-stu-id="f9837-120">The destination network</span></span>
-   <span data-ttu-id="f9837-121">Proprietario della route</span><span class="sxs-lookup"><span data-stu-id="f9837-121">The owner of the route</span></span>
-   <span data-ttu-id="f9837-122">Il vicino che ha fornito la route</span><span class="sxs-lookup"><span data-stu-id="f9837-122">The neighbor who supplied the route</span></span>

## <a name="metrics-and-preference"></a><span data-ttu-id="f9837-123">Metriche e preferenze</span><span class="sxs-lookup"><span data-stu-id="f9837-123">Metrics and Preference</span></span>

<span data-ttu-id="f9837-124">Ogni route ha una preferenza amministrativa (specificata dai criteri di routing) e una metrica dipendente dal client.</span><span class="sxs-lookup"><span data-stu-id="f9837-124">Each route has an administrative preference (specified by the routing policy), and a client-dependent metric.</span></span> <span data-ttu-id="f9837-125">Gestione tabelle di routing utilizza queste informazioni per determinare quale route è la migliore route a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="f9837-125">The routing table manager uses this information to determine which route is the better route to a destination.</span></span> <span data-ttu-id="f9837-126">Le route con preferenza inferiore sono Route migliori, una più bassa e quindi migliore.</span><span class="sxs-lookup"><span data-stu-id="f9837-126">Routes with lower preference are better routes (one being lowest, and therefore best).</span></span> <span data-ttu-id="f9837-127">Se due route hanno la stessa preferenza, la route con la metrica inferiore rappresenta il percorso migliore.</span><span class="sxs-lookup"><span data-stu-id="f9837-127">If two routes have the same preference, the route with the lower metric is the better route.</span></span>

<span data-ttu-id="f9837-128">In genere, la preferenza di una route è determinata dalla preferenza del client che ha aggiunto la route.</span><span class="sxs-lookup"><span data-stu-id="f9837-128">Normally, the preference of a route is determined by the preference of the client that added the route.</span></span> <span data-ttu-id="f9837-129">Tuttavia, per tutte le route aggiunte mediante lo strumento di gestione Netsh.exe, è possibile specificare un valore di preferenza per ogni route.</span><span class="sxs-lookup"><span data-stu-id="f9837-129">However, for any routes added using the Netsh.exe management tool, a preference value can be specified on a per-route basis.</span></span>

<span data-ttu-id="f9837-130">La preferenza viene in genere utilizzata per indicare la priorità tra i client.</span><span class="sxs-lookup"><span data-stu-id="f9837-130">Preference is normally used to indicate priority between clients.</span></span> <span data-ttu-id="f9837-131">Ad esempio, un amministratore può assegnare a OSPF una preferenza più bassa (migliore) rispetto a RIP.</span><span class="sxs-lookup"><span data-stu-id="f9837-131">For example, an administrator can assign OSPF a lower (better) preference than RIP.</span></span> <span data-ttu-id="f9837-132">In questo caso, le route OSPF sono preferibili per la copia delle route.</span><span class="sxs-lookup"><span data-stu-id="f9837-132">In this case, OSPF routes are preferable to RIP routes.</span></span>

 

 




