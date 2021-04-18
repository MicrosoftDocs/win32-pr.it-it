---
UID: NE:directml.DML_GRAPH_EDGE_TYPE
title: DML_GRAPH_EDGE_TYPE
description: Definisce le costanti che specificano un tipo di bordo del grafico. Per informazioni sull'utilizzo di questa enumerazione, vedere [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) .
helpviewer_keywords:
- DML_GRAPH_EDGE_TYPE
- DML_GRAPH_EDGE_TYPE structure
- direct3d12.dml_graph_edge_type
- directml/DML_GRAPH_EDGE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_TYPE, DML_GRAPH_EDGE_TYPE structure, direct3d12.dml_graph_edge_type, directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
- directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
ms.openlocfilehash: 19b11686f3741c386ca03e84af5a41af1ce5cb52
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320413"
---
# <a name="dml_graph_edge_type-enumeration-directmlh"></a><span data-ttu-id="40b51-104">Enumerazione DML_GRAPH_EDGE_TYPE (directml. h)</span><span class="sxs-lookup"><span data-stu-id="40b51-104">DML_GRAPH_EDGE_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="40b51-105">Definisce le costanti che specificano un tipo di bordo del grafico.</span><span class="sxs-lookup"><span data-stu-id="40b51-105">Defines constants that specify a type of graph edge.</span></span> <span data-ttu-id="40b51-106">Per informazioni sull'utilizzo di questa enumerazione, vedere [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="40b51-106">See [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) for the usage of this enumeration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40b51-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="40b51-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="40b51-108">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="40b51-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="40b51-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40b51-109">Syntax</span></span>
```cpp
typedef enum DML_GRAPH_EDGE_TYPE {
  DML_GRAPH_EDGE_TYPE_INVALID,
  DML_GRAPH_EDGE_TYPE_INPUT,
  DML_GRAPH_EDGE_TYPE_OUTPUT,
  DML_GRAPH_EDGE_TYPE_INTERMEDIATE
} ;
```

## <a name="constants"></a><span data-ttu-id="40b51-110">Costanti</span><span class="sxs-lookup"><span data-stu-id="40b51-110">Constants</span></span>

| <span data-ttu-id="40b51-111">Nome</span><span class="sxs-lookup"><span data-stu-id="40b51-111">Name</span></span> | <span data-ttu-id="40b51-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40b51-112">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="40b51-113">DML_GRAPH_EDGE_TYPE_INVALID</span><span class="sxs-lookup"><span data-stu-id="40b51-113">DML_GRAPH_EDGE_TYPE_INVALID</span></span> | <span data-ttu-id="40b51-114">Specifica un tipo di bordo grafico sconosciuto e non è mai valido.</span><span class="sxs-lookup"><span data-stu-id="40b51-114">Specifies an unknown graph edge type, and is never valid.</span></span> <span data-ttu-id="40b51-115">L'utilizzo di questo valore genera un errore.</span><span class="sxs-lookup"><span data-stu-id="40b51-115">Using this value results in an error.</span></span> |
| <span data-ttu-id="40b51-116">DML_GRAPH_EDGE_TYPE_INPUT</span><span class="sxs-lookup"><span data-stu-id="40b51-116">DML_GRAPH_EDGE_TYPE_INPUT</span></span> | <span data-ttu-id="40b51-117">Specifica che il bordo del grafico è descritto dalla struttura [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="40b51-117">Specifies that the graph edge is described by the [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) structure.</span></span> |
| <span data-ttu-id="40b51-118">DML_GRAPH_EDGE_TYPE_OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40b51-118">DML_GRAPH_EDGE_TYPE_OUTPUT</span></span> | <span data-ttu-id="40b51-119">Specifica che il bordo del grafico è descritto dalla struttura [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="40b51-119">Specifies that the graph edge is described by the [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) structure.</span></span> |
| <span data-ttu-id="40b51-120">DML_GRAPH_EDGE_TYPE_INTERMEDIATE</span><span class="sxs-lookup"><span data-stu-id="40b51-120">DML_GRAPH_EDGE_TYPE_INTERMEDIATE</span></span> | <span data-ttu-id="40b51-121">Specifica che il bordo del grafico è descritto dalla struttura [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="40b51-121">Specifies that the graph edge is described by the [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) structure.</span></span><br><br><span data-ttu-id="40b51-122"># # Disponibilità</span><span class="sxs-lookup"><span data-stu-id="40b51-122">## Availability</span></span><br><br><span data-ttu-id="40b51-123">Questa API è stata introdotta nella versione DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="40b51-123">This API was introduced in DirectML version `1.1.0`.</span></span> |


## <a name="requirements"></a><span data-ttu-id="40b51-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40b51-124">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="40b51-125">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="40b51-125">**Header**</span></span> | <span data-ttu-id="40b51-126">directml. h</span><span class="sxs-lookup"><span data-stu-id="40b51-126">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="40b51-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40b51-127">See also</span></span>

* [<span data-ttu-id="40b51-128">Metodo IDMLDevice1:: CompileGraph</span><span class="sxs-lookup"><span data-stu-id="40b51-128">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="40b51-129">Struttura DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="40b51-129">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)     
* [<span data-ttu-id="40b51-130">Struttura DML_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="40b51-130">DML_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_graph_edge_desc.md)
* [<span data-ttu-id="40b51-131">Struttura DML_INPUT_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="40b51-131">DML_INPUT_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_input_graph_edge_desc.md)
* [<span data-ttu-id="40b51-132">Struttura DML_OUTPUT_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="40b51-132">DML_OUTPUT_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_output_graph_edge_desc.md)
* [<span data-ttu-id="40b51-133">Struttura DML_INTERMEDIATE_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="40b51-133">DML_INTERMEDIATE_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_intermediate_graph_edge_desc.md)