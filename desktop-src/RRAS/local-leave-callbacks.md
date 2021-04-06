---
title: Callback di uscita locale
description: Quando il gestore del gruppo multicast riceve una notifica da IGMP che non sono presenti altri ricevitori per un gruppo in un'interfaccia, il gestore del gruppo multicast richiama la richiamata del callback \_ \_ di uscita locale \_ di PMGM al protocollo di routing su tale interfaccia se ne esiste una. Questo callback notifica il protocollo di routing della modifica.
ms.assetid: 47696533-603c-459f-9aa7-3ce42fff3332
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a98d32e041b048e15497bc7fe35d17628b9331d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044928"
---
# <a name="local-leave-callbacks"></a><span data-ttu-id="0ea5d-104">Callback di uscita locale</span><span class="sxs-lookup"><span data-stu-id="0ea5d-104">Local Leave Callbacks</span></span>

<span data-ttu-id="0ea5d-105">Quando il gestore del gruppo multicast riceve una notifica da IGMP che non sono presenti altri ricevitori per un gruppo in un'interfaccia, il gestore del gruppo multicast richiama la richiamata del callback di [**\_ \_ uscita \_ locale di PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) al protocollo di routing su tale interfaccia se ne esiste una.</span><span class="sxs-lookup"><span data-stu-id="0ea5d-105">After the multicast group manager is notified by IGMP that there are no more receivers present for a group on an interface, the multicast group manager invokes the [**PMGM\_LOCAL\_LEAVE\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) callback to the routing protocol on that interface if one exists.</span></span> <span data-ttu-id="0ea5d-106">Questo callback notifica il protocollo di routing della modifica.</span><span class="sxs-lookup"><span data-stu-id="0ea5d-106">This callback notifies the routing protocol of the change.</span></span>

<span data-ttu-id="0ea5d-107">Questo callback e il [**callback \_ \_ callback di \_ callback locale di PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) vengono usati per sincronizzare l'inoltro tra i protocolli IGMP e di routing.</span><span class="sxs-lookup"><span data-stu-id="0ea5d-107">This callback and the [**PMGM\_LOCAL\_JOIN\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) callback are used to synchronize forwarding between IGMP and routing protocols.</span></span>

 

 




