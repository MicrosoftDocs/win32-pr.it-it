---
UID: NE:directml.DML_DEPTH_SPACE_ORDER
title: DML_DEPTH_SPACE_ORDER
description: Definisce le costanti che controllano la trasformazione applicata negli operatori DirectML DML_OPERATOR_DEPTH_TO_SPACE1 [e](/windows/win32/api/directml/ne-directml-dml_operator_type) **DML_OPERATOR_SPACE_TO_DEPTH1**.
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_SPACE_ORDER
- directml/DML_DEPTH_SPACE_ORDER
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
- DML_DEPTH_SPACE_ORDER
ms.openlocfilehash: 009686adfc054c7b6344f01edafedaf2921693d5
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803537"
---
# <a name="dml_depth_space_order-enumeration-directmlh"></a>DML_DEPTH_SPACE_ORDER enumerazione (directml.h)

Definisce le costanti che controllano la trasformazione applicata negli operatori DirectML DML_OPERATOR_DEPTH_TO_SPACE1 [e](/windows/win32/api/directml/ne-directml-dml_operator_type) **DML_OPERATOR_SPACE_TO_DEPTH1**. Questi vengono usati all'interno [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) e [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) strutture.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
typedef enum DML_DEPTH_SPACE_ORDER {
  DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW,
  DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
} ;
```

## <a name="constants"></a>Costanti

| Nome | Descrizione |
| ---- |:---- |
| DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW | Fa sì che [](./ns-directml-dml_depth_to_space1_operator_desc.md) i tensori DML_DEPTH_TO_SPACE1_OPERATOR_DESC e [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) siano interpretati con i layout seguenti, in cui le dimensioni tra parentesi vengono appiattite insieme.<br><br>- **Versione di profondità:**[Batch, (BlockHeight, BlockWidth, Channels), Height, Width]<br>- **Versione spazio:**[Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)] |
| DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH | Fa sì che [](./ns-directml-dml_depth_to_space1_operator_desc.md) i tensori usati DML_DEPTH_TO_SPACE1_OPERATOR_DESC e [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) siano interpretati con i layout seguenti, in cui le dimensioni tra parentesi vengono appiattite insieme.<br><br>- **Versione di profondità:**[Batch, (Channels, BlockHeight, BlockWidth), Height, Width]<br>- **Versione spazio:**[Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)] |

## <a name="remarks"></a>Commenti

Vedere [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) e [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) per esempi che illustrano l'effetto di questi valori.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |

## <a name="see-also"></a>Vedi anche

* [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md)
* [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md)

## <a name="availability"></a>Disponibilità
Questa enumerazione è stata introdotta in `DML_FEATURE_LEVEL_2_1` .