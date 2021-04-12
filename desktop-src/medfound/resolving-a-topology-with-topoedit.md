---
description: Risoluzione di una topologia con TopoEdit
ms.assetid: da3e2bbc-7c9f-4a15-8842-c1bb00662cd2
title: Risoluzione di una topologia con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8397e380b19a6f45736c06e859d2a80456aad079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226507"
---
# <a name="resolving-a-topology-with-topoedit"></a><span data-ttu-id="18e65-103">Risoluzione di una topologia con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="18e65-103">Resolving a Topology with TopoEdit</span></span>

<span data-ttu-id="18e65-104">Esistono due tipi di topologie:</span><span class="sxs-lookup"><span data-stu-id="18e65-104">There are two types of topologies:</span></span>

-   <span data-ttu-id="18e65-105">Topologia parziale.</span><span class="sxs-lookup"><span data-stu-id="18e65-105">Partial Topology.</span></span> <span data-ttu-id="18e65-106">Il nodo di origine è connesso direttamente al nodo di output.</span><span class="sxs-lookup"><span data-stu-id="18e65-106">The source node is connected directly to the output node.</span></span> <span data-ttu-id="18e65-107">In alcuni casi, una topologia parziale può avere alcuni nodi di trasformazione intermedi, ad esempio effetti, ma non tutti.</span><span class="sxs-lookup"><span data-stu-id="18e65-107">In some cases, a partial topology can have some intermediate transform nodes, such as effects, but not all.</span></span> <span data-ttu-id="18e65-108">I nodi di trasformazione omessi sono in genere decodificatori o conversione di formato MFTs, ad esempio convertitori di colori e ricampionatori audio.</span><span class="sxs-lookup"><span data-stu-id="18e65-108">The transform nodes that are omitted are typically decoders or format conversion MFTs, such as color converters and audio resamplers.</span></span>

-   <span data-ttu-id="18e65-109">Topologia completa.</span><span class="sxs-lookup"><span data-stu-id="18e65-109">Full Topology.</span></span> <span data-ttu-id="18e65-110">Il nodo di origine è connesso al nodo di output tramite un nodo di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="18e65-110">The source node is connected to the output node through a transform node.</span></span> <span data-ttu-id="18e65-111">Questo tipo di topologia deve avere ogni nodo per elaborare i dati.</span><span class="sxs-lookup"><span data-stu-id="18e65-111">This type of topology must have every node to process data.</span></span>

<span data-ttu-id="18e65-112">TopoEdit può riprodurre solo topologie complete.</span><span class="sxs-lookup"><span data-stu-id="18e65-112">TopoEdit can only play full topologies.</span></span> <span data-ttu-id="18e65-113">TopoEdit utilizza l'oggetto caricatore della topologia, fornito da Media Foundation, per convertire una topologia parziale in una topologia completa inserendo le trasformazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="18e65-113">TopoEdit uses the topology loader object, provided by Media Foundation, to convert a partial topology into a full topology by inserting the required transforms.</span></span> <span data-ttu-id="18e65-114">Il processo di creazione di una topologia completa è denominato risoluzione di una topologia.</span><span class="sxs-lookup"><span data-stu-id="18e65-114">The process of creating a full topology is called resolving a topology.</span></span>

<span data-ttu-id="18e65-115">Per informazioni sui tipi di topologia, vedere la sezione topologie parziali in [informazioni sulle](about-topologies.md)topologie.</span><span class="sxs-lookup"><span data-stu-id="18e65-115">For information about topology types, see the Partial Topologies section in [About Topologies](about-topologies.md).</span></span>

<span data-ttu-id="18e65-116">Prima di risolvere una topologia, verificare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="18e65-116">Before you resolve a topology ensure that:</span></span>

-   <span data-ttu-id="18e65-117">La topologia contiene un nodo di origine e un nodo di output.</span><span class="sxs-lookup"><span data-stu-id="18e65-117">The topology contains a source node and an output node.</span></span>

-   <span data-ttu-id="18e65-118">I nodi di origine e di output sono connessi tramite una connessione di nodo valida.</span><span class="sxs-lookup"><span data-stu-id="18e65-118">The source and the output nodes are connected by a valid node connection.</span></span> <span data-ttu-id="18e65-119">Durante la risoluzione della topologia, il caricatore della topologia controlla il tipo di supporto dei nodi per la compatibilità.</span><span class="sxs-lookup"><span data-stu-id="18e65-119">During topology resolution, the topology loader checks the media type of the nodes for compatibility.</span></span> <span data-ttu-id="18e65-120">Se esiste una connessione nodo non valida, il processo ha esito negativo e viene visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="18e65-120">If an invalid node connection exists, then the process fails and an error message is displayed.</span></span>

<span data-ttu-id="18e65-121">Per risolvere una topologia, scegliere **Risolvi topologia** dal menu **topologia** .</span><span class="sxs-lookup"><span data-stu-id="18e65-121">To resolve a topology, from the **Topology** menu, click **Resolve Topology**.</span></span>

<span data-ttu-id="18e65-122">La barra degli strumenti indica lo stato della topologia: **\[ solved \]** o **\[ not resolved \]**.</span><span class="sxs-lookup"><span data-stu-id="18e65-122">The toolbar indicates the topology status: **\[Resolved\]** or **\[Not Resolved\]**.</span></span>

<span data-ttu-id="18e65-123">Se TopoEdit risolve correttamente una topologia, **lo stato della topologia** è impostato su **\[ risolto \]** e i controlli di riproduzione sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="18e65-123">If TopoEdit resolves a topology successfully, **Topology Status** is set to **\[Resolved\]** and the playback controls are enabled.</span></span>

<span data-ttu-id="18e65-124">Ogni volta che si apportano modifiche alla topologia, **lo stato della topologia** è impostato su **\[ non risolto \]** , a indicare che è necessario risolverlo di nuovo.</span><span class="sxs-lookup"><span data-stu-id="18e65-124">Each time you make changes to the topology, **Topology Status** is set to **\[Not Resolved\]** which indicates that it must be resolved again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18e65-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18e65-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18e65-126">Compilazione di topologie tramite TopoEdit</span><span class="sxs-lookup"><span data-stu-id="18e65-126">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="18e65-127">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="18e65-127">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



