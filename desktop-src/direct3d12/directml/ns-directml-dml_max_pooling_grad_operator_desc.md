---
UID: NS:directml.DML_MAX_POOLING_GRAD_OPERATOR_DESC
title: DML_MAX_POOLING_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per il pooling massimo (vedere [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).
helpviewer_keywords:
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- DML_MAX_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_MAX_POOLING_GRAD_OPERATOR_DESC, DML_MAX_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: 3b0b10fa8ee17c9d06e779c3c990f134bc4ae669
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803431"
---
# <a name="dml_max_pooling_grad_operator_desc-structure-directmlh"></a>DML_MAX_POOLING_GRAD_OPERATOR_DESC struttura (directml.h)

Calcola le sfumature di backpropagation per il pooling massimo (vedere [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).

Si consideri un **DML_MAX_POOLING2_OPERATOR_DESC** 2x2 senza spaziatura interna o dilazioni e uno stride di 1, che esegue le operazioni seguenti.

```
InputTensor             OutputTensor    IndicesTensor
[[1, 2, 3],   MaxPool    [[4, 4],        [[4, 4],
 [2, 4, 2],     -->       [6, 7]]         [7, 8]]
 [5, 6, 7]]
```

L'elemento più grande di ogni finestra 2x2 nel tensore di input produce un elemento dell'output. Di seguito è riportato un esempio dell'output **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, dati parametri simili.

```
InputTensor   InputGradientTensor            OutputGradientTensor
[[1, 2, 3],       [[1, 2],     MaxPoolGrad   [[0, 0, 0],
 [2, 4, 2],        [4, 5]]         -->        [0, 3, 0],
 [5, 6, 7]]                                   [0, 4, 5]]
```

In effetti, questo operatore usa *InputTensor* per determinare l'indice dell'elemento più grande da ogni finestra e distribuisce i valori di *InputGradientTensor* in *OutputGradientTensor* in base a questi indici. Se gli indici si sovrappongono, i valori vengono sommati. Qualsiasi elemento di output senza riferimenti viene azzerato.

Nel caso di un oggetto tie (in cui più di un elemento in una finestra ha lo stesso valore massimo), viene scelto l'elemento con l'indice logico di elemento più basso.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi

```cpp
struct DML_MAX_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  _Field_size_(DimensionCount) const UINT* Dilations;
};
```

## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore della funzionalità di input. Si tratta in genere dello stesso tensore fornito da *InputTensor* per DML_MAX_POOLING2_OPERATOR_DESC [nel](./ns-directml-dml_max_pooling2_operator_desc.md) passaggio in avanti.

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore sfumatura in ingresso. Questa operazione viene in genere ottenuta dall'output della retropropagazione di un livello precedente. In genere questo tensore avrebbe le stesse dimensioni *dell'output* del [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) corrispondente nel passaggio in avanti.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output contenente le sfumature backpropagate. In genere, questo tensore ha le stesse dimensioni *dell'input* del [parametro](./ns-directml-dml_max_pooling2_operator_desc.md) DML_MAX_POOLING2_OPERATOR_DESC nel passaggio in avanti.

`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di elementi nelle matrici *Strides,* *WindowSize,* *StartPadding,* *EndPadding* e *Dilations.* Questo valore deve essere uguale al numero di dimensioni spaziali (DimensionCount - 2 di InputTensor). Poiché questo operatore supporta solo tensori 4D, l'unico valore valido per questo parametro è 2.

`Strides`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Vedere *Strides* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`WindowSize`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Vedere *WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`StartPadding`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Vedere *StartPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`EndPadding`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Vedere *EndPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`Dilations`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Vedere *Dilazioni* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *InputTensor* e *OutputGradientTensor* devono avere le stesse *dimensioni*.
* *InputGradientTensor,* *InputTensor* e *OutputGradientTensor* devono avere lo stesso *tipo di dati*.

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Dimensioni | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | { BatchCount, ChannelCount, InputHeight, InputWidth } | 4 | FLOAT32, FLOAT16 |
| InputGradientTensor | Input | { BatchCount, ChannelCount, OutputHeight, OutputWidth } | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | { BatchCount, ChannelCount, InputHeight, InputWidth } | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |