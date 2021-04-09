---
title: Metodi using
description: Quando un client esegue la registrazione con gestione tabelle di routing, può esportare un set di metodi. Questi metodi vengono usati da altri client per ottenere informazioni specifiche del client. I metodi consentono la comunicazione privata tra i client di gestione tabelle di routing.
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd895fbb3f8f54224522786b5794c5c6c57a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955551"
---
# <a name="using-methods"></a><span data-ttu-id="2efd1-105">Metodi using</span><span class="sxs-lookup"><span data-stu-id="2efd1-105">Using Methods</span></span>

<span data-ttu-id="2efd1-106">Quando un client esegue la registrazione con gestione tabelle di routing, può esportare un set di metodi.</span><span class="sxs-lookup"><span data-stu-id="2efd1-106">When a client registers with the routing table manager, it can export a set of methods.</span></span> <span data-ttu-id="2efd1-107">Questi metodi vengono usati da altri client per ottenere informazioni specifiche del client.</span><span class="sxs-lookup"><span data-stu-id="2efd1-107">These methods are used by other clients to obtain client-specific information.</span></span> <span data-ttu-id="2efd1-108">I metodi consentono la comunicazione privata tra i client di gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="2efd1-108">Methods enable private communication between clients of the routing table manager.</span></span>

<span data-ttu-id="2efd1-109">Un client può ottenere l'elenco dei metodi esportati da un altro client.</span><span class="sxs-lookup"><span data-stu-id="2efd1-109">A client can obtain the list of methods exported by another client.</span></span> <span data-ttu-id="2efd1-110">Il client chiama la funzione [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) , specificando l'handle del client di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2efd1-110">The client calls the [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) function, supplying the target client's handle.</span></span>

<span data-ttu-id="2efd1-111">Ogni metodo esportato da un client viene identificato in modo univoco dal relativo identificatore del metodo.</span><span class="sxs-lookup"><span data-stu-id="2efd1-111">Each method exported by a client is uniquely identified by its method identifier.</span></span> <span data-ttu-id="2efd1-112">Ogni client può esportare fino a 32 metodi.</span><span class="sxs-lookup"><span data-stu-id="2efd1-112">Each client can export up to 32 methods.</span></span> <span data-ttu-id="2efd1-113">Ogni metodo corrisponde a un bit impostato nel membro **MethodType** della struttura del [**\_ metodo di \_ esportazione \_ dell'entità RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) .</span><span class="sxs-lookup"><span data-stu-id="2efd1-113">Each method corresponds to a bit set in the **MethodType** member of the [**RTM\_ENTITY\_EXPORT\_METHOD**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) structure.</span></span> <span data-ttu-id="2efd1-114">Per richiamare più metodi, il client deve eseguire un OR logico degli identificatori per tali metodi.</span><span class="sxs-lookup"><span data-stu-id="2efd1-114">To invoke multiple methods, the client should perform a logical OR of the identifiers for those methods.</span></span> <span data-ttu-id="2efd1-115">Quando il protocollo è implementato, è necessario specificare la sintassi e la semantica delle strutture di input e di output per ogni protocollo.</span><span class="sxs-lookup"><span data-stu-id="2efd1-115">The syntax and semantics of input and output structures for each protocol must be specified when the protocol is implemented.</span></span>

> [!Note]  
> <span data-ttu-id="2efd1-116">I valori dell'identificatore di metodo che corrispondono a un bit impostato nella metà inferiore del membro **MethodType** (i 16 bit inferiori) sono riservati da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2efd1-116">Method identifier values that correspond to a bit set in the lower half of the **MethodType** member (the lower 16 bits) are reserved by Microsoft.</span></span>

 

<span data-ttu-id="2efd1-117">Per richiamare un secondo metodo del client, un client chiama la funzione [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) .</span><span class="sxs-lookup"><span data-stu-id="2efd1-117">To invoke a second client's method, a client calls the [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) function.</span></span> <span data-ttu-id="2efd1-118">Gestione tabelle di routing arbitraggio tutte le richieste per richiamare i metodi di un client.</span><span class="sxs-lookup"><span data-stu-id="2efd1-118">The routing table manager arbitrates all requests to invoke a client's methods.</span></span> <span data-ttu-id="2efd1-119">Gestione tabelle di routing esegue due funzioni quando arbitraggio tra i client:</span><span class="sxs-lookup"><span data-stu-id="2efd1-119">The routing table manager performs two functions when it arbitrates between clients:</span></span>

-   <span data-ttu-id="2efd1-120">Impedire al secondo client di richiamare un metodo per un client che sta annullando la registrazione.</span><span class="sxs-lookup"><span data-stu-id="2efd1-120">Preventing the second client from invoking a method for a client that is unregistering.</span></span>
-   <span data-ttu-id="2efd1-121">Con una richiesta "Invoke" quando i metodi sono bloccati e consentendo la continuazione della richiesta quando i metodi vengono sbloccati.</span><span class="sxs-lookup"><span data-stu-id="2efd1-121">Holding an "invoke" request when methods are blocked, and allowing the request to continue when the methods are unblocked.</span></span>

<span data-ttu-id="2efd1-122">Se un client deve impedire l'esecuzione dei metodi di altri client, il client può chiamare [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods).</span><span class="sxs-lookup"><span data-stu-id="2efd1-122">If a client must prevent other clients from executing its methods, the client can call [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods).</span></span> <span data-ttu-id="2efd1-123">Gestione tabelle di routing non consente l'elaborazione di una chiamata a [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) fino a quando il client non sblocca nuovamente i relativi metodi.</span><span class="sxs-lookup"><span data-stu-id="2efd1-123">The routing table manager will not allow a call to [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) to be processed until the client unblocks its methods again.</span></span>

<span data-ttu-id="2efd1-124">I client in genere bloccano i metodi quando si apportano modifiche ai dati privati scambiati tra i client.</span><span class="sxs-lookup"><span data-stu-id="2efd1-124">Clients typically block methods when making changes to the private data that is exchanged between clients.</span></span> <span data-ttu-id="2efd1-125">I metodi di blocco sono un'azione facoltativa.</span><span class="sxs-lookup"><span data-stu-id="2efd1-125">Blocking methods is an optional action.</span></span> <span data-ttu-id="2efd1-126">Un client può inoltre utilizzare blocchi interni per impedire che altri client richiamino metodi.</span><span class="sxs-lookup"><span data-stu-id="2efd1-126">A client can also use internal locks to prevent other clients from invoking methods.</span></span>

<span data-ttu-id="2efd1-127">Per il codice di esempio che illustra come usare queste funzioni, vedere [ottenere e chiamare i metodi esportati per un client](obtain-and-call-the-exported-methods-for-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="2efd1-127">For sample code that shows how to use these functions, see [Obtain and Call the Exported Methods for a Client](obtain-and-call-the-exported-methods-for-a-client.md).</span></span>

 

 




