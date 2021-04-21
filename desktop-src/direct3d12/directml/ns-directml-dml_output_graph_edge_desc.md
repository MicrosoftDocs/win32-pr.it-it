---
UID: NS:directml.DML_OUTPUT_GRAPH_EDGE_DESC
title: DML_OUTPUT_GRAPH_EDGE_DESC
description: Descrive una connessione all'interno di un grafo di operatori DirectML definiti DML_GRAPH_DESC [e](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) passati a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Questa struttura viene usata per definire una connessione da un output di un nodo interno a un output grafico.
helpviewer_keywords:
- DML_OUTPUT_GRAPH_EDGE_DESC
- DML_OUTPUT_GRAPH_EDGE_DESC structure
- direct3d12.dml_output_graph_edge_desc
- directml/DML_OUTPUT_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/05/2020
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
- DML_OUTPUT_GRAPH_EDGE_DESC
- directml/DML_OUTPUT_GRAPH_EDGE_DESC
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
- DML_OUTPUT_GRAPH_EDGE_DESC
ms.openlocfilehash: 55d234fcf487e7ad92b39b60d43eb992b46d0d2c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803932"
---
# <a name="dml_output_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="f15ea-104">DML_OUTPUT_GRAPH_EDGE_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="f15ea-104">DML_OUTPUT_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="f15ea-105">Descrive una connessione all'interno di un grafo di operatori DirectML definiti da DML_GRAPH_DESC [e](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) passati a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="f15ea-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="f15ea-106">Questa struttura viene usata per definire una connessione da un output di un nodo interno a un output grafico.</span><span class="sxs-lookup"><span data-stu-id="f15ea-106">This structure is used to define a connection from an output of an internal node to a graph output.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f15ea-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="f15ea-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f15ea-108">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="f15ea-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f15ea-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f15ea-109">Syntax</span></span>
```cpp
struct DML_OUTPUT_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       GraphOutputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="f15ea-110">Members</span><span class="sxs-lookup"><span data-stu-id="f15ea-110">Members</span></span>

`FromNodeIndex`




`FromNodeOutputIndex`




`GraphOutputIndex`

<span data-ttu-id="f15ea-111">Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f15ea-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="f15ea-112">Indice dell'output del grafo a cui viene specificata una connessione da un output del nodo interno.</span><span class="sxs-lookup"><span data-stu-id="f15ea-112">The index of the graph output to which a connection from an internal node output is specified.</span></span>


`Name`

<span data-ttu-id="f15ea-113">Tipo: \_ Campo \_ z \_ \_ Maybenull \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="f15ea-113">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="f15ea-114">Nome facoltativo per la connessione al grafo.</span><span class="sxs-lookup"><span data-stu-id="f15ea-114">An optional name for the graph connection.</span></span> <span data-ttu-id="f15ea-115">Se specificato, può essere usato all'interno di determinati messaggi di errore generati dal livello di debug DirectML.</span><span class="sxs-lookup"><span data-stu-id="f15ea-115">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="f15ea-116">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="f15ea-116">Availability</span></span>

<span data-ttu-id="f15ea-117">Questa API è stata introdotta in DirectML versione `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="f15ea-117">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="f15ea-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f15ea-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f15ea-119">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="f15ea-119">**Header**</span></span> | <span data-ttu-id="f15ea-120">directml.h</span><span class="sxs-lookup"><span data-stu-id="f15ea-120">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="f15ea-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f15ea-121">See also</span></span>

* [<span data-ttu-id="f15ea-122">Metodo IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="f15ea-122">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="f15ea-123">DML_GRAPH_DESC struttura</span><span class="sxs-lookup"><span data-stu-id="f15ea-123">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="f15ea-124">DML_GRAPH_EDGE_DESC struttura</span><span class="sxs-lookup"><span data-stu-id="f15ea-124">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)