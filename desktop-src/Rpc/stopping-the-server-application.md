---
title: Arresto dell'applicazione server
description: Un'applicazione server può arrestare l'ascolto dei client chiamando RpcMgmtStopServerListening e RpcServerUnregisterIf oppure semplicemente uscendo dal processo host.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- RPC (Remote Procedure Call), attività, arresto dell'applicazione server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f95ba05588e0575949614e05370f86de78207d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713681"
---
# <a name="stopping-the-server-application"></a><span data-ttu-id="991cf-104">Arresto dell'applicazione server</span><span class="sxs-lookup"><span data-stu-id="991cf-104">Stopping the Server Application</span></span>

<span data-ttu-id="991cf-105">Un'applicazione server può arrestare l'ascolto dei client chiamando [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) e [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)oppure semplicemente uscendo dal processo host.</span><span class="sxs-lookup"><span data-stu-id="991cf-105">A server application can stop listening for clients by calling [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) and [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif), or by simply exiting the host process.</span></span> <span data-ttu-id="991cf-106">Entrambi i metodi sono accettabili.</span><span class="sxs-lookup"><span data-stu-id="991cf-106">Both methods are acceptable.</span></span> <span data-ttu-id="991cf-107">Se il server segue il primo approccio, deve implementare i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="991cf-107">If the server follows the first approach, it should implement the following steps:</span></span>

<span data-ttu-id="991cf-108">La funzione server [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) non torna al programma chiamante fino a quando non si verifica un'eccezione o fino a quando non si verifica una chiamata a [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) .</span><span class="sxs-lookup"><span data-stu-id="991cf-108">The server function [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) does not return to the calling program until an exception occurs or until a call to [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) occurs.</span></span> <span data-ttu-id="991cf-109">Per impostazione predefinita, solo un altro thread del server può arrestare il server RPC utilizzando **RpcMgmtStopServerListening**.</span><span class="sxs-lookup"><span data-stu-id="991cf-109">By default, only another server thread is allowed to halt the RPC server by using **RpcMgmtStopServerListening**.</span></span> <span data-ttu-id="991cf-110">I client che tentano di arrestare il server riceveranno l' \_ errore \_ accesso RPC \_ negato.</span><span class="sxs-lookup"><span data-stu-id="991cf-110">Clients who try to halt the server will receive the error RPC\_S\_ACCESS\_DENIED.</span></span> <span data-ttu-id="991cf-111">Tuttavia, è possibile configurare RPC per consentire ad alcuni o a tutti i client di arrestare il server.</span><span class="sxs-lookup"><span data-stu-id="991cf-111">However, it is possible to configure RPC to allow some or all clients to stop the server.</span></span> <span data-ttu-id="991cf-112">Per informazioni dettagliate, vedere **RpcMgmtStopServerListening** .</span><span class="sxs-lookup"><span data-stu-id="991cf-112">See **RpcMgmtStopServerListening** for details.</span></span>

<span data-ttu-id="991cf-113">È inoltre possibile fare in modo che l'applicazione client effettui una chiamata di procedura remota a una routine di arresto sul server.</span><span class="sxs-lookup"><span data-stu-id="991cf-113">You can also have the client application make a remote procedure call to a shutdown routine on the server.</span></span> <span data-ttu-id="991cf-114">La routine Shutdown chiama [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) e [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif).</span><span class="sxs-lookup"><span data-stu-id="991cf-114">The shutdown routine calls [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) and [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif).</span></span> <span data-ttu-id="991cf-115">Questa esercitazione del programma di esempio utilizza questo approccio aggiungendo una nuova funzione remota, **Shutdown**, al file ciau. c.</span><span class="sxs-lookup"><span data-stu-id="991cf-115">This tutorial example program application uses this approach by adding a new remote function, **Shutdown**, to the file Hellop.c.</span></span>

<span data-ttu-id="991cf-116">Nella funzione **Shutdown** il singolo parametro null di [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indica che l'applicazione locale deve interrompere l'ascolto delle chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="991cf-116">In the **Shutdown** function, the single null parameter to [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indicates that the local application should stop listening for remote procedure calls.</span></span> <span data-ttu-id="991cf-117">I due parametri null per [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) sono caratteri jolly, a indicare che è necessario annullare la registrazione di tutte le interfacce.</span><span class="sxs-lookup"><span data-stu-id="991cf-117">The two null parameters to [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) are wildcards, indicating that all interfaces should be unregistered.</span></span> <span data-ttu-id="991cf-118">Il parametro **false** indica che l'interfaccia deve essere rimossa immediatamente dal registro di sistema, anziché attendere il completamento delle chiamate in sospeso.</span><span class="sxs-lookup"><span data-stu-id="991cf-118">The **FALSE** parameter indicates that the interface should be removed from the registry immediately, rather than waiting for pending calls to complete.</span></span>


```C++
/* add this function to hellop.c */
void Shutdown(void)
{
    RPC_STATUS status;
 
    status = RpcMgmtStopServerListening(NULL);
 
    if (status) 
    {
       exit(status);
    }
 
    status = RpcServerUnregisterIf(NULL, NULL, FALSE);
 
    if (status) 
    {
       exit(status);
    }
} //end Shutdown
```



 

 




