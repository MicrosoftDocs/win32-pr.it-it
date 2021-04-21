---
UID: NS:directml.DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
title: DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
description: Moltiplica gli elementi di un tensore lungo un asse, scrivendo il numero di esecuzione del prodotto nel tensore di output.
helpviewer_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC structure
- direct3d12.dml_cumulative_product_operator_desc
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.openlocfilehash: 2f0c6a6b6f12792a245027a7f8e86c05f7e85192
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804518"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a>DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)

Moltiplica gli elementi di un tensore lungo un asse, scrivendo il numero di esecuzione del prodotto nel tensore di output.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.5 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* OutputTensor;
    UINT Axis;
    DML_AXIS_DIRECTION AxisDirection;
    BOOL HasExclusiveProduct;
};
```

## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati di input. Si tratta in genere dello stesso tensore fornito *dall'inputTensor* DML_BATCH_NORMALIZATION_OPERATOR_DESC [**nel**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passaggio in avanti.

Tensore di input contenente gli elementi da moltiplicare.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output in cui scrivere i prodotti cumulativi risultanti. Questo tensore deve avere le stesse dimensioni e tipo di dati di *InputTensor*.

`Axis`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Indice della dimensione su cui moltiplicare gli elementi. Questo valore deve essere minore di *DimensionCount* di *InputTensor*.

`AxisDirection`

Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Uno dei valori dell'enumerazione [DML_AXIS_DIRECTION.](./ne-directml-dml_axis_direction.md) Se impostato su **DML_AXIS_DIRECTION_INCREASING**, il prodotto si verifica attraversando il tensore lungo l'asse specificato tramite l'indice dell'elemento crescente. Se impostato su **DML_AXIS_DIRECTION_DECREASING**, il contrario è true e il prodotto si verifica scorrendo gli elementi in base all'indice decrescente.

`HasExclusiveProduct`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

Se **TRUE,** il valore dell'elemento corrente viene escluso durante la scrittura del numero di esecuzione nel tensore di output. Se **FALSE,** il valore dell'elemento corrente viene incluso nel numero in esecuzione.

## <a name="examples"></a>Esempio

Gli esempi in questa sezione usano tutti questo stesso tensore di input.

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a>Esempio 1. Prodotto cumulativo tra sliver orizzontali

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a>Esempio 2. Prodotti esclusivi

*L'impostazione di HasExclusiveProduct* su **TRUE** ha l'effetto di escludere il valore dell'elemento corrente dal totale in esecuzione durante la scrittura nel tensore di output.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a>Esempio 3. Direzione asse

*L'impostazione di AxisDirection* [**su DML_AXIS_DIRECTION_DECREASING**](/windows/win32/direct3d12/directml/ne-directml-dml_axis_direction) ha l'effetto di invertire l'ordine di attraversamento degli elementi durante il calcolo del numero di esecuzione.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a>Esempio 4. Moltiplicazione lungo un asse diverso

In questo esempio il prodotto si verifica verticalmente, lungo l'asse dell'altezza (seconda dimensione).

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a>Commenti
Questo operatore supporta l'esecuzione sul posto, vale a dire che il tensore di output è autorizzato a creare un alias *di InputTensor durante* l'associazione.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputTensor* e *OutputTensor* devono avere gli stessi *valori di DataType* *e Sizes.*

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |
