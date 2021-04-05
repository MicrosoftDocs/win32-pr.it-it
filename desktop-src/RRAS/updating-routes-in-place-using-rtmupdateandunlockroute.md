---
title: Aggiornamento delle route sul posto mediante RtmUpdateAndUnlockRoute
description: L'aggiornamento sul posto è in genere più efficiente rispetto all'aggiornamento della tabella di routing con un metodo indiretto, ad esempio quello usato dalla funzione RtmAddRouteToDest.
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d76d2af5d60172b890eefa1041a08d47a5221b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044873"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a><span data-ttu-id="bc2ca-103">Aggiornamento delle route sul posto mediante RtmUpdateAndUnlockRoute</span><span class="sxs-lookup"><span data-stu-id="bc2ca-103">Updating Routes In Place Using RtmUpdateAndUnlockRoute</span></span>

<span data-ttu-id="bc2ca-104">L'aggiornamento sul posto è in genere più efficiente rispetto all'aggiornamento della tabella di routing con un metodo indiretto, ad esempio quello usato dalla funzione [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) .</span><span class="sxs-lookup"><span data-stu-id="bc2ca-104">Updating in place is generally more efficient than updating the routing table with an indirect method such as that used by the [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) function.</span></span> <span data-ttu-id="bc2ca-105">Questo metodo è più efficiente perché il client non è necessario per ottenere un handle, né per passare la struttura delle [**\_ \_ informazioni sulla route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) da e verso gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="bc2ca-105">This method is more efficient because the client is not required to obtain a handle, nor to pass the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure to and from the routing table manager.</span></span> <span data-ttu-id="bc2ca-106">Questo metodo richiede anche meno tempo.</span><span class="sxs-lookup"><span data-stu-id="bc2ca-106">This method also takes less time.</span></span> <span data-ttu-id="bc2ca-107">Tuttavia, l'aggiornamento diretto della tabella di routing può essere rischioso, perché il servizio di gestione delle tabelle di routing non funziona come intermediario.</span><span class="sxs-lookup"><span data-stu-id="bc2ca-107">However, directly updating the routing table can be risky, since the routing table manager is not functioning as an intermediary.</span></span>

<span data-ttu-id="bc2ca-108">Per il codice di esempio che illustra come usare queste funzioni, vedere [aggiornare una route sul posto usando RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).</span><span class="sxs-lookup"><span data-stu-id="bc2ca-108">For sample code that shows how to use these functions, see [Update a Route In Place Using RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).</span></span>

 

 




