---
title: Aggiornare una route sul posto usando RtmUpdateAndUnlockRoute
description: Nella procedura riportata di seguito vengono illustrati i passaggi utilizzati per aggiornare una route sul posto. Il codice di esempio seguente illustra come implementare la procedura.
ms.assetid: 3598a28f-8ade-4b3f-9d31-4f2c84df2dd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb79b86645d77f0ee44ffd06b8ef6f403dbd8ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396318"
---
# <a name="update-a-route-in-place-using-rtmupdateandunlockroute"></a>Aggiornare una route sul posto usando RtmUpdateAndUnlockRoute

Nella procedura riportata di seguito vengono illustrati i passaggi utilizzati per aggiornare una route sul posto. Il codice di esempio seguente illustra come implementare la procedura.

**Per aggiornare una route sul posto, il client deve eseguire la procedura seguente**

1.  Bloccare la route chiamando [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute). Attualmente questa funzione blocca effettivamente la destinazione della route. Gestione tabelle di routing restituisce un puntatore alla route.
2.  Usare il puntatore alla struttura delle [**\_ \_ informazioni sulla route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) di gestione tabelle di routing, ottenuta nel passaggio 1, per apportare le modifiche necessarie alla route. Quando si esegue l'aggiornamento sul posto, è possibile modificare solo alcuni membri della struttura di **\_ \_ informazioni della route RTM** . Questi membri sono: **Neighbor**, **PrefInfo**, **EntitySpecificInfo**, **BelongsToViews** e **NextHopsList**.
    > [!Note]  
    > Se il client aggiunge informazioni ai membri **Neighbor** o **NextHopsList** , il client deve chiamare [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) per incrementare in modo esplicito il conteggio dei riferimenti mantenuto da Gestione tabelle di routing sull'oggetto hop successivo. Analogamente, se il client rimuove le informazioni dal membro **NextHopsList** , il client deve chiamare [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) per decrementare il conteggio dei riferimenti.

     

3.  Chiamare [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) per notificare al gestore della tabella di routing che è stata apportata una modifica. Gestione tabelle di routing consente di eseguire il commit delle modifiche, aggiornare la destinazione in modo che rifletta le nuove informazioni, quindi sbloccare la route.

Il codice di esempio seguente illustra come aggiornare direttamente una route, usando un puntatore alle informazioni effettive sulla Route nella tabella di routing.


```C++
Status = RtmLockRoute(RtmRegHandle,
                      RouteHandle,
                      TRUE,
                      TRUE,
                      &RoutePointer);

if (Status == NO_ERROR)
{
        // Update route parameters in place (i.e., directly on 
// the routing table manager's copy)
    
    // Update the metric and views of the route
    RoutePointer->PrefInfo.Metric = 16;

    // Change the views so that the route belongs to only the multicast view
    RoutePointer->BelongsToViews = RTM_VIEW_MASK_MCAST;

    // Set the entity-specific information to X
    RoutePointer->EntitySpecificInfo = X;

    // Note that the following manipulation of
    // next-hop references is not needed when
    // using RtmAddRouteToDest, as it is done
    // by the routing table manager automatically
    
    // Change next hop from NextHop1 to NextHop2
    NextHop1 = RoutePointer->NextHopsList.NextHop[0];

    // Explicitly dereference the old next hop
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHop1);

    RoutePointer->NextHopsList.NextHop[0] = NextHop2;

    // Explicitly reference next hop being added
    RtmReferenceHandles(RtmRegHandle, 1, &NextHop2);

    // Call the routing table manager to indicate that route information
    // has changed, and that its position might
    // have to be rearranged and the corresponding destination
    // needs to be updated to reflect this change.
    
    Status = RtmUpdateAndUnlockRoute(RtmRegHandle,
                                     RouteHandle,
                                     INFINITE, // Keep forever
                                     NULL,
                                     0,
                                     NULL,
                                     &ChangeFlags);
    ASSERT(Status == NO_ERROR);
}
```



 

 




