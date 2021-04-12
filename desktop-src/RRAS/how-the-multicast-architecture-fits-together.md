---
title: Interazione tra l'architettura multicast
description: In questa sezione viene descritta una configurazione di esempio e il modo in cui i componenti principali si adattano insieme.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc82178568bac01e89eb0a4d6ea9222d45e7f5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221674"
---
# <a name="how-the-multicast-architecture-fits-together"></a><span data-ttu-id="d6e0e-103">Interazione tra l'architettura multicast</span><span class="sxs-lookup"><span data-stu-id="d6e0e-103">How the Multicast Architecture Fits Together</span></span>

<span data-ttu-id="d6e0e-104">In questa sezione viene descritta una configurazione di esempio e il modo in cui i componenti principali si adattano insieme.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-104">This section describes a sample configuration and how the major components fit together.</span></span>

<span data-ttu-id="d6e0e-105">Nella figura seguente viene illustrata la relazione tra i vari componenti di un router.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-105">The following illustration shows the relationship between the various components of a router.</span></span>

![relazione tra i componenti del router Windows 2000](images/mrarch1.png)

<span data-ttu-id="d6e0e-107">Il gestore del gruppo multicast fa parte del servizio RRAS eseguito in un server che funziona come router.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-107">The multicast group manager is a part of the RRAS service that runs on a server that is operating as a router.</span></span>

<span data-ttu-id="d6e0e-108">Il router visualizzato presenta tre protocolli di routing multicast (protocollo 1, protocollo 2, protocollo 3) in esecuzione su di esso.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-108">The router shown has three multicast routing protocols (Protocol 1, Protocol 2, Protocol 3) running on it.</span></span> <span data-ttu-id="d6e0e-109">Ogni protocollo può essere proprietario di una o più interfacce (in questa illustrazione, il protocollo 1 è proprietario dell'interfaccia 1, il protocollo 2 possiede l'interfaccia 2 e il protocollo 3 è proprietario dell'interfaccia 3).</span><span class="sxs-lookup"><span data-stu-id="d6e0e-109">Each protocol can own one or more interfaces (in this illustration, Protocol 1 owns Interface 1, Protocol 2 owns Interface 2, and Protocol 3 owns Interface 3).</span></span> <span data-ttu-id="d6e0e-110">Ogni interfaccia può essere di proprietà di un solo protocollo di routing (oltre a IGMP, che è un caso speciale).</span><span class="sxs-lookup"><span data-stu-id="d6e0e-110">Each interface can be owned by only one routing protocol (in addition to IGMP, which is a special case).</span></span>

<span data-ttu-id="d6e0e-111">Il gestore del gruppo multicast viene eseguito sul router e coordina la distribuzione delle informazioni sul gruppo tra i protocolli di routing.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-111">The multicast group manager runs on the router and coordinates the distribution of group information between the routing protocols.</span></span>

<span data-ttu-id="d6e0e-112">Nella figura seguente viene illustrata la relazione tra due router in un'architettura multicast.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-112">The following illustration shows the relationship between two routers in a multicast architecture.</span></span>

![relazione tra due router nell'architettura multicast](images/mrarch2.png)

<span data-ttu-id="d6e0e-114">Nella figura precedente, il router 2 Invia un messaggio multicast alla rete 2 sull'interfaccia 3.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-114">In the previous illustration, Router 2 sends a multicast message to Network 2 on Interface 3.</span></span> <span data-ttu-id="d6e0e-115">Il router 1 riceve il messaggio multicast dalla rete 2 sull'interfaccia 3.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-115">Router 1 receives the multicast message from Network 2 on Interface 3.</span></span> <span data-ttu-id="d6e0e-116">In entrambi i router il protocollo 3 è proprietario della rispettiva interfaccia 3.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-116">On both routers, Protocol 3 owns the respective Interface 3.</span></span>

<span data-ttu-id="d6e0e-117">Nella figura seguente viene illustrato il percorso di un messaggio da un'origine multicast (a un gruppo multicast) per raggiungere l'host che è stato aggiunto al gruppo multicast.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-117">The following illustration shows the path a message from a multicast source (to a multicast group) takes to reach the host that has joined the multicast group.</span></span> <span data-ttu-id="d6e0e-118">I router nell'illustrazione usano la stessa configurazione delle illustrazioni precedenti. Tuttavia, i dettagli dell'interfaccia e del protocollo non vengono visualizzati per semplificare la figura.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-118">The routers in the illustration use the same configuration as previous illustrations; however, the interface and protocol details are not shown in order to keep the figure simple.</span></span>

![percorso del messaggio dall'origine multicast all'host di destinazione](images/mrarch3.png)

<span data-ttu-id="d6e0e-120">Nello scenario seguente vengono descritti gli eventi che si verificano quando un host viene aggiunto a un gruppo multicast.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-120">The following scenario describes the events that take place when a host joins a multicast group.</span></span> <span data-ttu-id="d6e0e-121">Vedere la figura precedente per le relazioni tra le diverse entità.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-121">Refer to the previous illustration for relationships between the various entities.</span></span>

1.  <span data-ttu-id="d6e0e-122">L'host 1 partecipa al gruppo multicast G sulla rete 3.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-122">Host 1 joins the multicast group G on Network 3.</span></span>
2.  <span data-ttu-id="d6e0e-123">Il router 3 apprende informazioni su G tramite IGMP.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-123">Router 3 learns about G via IGMP.</span></span>
3.  <span data-ttu-id="d6e0e-124">Il gestore del gruppo multicast sul router 3 informa il protocollo 3 sul router 3 che sono presenti nuovi ricevitori per G.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-124">The multicast group manager on Router 3 notifies Protocol 3 on Router 3 that there are new receivers for G.</span></span>
4.  <span data-ttu-id="d6e0e-125">Il protocollo 3 sul router 3 notifica quindi il protocollo 3 sul router 1 circa G.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-125">Protocol 3 on Router 3 then notifies Protocol 3 on Router 1 about G.</span></span>
5.  <span data-ttu-id="d6e0e-126">Il protocollo 3 sul router 1 informa a sua volta il gestore del gruppo multicast sul router 1 circa G.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-126">In turn, Protocol 3 on Router 1 notifies the multicast group manager on Router 1 about G.</span></span>
6.  <span data-ttu-id="d6e0e-127">Il gestore del gruppo multicast sul router 1 informa quindi il protocollo 1 e il protocollo 2 circa G.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-127">The multicast group manager on Router 1 then notifies Protocol 1 and Protocol 2 about G.</span></span>
7.  <span data-ttu-id="d6e0e-128">Il protocollo 2 potrebbe informare il router 2 circa G, se il protocollo è stato progettato per farlo.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-128">Protocol 2 may inform Router 2 about G, if the protocol is designed to do so.</span></span>

<span data-ttu-id="d6e0e-129">Nello scenario seguente vengono descritti gli eventi che si verificano quando un messaggio viene inviato a un gruppo multicast.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-129">The following scenario describes the events that take place when a message is sent to a multicast group.</span></span> <span data-ttu-id="d6e0e-130">Fare riferimento alla figura precedente per le relazioni tra le diverse entità.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-130">Refer to the previous illustration for the relationships between the various entities.</span></span>

1.  <span data-ttu-id="d6e0e-131">Un'origine sulla rete 1 Invia un messaggio al gruppo G.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-131">A source on Network 1 sends a message to Group G.</span></span>
2.  <span data-ttu-id="d6e0e-132">Il messaggio inviato dall'origine S passa prima al router 2, che lo inoltra al router 1 usando l'interfaccia 2 (poiché il router 2 è stato informato dal protocollo 2 che i destinatari sono presenti a valle).</span><span class="sxs-lookup"><span data-stu-id="d6e0e-132">The message sent from Source S goes first to Router 2, which then forwards it to Router 1 using Interface 2 (since Router 2 has been informed by Protocol 2 that receivers are present downstream).</span></span>
3.  <span data-ttu-id="d6e0e-133">Il router 1 trasmette il messaggio al router 3 (poiché il router 1 è stato informato dal protocollo 2 che i destinatari sono presenti a valle).</span><span class="sxs-lookup"><span data-stu-id="d6e0e-133">Router 1 forwards the message to Router 3 (since Router 1 has been informed by Protocol 2 that receivers are present downstream).</span></span>
4.  <span data-ttu-id="d6e0e-134">Il router 3 Invia il messaggio alla rete 3 e pertanto arriva all'host 1.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-134">Router 3 forwards the message to Network 3, and therefore it arrives at Host 1.</span></span>

<span data-ttu-id="d6e0e-135">Per ulteriori informazioni sull'interazione del protocollo di routing multicast, vedere [RFC 2715](routing-protocols-request-for-comments.md), regole di interoperabilità per i protocolli di routing multicast.</span><span class="sxs-lookup"><span data-stu-id="d6e0e-135">For further information on multicast routing protocol interaction, see [RFC 2715](routing-protocols-request-for-comments.md), Interoperability Rules for Multicast Routing Protocols.</span></span>

 

 




