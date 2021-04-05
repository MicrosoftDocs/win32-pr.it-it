---
title: Prestare attenzione ad altri endpoint RPC in esecuzione nello stesso processo
description: Quando un'applicazione si trova in un processo con altri server RPC, tutte le applicazioni restano in attesa su tutti i protocolli.
ms.assetid: edb20108-e0c3-4b9b-b57d-45a96d9472ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00828ddf95fd024069a8a535c95673eb014d84b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711572"
---
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a><span data-ttu-id="19cda-103">Prestare attenzione ad altri endpoint RPC in esecuzione nello stesso processo</span><span class="sxs-lookup"><span data-stu-id="19cda-103">Be Wary of Other RPC Endpoints Running in the Same Process</span></span>

<span data-ttu-id="19cda-104">Quando un'applicazione si trova in un processo con altri server RPC, tutte le applicazioni restano in attesa su tutti i protocolli.</span><span class="sxs-lookup"><span data-stu-id="19cda-104">When an application resides in a process with other RPC servers, all applications listen on all protocols.</span></span> <span data-ttu-id="19cda-105">Di conseguenza, se un componente chiama solo [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* per LRPC, non è necessariamente accessibile solo su LRPC.</span><span class="sxs-lookup"><span data-stu-id="19cda-105">As such, if a component calls [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)\* for LRPC only, it is not necessarily accessible over LRPC only.</span></span> <span data-ttu-id="19cda-106">Può essere accessibile tramite altri protocolli, dal momento che altri server RPC nel processo potrebbero essere in ascolto su pipe o socket (ad esempio).</span><span class="sxs-lookup"><span data-stu-id="19cda-106">It may be accessible over other protocols, since other RPC servers in the process may be listening on pipes or sockets (for example).</span></span>

<span data-ttu-id="19cda-107">Analogamente agli handle di contesto rigorosi, non l'inserimento di un altro endpoint nel processo non significa che un altro endpoint non esiste.</span><span class="sxs-lookup"><span data-stu-id="19cda-107">Similar to strict context handles, not putting another endpoint in the process does not mean another endpoint does not exist.</span></span> <span data-ttu-id="19cda-108">Indipendentemente dalla modalità di registrazione del server, non esiste un'associazione speciale tra l'interfaccia e l'endpoint. tutte le interfacce possono essere richiamate su tutti gli endpoint in tale processo.</span><span class="sxs-lookup"><span data-stu-id="19cda-108">Regardless of how you register your server, there is no special association between your interface and your endpoint; all interfaces are callable on all endpoints in that process.</span></span> <span data-ttu-id="19cda-109">Questo è un altro motivo per cui il modello di sicurezza degli endpoint non è efficace; Se un descrittore di sicurezza viene inserito in un endpoint, gli utenti malintenzionati possono chiamare l'interfaccia su un altro endpoint.</span><span class="sxs-lookup"><span data-stu-id="19cda-109">This is another reason why the endpoint security model is ineffective; if a security descriptor is placed on an endpoint, attackers can call the interface on another endpoint.</span></span>

<span data-ttu-id="19cda-110">Per assicurarsi che un processo venga chiamato solo su una sequenza di protocollo specifica, registrare una funzione di callback di sicurezza e, in tale funzione, controllare la sequenza di protocollo effettuata dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="19cda-110">To ensure a process be called only on a specific protocol sequence, register a security callback function, and in that function, check on which protocol sequence the call is made.</span></span>

 

 




