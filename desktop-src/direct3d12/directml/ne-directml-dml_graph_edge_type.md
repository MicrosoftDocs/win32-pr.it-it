---
UID: NE:directml.DML_GRAPH_EDGE_TYPE
title: DML_GRAPH_EDGE_TYPE
description: Definisce le costanti che specificano un tipo di bordo del grafo. Vedere [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) per l'utilizzo di questa enumerazione.
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
ms.openlocfilehash: d65649fcd2115cc7cdcc1b01da20ef44b0436e6f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417920"
---
# <a name="dml_graph_edge_type-enumeration-directmlh"></a><span data-ttu-id="ec22c-104">DML_GRAPH_EDGE_TYPE enumerazione (directml.h)</span><span class="sxs-lookup"><span data-stu-id="ec22c-104">DML_GRAPH_EDGE_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="ec22c-105">Definisce le costanti che specificano un tipo di bordo del grafo.</span><span class="sxs-lookup"><span data-stu-id="ec22c-105">Defines constants that specify a type of graph edge.</span></span> <span data-ttu-id="ec22c-106">Vedere [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) per l'utilizzo di questa enumerazione.</span><span class="sxs-lookup"><span data-stu-id="ec22c-106">See [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) for the usage of this enumeration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec22c-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="ec22c-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="ec22c-108">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="ec22c-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ec22c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec22c-109">Syntax</span></span>
```cpp
typedef enum DML_GRAPH_EDGE_TYPE {
  DML_GRAPH_EDGE_TYPE_INVALID,
  DML_GRAPH_EDGE_TYPE_INPUT,
  DML_GRAPH_EDGE_TYPE_OUTPUT,
  DML_GRAPH_EDGE_TYPE_INTERMEDIATE
} ;
```

## <a name="constants"></a><span data-ttu-id="ec22c-110">Costanti</span><span class="sxs-lookup"><span data-stu-id="ec22c-110">Constants</span></span>

| <span data-ttu-id="ec22c-111">Nome</span><span class="sxs-lookup"><span data-stu-id="ec22c-111">Name</span></span> | <span data-ttu-id="ec22c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec22c-112">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="ec22c-113">DML_GRAPH_EDGE_TYPE_INVALID</span><span class="sxs-lookup"><span data-stu-id="ec22c-113">DML_GRAPH_EDGE_TYPE_INVALID</span></span> | <span data-ttu-id="ec22c-114">Specifica un tipo di bordo del grafo sconosciuto e non è mai valido.</span><span class="sxs-lookup"><span data-stu-id="ec22c-114">Specifies an unknown graph edge type, and is never valid.</span></span> <span data-ttu-id="ec22c-115">L'uso di questo valore comporta un errore.</span><span class="sxs-lookup"><span data-stu-id="ec22c-115">Using this value results in an error.</span></span> |
| <span data-ttu-id="ec22c-116">DML_GRAPH_EDGE_TYPE_INPUT</span><span class="sxs-lookup"><span data-stu-id="ec22c-116">DML_GRAPH_EDGE_TYPE_INPUT</span></span> | <span data-ttu-id="ec22c-117">Specifica che il bordo del grafo è descritto dalla [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) struttura.</span><span class="sxs-lookup"><span data-stu-id="ec22c-117">Specifies that the graph edge is described by the [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) structure.</span></span> |
| <span data-ttu-id="ec22c-118">DML_GRAPH_EDGE_TYPE_OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec22c-118">DML_GRAPH_EDGE_TYPE_OUTPUT</span></span> | <span data-ttu-id="ec22c-119">Specifica che il bordo del grafo viene descritto dalla [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) struttura .</span><span class="sxs-lookup"><span data-stu-id="ec22c-119">Specifies that the graph edge is described by the [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) structure.</span></span> |
| <span data-ttu-id="ec22c-120">DML_GRAPH_EDGE_TYPE_INTERMEDIATE</span><span class="sxs-lookup"><span data-stu-id="ec22c-120">DML_GRAPH_EDGE_TYPE_INTERMEDIATE</span></span> | <span data-ttu-id="ec22c-121">Specifica che il bordo del grafo è descritto dalla [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) struttura.</span><span class="sxs-lookup"><span data-stu-id="ec22c-121">Specifies that the graph edge is described by the [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) structure.</span></span><br><br><span data-ttu-id="ec22c-122">Disponibilità ##</span><span class="sxs-lookup"><span data-stu-id="ec22c-122">## Availability</span></span><br><br><span data-ttu-id="ec22c-123">Questa API è stata introdotta nella versione di `1.1.0` DirectML.</span><span class="sxs-lookup"><span data-stu-id="ec22c-123">This API was introduced in DirectML version `1.1.0`.</span></span> |


## <a name="requirements"></a><span data-ttu-id="ec22c-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec22c-124">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ec22c-125">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="ec22c-125">**Header**</span></span> | <span data-ttu-id="ec22c-126">directml.h</span><span class="sxs-lookup"><span data-stu-id="ec22c-126">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="ec22c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec22c-127">See also</span></span>

* [<span data-ttu-id="ec22c-128">Metodo IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="ec22c-128">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="ec22c-129">DML_GRAPH_DESC struttura</span><span class="sxs-lookup"><span data-stu-id="ec22c-129">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)     
* [<span data-ttu-id="ec22c-130">DML_GRAPH_EDGE_DESC struttura</span><span class="sxs-lookup"><span data-stu-id="ec22c-130">DML_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_graph_edge_desc.md)
* [<span data-ttu-id="ec22c-131">DML_INPUT_GRAPH_EDGE_DESC struttura</span><span class="sxs-lookup"><span data-stu-id="ec22c-131">DML_INPUT_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_input_graph_edge_desc.md)
* [<span data-ttu-id="ec22c-132">DML_OUTPUT_GRAPH_EDGE_DESC struttura</span><span class="sxs-lookup"><span data-stu-id="ec22c-132">DML_OUTPUT_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_output_graph_edge_desc.md)
* [<span data-ttu-id="ec22c-133">DML_INTERMEDIATE_GRAPH_EDGE_DESC struttura</span><span class="sxs-lookup"><span data-stu-id="ec22c-133">DML_INTERMEDIATE_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_intermediate_graph_edge_desc.md)