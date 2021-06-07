---
UID: NS:directml.DML_INTERMEDIATE_GRAPH_EDGE_DESC
title: DML_INTERMEDIATE_GRAPH_EDGE_DESC
description: Descrive una connessione all'interno di un grafo di operatori DirectML definiti da DML_GRAPH_DESC [e](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) passati a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Questa struttura viene usata per definire una connessione tra nodi interni.
helpviewer_keywords:
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
- DML_INTERMEDIATE_GRAPH_EDGE_DESC structure
- direct3d12.dml_intermediate_graph_edge_desc
- directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_INTERMEDIATE_GRAPH_EDGE_DESC, DML_INTERMEDIATE_GRAPH_EDGE_DESC structure, direct3d12.dml_intermediate_graph_edge_desc, directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
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
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
- directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
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
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
ms.openlocfilehash: 17cf62def075e84ba86e97a5adfa48fb452f475e
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417433"
---
# <a name="dml_intermediate_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="3ec8a-104">DML_INTERMEDIATE_GRAPH_EDGE_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="3ec8a-104">DML_INTERMEDIATE_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="3ec8a-105">Descrive una connessione all'interno di un grafo di operatori DirectML definiti da DML_GRAPH_DESC [e](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) passati a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="3ec8a-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="3ec8a-106">Questa struttura viene usata per definire una connessione tra nodi interni.</span><span class="sxs-lookup"><span data-stu-id="3ec8a-106">This structure is used to define a connection between internal nodes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ec8a-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="3ec8a-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="3ec8a-108">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="3ec8a-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ec8a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ec8a-109">Syntax</span></span>
```cpp
struct DML_INTERMEDIATE_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="3ec8a-110">Members</span><span class="sxs-lookup"><span data-stu-id="3ec8a-110">Members</span></span>

`FromNodeIndex`

<span data-ttu-id="3ec8a-111">Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ec8a-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="3ec8a-112">Indice del nodo del grafo da cui viene specificata una connessione a un altro nodo.</span><span class="sxs-lookup"><span data-stu-id="3ec8a-112">The index of the graph node from which a connection to another node is specified.</span></span>


`FromNodeOutputIndex`

<span data-ttu-id="3ec8a-113">Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ec8a-113">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="3ec8a-114">Indice dell'output nel nodo in corrispondenza dell'indice *FromNodeIndex* in cui è specificata la connessione.</span><span class="sxs-lookup"><span data-stu-id="3ec8a-114">The index of the output on the node at index *FromNodeIndex* where the connection is specified.</span></span>


`ToNodeIndex`

<span data-ttu-id="3ec8a-115">Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ec8a-115">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="3ec8a-116">Indice del nodo del grafo in cui viene specificata una connessione da un altro nodo.</span><span class="sxs-lookup"><span data-stu-id="3ec8a-116">The index of the graph node into which a connection from another node is specified.</span></span>


`ToNodeInputIndex`

<span data-ttu-id="3ec8a-117">Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ec8a-117">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="3ec8a-118">Indice dell'input nel nodo in corrispondenza dell'indice *ToNodeIndex* in cui è specificata la connessione.</span><span class="sxs-lookup"><span data-stu-id="3ec8a-118">The index of the input on the node at index *ToNodeIndex* where the connection is specified.</span></span>


`Name`

<span data-ttu-id="3ec8a-119">Tipo: \_ Campo \_ z \_ \_ Maybenull \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="3ec8a-119">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="3ec8a-120">Nome facoltativo per la connessione al grafo.</span><span class="sxs-lookup"><span data-stu-id="3ec8a-120">An optional name for the graph connection.</span></span> <span data-ttu-id="3ec8a-121">Se specificato, può essere usato all'interno di determinati messaggi di errore generati dal livello di debug DirectML.</span><span class="sxs-lookup"><span data-stu-id="3ec8a-121">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="3ec8a-122">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="3ec8a-122">Availability</span></span>

<span data-ttu-id="3ec8a-123">Questa API è stata introdotta in DirectML versione `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="3ec8a-123">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="3ec8a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ec8a-124">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3ec8a-125">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="3ec8a-125">**Header**</span></span> | <span data-ttu-id="3ec8a-126">directml.h</span><span class="sxs-lookup"><span data-stu-id="3ec8a-126">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="3ec8a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ec8a-127">See also</span></span>

* [<span data-ttu-id="3ec8a-128">Metodo IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="3ec8a-128">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="3ec8a-129">DML_GRAPH_DESC struttura</span><span class="sxs-lookup"><span data-stu-id="3ec8a-129">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="3ec8a-130">DML_GRAPH_EDGE_DESC struttura</span><span class="sxs-lookup"><span data-stu-id="3ec8a-130">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)