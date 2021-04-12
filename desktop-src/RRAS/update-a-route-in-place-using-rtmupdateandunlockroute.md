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
# <a name="update-a-route-in-place-using-rtmupdateandunlockroute"></a><span data-ttu-id="d8b4b-104">Aggiornare una route sul posto usando RtmUpdateAndUnlockRoute</span><span class="sxs-lookup"><span data-stu-id="d8b4b-104">Update a Route In Place Using RtmUpdateAndUnlockRoute</span></span>

<span data-ttu-id="d8b4b-105">Nella procedura riportata di seguito vengono illustrati i passaggi utilizzati per aggiornare una route sul posto.</span><span class="sxs-lookup"><span data-stu-id="d8b4b-105">The following procedure outlines the steps used to update a route in place.</span></span> <span data-ttu-id="d8b4b-106">Il codice di esempio seguente illustra come implementare la procedura.</span><span class="sxs-lookup"><span data-stu-id="d8b4b-106">The sample code that follows shows how to implement the procedure.</span></span>

<span data-ttu-id="d8b4b-107">**Per aggiornare una route sul posto, il client deve eseguire la procedura seguente**</span><span class="sxs-lookup"><span data-stu-id="d8b4b-107">**To update a route in place, the client should take the following steps**</span></span>

1.  <span data-ttu-id="d8b4b-108">Bloccare la route chiamando [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute).</span><span class="sxs-lookup"><span data-stu-id="d8b4b-108">Lock the route by calling [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute).</span></span> <span data-ttu-id="d8b4b-109">Attualmente questa funzione blocca effettivamente la destinazione della route.</span><span class="sxs-lookup"><span data-stu-id="d8b4b-109">Currently, this function actually locks the route's destination.</span></span> <span data-ttu-id="d8b4b-110">Gestione tabelle di routing restituisce un puntatore alla route.</span><span class="sxs-lookup"><span data-stu-id="d8b4b-110">The routing table manager returns a pointer to the route.</span></span>
2.  <span data-ttu-id="d8b4b-111">Usare il puntatore alla struttura delle [**\_ \_ informazioni sulla route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) di gestione tabelle di routing, ottenuta nel passaggio 1, per apportare le modifiche necessarie alla route.</span><span class="sxs-lookup"><span data-stu-id="d8b4b-111">Use the pointer to the routing table manager's [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure, obtained in step 1, to make the necessary changes to the route.</span></span> <span data-ttu-id="d8b4b-112">Quando si esegue l'aggiornamento sul posto, è possibile modificare solo alcuni membri della struttura di **\_ \_ informazioni della route RTM** .</span><span class="sxs-lookup"><span data-stu-id="d8b4b-112">Only certain members of the **RTM\_ROUTE\_INFO** structure can be modified when updating in place.</span></span> <span data-ttu-id="d8b4b-113">Questi membri sono: **Neighbor**, **PrefInfo**, **EntitySpecificInfo**, **BelongsToViews** e **NextHopsList**.</span><span class="sxs-lookup"><span data-stu-id="d8b4b-113">These members are: **Neighbour**, **PrefInfo**, **EntitySpecificInfo**, **BelongsToViews**, and **NextHopsList**.</span></span>
    > [!Note]  
    > <span data-ttu-id="d8b4b-114">Se il client aggiunge informazioni ai membri **Neighbor** o **NextHopsList** , il client deve chiamare [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) per incrementare in modo esplicito il conteggio dei riferimenti mantenuto da Gestione tabelle di routing sull'oggetto hop successivo.</span><span class="sxs-lookup"><span data-stu-id="d8b4b-114">If the client adds information to either the **Neighbour** or **NextHopsList** members, the client must call [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) to explicitly increment the reference count that the routing table manager keeps on the next-hop object.</span></span> <span data-ttu-id="d8b4b-115">Analogamente, se il client rimuove le informazioni dal membro **NextHopsList** , il client deve chiamare [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) per decrementare il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="d8b4b-115">Similarly, if the client removes information from the **NextHopsList** member, the client must call [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) to decrement the reference count.</span></span>

     

3.  <span data-ttu-id="d8b4b-116">Chiamare [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) per notificare al gestore della tabella di routing che è stata apportata una modifica.</span><span class="sxs-lookup"><span data-stu-id="d8b4b-116">Call [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) to notify the routing table manager that a change has taken place.</span></span> <span data-ttu-id="d8b4b-117">Gestione tabelle di routing consente di eseguire il commit delle modifiche, aggiornare la destinazione in modo che rifletta le nuove informazioni, quindi sbloccare la route.</span><span class="sxs-lookup"><span data-stu-id="d8b4b-117">The routing table manager commits the changes, updates the destination to reflect the new information, and then unlocks the route.</span></span>

<span data-ttu-id="d8b4b-118">Il codice di esempio seguente illustra come aggiornare direttamente una route, usando un puntatore alle informazioni effettive sulla Route nella tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="d8b4b-118">The following sample code shows how to update a route directly, using a pointer to the actual route information in the routing table.</span></span>


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



 

 




