---
title: Informazioni su Routing Table Manager versione 2
description: Nella documentazione seguente viene descritta la tecnologia Routing Table Manager versione 2 (RTMv2).
ms.assetid: 9f84863e-45ed-49d1-8df4-3b59b1b5f3c9
keywords:
- Servizio Routing e accesso remoto RRAS, gestione tabelle di routing versione 2
- Servizio Routing e accesso remoto RRAS, gestione tabelle di routing versione 2, descritto
- Gestione tabelle di routing versione 2 RRAS
- Gestione tabelle di routing versione 2 RRAS, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5014dc894c4a517bfdfac8478e520658a4987d4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044836"
---
# <a name="about-routing-table-manager-version-2"></a><span data-ttu-id="abdc2-107">Informazioni su Routing Table Manager versione 2</span><span class="sxs-lookup"><span data-stu-id="abdc2-107">About Routing Table Manager Version 2</span></span>

<span data-ttu-id="abdc2-108">Nella documentazione seguente viene descritta la tecnologia Routing Table Manager versione 2 (RTMv2).</span><span class="sxs-lookup"><span data-stu-id="abdc2-108">The following documentation describes the Routing Table Manager Version 2 (RTMv2) technology.</span></span> <span data-ttu-id="abdc2-109">L'API RTMv2 è una funzionalità di Windows 2000 e sistemi operativi successivi che è possibile usare per scrivere protocolli di routing che interagiscono con gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="abdc2-109">The RTMv2 API is a feature of Windows 2000 and later operating systems that you can use to write routing protocols that interact with the routing table manager.</span></span>

<span data-ttu-id="abdc2-110">Gestione tabelle di routing è il repository centrale di informazioni di routing per tutti i protocolli di routing che operano nel servizio Routing e accesso remoto (RRAS).</span><span class="sxs-lookup"><span data-stu-id="abdc2-110">The routing table manager is the central repository of routing information for all routing protocols that operate under the Routing and Remote Access Service (RRAS).</span></span>

<span data-ttu-id="abdc2-111">RTMv2 non è disponibile per Windows NT versione 4,0.</span><span class="sxs-lookup"><span data-stu-id="abdc2-111">RTMv2 is not available for Windows NT version 4.0.</span></span> <span data-ttu-id="abdc2-112">Non è inoltre possibile utilizzare RTMv2 per i protocolli di routing IPX eseguiti in Windows NT 4,0 o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="abdc2-112">Additionally, RTMv2 cannot be used for IPX routing protocols that run on Windows NT 4.0 or Windows 2000.</span></span> <span data-ttu-id="abdc2-113">Se si utilizza IPX o si scrivono protocolli di routing per Windows NT 4,0, consultare [informazioni su Routing Table Manager versione 1](about-routing-table-manager-version-1.md).</span><span class="sxs-lookup"><span data-stu-id="abdc2-113">If you are using IPX or writing routing protocols for Windows NT 4.0, please refer to [About Routing Table Manager Version 1](about-routing-table-manager-version-1.md).</span></span>

<span data-ttu-id="abdc2-114">In questa panoramica vengono descritti gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="abdc2-114">This overview describes the following topics:</span></span>

-   [<span data-ttu-id="abdc2-115">Componenti dell'architettura di gestione tabelle di routing</span><span class="sxs-lookup"><span data-stu-id="abdc2-115">Components of the Routing Table Manager Architecture</span></span>](components-of-the-routing-table-manager-architecture.md)
-   [<span data-ttu-id="abdc2-116">Registrazione con gestione tabelle di routing</span><span class="sxs-lookup"><span data-stu-id="abdc2-116">Registering with the Routing Table Manager</span></span>](registering-with-the-routing-table-manager.md)
-   [<span data-ttu-id="abdc2-117">Enumerazione delle entità registrate</span><span class="sxs-lookup"><span data-stu-id="abdc2-117">Enumerating Registered Entities</span></span>](enumerating-registered-entities.md)
-   [<span data-ttu-id="abdc2-118">Metodi using</span><span class="sxs-lookup"><span data-stu-id="abdc2-118">Using Methods</span></span>](using-methods.md)
-   [<span data-ttu-id="abdc2-119">Utilizzo di puntatori opachi</span><span class="sxs-lookup"><span data-stu-id="abdc2-119">Using Opaque Pointers</span></span>](using-opaque-pointers.md)
-   [<span data-ttu-id="abdc2-120">Contrassegno delle route per lo stato Hold-Down</span><span class="sxs-lookup"><span data-stu-id="abdc2-120">Marking Routes for the Hold-Down State</span></span>](marking-routes-for-the-hold-down-state.md)
-   [<span data-ttu-id="abdc2-121">Aggiunta di route</span><span class="sxs-lookup"><span data-stu-id="abdc2-121">Adding Routes</span></span>](adding-routes.md)
-   [<span data-ttu-id="abdc2-122">Recupero delle informazioni sulla Route</span><span class="sxs-lookup"><span data-stu-id="abdc2-122">Retrieving Route Information</span></span>](retrieving-route-information.md)
-   [<span data-ttu-id="abdc2-123">Aggiornamento di route</span><span class="sxs-lookup"><span data-stu-id="abdc2-123">Updating Routes</span></span>](updating-routes.md)
-   [<span data-ttu-id="abdc2-124">Ricezione di notifiche di modifiche</span><span class="sxs-lookup"><span data-stu-id="abdc2-124">Receiving Notification of Changes</span></span>](receiving-notification-of-changes.md)
-   [<span data-ttu-id="abdc2-125">Utilizzo degli hop successivi</span><span class="sxs-lookup"><span data-stu-id="abdc2-125">Working with Next Hops</span></span>](working-with-next-hops.md)
-   [<span data-ttu-id="abdc2-126">Enumerazione delle voci della tabella di routing</span><span class="sxs-lookup"><span data-stu-id="abdc2-126">Enumerating Routing Table Entries</span></span>](enumerating-routing-table-entries.md)
-   [<span data-ttu-id="abdc2-127">Ricerca di informazioni specifiche nella tabella di routing</span><span class="sxs-lookup"><span data-stu-id="abdc2-127">Finding Specific Information in the Routing Table</span></span>](finding-specific-information-in-the-routing-table.md)
-   [<span data-ttu-id="abdc2-128">Gestione degli elenchi di Client-Specific</span><span class="sxs-lookup"><span data-stu-id="abdc2-128">Maintaining Client-Specific Lists</span></span>](maintaining-client-specific-lists.md)
-   [<span data-ttu-id="abdc2-129">Gestione degli handle</span><span class="sxs-lookup"><span data-stu-id="abdc2-129">Managing Handles</span></span>](managing-handles.md)

 

 




