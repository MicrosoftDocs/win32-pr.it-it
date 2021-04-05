---
title: Ascolto delle chiamate client
description: Dopo che l'applicazione server ha registrato le interfacce, creato le informazioni di binding necessarie e ha registrato gli endpoint, è pronto per iniziare ad ascoltare le chiamate di procedure remote da programmi client.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- RPC, attività, ascolto per le chiamate client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f375a4620e301f59d168bf5f7a4dbeedc0fb89f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856742"
---
# <a name="listening-for-client-calls"></a><span data-ttu-id="4ee75-104">Ascolto delle chiamate client</span><span class="sxs-lookup"><span data-stu-id="4ee75-104">Listening for Client Calls</span></span>

<span data-ttu-id="4ee75-105">Dopo che l'applicazione server ha registrato le interfacce, creato le informazioni di binding necessarie e ha registrato gli endpoint, è pronto per iniziare ad ascoltare le chiamate di procedure remote da programmi client.</span><span class="sxs-lookup"><span data-stu-id="4ee75-105">After your server application has registered its interfaces, created the necessary binding information, and registered its endpoints, it is ready to begin listening for remote procedure calls from client programs.</span></span>

<span data-ttu-id="4ee75-106">Per ascoltare le chiamate a procedure remote, il programma server deve chiamare [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), come illustrato nel frammento di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="4ee75-106">To listen for remote procedure calls, your server program must call [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), as shown in the following code fragment:</span></span>


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



<span data-ttu-id="4ee75-107">Un server RPC ha uno o più thread che prelevano chiamate client e le inviano alle routine nelle interfacce registrate.</span><span class="sxs-lookup"><span data-stu-id="4ee75-107">An RPC Server has one or more threads that pick up client calls and deliver them to the routines in the registered interfaces.</span></span> <span data-ttu-id="4ee75-108">Il primo parametro della funzione [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) è il numero minimo di thread da creare.</span><span class="sxs-lookup"><span data-stu-id="4ee75-108">The first parameter to the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function is the minimum number of threads to create.</span></span> <span data-ttu-id="4ee75-109">Il parametro è solo un hint; il tempo di esecuzione RPC può scegliere di ignorarlo.</span><span class="sxs-lookup"><span data-stu-id="4ee75-109">The parameter is only a hint; the RPC run time may chose to ignore it.</span></span>

<span data-ttu-id="4ee75-110">Il secondo parametro di [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) è il numero massimo di chiamate a procedure remote simultanee da gestire.</span><span class="sxs-lookup"><span data-stu-id="4ee75-110">The second parameter to [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) is the maximum number of concurrent remote procedure calls to handle.</span></span> <span data-ttu-id="4ee75-111">Se si desidera che l'applicazione utilizzi il valore massimo predefinito, il passaggio RPC \_ C \_ Listen \_ Max \_ calls \_ default come valore per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="4ee75-111">If you want your application to use the default maximum value, pass RPC\_C\_LISTEN\_MAX\_CALLS\_DEFAULT as the value for this parameter.</span></span>

<span data-ttu-id="4ee75-112">La specifica DCE chiama per la continuazione dell'esecuzione di [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) fino a quando non riceve un segnale per l'arresto.</span><span class="sxs-lookup"><span data-stu-id="4ee75-112">The DCE specification calls for [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) to keep running until it receives a signal to stop.</span></span> <span data-ttu-id="4ee75-113">Un'estensione Microsoft a questa funzione consente di iniziare l'ascolto e restituire immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="4ee75-113">One Microsoft extension to this function is to enable it to begin listening and return immediately.</span></span> <span data-ttu-id="4ee75-114">Se si vuole che l'applicazione usi il comportamento predefinito di DCE, impostare il terzo parametro su zero.</span><span class="sxs-lookup"><span data-stu-id="4ee75-114">If you want your application to use the default DCE behavior, set the third parameter to zero.</span></span> <span data-ttu-id="4ee75-115">Per informazioni dettagliate, vedere [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)e [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) .</span><span class="sxs-lookup"><span data-stu-id="4ee75-115">See [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), and [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) for details.</span></span>

 

 




