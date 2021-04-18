---
UID: NS:directml.DML_MAX_POOLING_GRAD_OPERATOR_DESC
title: DML_MAX_POOLING_GRAD_OPERATOR_DESC
description: Calcola le sfumature di propagazione per il pool massimo (vedere [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).
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
ms.openlocfilehash: b7314cb6b9456d9ac9f99e90100085e86f88ffd9
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320852"
---
# <a name="dml_max_pooling_grad_operator_desc-structure-directmlh"></a>Struttura DML_MAX_POOLING_GRAD_OPERATOR_DESC (directml. h)

Calcola le sfumature di propagazione per il pool massimo (vedere [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).

Si consideri un **DML_MAX_POOLING2_OPERATOR_DESC** 2x2 senza spaziatura o dilatazioni e un stride di 1, che esegue le operazioni seguenti.

```
InputTensor             OutputTensor    IndicesTensor
[[1, 2, 3],   MaxPool    [[4, 4],        [[4, 4],
 [2, 4, 2],     -->       [6, 7]]         [7, 8]]
 [5, 6, 7]]
```

L'elemento più grande di ogni finestra 2x2 nel tensore di input produce un elemento dell'output. Di seguito è riportato un esempio dell'output di **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, in base a parametri simili.

```
InputTensor   InputGradientTensor            OutputGradientTensor
[[1, 2, 3],       [[1, 2],     MaxPoolGrad   [[0, 0, 0],
 [2, 4, 2],        [4, 5]]         -->        [0, 3, 0],
 [5, 6, 7]]                                   [0, 4, 5]]
```

In effetti, questo operatore usa *InputTensor* per determinare l'indice dell'elemento più grande da ogni finestra e distribuisce i valori di *InputGradientTensor* in *OutputGradientTensor* in base a questi indici. Quando gli indici si sovrappongono, i valori vengono sommati. Tutti gli elementi di output senza riferimenti vengono azzerati.

Nel caso di un tie (dove più di un elemento in una finestra ha lo stesso valore massimo), viene scelto l'elemento con l'indice dell'elemento logico più basso.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

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

Tensore della funzionalità di input. Si tratta in genere dello stesso tensore fornito come *InputTensor* per [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) nel passaggio successivo.

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di sfumatura in ingresso. Questa operazione viene in genere ottenuta dall'output di propagation di un livello precedente. In genere, questo tensore avrebbe le stesse dimensioni dell' *output* del [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) corrispondente nel passaggio successivo.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore di output contenente le sfumature ripropagate. In genere, questo tensore avrebbe le stesse dimensioni dell' *input* del [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) corrispondente nel passaggio successivo.

`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Il numero di elementi nelle matrici *Strides*, *WindowSize*, *StartPadding*, *EndPadding* e *dilatations* . Questo valore deve essere uguale al numero di dimensioni spaziali (InputTensor DimensionCount-2). Poiché questo operatore supporta solo i tensori 4D, l'unico valore valido per questo parametro è 2.

`Strides`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Vedere *stride* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`WindowSize`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Vedere *WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`StartPadding`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Vedere *StartPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`EndPadding`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Vedere *EndPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`Dilations`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Vedere le *dilatazioni* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *InputTensor* e *OutputGradientTensor* devono avere le stesse *dimensioni*.
* *InputGradientTensor*, *InputTensor* e *OutputGradientTensor* devono avere lo stesso *tipo* di dati.

## <a name="tensor-support"></a>Supporto tensore
| Tensore | Tipo | Dimensioni | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | {BatchCount, ChannelCount, InputHeight, InputWidth} | 4 | FLOAT32, FLOAT16 |
| InputGradientTensor | Input | {BatchCount, ChannelCount, OutputHeight, OutputWidth} | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | {BatchCount, ChannelCount, InputHeight, InputWidth} | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |