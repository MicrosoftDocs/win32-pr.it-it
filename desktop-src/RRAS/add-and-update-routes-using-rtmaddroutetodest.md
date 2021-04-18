---
title: Aggiungere e aggiornare le route con RtmAddRouteToDest
description: La funzione RtmAddRouteToDest viene usata per aggiungere nuove route e aggiornare le route esistenti per una destinazione. Nelle procedure seguenti vengono illustrati entrambi i casi. Il codice di esempio seguente illustra come implementare la prima procedura.
ms.assetid: 17a04511-69f8-4e50-993c-0e558ee72184
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3594aee054e6815094834bedbc1aae158fc4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298402"
---
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a><span data-ttu-id="53fe5-105">Aggiungere e aggiornare le route con RtmAddRouteToDest</span><span class="sxs-lookup"><span data-stu-id="53fe5-105">Add and Update Routes Using RtmAddRouteToDest</span></span>

<span data-ttu-id="53fe5-106">La funzione [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) viene usata per aggiungere nuove route e aggiornare le route esistenti per una destinazione.</span><span class="sxs-lookup"><span data-stu-id="53fe5-106">The function [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) is used to add new routes and update existing routes for a destination.</span></span> <span data-ttu-id="53fe5-107">Nelle procedure seguenti vengono illustrati entrambi i casi.</span><span class="sxs-lookup"><span data-stu-id="53fe5-107">The following procedures explain both cases.</span></span> <span data-ttu-id="53fe5-108">Il codice di esempio seguente illustra come implementare la prima procedura.</span><span class="sxs-lookup"><span data-stu-id="53fe5-108">The sample code that follows shows how to implement the first procedure.</span></span>

<span data-ttu-id="53fe5-109">**Per aggiungere una route, il client deve eseguire la procedura seguente**</span><span class="sxs-lookup"><span data-stu-id="53fe5-109">**To add a route, the client should take the following steps**</span></span>

1.  <span data-ttu-id="53fe5-110">Se il client ha già memorizzato nella cache l'handle di hop successivo, andare al passaggio 4.</span><span class="sxs-lookup"><span data-stu-id="53fe5-110">If the client has already cached the next-hop handle, go to step 4.</span></span>
2.  <span data-ttu-id="53fe5-111">Creare una struttura di [**\_ \_ informazioni NEXTHOP RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) e riempirla con le informazioni appropriate.</span><span class="sxs-lookup"><span data-stu-id="53fe5-111">Create an [**RTM\_NEXTHOP\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) structure and fill it with the appropriate information.</span></span>
3.  <span data-ttu-id="53fe5-112">Aggiungere l'hop successivo alla tabella di routing chiamando [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span><span class="sxs-lookup"><span data-stu-id="53fe5-112">Add the next hop to the routing table by calling [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span></span> <span data-ttu-id="53fe5-113">Gestione tabelle di routing restituisce un handle per l'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="53fe5-113">The routing table manager returns a handle to the next hop.</span></span> <span data-ttu-id="53fe5-114">Se l'hop successivo esiste già, la tabella di routing non aggiunge l'hop successivo. viene invece restituito l'handle per l'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="53fe5-114">If the next hop already exists, the routing table does not add the next hop; instead it returns the handle to the next hop.</span></span>
4.  <span data-ttu-id="53fe5-115">Creare una struttura di [**\_ \_ informazioni sulla route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) e riempirla con le informazioni appropriate, incluso l'handle di hop successivo restituito da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="53fe5-115">Create an [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure and fill it with the appropriate information, including the next-hop handle returned by the routing table manager.</span></span>
5.  <span data-ttu-id="53fe5-116">Aggiungere la route alla tabella di routing chiamando [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest).</span><span class="sxs-lookup"><span data-stu-id="53fe5-116">Add the route to the routing table by calling [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest).</span></span> <span data-ttu-id="53fe5-117">Gestione tabelle di routing confronta la nuova route con le route già presenti nella tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="53fe5-117">The routing table manager compares the new route to the routes that are already in the routing table.</span></span> <span data-ttu-id="53fe5-118">Due route sono uguali se si verificano tutte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="53fe5-118">Two routes are equal if all of the following conditions are true:</span></span>

    -   <span data-ttu-id="53fe5-119">La route viene aggiunta alla stessa destinazione.</span><span class="sxs-lookup"><span data-stu-id="53fe5-119">The route is being added to the same destination.</span></span>
    -   <span data-ttu-id="53fe5-120">La route viene aggiunta dallo stesso client come specificato dal membro **proprietario** della struttura di informazioni della [**\_ route RTM \_**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .</span><span class="sxs-lookup"><span data-stu-id="53fe5-120">The route is being added by the same client as specified by the **Owner** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>
    -   <span data-ttu-id="53fe5-121">La route viene annunciata dallo stesso adiacente, come specificato dal membro **adiacente** della struttura di [**\_ \_ informazioni della route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .</span><span class="sxs-lookup"><span data-stu-id="53fe5-121">The route is advertised by the same neighbor as specified by the **Neighbor** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>

    <span data-ttu-id="53fe5-122">Se la route esiste, il gestore delle tabelle di routing restituisce l'handle alla route esistente.</span><span class="sxs-lookup"><span data-stu-id="53fe5-122">If the route exists, the routing table manager returns the handle to the existing route.</span></span> <span data-ttu-id="53fe5-123">In caso contrario, il gestore tabelle di routing aggiunge la route e restituisce l'handle alla nuova route.</span><span class="sxs-lookup"><span data-stu-id="53fe5-123">Otherwise, the routing table manager adds the route and returns the handle to the new route.</span></span>

    <span data-ttu-id="53fe5-124">Il client può impostare il parametro *Change \_ Flags* sulla \_ route RTM \_ Change \_ New per indicare a gestione tabelle di routing di aggiungere una nuova route nella destinazione, anche se esiste un'altra route con lo stesso proprietario e i campi adiacenti.</span><span class="sxs-lookup"><span data-stu-id="53fe5-124">The client can set the *Change\_Flags* parameter to RTM\_ROUTE\_CHANGE\_NEW to instruct the routing table manager to add a new route on the destination, even if another route with the same owner and neighbor fields exists.</span></span>

    <span data-ttu-id="53fe5-125">Il client può impostare il parametro *Change \_ Flags* su RTM \_ route \_ Change \_ prima per indicare a gestione tabelle di routing di aggiornare la prima route nella destinazione di proprietà del client.</span><span class="sxs-lookup"><span data-stu-id="53fe5-125">The client can set the *Change\_Flags* parameter to RTM\_ROUTE\_CHANGE\_FIRST to tell the routing table manager to update the first route on the destination owned by the client.</span></span> <span data-ttu-id="53fe5-126">Questo aggiornamento può essere eseguito se esiste una route di questo tipo, anche se il campo adiacente non corrisponde.</span><span class="sxs-lookup"><span data-stu-id="53fe5-126">This update can be performed if such a route exists, even if the neighbor field does not match.</span></span> <span data-ttu-id="53fe5-127">Questo flag viene usato dai client che gestiscono una singola route per destinazione.</span><span class="sxs-lookup"><span data-stu-id="53fe5-127">This flag is used by clients that maintain a single route per destination.</span></span>

<span data-ttu-id="53fe5-128">**Per aggiornare una route, il client deve eseguire la procedura seguente**</span><span class="sxs-lookup"><span data-stu-id="53fe5-128">**To update a route, the client should take the following steps**</span></span>

1.  <span data-ttu-id="53fe5-129">Chiamare [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) con l'handle per la route.</span><span class="sxs-lookup"><span data-stu-id="53fe5-129">Call [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) with the handle to the route.</span></span> <span data-ttu-id="53fe5-130">L'handle è uno precedentemente memorizzato nella cache dal client o restituito da Gestione tabelle di routing da una chiamata che restituisce un handle di route, ad esempio **RtmGetRouteInfo**.</span><span class="sxs-lookup"><span data-stu-id="53fe5-130">The handle is either one previously cached by the client, or returned by the routing table manager from a call that returns a route handle such as **RtmGetRouteInfo**.</span></span>
2.  <span data-ttu-id="53fe5-131">Apportare le modifiche alla struttura [**delle \_ \_ informazioni sulla route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) restituita da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="53fe5-131">Make the changes to the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure that is returned by the routing table manager.</span></span>
3.  <span data-ttu-id="53fe5-132">Chiamare [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) con l'handle per la route e la struttura [**di \_ \_ informazioni della route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) modificata.</span><span class="sxs-lookup"><span data-stu-id="53fe5-132">Call [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) with the handle to the route and the changed [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>

<span data-ttu-id="53fe5-133">Nell'esempio di codice seguente viene illustrato come aggiungere una route a una destinazione utilizzando Gestione tabelle di routing come intermediario.</span><span class="sxs-lookup"><span data-stu-id="53fe5-133">The following sample code shows how to add a route to a destination using the routing table manager as an intermediary.</span></span>


```C++
// Add a route to a destination given by (addr, masklen)
// using a next hop reachable with an interface

RTM_NEXTHOP_INFO NextHopInfo;

// First, create and add a next hop to the caller's
// next-hop tree (if it does not already exist)

ZeroMemory(&NextHopInfo, sizeof(RTM_NEXTHOP_INFO);

RTM_IPV4_MAKE_NET_ADDRESS(&NextHopInfo.NextHopAddress,
                          nexthop, // Address of the next hop
                          32);

NextHopInfo.InterfaceIndex = interface;

NextHopHandle = NULL;

Status = RtmAddNextHop(RtmRegHandle,
                       &NextHopInfo,
                       &NextHopHandle,
                       &ChangeFlags);

if (Status == NO_ERROR)
{
    // Created a new next hop or found an old one

        // Fill in the route information for the route
    
    ZeroMemory(&RouteInfo, sizeof(RTM_ROUTE_INFO);

    // Fill in the destination network's address and mask values
    RTM_IPV4_MAKE_NET_ADDRESS(&NetAddress, addr, masklen);

    // Assume 'neighbour learnt from' is the first next hop
    RouteInfo.Neighbour = NextHopHandle;

    // Set metric for route; Preference set internally
    RouteInfo.PrefInfo.Metric = metric;

    // Adding a route to both the unicast and multicast views
    RouteInfo.BelongsToViews = RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST;

    RouteInfo.NextHopsList.NumNextHops = 1;
    RouteInfo.NextHopsList.NextHops[0] = NextHopHandle;

    // If you want to add a new route, regardless of
    // whether a similar route already exists, use the following 
    //     ChangeFlags = RTM_ROUTE_CHANGE_NEW;

    ChangeFlags = 0;

    Status = RtmAddRouteToDest(RtmRegHandle,
                               &RouteHandle,     // Can be NULL if you do not need handle
                               &NetAddress,
                               &RouteInfo,
                               1000,             // Time out route after 1000 ms
                               RouteListHandle1, // Also add the route to this list
                               0,
                               NULL,
                               &ChangeFlags);

    if (Status == NO_ERROR)
    {
        if (ChangeFlags & RTM_ROUTE_CHANGE_NEW)
        {
        ; // A new route has been created
        }
        else
        {
        ; // An existing route is updated
        }

        if (ChangeFlags & RTM_ROUTE_CHANGE_BEST)
        {
        ; // Best route information has changed
        }

        // Release the route handle if you do not need it
        RtmReleaseRoutes(RtmRegHandle, 1, &RouteHandle);
    }

    // Also release the next hop since it is no longer needed 
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHopHandle);
}
```



 

 




