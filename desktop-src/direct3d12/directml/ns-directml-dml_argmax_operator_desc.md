---
UID: NS:directml.DML_ARGMAX_OPERATOR_DESC
title: DML_ARGMAX_OPERATOR_DESC
description: Restituisce gli indici degli elementi con valori massimi all'interno di una o più dimensioni del tensore di input.
helpviewer_keywords:
- DML_ARGMAX_OPERATOR_DESC
- DML_ARGMAX_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMAX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMAX_OPERATOR_DESC, DML_ARGMAX_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
- directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
ms.openlocfilehash: 4c2852c3d301a12d318c5e3006b26830c6eaa6e1
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417776"
---
# <a name="dml_argmax_operator_desc-structure-directmlh"></a>DML_ARGMAX_OPERATOR_DESC struttura (directml.h)

Restituisce gli indici degli elementi con valori massimi all'interno di una o più dimensioni del tensore di input.

Ogni elemento di output è il risultato dell'applicazione di *una riduzione argmax* su un subset del tensore di input. La *funzione argmax* restituisce l'indice dell'elemento con valori massimi all'interno di un set di elementi di input. Gli elementi di input coinvolti in ogni riduzione sono determinati dagli assi di input forniti. Analogamente, ogni indice di output è rispetto agli assi di input forniti. Se vengono specificati tutti gli assi di input, l'operatore applica una singola *riduzione argmax* e produce un singolo elemento di output.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_ARGMAX_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore da cui leggere.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore in cui scrivere i risultati. Ogni elemento di output è il risultato di *una riduzione argmax* su un subset di elementi da *InputTensor.* 

- *DimensionCount deve* corrispondere a *InputTensor.DimensionCount* (viene mantenuta la classificazione del tensore di input).
- *Le* dimensioni devono corrispondere *a InputTensor.Sizes*, ad eccezione delle dimensioni incluse negli assi *ridotti,* che devono essere di dimensioni 1.

`AxisCount`

Tipo: **[UINT](../../winprog/windows-data-types.md)**

Numero di assi da ridurre. Questo campo determina le dimensioni della *matrice Axes.*

`Axes`

Tipo: \_ Field_size \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \***

Assi lungo i quali eseguire la riduzione. I valori devono essere nell'intervallo `[0, InputTensor.DimensionCount - 1]` .

`AxisDirection`

Tipo: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**

Determina l'indice da selezionare quando più elementi di input hanno lo stesso valore.
- **DML_AXIS_DIRECTION_INCREASING** restituisce l'indice del primo elemento con valori massimi (ad esempio, `argmax({3,2,1,2,3}) = 0` )
- **DML_AXIS_DIRECTION_DECREASING** restituisce l'indice dell'ultimo elemento con valori massimi (ad esempio, `argmax({3,2,1,2,3}) = 4` )

## <a name="examples"></a>Esempio

Gli esempi in questa sezione usano tutti questo stesso tensore di input bidimensionale.

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmax-to-columns"></a>Esempio 1. Applicazione di *argmax* alle colonne

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[1,  // argmax({1, 3, 2})
  2,  // argmax({2, 0, 5})
  1]] // argmax({3, 4, 2})
```

### <a name="example-2-applying-argmax-to-rows"></a>Esempio 2. Applicazione di *argmax* alle righe

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[2], // argmax({1, 2, 3})
 [2], // argmax({3, 0, 4})
 [1]] // argmax({2, 5, 2})
```

### <a name="example-3-applying-argmax-to-all-axes-the-entire-tensor"></a>Esempio 3. Applicazione di *argmax* a tutti gli assi (l'intero tensore)

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[7]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a>Commenti
Le dimensioni del tensore di output devono corrispondere alle dimensioni del tensore di input, ad eccezione degli assi ridotti, che devono essere 1.

Quando *AxisDirection è* [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), questa API equivale a DML_REDUCE_OPERATOR_DESC [con](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).

Un subset di questa funzionalità viene esposto tramite l'operatore [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) ed è supportato nei livelli di funzionalità DirectML precedenti.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputTensor* e *OutputTensor* devono avere lo stesso *dimensionCount*.

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | Da 1 a 8 | INT64, INT32, UINT64, UINT32 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |