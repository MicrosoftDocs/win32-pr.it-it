---
title: Callback di avviso RPF
description: Dopo che il gestore del gruppo multicast riceve la notifica di un pacchetto da una nuova origine o da un pacchetto destinato a un nuovo gruppo, il gestore del gruppo multicast cerca la route verso l'origine nella visualizzazione multicast della tabella di routing.
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7832a25f8b44821f4b46a69943b4bba3519207c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714665"
---
# <a name="rpf-alert-callbacks"></a><span data-ttu-id="3ddef-103">Callback di avviso RPF</span><span class="sxs-lookup"><span data-stu-id="3ddef-103">RPF Alert Callbacks</span></span>

<span data-ttu-id="3ddef-104">Dopo che il gestore del gruppo multicast riceve la notifica di un pacchetto da una nuova origine o da un pacchetto destinato a un nuovo gruppo, il gestore del gruppo multicast cerca la route verso l'origine nella visualizzazione multicast della tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="3ddef-104">After the multicast group manager receives notification of a packet from a new source or of a packet that is destined for a new group, the multicast group manager looks up the route to the source in the multicast view of the routing table.</span></span> <span data-ttu-id="3ddef-105">Il gestore del gruppo multicast richiama quindi il callback di [**\_ \_ callback RPF di PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) al protocollo che possiede l'interfaccia su cui sono stati ricevuti i dati.</span><span class="sxs-lookup"><span data-stu-id="3ddef-105">The multicast group manager then invokes the [**PMGM\_RPF\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) callback to the protocol that owns the interface the data arrived on.</span></span>

<span data-ttu-id="3ddef-106">Una volta richiamato questo callback, il protocollo di routing può modificare l'interfaccia in ingresso se il protocollo di routing deve ricevere i dati per il gruppo in un'interfaccia diversa.</span><span class="sxs-lookup"><span data-stu-id="3ddef-106">After this callback is invoked, the routing protocol can change the incoming interface if the routing protocol must receive the data for the group on a different interface.</span></span>

 

 




