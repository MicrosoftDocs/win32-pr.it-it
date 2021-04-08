---
title: Ascolto delle chiamate a procedure remote
description: Dopo che un programma server ha registrato le informazioni di binding e ne annuncia la presenza in un database del servizio dei nomi, può iniziare l'ascolto dell'endpoint per le chiamate di procedura remota.
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d9463e0591279377502394541190be685cccd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044000"
---
# <a name="listening-for-remote-procedure-calls"></a><span data-ttu-id="04a43-103">Ascolto delle chiamate a procedure remote</span><span class="sxs-lookup"><span data-stu-id="04a43-103">Listening for Remote Procedure Calls</span></span>

<span data-ttu-id="04a43-104">Dopo che un programma server ha registrato le informazioni di binding e ne annuncia la presenza in un database del servizio dei nomi, può iniziare l'ascolto dell'endpoint per le chiamate di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="04a43-104">After a server program registers its binding information and advertises its presence in a name service database, it can begin listening to the endpoint for remote procedure calls.</span></span> <span data-ttu-id="04a43-105">I programmi server chiamano la funzione [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) per monitorare gli endpoint per le chiamate client di procedure remote.</span><span class="sxs-lookup"><span data-stu-id="04a43-105">Server programs call the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to monitor endpoints for client invocations of remote procedures.</span></span>

<span data-ttu-id="04a43-106">La specifica DCE di [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indica che non deve essere restituita finché una funzione del programma server non chiama [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening).</span><span class="sxs-lookup"><span data-stu-id="04a43-106">The DCE specification of [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indicates that it should not return until a function in the server program calls [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening).</span></span> <span data-ttu-id="04a43-107">L'implementazione di Microsoft RPC di **RpcServerListen** usa due parametri che non sono presenti nella specifica DCE: *DontWait* e *MinimumCallThreads*.</span><span class="sxs-lookup"><span data-stu-id="04a43-107">The Microsoft RPC implementation of **RpcServerListen** uses two parameters that do not appear in the DCE specification: *DontWait* and *MinimumCallThreads*.</span></span> <span data-ttu-id="04a43-108">Il programma server può passare un valore diverso da zero per il parametro *DontWait* .</span><span class="sxs-lookup"><span data-stu-id="04a43-108">Your server program can pass a nonzero value for the *DontWait* parameter.</span></span> <span data-ttu-id="04a43-109">In caso contrario, la funzione **RpcServerListen** restituirà immediatamente.</span><span class="sxs-lookup"><span data-stu-id="04a43-109">If it does, the **RpcServerListen** function will return immediately.</span></span> <span data-ttu-id="04a43-110">Usare la routine [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) per eseguire l'operazione di attesa in genere associata a **RpcServerListen**.</span><span class="sxs-lookup"><span data-stu-id="04a43-110">Use the [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) routine to perform the wait operation usually associated with **RpcServerListen**.</span></span>

 

 




