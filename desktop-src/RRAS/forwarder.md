---
title: Server d'inoltro
description: Il server d'trasmissione è il componente in modalità kernel del router responsabile dell'invio dei dati da un'interfaccia del router alle altre.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52885000a9f1fcc117cd1fefc207531b9b524e74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044762"
---
# <a name="forwarder"></a><span data-ttu-id="3775c-103">Server d'inoltro</span><span class="sxs-lookup"><span data-stu-id="3775c-103">Forwarder</span></span>

<span data-ttu-id="3775c-104">Il server d'trasmissione è il componente in modalità kernel del router responsabile dell'invio dei dati da un'interfaccia del router alle altre.</span><span class="sxs-lookup"><span data-stu-id="3775c-104">The forwarder is the kernel-mode component of the router that is responsible for forwarding data from one router interface to the others.</span></span> <span data-ttu-id="3775c-105">Il server d'inoltre decide inoltre se un pacchetto è destinato al recapito locale, se è destinato all'uscita da un'altra interfaccia o a entrambi.</span><span class="sxs-lookup"><span data-stu-id="3775c-105">The forwarder also decides whether a packet is destined for local delivery, whether it is destined to be forwarded out of another interface, or both.</span></span>

<span data-ttu-id="3775c-106">Sono disponibili due server d'avvio in modalità kernel: unicast e multicast.</span><span class="sxs-lookup"><span data-stu-id="3775c-106">There are two kernel-mode forwarders: unicast and multicast.</span></span>

<span data-ttu-id="3775c-107">Gestione router ottiene le route migliori per tutte le destinazioni da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="3775c-107">The router manager obtains the best routes to all destinations from the routing table manager.</span></span> <span data-ttu-id="3775c-108">Queste route vengono passate al server d'avvio unicast.</span><span class="sxs-lookup"><span data-stu-id="3775c-108">These routes are passed to the unicast forwarder.</span></span> <span data-ttu-id="3775c-109">Il server d'avvio unicast usa queste route per eseguire l'effettivo invio di dati unicast.</span><span class="sxs-lookup"><span data-stu-id="3775c-109">The unicast forwarder uses these routes to perform the actual forwarding of unicast data.</span></span> <span data-ttu-id="3775c-110">In questo modo, il server d'inoltro unicast gestisce una cache delle route migliori nella visualizzazione unicast della tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="3775c-110">In this manner, the unicast forwarder maintains a cache of the best routes in the unicast view of the routing table.</span></span>

<span data-ttu-id="3775c-111">Il gestore del gruppo multicast utilizza le informazioni della visualizzazione multicast della tabella di routing per aggiungere le voci di inoltro multicast al server di inoltro multicast.</span><span class="sxs-lookup"><span data-stu-id="3775c-111">The multicast group manager uses information from the multicast view of the routing table to add multicast forwarding entries to the multicast forwarder.</span></span>

 

 




