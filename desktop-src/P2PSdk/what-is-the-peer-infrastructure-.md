---
description: L'infrastruttura peer è un set di diverse API potenti e flessibili.
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: Che cos'è l'infrastruttura peer?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873717b3f90497fe9ab9f50bb9c18e6f0692a4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312209"
---
# <a name="what-is-the-peer-infrastructure"></a><span data-ttu-id="da1d9-103">Che cos'è l'infrastruttura peer?</span><span class="sxs-lookup"><span data-stu-id="da1d9-103">What is the Peer Infrastructure?</span></span>

<span data-ttu-id="da1d9-104">L'infrastruttura peer è un set di diverse API potenti e flessibili.</span><span class="sxs-lookup"><span data-stu-id="da1d9-104">The Peer Infrastructure is a set of several APIs that are powerful and flexible.</span></span> <span data-ttu-id="da1d9-105">I componenti principali includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="da1d9-105">The major components include the following:</span></span>

-   [<span data-ttu-id="da1d9-106">API di Peer Graphing</span><span class="sxs-lookup"><span data-stu-id="da1d9-106">Peer Graphing API</span></span>](#peer-graphing-api)
-   [<span data-ttu-id="da1d9-107">API di raggruppamento peer</span><span class="sxs-lookup"><span data-stu-id="da1d9-107">Peer Grouping API</span></span>](#peer-grouping-api)
-   [<span data-ttu-id="da1d9-108">API peer Identity Manager</span><span class="sxs-lookup"><span data-stu-id="da1d9-108">Peer Identity Manager API</span></span>](#peer-identity-manager-api)
-   [<span data-ttu-id="da1d9-109">API provider dello spazio dei nomi PNRP</span><span class="sxs-lookup"><span data-stu-id="da1d9-109">PNRP Namespace Provider API</span></span>](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a><span data-ttu-id="da1d9-110">API di Peer Graphing</span><span class="sxs-lookup"><span data-stu-id="da1d9-110">Peer Graphing API</span></span>

<span data-ttu-id="da1d9-111">L'infrastruttura peer offre una tecnologia di grafica che consente di passare le informazioni in modo efficiente e affidabile tra i peer in un grafo peer.</span><span class="sxs-lookup"><span data-stu-id="da1d9-111">The Peer Infrastructure provides a graphing technology that can pass information efficiently and reliably between peers in a peer graph.</span></span> <span data-ttu-id="da1d9-112">L' [API per la rappresentazione grafica dei peer](graphing-api.md) garantisce che ogni nodo disponga di una visualizzazione coerente dei dati in un grafico.</span><span class="sxs-lookup"><span data-stu-id="da1d9-112">The [Peer Graphing API](graphing-api.md) ensures that each node has a consistent view of the data in a graph.</span></span>

<span data-ttu-id="da1d9-113">È possibile usare l' [API di Peer Graphing](graphing-api.md) per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="da1d9-113">You can use the [Peer Graphing API](graphing-api.md) to do the following:</span></span>

-   <span data-ttu-id="da1d9-114">Creare e gestire grafici peer</span><span class="sxs-lookup"><span data-stu-id="da1d9-114">Create and manage peer graphs</span></span>
-   <span data-ttu-id="da1d9-115">Enumerare e interagire con altri peer in un grafico peer</span><span class="sxs-lookup"><span data-stu-id="da1d9-115">Enumerate and interact with other peers in a peer graph</span></span>
-   <span data-ttu-id="da1d9-116">Inviare dati sotto forma di [record](records.md) a ogni nodo in un grafico peer</span><span class="sxs-lookup"><span data-stu-id="da1d9-116">Send data in the form of a [record](records.md) to each node in a peer graph</span></span>

## <a name="peer-grouping-api"></a><span data-ttu-id="da1d9-117">API di raggruppamento peer</span><span class="sxs-lookup"><span data-stu-id="da1d9-117">Peer Grouping API</span></span>

<span data-ttu-id="da1d9-118">L' [API di raggruppamento peer](grouping-api.md) combina e migliora le API peer [PNRP](#pnrp-namespace-provider-api) e [Graphing](#peer-graphing-api) e aggiunge i due componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="da1d9-118">The [Peer Grouping API](grouping-api.md) combines and enhances the Peer [PNRP](#pnrp-namespace-provider-api) and [Graphing](#peer-graphing-api) APIs, and adds the following two components:</span></span>

-   <span data-ttu-id="da1d9-119">Livello di multiplexing che consente a più applicazioni in esecuzione su un'entità peer di connettersi a un gruppo</span><span class="sxs-lookup"><span data-stu-id="da1d9-119">A multiplexing layer that allows multiple applications running on one peer entity to connect to a group</span></span>
-   <span data-ttu-id="da1d9-120">Un modello di sicurezza specifico che garantisce che solo i peer invitati a un gruppo possano connettersi al gruppo attraverso la durata del gruppo</span><span class="sxs-lookup"><span data-stu-id="da1d9-120">A specific security model that ensures only peers invited to a group can connect to the group through the lifetime of the group</span></span>

<span data-ttu-id="da1d9-121">È possibile utilizzare l'API di raggruppamento peer per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="da1d9-121">You can use the Peer Grouping API to do the following:</span></span>

-   <span data-ttu-id="da1d9-122">Creare e gestire gruppi di peer sicuri</span><span class="sxs-lookup"><span data-stu-id="da1d9-122">Create and manage secure peer groups</span></span>
-   <span data-ttu-id="da1d9-123">Enumerare e interagire con altri peer in un gruppo</span><span class="sxs-lookup"><span data-stu-id="da1d9-123">Enumerate and interact with other peers in a group</span></span>
-   <span data-ttu-id="da1d9-124">Inviare dati sotto forma di [record](records.md) a ogni nodo in un gruppo peer</span><span class="sxs-lookup"><span data-stu-id="da1d9-124">Send data in the form of a [record](records.md) to each node in a peer group</span></span>

## <a name="peer-identity-manager-api"></a><span data-ttu-id="da1d9-125">API peer Identity Manager</span><span class="sxs-lookup"><span data-stu-id="da1d9-125">Peer Identity Manager API</span></span>

<span data-ttu-id="da1d9-126">Usando l' [API peer Identity Manager](identity-manager-api.md) è possibile creare nomi di [peer](peer-names.md) sicuri che PNRP può usare per garantire che un utente che pubblica un nome sia ufficialmente proprietario del nome.</span><span class="sxs-lookup"><span data-stu-id="da1d9-126">By using the [Peer Identity Manager API](identity-manager-api.md) you can create secure [peer names](peer-names.md) that PNRP can use to ensure that a person publishing a name officially owns the name.</span></span> <span data-ttu-id="da1d9-127">I nomi di peer sono anche denominati identità e vengono usati nell'API di raggruppamento peer per identificare gli utenti di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="da1d9-127">Peer names are also called identities, and they are used in the Peer Grouping API to identify the individuals in a group.</span></span>

<span data-ttu-id="da1d9-128">È possibile usare l' [API peer Identity Manager](identity-manager-api.md) per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="da1d9-128">You can use the [Peer Identity Manager API](identity-manager-api.md) to do the following:</span></span>

-   <span data-ttu-id="da1d9-129">Creazione, enumerazione e gestione delle identità peer.</span><span class="sxs-lookup"><span data-stu-id="da1d9-129">Create, enumerate, and manage peer identities.</span></span>

## <a name="pnrp-namespace-provider-api"></a><span data-ttu-id="da1d9-130">API provider dello spazio dei nomi PNRP</span><span class="sxs-lookup"><span data-stu-id="da1d9-130">PNRP Namespace Provider API</span></span>

<span data-ttu-id="da1d9-131">L'infrastruttura peer fornisce una tecnologia di risoluzione dei nomi senza server denominata [API del provider dello spazio dei nomi PNRP](pnrp-namespace-provider-api.md).</span><span class="sxs-lookup"><span data-stu-id="da1d9-131">The Peer Infrastructure provides a serverless name resolution technology called the [PNRP Namespace Provider API](pnrp-namespace-provider-api.md).</span></span> <span data-ttu-id="da1d9-132">Utilizzando l'API del provider dello spazio dei nomi PNRP 2 PNRP, un endpoint di peer, servizio, calcolo e gruppo peer può gestire, registrare, annullare la registrazione e risolvere un altro endpoint in un [cloud](clouds.md)PNRP.</span><span class="sxs-lookup"><span data-stu-id="da1d9-132">By using the Winsock 2 PNRP Namespace Provider API, a peer, service, computing device, and peer group endpoint can manage, register, unregister, and resolve another endpoint in a PNRP [cloud](clouds.md).</span></span>

> [!Note]  
> <span data-ttu-id="da1d9-133">PNRP è un acronimo del **protocollo di risoluzione dei nomi peer**.</span><span class="sxs-lookup"><span data-stu-id="da1d9-133">PNRP is an acronym for **peer name resolution protocol**.</span></span>

 

 

 



