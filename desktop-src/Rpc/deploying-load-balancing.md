---
title: Distribuzione del bilanciamento del carico
description: Distribuzione del bilanciamento del carico
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00430e8e93334c04dc74c57fc8b50db7d3c899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221221"
---
# <a name="deploying-load-balancing"></a><span data-ttu-id="8e961-103">Distribuzione del bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="8e961-103">Deploying Load Balancing</span></span>

<span data-ttu-id="8e961-104">L'ambiente di distribuzione tipico e il caso d'uso sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e961-104">The typical deployment environment and use case is which the RPC Load balancer is utilized is shown below:</span></span>![bilanciamento del carico RPC](images/rpc-load-balancing.png)

1.  <span data-ttu-id="8e961-106">Il client RPC esegue una connessione RPC/HTTP al server farm.</span><span class="sxs-lookup"><span data-stu-id="8e961-106">The RPC client makes an RPC/HTTP connection to the server farm.</span></span>
2.  <span data-ttu-id="8e961-107">La connessione viene trasmessa attraverso la rete a un servizio di bilanciamento del carico front-end</span><span class="sxs-lookup"><span data-stu-id="8e961-107">The connection is forwarded through the network to a front end load balancer</span></span>
3.  <span data-ttu-id="8e961-108">Il servizio di bilanciamento del carico front-end sceglie un server per la manutenzione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="8e961-108">The front end load balancer chooses a server to service the request.</span></span> <span data-ttu-id="8e961-109">In questo esempio il servizio di bilanciamento del carico front-end trasmette la connessione al server 1.</span><span class="sxs-lookup"><span data-stu-id="8e961-109">In this example, the front end load balancer forwards the connection to Server 1.</span></span>
4.  <span data-ttu-id="8e961-110">Il servizio di bilanciamento del carico RPC arbitraggio la connessione.</span><span class="sxs-lookup"><span data-stu-id="8e961-110">The RPC Load balancer service arbitrates the connection.</span></span> <span data-ttu-id="8e961-111">Determina che si tratta della prima connessione dal client e associa la connessione al server locale, server 1.</span><span class="sxs-lookup"><span data-stu-id="8e961-111">It determines that this is the first connection from the client and associates the connection with the local server, Server 1.</span></span>
5.  <span data-ttu-id="8e961-112">Il client effettua una seconda richiesta RPC/HTTP.</span><span class="sxs-lookup"><span data-stu-id="8e961-112">The client makes a second RPC/HTTP request.</span></span>
6.  <span data-ttu-id="8e961-113">La richiesta viene trasmessa attraverso la rete al servizio di bilanciamento del carico front-end.</span><span class="sxs-lookup"><span data-stu-id="8e961-113">The request is forwarded through the network to the front end load balancer.</span></span>
7.  <span data-ttu-id="8e961-114">Il servizio di bilanciamento del carico front-end sceglie un server per la manutenzione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="8e961-114">The front end load balancer chooses a server to service the request.</span></span> <span data-ttu-id="8e961-115">In questo caso, il servizio di bilanciamento del carico front-end sceglie il server 2 per servire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="8e961-115">In this case, the front end load balancer chooses Server 2 to service the request.</span></span>
8.  <span data-ttu-id="8e961-116">Il servizio RPC Load Balancer arbitraggio la connessione.</span><span class="sxs-lookup"><span data-stu-id="8e961-116">The RPC Load Balancer service arbitrates the connection.</span></span> <span data-ttu-id="8e961-117">Riconosce che le connessioni da questo client vengono gestite dal server 1.</span><span class="sxs-lookup"><span data-stu-id="8e961-117">It recognizes that connections from this client is being serviced by Server 1.</span></span>
9.  <span data-ttu-id="8e961-118">La connessione viene trasmessa al server 1.</span><span class="sxs-lookup"><span data-stu-id="8e961-118">The connection is forwarded to Server 1.</span></span>

 

 




