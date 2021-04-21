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
# <a name="dml_output_graph_edge_desc-structure-directmlh"></a>DML_OUTPUT_GRAPH_EDGE_DESC struttura (directml.h)
Descrive una connessione all'interno di un grafo di operatori DirectML definiti da DML_GRAPH_DESC [e](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) passati a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Questa struttura viene usata per definire una connessione da un output di un nodo interno a un output grafico.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_OUTPUT_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       GraphOutputIndex;
  const char *Name;
};
```



## <a name="members"></a>Members

`FromNodeIndex`




`FromNodeOutputIndex`




`GraphOutputIndex`

Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**

Indice dell'output del grafo a cui viene specificata una connessione da un output del nodo interno.


`Name`

Tipo: \_ Campo \_ z \_ \_ Maybenull \_ **const char \***

Nome facoltativo per la connessione al grafo. Se specificato, può essere usato all'interno di determinati messaggi di errore generati dal livello di debug DirectML.

## <a name="availability"></a>Disponibilità

Questa API è stata introdotta in DirectML versione `1.1.0` .



## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |

## <a name="see-also"></a>Vedi anche

* [Metodo IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC struttura](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [DML_GRAPH_EDGE_DESC struttura](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)