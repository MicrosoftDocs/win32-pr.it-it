---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Copia l'intero tensore di input nell'output, quindi sovrascrive gli indici selezionati con i valori corrispondenti dal tensore degli aggiornamenti.
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_SCATTER_ND_OPERATOR_DESC
f1_keywords:
- DML_SCATTER_ND_OPERATOR_DESC
- directml/DML_SCATTER_ND_OPERATOR_DESC
ms.openlocfilehash: ae9a3022a7070bbf0253e71550f2ca1ceced6768
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320397"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a>Struttura DML_SCATTER_ND_OPERATOR_DESC (directml. h)
Copia l'intero tensore di input nell'output, quindi sovrascrive gli indici selezionati con i valori corrispondenti dal tensore degli aggiornamenti. Questo operatore esegue lo pseudocodice seguente, dove "..." rappresenta una serie di coordinate, con il comportamento esatto determinato dall'asse e dalle dimensioni degli indici.

```
output = input
output[indices[...]] = updates[...]
```

Se due indici di elementi di output si sovrappongono (che non è valido), non esiste alcuna garanzia di quale sia l'ultima scrittura WINS.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintassi
```cpp
struct DML_SCATTER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *UpdatesTensor;
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

Un tensore contenente gli indici. Il *DimensionCount* di questo tensore deve corrispondere a *InputTensor. DimensionCount*. L'ultima dimensione di *IndicesTensor* è in realtà il numero di coordinate per tupla dell'indice e non deve superare *InputTensor. DimensionCount*. Ad esempio, un tensore indici di dimensioni `{1,4,5,2}` con *IndicesDimensionCount* = 3 indica una matrice 4x5 di Tuple coordinate a 2 valori che indicizzano in *InputTensor*.

A partire da `DML_FEATURE_LEVEL_3_0` , questo operatore supporta valori di indice negativi quando si usa un tipo integrale con segno con questo tensore. Gli indici negativi vengono interpretati come relativi alla fine della rispettiva dimensione. Ad esempio, un indice di-1 si riferisce all'ultimo elemento lungo la dimensione.


`UpdatesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore contenente i nuovi valori per sostituire i valori di input esistenti in corrispondenza degli indici corrispondenti. Il *DimensionCount* di questo tensore deve corrispondere a *InputTensor. DimensionCount*. Il *UpdatesTensor. sizes* previsto è la concatenazione dei segmenti iniziali *IndicesTensor. sizes* e del segmento finale *InputTensor. sizes* per produrre quanto segue.

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

Le dimensioni sono allineate a destra, con 1 valori iniziali anteposti se necessario per soddisfare *UpdatesTensor. DimensionCount*.

Ecco un esempio.

```
InputTensor.Sizes = [3,4,5,6,7]
InputDimensionCount = 5
IndicesTensor.Sizes = [1,1, 1,2,3]
IndicesDimensionCount = 3 // can be thought of as a [1,2] array of 3-coordinate tuples

// The [1,2] comes from the indices tensor (ignoring last dimension, which is the tuple size),
// and the [6,7] comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
UpdatesTensor.Sizes = [1, 1,2,6,7]
```


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore in cui scrivere i risultati. Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere a *InputTensor. sizes*.


`InputDimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Il numero di dimensioni di input effettive all'interno di *InputTensor* dopo aver ignorato gli eventuali primitivi irrilevanti, che includono [1, *InputTensor. DimensionCount*). Ad esempio, dato *InputTensor. sizes* = {1,1,4,6} e *InputDimensionCount* = 3, gli indici significativi effettivi sono {1,4,6} .


`IndicesDimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Il numero di dimensioni effettive dell'indice all'interno di *IndicesTensor* dopo aver ignorato gli eventuali primitivi irrilevanti, che vanno da [1, *IndicesTensor. DimensionCount*). Ad esempio, dato *IndicesTensor. sizes* = {1,1,4,6} e *IndicesDimensionCount* = 3, gli indici significativi effettivi sono {1,4,6} .

## <a name="examples"></a>Esempio

```
InputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 2, 3, 4, 5, 6, 7, 8]

IndicesTensor: (Sizes:{4,1}, DataType:FLOAT32)
    [[4], [3], [1], [7]]

UpdatesTensor: (Sizes:{4}, DataType:FLOAT32)
    [9, 10, 11, 12]

// output = input
// output[indices[x, 0]] = updates[x]
OutputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 11, 3, 10, 9, 6, 7, 12]
```

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *IndicesTensor*, *InputTensor*, *OutputTensor* e `UpdatesTensor` devono avere lo stesso *DimensionCount*.
* *InputTensor*, *OutputTensor* e `UpdatesTensor` devono avere lo stesso *tipo* di dati.

## <a name="tensor-support"></a>Supporto tensore
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 e versioni successive
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Input | da 1 a 8 | INT64, INT32, UINT64, UINT32 |
| UpdatesTensor | Input | da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e versioni successive
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Input | 4 | UINT32 |
| UpdatesTensor | Input | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |