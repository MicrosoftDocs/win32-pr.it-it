---
title: Enumerare tutte le route
description: La procedura seguente illustra i passaggi usati per enumerare le entità usate dall'API RTMv2. Il codice di esempio seguente illustra come enumerare tutte le route.
ms.assetid: 78a50e4a-f3c7-4a0d-a528-18d35b66369d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5f8707c7cf78f274fedaca3fb4882ae36dbd569ab5fa1260ec3b6cb663aced3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101851"
---
# <a name="enumerate-all-routes"></a>Enumerare tutte le route

La procedura seguente illustra i passaggi usati per enumerare le entità usate dall'API RTMv2. Il codice di esempio seguente illustra come enumerare tutte le route.

**Il processo di base per ogni enumerazione è il seguente:**

1.  Avviare l'enumerazione ottenendo un handle dal gestore tabelle di routing. Chiamare [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) e [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) per specificare i criteri che specificano il tipo di informazioni da enumerare. Questi criteri includono, ma non è limitato a un intervallo di destinazioni, a una particolare interfaccia e alle viste in cui si trovano le informazioni.
2.  Chiamare [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) e [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) una o più volte per recuperare i dati finché la gestione tabelle di routing non restituisce ERROR \_ NO MORE \_ \_ ITEMS. I dati di route, destinazione e hop successivo vengono restituiti in base alle informazioni sull'indirizzo (e ai valori di preferenza e metrica, se le route vengono enumerate).
3.  Chiamare [**RtmReleaseDests,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests) [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) e [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) quando gli handle o le strutture di informazioni associate all'enumerazione non sono più necessari.
4.  Chiamare [**RtmDeleteEnumHandle per**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) rilasciare l'handle di enumerazione restituito al momento della creazione dell'enumerazione. Questa funzione viene usata per rilasciare l'handle per tutti i tipi di enumerazioni.

> [!Note]  
> Le route in stato di blocco vengono enumerate solo quando un client richiede dati da tutte le viste usando RTM \_ VIEW \_ MASK \_ ANY.

 

Il codice di esempio seguente illustra come enumerare tutte le route nella tabella di routing.


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



 

 




