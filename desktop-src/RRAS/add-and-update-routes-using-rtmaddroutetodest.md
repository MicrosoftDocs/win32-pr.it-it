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
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a>Aggiungere e aggiornare le route con RtmAddRouteToDest

La funzione [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) viene usata per aggiungere nuove route e aggiornare le route esistenti per una destinazione. Nelle procedure seguenti vengono illustrati entrambi i casi. Il codice di esempio seguente illustra come implementare la prima procedura.

**Per aggiungere una route, il client deve eseguire la procedura seguente**

1.  Se il client ha già memorizzato nella cache l'handle di hop successivo, andare al passaggio 4.
2.  Creare una struttura di [**\_ \_ informazioni NEXTHOP RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) e riempirla con le informazioni appropriate.
3.  Aggiungere l'hop successivo alla tabella di routing chiamando [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop). Gestione tabelle di routing restituisce un handle per l'hop successivo. Se l'hop successivo esiste già, la tabella di routing non aggiunge l'hop successivo. viene invece restituito l'handle per l'hop successivo.
4.  Creare una struttura di [**\_ \_ informazioni sulla route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) e riempirla con le informazioni appropriate, incluso l'handle di hop successivo restituito da Gestione tabelle di routing.
5.  Aggiungere la route alla tabella di routing chiamando [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest). Gestione tabelle di routing confronta la nuova route con le route già presenti nella tabella di routing. Due route sono uguali se si verificano tutte le condizioni seguenti:

    -   La route viene aggiunta alla stessa destinazione.
    -   La route viene aggiunta dallo stesso client come specificato dal membro **proprietario** della struttura di informazioni della [**\_ route RTM \_**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .
    -   La route viene annunciata dallo stesso adiacente, come specificato dal membro **adiacente** della struttura di [**\_ \_ informazioni della route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .

    Se la route esiste, il gestore delle tabelle di routing restituisce l'handle alla route esistente. In caso contrario, il gestore tabelle di routing aggiunge la route e restituisce l'handle alla nuova route.

    Il client può impostare il parametro *Change \_ Flags* sulla \_ route RTM \_ Change \_ New per indicare a gestione tabelle di routing di aggiungere una nuova route nella destinazione, anche se esiste un'altra route con lo stesso proprietario e i campi adiacenti.

    Il client può impostare il parametro *Change \_ Flags* su RTM \_ route \_ Change \_ prima per indicare a gestione tabelle di routing di aggiornare la prima route nella destinazione di proprietà del client. Questo aggiornamento può essere eseguito se esiste una route di questo tipo, anche se il campo adiacente non corrisponde. Questo flag viene usato dai client che gestiscono una singola route per destinazione.

**Per aggiornare una route, il client deve eseguire la procedura seguente**

1.  Chiamare [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) con l'handle per la route. L'handle è uno precedentemente memorizzato nella cache dal client o restituito da Gestione tabelle di routing da una chiamata che restituisce un handle di route, ad esempio **RtmGetRouteInfo**.
2.  Apportare le modifiche alla struttura [**delle \_ \_ informazioni sulla route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) restituita da Gestione tabelle di routing.
3.  Chiamare [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) con l'handle per la route e la struttura [**di \_ \_ informazioni della route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) modificata.

Nell'esempio di codice seguente viene illustrato come aggiungere una route a una destinazione utilizzando Gestione tabelle di routing come intermediario.


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



 

 




