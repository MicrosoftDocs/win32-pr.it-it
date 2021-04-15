---
description: Una trasmissione generale attraverso Internet viene eseguita impostando i campi SA \_ netnum e sa \_ nodenum su quelli binari (1).
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Tutte le route trasmesse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15830ad4f82a3cc5d93e84762c8c17ed0cfd85bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484964"
---
# <a name="all-routes-broadcast"></a><span data-ttu-id="d7322-103">Tutte le route trasmesse</span><span class="sxs-lookup"><span data-stu-id="d7322-103">All Routes Broadcast</span></span>

<span data-ttu-id="d7322-104">Una trasmissione generale attraverso Internet viene eseguita impostando i campi **sa \_ netnum** e **sa \_ nodenum** su quelli binari (1).</span><span class="sxs-lookup"><span data-stu-id="d7322-104">A general broadcast through the Internet is achieved by setting the **sa\_netnum** and **sa\_nodenum** fields to binary ones (1).</span></span> <span data-ttu-id="d7322-105">Il provider di servizi traduce la richiesta in un pacchetto di tipo-20, che i router IPX riconoscono e inoltrano.</span><span class="sxs-lookup"><span data-stu-id="d7322-105">The service provider translates this request to a type-20 packet, which IPX routers recognize and forward.</span></span> <span data-ttu-id="d7322-106">Il pacchetto visita tutte le subnet e può essere duplicato più volte.</span><span class="sxs-lookup"><span data-stu-id="d7322-106">The packet visits all subnets and may be duplicated several times.</span></span> <span data-ttu-id="d7322-107">I ricevitori devono gestire diverse copie duplicate del datagramma.</span><span class="sxs-lookup"><span data-stu-id="d7322-107">Receivers must handle several duplicate copies of the datagram.</span></span>

<span data-ttu-id="d7322-108">L'uso di questo tipo di trasmissione non è popolare tra gli amministratori di rete, quindi il suo utilizzo dovrebbe essere estremamente limitato.</span><span class="sxs-lookup"><span data-stu-id="d7322-108">Use of this broadcast type is unpopular among network administrators, so its use should be extremely limited.</span></span> <span data-ttu-id="d7322-109">Molti router disabilitano questo tipo di trasmissione, lasciando le parti della subnet invisibili al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d7322-109">Many routers disable this type of broadcast, leaving parts of the subnet invisible to the packet.</span></span>

 

 



