---
title: Connessione del client e del server
description: Per comunicare, i programmi client e server devono stabilire una sessione di comunicazione attraverso la rete o le reti che li collegano.
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- RPC (Remote Procedure Call), attività, connessione di client e server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a22ea7a9a6dd30f2b9495b6d2ee868aac217f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471390"
---
# <a name="connecting-the-client-and-the-server"></a><span data-ttu-id="b5d9b-104">Connessione del client e del server</span><span class="sxs-lookup"><span data-stu-id="b5d9b-104">Connecting the Client and the Server</span></span>

<span data-ttu-id="b5d9b-105">Per comunicare, i programmi client e server devono stabilire una sessione di comunicazione attraverso la rete o le reti che li collegano.</span><span class="sxs-lookup"><span data-stu-id="b5d9b-105">To communicate, client and server programs must establish a communication session across the network or networks that connect them.</span></span> <span data-ttu-id="b5d9b-106">Una volta stabilita la connessione, il client può chiamare le procedure remote nel programma server come se fossero locali per il programma client.</span><span class="sxs-lookup"><span data-stu-id="b5d9b-106">Once they establish the connection, the client can call remote procedures in the server program as if they were local to the client program.</span></span>

<span data-ttu-id="b5d9b-107">In questa sezione viene fornita una panoramica concettuale su come stabilire una connessione tra client e server per chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="b5d9b-107">This section provides a conceptual overview of how to establish a connection between clients and servers for remote procedure calls.</span></span> <span data-ttu-id="b5d9b-108">Non fornisce una descrizione approfondita di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="b5d9b-108">It does not provide an in-depth discussion of this topic.</span></span> <span data-ttu-id="b5d9b-109">Tutti i concetti illustrati in questa sezione sono descritti in dettaglio nei capitoli successivi e nella sezione riferimento alle funzioni RPC.</span><span class="sxs-lookup"><span data-stu-id="b5d9b-109">All of the concepts in this section are presented in detail in later chapters and in the RPC Function Reference section.</span></span>

<span data-ttu-id="b5d9b-110">La discussione presentata in questa sezione è divisa negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="b5d9b-110">The discussion presented in this section is divided into the following topics:</span></span>

-   [<span data-ttu-id="b5d9b-111">Terminologia di associazione RPC essenziale</span><span class="sxs-lookup"><span data-stu-id="b5d9b-111">Essential RPC Binding Terminology</span></span>](essential-rpc-binding-terminology.md)
-   [<span data-ttu-id="b5d9b-112">Preparazione del server per una connessione</span><span class="sxs-lookup"><span data-stu-id="b5d9b-112">How the Server Prepares for a Connection</span></span>](how-the-server-prepares-for-a-connection.md)
-   [<span data-ttu-id="b5d9b-113">Come il client stabilisce una connessione</span><span class="sxs-lookup"><span data-stu-id="b5d9b-113">How the Client Establishes a Connection</span></span>](how-the-client-establishes-a-connection.md)

<span data-ttu-id="b5d9b-114">Si noti che la discussione presuppone handle di binding espliciti.</span><span class="sxs-lookup"><span data-stu-id="b5d9b-114">Note that the discussion assumes explicit binding handles.</span></span> <span data-ttu-id="b5d9b-115">Tuttavia, se l'applicazione usa altri tipi di handle di associazione, potrebbe essere necessario modificare i passaggi presentati in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="b5d9b-115">However, if your application uses other types of binding handles, you may have to modify the steps presented in this section.</span></span> <span data-ttu-id="b5d9b-116">Per ulteriori informazioni, vedere [Binding e handle](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="b5d9b-116">For more information, see [Binding and Handles](binding-and-handles.md).</span></span>

 

 




