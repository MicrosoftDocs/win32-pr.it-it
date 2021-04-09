---
title: Utilizzo di gestione tabelle di routing versione 2
description: Prima di iniziare a sviluppare client che usano le API RTMv2, esaminare i problemi di programmazione di RTMv2.
ms.assetid: c0187b65-3cb2-4ab0-8d5f-ca37e8bc0ad7
keywords:
- Servizio Routing e accesso remoto RRAS, gestione tabelle di routing versione 2, attività
- Gestione tabelle di routing versione 2 RRAS, attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29bc7acab213325a0683de215995eeb2f635b102
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955574"
---
# <a name="using-routing-table-manager-version-2"></a><span data-ttu-id="6b342-105">Utilizzo di gestione tabelle di routing versione 2</span><span class="sxs-lookup"><span data-stu-id="6b342-105">Using Routing Table Manager Version 2</span></span>

<span data-ttu-id="6b342-106">Prima di iniziare a sviluppare client che usano le API RTMv2, esaminare i [problemi di programmazione di RTMv2](rtmv2-programming-issues.md).</span><span class="sxs-lookup"><span data-stu-id="6b342-106">Before you begin developing clients that use the RTMv2 APIs, review the [RTMv2 Programming Issues](rtmv2-programming-issues.md).</span></span>

<span data-ttu-id="6b342-107">Questa sezione contiene codice di esempio che può essere usato quando si sviluppano client quali i protocolli di routing.</span><span class="sxs-lookup"><span data-stu-id="6b342-107">This section contains sample code that can be used when developing clients such as routing protocols.</span></span>

-   [<span data-ttu-id="6b342-108">Problemi di programmazione di RTMv2</span><span class="sxs-lookup"><span data-stu-id="6b342-108">RTMv2 Programming Issues</span></span>](rtmv2-programming-issues.md)
-   [<span data-ttu-id="6b342-109">Eseguire la registrazione con gestione tabelle di routing</span><span class="sxs-lookup"><span data-stu-id="6b342-109">Register with the Routing Table Manager</span></span>](register-with-the-routing-table-manager.md)
-   [<span data-ttu-id="6b342-110">Enumerare le entità registrate</span><span class="sxs-lookup"><span data-stu-id="6b342-110">Enumerate the Registered Entities</span></span>](enumerate-the-registered-entities.md)
-   [<span data-ttu-id="6b342-111">Ottenere e chiamare i metodi esportati per un client</span><span class="sxs-lookup"><span data-stu-id="6b342-111">Obtain and Call the Exported Methods for a Client</span></span>](obtain-and-call-the-exported-methods-for-a-client.md)
-   [<span data-ttu-id="6b342-112">Registra per notifica modifiche</span><span class="sxs-lookup"><span data-stu-id="6b342-112">Register for Change Notification</span></span>](register-for-change-notification.md)
-   [<span data-ttu-id="6b342-113">Aggiungere e aggiornare le route con RtmAddRouteToDest</span><span class="sxs-lookup"><span data-stu-id="6b342-113">Add and Update Routes Using RtmAddRouteToDest</span></span>](add-and-update-routes-using-rtmaddroutetodest.md)
-   [<span data-ttu-id="6b342-114">Aggiornare una route sul posto usando RtmUpdateAndUnlockRoute</span><span class="sxs-lookup"><span data-stu-id="6b342-114">Update a Route In Place Using RtmUpdateAndUnlockRoute</span></span>](update-a-route-in-place-using-rtmupdateandunlockroute.md)
-   [<span data-ttu-id="6b342-115">USA lo stato di Hold-Down Route</span><span class="sxs-lookup"><span data-stu-id="6b342-115">Use the Route Hold-Down State</span></span>](use-the-route-hold-down-state.md)
-   [<span data-ttu-id="6b342-116">Enumera tutte le destinazioni</span><span class="sxs-lookup"><span data-stu-id="6b342-116">Enumerate All Destinations</span></span>](enumerate-all-destinations.md)
-   [<span data-ttu-id="6b342-117">Enumera tutte le route</span><span class="sxs-lookup"><span data-stu-id="6b342-117">Enumerate All Routes</span></span>](enumerate-all-routes.md)
-   [<span data-ttu-id="6b342-118">Cerca la route migliore</span><span class="sxs-lookup"><span data-stu-id="6b342-118">Search for the Best Route</span></span>](search-for-the-best-route.md)
-   [<span data-ttu-id="6b342-119">Cercare le route usando un albero di prefisso</span><span class="sxs-lookup"><span data-stu-id="6b342-119">Search for Routes Using a Prefix Tree</span></span>](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md)
-   [<span data-ttu-id="6b342-120">Accedere al puntatore opaco in una destinazione</span><span class="sxs-lookup"><span data-stu-id="6b342-120">Access the Opaque Pointer in a Destination</span></span>](access-the-opaque-pointer-in-a-destination.md)
-   [<span data-ttu-id="6b342-121">Usare un elenco di route Client-Specific</span><span class="sxs-lookup"><span data-stu-id="6b342-121">Use a Client-Specific Route List</span></span>](use-a-client-specific-route-list.md)
-   [<span data-ttu-id="6b342-122">USA callback di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="6b342-122">Use the Event Notification Callback</span></span>](use-the-event-notification-callback.md)

 

 




