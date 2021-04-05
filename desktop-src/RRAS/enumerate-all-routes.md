---
title: Enumera tutte le route
description: La procedura seguente illustra i passaggi usati per enumerare le entità usate dall'API RTMv2. Nel codice di esempio seguente viene illustrato come enumerare tutte le route.
ms.assetid: 78a50e4a-f3c7-4a0d-a528-18d35b66369d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c927665cab8d4db492d3a2c5f8e9363fc1fe7be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711341"
---
# <a name="enumerate-all-routes"></a><span data-ttu-id="47619-104">Enumera tutte le route</span><span class="sxs-lookup"><span data-stu-id="47619-104">Enumerate All Routes</span></span>

<span data-ttu-id="47619-105">La procedura seguente illustra i passaggi usati per enumerare le entità usate dall'API RTMv2.</span><span class="sxs-lookup"><span data-stu-id="47619-105">The following procedure outlines the steps used to enumerate any of the entities used by the RTMv2 API.</span></span> <span data-ttu-id="47619-106">Nel codice di esempio seguente viene illustrato come enumerare tutte le route.</span><span class="sxs-lookup"><span data-stu-id="47619-106">The sample code that follows shows how to enumerate all routes.</span></span>

<span data-ttu-id="47619-107">**Il processo di base per ogni enumerazione è il seguente:**</span><span class="sxs-lookup"><span data-stu-id="47619-107">**The basic process for each enumeration is as follows**</span></span>

1.  <span data-ttu-id="47619-108">Avviare l'enumerazione ottenendo un handle da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="47619-108">Start the enumeration by obtaining a handle from the routing table manager.</span></span> <span data-ttu-id="47619-109">Chiamare [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) e [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) per fornire i criteri che specificano il tipo di informazioni enumerate.</span><span class="sxs-lookup"><span data-stu-id="47619-109">Call [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) and [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) to supply the criteria that specifies the kind of information being enumerated.</span></span> <span data-ttu-id="47619-110">Questo criterio include, tuttavia, non è limitato a un intervallo di destinazioni, a una particolare interfaccia e alle visualizzazioni in cui si trovano le informazioni.</span><span class="sxs-lookup"><span data-stu-id="47619-110">This criteria includes, but is not limited to a range of destinations, a particular interface, and the views in which the information resides.</span></span>
2.  <span data-ttu-id="47619-111">Chiamare [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) e [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) una o più volte per recuperare i dati fino a quando non viene restituito \_ nessun \_ altro elemento da Gestione tabelle di routing \_ .</span><span class="sxs-lookup"><span data-stu-id="47619-111">Call [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) and [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) one or more times to retrieve data until the routing table manager returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="47619-112">I dati di route, di destinazione e di hop successivo vengono restituiti nell'ordine delle informazioni sugli indirizzi (e dei valori di preferenza e metrica, se le route vengono enumerate).</span><span class="sxs-lookup"><span data-stu-id="47619-112">The route, destination, and next-hop data is returned in order of the address information (and the preference and metric values, if routes are being enumerated).</span></span>
3.  <span data-ttu-id="47619-113">Chiamare [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) e [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) quando gli handle o le strutture di informazioni associate all'enumerazione non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="47619-113">Call [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) and [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) when the handles or information structures associated with the enumeration are no longer required.</span></span>
4.  <span data-ttu-id="47619-114">Chiamare [**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) per rilasciare l'handle di enumerazione che è stato restituito quando è stata creata l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="47619-114">Call [**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) to release the enumeration handle that was returned when the enumeration was created.</span></span> <span data-ttu-id="47619-115">Questa funzione viene usata per rilasciare l'handle per tutti i tipi di enumerazioni.</span><span class="sxs-lookup"><span data-stu-id="47619-115">This function is used to release the handle for all types of enumerations.</span></span>

> [!Note]  
> <span data-ttu-id="47619-116">Le route presenti nello stato di attesa vengono enumerate solo quando un client richiede i dati di tutte le viste utilizzando la \_ maschera di visualizzazione RTM \_ \_ any.</span><span class="sxs-lookup"><span data-stu-id="47619-116">Routes that are in the hold-down state are only enumerated when a client requests data from all views using RTM\_VIEW\_MASK\_ANY.</span></span>

 

<span data-ttu-id="47619-117">Nell'esempio di codice riportato di seguito viene illustrato come enumerare tutte le route nella tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="47619-117">The following sample code shows how to enumerate all routes in the routing table.</span></span>


```C++
MaxHandles = RegnProfile.MaxHandlesInEnum;

RouteHandles = _alloca(MaxHandles * sizeof(HANDLE));

// Do a "route enumeration" over the whole table
// by passing a NULL DestHandle in this function.

DestHandle = NULL; // Give a valid handle to enumerate over a particular destination

Status = RtmCreateRouteEnum(RtmRegHandle,
                            DestHandle,
                            RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST,
                            RTM_ENUM_OWN_ROUTES, // Get only your own routes
                            NULL,
                            0,
                            NULL,
                            0,
                            &EnumHandle2);
if (Status == NO_ERROR)
{
    do
    {
        NumHandles = MaxHandles;

        Status = RtmGetEnumRoutes(RtmRegHandle
                                  EnumHandle2,
                                  &NumHandles,
                                  RouteHandles);

        for (k = 0; k < NumHandles; k++)
        {
            wprintf("Route %d: %p\n", l++, RouteHandles[k]);

            // Get route information using the route's handle
            Status = RtmGetRouteInfo(...RouteHandles[k]...);

            if (Status == NO_ERROR)
            {
                // Do whatever you want with the route info
                //...

                // Release the route information once you are done
                RtmReleaseRouteInfo(...);
            }
        }

        RtmReleaseRoutes(RtmRegHandle, NumHandles, RouteHandles);
    }
    while (Status == NO_ERROR)

    // Close the enumeration and release its resources
    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle2);
}
```



 

 




