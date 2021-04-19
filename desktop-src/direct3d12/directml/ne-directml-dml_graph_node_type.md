---
UID: NE:directml.DML_GRAPH_NODE_TYPE
title: DML_GRAPH_NODE_TYPE
description: Definisce le costanti che specificano un tipo di nodo del grafo. Per informazioni sull'utilizzo di questa enumerazione, vedere [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) .
helpviewer_keywords:
- DML_GRAPH_NODE_TYPE
- DML_GRAPH_NODE_TYPE structure
- direct3d12.dml_graph_node_type
- directml/DML_GRAPH_NODE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_NODE_TYPE, DML_GRAPH_NODE_TYPE structure, direct3d12.dml_graph_node_type, directml/DML_GRAPH_NODE_TYPE
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
- DML_GRAPH_NODE_TYPE
- directml/DML_GRAPH_NODE_TYPE
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
- DML_GRAPH_NODE_TYPE
ms.openlocfilehash: 1788dfcce20ce2a9e490bf7ed6e8ef84e306d659
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320279"
---
# <a name="dml_graph_node_type-enumeration-directmlh"></a><span data-ttu-id="d06ab-104">Enumerazione DML_GRAPH_NODE_TYPE (directml. h)</span><span class="sxs-lookup"><span data-stu-id="d06ab-104">DML_GRAPH_NODE_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="d06ab-105">Definisce le costanti che specificano un tipo di nodo del grafo.</span><span class="sxs-lookup"><span data-stu-id="d06ab-105">Defines constants that specify a type of graph node.</span></span> <span data-ttu-id="d06ab-106">Per informazioni sull'utilizzo di questa enumerazione, vedere [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="d06ab-106">See [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) for the usage of this enumeration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d06ab-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="d06ab-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="d06ab-108">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="d06ab-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d06ab-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d06ab-109">Syntax</span></span>
```cpp
typedef enum DML_GRAPH_NODE_TYPE {
  DML_GRAPH_NODE_TYPE_INVALID,
  DML_GRAPH_NODE_TYPE_OPERATOR
} ;
```

## <a name="constants"></a><span data-ttu-id="d06ab-110">Costanti</span><span class="sxs-lookup"><span data-stu-id="d06ab-110">Constants</span></span>

| <span data-ttu-id="d06ab-111">Nome</span><span class="sxs-lookup"><span data-stu-id="d06ab-111">Name</span></span> | <span data-ttu-id="d06ab-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d06ab-112">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="d06ab-113">DML_GRAPH_NODE_TYPE_INVALID</span><span class="sxs-lookup"><span data-stu-id="d06ab-113">DML_GRAPH_NODE_TYPE_INVALID</span></span> | <span data-ttu-id="d06ab-114">Specifica un tipo di bordo grafico sconosciuto e non è mai valido.</span><span class="sxs-lookup"><span data-stu-id="d06ab-114">Specifies an unknown graph edge type, and is never valid.</span></span> <span data-ttu-id="d06ab-115">L'utilizzo di questo valore genera un errore.</span><span class="sxs-lookup"><span data-stu-id="d06ab-115">Using this value results in an error.</span></span> |
| <span data-ttu-id="d06ab-116">DML_GRAPH_NODE_TYPE_OPERATOR</span><span class="sxs-lookup"><span data-stu-id="d06ab-116">DML_GRAPH_NODE_TYPE_OPERATOR</span></span> | <span data-ttu-id="d06ab-117">Specifica che il bordo del grafico è descritto dalla struttura [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="d06ab-117">Specifies that the graph edge is described by the [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md) structure.</span></span><br><br><span data-ttu-id="d06ab-118"># # Disponibilità</span><span class="sxs-lookup"><span data-stu-id="d06ab-118">## Availability</span></span><br><br><span data-ttu-id="d06ab-119">Questa API è stata introdotta nella versione DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="d06ab-119">This API was introduced in DirectML version `1.1.0`.</span></span> |


## <a name="requirements"></a><span data-ttu-id="d06ab-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d06ab-120">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d06ab-121">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="d06ab-121">**Header**</span></span> | <span data-ttu-id="d06ab-122">directml. h</span><span class="sxs-lookup"><span data-stu-id="d06ab-122">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="d06ab-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d06ab-123">See also</span></span>

* [<span data-ttu-id="d06ab-124">Metodo IDMLDevice1:: CompileGraph</span><span class="sxs-lookup"><span data-stu-id="d06ab-124">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="d06ab-125">Struttura DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="d06ab-125">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)     
* [<span data-ttu-id="d06ab-126">Struttura DML_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="d06ab-126">DML_GRAPH_NODE_DESC structure</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="d06ab-127">DML_OPERATOR_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="d06ab-127">DML_OPERATOR_GRAPH_NODE_DESC</span></span>](./ns-directml-dml_operator_graph_node_desc.md)