---
UID: NS:directml.DML_GRAPH_NODE_DESC
title: DML_GRAPH_NODE_DESC
description: "Contenitore generico per un nodo all'interno di un grafico di operatori DirectML definiti da [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) e passati a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)."
helpviewer_keywords:
- DML_GRAPH_NODE_DESC
- DML_GRAPH_NODE_DESC structure
- direct3d12.dml_graph_node_desc
- directml/DML_GRAPH_NODE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_NODE_DESC, DML_GRAPH_NODE_DESC structure, direct3d12.dml_graph_node_desc, directml/DML_GRAPH_NODE_DESC
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
- DML_GRAPH_NODE_DESC
- directml/DML_GRAPH_NODE_DESC
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
- DML_GRAPH_NODE_DESC
ms.openlocfilehash: 8c79719f51efb4a59f9459a28765d3442ed3f4ee
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320406"
---
# <a name="dml_graph_node_desc-structure-directmlh"></a>Struttura DML_GRAPH_NODE_DESC (directml. h)
Contenitore generico per un nodo all'interno di un grafico di operatori DirectML definiti da [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) e passati a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintassi
```cpp
struct DML_GRAPH_NODE_DESC {
  DML_GRAPH_NODE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a>Members

`Type`

Tipo: **[DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md)**

Tipo di nodo del grafo. Vedere [DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md) per i tipi disponibili.


`Desc`

Tipo: \_ \_ Dimensione campo \_ ( \_ inesprimibile \_ ("dipendente dal tipo di nodo")) **const void \***

Puntatore alla descrizione del nodo Graph. Il tipo dello struct puntato deve corrispondere al valore specificato nel *tipo*.

## <a name="availability"></a>Disponibilità

Questa API è stata introdotta nella versione DirectML `1.1.0` .



## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |

## <a name="see-also"></a>Vedi anche

* [Metodo IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Struttura DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)