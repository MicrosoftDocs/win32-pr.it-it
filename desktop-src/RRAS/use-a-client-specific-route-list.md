---
title: Usare un elenco di route Client-Specific
description: Nelle procedure riportate di seguito vengono descritti i passaggi per utilizzare gli elenchi di route specifici del client. Il codice di esempio seguente illustra come implementare la procedura.
ms.assetid: aa9b7b2a-259f-4ce1-afb6-c04875e8ffe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cfa893bda9e850527c7ebe35590dbe2d08a490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298749"
---
# <a name="use-a-client-specific-route-list"></a><span data-ttu-id="148d9-104">Usare un elenco di route Client-Specific</span><span class="sxs-lookup"><span data-stu-id="148d9-104">Use a Client-Specific Route List</span></span>

<span data-ttu-id="148d9-105">Nelle procedure riportate di seguito vengono descritti i passaggi per utilizzare gli elenchi di route specifici del client.</span><span class="sxs-lookup"><span data-stu-id="148d9-105">The following procedures outlines the steps to use the client-specific route lists.</span></span> <span data-ttu-id="148d9-106">Il codice di esempio seguente illustra come implementare la procedura.</span><span class="sxs-lookup"><span data-stu-id="148d9-106">The sample code that follows shows how to implement the procedure.</span></span>

<span data-ttu-id="148d9-107">**Per usare questa funzionalità, un client deve eseguire la procedura seguente**</span><span class="sxs-lookup"><span data-stu-id="148d9-107">**To use this feature, a client should take the following steps**</span></span>

1.  <span data-ttu-id="148d9-108">Chiamare [**RtmCreateRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist) per ottenere un handle da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="148d9-108">Call [**RtmCreateRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist) to obtain a handle from the routing table manager.</span></span>
2.  <span data-ttu-id="148d9-109">Chiamare [**RtmInsertInRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist) ogni volta che il client deve aggiungere una route a questo elenco.</span><span class="sxs-lookup"><span data-stu-id="148d9-109">Call [**RtmInsertInRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist) whenever the client must add a route to this list.</span></span>
3.  <span data-ttu-id="148d9-110">Quando il client non richiede più l'elenco, deve chiamare [**RtmDeleteRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist) per rimuovere l'elenco.</span><span class="sxs-lookup"><span data-stu-id="148d9-110">When the client no longer requires the list, it should call [**RtmDeleteRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist) to remove the list.</span></span>

<span data-ttu-id="148d9-111">**Se il client deve enumerare le route nell'elenco, il client deve eseguire i passaggi seguenti.**</span><span class="sxs-lookup"><span data-stu-id="148d9-111">**If the client must enumerate the routes on the list, the client should take the following steps**</span></span>

1.  <span data-ttu-id="148d9-112">Chiamare [**RtmCreateRouteListEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum) per ottenere un handle di enumerazione da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="148d9-112">Call [**RtmCreateRouteListEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum) to obtain an enumeration handle from the routing table manager.</span></span>
2.  <span data-ttu-id="148d9-113">Chiamare [**RtmGetListEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes) per ottenere gli handle per le route nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="148d9-113">Call [**RtmGetListEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes) to obtain the handles to the routes in the list.</span></span>
3.  <span data-ttu-id="148d9-114">Chiamare [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) per rilasciare gli handle quando non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="148d9-114">Call [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) to release the handles when no longer required.</span></span>

<span data-ttu-id="148d9-115">Nell'esempio di codice seguente viene illustrato come creare e utilizzare un elenco di route specifico del client.</span><span class="sxs-lookup"><span data-stu-id="148d9-115">The following sample code shows how to create and use a client-specific route list.</span></span>


```C++
HANDLE RouteListHandle1;
HANDLE RouteListHandle2;

// Create two entity-specific lists to add routes to

Status = RtmCreateRouteList(RtmRegHandle,
                            &RouteListHandle1);
// Check Status
//...

Status = RtmCreateRouteList(RtmRegHandle,
                            &RouteListHandle2);
// Check Status
//...

// Assume you have added a bunch of routes
// by calling RtmAddRouteToDest many times
// with 'RouteListHandle1' specified similar to
// Status = RtmAddRouteToDest(RtmRegHandle,
//                            ...
//                            RouteListHandle1,
//                            ...
//                            &ChangeFlags);

// Enumerate routes in RouteListHandle1 list

// Create an enumeration on the route list

Status = RtmCreateRouteListEnum(RtmRegHandle,
                                RouteListHandle1,
                                &EnumHandle);

if (Status == NO_ERROR)
{
        // Allocate space on the top of the stack
        
    MaxHandles = RegnProfile.MaxHandlesInEnum;

    RouteHandles = _alloca(MaxHandles * sizeof(HANDLE));

    // Note how the termination condition is different
    // from other enumerations - the call to the function
    // RtmGetListEnumRoutes always returns NO_ERROR
    // Quit when you get fewer handles than requested
    
    do
    {
                // Get next set of routes from the list enumeration
        
        NumHandles = MaxHandles;

        Status = RtmGetListEnumRoutes(RtmRegHandle,
                                      EnumHandle,
                                      &NumHandles,
                                      RouteHandles);

        for (i = 0; i < NumHandles; i++)
        {
            Print("Route Handle %5lu: %p\n", i, RouteHandles[i]);
        }

        // Move all these routes to another route list
        // They are automatically removed from the old one
        
        Status = RtmInsertInRouteList(RtmRegHandle,
                                      RouteListHandle2,
                                      NumHandles,
                                      RouteHandles);
        // Check Status...
        
                // Release the routes that have been enumerated
        
        RtmReleaseRoutes(RtmRegHandle, NumHandles, RouteHandles);
    }
    while (NumHandles == MaxHandles);

    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle);
}

// Destroy all the entity-specific route lists 
// after removing all routes from these lists;
// the routes themselves are not deleted

Status = RtmDeleteRouteList(RtmRegHandle, RouteListHandle1);
ASSERT(Status == NO_ERROR);


Status = RtmDeleteRouteList(RtmRegHandle, RouteListHandle2);
ASSERT(Status == NO_ERROR);
```



 

 




