---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per Slice (vedere [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
helpviewer_keywords:
- DML_SLICE_GRAD_OPERATOR_DESC
- DML_SLICE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_SLICE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_SLICE_GRAD_OPERATOR_DESC, DML_SLICE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
- directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
ms.openlocfilehash: a22efe9b0b74f5fdc7b498b97784086f40f243b9
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803972"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a>DML_SLICE_GRAD_OPERATOR_DESC struttura (directml.h)

Calcola le sfumature di backpropagation per Slice (vedere [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).

Tenere presente [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) estrae una sottoarea di un tensore di input. Dato un *InputGradientTensor* con le stesse dimensioni *dell'output* di un **DML_SLICE1_OPERATOR_DESC equivalente,** questo operatore produce un *OutputGradientTensor* con le stesse dimensioni dell'input di **DML_SLICE1_OPERATOR_DESC**.  Gli elementi sezionati vengono propagati all'output e tutti gli altri elementi vengono impostati su 0.

Si consideri ad esempio un **DML_SLICE1_OPERATOR_DESC** che estrae gli elementi seguenti da un tensore:

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

Se si specificano gli stessi stride di dimensioni di *InputWindowOffsets* dell'esempio precedente, questo /  /  operatore eseguirà la trasformazione seguente.

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi

```cpp
struct DML_SLICE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* InputWindowOffsets;
  _Field_size_(DimensionCount) const UINT* InputWindowSizes;
  _Field_size_(DimensionCount) const INT* InputWindowStrides;
};
```

## <a name="members"></a>Members

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore sfumatura in ingresso. Questa operazione viene in genere ottenuta dall'output della backpropagazione di un livello precedente. In genere, questo tensore avrebbe le stesse dimensioni *dell'output* dell'DML_SLICE1_OPERATOR_DESC [corrispondente](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) nel passaggio in avanti.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output contenente le sfumature di backpropagated. In genere, questo tensore avrebbe le stesse dimensioni *dell'input* del valore [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) nel passaggio in avanti.

`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di elementi nelle matrici *InputWindowOffsets,* *InputWindowSizes* e *InputWindowStrides.* Questo valore deve essere uguale *a DimensionCount* specificato in *InputGradientTensor* e *OutputGradientTensor*.

`InputWindowOffsets`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Vedere *InputWindowOffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

`InputWindowSizes`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Vedere *InputWindowSizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

`InputWindowStrides`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Vedere *InputWindowStrides* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

A differenza **di DML_SLICE1_OPERATOR_DESC**, questo operatore richiede passi diversi da zero. Questo perché con uno zero stride è ambiguo su quale elemento di input deve essere mappato a ogni elemento di output e pertanto non è possibile eseguire la backpropagation. Come **DML_SLICE1_OPERATOR_DESC**, gli stride negativi capovolgeno la direzione della finestra di input lungo tale asse.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputGradientTensor* e *OutputGradientTensor* devono avere gli stessi *DataType* *e DimensionCount*.

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputGradientTensor | Output | Da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |