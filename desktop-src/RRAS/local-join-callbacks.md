---
title: Callback di join locali
description: Quando il gestore del gruppo multicast riceve una notifica da IGMP che sono presenti nuovi ricevitori per un gruppo in un'interfaccia, il gestore del gruppo multicast richiama \_ il \_ \_ callback di callback di PMGM local join al protocollo di routing che possiede l'interfaccia, se esistente.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c97f0e16e08bc3781b946a51f69d2b0d65b3272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471550"
---
# <a name="local-join-callbacks"></a><span data-ttu-id="ff9ca-103">Callback di join locali</span><span class="sxs-lookup"><span data-stu-id="ff9ca-103">Local Join Callbacks</span></span>

<span data-ttu-id="ff9ca-104">Quando il gestore del gruppo multicast riceve una notifica da IGMP che sono presenti nuovi ricevitori per un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il callback di [**callback di PMGM \_ Local \_ join \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) al protocollo di routing che possiede l'interfaccia, se esistente.</span><span class="sxs-lookup"><span data-stu-id="ff9ca-104">After the multicast group manager is notified by IGMP that new receivers are present for a group on an interface, the multicast group manager invokes the [**PMGM\_LOCAL\_JOIN\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) callback to the routing protocol that owns the interface if one exists.</span></span> <span data-ttu-id="ff9ca-105">Questo callback notifica il protocollo di routing della modifica.</span><span class="sxs-lookup"><span data-stu-id="ff9ca-105">This callback notifies the routing protocol of the change.</span></span>

<span data-ttu-id="ff9ca-106">Questo callback e il callback di [**\_ \_ \_ callback di uscita locale PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) vengono usati per sincronizzare l'inoltro tra i protocolli IGMP e di routing.</span><span class="sxs-lookup"><span data-stu-id="ff9ca-106">This callback and the [**PMGM\_LOCAL\_LEAVE\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) callback are used to synchronize forwarding between IGMP and routing protocols.</span></span>

 

 




