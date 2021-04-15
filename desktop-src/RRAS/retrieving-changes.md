---
title: Recupero delle modifiche
description: Una volta che un client si è registrato per la notifica di determinate modifiche e si verifica una o più di queste modifiche, il client riceve una notifica da Gestione tabelle di routing.
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ccf66d8a1df671cbd9059c444cf26321911bb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515619"
---
# <a name="retrieving-changes"></a><span data-ttu-id="c6118-103">Recupero delle modifiche</span><span class="sxs-lookup"><span data-stu-id="c6118-103">Retrieving Changes</span></span>

<span data-ttu-id="c6118-104">Una volta che un client si è registrato per la notifica di determinate modifiche e si verifica una o più di queste modifiche, il client riceve una notifica da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="c6118-104">Once a client has registered for notification of certain changes and one or more of these changes occurs, the client receives a notification from the routing table manager.</span></span> <span data-ttu-id="c6118-105">Gestione tabelle di routing utilizza il callback di [**\_ \_ callback evento RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) fornito in una chiamata precedente a [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity).</span><span class="sxs-lookup"><span data-stu-id="c6118-105">The routing table manager uses the [**RTM\_EVENT\_CALLBACK**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) callback that was supplied in a previous call to [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity).</span></span> <span data-ttu-id="c6118-106">Gestione tabelle di routing indica che \_ \_ si è verificato un evento di notifica della modifica RTM.</span><span class="sxs-lookup"><span data-stu-id="c6118-106">The routing table manager indicates that a RTM\_CHANGE\_NOTIFICATION event has occurred.</span></span>

<span data-ttu-id="c6118-107">Per il codice di esempio che illustra come usare queste funzioni, vedere [usare il callback di notifica degli eventi](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="c6118-107">For sample code that shows how to use these functions, see [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




