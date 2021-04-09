---
title: Route statiche e autostatiche
description: In genere, le route alle reti remote vengono ottenute in modo dinamico tramite protocolli di routing.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3faa8931e0fee5c75f598b920b7b97a1e0e829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955751"
---
# <a name="static-and-autostatic-routes"></a><span data-ttu-id="5a9ee-103">Route statiche e autostatiche</span><span class="sxs-lookup"><span data-stu-id="5a9ee-103">Static and Autostatic Routes</span></span>

<span data-ttu-id="5a9ee-104">In genere, le route alle reti remote vengono ottenute in modo dinamico tramite protocolli di routing.</span><span class="sxs-lookup"><span data-stu-id="5a9ee-104">Typically, routes to remote networks are obtained dynamically through routing protocols.</span></span> <span data-ttu-id="5a9ee-105">Tuttavia, l'amministratore può anche eseguire il *seeding* della tabella di routing fornendo le route manualmente.</span><span class="sxs-lookup"><span data-stu-id="5a9ee-105">However, the administrator can also *seed* the routing table by providing routes manually.</span></span> <span data-ttu-id="5a9ee-106">Queste route sono denominate *static*.</span><span class="sxs-lookup"><span data-stu-id="5a9ee-106">These routes are referred to as *static*.</span></span> <span data-ttu-id="5a9ee-107">Una route statica è associata a un'interfaccia che rappresenta la rete remota.</span><span class="sxs-lookup"><span data-stu-id="5a9ee-107">A static route is associated with an interface that represents the remote network.</span></span> <span data-ttu-id="5a9ee-108">Diversamente dalle route dinamiche, le route statiche vengono mantenute anche se il router viene riavviato o l'interfaccia è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5a9ee-108">Unlike dynamic routes, static routes are retained even if the router is restarted or the interface is disabled.</span></span>

<span data-ttu-id="5a9ee-109">Una route *autostatic* viene ottenuta tramite un protocollo di routing, ma una volta ottenuta si comporta come una route statica.</span><span class="sxs-lookup"><span data-stu-id="5a9ee-109">An *autostatic* route is obtained through a routing protocol, but once obtained behaves like a static route.</span></span> <span data-ttu-id="5a9ee-110">Il processo per ottenere le route autostatiche è il seguente: la gestione router IP o IPX invia una richiesta di aggiornamento delle informazioni di routing per un'interfaccia specifica da parte di un protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="5a9ee-110">The process for obtaining autostatic routes is as follows: The IP or IPX router manager issues a request that a routing protocol update the routing information for a specific interface.</span></span> <span data-ttu-id="5a9ee-111">I risultati dell'aggiornamento vengono quindi convertiti in route statiche.</span><span class="sxs-lookup"><span data-stu-id="5a9ee-111">The results of the update are then converted into static routes.</span></span> <span data-ttu-id="5a9ee-112">Si noti che solo alcuni protocolli di routing supportano le richieste di aggiornamenti della route autostatic.</span><span class="sxs-lookup"><span data-stu-id="5a9ee-112">Note that only certain routing protocols support requests for autostatic route updates.</span></span>

 

 




