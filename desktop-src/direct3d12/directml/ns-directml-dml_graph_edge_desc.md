---
UID: NS:directml.DML_GRAPH_EDGE_DESC
title: DML_GRAPH_EDGE_DESC
description: Contenitore generico per una connessione all'interno di un grafico di operatori DirectML definiti da [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) e passati a [IDMLDevice1::CompileGraph.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
helpviewer_keywords:
- DML_GRAPH_EDGE_DESC
- DML_GRAPH_EDGE_DESC structure
- direct3d12.dml_graph_edge_desc
- directml/DML_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_DESC, DML_GRAPH_EDGE_DESC structure, direct3d12.dml_graph_edge_desc, directml/DML_GRAPH_EDGE_DESC
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
- DML_GRAPH_EDGE_DESC
- directml/DML_GRAPH_EDGE_DESC
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
- DML_GRAPH_EDGE_DESC
ms.openlocfilehash: 58cdf22dd85b1464d68cf1db75ff47a34817514c
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417792"
---
# <a name="dml_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="cc694-103">DML_GRAPH_EDGE_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="cc694-103">DML_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="cc694-104">Contenitore generico per una connessione all'interno di un grafico di operatori DirectML definiti da [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) e passati a [IDMLDevice1::CompileGraph.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="cc694-104">A generic container for a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc694-105">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="cc694-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="cc694-106">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="cc694-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc694-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc694-107">Syntax</span></span>
```cpp
struct DML_GRAPH_EDGE_DESC {
  DML_GRAPH_EDGE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a><span data-ttu-id="cc694-108">Members</span><span class="sxs-lookup"><span data-stu-id="cc694-108">Members</span></span>

`Type`

<span data-ttu-id="cc694-109">Tipo: **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**</span><span class="sxs-lookup"><span data-stu-id="cc694-109">Type: **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**</span></span>

<span data-ttu-id="cc694-110">Tipo di bordo del grafo.</span><span class="sxs-lookup"><span data-stu-id="cc694-110">The type of graph edge.</span></span> <span data-ttu-id="cc694-111">Vedere [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) per i tipi disponibili e [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) dove usare ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="cc694-111">See [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) for available types, and [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) for where to use each type.</span></span>


`Desc`

<span data-ttu-id="cc694-112">Tipo: \_ Dimensione del campo ( \_ \_ \_ inespressibile \_ ("Dipendente dal tipo di bordo")) **const void \***</span><span class="sxs-lookup"><span data-stu-id="cc694-112">Type: \_Field\_size\_(\_Inexpressible\_("Dependent on edge type")) **const void\***</span></span>

<span data-ttu-id="cc694-113">Puntatore alla descrizione del bordo del grafo.</span><span class="sxs-lookup"><span data-stu-id="cc694-113">A pointer to the graph edge description.</span></span> <span data-ttu-id="cc694-114">Il tipo dello struct a cui si punta deve corrispondere al valore specificato in *Tipo*.</span><span class="sxs-lookup"><span data-stu-id="cc694-114">The type of the pointed-to struct must match the value specified in *Type*.</span></span>

## <a name="availability"></a><span data-ttu-id="cc694-115">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="cc694-115">Availability</span></span>

<span data-ttu-id="cc694-116">Questa API è stata introdotta nella versione di `1.1.0` DirectML.</span><span class="sxs-lookup"><span data-stu-id="cc694-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="cc694-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc694-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cc694-118">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="cc694-118">**Header**</span></span> | <span data-ttu-id="cc694-119">directml.h</span><span class="sxs-lookup"><span data-stu-id="cc694-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="cc694-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc694-120">See also</span></span>

* [<span data-ttu-id="cc694-121">Metodo IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="cc694-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="cc694-122">DML_GRAPH_DESC struttura</span><span class="sxs-lookup"><span data-stu-id="cc694-122">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)