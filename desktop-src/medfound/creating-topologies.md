---
description: Creazione di topologie
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Creazione di topologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ec738c82ea2b85bcae7d4c05627b81ad939db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401546"
---
# <a name="creating-topologies"></a><span data-ttu-id="7bb88-103">Creazione di topologie</span><span class="sxs-lookup"><span data-stu-id="7bb88-103">Creating Topologies</span></span>

<span data-ttu-id="7bb88-104">In questa sezione vengono descritte alcune delle procedure generali per la creazione di una topologia.</span><span class="sxs-lookup"><span data-stu-id="7bb88-104">This section describes some of the general procedures for creating a topology.</span></span>

<span data-ttu-id="7bb88-105">La procedura generale per la creazione di una topologia è la seguente:</span><span class="sxs-lookup"><span data-stu-id="7bb88-105">The general steps for creating a topology are as follows:</span></span>

1.  <span data-ttu-id="7bb88-106">Creare un nuovo oggetto topologia chiamando [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span><span class="sxs-lookup"><span data-stu-id="7bb88-106">Create a new topology object by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span> <span data-ttu-id="7bb88-107">Questa funzione restituisce un puntatore all'interfaccia [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) della topologia.</span><span class="sxs-lookup"><span data-stu-id="7bb88-107">This function returns a pointer to the topology's [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface.</span></span>

2.  <span data-ttu-id="7bb88-108">Inizialmente, la topologia non contiene alcun nodo.</span><span class="sxs-lookup"><span data-stu-id="7bb88-108">Initially, the topology does not contain any nodes.</span></span> <span data-ttu-id="7bb88-109">Per creare nodi per la topologia, chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode).</span><span class="sxs-lookup"><span data-stu-id="7bb88-109">To create nodes for the topology, call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode).</span></span> <span data-ttu-id="7bb88-110">Questa funzione restituisce un puntatore all'interfaccia [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) del nodo.</span><span class="sxs-lookup"><span data-stu-id="7bb88-110">This function returns a pointer to the node's [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) interface.</span></span> <span data-ttu-id="7bb88-111">Quando si crea il nodo, è necessario specificare il tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="7bb88-111">You must specify the node type when you create the node:</span></span>

    -   <span data-ttu-id="7bb88-112">Nodo di origine.</span><span class="sxs-lookup"><span data-stu-id="7bb88-112">Source node.</span></span>

    -   <span data-ttu-id="7bb88-113">Nodo Transform.</span><span class="sxs-lookup"><span data-stu-id="7bb88-113">Transform node.</span></span>

    -   <span data-ttu-id="7bb88-114">Nodo di output.</span><span class="sxs-lookup"><span data-stu-id="7bb88-114">Output node.</span></span>

    -   <span data-ttu-id="7bb88-115">Nodo tee.</span><span class="sxs-lookup"><span data-stu-id="7bb88-115">Tee node.</span></span>

3.  <span data-ttu-id="7bb88-116">Inizializzare ogni nodo.</span><span class="sxs-lookup"><span data-stu-id="7bb88-116">Initialize each node.</span></span> <span data-ttu-id="7bb88-117">Il processo di inizializzazione dipende dal tipo di nodo, come descritto negli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="7bb88-117">The initialization process depends on the node type, as described in the topics that follow.</span></span>

4.  <span data-ttu-id="7bb88-118">Aggiungere ogni nodo alla topologia chiamando [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).</span><span class="sxs-lookup"><span data-stu-id="7bb88-118">Add each node to the topology by calling [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).</span></span>

5.  <span data-ttu-id="7bb88-119">Connettere i nodi.</span><span class="sxs-lookup"><span data-stu-id="7bb88-119">Connect the nodes.</span></span> <span data-ttu-id="7bb88-120">Per connettere un nodo, chiamare [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) sul nodo upstream e passare un puntatore al nodo downstream.</span><span class="sxs-lookup"><span data-stu-id="7bb88-120">To connect a node, call [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) on the upstream node, and pass in a pointer to the downstream node.</span></span>

<span data-ttu-id="7bb88-121">Negli argomenti seguenti vengono illustrati i passaggi specifici per ogni tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="7bb88-121">The following topics give the specific steps for each node type.</span></span>



| <span data-ttu-id="7bb88-122">Argomento</span><span class="sxs-lookup"><span data-stu-id="7bb88-122">Topic</span></span>                                                    | <span data-ttu-id="7bb88-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bb88-123">Description</span></span>                     |
|----------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="7bb88-124">Creazione di nodi di origine</span><span class="sxs-lookup"><span data-stu-id="7bb88-124">Creating Source Nodes</span></span>](creating-source-nodes.md)       | <span data-ttu-id="7bb88-125">Come creare un nodo di origine.</span><span class="sxs-lookup"><span data-stu-id="7bb88-125">How to create a source node.</span></span>    |
| [<span data-ttu-id="7bb88-126">Creazione di nodi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="7bb88-126">Creating Transform Nodes</span></span>](creating-transform-nodes.md) | <span data-ttu-id="7bb88-127">Creazione di un nodo Transform.</span><span class="sxs-lookup"><span data-stu-id="7bb88-127">How to create a transform node.</span></span> |
| [<span data-ttu-id="7bb88-128">Creazione di nodi di output</span><span class="sxs-lookup"><span data-stu-id="7bb88-128">Creating Output Nodes</span></span>](creating-output-nodes.md)       | <span data-ttu-id="7bb88-129">Come creare un nodo di output.</span><span class="sxs-lookup"><span data-stu-id="7bb88-129">How to create an output node.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="7bb88-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7bb88-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bb88-131">Topologie</span><span class="sxs-lookup"><span data-stu-id="7bb88-131">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



