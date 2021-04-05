---
title: Non utilizzare la sicurezza degli endpoint
description: Endpoint Security è un modello di sicurezza in cui viene fornito un descrittore di sicurezza quando viene creato un endpoint con il gruppo RpcServerUseProtseq \ di funzioni RPC.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289513810ba7e67e0da625151c3c2975e0eaaf99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709961"
---
# <a name="do-not-use-endpoint-security"></a><span data-ttu-id="bcd66-103">Non utilizzare la sicurezza degli endpoint</span><span class="sxs-lookup"><span data-stu-id="bcd66-103">Do Not Use Endpoint Security</span></span>

<span data-ttu-id="bcd66-104">Endpoint Security è un modello di sicurezza in cui viene fornito un descrittore di sicurezza quando viene creato un endpoint con il gruppo [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* di funzioni RPC.</span><span class="sxs-lookup"><span data-stu-id="bcd66-104">Endpoint security is a security model in which a security descriptor is given when an endpoint is created with the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)\* group of RPC functions.</span></span> <span data-ttu-id="bcd66-105">Non utilizzare questo modello di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="bcd66-105">Do not use this security model.</span></span> <span data-ttu-id="bcd66-106">Non assegnare descrittori di sicurezza a tali funzioni.</span><span class="sxs-lookup"><span data-stu-id="bcd66-106">Do not give security descriptors to those functions.</span></span> <span data-ttu-id="bcd66-107">Al meglio, questo metodo è uno spreco di risorse della CPU.</span><span class="sxs-lookup"><span data-stu-id="bcd66-107">At best, this method is a waste of CPU resources.</span></span> <span data-ttu-id="bcd66-108">Nel peggiore dei casi, in molti ambienti è possibile aggirare il descrittore di sicurezza, in quanto gli [altri endpoint RPC in esecuzione nella stessa](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) sezione del processo esemplificano.</span><span class="sxs-lookup"><span data-stu-id="bcd66-108">At worst, in many environments it is possible to circumvent the security descriptor, as the [Be Wary of Other RPC Endpoints Running In the Same Process](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) section exemplifies.</span></span>

<span data-ttu-id="bcd66-109">La sicurezza degli endpoint esiste solo per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="bcd66-109">Endpoint security exists only for backward compatibility.</span></span>

 

 




