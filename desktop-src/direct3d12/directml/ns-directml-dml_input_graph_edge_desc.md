---
UID: NS:directml.DML_INPUT_GRAPH_EDGE_DESC
title: DML_INPUT_GRAPH_EDGE_DESC
description: "Descrive una connessione all'interno di un grafico di operatori DirectML definiti da [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) e passati a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Questa struttura viene utilizzata per definire una connessione da un input del grafo a un input di un nodo interno."
helpviewer_keywords:
- DML_INPUT_GRAPH_EDGE_DESC
- DML_INPUT_GRAPH_EDGE_DESC structure
- direct3d12.dml_input_graph_edge_desc
- directml/DML_INPUT_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_INPUT_GRAPH_EDGE_DESC, DML_INPUT_GRAPH_EDGE_DESC structure, direct3d12.dml_input_graph_edge_desc, directml/DML_INPUT_GRAPH_EDGE_DESC
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
- DML_INPUT_GRAPH_EDGE_DESC
- directml/DML_INPUT_GRAPH_EDGE_DESC
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
- DML_INPUT_GRAPH_EDGE_DESC
ms.openlocfilehash: 180bfc89a37aad2ba0b6f287c302aa30b0b04110
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320371"
---
# <a name="dml_input_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="03735-104">Struttura DML_INPUT_GRAPH_EDGE_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="03735-104">DML_INPUT_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="03735-105">Descrive una connessione all'interno di un grafico di operatori DirectML definiti da [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) e passati a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="03735-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="03735-106">Questa struttura viene utilizzata per definire una connessione da un input del grafo a un input di un nodo interno.</span><span class="sxs-lookup"><span data-stu-id="03735-106">This structure is used to define a connection from a graph input to an input of an internal node.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03735-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="03735-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="03735-108">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="03735-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="03735-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03735-109">Syntax</span></span>
```cpp
struct DML_INPUT_GRAPH_EDGE_DESC {
  UINT       GraphInputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="03735-110">Members</span><span class="sxs-lookup"><span data-stu-id="03735-110">Members</span></span>

`GraphInputIndex`

<span data-ttu-id="03735-111">Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="03735-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="03735-112">Indice dell'input del grafico da cui viene specificata una connessione a un input del nodo interno.</span><span class="sxs-lookup"><span data-stu-id="03735-112">The index of the graph input from which a connection to an internal node input is specified.</span></span>


`ToNodeIndex`

<span data-ttu-id="03735-113">Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="03735-113">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="03735-114">Indice del nodo interno su cui è specificata la connessione dall'input del grafo.</span><span class="sxs-lookup"><span data-stu-id="03735-114">The index of the internal node onto which the connection from the graph input is specified.</span></span>


`ToNodeInputIndex`

<span data-ttu-id="03735-115">Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="03735-115">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="03735-116">Indice dell'input sul nodo interno in cui è specificata la connessione.</span><span class="sxs-lookup"><span data-stu-id="03735-116">The index of the input on the internal node where the connection is specified.</span></span>


`Name`

<span data-ttu-id="03735-117">Tipo: \_ Field \_ z \_ \_ MAYBENULL \_ **const \* char**</span><span class="sxs-lookup"><span data-stu-id="03735-117">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="03735-118">Nome facoltativo per la connessione Graph.</span><span class="sxs-lookup"><span data-stu-id="03735-118">An optional name for the graph connection.</span></span> <span data-ttu-id="03735-119">Se specificato, questo può essere usato in alcuni messaggi di errore generati dal livello di debug DirectML.</span><span class="sxs-lookup"><span data-stu-id="03735-119">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="03735-120">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="03735-120">Availability</span></span>

<span data-ttu-id="03735-121">Questa API è stata introdotta nella versione DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="03735-121">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="03735-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03735-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="03735-123">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="03735-123">**Header**</span></span> | <span data-ttu-id="03735-124">directml. h</span><span class="sxs-lookup"><span data-stu-id="03735-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="03735-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03735-125">See also</span></span>

* [<span data-ttu-id="03735-126">Metodo IDMLDevice1:: CompileGraph</span><span class="sxs-lookup"><span data-stu-id="03735-126">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="03735-127">Struttura DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="03735-127">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="03735-128">Struttura DML_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="03735-128">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)