---
UID: NS:directml.DML_GATHER_ND1_OPERATOR_DESC
title: DML_GATHER_ND1_OPERATOR_DESC
description: Raccoglie gli elementi dal tensore di input, usando il tensore indici per eseguire il mapping degli indici a interi sottoblocchi dell'input. | DML_GATHER_ND1_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND1_OPERATOR_DESC
- DML_GATHER_ND1_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_GATHER_ND1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_GATHER_ND1_OPERATOR_DESC, DML_GATHER_ND1_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
- directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
ms.openlocfilehash: dc7f33f50fa6a0c1cd2850b8e02aad30d75afeb1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321868"
---
# <a name="dml_gather_nd1_operator_desc-structure-directmlh"></a>Struttura DML_GATHER_ND1_OPERATOR_DESC (directml. h)

Raccoglie gli elementi dal tensore di input, usando il tensore indici per eseguire il mapping degli indici a interi sottoblocchi dell'input. Questo operatore esegue lo pseudocodice seguente, dove "..." rappresenta una serie di coordinate, con il comportamento esatto dipendente dal conteggio delle dimensioni del batch, dell'input e degli indici.

```
output[batch, ...] = input[batch, indices[batch, ...], ...]
```

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintassi

```cpp
struct DML_GATHER_ND1_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* IndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT InputDimensionCount;
  UINT IndicesDimensionCount;
  UINT BatchDimensionCount;
};
```

## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore da cui leggere.

`IndicesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Il tensore contenente gli indici. Il *DimensionCount* di questo tensore deve corrispondere a *InputTensor. DimensionCount*. L'ultima dimensione di *IndicesTensor* è in realtà il numero di coordinate per tupla dell'indice e non può superare *InputTensor. DimensionCount*. Ad esempio, un tensore indici di *dimensioni* `{1,4,5,2}` con *IndicesDimensionCount* = 3 indica una matrice 4x5 di tuple a 2 Coordinate che indicizzano in *InputTensor*.

A partire da `DML_FEATURE_LEVEL_3_0` , questo operatore supporta valori di indice negativi quando si usa un tipo integrale con segno con questo tensore. Gli indici negativi vengono interpretati come relativi alla fine della rispettiva dimensione. Ad esempio, un indice di-1 si riferisce all'ultimo elemento lungo la dimensione.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore in cui scrivere i risultati. Il *DimensionCount* e il *tipo* di dati di questo tensore devono corrispondere a *InputTensor. DimensionCount*. Il *OutputTensor. sizes* previsto è la concatenazione dei segmenti iniziali *IndicesTensor. sizes* e del segmento finale *InputTensor. sizes* , che produce quanto segue.

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

Le dimensioni sono allineate a destra, con 1 valori iniziali anteposti se necessario per soddisfare *OutputTensor. DimensionCount*.

Ecco un esempio.

```
InputTensor.Sizes = {3,4,5,6,7}
InputDimensionCount = 5
IndicesTensor.Sizes = {1,1, 1,2,3}
IndicesDimensionCount = 3 // can be thought of as a {1,2} array of 3-coordinate tuples

// The {1,2} comes from the indices tensor (ignoring last dimension which is the tuple size),
// and the {6,7} comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
OutputTensor.Sizes = {1, 1,2,6,7}
```

`InputDimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Il numero di dimensioni di input effettive all'interno di *InputTensor* dopo aver ignorato gli eventuali valori iniziali irrilevanti `[1, *InputTensor.DimensionCount*]` . Ad esempio, dato *InputTensor. sizes*  =  `{1,1,4,6}` e `InputDimensionCount` = 3, gli indici significativi effettivi sono `{1,4,6}` .

`IndicesDimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Il numero di dimensioni effettive dell'indice all'interno di *IndicesTensor* dopo aver ignorato gli eventuali primitivi irrilevanti, che vanno da [1, *IndicesTensor. DimensionCount*]. Ad esempio, dato *IndicesTensor. sizes*  =  `{1,1,4,6}` e *IndicesDimensionCount* = 3, gli indici significativi effettivi sono `{1,4,6}` .

`BatchDimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Il numero di dimensioni all'interno di ogni tensore (*InputTensor*, *IndicesTensor*, *OutputTensor*) che sono considerati batch indipendenti, compresi tra [0, *InputTensor. DimensionCount*) e [0, *IndicesTensor. DimensionCount*). Il numero di batch può essere 0, che implica un singolo batch. Ad esempio, date *IndicesTensor. sizes*  =  `{1,3,4,5,6,7}` e *IndicesDimensionCount* = 5 e `BatchDimensionCount` = 2, sono presenti batch `{3,4}` e indici significativi `{5,6,7}` .

## <a name="remarks"></a>Commenti
**DML_GATHER_ND1_OPERATOR_DESC** aggiunge *BatchDimensionCount* ed è equivalente a [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) quando *BatchDimensionCount* = 0.

## <a name="examples"></a>Esempi

### <a name="example-1-1d-remapping"></a>Esempio 1. 1D (nuovo mapping)

```
InputDimensionCount: 2
IndicesDimensionCount: 2
BatchDimensionCount: 0

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping-with-batch-count"></a>Esempio 2. rimappatura 2D con conteggio batch

```
InputDimensionCount: 3
IndicesDimensionCount: 3
BatchDimensionCount: 1

// 3 batches.
InputTensor: (Sizes:{1, 3,2,2}, DataType:FLOAT32)
    [
        [[[0,1],[2,3]],   // batch 0
         [[4,5],[6,7]],   // batch 1
         [[8,9],[10,11]]] // batch 2
    ]

// A 3x2 array of 2D tuples indexing into InputTensor.
// e.g. a tuple of <1,0> in batch 1 corresponds to input value 6.
IndicesTensor: (Sizes:{1, 3,2,2}, DataType:UINT32)
    [
        [[[0,0],[1,1]],
         [[1,1],[0,0]],
         [[0,1],[1,0]]]
    ]

// output[batch, x] = input[batch, indices[batch, x, 0], indices[batch, x, 1]]
OutputTensor: (Sizes:{1,1, 3,2}, DataType:FLOAT32)
    [[
        [[0,3],
         [7,4],
         [9,10]]
    ]]
```

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *IndicesTensor*, *InputTensor* e *OutputTensor* devono avere lo stesso *DimensionCount*.
* *InputTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati.

## <a name="tensor-support"></a>Supporto tensore
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Input | da 1 a 8 | INT64, INT32, UINT64, UINT32 |
| OutputTensor | Output | da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |
