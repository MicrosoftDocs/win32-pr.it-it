---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Raccoglie gli elementi dal tensore di input, usando il tensore indici per eseguire il mapping degli indici a interi sottoblocchi dell'input. | DML_GATHER_ND_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND_OPERATOR_DESC
- DML_GATHER_ND_OPERATOR_DESC structure
- direct3d12.dml_gather_nd_operator_desc
- directml/DML_GATHER_ND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/31/2020
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
- DML_GATHER_ND_OPERATOR_DESC
- directml/DML_GATHER_ND_OPERATOR_DESC
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
- DML_GATHER_ND_OPERATOR_DESC
ms.openlocfilehash: 6a48fd19621bed100a13412dbb1992974d125323
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321867"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a>Struttura DML_GATHER_ND_OPERATOR_DESC (directml. h)

Raccoglie gli elementi dal tensore di input, usando il tensore indici per eseguire il mapping degli indici a interi sottoblocchi dell'input. Questo operatore esegue lo pseudocodice seguente, dove "..." rappresenta una serie di coordinate, con il comportamento esatto dipendente dal conteggio delle dimensioni di input e indici.

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintassi
```cpp
struct DML_GATHER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
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

Tensore in cui scrivere i risultati. Il *DimensionCount* e il *tipo* di dati di questo tensore devono corrispondere a *InputTensor. DimensionCount*. Il *OutputTensor. sizes* previsto è la concatenazione dei segmenti iniziali *IndicesTensor. sizes* e del segmento finale *InputTensor. sizes* da produrre:

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

Le dimensioni di output sono allineate a destra, con 1 valori iniziali anteposti, se necessario, per soddisfare fino a *OutputTensor. DimensionCount*.

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

## <a name="examples"></a>Esempi

### <a name="example-1-1d-remapping"></a>Esempio 1. 1D (nuovo mapping)

```
InputDimensionCount: 2
IndicesDimensionCount: 2

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping"></a>Esempio 2. rimappatura 2D

```
InputDimensionCount: 3
IndicesDimensionCount: 2

InputTensor: (Sizes:{1, 2,2,2}, DataType:FLOAT32)
    [ [[[0,1],[2,3]],[[4,5],[6,7]]] ]

IndicesTensor: (Sizes:{1,1, 2,2}, DataType:UINT32)
    [[ [[0,1],[1,0]] ]]

// output[y, x] = input[indices[y, 0], indices[y, 1], x]
OutputTensor: (Sizes:{1,1, 2,2}, DataType:FLOAT32)
    [[ [[2,3],[4,5]] ]]
```


## <a name="remarks"></a>Commenti
Una versione più recente di questo operatore, `DML_OPERATOR_GATHER_ND1` , è stata introdotta in `DML_FEATURE_LEVEL_3_0` .

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *IndicesTensor*, *InputTensor* e *OutputTensor* devono avere lo stesso *DimensionCount*.
* *InputTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati.

## <a name="tensor-support"></a>Supporto tensore
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 e versioni successive
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Input | da 1 a 8 | INT64, INT32, UINT64, UINT32 |
| OutputTensor | Output | da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e versioni successive
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Input | 4 | UINT32 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |
