---
description: La rete peer-to-peer è una tecnologia di rete senza server che consente a più dispositivi di rete di condividere le risorse e comunicare direttamente tra loro.
ms.assetid: d2a43d3b-2782-4777-8c65-05e2c52930d0
title: Che cos'è la rete peer?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c456fac9b7695a2846765ee0ccd38c1e5df646e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967528"
---
# <a name="what-is-peer-networking"></a><span data-ttu-id="77ea5-103">Che cos'è la rete peer?</span><span class="sxs-lookup"><span data-stu-id="77ea5-103">What is Peer Networking?</span></span>

<span data-ttu-id="77ea5-104">La rete peer-to-peer è una tecnologia di rete senza server che consente a più dispositivi di rete di condividere le risorse e comunicare direttamente tra loro.</span><span class="sxs-lookup"><span data-stu-id="77ea5-104">Peer-to-peer networking is a serverless networking technology that allows several network devices to share resources and communicate directly with each other.</span></span> <span data-ttu-id="77ea5-105">Questa tecnologia è disponibile per i client Windows XP con Service Pack 1 (SP1) e versioni successive che eseguono Advanced Networking Pack per l'infrastruttura peer-to-peer.</span><span class="sxs-lookup"><span data-stu-id="77ea5-105">This technology is available for Windows XP with Service Pack 1 (SP1) and later clients that run the Advanced Networking Pack for the Peer-to-Peer Infrastructure.</span></span>

<span data-ttu-id="77ea5-106">L'infrastruttura peer-to-peer è un set di API di rete che consentono di sviluppare applicazioni di rete decentralizzate che usano la potenza collettiva dei computer in una rete.</span><span class="sxs-lookup"><span data-stu-id="77ea5-106">The Peer-to-Peer Infrastructure is a set of networking APIs to help you develop decentralized networking applications that use the collective power of computers on a network.</span></span> <span data-ttu-id="77ea5-107">Ad esempio, le applicazioni peer-to-peer possono essere comunicazioni collaborative, tecnologie per la distribuzione di contenuti e così via.</span><span class="sxs-lookup"><span data-stu-id="77ea5-107">For example, peer-to-peer applications can be collaborative communications, content distribution technologies, and so on.</span></span>

<span data-ttu-id="77ea5-108">L'infrastruttura peer-to-peer offre un'infrastruttura di rete solida, che consente di concentrarsi sullo sviluppo di applicazioni, poiché l'infrastruttura è stata sviluppata.</span><span class="sxs-lookup"><span data-stu-id="77ea5-108">The Peer-to-Peer Infrastructure provides a solid networking infrastructure so that you can concentrate on developing applications, because the infrastructure is developed for you.</span></span>

<span data-ttu-id="77ea5-109">L'infrastruttura peer-to-peer include i componenti principali seguenti:</span><span class="sxs-lookup"><span data-stu-id="77ea5-109">The Peer-to-Peer Infrastructure includes the following major components:</span></span>

-   [<span data-ttu-id="77ea5-110">Risoluzione dei nomi peer scalabile e sicura</span><span class="sxs-lookup"><span data-stu-id="77ea5-110">Scalable and secure peer name resolution</span></span>](#scalable-and-secure-peer-name-resolution)
-   [<span data-ttu-id="77ea5-111">Comunicazione multipoint efficiente</span><span class="sxs-lookup"><span data-stu-id="77ea5-111">Efficient multipoint communication</span></span>](#efficient-multipoint-communication)
-   [<span data-ttu-id="77ea5-112">Gestione dei dati distribuiti</span><span class="sxs-lookup"><span data-stu-id="77ea5-112">Distributed data management</span></span>](#distributed-data-management)
-   [<span data-ttu-id="77ea5-113">Identità peer sicure</span><span class="sxs-lookup"><span data-stu-id="77ea5-113">Secure peer identities</span></span>](#secure-peer-identities)
-   [<span data-ttu-id="77ea5-114">Gruppi peer-to-peer sicuri</span><span class="sxs-lookup"><span data-stu-id="77ea5-114">Secure Peer-to-Peer groups</span></span>](#secure-peer-to-peer-groups)

## <a name="scalable-and-secure-peer-name-resolution"></a><span data-ttu-id="77ea5-115">Risoluzione dei nomi peer scalabile e sicura</span><span class="sxs-lookup"><span data-stu-id="77ea5-115">Scalable and Secure Peer Name Resolution</span></span>

<span data-ttu-id="77ea5-116">L' [API del provider dello spazio dei nomi PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) è un protocollo di risoluzione da nome a indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="77ea5-116">The [Peer Name Resolution Protocol (PNRP) Namespace Provider API](pnrp-namespace-provider-api.md) is a name-to-IP resolution protocol.</span></span> <span data-ttu-id="77ea5-117">L'ambito o il contesto IPv6 che include tutti i peer partecipanti è denominato [cloud](clouds.md).</span><span class="sxs-lookup"><span data-stu-id="77ea5-117">The IPv6 scope or context that includes all participating peers is called a [cloud](clouds.md).</span></span> <span data-ttu-id="77ea5-118">PNRP consente ai peer di interagire tra loro all'interno di un cloud.</span><span class="sxs-lookup"><span data-stu-id="77ea5-118">PNRP allows peers to interact with each other within a cloud.</span></span>

## <a name="efficient-multipoint-communication"></a><span data-ttu-id="77ea5-119">Comunicazione multipoint efficiente</span><span class="sxs-lookup"><span data-stu-id="77ea5-119">Efficient Multipoint Communication</span></span>

<span data-ttu-id="77ea5-120">L'infrastruttura peer-to-peer include l' [API Graphing](graphing-api.md) che fornisce una comunicazione multipoint efficiente.</span><span class="sxs-lookup"><span data-stu-id="77ea5-120">The Peer-to-Peer Infrastructure includes the [Graphing API](graphing-api.md) that provides efficient multipoint communication.</span></span> <span data-ttu-id="77ea5-121">Analogamente a PNRP, i grafici peer-to-peer consentono a un set di nodi di interagire e passano i dati tra loro sotto forma di [record](records.md).</span><span class="sxs-lookup"><span data-stu-id="77ea5-121">Like PNRP, peer-to-peer graphing allows a set of nodes to interact, and pass data to and from each other in the form of a [record](records.md).</span></span> <span data-ttu-id="77ea5-122">Ogni record generato o aggiornato da un peer viene inviato a tutti i nodi di un grafo.</span><span class="sxs-lookup"><span data-stu-id="77ea5-122">Each record that a peer generates or updates is sent to all nodes in a graph.</span></span>

## <a name="distributed-data-management"></a><span data-ttu-id="77ea5-123">Gestione dati distribuite</span><span class="sxs-lookup"><span data-stu-id="77ea5-123">Distributed Data Management</span></span>

<span data-ttu-id="77ea5-124">Gestione dati distribuiti archivia automaticamente tutti i record inviati a un grafo peer-to-peer fino alla data di scadenza specificata per ogni record.</span><span class="sxs-lookup"><span data-stu-id="77ea5-124">Distributed data management automatically stores all records sent to a peer-to-peer graph until the specified expiration time for each record.</span></span> <span data-ttu-id="77ea5-125">La rete peer-to-peer garantisce che ogni nodo in un grafo peer-to-peer abbia una visualizzazione simile del database di record.</span><span class="sxs-lookup"><span data-stu-id="77ea5-125">Peer-to-peer networking ensures that each node in a peer-to-peer graph has a similar view of the record database.</span></span> <span data-ttu-id="77ea5-126">Se a un grafo peer-to-peer è associato un modello di sicurezza, il grafo contiene le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="77ea5-126">If a peer-to-peer graph has a security model associated with it, the graph contains the following information:</span></span>

-   <span data-ttu-id="77ea5-127">Utenti che possono e non possono connettersi a un grafo</span><span class="sxs-lookup"><span data-stu-id="77ea5-127">Who can and cannot connect to a graph</span></span>
-   <span data-ttu-id="77ea5-128">Utenti che possono proteggere e convalidare i record in base a criteri definiti esternamente</span><span class="sxs-lookup"><span data-stu-id="77ea5-128">Who can secure and validate records based on externally defined criteria</span></span>

## <a name="secure-peer-identities"></a><span data-ttu-id="77ea5-129">Identità peer sicure</span><span class="sxs-lookup"><span data-stu-id="77ea5-129">Secure Peer Identities</span></span>

<span data-ttu-id="77ea5-130">L'infrastruttura peer-to-peer fornisce un' [API di gestione delle identità](identity-manager-api.md) peer-to-peer che consente di creare, gestire e modificare le identità peer.</span><span class="sxs-lookup"><span data-stu-id="77ea5-130">The Peer-to-Peer Infrastructure provides a Peer-to-Peer [Identity Manager API](identity-manager-api.md) that allows you to create, manage, and manipulate the peer identities.</span></span> <span data-ttu-id="77ea5-131">Le identità peer vengono usate per definire i nomi per gli endpoint sicuri in PNRP e possono rappresentare qualsiasi risorsa che partecipa a una rete peer-to-peer, inclusi i gruppi e i servizi peer-to-peer sicuri.</span><span class="sxs-lookup"><span data-stu-id="77ea5-131">Peer identities are used to define names for secure endpoints in PNRP, and can represent any resource that participates in a peer-to-peer network, including secure peer-to-peer groups and services.</span></span>

## <a name="secure-peer-to-peer-groups"></a><span data-ttu-id="77ea5-132">Gruppi peer-to-peer sicuri</span><span class="sxs-lookup"><span data-stu-id="77ea5-132">Secure Peer-to-Peer Groups</span></span>

<span data-ttu-id="77ea5-133">L' [API di raggruppamento](grouping-api.md) peer-to-peer combina le API peer-to-Peer Graphing, Identity Manager e PNRP per formare una soluzione coerente e pratica per lo sviluppo di applicazioni di rete peer-to-peer.</span><span class="sxs-lookup"><span data-stu-id="77ea5-133">The Peer-to-Peer [Grouping API](grouping-api.md) combines the Peer-to-Peer Graphing, Identity Manager, and PNRP APIs to form a cohesive and convenient solution for peer-to-peer networking application development.</span></span> <span data-ttu-id="77ea5-134">L'API di raggruppamento peer-to-peer usa l'API di gestione delle identità peer-to-peer e uno schema di certificato autofirmato per garantire la sicurezza all'interno dell'infrastruttura di Graphing.</span><span class="sxs-lookup"><span data-stu-id="77ea5-134">The Peer-to-Peer Grouping API uses the Peer-to-Peer Identity Manager API and a self-signed certificate scheme to ensure security within the graphing infrastructure.</span></span> <span data-ttu-id="77ea5-135">Ogni gruppo può essere risolto e registrato tramite PNRP, che consente la risoluzione dei nomi dei peer casuali all'interno di un gruppo peer-to-peer registrato.</span><span class="sxs-lookup"><span data-stu-id="77ea5-135">Each group can be resolved and registered through PNRP, which allows for the name resolution of random peers within a registered peer-to-peer group.</span></span> <span data-ttu-id="77ea5-136">Un gruppo può essere un endpoint in PNRP, proprio come un peer.</span><span class="sxs-lookup"><span data-stu-id="77ea5-136">A group can be an endpoint in PNRP, just like a peer.</span></span>

<span data-ttu-id="77ea5-137">Per una panoramica dell'infrastruttura peer-to-peer, vedere l'articolo "[Introduzione alla rete peer-to-peer di Windows XP](https://www.microsoft.com/windowsxp/pro/techinfo/administration/p2p/introduction.asp)".</span><span class="sxs-lookup"><span data-stu-id="77ea5-137">For an overview of the Peer-to-Peer Infrastructure, see the article "[Introduction to Windows XP Peer-to-Peer Networking](https://www.microsoft.com/windowsxp/pro/techinfo/administration/p2p/introduction.asp)".</span></span>

<span data-ttu-id="77ea5-138">Per una panoramica delle API nell'infrastruttura peer-to-peer, vedere l'argomento relativo [all'infrastruttura peer](what-is-the-peer-infrastructure-.md).</span><span class="sxs-lookup"><span data-stu-id="77ea5-138">For an overview of the APIs in the Peer-to-Peer Infrastructure, see the topic [What is the Peer Infrastructure?](what-is-the-peer-infrastructure-.md).</span></span>

 

 



