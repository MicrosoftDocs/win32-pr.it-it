---
UID: NE:directml.DML_GRAPH_EDGE_TYPE
title: DML_GRAPH_EDGE_TYPE
description: Definisce le costanti che specificano un tipo di bordo del grafo. Vedere [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) per l'utilizzo di questa enumerazione.
helpviewer_keywords:
- DML_GRAPH_EDGE_TYPE
- DML_GRAPH_EDGE_TYPE structure
- direct3d12.dml_graph_edge_type
- directml/DML_GRAPH_EDGE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_TYPE, DML_GRAPH_EDGE_TYPE structure, direct3d12.dml_graph_edge_type, directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
- directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
ms.openlocfilehash: d65649fcd2115cc7cdcc1b01da20ef44b0436e6f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417920"
---
# <a name="dml_graph_edge_type-enumeration-directmlh"></a>DML_GRAPH_EDGE_TYPE enumerazione (directml.h)

Definisce le costanti che specificano un tipo di bordo del grafo. Vedere [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) per l'utilizzo di questa enumerazione.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
typedef enum DML_GRAPH_EDGE_TYPE {
  DML_GRAPH_EDGE_TYPE_INVALID,
  DML_GRAPH_EDGE_TYPE_INPUT,
  DML_GRAPH_EDGE_TYPE_OUTPUT,
  DML_GRAPH_EDGE_TYPE_INTERMEDIATE
} ;
```

## <a name="constants"></a>Costanti

| Nome | Descrizione |
| ---- |:---- |
| DML_GRAPH_EDGE_TYPE_INVALID | Specifica un tipo di bordo del grafo sconosciuto e non è mai valido. L'uso di questo valore comporta un errore. |
| DML_GRAPH_EDGE_TYPE_INPUT | Specifica che il bordo del grafo è descritto dalla [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) struttura. |
| DML_GRAPH_EDGE_TYPE_OUTPUT | Specifica che il bordo del grafo viene descritto dalla [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) struttura . |
| DML_GRAPH_EDGE_TYPE_INTERMEDIATE | Specifica che il bordo del grafo è descritto dalla [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) struttura.<br><br>Disponibilità ##<br><br>Questa API è stata introdotta nella versione di `1.1.0` DirectML. |


## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |

## <a name="see-also"></a>Vedi anche

* [Metodo IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC struttura](./ns-directml-dml_graph_desc.md)     
* [DML_GRAPH_EDGE_DESC struttura](./ns-directml-dml_graph_edge_desc.md)
* [DML_INPUT_GRAPH_EDGE_DESC struttura](./ns-directml-dml_input_graph_edge_desc.md)
* [DML_OUTPUT_GRAPH_EDGE_DESC struttura](./ns-directml-dml_output_graph_edge_desc.md)
* [DML_INTERMEDIATE_GRAPH_EDGE_DESC struttura](./ns-directml-dml_intermediate_graph_edge_desc.md)