---
title: Contrassegno delle route per lo stato Hold-Down
description: Alcuni client, ad esempio i protocolli per vettori di distanza come RIP e DVMRP, richiedono che le destinazioni siano annunciate come irraggiungibili per un determinato periodo di tempo dopo l'eliminazione dell'ultima route alla destinazione.
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af10832452a3a0b9ca851c209d240c97998ef519
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955563"
---
# <a name="marking-routes-for-the-hold-down-state"></a><span data-ttu-id="885c6-103">Contrassegno delle route per lo stato Hold-Down</span><span class="sxs-lookup"><span data-stu-id="885c6-103">Marking Routes for the Hold-Down State</span></span>

<span data-ttu-id="885c6-104">Alcuni client, ad esempio i protocolli per vettori di distanza come RIP e DVMRP, richiedono che le destinazioni siano annunciate come irraggiungibili per un determinato periodo di tempo dopo l'eliminazione dell'ultima route alla destinazione.</span><span class="sxs-lookup"><span data-stu-id="885c6-104">Some clients, such as distance vector protocols like RIP and DVMRP, require that destinations be advertised as unreachable for a certain time after the last route to the destination is deleted.</span></span> <span data-ttu-id="885c6-105">L'ultima route eliminata deve essere annunciata come irraggiungibile anche se le route più recenti arrivano nel frattempo.</span><span class="sxs-lookup"><span data-stu-id="885c6-105">The last route that is deleted must be advertised as unreachable even if newer routes arrive in the meantime.</span></span> <span data-ttu-id="885c6-106">L'ultima route eliminata è contrassegnata come in uno *stato di attesa*.</span><span class="sxs-lookup"><span data-stu-id="885c6-106">The last route deleted is marked as being in a *hold-down state*.</span></span> <span data-ttu-id="885c6-107">Il processo di attesa impedisce la formazione dei cicli di routing.</span><span class="sxs-lookup"><span data-stu-id="885c6-107">The hold-down process prevents the formation of routing loops.</span></span> <span data-ttu-id="885c6-108">I cicli di routing vengono causati quando un protocollo di routing annuncia informazioni di routing obsolete.</span><span class="sxs-lookup"><span data-stu-id="885c6-108">Routing loops are caused when a routing protocol advertises obsolete routing information.</span></span> <span data-ttu-id="885c6-109">Quando il periodo di attesa scade, questi protocolli riprendono l'annuncio con la nuova route migliore.</span><span class="sxs-lookup"><span data-stu-id="885c6-109">When the hold-down expires, these protocols resume their advertisement with the new best route.</span></span>

<span data-ttu-id="885c6-110">Un protocollo che implementa gli Stati di attesa indica che una destinazione si trova in uno stato di attesa tramite la funzione [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) .</span><span class="sxs-lookup"><span data-stu-id="885c6-110">A protocol that implements hold-down states indicates that a destination is in a hold-down state by using the [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) function.</span></span> <span data-ttu-id="885c6-111">Il client chiama questa funzione quando annuncia la route migliore a questa destinazione.</span><span class="sxs-lookup"><span data-stu-id="885c6-111">The client calls this function when it advertises the best route to this destination.</span></span> <span data-ttu-id="885c6-112">Se in seguito vengono eliminate tutte le route a questa destinazione, l'ultima route eliminata viene mantenuta in uno stato di attesa per il periodo di tempo specificato nella chiamata precedente a **RtmHoldDestination**.</span><span class="sxs-lookup"><span data-stu-id="885c6-112">If all routes to this destination are later deleted, the last route that is deleted is kept in a hold-down state for the period of time specified in the earlier call to **RtmHoldDestination**.</span></span>

<span data-ttu-id="885c6-113">Quando un protocollo annuncia una destinazione, le informazioni sulla route utilizzate variano a seconda che il protocollo usi gli Stati di attesa e se è presente una route nello stato di attesa per la destinazione.</span><span class="sxs-lookup"><span data-stu-id="885c6-113">When a protocol advertises a destination, the route information that is used depends on whether the protocol uses hold-down states and if a route in the hold-down state exists for the destination.</span></span>

<span data-ttu-id="885c6-114">I protocolli che non utilizzano gli Stati di attesa possono ignorare le informazioni relative alla route correlate agli Stati di attesa per una destinazione e annunciare sempre la migliore route.</span><span class="sxs-lookup"><span data-stu-id="885c6-114">Protocols that do not use hold-down states can ignore route information that relates to hold-down states for a destination, and always advertise the best route.</span></span>

<span data-ttu-id="885c6-115">Per il codice di esempio che illustra come usare queste funzioni, vedere [usare lo stato Hold-Down Route](use-the-route-hold-down-state.md).</span><span class="sxs-lookup"><span data-stu-id="885c6-115">For sample code that shows how to use these functions, see [Use the Route Hold-Down State](use-the-route-hold-down-state.md).</span></span>

 

 




