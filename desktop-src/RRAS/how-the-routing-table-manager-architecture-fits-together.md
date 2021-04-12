---
title: Interazione tra l'architettura di gestione tabelle di routing
description: Nella figura seguente viene illustrata la relazione tra i diversi componenti di un router.
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM, architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc36c339ac89f01d5ba14c00857b3ced9c29414c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332751"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a><span data-ttu-id="7edde-104">Interazione tra l'architettura di gestione tabelle di routing</span><span class="sxs-lookup"><span data-stu-id="7edde-104">How the Routing Table Manager Architecture Fits Together</span></span>

<span data-ttu-id="7edde-105">Nella figura seguente viene illustrata la relazione tra i diversi componenti di un router.</span><span class="sxs-lookup"><span data-stu-id="7edde-105">The following illustration shows the relationship between the different components of a router.</span></span>

![relazione tra componenti router](images/rtsrvarch.png)

<span data-ttu-id="7edde-107">Quando il router viene bootstrap, viene avviato il servizio Gestione router, oltre a uno o più protocolli di routing.</span><span class="sxs-lookup"><span data-stu-id="7edde-107">When the router is bootstrapped, the router manager service is started, as well as one or more routing protocols.</span></span> <span data-ttu-id="7edde-108">I protocolli di routing sono associati alle varie interfacce sul router.</span><span class="sxs-lookup"><span data-stu-id="7edde-108">Routing protocols are associated with the various interfaces on the router.</span></span> <span data-ttu-id="7edde-109">Gestione router avvia inoltre gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="7edde-109">The router manager also starts the routing table manager.</span></span>

<span data-ttu-id="7edde-110">Nella figura seguente viene illustrata la relazione tra i client di e i diversi componenti di gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="7edde-110">The following illustration shows the relationship between clients and the different components of the routing table manager.</span></span>

![relazione tra client e componenti di gestione tabelle di routing](images/rtmentrel.png)

<span data-ttu-id="7edde-112">Gestione router avvia una o più istanze di gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="7edde-112">The router manager starts one or more instances of the routing table manager.</span></span> <span data-ttu-id="7edde-113">Quando vengono avviate più istanze di gestione tabelle di routing, il router è stato configurato per fungere da uno o più router virtuali.</span><span class="sxs-lookup"><span data-stu-id="7edde-113">When multiple instances of the routing table manager are started, the router has been configured to act as one or more virtual routers.</span></span> <span data-ttu-id="7edde-114">Ogni istanza di gestione tabelle di routing è proprietaria di una o più interfacce. ogni interfaccia può essere di proprietà di un'istanza di gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="7edde-114">Each instance of the routing table manager owns one or more interfaces; each interface can only be owned by one instance of the routing table manager.</span></span>

<span data-ttu-id="7edde-115">Ogni istanza di gestione tabelle di routing è indipendente dagli altri. Nessuna informazione viene scambiata tra le istanze.</span><span class="sxs-lookup"><span data-stu-id="7edde-115">Each instance of the routing table manager is independent from the others; no information is exchanged between the instances.</span></span>

<span data-ttu-id="7edde-116">Ogni istanza di gestione tabelle di routing contiene una o più tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="7edde-116">Each instance of the routing table manager contains one or more routing tables.</span></span> <span data-ttu-id="7edde-117">Ogni tabella di routing è associata a una famiglia di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="7edde-117">Each routing table is associated with an address family.</span></span>

<span data-ttu-id="7edde-118">Ogni tabella di routing contiene una o più viste.</span><span class="sxs-lookup"><span data-stu-id="7edde-118">Each routing table contains one or more views.</span></span> <span data-ttu-id="7edde-119">In questo esempio, la tabella di routing viene visualizzata con una visualizzazione unicast e multicast.</span><span class="sxs-lookup"><span data-stu-id="7edde-119">In this example, the routing table is shown with a unicast and multicast view.</span></span> <span data-ttu-id="7edde-120">Ogni visualizzazione è un subset della tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="7edde-120">Each view is a subset of the routing table.</span></span>

<span data-ttu-id="7edde-121">Nella figura seguente viene illustrata la relazione tra i client di e più istanze di gestione tabelle di routing, le tabelle di routing e le viste.</span><span class="sxs-lookup"><span data-stu-id="7edde-121">The following illustration shows the relationship between clients and multiple instances of the routing table manager, routing tables, and views.</span></span>

![client di relazioni, gestione tabelle di routing, tabelle di routing, viste](images/multrtabrel.png)

<span data-ttu-id="7edde-123">Un'istanza del client può essere registrata più volte con un'istanza di gestione tabelle di routing, una volta per ogni famiglia di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="7edde-123">An instance of the client can register multiple times with an instance of the routing table manager — once per address family.</span></span> <span data-ttu-id="7edde-124">Un client può eseguire la registrazione a ogni istanza di gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="7edde-124">A client can register with each instance of the routing table manager.</span></span>

<span data-ttu-id="7edde-125">Nella figura seguente viene illustrata la correlazione tra le voci della tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="7edde-125">The following illustration shows how the routing table entries are related.</span></span> <span data-ttu-id="7edde-126">Per ulteriori informazioni sulle voci della tabella di routing, vedere [voci della tabella di routing](routing-table-entries.md).</span><span class="sxs-lookup"><span data-stu-id="7edde-126">For more information on routing table entries, see [Routing Table Entries](routing-table-entries.md).</span></span>

![relazione tra le voci della tabella di routing](images/nexthop.png)

<span data-ttu-id="7edde-128">La tabella di routing contiene destinazioni.</span><span class="sxs-lookup"><span data-stu-id="7edde-128">The routing table contains destinations.</span></span> <span data-ttu-id="7edde-129">Ogni destinazione è correlata a una o più route.</span><span class="sxs-lookup"><span data-stu-id="7edde-129">Each destination is related to one or more routes.</span></span> <span data-ttu-id="7edde-130">Ogni route ha zero, uno o più puntatori agli hop successivi associati alla route.</span><span class="sxs-lookup"><span data-stu-id="7edde-130">Each route has zero, one, or more pointers to next hops that are associated with the route.</span></span> <span data-ttu-id="7edde-131">Ogni puntatore si riferisce all'hop successivo effettivo nell'elenco di hop successivi.</span><span class="sxs-lookup"><span data-stu-id="7edde-131">Each pointer refers to the actual next hop in the list of next hops.</span></span> <span data-ttu-id="7edde-132">Ogni client che esegue la registrazione con gestione tabelle di routing crea un elenco di hop successivi di proprietà del client.</span><span class="sxs-lookup"><span data-stu-id="7edde-132">Each client that registers with the routing table manager creates a list of next hops that the client owns.</span></span>

<span data-ttu-id="7edde-133">Le route possono contenere solo puntatori all'elenco di hop successivo associato al client proprietario della route.</span><span class="sxs-lookup"><span data-stu-id="7edde-133">Routes can only contain pointers to the next-hop list associated with the client that owns the route.</span></span>

 

 




