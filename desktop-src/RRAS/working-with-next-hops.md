---
title: Utilizzo degli hop successivi
description: L'API RTMv2 consente ai client di usare l'elenco degli hop successivi associati alle route e alle destinazioni.
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20a812fd272afafd2cd8eb1d6fb93d97530a2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396723"
---
# <a name="working-with-next-hops"></a><span data-ttu-id="a6362-103">Utilizzo degli hop successivi</span><span class="sxs-lookup"><span data-stu-id="a6362-103">Working with Next Hops</span></span>

<span data-ttu-id="a6362-104">L'API RTMv2 consente ai client di usare l'elenco degli hop successivi associati alle route e alle destinazioni.</span><span class="sxs-lookup"><span data-stu-id="a6362-104">The RTMv2 API allows clients to work with the list of next hops that are associated with routes and destinations.</span></span> <span data-ttu-id="a6362-105">I client possono aggiungere o aggiornare un hop successivo chiamando [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span><span class="sxs-lookup"><span data-stu-id="a6362-105">Clients can add or update a next hop by calling [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span></span> <span data-ttu-id="a6362-106">I client possono eliminare un hop successivo usando [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop).</span><span class="sxs-lookup"><span data-stu-id="a6362-106">Clients can delete a next hop using [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop).</span></span> <span data-ttu-id="a6362-107">I client possono cercare hop successivi chiamando [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).</span><span class="sxs-lookup"><span data-stu-id="a6362-107">Clients can search for next hops by calling [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).</span></span>

<span data-ttu-id="a6362-108">I client possono anche aggiornare direttamente l'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="a6362-108">Clients can also update the next hop directly.</span></span> <span data-ttu-id="a6362-109">A tale scopo, il client deve prima bloccare l'hop successivo con la funzione [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) .</span><span class="sxs-lookup"><span data-stu-id="a6362-109">To do so, the client must first lock the next hop with the [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) function.</span></span> <span data-ttu-id="a6362-110">Il client può quindi utilizzare il puntatore diretto alla struttura delle [**\_ \_ informazioni RTM NEXTHOP**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) di gestione tabelle di routing per apportare le modifiche necessarie.</span><span class="sxs-lookup"><span data-stu-id="a6362-110">Then the client can use the direct pointer to the routing table manager's [**RTM\_NEXTHOP\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) structure to make necessary modifications.</span></span> <span data-ttu-id="a6362-111">Infine, il client può sbloccare l'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="a6362-111">Finally, the client can unlock the next hop.</span></span>

> [!Note]  
> <span data-ttu-id="a6362-112">I campi indirizzo hop successivo e indice interfaccia nell'hop successivo identificano in modo univoco l'hop successivo e non devono essere modificati.</span><span class="sxs-lookup"><span data-stu-id="a6362-112">The next-hop address and interface index fields in the next hop uniquely identify the next hop and should not be modified.</span></span>

 

 

 




