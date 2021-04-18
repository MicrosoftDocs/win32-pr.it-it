---
title: Gestione tabelle di routing
description: Gestione tabelle di routing è il repository centrale di informazioni di routing per tutti i protocolli di routing che operano nel servizio Routing e accesso remoto (RRAS).
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98094eb34c8575e0c24854813fc7458c98749568
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297829"
---
# <a name="routing-table-manager"></a><span data-ttu-id="25bf2-103">Gestione tabelle di routing</span><span class="sxs-lookup"><span data-stu-id="25bf2-103">Routing Table Manager</span></span>

<span data-ttu-id="25bf2-104">Gestione tabelle di routing è il repository centrale di informazioni di routing per tutti i protocolli di routing che operano nel servizio Routing e accesso remoto (RRAS).</span><span class="sxs-lookup"><span data-stu-id="25bf2-104">The routing table manager is the central repository of routing information for all routing protocols that operate under the Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="25bf2-105">Invia una notifica ai client quando si sono verificate modifiche e consente ai client di scambiare informazioni private.</span><span class="sxs-lookup"><span data-stu-id="25bf2-105">It notifies clients when changes have occurred, and allows clients to exchange private information.</span></span>

<span data-ttu-id="25bf2-106">Gestione tabelle di routing fornisce informazioni di routing a tutti i client interessati, ad esempio i protocolli di routing, i programmi di gestione e i programmi di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="25bf2-106">The routing table manager provides routing information to all interested clients, such as routing protocols, management programs, and monitoring programs.</span></span> <span data-ttu-id="25bf2-107">Gestione tabelle di routing determina inoltre il percorso migliore per ogni rete di destinazione nota ai protocolli di routing.</span><span class="sxs-lookup"><span data-stu-id="25bf2-107">The routing table manager also determines the best route to each destination network that is known to the routing protocols.</span></span> <span data-ttu-id="25bf2-108">Gestione tabelle di routing determina questa route in base alle priorità del protocollo di routing e alle metriche associate alle route.</span><span class="sxs-lookup"><span data-stu-id="25bf2-108">The routing table manager determines this route based on routing protocol priorities and on the metrics associated with the routes.</span></span> <span data-ttu-id="25bf2-109">La persona che gestisce il router può configurare le priorità del protocollo di routing tramite la console di gestione di RRAS.</span><span class="sxs-lookup"><span data-stu-id="25bf2-109">The person administering the router can configure routing protocol priorities using the RRAS management console.</span></span>

<span data-ttu-id="25bf2-110">Gestione tabelle di routing passa le informazioni sulla route migliore ai server d'inoltro (uno per famiglia di indirizzi o uno per interfaccia) e a tutti i client interessati.</span><span class="sxs-lookup"><span data-stu-id="25bf2-110">The routing table manager passes the best-route information to the forwarders (one per address family, or one per interface) and to all interested clients.</span></span>

<span data-ttu-id="25bf2-111">Ogni client esegue la registrazione con gestione tabelle di routing e in return riceve un handle che il client usa per aggiungere o eliminare route.</span><span class="sxs-lookup"><span data-stu-id="25bf2-111">Each client registers with the routing table manager, and in return receives a handle that the client uses to add or delete routes.</span></span> <span data-ttu-id="25bf2-112">I client possono recuperare le informazioni archiviate nella tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="25bf2-112">Clients can retrieve information stored in the routing table.</span></span> <span data-ttu-id="25bf2-113">Inoltre, i client possono eseguire la registrazione con gestione tabelle di routing per ricevere notifiche delle modifiche apportate al percorso migliore a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="25bf2-113">Additionally, clients can register with the routing table manager to receive notification of changes to the best route to a destination.</span></span>

 

 




