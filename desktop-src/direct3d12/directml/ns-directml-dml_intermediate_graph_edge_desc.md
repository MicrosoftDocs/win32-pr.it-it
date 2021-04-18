---
UID: NS:directml.DML_INTERMEDIATE_GRAPH_EDGE_DESC
title: DML_INTERMEDIATE_GRAPH_EDGE_DESC
description: "Descrive una connessione all'interno di un grafico di operatori DirectML definiti da [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) e passati a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Questa struttura viene utilizzata per definire una connessione tra nodi interni."
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
ms.openlocfilehash: 55b8385d3d8b6247681dd7078a04d8f5e196abd7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320405"
---
# <a name="dml_intermediate_graph_edge_desc-structure-directmlh"></a>Struttura DML_INTERMEDIATE_GRAPH_EDGE_DESC (directml. h)
Descrive una connessione all'interno di un grafico di operatori DirectML definiti da [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) e passati a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Questa struttura viene utilizzata per definire una connessione tra nodi interni.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintassi
```cpp
struct DML_INTERMEDIATE_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a>Members

`FromNodeIndex`

Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**

Indice del nodo grafico da cui viene specificata una connessione a un altro nodo.


`FromNodeOutputIndex`

Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**

Indice dell'output nel nodo in corrispondenza dell'indice *FromNodeIndex* in cui è specificata la connessione.


`ToNodeIndex`

Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**

Indice del nodo Graph in cui viene specificata una connessione da un altro nodo.


`ToNodeInputIndex`

Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**

Indice dell'input nel nodo in corrispondenza dell'indice *ToNodeIndex* in cui è specificata la connessione.


`Name`

Tipo: \_ Field \_ z \_ \_ MAYBENULL \_ **const \* char**

Nome facoltativo per la connessione Graph. Se specificato, questo può essere usato in alcuni messaggi di errore generati dal livello di debug DirectML.

## <a name="availability"></a>Disponibilità

Questa API è stata introdotta nella versione DirectML `1.1.0` .



## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |

## <a name="see-also"></a>Vedi anche

* [Metodo IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Struttura DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [Struttura DML_GRAPH_EDGE_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)