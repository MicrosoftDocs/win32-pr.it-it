---
UID: NS:directml.DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
description: Calcola l'operatore OR bit per bit tra ogni elemento corrispondente dei tensori di input e scrive il risultato nel tensore di output.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
ms.openlocfilehash: 7138c6647e1bd4df5d8957468ca67f103f4a3f5a
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803216"
---
# <a name="dml_element_wise_bit_or_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC struttura (directml.h)

Calcola l'operatore OR bit per bit tra ogni elemento corrispondente dei tensori di input e scrive il risultato nel tensore di output.

Il tensore di input e output deve avere gli stessi *valori di DimensionCount,* *Sizes* e *DataType.*

Questo operatore supporta l'esecuzione sul posto, vale a dire che il tensore di output può creare un alias per uno o più tensori di input durante l'associazione.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi

```cpp
struct DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
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
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
*ATensor,* *BTensor* e *OutputTensor* devono avere gli stessi *valori di DataType,* *DimensionCount* e *Sizes.*

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | Da 1 a 8 | UINT32, UINT16, UINT8 |
| BTensor | Input | Da 1 a 8 | UINT32, UINT16, UINT8 |
| OutputTensor | Output | Da 1 a 8 | UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |