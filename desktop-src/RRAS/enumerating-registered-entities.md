---
title: Enumerazione delle entità registrate
description: Dopo la registrazione di un client, il client può ottenere un elenco di tutti gli altri client registrati con gestione tabelle di routing. Alcuni client devono eseguire determinate operazioni se viene rilevata la presenza di un determinato tipo di client.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac92ccf89336d3fbca378209b9e79877d9b426a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044765"
---
# <a name="enumerating-registered-entities"></a><span data-ttu-id="a5b6f-104">Enumerazione delle entità registrate</span><span class="sxs-lookup"><span data-stu-id="a5b6f-104">Enumerating Registered Entities</span></span>

<span data-ttu-id="a5b6f-105">Dopo la registrazione di un client, il client può ottenere un elenco di tutti gli altri client registrati con gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="a5b6f-105">After a client has registered, the client can obtain a list of all the other clients that have registered with the routing table manager.</span></span> <span data-ttu-id="a5b6f-106">Alcuni client devono eseguire determinate operazioni se viene rilevata la presenza di un determinato tipo di client.</span><span class="sxs-lookup"><span data-stu-id="a5b6f-106">Some clients must perform certain operations if the presence of a particular type of client is detected.</span></span>

<span data-ttu-id="a5b6f-107">Il client può chiamare la funzione [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) .</span><span class="sxs-lookup"><span data-stu-id="a5b6f-107">The client can call the [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) function.</span></span> <span data-ttu-id="a5b6f-108">Viene restituito un buffer di strutture di [**\_ \_ informazioni sull'entità RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) .</span><span class="sxs-lookup"><span data-stu-id="a5b6f-108">A buffer of [**RTM\_ENTITY\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) structures is returned.</span></span> <span data-ttu-id="a5b6f-109">Dopo che il client ha elaborato queste informazioni, il client deve chiamare [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) per rilasciare gli handle nelle strutture delle **\_ \_ informazioni sull'entità RTM** .</span><span class="sxs-lookup"><span data-stu-id="a5b6f-109">After the client has processed this information, the client should call [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) to release the handles in the **RTM\_ENTITY\_INFO** structures.</span></span>

<span data-ttu-id="a5b6f-110">Se il client di gestione tabelle di routing ha fornito una funzione di callback nella chiamata a [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), il client riceve una notifica quando viene effettuata la registrazione o l'annullamento della registrazione di altri client.</span><span class="sxs-lookup"><span data-stu-id="a5b6f-110">If the routing table manager client supplied a callback function in the call to [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), the client is notified when any other clients register or unregister.</span></span>

<span data-ttu-id="a5b6f-111">Per il codice di esempio che illustra come usare queste funzioni, vedere [enumerare le entità registrate](enumerate-the-registered-entities.md) e [usare il callback di notifica degli eventi](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="a5b6f-111">For sample code that shows how to use these functions, see [Enumerate the Registered Entities](enumerate-the-registered-entities.md) and [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




