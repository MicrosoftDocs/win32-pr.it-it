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
# <a name="enumerate-all-routes"></a>Enumera tutte le route

La procedura seguente illustra i passaggi usati per enumerare le entità usate dall'API RTMv2. Nel codice di esempio seguente viene illustrato come enumerare tutte le route.

**Il processo di base per ogni enumerazione è il seguente:**

1.  Avviare l'enumerazione ottenendo un handle da Gestione tabelle di routing. Chiamare [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) e [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) per fornire i criteri che specificano il tipo di informazioni enumerate. Questo criterio include, tuttavia, non è limitato a un intervallo di destinazioni, a una particolare interfaccia e alle visualizzazioni in cui si trovano le informazioni.
2.  Chiamare [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) e [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) una o più volte per recuperare i dati fino a quando non viene restituito \_ nessun \_ altro elemento da Gestione tabelle di routing \_ . I dati di route, di destinazione e di hop successivo vengono restituiti nell'ordine delle informazioni sugli indirizzi (e dei valori di preferenza e metrica, se le route vengono enumerate).
3.  Chiamare [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) e [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) quando gli handle o le strutture di informazioni associate all'enumerazione non sono più necessari.
4.  Chiamare [**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) per rilasciare l'handle di enumerazione che è stato restituito quando è stata creata l'enumerazione. Questa funzione viene usata per rilasciare l'handle per tutti i tipi di enumerazioni.

> [!Note]  
> Le route presenti nello stato di attesa vengono enumerate solo quando un client richiede i dati di tutte le viste utilizzando la \_ maschera di visualizzazione RTM \_ \_ any.

 

Nell'esempio di codice riportato di seguito viene illustrato come enumerare tutte le route nella tabella di routing.


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



 

 




