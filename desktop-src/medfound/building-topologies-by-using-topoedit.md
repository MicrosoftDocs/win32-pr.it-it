---
description: Compilazione di topologie tramite TopoEdit
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: Compilazione di topologie tramite TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92758911113c7500cb13fa814d07321435fafeb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127999"
---
# <a name="building-topologies-by-using-topoedit"></a><span data-ttu-id="c5c2c-103">Compilazione di topologie tramite TopoEdit</span><span class="sxs-lookup"><span data-stu-id="c5c2c-103">Building Topologies by Using TopoEdit</span></span>

<span data-ttu-id="c5c2c-104">Una topologia deve disporre dei tre nodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5c2c-104">A topology must have the following three nodes:</span></span>

-   <span data-ttu-id="c5c2c-105">Nodo di origine: flussi da un file multimediale, usati come origine per la topologia.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-105">Source node: The streams from a media file, which are used as a source for the topology.</span></span>
-   <span data-ttu-id="c5c2c-106">Nodo Transform: una trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="c5c2c-106">Transform node: A Media Foundation transform (MFT).</span></span> <span data-ttu-id="c5c2c-107">Questi nodi sono in genere codificatori, decodificatori ed effetti per la topologia.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-107">These nodes are usually encoders, decoders, and effects for the topology.</span></span>
-   <span data-ttu-id="c5c2c-108">Nodo di output: sink del flusso che passa i dati multimediali, i fotogrammi video o i flussi audio alla sessione multimediale per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-108">Output node: The stream sink that passes the media data, video frames, or audio streams to the Media Session for playback.</span></span>

<span data-ttu-id="c5c2c-109">Per informazioni sulla struttura della topologia, vedere [informazioni sulle topologie](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="c5c2c-109">For information about topology structure, see [About Topologies](about-topologies.md).</span></span>

<span data-ttu-id="c5c2c-110">Per compilare una topologia, è necessario aggiungere i nodi, connettere i nodi e risolvere la topologia in modo che sia possibile riprodurli.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-110">To build a topology, you must add the nodes, connect the nodes, and resolve the topology so that it can be played.</span></span>

<span data-ttu-id="c5c2c-111">I nodi della topologia vengono visualizzati come caselle, con testo che mostra il nome del nodo.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-111">Topology nodes are displayed as boxes, with text showing the name of the node.</span></span> <span data-ttu-id="c5c2c-112">Le caselle verdi rappresentano i nodi aggiunti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-112">Green boxes represent the nodes that are added by the user.</span></span> <span data-ttu-id="c5c2c-113">Quando viene risolta una topologia, TopoEdit può aggiungere nodi Transform alla topologia automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-113">When a topology is resolved, TopoEdit can add transform nodes to the topology automatically.</span></span> <span data-ttu-id="c5c2c-114">Questi vengono visualizzati come caselle blu nel **riquadro topologia**.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-114">These appear as blue boxes on the **Topology Pane**.</span></span>

<span data-ttu-id="c5c2c-115">Gli input e gli output della topologia sono rappresentati da quadratini neri lungo il bordo del nodo.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-115">Topology inputs and outputs are represented by as black squares along the edge of the node.</span></span> <span data-ttu-id="c5c2c-116">L' *input del nodo* viene visualizzato sul lato sinistro del nodo e l'output del *nodo* si trova sul lato destro del nodo.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-116">The *node input* is shown on the left side of the node, and the *node output* is on the right side of the node.</span></span>

<span data-ttu-id="c5c2c-117">I nodi della topologia sono connessi tramite una *connessione al nodo* visualizzata come una linea nera che connette l'input del nodo di un nodo all'output del nodo di un altro nodo.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-117">The topology nodes are connected through a *node connection* that appears as a black line connecting the node input of one node to the node output of another node.</span></span>

<span data-ttu-id="c5c2c-118">Nella figura seguente viene illustrata una topologia connessa per un'origine audio.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-118">The following illustration shows a connected topology for an audio source.</span></span>

![illustrazione che mostra le connessioni dal nodo di origine a due nodi di trasformazione, quindi al nodo di output](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

<span data-ttu-id="c5c2c-120">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="c5c2c-120">This section contains the following topics:</span></span>



| <span data-ttu-id="c5c2c-121">Argomento</span><span class="sxs-lookup"><span data-stu-id="c5c2c-121">Topic</span></span>                                                                                          | <span data-ttu-id="c5c2c-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5c2c-122">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="c5c2c-123">Aggiunta di nodi di origine con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="c5c2c-123">Adding Source Nodes with TopoEdit</span></span>](adding-source-nodes-with-topoedit.md)                     | <span data-ttu-id="c5c2c-124">Viene descritto il processo di aggiunta di nodi di origine a una topologia.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-124">Describes the process of adding source nodes to a topology.</span></span>    |
| [<span data-ttu-id="c5c2c-125">Aggiunta di nodi Transform con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="c5c2c-125">Adding Transform Nodes with TopoEdit</span></span>](adding-transform-nodes-with-topoedit.md)               | <span data-ttu-id="c5c2c-126">Viene descritto il processo di aggiunta di nodi Transform a una topologia.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-126">Describes the process of adding transform nodes to a topology.</span></span> |
| [<span data-ttu-id="c5c2c-127">Aggiunta di nodi di output con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="c5c2c-127">Adding Output Nodes with TopoEdit</span></span>](adding-output-nodes-with-topoedit.md)                     | <span data-ttu-id="c5c2c-128">Viene descritto il processo di aggiunta di nodi di output a una topologia.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-128">Describes the process of adding output nodes to a topology.</span></span>    |
| [<span data-ttu-id="c5c2c-129">Connessione e disconnessione di nodi della topologia</span><span class="sxs-lookup"><span data-stu-id="c5c2c-129">Connecting and Disconnecting Topology Nodes</span></span>](connecting-and-disconnecting-topology-nodes.md) | <span data-ttu-id="c5c2c-130">Descrive il processo di connessione di due nodi.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-130">Describes the process of connecting two nodes.</span></span>                 |
| [<span data-ttu-id="c5c2c-131">Risoluzione di una topologia con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="c5c2c-131">Resolving a Topology with TopoEdit</span></span>](resolving-a-topology-with-topoedit.md)                   | <span data-ttu-id="c5c2c-132">Descrive il processo di risoluzione della topologia.</span><span class="sxs-lookup"><span data-stu-id="c5c2c-132">Describes the process of topology resolution.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="c5c2c-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5c2c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5c2c-134">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="c5c2c-134">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



