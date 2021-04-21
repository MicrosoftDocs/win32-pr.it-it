---
UID: NS:directml.DML_OPERATOR_GRAPH_NODE_DESC
title: DML_OPERATOR_GRAPH_NODE_DESC
description: Decrittografa un nodo all'interno di un grafico di operatori DirectML definiti da [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) e passati a [IDMLDevice1::CompileGraph.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
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
ms.openlocfilehash: 997f441de76a60229b76f2f7d67b7acf1a26ed5f
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803562"
---
# <a name="dml_operator_graph_node_desc-structure-directmlh"></a>DML_OPERATOR_GRAPH_NODE_DESC struttura (directml.h)
Decrittografa un nodo all'interno di un grafico di operatori DirectML definiti da [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) e passati a [IDMLDevice1::CompileGraph.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)

Il comportamento di questo nodo è definito da un operatore DirectML.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_OPERATOR_GRAPH_NODE_DESC {
  IDMLOperator *Operator;
  const char   *Name;
};
```



## <a name="members"></a>Members

`Operator`

Tipo: <b> [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator)*</b>

Operatore DirectML che definisce il comportamento del nodo.


`Name`

Tipo: \_ Campo \_ z \_ \_ Maybenull \_ **const char \***

Nome facoltativo per la connessione al grafo. Se specificato, può essere usato all'interno di determinati messaggi di errore generati dal livello di debug DirectML.

## <a name="availability"></a>Disponibilità

Questa API è stata introdotta nella versione di `1.1.0` DirectML.



## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |

## <a name="see-also"></a>Vedi anche

* [Metodo IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC struttura](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [DML_GRAPH_NODE_DESC struttura](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_node_desc)