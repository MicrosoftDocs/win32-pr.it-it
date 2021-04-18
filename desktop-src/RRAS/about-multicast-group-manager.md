---
title: Informazioni su Gestione gruppi multicast
description: Questa documentazione descrive la tecnologia di gestione dei gruppi multicast (MGM).
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- Gestione gruppo multicast RRAS
- Gestore del gruppo multicast RRAS, descritto
- Servizio Routing e accesso remoto RRAS, gestione gruppo multicast
- Servizio Routing e accesso remoto RRAS, gestione gruppo multicast, descritto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 034d37b99aaa9ca0139b5425cd5b85e7b3f280e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298294"
---
# <a name="about-multicast-group-manager"></a><span data-ttu-id="15742-107">Informazioni su Gestione gruppi multicast</span><span class="sxs-lookup"><span data-stu-id="15742-107">About Multicast Group Manager</span></span>

<span data-ttu-id="15742-108">Questa documentazione descrive la tecnologia di gestione dei gruppi multicast (MGM).</span><span class="sxs-lookup"><span data-stu-id="15742-108">This documentation describes the Multicast Group Manager (MGM) technology.</span></span>

<span data-ttu-id="15742-109">Il multicast consente a un host di inviare dati solo alle destinazioni che richiedono la ricezione dei dati in modo specifico.</span><span class="sxs-lookup"><span data-stu-id="15742-109">Multicasting allows a host to send data to only those destinations that specifically request to receive the data.</span></span> <span data-ttu-id="15742-110">In questo modo, il multicasting è diverso dall'invio di dati broadcast, dal momento che i dati di trasmissione vengono inviati a tutti gli host.</span><span class="sxs-lookup"><span data-stu-id="15742-110">In this way, multicasting differs from sending broadcast data, since broadcast data is sent to all hosts.</span></span>

<span data-ttu-id="15742-111">Il multicast consente di risparmiare larghezza di banda poiché i dati multicast vengono ricevuti solo da tali host che richiedono i dati e i dati vengono trasmessi su qualsiasi collegamento una sola volta.</span><span class="sxs-lookup"><span data-stu-id="15742-111">Multicasting saves network bandwidth because multicast data is only received by those hosts that request the data, and the data travels over any link only once.</span></span> <span data-ttu-id="15742-112">Il multicast consente di risparmiare larghezza di banda del server poiché un server deve inviare un solo messaggio multicast per rete anziché un messaggio unicast per ricevitore.</span><span class="sxs-lookup"><span data-stu-id="15742-112">Multicasting saves server bandwidth because a server has to send only one multicast message per network instead of one unicast message per receiver.</span></span> <span data-ttu-id="15742-113">Esempi di applicazioni multicast più diffuse sono incontri online e Internet radio.</span><span class="sxs-lookup"><span data-stu-id="15742-113">Examples of popular multicast applications are online meetings and Internet radio.</span></span>

<span data-ttu-id="15742-114">L'API MGM consente agli sviluppatori di scrivere protocolli di routing multicast che interagiscono con i router che eseguono il gestore del gruppo multicast.</span><span class="sxs-lookup"><span data-stu-id="15742-114">The MGM API enables developers to write multicast routing protocols that interoperate with routers running the multicast group manager.</span></span>

<span data-ttu-id="15742-115">Quando in un router è abilitato più di un protocollo di routing multicast, il gestore del gruppo multicast coordina le operazioni tra tutti i protocolli di routing.</span><span class="sxs-lookup"><span data-stu-id="15742-115">When more than one multicast routing protocol is enabled on a router, the multicast group manager coordinates operations between all routing protocols.</span></span> <span data-ttu-id="15742-116">Il gestore del gruppo multicast informa ogni protocollo di routing quando si verificano modifiche all'appartenenza al gruppo e quando vengono ricevuti i dati multicast da una nuova origine o destinata a un nuovo gruppo.</span><span class="sxs-lookup"><span data-stu-id="15742-116">The multicast group manager informs each routing protocol when group membership changes occur, and when multicast data from a new source or destined to a new group is received.</span></span>

<span data-ttu-id="15742-117">L'API MGM offre le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="15742-117">The MGM API provides the following features:</span></span>

-   <span data-ttu-id="15742-118">Registrazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="15742-118">Protocol registration</span></span>
-   <span data-ttu-id="15742-119">Gestione di gruppi</span><span class="sxs-lookup"><span data-stu-id="15742-119">Group management</span></span>
-   <span data-ttu-id="15742-120">Enumerazione MFE (multicast inoltring entry)</span><span class="sxs-lookup"><span data-stu-id="15742-120">Multicast forwarding entry (MFE) enumeration</span></span>
-   <span data-ttu-id="15742-121">Definizioni di callback per i protocolli di routing multicast</span><span class="sxs-lookup"><span data-stu-id="15742-121">Callback definitions for multicast routing protocols</span></span>

<span data-ttu-id="15742-122">Questa panoramica descrive i componenti dell'architettura multicast, gli scenari client usati per interagire con gestione gruppi multicast e le considerazioni sulla programmazione per l'uso dell'API MGM.</span><span class="sxs-lookup"><span data-stu-id="15742-122">This overview describes the components of the multicast architecture, the client scenarios that are used to interoperate with the multicast group manager, and programming considerations for using the MGM API.</span></span>

 

 




