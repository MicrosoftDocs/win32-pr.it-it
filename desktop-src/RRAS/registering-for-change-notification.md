---
title: Registrazione per la notifica delle modifiche
description: Un client può effettuare la registrazione per ricevere la notifica delle modifiche alle informazioni di routing archiviate in Gestione tabelle di routing. Questa richiesta può essere eseguita solo dopo che un client è stato registrato con gestione tabelle di routing.
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3a98062fee73c481c1f47c32fa7eeb5465a112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329604"
---
# <a name="registering-for-change-notification"></a><span data-ttu-id="935e7-104">Registrazione per la notifica delle modifiche</span><span class="sxs-lookup"><span data-stu-id="935e7-104">Registering for Change Notification</span></span>

<span data-ttu-id="935e7-105">Un client può effettuare la registrazione per ricevere la notifica delle modifiche alle informazioni di routing archiviate in Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="935e7-105">A client can register to receive notification of changes to routing information that is stored in the routing table manager.</span></span> <span data-ttu-id="935e7-106">Questa richiesta può essere eseguita solo dopo che un client è stato registrato con gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="935e7-106">This request can only be made after a client has registered with the routing table manager.</span></span>

<span data-ttu-id="935e7-107">Per eseguire la registrazione per la notifica delle modifiche, un client deve chiamare [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), specificando i tipi di modifiche per cui il client deve ricevere una notifica.</span><span class="sxs-lookup"><span data-stu-id="935e7-107">To register for change notification, a client must call [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), specifying the types of changes for which the client must receive notification.</span></span> <span data-ttu-id="935e7-108">Se il client deve ricevere una notifica di modifica a destinazioni specifiche, il client chiama [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) una volta per ogni destinazione.</span><span class="sxs-lookup"><span data-stu-id="935e7-108">If the client must be notified of change to specific destinations, the client calls [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) once for each destination.</span></span>

<span data-ttu-id="935e7-109">Il client può arrestare la ricezione delle notifiche di modifica chiamando [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).</span><span class="sxs-lookup"><span data-stu-id="935e7-109">The client can stop receiving change notifications by calling [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).</span></span>

<span data-ttu-id="935e7-110">Per il codice di esempio che illustra come usare queste funzioni, vedere [registrarsi per la notifica delle modifiche](register-for-change-notification.md).</span><span class="sxs-lookup"><span data-stu-id="935e7-110">For sample code that shows how to use these functions, see [Register For Change Notification](register-for-change-notification.md).</span></span>

 

 




