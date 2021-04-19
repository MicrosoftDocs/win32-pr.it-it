---
UID: NS:directml.DML_OPERATOR_GRAPH_NODE_DESC
title: DML_OPERATOR_GRAPH_NODE_DESC
description: "Descrive un nodo all'interno di un grafico di operatori DirectML definiti da [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) e passati a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)."
helpviewer_keywords:
- DML_OPERATOR_GRAPH_NODE_DESC
- DML_OPERATOR_GRAPH_NODE_DESC structure
- direct3d12.dml_operator_graph_node_desc
- directml/DML_OPERATOR_GRAPH_NODE_DESC
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
- DML_OPERATOR_GRAPH_NODE_DESC
- directml/DML_OPERATOR_GRAPH_NODE_DESC
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
- DML_OPERATOR_GRAPH_NODE_DESC
ms.openlocfilehash: 6081f81044ff2ce384f7906af9c6e80f6b06f774
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320363"
---
# <a name="dml_operator_graph_node_desc-structure-directmlh"></a><span data-ttu-id="6f8e9-103">Struttura DML_OPERATOR_GRAPH_NODE_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="6f8e9-103">DML_OPERATOR_GRAPH_NODE_DESC structure (directml.h)</span></span>
<span data-ttu-id="6f8e9-104">Descrive un nodo all'interno di un grafico di operatori DirectML definiti da [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) e passati a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="6f8e9-104">Decribes a node within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

<span data-ttu-id="6f8e9-105">Il comportamento di questo nodo è definito da un operatore DirectML.</span><span class="sxs-lookup"><span data-stu-id="6f8e9-105">The behavior of this node is defined by a DirectML operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f8e9-106">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="6f8e9-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="6f8e9-107">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="6f8e9-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f8e9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f8e9-108">Syntax</span></span>
```cpp
struct DML_OPERATOR_GRAPH_NODE_DESC {
  IDMLOperator *Operator;
  const char   *Name;
};
```



## <a name="members"></a><span data-ttu-id="6f8e9-109">Members</span><span class="sxs-lookup"><span data-stu-id="6f8e9-109">Members</span></span>

`Operator`

<span data-ttu-id="6f8e9-110">Tipo: <b> [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator)\*</b></span><span class="sxs-lookup"><span data-stu-id="6f8e9-110">Type: <b>[IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator)\*</b></span></span>

<span data-ttu-id="6f8e9-111">Operatore DirectML che definisce il comportamento del nodo.</span><span class="sxs-lookup"><span data-stu-id="6f8e9-111">A DirectML operator defining the behavior of the node.</span></span>


`Name`

<span data-ttu-id="6f8e9-112">Tipo: \_ Field \_ z \_ \_ MAYBENULL \_ **const \* char**</span><span class="sxs-lookup"><span data-stu-id="6f8e9-112">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="6f8e9-113">Nome facoltativo per la connessione Graph.</span><span class="sxs-lookup"><span data-stu-id="6f8e9-113">An optional name for the graph connection.</span></span> <span data-ttu-id="6f8e9-114">Se specificato, questo può essere usato in alcuni messaggi di errore generati dal livello di debug DirectML.</span><span class="sxs-lookup"><span data-stu-id="6f8e9-114">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="6f8e9-115">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="6f8e9-115">Availability</span></span>

<span data-ttu-id="6f8e9-116">Questa API è stata introdotta nella versione DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="6f8e9-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="6f8e9-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f8e9-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6f8e9-118">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="6f8e9-118">**Header**</span></span> | <span data-ttu-id="6f8e9-119">directml. h</span><span class="sxs-lookup"><span data-stu-id="6f8e9-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="6f8e9-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f8e9-120">See also</span></span>

* [<span data-ttu-id="6f8e9-121">Metodo IDMLDevice1:: CompileGraph</span><span class="sxs-lookup"><span data-stu-id="6f8e9-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="6f8e9-122">Struttura DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="6f8e9-122">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="6f8e9-123">Struttura DML_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="6f8e9-123">DML_GRAPH_NODE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_node_desc)