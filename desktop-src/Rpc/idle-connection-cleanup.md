---
title: Pulizia della connessione inattiva
description: Per impostazione predefinita, le connessioni nel pool di thread non vengono chiuse fino a quando l'intera associazione non viene arrestata.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75587781991c2aae86968d90c9da51331d7a29e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855622"
---
# <a name="idle-connection-cleanup"></a><span data-ttu-id="febf4-103">Pulizia della connessione inattiva</span><span class="sxs-lookup"><span data-stu-id="febf4-103">Idle Connection Cleanup</span></span>

<span data-ttu-id="febf4-104">Per impostazione predefinita, le connessioni nel pool di thread non vengono chiuse fino a quando l'intera associazione non viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="febf4-104">By default, connections in the thread pool are not closed until the whole association is shut down.</span></span> <span data-ttu-id="febf4-105">Questo criterio consente ai client con un numero elevato di thread o identità di sicurezza di eseguire chiamate RPC al server in modo efficiente.</span><span class="sxs-lookup"><span data-stu-id="febf4-105">This policy enables clients with a large number of threads or security identities to make RPC calls to the server in an efficient manner.</span></span> <span data-ttu-id="febf4-106">Lo svantaggio è che una quantità inordinata di risorse può essere impegnata a gestire tali connessioni.</span><span class="sxs-lookup"><span data-stu-id="febf4-106">The drawback is that an inordinate amount of resources may be committed to maintaining those connections.</span></span> <span data-ttu-id="febf4-107">Per gestire il processo, RPC fornisce la funzione [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) .</span><span class="sxs-lookup"><span data-stu-id="febf4-107">To manage the process, RPC provides the [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) function.</span></span> <span data-ttu-id="febf4-108">Questa funzione Abilita la pulizia della connessione inattiva; il client analizza periodicamente il pool di connessioni e chiude le connessioni che non sono state usate di recente.</span><span class="sxs-lookup"><span data-stu-id="febf4-108">This function enables idle connection cleanup; the client periodically scans the connection pool and closes connections that have not been recently used.</span></span> <span data-ttu-id="febf4-109">Se l'associazione ha mantenuto handle del contesto, la pulizia della connessione inattiva chiude tutte le connessioni inattive, ma verifica che almeno una connessione venga lasciata aperta, anche se la connessione è inattiva (in caso contrario, il server ottiene le esecuzioni dell'handle del contesto).</span><span class="sxs-lookup"><span data-stu-id="febf4-109">If the association has maintained context handles, the idle connection cleanup closes all idle connections, but makes sure at least one connection is left open, even if the connection is idle (otherwise the server gets context handle run downs).</span></span> <span data-ttu-id="febf4-110">Se l'associazione non ha mantenuto gli handle del contesto, la pulizia della connessione inattiva chiude tutte le connessioni inattive, anche se in questo modo non si lascia alcuna connessione nel pool.</span><span class="sxs-lookup"><span data-stu-id="febf4-110">If the association has not maintained context handles, idle connection cleanup closes all idle connections, even if doing so leaves no connections in the pool.</span></span>

<span data-ttu-id="febf4-111">In Windows XP, il tempo di esecuzione RPC tiene traccia del numero di connessioni aperte in un'associazione e attiva automaticamente la pulizia della connessione inattiva se il numero di connessioni in qualsiasi associazione supera una determinata soglia.</span><span class="sxs-lookup"><span data-stu-id="febf4-111">On Windows XP, the RPC run time keeps track of the number of open connections in an association, and automatically turns on idle connection cleanup if the number of connections in any association exceeds a certain threshold.</span></span>

 

 




