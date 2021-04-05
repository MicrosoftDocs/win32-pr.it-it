---
title: Aggiornamento di route con RtmAddRouteToDest
description: Se il client non richiede efficienza durante l'aggiunta di una route, deve usare il metodo seguente per aggiornare le route.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c7972b2d5ec0996cafc1dd32a8a4056a6aeb0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955749"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a><span data-ttu-id="55cdc-103">Aggiornamento di route con RtmAddRouteToDest</span><span class="sxs-lookup"><span data-stu-id="55cdc-103">Updating Routes Using RtmAddRouteToDest</span></span>

<span data-ttu-id="55cdc-104">Se il client non richiede efficienza durante l'aggiunta di una route, deve usare il metodo seguente per aggiornare le route.</span><span class="sxs-lookup"><span data-stu-id="55cdc-104">If the client does not require efficiency when adding a route, it should use the following method of updating routes.</span></span> <span data-ttu-id="55cdc-105">Questo metodo è meno efficiente poiché richiede l'ottenimento di un handle per la route e il passaggio della struttura delle [**\_ \_ informazioni sulla route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) da e verso gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="55cdc-105">This method is less efficient since it requires obtaining a handle to the route and passing the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure to and from the routing table manager.</span></span> <span data-ttu-id="55cdc-106">Questo metodo richiede inoltre più tempo.</span><span class="sxs-lookup"><span data-stu-id="55cdc-106">This method also takes more time.</span></span> <span data-ttu-id="55cdc-107">Poiché [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) non modifica direttamente la tabella di routing, l'utilizzo di questo metodo consente di rendere più semplice l'efficienza.</span><span class="sxs-lookup"><span data-stu-id="55cdc-107">Since [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) does not manipulate the routing table directly, using this method trades efficiency for simplicity.</span></span>

<span data-ttu-id="55cdc-108">Per il codice di esempio che illustra come usare queste funzioni, vedere [aggiungere e aggiornare le route con RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).</span><span class="sxs-lookup"><span data-stu-id="55cdc-108">For sample code that shows how to use these functions, see [Add and Update Routes Using RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).</span></span>

 

 




