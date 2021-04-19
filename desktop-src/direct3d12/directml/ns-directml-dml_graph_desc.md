---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Descrive un grafico degli operatori DirectML usati per compilare un operatore combinato e ottimizzato.
helpviewer_keywords:
- DML_GRAPH_DESC
- DML_GRAPH_DESC structure
- direct3d12.dml_graph_desc
- directml/DML_GRAPH_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_DESC, DML_GRAPH_DESC structure, direct3d12.dml_graph_desc, directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
- directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
ms.openlocfilehash: e72209d19bb26524576783becbbfbf94566d8370
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320374"
---
# <a name="dml_graph_desc-structure-directmlh"></a>Struttura DML_GRAPH_DESC (directml. h)

Descrive un grafico degli operatori DirectML usati per compilare un operatore combinato e ottimizzato. Vedere [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintassi
```cpp
struct DML_GRAPH_DESC {
  UINT                      InputCount;
  UINT                      OutputCount;
  UINT                      NodeCount;
  const DML_GRAPH_NODE_DESC *Nodes;
  UINT                      InputEdgeCount;
  const DML_GRAPH_EDGE_DESC *InputEdges;
  UINT                      OutputEdgeCount;
  const DML_GRAPH_EDGE_DESC *OutputEdges;
  UINT                      IntermediateEdgeCount;
  const DML_GRAPH_EDGE_DESC *IntermediateEdges;
};
```



## <a name="members"></a>Members

`InputCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Numero di input del grafico complessivo. Ogni input del grafo può essere connesso a un numero variabile di nodi interni, pertanto può essere diverso da *InputEdgeCount*.


`OutputCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Numero di output del grafico complessivo. Ogni output del grafo può essere connesso a un numero variabile di nodi interni, pertanto può essere diverso da *OutputEdgeCount*.


`NodeCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Numero di nodi interni nel grafico.


`Nodes`

Tipo: \_ \_ Dimensione campo \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***

Nodi interni nel grafico.


`InputEdgeCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Numero di connessioni tra input e input del grafo dei nodi interni nel grafico.


`InputEdges`

Tipo: \_ \_ Dimensione campo \_ (InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Matrice di connessioni tra input del grafo e input di nodi interni nel grafico. Il campo *tipo* all'interno di ogni elemento deve essere impostato su [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).


`OutputEdgeCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Il numero di connessioni tra output del grafo e output dei nodi interni nel grafico.


`OutputEdges`

Tipo: \_ \_ Dimensione campo \_ (OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Matrice di connessioni tra output del grafo e output dei nodi interni nel grafico. Il campo *tipo* all'interno di ogni elemento deve essere impostato su [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).


`IntermediateEdgeCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Numero di connessioni interne tra i nodi del grafico.


`IntermediateEdges`

Tipo: \_ \_ Dimensione campo \_ (IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Matrice di connessioni tra input e output dei nodi interni nel grafico. Il campo tipo all'interno di ogni elemento deve essere impostato su [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)


## <a name="remarks"></a>Commenti
Il grafo descritto da questa struttura deve essere un grafico aciclici diretto. È necessario definire una connessione per l'input e l'output di ogni nodo fornito, eccetto gli input e gli output facoltativi per l'operatore associato.

I nodi possono utilizzare operatori creati utilizzando il flag di [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) per determinati input. Tutti gli input dell'operatore che usano questo flag devono essere connessi agli input del grafo. Tutti gli input dell'operatore connessi allo stesso input del grafo devono usare o omettere questo flag in modo equivalente.

È possibile connettere gli operatori i cui input e output connessi utilizzano conteggi di dimensione, dimensioni e tipi di dati diversi. Questo implica che il BLOB di dati del tensore viene interpretato in modo diverso da ogni operatore. Tuttavia, il campo *TotalTensorSizeInBytes* di input e output del tensore connesso deve essere identico. Gli operatori devono leggere solo le aree di i tensori scritti dagli operatori precedenti. Le aree di riempimento nell'output di un'operazione (risultante dall'uso di stride) non sono necessariamente lette come zero dagli operatori di flusso inattivo.

## <a name="availability"></a>Disponibilità

Questa API è stata introdotta nella versione DirectML `1.1.0` .


## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |

## <a name="see-also"></a>Vedi anche

* [Metodo IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Struct DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md)
* [Struct DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)