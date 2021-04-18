---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: Inverte gli elementi di una o più *sottosequenze* di un tensore. Il set di sottosequenze da invertire viene scelto in base all'asse e alle lunghezze della sequenza specificati.
helpviewer_keywords:
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure
- direct3d12.dml_reverse_subsequences_operator_desc
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.openlocfilehash: 5baf16c5acd1ce5c5f44e68420e93aabaa276ea7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320400"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a>Struttura DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC (directml. h)
Inverte gli elementi di una o più *sottosequenze* di un tensore. Il set di sottosequenze da invertire viene scelto in base all'asse e alle lunghezze della sequenza specificati.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintassi
```cpp
struct DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *SequenceLengthsTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Il tensore di input contenente gli elementi da invertire.


`SequenceLengthsTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore contenente un valore per ogni sottosequenza da invertire, che indica la lunghezza in elementi della sottosequenza. Solo gli elementi all'interno della lunghezza della sottosequenza vengono invertiti; gli elementi rimanenti lungo tale asse vengono copiati nell'output senza modifiche.

Questo tensore deve avere un numero di dimensioni e dimensioni uguali a *InputTensor*, *ad eccezione* della dimensione specificata dal parametro *Axis* . La dimensione della dimensione dell' *asse* deve essere 1. Se, ad esempio, il *InputTensor* ha dimensioni di `{2,3,4,5}` e *Axis* è 1, le dimensioni di *SequenceLengthsTensor* devono essere `{2,1,4,5}` .

Se la lunghezza di una sottosequenza supera il numero massimo di elementi lungo tale asse, questo operatore si comporta come se il valore fosse stato fissato al massimo.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output in cui scrivere i risultati. Questo tensore deve avere le stesse dimensioni e il tipo di dati di *InputTensor*.


`Axis`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Indice della dimensione su cui invertire gli elementi. Questo valore deve essere minore del valore di DimensionCount di *InputTensor*.

## <a name="examples"></a>Esempi

### <a name="example-1"></a>Esempio 1

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,3,1}, DataType:UINT32)
[[[[2],
   [4],
   [3]]]]

Axis: 3

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  4],
   [ 8,  7,  6,  5],
   [11, 10,  9, 12]]]]
```

### <a name="example-2-reversing-along-a-different-axis"></a>Esempio 2. Inversione lungo un asse diverso

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,1,4}, DataType:UINT32)
[[[[2, 3, 1, 0]]]]

Axis: 2

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[5, 10,  3,  4], // Notice that sequence lengths of 1 and 0 are effective nops
   [1,  6,  7,  8],
   [9,  2, 11, 12]]]]
```

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *InputTensor*, *OutputTensor* e *SequenceLengthsTensor* devono avere lo stesso *DimensionCount*.
* *InputTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati.

## <a name="tensor-support"></a>Supporto tensore
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 e versioni successive
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | da 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| SequenceLengthsTensor | Input | da 4 a 5 | UINT32 |
| OutputTensor | Output | da 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e versioni successive
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| SequenceLengthsTensor | Input | 4 | UINT32 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |