---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Seleziona gli elementi *K* più grandi o più piccoli da ogni sequenza lungo un asse di *InputTensor* e restituisce rispettivamente i valori e gli indici di tali elementi in *OutputValueTensor* e *OutputIndexTensor.*
helpviewer_keywords:
- DML_TOP_K1_OPERATOR_DESC
- DML_TOP_K1_OPERATOR_DESC structure
- direct3d12.dml_top_k1_operator_desc
- directml/DML_TOP_K1_OPERATOR_DESC
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
f1_keywords:
- DML_TOP_K1_OPERATOR_DESC
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
ms.openlocfilehash: 599541032e0f1711c0e747a4ca5906391849a932
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417635"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a>DML_TOP_K1_OPERATOR_DESC struttura (directml.h)
Seleziona gli elementi *K* più grandi o più piccoli da ogni sequenza lungo un asse di *InputTensor* e restituisce rispettivamente i valori e gli indici di tali elementi in *OutputValueTensor* e *OutputIndexTensor.* Una *sequenza* fa riferimento a uno dei set di elementi presenti lungo la *dimensione Asse* di *InputTensor*.

È possibile scegliere se selezionare gli elementi K più grandi o gli elementi K più piccoli usando *AxisDirection.*

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_TOP_K1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputValueTensor;
  const DML_TENSOR_DESC *OutputIndexTensor;
  UINT                  Axis;
  UINT                  K;
  DML_AXIS_DIRECTION    AxisDirection;
};
```

## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di input contenente gli elementi da selezionare.

`OutputValueTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output in cui scrivere i valori dei primi *elementi K.* Gli elementi *K principali* vengono selezionati in base al fatto che siano il più grande o il più piccolo, a seconda del valore di *AxisDirection.* Questo tensore deve avere dimensioni uguali a *InputTensor* *,* ad eccezione della dimensione specificata dal parametro *Axis,* che deve avere dimensioni uguali a *K*.

I *valori K* selezionati da ogni sequenza di input vengono sempre ordinati in senso decrescente (dal più grande al più piccolo) se *AxisDirection* è [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md). In caso contrario, il contrario è true e i valori selezionati vengono sempre ordinati in ordine crescente (dal più piccolo al più grande).

`OutputIndexTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output in cui scrivere gli indici dei primi *elementi K.* Questo tensore deve avere dimensioni uguali a *InputTensor* *,* ad eccezione della dimensione specificata dal parametro *Axis,* che deve avere dimensioni uguali a *K*.

Gli indici restituiti in questo tensore vengono misurati rispetto all'inizio della sequenza (anziché all'inizio del tensore). Ad esempio, un indice 0 fa sempre riferimento al primo elemento per tutte le sequenze in un asse.

Nei casi in cui due o più elementi nella parte superiore K hanno lo stesso valore ,ovvero quando è presente un'aezione, vengono inclusi gli indici di entrambi gli elementi e viene garantito l'ordinamento in base all'indice crescente degli elementi. Si noti che questo è vero indipendentemente dal valore di *AxisDirection*.

`Axis`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Indice della dimensione in cui selezionare gli elementi. Questo valore deve essere minore di *DimensionCount* di *InputTensor*.

`K`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di elementi da selezionare. *K* deve essere maggiore di 0, ma minore del numero di elementi in *InputTensor* lungo la dimensione specificata da *Axis*.

`AxisDirection`

Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Valore [dell'enumerazione DML_AXIS_DIRECTION.](./ne-directml-dml_axis_direction.md) Se impostato su **DML_AXIS_DIRECTION_INCREASING**, questo operatore restituisce gli *elementi* K più *piccoli* in ordine di valore crescente. In caso contrario, restituisce gli *elementi* K *più grandi* in ordine decrescente.

## <a name="examples"></a>Esempi

### <a name="example-1"></a>Esempio 1

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 3
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
[[[[11, 10],
   [ 9,  8],
   [ 7,  6]]]]

OutputIndexTensor: (Sizes:{1,1,3,2}, DataType:UINT32)
[[[[3, 2],
   [2, 3],
   [3, 2]]]]
```

### <a name="example-2-using-a-different-axis"></a>Esempio 2. Uso di un asse diverso

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 2
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[[[ 4,  5, 10, 11],
   [ 3,  2,  9,  8]]]]

OutputIndexTensor: (Sizes:{1,1,2,4}, DataType:UINT32)
[[[[2, 2, 0, 0],
   [1, 1, 1, 1]]]]
```

### <a name="example-3-tied-values"></a>Esempio 3. Valori associati

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[3, 2, 2],
   [5, 5, 4],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[3, 1, 2],
   [2, 3, 1],
   [0, 1, 2]]]]
```

### <a name="example-4-increasing-axis-direction"></a>Esempio 4. Aumento della direzione dell'asse

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[1, 2, 2],
   [3, 4, 5],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[0, 1, 2],
   [0, 1, 2],
   [0, 1, 2]]]]
```


## <a name="remarks"></a>Commenti
Quando *AxisDirection è* impostato su [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), questo operatore equivale a [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore

* *InputTensor,* *OutputIndexTensor* e *OutputValueTensor* devono avere lo stesso *dimensioncount.*
* *InputTensor* e *OutputValueTensor* devono avere lo stesso *Tipo di dati*.

## <a name="tensor-support"></a>Supporto di Tensor

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 e successive

| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputValueTensor | Output | Da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputIndexTensor | Output | Da 1 a 8 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e successive

| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputValueTensor | Output | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputIndexTensor | Output | 4 | UINT32 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |
