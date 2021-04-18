---
description: Connessione e disconnessione di nodi della topologia
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: Connessione e disconnessione di nodi della topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08057eba74314ae6b87da418b743a089506a3b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305475"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a><span data-ttu-id="d0d71-103">Connessione e disconnessione di nodi della topologia</span><span class="sxs-lookup"><span data-stu-id="d0d71-103">Connecting and Disconnecting Topology Nodes</span></span>

<span data-ttu-id="d0d71-104">Per una topologia funzionante, è necessario che il nodo di origine e il nodo di output siano connessi.</span><span class="sxs-lookup"><span data-stu-id="d0d71-104">For a topology to be functional, the source node and the output node must be connected.</span></span> <span data-ttu-id="d0d71-105">Per connettere due nodi della topologia, trascinare l'output del nodo di un nodo nell'input del nodo dell'altro nodo.</span><span class="sxs-lookup"><span data-stu-id="d0d71-105">To connect two topology nodes, drag the node output of one node to the node input of the other node.</span></span> <span data-ttu-id="d0d71-106">TopoEdit Visualizza la connessione al nodo come linea nera.</span><span class="sxs-lookup"><span data-stu-id="d0d71-106">TopoEdit displays the node connection as a black line.</span></span> <span data-ttu-id="d0d71-107">Equivale a connettere i nodi della topologia chiamando il metodo [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) .</span><span class="sxs-lookup"><span data-stu-id="d0d71-107">This is equivalent to connecting topology nodes by calling the [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) method.</span></span>

<span data-ttu-id="d0d71-108">La topologia può essere risolta solo se la connessione al nodo è valida. ovvero se i tipi di supporti dei due nodi sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="d0d71-108">The topology can be resolved only if the node connection is valid; that is, if the media types of the two nodes are compatible.</span></span> <span data-ttu-id="d0d71-109">Per informazioni sulla risoluzione delle topologie, vedere la pagina relativa alla [risoluzione di una topologia con TopoEdit](resolving-a-topology-with-topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="d0d71-109">For information about resolving topologies, see [Resolving a Topology with TopoEdit](resolving-a-topology-with-topoedit.md).</span></span>

<span data-ttu-id="d0d71-110">Se si tenta di effettuare una connessione da un nodo già connesso, la nuova connessione al nodo sostituisce quella precedente.</span><span class="sxs-lookup"><span data-stu-id="d0d71-110">If you attempt to make a connection from a node that is already connected, the new node connection replaces the old node connection.</span></span>

<span data-ttu-id="d0d71-111">Per eliminare una connessione, selezionare la connessione al nodo e premere il tasto CANC o scegliere **Elimina** dal menu **topologia** .</span><span class="sxs-lookup"><span data-stu-id="d0d71-111">To delete a connection, select the node connection and press the DELETE key or select **Delete** from the **Topology** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0d71-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d0d71-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0d71-113">Compilazione di topologie tramite TopoEdit</span><span class="sxs-lookup"><span data-stu-id="d0d71-113">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="d0d71-114">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="d0d71-114">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



