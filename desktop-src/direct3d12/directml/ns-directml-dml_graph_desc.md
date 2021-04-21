---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Descrive un grafico degli operatori DirectML usati per compilare un operatore combinato ottimizzato.
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
ms.openlocfilehash: a42996fc9fd7825e13232b245ab764c6439f9489
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802875"
---
# <a name="dml_graph_desc-structure-directmlh"></a>DML_GRAPH_DESC struttura (directml.h)

Descrive un grafico degli operatori DirectML usati per compilare un operatore combinato ottimizzato. Vedere [IDMLDevice1::CompileGraph.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

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

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di input del grafico complessivo. Ogni input del grafo può essere connesso a un numero variabile di nodi interni, pertanto può essere diverso da *InputEdgeCount.*


`OutputCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di output del grafico complessivo. Ogni output del grafo può essere connesso a un numero variabile di nodi interni, pertanto può essere diverso da *OutputEdgeCount.*


`NodeCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di nodi interni nel grafico.


`Nodes`

Tipo: \_ Dimensione \_ campo \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***

Nodi interni nel grafico.


`InputEdgeCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di connessioni tra gli input del grafo e gli input dei nodi interni nel grafico.


`InputEdges`

Tipo: \_ Dimensione \_ campo \_ (InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Matrice di connessioni tra gli input del grafo e gli input dei nodi interni nel grafico. Il *campo Tipo* all'interno di ogni elemento deve essere impostato su [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).


`OutputEdgeCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di connessioni tra gli output del grafo e gli output dei nodi interni nel grafico.


`OutputEdges`

Tipo: \_ Dimensione \_ campo \_ (OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Matrice di connessioni tra gli output del grafo e gli output dei nodi interni nel grafo. Il *campo Tipo* all'interno di ogni elemento deve essere impostato su [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).


`IntermediateEdgeCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di connessioni interne tra i nodi nel grafico.


`IntermediateEdges`

Tipo: \_ Dimensione \_ campo \_ (IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Matrice di connessioni tra input e output di nodi interni nel grafico. Il campo Tipo all'interno di ogni elemento deve essere impostato [su DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)


## <a name="remarks"></a>Commenti
Il grafo descritto da questa struttura deve essere un grafo aciclico diretto. È necessario definire una connessione per l'input e l'output di ogni nodo fornito, ad eccezione degli input e degli output facoltativi per l'operatore associato.

I nodi possono usare operatori creati usando il flag [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) per determinati input. Qualsiasi input dell'operatore che usa questo flag deve essere connesso agli input del grafico. Tutti gli input dell'operatore connessi allo stesso input del grafo devono usare o omettere questo flag in modo equivalente.

È legale connettere operatori i cui input e output connessi usano conteggi, dimensioni e tipi di dati diversi per le dimensioni. Ciò implica che il BLOB di dati tensor viene interpretato in modo diverso da ogni operatore. Il *campo TotalTensorSizeInBytes* degli input e degli output del tensore connesso deve tuttavia essere identico. Gli operatori devono leggere solo le aree dei tensori scritti dagli operatori precedenti. Non è garantito che le aree di riempimento nell'output di un'operazione (derivanti dall'uso di stride) siano lette come zero dagli operatori down stream.

## <a name="availability"></a>Disponibilità

Questa API è stata introdotta nella versione di `1.1.0` DirectML.


## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |

## <a name="see-also"></a>Vedi anche

* [Metodo IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_NODE_DESC struct](./ns-directml-dml_graph_node_desc.md)
* [DML_GRAPH_EDGE_DESC struct](./ns-directml-dml_graph_edge_desc.md)