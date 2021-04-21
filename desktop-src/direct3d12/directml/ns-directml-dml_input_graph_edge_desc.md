---
UID: NS:directml.DML_INPUT_GRAPH_EDGE_DESC
title: DML_INPUT_GRAPH_EDGE_DESC
description: Descrive una connessione all'interno di un grafo di operatori DirectML definiti DML_GRAPH_DESC [e](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) passati a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Questa struttura viene usata per definire una connessione da un input grafico a un input di un nodo interno.
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
ms.openlocfilehash: 00fcece76f4cb7ac46589914df4d74321d957fbc
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802889"
---
# <a name="dml_input_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="0db8b-104">DML_INPUT_GRAPH_EDGE_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="0db8b-104">DML_INPUT_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="0db8b-105">Descrive una connessione all'interno di un grafo di operatori DirectML definiti DML_GRAPH_DESC [e](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) passati a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="0db8b-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="0db8b-106">Questa struttura viene usata per definire una connessione da un input grafico a un input di un nodo interno.</span><span class="sxs-lookup"><span data-stu-id="0db8b-106">This structure is used to define a connection from a graph input to an input of an internal node.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0db8b-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="0db8b-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="0db8b-108">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="0db8b-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0db8b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0db8b-109">Syntax</span></span>
```cpp
struct DML_INPUT_GRAPH_EDGE_DESC {
  UINT       GraphInputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="0db8b-110">Members</span><span class="sxs-lookup"><span data-stu-id="0db8b-110">Members</span></span>

`GraphInputIndex`

<span data-ttu-id="0db8b-111">Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0db8b-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="0db8b-112">Indice dell'input del grafo da cui viene specificata una connessione a un input del nodo interno.</span><span class="sxs-lookup"><span data-stu-id="0db8b-112">The index of the graph input from which a connection to an internal node input is specified.</span></span>


`ToNodeIndex`

<span data-ttu-id="0db8b-113">Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0db8b-113">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="0db8b-114">Indice del nodo interno in cui viene specificata la connessione dall'input del grafo.</span><span class="sxs-lookup"><span data-stu-id="0db8b-114">The index of the internal node onto which the connection from the graph input is specified.</span></span>


`ToNodeInputIndex`

<span data-ttu-id="0db8b-115">Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0db8b-115">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="0db8b-116">Indice dell'input nel nodo interno in cui è specificata la connessione.</span><span class="sxs-lookup"><span data-stu-id="0db8b-116">The index of the input on the internal node where the connection is specified.</span></span>


`Name`

<span data-ttu-id="0db8b-117">Tipo: \_ Campo \_ z \_ \_ Maybenull \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="0db8b-117">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="0db8b-118">Nome facoltativo per la connessione al grafo.</span><span class="sxs-lookup"><span data-stu-id="0db8b-118">An optional name for the graph connection.</span></span> <span data-ttu-id="0db8b-119">Se specificato, può essere usato all'interno di determinati messaggi di errore generati dal livello di debug DirectML.</span><span class="sxs-lookup"><span data-stu-id="0db8b-119">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="0db8b-120">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="0db8b-120">Availability</span></span>

<span data-ttu-id="0db8b-121">Questa API è stata introdotta in DirectML versione `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="0db8b-121">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="0db8b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0db8b-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0db8b-123">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="0db8b-123">**Header**</span></span> | <span data-ttu-id="0db8b-124">directml.h</span><span class="sxs-lookup"><span data-stu-id="0db8b-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="0db8b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0db8b-125">See also</span></span>

* [<span data-ttu-id="0db8b-126">Metodo IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="0db8b-126">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="0db8b-127">DML_GRAPH_DESC struttura</span><span class="sxs-lookup"><span data-stu-id="0db8b-127">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="0db8b-128">DML_GRAPH_EDGE_DESC struttura</span><span class="sxs-lookup"><span data-stu-id="0db8b-128">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)