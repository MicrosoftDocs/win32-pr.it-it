---
title: Aggiungere e aggiornare route tramite RtmAddRouteToDest
description: La funzione RtmAddRouteToDest viene usata per aggiungere nuove route e aggiornare le route esistenti per una destinazione. Le procedure seguenti illustrano entrambi i casi. Il codice di esempio seguente illustra come implementare la prima procedura.
ms.assetid: 17a04511-69f8-4e50-993c-0e558ee72184
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64032aa5f73019e08bb82405d85ffa5ef85abd0526cf7748ec8881b97ab900e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030601"
---
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a>Aggiungere e aggiornare route tramite RtmAddRouteToDest

La funzione [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) viene usata per aggiungere nuove route e aggiornare le route esistenti per una destinazione. Le procedure seguenti illustrano entrambi i casi. Il codice di esempio seguente illustra come implementare la prima procedura.

**Per aggiungere una route, il client deve seguire questa procedura**

1.  Se il client ha già memorizzato nella cache l'handle dell'hop successivo, andare al passaggio 4.
2.  Creare una [**struttura RTM \_ NEXTHOP \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) e compilarla con le informazioni appropriate.
3.  Aggiungere l'hop successivo alla tabella di routing chiamando [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop). Il gestore tabelle di routing restituisce un handle all'hop successivo. Se l'hop successivo esiste già, la tabella di routing non aggiunge l'hop successivo. restituisce invece l'handle all'hop successivo.
4.  Creare una [**struttura RTM \_ ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) e compilarla con le informazioni appropriate, incluso l'handle dell'hop successivo restituito dal gestore tabelle di routing.
5.  Aggiungere la route alla tabella di routing chiamando [**RtmAddRouteToDest.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) Il gestore tabelle di routing confronta la nuova route con le route già presenti nella tabella di routing. Due route sono uguali se si verificano tutte le condizioni seguenti:

    -   La route viene aggiunta alla stessa destinazione.
    -   La route viene aggiunta dallo stesso client specificato dal membro **Owner** della [**struttura RTM ROUTE \_ \_ INFO.**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)
    -   La route viene annunciata dallo stesso router adiacente specificato dal membro **Neighbor** della [**struttura RTM ROUTE \_ \_ INFO.**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)

    Se la route esiste, il gestore delle tabelle di routing restituisce l'handle alla route esistente. In caso contrario, il gestore delle tabelle di routing aggiunge la route e restituisce l'handle alla nuova route.

    Il client può impostare il parametro *Flag \_* di modifica su RTM ROUTE CHANGE NEW per indicare al gestore delle tabelle di routing di aggiungere una nuova route nella destinazione, anche se esiste un'altra route con lo stesso proprietario e gli stessi campi \_ \_ \_ adiacenti.

    Il client può impostare il parametro *\_ Flag* di modifica su RTM ROUTE CHANGE FIRST per indicare al gestore tabelle di routing di aggiornare la prima route nella destinazione di proprietà \_ del \_ \_ client. Questo aggiornamento può essere eseguito se esiste una route di questo tipo, anche se il campo adiacente non corrisponde. Questo flag viene usato dai client che gestiscono una singola route per ogni destinazione.

**Per aggiornare una route, il client deve seguire questa procedura**

1.  Chiamare [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) con l'handle per la route. L'handle è un handle precedentemente memorizzato nella cache dal client o restituito dal gestore tabelle di routing da una chiamata che restituisce un handle di route, ad esempio **RtmGetRouteInfo.**
2.  Apportare le modifiche alla [**struttura RTM \_ ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) restituita dal gestore tabelle di routing.
3.  Chiamare [**RtmAddRouteToDest con**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) l'handle per la route e la struttura [**RTM ROUTE \_ \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) modificata.

Nell'esempio di codice seguente viene illustrato come aggiungere una route a una destinazione utilizzando il gestore tabelle di routing come intermediario.


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



 

 




