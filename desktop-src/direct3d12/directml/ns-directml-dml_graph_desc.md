---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Descrive un grafico degli operatori DirectML usati per compilare un operatore combinato e ottimizzato.
helpviewer_keywords:
- DML_GRAPH_DESC
- DML_GRAPH_DESC structure
- direct3d12.dml_graph_desc
- directml/DML_GRAPH_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_DESC, DML_GRAPH_DESC structure, direct3d12.dml_graph_desc, directml/DML_GRAPH_DESC
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_GRAPH_DESC
- directml/DML_GRAPH_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_GRAPH_DESC
ms.openlocfilehash: e72209d19bb26524576783becbbfbf94566d8370
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320374"
---
# <a name="dml_graph_desc-structure-directmlh"></a><span data-ttu-id="ac52c-103">Struttura DML_GRAPH_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="ac52c-103">DML_GRAPH_DESC structure (directml.h)</span></span>

<span data-ttu-id="ac52c-104">Descrive un grafico degli operatori DirectML usati per compilare un operatore combinato e ottimizzato.</span><span class="sxs-lookup"><span data-stu-id="ac52c-104">Describes a graph of DirectML operators used to compile a combined, optimized operator.</span></span> <span data-ttu-id="ac52c-105">Vedere [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="ac52c-105">See [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac52c-106">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="ac52c-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="ac52c-107">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="ac52c-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ac52c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac52c-108">Syntax</span></span>
```cpp
struct DML_GRAPH_DESC {
  UINT                      InputCount;
  UINT                      OutputCount;
  UINT                      NodeCount;
  const DML_GRAPH_NODE_DESC *Nodes;
  UINT                      InputEdgeCount;
  const DML_GRAPH_EDGE_DESC *InputEdges;
  UINT                      OutputEdgeCount;
  const DML_GRAPH_EDGE_DESC *OutputEdges;
  UINT                      IntermediateEdgeCount;
  const DML_GRAPH_EDGE_DESC *IntermediateEdges;
};
```



## <a name="members"></a><span data-ttu-id="ac52c-109">Members</span><span class="sxs-lookup"><span data-stu-id="ac52c-109">Members</span></span>

`InputCount`

<span data-ttu-id="ac52c-110">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ac52c-110">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="ac52c-111">Numero di input del grafico complessivo.</span><span class="sxs-lookup"><span data-stu-id="ac52c-111">The number of inputs of the overall graph.</span></span> <span data-ttu-id="ac52c-112">Ogni input del grafo può essere connesso a un numero variabile di nodi interni, pertanto può essere diverso da *InputEdgeCount*.</span><span class="sxs-lookup"><span data-stu-id="ac52c-112">Each graph input may be connected to a variable number of internal nodes, therefore this may be different from *InputEdgeCount*.</span></span>


`OutputCount`

<span data-ttu-id="ac52c-113">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ac52c-113">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="ac52c-114">Numero di output del grafico complessivo.</span><span class="sxs-lookup"><span data-stu-id="ac52c-114">The number of outputs of the overall graph.</span></span> <span data-ttu-id="ac52c-115">Ogni output del grafo può essere connesso a un numero variabile di nodi interni, pertanto può essere diverso da *OutputEdgeCount*.</span><span class="sxs-lookup"><span data-stu-id="ac52c-115">Each graph output may be connected to a variable number of internal nodes, therefore this may be different from *OutputEdgeCount*.</span></span>


`NodeCount`

<span data-ttu-id="ac52c-116">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ac52c-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="ac52c-117">Numero di nodi interni nel grafico.</span><span class="sxs-lookup"><span data-stu-id="ac52c-117">The number of internal nodes in the graph.</span></span>


`Nodes`

<span data-ttu-id="ac52c-118">Tipo: \_ \_ Dimensione campo \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="ac52c-118">Type: \_Field\_size\_(NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md)\***</span></span>

<span data-ttu-id="ac52c-119">Nodi interni nel grafico.</span><span class="sxs-lookup"><span data-stu-id="ac52c-119">The internal nodes in the graph.</span></span>


`InputEdgeCount`

<span data-ttu-id="ac52c-120">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ac52c-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="ac52c-121">Numero di connessioni tra input e input del grafo dei nodi interni nel grafico.</span><span class="sxs-lookup"><span data-stu-id="ac52c-121">The number of connections between graph inputs and inputs of internal nodes in the graph.</span></span>


`InputEdges`

<span data-ttu-id="ac52c-122">Tipo: \_ \_ Dimensione campo \_ (InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="ac52c-122">Type: \_Field\_size\_(InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="ac52c-123">Matrice di connessioni tra input del grafo e input di nodi interni nel grafico.</span><span class="sxs-lookup"><span data-stu-id="ac52c-123">An array of connections between graph inputs and inputs of internal nodes in the graph.</span></span> <span data-ttu-id="ac52c-124">Il campo *tipo* all'interno di ogni elemento deve essere impostato su [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span><span class="sxs-lookup"><span data-stu-id="ac52c-124">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`OutputEdgeCount`

<span data-ttu-id="ac52c-125">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ac52c-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="ac52c-126">Il numero di connessioni tra output del grafo e output dei nodi interni nel grafico.</span><span class="sxs-lookup"><span data-stu-id="ac52c-126">The number of connections between graph outputs and outputs of internal nodes in the graph.</span></span>


`OutputEdges`

<span data-ttu-id="ac52c-127">Tipo: \_ \_ Dimensione campo \_ (OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="ac52c-127">Type: \_Field\_size\_(OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="ac52c-128">Matrice di connessioni tra output del grafo e output dei nodi interni nel grafico.</span><span class="sxs-lookup"><span data-stu-id="ac52c-128">An array of connections between graph outputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="ac52c-129">Il campo *tipo* all'interno di ogni elemento deve essere impostato su [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span><span class="sxs-lookup"><span data-stu-id="ac52c-129">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`IntermediateEdgeCount`

<span data-ttu-id="ac52c-130">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ac52c-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="ac52c-131">Numero di connessioni interne tra i nodi del grafico.</span><span class="sxs-lookup"><span data-stu-id="ac52c-131">The number of internal connections between nodes in the graph.</span></span>


`IntermediateEdges`

<span data-ttu-id="ac52c-132">Tipo: \_ \_ Dimensione campo \_ (IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="ac52c-132">Type: \_Field\_size\_(IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="ac52c-133">Matrice di connessioni tra input e output dei nodi interni nel grafico.</span><span class="sxs-lookup"><span data-stu-id="ac52c-133">An array of connections between inputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="ac52c-134">Il campo tipo all'interno di ogni elemento deve essere impostato su [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span><span class="sxs-lookup"><span data-stu-id="ac52c-134">The Type field within each element should be set to [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span></span>


## <a name="remarks"></a><span data-ttu-id="ac52c-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac52c-135">Remarks</span></span>
<span data-ttu-id="ac52c-136">Il grafo descritto da questa struttura deve essere un grafico aciclici diretto.</span><span class="sxs-lookup"><span data-stu-id="ac52c-136">The graph described by this structure must be a directed acyclic graph.</span></span> <span data-ttu-id="ac52c-137">È necessario definire una connessione per l'input e l'output di ogni nodo fornito, eccetto gli input e gli output facoltativi per l'operatore associato.</span><span class="sxs-lookup"><span data-stu-id="ac52c-137">You must define a connection for the input and output of each supplied node, except for inputs and outputs that are optional for the associated operator.</span></span>

<span data-ttu-id="ac52c-138">I nodi possono utilizzare operatori creati utilizzando il flag di [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) per determinati input.</span><span class="sxs-lookup"><span data-stu-id="ac52c-138">Nodes may use operators that were created using the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag for certain inputs.</span></span> <span data-ttu-id="ac52c-139">Tutti gli input dell'operatore che usano questo flag devono essere connessi agli input del grafo.</span><span class="sxs-lookup"><span data-stu-id="ac52c-139">Any operator inputs using this flag must be connected to graph inputs.</span></span> <span data-ttu-id="ac52c-140">Tutti gli input dell'operatore connessi allo stesso input del grafo devono usare o omettere questo flag in modo equivalente.</span><span class="sxs-lookup"><span data-stu-id="ac52c-140">All operator inputs connected to the same graph input must use or omit this flag equivalently.</span></span>

<span data-ttu-id="ac52c-141">È possibile connettere gli operatori i cui input e output connessi utilizzano conteggi di dimensione, dimensioni e tipi di dati diversi.</span><span class="sxs-lookup"><span data-stu-id="ac52c-141">It is legal to connect operators whose connected inputs and outputs use different dimension counts, sizes, and data types.</span></span> <span data-ttu-id="ac52c-142">Questo implica che il BLOB di dati del tensore viene interpretato in modo diverso da ogni operatore.</span><span class="sxs-lookup"><span data-stu-id="ac52c-142">This implies that the tensor data blob is interpreted differently by each operator.</span></span> <span data-ttu-id="ac52c-143">Tuttavia, il campo *TotalTensorSizeInBytes* di input e output del tensore connesso deve essere identico.</span><span class="sxs-lookup"><span data-stu-id="ac52c-143">The *TotalTensorSizeInBytes* field of connected tensor inputs and outputs must be identical, though.</span></span> <span data-ttu-id="ac52c-144">Gli operatori devono leggere solo le aree di i tensori scritti dagli operatori precedenti.</span><span class="sxs-lookup"><span data-stu-id="ac52c-144">Operators should only read regions of tensors written by earlier operators.</span></span> <span data-ttu-id="ac52c-145">Le aree di riempimento nell'output di un'operazione (risultante dall'uso di stride) non sono necessariamente lette come zero dagli operatori di flusso inattivo.</span><span class="sxs-lookup"><span data-stu-id="ac52c-145">Any padding regions in the output of an operation (resulting from the use of strides) are not guaranteed to be read as zero by down-stream operators.</span></span>

## <a name="availability"></a><span data-ttu-id="ac52c-146">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="ac52c-146">Availability</span></span>

<span data-ttu-id="ac52c-147">Questa API è stata introdotta nella versione DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="ac52c-147">This API was introduced in DirectML version `1.1.0`.</span></span>


## <a name="requirements"></a><span data-ttu-id="ac52c-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac52c-148">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ac52c-149">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="ac52c-149">**Header**</span></span> | <span data-ttu-id="ac52c-150">directml. h</span><span class="sxs-lookup"><span data-stu-id="ac52c-150">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="ac52c-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac52c-151">See also</span></span>

* [<span data-ttu-id="ac52c-152">Metodo IDMLDevice1:: CompileGraph</span><span class="sxs-lookup"><span data-stu-id="ac52c-152">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="ac52c-153">Struct DML_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="ac52c-153">DML_GRAPH_NODE_DESC struct</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="ac52c-154">Struct DML_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="ac52c-154">DML_GRAPH_EDGE_DESC struct</span></span>](./ns-directml-dml_graph_edge_desc.md)