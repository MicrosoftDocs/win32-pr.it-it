---
UID: NS:directml.DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
title: DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
description: Sottrae ogni elemento di *BTensor* dall'elemento corrispondente di *ATensor,* moltiplica il risultato per se stesso e inserisce il risultato nell'elemento corrispondente di *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
ms.openlocfilehash: 3e3e7ab8f222f42def82a168ed861e58347f3b20
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804480"
---
# <a name="dml_element_wise_difference_square_operator_desc-directmlh"></a>DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC (directml.h)

Sottrae ogni elemento di *BTensor* dall'elemento corrispondente di *ATensor,* moltiplica il risultato per se stesso e inserisce il risultato nell'elemento corrispondente di *OutputTensor*.

```
f(a, b) = (a - b) * (a - b)
```

Questo operatore supporta l'esecuzione sul posto, ovvero *OutputTensor* è autorizzato ad aggiungere alias *ad ATensor* o *BTensor* durante l'associazione.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.5 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a>Members

`ATensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente gli input sul lato sinistro.

`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente gli input sul lato destro.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output in cui scrivere i risultati.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
*ATensor,* *BTensor* e *OutputTensor* devono avere gli stessi *datatype*, *DimensionCount* e *Sizes*.

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | Da 1 a 8 | FLOAT32, FLOAT16, INT32, UINT32 |
| BTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16, INT32, UINT32 |
| OutputTensor | Output | Da 1 a 8 | FLOAT32, FLOAT16, INT32, UINT32 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |
