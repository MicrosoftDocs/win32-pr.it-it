---
title: Protocollo di routing
description: Un protocollo di routing è un tipo di client che esegue la registrazione con gestione tabelle di routing. I router utilizzano i protocolli di routing per scambiare informazioni riguardanti le route a una destinazione.
ms.assetid: 957ec896-94e3-4bdb-801a-12b861460fff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e64d12912494d0d6c20f484eba588b47670a808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044619"
---
# <a name="routing-protocol"></a><span data-ttu-id="7c31a-104">Protocollo di routing</span><span class="sxs-lookup"><span data-stu-id="7c31a-104">Routing Protocol</span></span>

<span data-ttu-id="7c31a-105">Un protocollo di routing è un tipo di client che esegue la registrazione con gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="7c31a-105">A routing protocol is a type of client that registers with the routing table manager.</span></span> <span data-ttu-id="7c31a-106">I router utilizzano i protocolli di routing per scambiare informazioni riguardanti le route a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="7c31a-106">Routers use routing protocols to exchange information regarding routes to a destination.</span></span>

<span data-ttu-id="7c31a-107">I protocolli di routing sono unicast o multicast.</span><span class="sxs-lookup"><span data-stu-id="7c31a-107">Routing protocols are either unicast or multicast.</span></span> <span data-ttu-id="7c31a-108">I protocolli di routing annunciano le route a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="7c31a-108">Routing protocols advertise routes to a destination.</span></span>

<span data-ttu-id="7c31a-109">Una route unicast a una destinazione viene utilizzata da un protocollo di routing unicast per inoltrare i dati unicast a tale destinazione.</span><span class="sxs-lookup"><span data-stu-id="7c31a-109">A unicast route to a destination is used by a unicast routing protocol to forward unicast data to that destination.</span></span> <span data-ttu-id="7c31a-110">Tra gli esempi di protocolli di routing unicast sono inclusi: Routing Information Protocol (RIP), Open Short Path First (OSPF) e Border Gateway Protocol (BGP).</span><span class="sxs-lookup"><span data-stu-id="7c31a-110">Examples of unicast routing protocols include: Routing Information Protocol (RIP), Open Shortest Path First (OSPF), and Border Gateway Protocol (BGP).</span></span>

<span data-ttu-id="7c31a-111">Una route multicast a una destinazione viene utilizzata da alcuni protocolli di routing multicast per creare le informazioni utilizzate per inoltrare i dati multicast dagli host nella rete di destinazione della route (noto come inoltro del percorso inverso). Esempi di protocolli di routing multicast sono: multicast Open Short Path First (MOSPF), Distance Vector Multicast Routing Protocol (DVMRP) e Protocol Independent Multicast (PIM).</span><span class="sxs-lookup"><span data-stu-id="7c31a-111">A multicast route to a destination is used by some multicast routing protocols to create the information that is used to forward multicast data from hosts on the destination network of the route (known as reverse path forwarding).Examples of multicast routing protocols include: Multicast Open Shortest Path First (MOSPF), Distance Vector Multicast Routing Protocol (DVMRP), and Protocol Independent Multicast (PIM).</span></span>

<span data-ttu-id="7c31a-112">Gestione tabelle di routing supporta più istanze dello stesso protocollo, ad esempio l'implementazione Microsoft di OSPF e un OSPF di terze parti, in esecuzione sul router.</span><span class="sxs-lookup"><span data-stu-id="7c31a-112">The routing table manager supports multiple instances of the same protocol (such as Microsoft's implementation of OSPF and a third-party OSPF) running on the router.</span></span> <span data-ttu-id="7c31a-113">Questo consente ai router di usare le diverse funzionalità di ogni versione.</span><span class="sxs-lookup"><span data-stu-id="7c31a-113">This allows routers to use the different capabilities of each version.</span></span> <span data-ttu-id="7c31a-114">Questi protocolli hanno identificatori di protocollo diversi.</span><span class="sxs-lookup"><span data-stu-id="7c31a-114">These protocols have different protocol identifiers.</span></span>

<span data-ttu-id="7c31a-115">Gli identificatori di protocollo sono costituiti da un identificatore del fornitore e da un identificatore specifico del protocollo.</span><span class="sxs-lookup"><span data-stu-id="7c31a-115">Protocol identifiers are comprised of a vendor identifier and a protocol-specific identifier.</span></span> <span data-ttu-id="7c31a-116">L'identificatore specifico del protocollo è identico per le diverse implementazioni del protocollo, ad esempio l'implementazione di OSPF di Microsoft e un'implementazione di terze parti di OSPF.</span><span class="sxs-lookup"><span data-stu-id="7c31a-116">The protocol-specific identifier is the same for different implementations of the protocol, such as Microsoft's implementation of OSPF and a third-party implementation of OSPF.</span></span> <span data-ttu-id="7c31a-117">Solo quando vengono combinati gli identificatori specifici del fornitore e del protocollo, esiste un identificatore univoco per un protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="7c31a-117">Only when the vendor and protocol-specific identifiers are combined is there a unique identifier for a routing protocol.</span></span>

<span data-ttu-id="7c31a-118">Un protocollo con lo stesso identificatore di protocollo (ovvero lo stesso identificatore del fornitore e identificatore specifico del protocollo) può registrare più volte con gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="7c31a-118">A protocol with the same protocol identifier (that is, the same vendor identifier and protocol-specific identifier) can register with the routing table manager multiple times.</span></span> <span data-ttu-id="7c31a-119">Ogni volta, il protocollo viene registrato utilizzando un identificatore di istanza di protocollo diverso.</span><span class="sxs-lookup"><span data-stu-id="7c31a-119">Each time, the protocol registers using a different protocol instance identifier.</span></span> <span data-ttu-id="7c31a-120">Ad esempio, un'implementazione di OSPF da un particolare fornitore può essere registrata come vendor-OSPF-1 e vendor-OSPF-2.</span><span class="sxs-lookup"><span data-stu-id="7c31a-120">For example, an implementation of OSPF from a particular vendor can register as Vendor-OSPF-1 and Vendor-OSPF-2.</span></span> <span data-ttu-id="7c31a-121">Questo consente a un'implementazione del protocollo specifica di partizionare le informazioni che mantiene nella tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="7c31a-121">This enables a specific protocol implementation to partition the information that it keeps in the routing table.</span></span>

 

 




