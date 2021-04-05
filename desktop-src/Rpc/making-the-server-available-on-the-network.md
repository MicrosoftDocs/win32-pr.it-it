---
title: Rendere disponibile il server in rete
description: Prima che un'applicazione server possa accettare chiamate a procedure remote, è necessario che sia disponibile in rete.
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- RPC (Remote Procedure Call), attività, rendere disponibile il server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2826e4e63e7e78e7f87f6afc120b80e885cd3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044922"
---
# <a name="making-the-server-available-on-the-network"></a><span data-ttu-id="0e0c3-104">Rendere disponibile il server in rete</span><span class="sxs-lookup"><span data-stu-id="0e0c3-104">Making the Server Available on the Network</span></span>

<span data-ttu-id="0e0c3-105">Prima che un'applicazione server possa accettare chiamate a procedure remote, è necessario che sia disponibile in rete.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-105">Before a server application can accept remote procedure calls, it must be available on the network.</span></span> <span data-ttu-id="0e0c3-106">A tale scopo, il server indica al tempo di esecuzione RPC che è disposto ad accettare le chiamate su una o più sequenze di protocollo.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-106">To do this, the server indicates to the RPC Run time that it is willing to accept calls on one or more protocol sequences.</span></span> <span data-ttu-id="0e0c3-107">La scelta delle sequenze di protocollo supportate da un'applicazione server è una decisione importante. diverse sequenze di protocollo hanno funzionalità molto diverse.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-107">Choosing the protocol sequences a server application supports is an important decision; different protocol sequences have very different capabilities.</span></span> <span data-ttu-id="0e0c3-108">I server che prevedono la ricezione locale delle chiamate devono usare **ncalrpc**.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-108">Servers that expect calls to be received locally should use **ncalrpc**.</span></span> <span data-ttu-id="0e0c3-109">I server che accettano chiamate remote devono **usare \_ \_ TCP IP di ncacn**.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-109">Servers that accept remote calls should use **ncacn\_ip\_tcp**.</span></span> <span data-ttu-id="0e0c3-110">I server non devono verificare che la sequenza di protocollo su cui ricevono chiamate sia la sequenza di protocollo su cui si aspettano di ricevere chiamate.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-110">Servers should not verify that the protocol sequence on which they receive calls is the protocol sequence on which they expect to receive calls.</span></span> <span data-ttu-id="0e0c3-111">Per ulteriori informazioni, vedere prestare attenzione ad altri endpoint RPC in esecuzione nello stesso processo in procedure di programmazione RPC ottimali.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-111">See Be Wary of Other RPC Endpoints Running in the Same Process in Best RPC Programming Practices for more information.</span></span>

<span data-ttu-id="0e0c3-112">Nell'esempio seguente viene usato **ncacn \_ IP \_ TCP**.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-112">The following example uses **ncacn\_ip\_tcp**.</span></span>

<span data-ttu-id="0e0c3-113">La maggior parte dei programmi server utilizza tutte le sequenze di protocollo disponibili sulla rete.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-113">Most server programs use all protocol sequences available on the network.</span></span> <span data-ttu-id="0e0c3-114">A tale scopo, richiamano la funzione [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) , come illustrato nel frammento di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="0e0c3-114">To do this, they invoke the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) function, as shown in the following code fragment:</span></span>


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



<span data-ttu-id="0e0c3-115">Il primo parametro della funzione [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) è la sequenza del protocollo.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-115">The first parameter to the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) function is the protocol sequence.</span></span> <span data-ttu-id="0e0c3-116">Il secondo parametro dipende dalla sequenza del protocollo.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-116">The second parameter is dependent on the protocol sequence.</span></span> <span data-ttu-id="0e0c3-117">Come illustrato nel frammento di codice, la maggior parte dei programmi server imposta questo parametro su **RPC \_ C \_ PROTSEQ \_ Max \_ Rich \_ default**.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-117">As illustrated in the code fragment, most server programs set this parameter to **RPC\_C\_PROTSEQ\_MAX\_REQS\_DEFAULT**.</span></span> <span data-ttu-id="0e0c3-118">Questo valore imposta la libreria RPC per l'utilizzo del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-118">This value sets the RPC library to use the default value.</span></span> <span data-ttu-id="0e0c3-119">Il terzo parametro è un descrittore di sicurezza e non deve essere usato nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-119">The third parameter is a security descriptor and should not be used in applications.</span></span> <span data-ttu-id="0e0c3-120">Per ulteriori informazioni, vedere [**sicurezza**](security.md).</span><span class="sxs-lookup"><span data-stu-id="0e0c3-120">For more information, see [**Security**](security.md).</span></span>

<span data-ttu-id="0e0c3-121">È anche possibile usare le funzioni [**RpcServerUseAllProtSeqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)o [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) .</span><span class="sxs-lookup"><span data-stu-id="0e0c3-121">You can also use the [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep), or [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) functions.</span></span>

<span data-ttu-id="0e0c3-122">Quando un'applicazione server seleziona almeno una sequenza di protocolli, i server che utilizzano endpoint dinamici devono creare informazioni di binding per ogni sequenza di protocollo utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-122">After a server application selects at least one protocol sequence, servers that use dynamic endpoints must create binding information for each protocol sequence it uses.</span></span> <span data-ttu-id="0e0c3-123">Il server archivia le informazioni di binding in un vettore di associazione che può quindi esportare nel servizio di mapping degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="0e0c3-123">The server stores the binding information in a binding vector that it can then export to the endpoint mapper service.</span></span>

<span data-ttu-id="0e0c3-124">Usare la funzione [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) per ottenere un vettore di associazione per l'applicazione server, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="0e0c3-124">Use the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) function to obtain a binding vector for the server application, as shown in the following example:</span></span>


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



<span data-ttu-id="0e0c3-125">L'unico parametro passato alla funzione [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) è un puntatore a un puntatore a una struttura [**di \_ \_ vettori di binding RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) .</span><span class="sxs-lookup"><span data-stu-id="0e0c3-125">The only parameter passed to the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) function is a pointer to a pointer to an [**RPC\_BINDING\_VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) structure.</span></span> <span data-ttu-id="0e0c3-126">La libreria di runtime RPC alloca dinamicamente una matrice di vettori di associazione e archivia l'indirizzo della matrice nella variabile del parametro (in questo caso, **rpcBindingVector**).</span><span class="sxs-lookup"><span data-stu-id="0e0c3-126">The RPC run-time library dynamically allocates an array of binding vectors and stores the address of the array in the parameter variable (in this case, **rpcBindingVector**).</span></span> <span data-ttu-id="0e0c3-127">Ogni applicazione server è responsabile di liberare questo vettore di associazione usando la funzione [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) una volta che ha terminato l'uso (ad esempio, dopo averla passata alle funzioni appropriate).</span><span class="sxs-lookup"><span data-stu-id="0e0c3-127">Each server application is responsible for freeing this binding vector using the [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) function once it has finished using it (for example, after it has passed it to the appropriate functions).</span></span>

 

 




