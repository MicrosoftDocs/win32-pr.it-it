---
title: Informazioni su Routing Table Manager versione 1
description: Gestione tabelle di routing è un repository centrale di informazioni di routing per tutti i protocolli di routing che operano con il servizio Routing e accesso remoto (RRAS).
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- Servizio Routing e accesso remoto RRAS, gestione tabelle di routing versione 1
- Servizio Routing e accesso remoto RRAS, gestione tabelle di routing versione 1, descritta
- Gestione tabelle di routing versione 1 RRAS
- Gestione tabelle di routing versione 1 RRAS, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99f913230db6e6882a36b414914c3924181a221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044837"
---
# <a name="about-routing-table-manager-version-1"></a><span data-ttu-id="09e3b-107">Informazioni su Routing Table Manager versione 1</span><span class="sxs-lookup"><span data-stu-id="09e3b-107">About Routing Table Manager Version 1</span></span>

<span data-ttu-id="09e3b-108">**Windows Server 2003:** Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="09e3b-108">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="09e3b-109">Le nuove applicazioni devono usare l'API di Routing Table Manager versione 2.</span><span class="sxs-lookup"><span data-stu-id="09e3b-109">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="09e3b-110">Gestione tabelle di routing è un repository centrale di informazioni di routing per tutti i protocolli di routing che operano con il servizio Routing e accesso remoto (RRAS).</span><span class="sxs-lookup"><span data-stu-id="09e3b-110">The routing table manager is a central repository of routing information for all routing protocols that operate under Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="09e3b-111">Gestione tabelle di routing fornisce informazioni di routing a tutti i componenti interessati, ad esempio i protocolli di routing, gli agenti di gestione e gli agenti di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="09e3b-111">The routing table manager provides routing information to all interested components, such as routing protocols, management agents, and monitoring agents.</span></span> <span data-ttu-id="09e3b-112">Gestione tabelle di routing determina inoltre la migliore route per ogni rete di destinazione nota ai protocolli di routing.</span><span class="sxs-lookup"><span data-stu-id="09e3b-112">The routing table manager also determines the best route to each destination network known to the routing protocols.</span></span> <span data-ttu-id="09e3b-113">Determina questa route in base alle priorità del protocollo di routing e alle metriche associate alle route.</span><span class="sxs-lookup"><span data-stu-id="09e3b-113">It determines this route based on routing protocol priorities and on metrics associated with the routes.</span></span> <span data-ttu-id="09e3b-114">Si noti che l'amministratore è in grado di configurare le priorità del protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="09e3b-114">Note that the administrator is able to configure routing protocol priorities.</span></span> <span data-ttu-id="09e3b-115">Gestione tabelle di routing passa quindi le informazioni sulle route migliori sui server d'inoltro e di nuovo ai protocolli di routing.</span><span class="sxs-lookup"><span data-stu-id="09e3b-115">The routing table manager then passes the best-route information on to the forwarders and back to the routing protocols.</span></span>

<span data-ttu-id="09e3b-116">Ogni protocollo di routing chiama [**RtmRegisterClient**](rtmregisterclient.md) per la registrazione con gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="09e3b-116">Each routing protocol calls [**RtmRegisterClient**](rtmregisterclient.md) to register with the routing table manager.</span></span> <span data-ttu-id="09e3b-117">**RtmRegisterClient** restituisce un handle utilizzato dal protocollo di routing per aggiungere o eliminare le voci della route.</span><span class="sxs-lookup"><span data-stu-id="09e3b-117">**RtmRegisterClient** returns a handle that is used by the routing protocol to add or delete route entries.</span></span> <span data-ttu-id="09e3b-118">**RtmRegisterClient** consente inoltre al protocollo di routing di registrare un oggetto evento con gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="09e3b-118">**RtmRegisterClient** also allows the routing protocol to register an event object with the routing table manager.</span></span> <span data-ttu-id="09e3b-119">Questo oggetto evento viene segnalato da Gestione tabelle di routing per notificare al protocollo di routing le modifiche apportate alle informazioni sulla Route consigliata.</span><span class="sxs-lookup"><span data-stu-id="09e3b-119">The routing table manager signals this event object to notify the routing protocol of changes in best-route information.</span></span> <span data-ttu-id="09e3b-120">Tutti gli altri componenti possono ottenere informazioni archiviate in Gestione tabelle di routing tramite l'enumerazione route.</span><span class="sxs-lookup"><span data-stu-id="09e3b-120">All other components can obtain information stored in the routing table manager through route enumeration.</span></span>

 

 




