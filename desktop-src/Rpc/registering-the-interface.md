---
title: Registrazione dell'interfaccia
description: La registrazione dell'interfaccia supportata da un programma server consente di inviare chiamate a procedure remote da programmi client alla routine del server appropriata.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- RPC (Remote Procedure Call), attività, registrazione dell'interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a12de37b39c719de246ceb79a92d6a51fc361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220905"
---
# <a name="registering-the-interface"></a><span data-ttu-id="05e2e-104">Registrazione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="05e2e-104">Registering the Interface</span></span>

<span data-ttu-id="05e2e-105">La registrazione dell'interfaccia supportata da un programma server consente di inviare chiamate a procedure remote da programmi client alla routine del server appropriata.</span><span class="sxs-lookup"><span data-stu-id="05e2e-105">Registering the interface that a server program supports enables remote procedure calls from client programs to be dispatched to the proper server routine.</span></span> <span data-ttu-id="05e2e-106">I programmi server chiamano [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) per registrare le interfacce.</span><span class="sxs-lookup"><span data-stu-id="05e2e-106">Server programs call [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to register their interfaces.</span></span> <span data-ttu-id="05e2e-107">Il frammento di codice seguente ne illustra l'uso:</span><span class="sxs-lookup"><span data-stu-id="05e2e-107">The following code fragment demonstrates its use:</span></span>


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



<span data-ttu-id="05e2e-108">Il primo parametro della funzione [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) è una struttura generata dal compilatore MIDL dal file IDL che definisce l'interfaccia (o le interfacce) per il server.</span><span class="sxs-lookup"><span data-stu-id="05e2e-108">The first parameter to the [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) function is a structure the MIDL compiler generates from the IDL file that defines the interface (or interfaces) for the server.</span></span> <span data-ttu-id="05e2e-109">Il secondo e il terzo parametro sono rispettivamente un UUID e un vettore del punto di ingresso.</span><span class="sxs-lookup"><span data-stu-id="05e2e-109">The second and third parameters are a UUID and an entry-point vector, respectively.</span></span> <span data-ttu-id="05e2e-110">In questo esempio sono impostate su **null** .</span><span class="sxs-lookup"><span data-stu-id="05e2e-110">They are set to **NULL** in this example.</span></span> <span data-ttu-id="05e2e-111">In molti casi, il programma server imposterà questi valori di parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="05e2e-111">In many instances, your server program will set these parameter values to **NULL**.</span></span> <span data-ttu-id="05e2e-112">I programmi server usano il secondo e il terzo parametro quando forniscono più implementazioni delle stesse procedure in un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="05e2e-112">Server programs use the second and third parameters when they provide multiple implementations of the same procedures in an interface.</span></span> <span data-ttu-id="05e2e-113">Per altre informazioni, vedere [vettori di punti di ingresso](registering-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="05e2e-113">For more information, see [Entry-Point Vectors](registering-interfaces.md).</span></span>

<span data-ttu-id="05e2e-114">I programmi server possono anche usare [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) per registrare un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="05e2e-114">Server programs can also use [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) to register an interface.</span></span> <span data-ttu-id="05e2e-115">Un vantaggio dell'uso di questa funzione è che fornisce all'applicazione la possibilità di impostare una funzione di callback di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="05e2e-115">One advantage of using this function is that it provides your application with the ability to set a security-callback function.</span></span> <span data-ttu-id="05e2e-116">L'utilizzo delle funzioni di callback di sicurezza è l'approccio consigliato per la protezione di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="05e2e-116">Using security-callback functions is the recommended approach to securing an interface.</span></span>

> [!Note]  
> <span data-ttu-id="05e2e-117">MIDL produce due strutture molto simili, una per il client e una per il server.</span><span class="sxs-lookup"><span data-stu-id="05e2e-117">MIDL produces two very similar structures, one for the client and one for the server.</span></span> <span data-ttu-id="05e2e-118">La struttura passata alla funzione [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) è la versione server della struttura che produce MIDL.</span><span class="sxs-lookup"><span data-stu-id="05e2e-118">The structure passed to the [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) function is the server version of the MIDL-produced structure.</span></span>

 

 

 




