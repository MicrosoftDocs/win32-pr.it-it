---
title: Applicazioni di esempio (infrastruttura peer)
description: Le seguenti applicazioni di esempio sono incluse in Windows XP Peer SDK.
ms.assetid: 26c45360-f232-4e29-90b5-44ccacb5a9c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c15e2bf3162151a4cbf18547fdfe482c7ea77fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967532"
---
# <a name="sample-applications-peer-infrastructure"></a><span data-ttu-id="032e4-103">Applicazioni di esempio (infrastruttura peer)</span><span class="sxs-lookup"><span data-stu-id="032e4-103">Sample applications (Peer Infrastructure)</span></span>

<span data-ttu-id="032e4-104">Le seguenti applicazioni di esempio sono incluse in Windows XP Peer SDK.</span><span class="sxs-lookup"><span data-stu-id="032e4-104">The following sample applications are included in the Windows XP Peer SDK.</span></span> <span data-ttu-id="032e4-105">Gli esempi possono essere utili quando si sviluppano applicazioni peer personalizzate mediante l'infrastruttura peer.</span><span class="sxs-lookup"><span data-stu-id="032e4-105">The samples can help you when you develop your own peer applications using the Peer Infrastructure.</span></span>

-   [<span data-ttu-id="032e4-106">Chat Graph</span><span class="sxs-lookup"><span data-stu-id="032e4-106">Graph Chat</span></span>](#graph-chat)
-   [<span data-ttu-id="032e4-107">Chat di gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-107">Group Chat</span></span>](#group-chat)
-   [<span data-ttu-id="032e4-108">Browser del gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-108">Group Browser</span></span>](#group-browser)

## <a name="graph-chat"></a><span data-ttu-id="032e4-109">Chat Graph</span><span class="sxs-lookup"><span data-stu-id="032e4-109">Graph Chat</span></span>

<span data-ttu-id="032e4-110">L'applicazione di esempio Graph chat è una semplice applicazione di chat che illustra come usare le API per la rappresentazione grafica dei peer e il provider dello spazio dei nomi PNRP (Peer Name Resolution Protocol) con l'API Winsock 2.</span><span class="sxs-lookup"><span data-stu-id="032e4-110">The Graph Chat sample application is a simple chat application that demonstrates how to use the Peer Graphing APIs and the Peer Name Resolution Protocol (PNRP) Namespace Provider with the Winsock 2 API.</span></span> <span data-ttu-id="032e4-111">L'applicazione illustra le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="032e4-111">The application demonstrates the following tasks:</span></span>

-   <span data-ttu-id="032e4-112">Creazione di un grafico</span><span class="sxs-lookup"><span data-stu-id="032e4-112">Creating a graph</span></span>
-   <span data-ttu-id="032e4-113">Connessione a un grafo esistente</span><span class="sxs-lookup"><span data-stu-id="032e4-113">Connecting to an existing graph</span></span>
-   <span data-ttu-id="032e4-114">Disconnessione da un grafo esistente</span><span class="sxs-lookup"><span data-stu-id="032e4-114">Disconnecting from an existing graph</span></span>
-   <span data-ttu-id="032e4-115">Enumerazione di entità peer</span><span class="sxs-lookup"><span data-stu-id="032e4-115">Enumerating peer entities</span></span>
-   <span data-ttu-id="032e4-116">Aggiunta di record al grafo</span><span class="sxs-lookup"><span data-stu-id="032e4-116">Adding records to the graph</span></span>
-   <span data-ttu-id="032e4-117">Utilizzo di connessioni dirette con un grafo</span><span class="sxs-lookup"><span data-stu-id="032e4-117">Using direct connections with a graph</span></span>
-   <span data-ttu-id="032e4-118">Uso dell'infrastruttura di notifiche ed eventi con i grafici</span><span class="sxs-lookup"><span data-stu-id="032e4-118">Using the notification and event infrastructure with graphs</span></span>
-   <span data-ttu-id="032e4-119">Registrazione dei nomi con PNRP</span><span class="sxs-lookup"><span data-stu-id="032e4-119">Registering names with PNRP</span></span>
-   <span data-ttu-id="032e4-120">Risoluzione dei nomi con PNRP</span><span class="sxs-lookup"><span data-stu-id="032e4-120">Resolving names with PNRP</span></span>
-   <span data-ttu-id="032e4-121">Annullamento della registrazione dei nomi con PNRP</span><span class="sxs-lookup"><span data-stu-id="032e4-121">Unregistering names with PNRP</span></span>

## <a name="group-chat"></a><span data-ttu-id="032e4-122">Chat di gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-122">Group Chat</span></span>

<span data-ttu-id="032e4-123">L'applicazione di esempio Group Chat è una semplice applicazione di chat che illustra come utilizzare le API di raggruppamento peer e gestione identità.</span><span class="sxs-lookup"><span data-stu-id="032e4-123">The Group Chat sample application is a simple chat application that demonstrates how to use the Peer Grouping and Identity Manager APIs.</span></span> <span data-ttu-id="032e4-124">L'applicazione illustra le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="032e4-124">The application demonstrates the following tasks:</span></span>

-   <span data-ttu-id="032e4-125">Creazione di un'identità</span><span class="sxs-lookup"><span data-stu-id="032e4-125">Creating an identity</span></span>
-   <span data-ttu-id="032e4-126">Creazione e recupero di informazioni sull'identità</span><span class="sxs-lookup"><span data-stu-id="032e4-126">Creating and obtaining identity information</span></span>
-   <span data-ttu-id="032e4-127">Enumerazione delle identità</span><span class="sxs-lookup"><span data-stu-id="032e4-127">Enumerating identities</span></span>
-   <span data-ttu-id="032e4-128">Enumerazione dei gruppi associati a un'identità</span><span class="sxs-lookup"><span data-stu-id="032e4-128">Enumerating groups associated with an identity</span></span>
-   <span data-ttu-id="032e4-129">Creazione di un gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-129">Creating a group</span></span>
-   <span data-ttu-id="032e4-130">Creazione di inviti per un gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-130">Creating invitations for a group</span></span>
-   <span data-ttu-id="032e4-131">Connessione a un gruppo esistente</span><span class="sxs-lookup"><span data-stu-id="032e4-131">Connecting to an existing group</span></span>
-   <span data-ttu-id="032e4-132">Disconnessione da un gruppo esistente</span><span class="sxs-lookup"><span data-stu-id="032e4-132">Disconnecting from an existing group</span></span>
-   <span data-ttu-id="032e4-133">Estrazione di informazioni dalle proprietà del gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-133">Extracting information from the group properties</span></span>
-   <span data-ttu-id="032e4-134">Utilizzo di connessioni dirette con un gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-134">Using direct connections with a group</span></span>
-   <span data-ttu-id="032e4-135">Uso delle funzioni di enumerazione in un gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-135">Using the enumeration functions within a group</span></span>
-   <span data-ttu-id="032e4-136">Enumerazione dei membri del gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-136">Enumerating group members</span></span>
-   <span data-ttu-id="032e4-137">Aggiunta di record a un gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-137">Adding records to a group</span></span>
-   <span data-ttu-id="032e4-138">Uso dell'infrastruttura di notifica ed evento con i gruppi</span><span class="sxs-lookup"><span data-stu-id="032e4-138">Using the notification and event infrastructure with groups</span></span>

## <a name="group-browser"></a><span data-ttu-id="032e4-139">Browser del gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-139">Group Browser</span></span>

<span data-ttu-id="032e4-140">L'applicazione di esempio del browser del gruppo è un semplice strumento di gestione dei gruppi di peer che illustra come utilizzare le API di raggruppamento peer e gestione identità.</span><span class="sxs-lookup"><span data-stu-id="032e4-140">The Group Browser sample application is a simple peer group management tool that demonstrates how to use the Peer Grouping and Identity Manager APIs.</span></span> <span data-ttu-id="032e4-141">L'applicazione illustra le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="032e4-141">The application demonstrates the following tasks:</span></span>

-   <span data-ttu-id="032e4-142">Enumerazione dei Cloud PNRP</span><span class="sxs-lookup"><span data-stu-id="032e4-142">Enumerating PNRP clouds</span></span>
-   <span data-ttu-id="032e4-143">Enumerazione delle identità</span><span class="sxs-lookup"><span data-stu-id="032e4-143">Enumerating identities</span></span>
-   <span data-ttu-id="032e4-144">Enumerazione dei gruppi associati a un'identità</span><span class="sxs-lookup"><span data-stu-id="032e4-144">Enumerating groups associated with an identity</span></span>
-   <span data-ttu-id="032e4-145">Creazione ed eliminazione di identità</span><span class="sxs-lookup"><span data-stu-id="032e4-145">Creating and deleting identities</span></span>
-   <span data-ttu-id="032e4-146">Creazione di un gruppo e relativa associazione a un'identità</span><span class="sxs-lookup"><span data-stu-id="032e4-146">Creating a group and associating it with an identity</span></span>
-   <span data-ttu-id="032e4-147">Creazione di un invito e salvataggio</span><span class="sxs-lookup"><span data-stu-id="032e4-147">Creating an invitation and saving it</span></span>
-   <span data-ttu-id="032e4-148">Apertura e utilizzo di un invito per l'aggiunta a un gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-148">Opening an invitation and using it to join a group</span></span>
-   <span data-ttu-id="032e4-149">Eliminazione di identità e appartenenza a un gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-149">Deleting an identity and group membership</span></span>
-   <span data-ttu-id="032e4-150">Connessione a un gruppo esistente</span><span class="sxs-lookup"><span data-stu-id="032e4-150">Connecting to an existing group</span></span>
-   <span data-ttu-id="032e4-151">Disconnessione da un gruppo esistente</span><span class="sxs-lookup"><span data-stu-id="032e4-151">Disconnecting from an existing group</span></span>
-   <span data-ttu-id="032e4-152">Estrazione di informazioni dalle proprietà del gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-152">Extracting information from group properties</span></span>
-   <span data-ttu-id="032e4-153">Uso delle funzioni di enumerazione in un gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-153">Using the enumeration functions within a group</span></span>
-   <span data-ttu-id="032e4-154">Enumerazione dei membri del gruppo</span><span class="sxs-lookup"><span data-stu-id="032e4-154">Enumerating group members</span></span>
-   <span data-ttu-id="032e4-155">Uso dell'infrastruttura di notifica ed evento con i gruppi</span><span class="sxs-lookup"><span data-stu-id="032e4-155">Using the notification and event infrastructure with groups</span></span>

 

 



