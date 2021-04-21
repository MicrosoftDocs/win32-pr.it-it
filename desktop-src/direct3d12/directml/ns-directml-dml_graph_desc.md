---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Descrive un grafico degli operatori DirectML usati per compilare un operatore combinato ottimizzato.
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
ms.openlocfilehash: a42996fc9fd7825e13232b245ab764c6439f9489
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802875"
---
# <a name="dml_graph_desc-structure-directmlh"></a><span data-ttu-id="73307-103">DML_GRAPH_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="73307-103">DML_GRAPH_DESC structure (directml.h)</span></span>

<span data-ttu-id="73307-104">Descrive un grafico degli operatori DirectML usati per compilare un operatore combinato ottimizzato.</span><span class="sxs-lookup"><span data-stu-id="73307-104">Describes a graph of DirectML operators used to compile a combined, optimized operator.</span></span> <span data-ttu-id="73307-105">Vedere [IDMLDevice1::CompileGraph.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="73307-105">See [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73307-106">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="73307-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="73307-107">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="73307-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="73307-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73307-108">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="73307-109">Members</span><span class="sxs-lookup"><span data-stu-id="73307-109">Members</span></span>

`InputCount`

<span data-ttu-id="73307-110">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="73307-110">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="73307-111">Numero di input del grafico complessivo.</span><span class="sxs-lookup"><span data-stu-id="73307-111">The number of inputs of the overall graph.</span></span> <span data-ttu-id="73307-112">Ogni input del grafo può essere connesso a un numero variabile di nodi interni, pertanto può essere diverso da *InputEdgeCount.*</span><span class="sxs-lookup"><span data-stu-id="73307-112">Each graph input may be connected to a variable number of internal nodes, therefore this may be different from *InputEdgeCount*.</span></span>


`OutputCount`

<span data-ttu-id="73307-113">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="73307-113">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="73307-114">Numero di output del grafico complessivo.</span><span class="sxs-lookup"><span data-stu-id="73307-114">The number of outputs of the overall graph.</span></span> <span data-ttu-id="73307-115">Ogni output del grafo può essere connesso a un numero variabile di nodi interni, pertanto può essere diverso da *OutputEdgeCount.*</span><span class="sxs-lookup"><span data-stu-id="73307-115">Each graph output may be connected to a variable number of internal nodes, therefore this may be different from *OutputEdgeCount*.</span></span>


`NodeCount`

<span data-ttu-id="73307-116">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="73307-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="73307-117">Numero di nodi interni nel grafico.</span><span class="sxs-lookup"><span data-stu-id="73307-117">The number of internal nodes in the graph.</span></span>


`Nodes`

<span data-ttu-id="73307-118">Tipo: \_ Dimensione \_ campo \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="73307-118">Type: \_Field\_size\_(NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md)\***</span></span>

<span data-ttu-id="73307-119">Nodi interni nel grafico.</span><span class="sxs-lookup"><span data-stu-id="73307-119">The internal nodes in the graph.</span></span>


`InputEdgeCount`

<span data-ttu-id="73307-120">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="73307-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="73307-121">Numero di connessioni tra gli input del grafo e gli input dei nodi interni nel grafico.</span><span class="sxs-lookup"><span data-stu-id="73307-121">The number of connections between graph inputs and inputs of internal nodes in the graph.</span></span>


`InputEdges`

<span data-ttu-id="73307-122">Tipo: \_ Dimensione \_ campo \_ (InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="73307-122">Type: \_Field\_size\_(InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="73307-123">Matrice di connessioni tra gli input del grafo e gli input dei nodi interni nel grafico.</span><span class="sxs-lookup"><span data-stu-id="73307-123">An array of connections between graph inputs and inputs of internal nodes in the graph.</span></span> <span data-ttu-id="73307-124">Il *campo Tipo* all'interno di ogni elemento deve essere impostato su [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span><span class="sxs-lookup"><span data-stu-id="73307-124">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`OutputEdgeCount`

<span data-ttu-id="73307-125">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="73307-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="73307-126">Numero di connessioni tra gli output del grafo e gli output dei nodi interni nel grafico.</span><span class="sxs-lookup"><span data-stu-id="73307-126">The number of connections between graph outputs and outputs of internal nodes in the graph.</span></span>


`OutputEdges`

<span data-ttu-id="73307-127">Tipo: \_ Dimensione \_ campo \_ (OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="73307-127">Type: \_Field\_size\_(OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="73307-128">Matrice di connessioni tra gli output del grafo e gli output dei nodi interni nel grafo.</span><span class="sxs-lookup"><span data-stu-id="73307-128">An array of connections between graph outputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="73307-129">Il *campo Tipo* all'interno di ogni elemento deve essere impostato su [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span><span class="sxs-lookup"><span data-stu-id="73307-129">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`IntermediateEdgeCount`

<span data-ttu-id="73307-130">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="73307-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="73307-131">Numero di connessioni interne tra i nodi nel grafico.</span><span class="sxs-lookup"><span data-stu-id="73307-131">The number of internal connections between nodes in the graph.</span></span>


`IntermediateEdges`

<span data-ttu-id="73307-132">Tipo: \_ Dimensione \_ campo \_ (IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="73307-132">Type: \_Field\_size\_(IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="73307-133">Matrice di connessioni tra input e output di nodi interni nel grafico.</span><span class="sxs-lookup"><span data-stu-id="73307-133">An array of connections between inputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="73307-134">Il campo Tipo all'interno di ogni elemento deve essere impostato [su DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span><span class="sxs-lookup"><span data-stu-id="73307-134">The Type field within each element should be set to [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span></span>


## <a name="remarks"></a><span data-ttu-id="73307-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="73307-135">Remarks</span></span>
<span data-ttu-id="73307-136">Il grafo descritto da questa struttura deve essere un grafo aciclico diretto.</span><span class="sxs-lookup"><span data-stu-id="73307-136">The graph described by this structure must be a directed acyclic graph.</span></span> <span data-ttu-id="73307-137">È necessario definire una connessione per l'input e l'output di ogni nodo fornito, ad eccezione degli input e degli output facoltativi per l'operatore associato.</span><span class="sxs-lookup"><span data-stu-id="73307-137">You must define a connection for the input and output of each supplied node, except for inputs and outputs that are optional for the associated operator.</span></span>

<span data-ttu-id="73307-138">I nodi possono usare operatori creati usando il flag [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) per determinati input.</span><span class="sxs-lookup"><span data-stu-id="73307-138">Nodes may use operators that were created using the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag for certain inputs.</span></span> <span data-ttu-id="73307-139">Qualsiasi input dell'operatore che usa questo flag deve essere connesso agli input del grafico.</span><span class="sxs-lookup"><span data-stu-id="73307-139">Any operator inputs using this flag must be connected to graph inputs.</span></span> <span data-ttu-id="73307-140">Tutti gli input dell'operatore connessi allo stesso input del grafo devono usare o omettere questo flag in modo equivalente.</span><span class="sxs-lookup"><span data-stu-id="73307-140">All operator inputs connected to the same graph input must use or omit this flag equivalently.</span></span>

<span data-ttu-id="73307-141">È legale connettere operatori i cui input e output connessi usano conteggi, dimensioni e tipi di dati diversi per le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="73307-141">It is legal to connect operators whose connected inputs and outputs use different dimension counts, sizes, and data types.</span></span> <span data-ttu-id="73307-142">Ciò implica che il BLOB di dati tensor viene interpretato in modo diverso da ogni operatore.</span><span class="sxs-lookup"><span data-stu-id="73307-142">This implies that the tensor data blob is interpreted differently by each operator.</span></span> <span data-ttu-id="73307-143">Il *campo TotalTensorSizeInBytes* degli input e degli output del tensore connesso deve tuttavia essere identico.</span><span class="sxs-lookup"><span data-stu-id="73307-143">The *TotalTensorSizeInBytes* field of connected tensor inputs and outputs must be identical, though.</span></span> <span data-ttu-id="73307-144">Gli operatori devono leggere solo le aree dei tensori scritti dagli operatori precedenti.</span><span class="sxs-lookup"><span data-stu-id="73307-144">Operators should only read regions of tensors written by earlier operators.</span></span> <span data-ttu-id="73307-145">Non è garantito che le aree di riempimento nell'output di un'operazione (derivanti dall'uso di stride) siano lette come zero dagli operatori down stream.</span><span class="sxs-lookup"><span data-stu-id="73307-145">Any padding regions in the output of an operation (resulting from the use of strides) are not guaranteed to be read as zero by down-stream operators.</span></span>

## <a name="availability"></a><span data-ttu-id="73307-146">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="73307-146">Availability</span></span>

<span data-ttu-id="73307-147">Questa API è stata introdotta nella versione di `1.1.0` DirectML.</span><span class="sxs-lookup"><span data-stu-id="73307-147">This API was introduced in DirectML version `1.1.0`.</span></span>


## <a name="requirements"></a><span data-ttu-id="73307-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73307-148">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="73307-149">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="73307-149">**Header**</span></span> | <span data-ttu-id="73307-150">directml.h</span><span class="sxs-lookup"><span data-stu-id="73307-150">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="73307-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73307-151">See also</span></span>

* [<span data-ttu-id="73307-152">Metodo IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="73307-152">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="73307-153">DML_GRAPH_NODE_DESC struct</span><span class="sxs-lookup"><span data-stu-id="73307-153">DML_GRAPH_NODE_DESC struct</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="73307-154">DML_GRAPH_EDGE_DESC struct</span><span class="sxs-lookup"><span data-stu-id="73307-154">DML_GRAPH_EDGE_DESC struct</span></span>](./ns-directml-dml_graph_edge_desc.md)