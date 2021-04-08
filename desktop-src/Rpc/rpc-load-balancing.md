---
title: Bilanciamento del carico RPC
description: Bilanciamento del carico RPC
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4039742fcfcc67280c610270908bed51034f691a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044157"
---
# <a name="rpc-load-balancing"></a><span data-ttu-id="28abe-103">Bilanciamento del carico RPC</span><span class="sxs-lookup"><span data-stu-id="28abe-103">RPC Load Balancing</span></span>

<span data-ttu-id="28abe-104">Il bilanciamento del carico di Microsoft RPC è progettato per offrire una soluzione scalabile per gli scenari che richiedono un elevato carico di [RPC sul traffico http](remote-procedure-calls-using-rpc-over-http.md) .</span><span class="sxs-lookup"><span data-stu-id="28abe-104">Microsoft RPC Load Balancing is intended to provide a scalable solution for scenarios which demand a high load of [RPC over HTTP](remote-procedure-calls-using-rpc-over-http.md) traffic.</span></span> <span data-ttu-id="28abe-105">Lo scopo principale del Load Balancer RPC è garantire che il traffico RPC/HTTP possa essere gestito da un server farm per migliorare la scalabilità.</span><span class="sxs-lookup"><span data-stu-id="28abe-105">The RPC Load Balancer’s primary purpose is to ensure RPC/HTTP traffic can be serviced by a server farm to improve scalability.</span></span> <span data-ttu-id="28abe-106">Per ottenere questo risultato, RPC deve garantire che tutte le connessioni da un processo client siano gestite dallo stesso endpoint server nel server farm.</span><span class="sxs-lookup"><span data-stu-id="28abe-106">To achieve this, RPC must ensure that all connections from a client process are serviced by the same server endpoint in the server farm.</span></span> <span data-ttu-id="28abe-107">Il Load Balancer RPC viene implementato come un servizio che viene eseguito insieme al servizio proxy RPC su HTTP.</span><span class="sxs-lookup"><span data-stu-id="28abe-107">The RPC Load Balancer is implemented as a service which runs in conjunction with the RPC over HTTP Proxy service.</span></span>

<span data-ttu-id="28abe-108">Per abilitare il bilanciamento del carico, il servizio di bilanciamento del carico RPC in esecuzione su ogni server comunica tra loro per determinare il server preferito per la connessione client iniziale.</span><span class="sxs-lookup"><span data-stu-id="28abe-108">To enable load balancing, the RPC Load Balancing service running on each of the servers communicates with each other to determine the preferred server for the initial client connection.</span></span> <span data-ttu-id="28abe-109">Questo processo viene chiamato arbitraggio e si verifica al momento della connessione iniziale del client.</span><span class="sxs-lookup"><span data-stu-id="28abe-109">This process is called arbitration and it occurs at the time of the initial client connection.</span></span> <span data-ttu-id="28abe-110">Per ridurre il traffico tra server, il servizio di bilanciamento del carico RPC sceglie l'endpoint locale per servire la connessione se il client non è già associato a un server.</span><span class="sxs-lookup"><span data-stu-id="28abe-110">To reduce cross server traffic, the RPC Load Balancing service chooses the local endpoint to service the connection if the client is not already associated with a server.</span></span> <span data-ttu-id="28abe-111">Per una determinata connessione client, il risultato dell'arbitraggio è una delle due opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="28abe-111">For a given client connection, the outcome of arbitration is one of two possibilities:</span></span>

-   <span data-ttu-id="28abe-112">Se il client ha già eseguito una connessione, il server per la prima ricezione della connessione gestirà le connessioni successive.</span><span class="sxs-lookup"><span data-stu-id="28abe-112">If the client has already made a connection, the server to first receive the connection will handle the subsequent connections.</span></span>
-   <span data-ttu-id="28abe-113">Se si tratta della prima connessione dal client, l'arbitraggio comporterà la gestione della connessione da parte del server locale e quindi tutte le connessioni dal client.</span><span class="sxs-lookup"><span data-stu-id="28abe-113">If this is the first connection from the client, arbitration will result in the local server handling the connection, and thus all connections from the client.</span></span> <span data-ttu-id="28abe-114">Queste informazioni, una volta determinate, verranno sottoposte a commit per gli altri servizi RPC Load Balancer nel server farm, in modo da informarli del server che gestisce tutte le richieste del client.</span><span class="sxs-lookup"><span data-stu-id="28abe-114">This information, once determined, will be committed to the other RPC Load Balancer services in the server farm, thus informing them of the server handling all of the client’s requests.</span></span>

<span data-ttu-id="28abe-115">In questa sezione viene fornita una panoramica del bilanciamento del carico RPC negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="28abe-115">This section provides an overview of RPC Load Balancing in the following topics:</span></span>

-   [<span data-ttu-id="28abe-116">Distribuzione del bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="28abe-116">Deploying Load Balancing</span></span>](deploying-load-balancing.md)
-   [<span data-ttu-id="28abe-117">Configurazione del bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="28abe-117">Configuring Load Balancing</span></span>](configuring-load-balancing.md)
-   [<span data-ttu-id="28abe-118">Procedure consigliate per il bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="28abe-118">Load Balancing Best Practices</span></span>](load-balancing-best-practices.md)

## <a name="requirements"></a><span data-ttu-id="28abe-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28abe-119">Requirements</span></span>

<span data-ttu-id="28abe-120">Il servizio di bilanciamento del carico RPC è supportato nei server che eseguono Windows Server 2008 R2 o versione successiva e i client che eseguono Windows 7 o versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="28abe-120">The RPC Load Balancing service is supported on servers running Windows Server 2008 R2 or later and clients running Windows 7 or later versions of Windows.</span></span>

<span data-ttu-id="28abe-121">Il servizio proxy RPC, il servizio di bilanciamento del carico RPC e gli endpoint server devono essere tutti in esecuzione nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="28abe-121">The RPC Proxy service, the RPC Load Balancing service and the server endpoints must all be running on the same machine.</span></span> <span data-ttu-id="28abe-122">Inoltre, tutti i server nel server farm devono essere in grado di gestire l'endpoint richiesto.</span><span class="sxs-lookup"><span data-stu-id="28abe-122">Additionally, all servers in the server farm must be capable of servicing the requested endpoint.</span></span> <span data-ttu-id="28abe-123">Per informazioni sulla configurazione del servizio proxy RPC e del servizio di bilanciamento del carico RPC, vedere [configurazione dei computer per RPC su http](configuring-computers-for-rpc-over-http.md) e [configurazione del bilanciamento del carico](configuring-load-balancing.md), rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="28abe-123">For information on configuring the RPC Proxy service and the RPC Load Balancing service, see [Configuring Computers for RPC over HTTP](configuring-computers-for-rpc-over-http.md) and [Configuring Load Balancing](configuring-load-balancing.md), respectively.</span></span>

## <a name="limitations"></a><span data-ttu-id="28abe-124">Limitazioni</span><span class="sxs-lookup"><span data-stu-id="28abe-124">Limitations</span></span>

<span data-ttu-id="28abe-125">A questo punto, il bilanciamento del carico RPC supporta solo un server farm per risorsa.</span><span class="sxs-lookup"><span data-stu-id="28abe-125">At this time, RPC Load Balancing supports only one server farm per resource.</span></span> <span data-ttu-id="28abe-126">Tutti i server in tutte le server farm devono essere in grado di gestire anche tutte le risorse.</span><span class="sxs-lookup"><span data-stu-id="28abe-126">All servers in all server farms must be capable of servicing all resources as well.</span></span>

 

 




