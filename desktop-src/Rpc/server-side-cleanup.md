---
title: Pulizia lato server
description: Pulizia lato server e RPC (Remote Procedure Call).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a66272fc3cca209d6825ac34d5158094ddff39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044973"
---
# <a name="server-side-cleanup"></a><span data-ttu-id="c8bc2-103">Pulizia lato server</span><span class="sxs-lookup"><span data-stu-id="c8bc2-103">Server-side Cleanup</span></span>

<span data-ttu-id="c8bc2-104">Si immagini lo scenario seguente:</span><span class="sxs-lookup"><span data-stu-id="c8bc2-104">Imagine the following scenario:</span></span>

<span data-ttu-id="c8bc2-105">Un client apre un handle di contesto e quindi interrompe o perde la connettività al server.</span><span class="sxs-lookup"><span data-stu-id="c8bc2-105">A client opens a context handle, and then either stops or loses connectivity to the server.</span></span> <span data-ttu-id="c8bc2-106">In che modo il server rileva che il client ha avuto esito negativo e l'handle del contesto dovrebbe essere disattivato?</span><span class="sxs-lookup"><span data-stu-id="c8bc2-106">How does the server detect that the client has failed and the context handle should be run down?</span></span> <span data-ttu-id="c8bc2-107">Esistono due Sottoscenari: uno è che il client viene arrestato in modo ordinato.</span><span class="sxs-lookup"><span data-stu-id="c8bc2-107">There are two subscenarios: one is that the client is shut down in an orderly manner.</span></span> <span data-ttu-id="c8bc2-108">In tal caso, viene inviata una notifica al server che sta per essere arrestata e il server è in grado di eseguire la pulizia, incluse le esecuzioni del contesto.</span><span class="sxs-lookup"><span data-stu-id="c8bc2-108">In such case, it notifies the server that it is shutting down, and the server can clean up, including performing context run downs.</span></span> <span data-ttu-id="c8bc2-109">Se il client non viene arrestato in modo ordinato o non può inviare una notifica al server, il server utilizza keep alive per determinare se il client è ancora disponibile.</span><span class="sxs-lookup"><span data-stu-id="c8bc2-109">If the client does not shut down in an orderly manner or it cannot notify the server, the server uses keep alives to determine whether the client is still available.</span></span> <span data-ttu-id="c8bc2-110">Sul lato server, la funzione [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="c8bc2-110">On the server side, the [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) function has no effect.</span></span> <span data-ttu-id="c8bc2-111">Al contrario, il server usa l'impostazione globale per computer-Keep-Alive, che per impostazione predefinita è di circa due ore.</span><span class="sxs-lookup"><span data-stu-id="c8bc2-111">Instead, the server uses the global per machine–keep alive setting, which defaults to approximately two hours.</span></span> <span data-ttu-id="c8bc2-112">Se il client non risponde alle Keep-Alive del server, la connessione viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="c8bc2-112">If the client does not respond to the server's keep alives, the connection is closed.</span></span> <span data-ttu-id="c8bc2-113">Quando tutte le connessioni a un determinato processo client vengono chiuse, il server pulisce ed esegue gli handle di contesto in attesa.</span><span class="sxs-lookup"><span data-stu-id="c8bc2-113">When all connections to a given client process are closed, the server cleans up and runs down outstanding context handles.</span></span>

 

 




