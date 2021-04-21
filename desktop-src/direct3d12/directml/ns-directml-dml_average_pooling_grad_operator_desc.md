---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per il pooling medio (vedere [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: 5c2803fc300ca862d54a74aee1c864e9097e3d8e
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803356"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a>DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC struttura (directml.h)

Calcola le sfumature di backpropagation per il pooling medio (vedere [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).

Si consideri un DML_AVERAGE_POOLING_OPERATOR_DESC 2x2, senza spaziatura interna e uno stride di 1, che esegue le operazioni seguenti.

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

Ogni finestra 2x2 nel tensore di input viene mediata per produrre un elemento dell'output (lettura degli zeri per gli elementi oltre il bordo). Di seguito è riportato un esempio dell'output **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** parametri simili.

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

Si noti che i valori in *OutputGradientTensor* rappresentano i contributi ponderati di [](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) tale elemento a *OutputTensor* durante l'operatore DML_AVERAGE_POOLING_OPERATOR_DESC originale.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a>Members

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore sfumatura in ingresso. Questa operazione viene in genere ottenuta dall'output della retropropagazione di un livello precedente. In genere questo tensore avrebbe le stesse dimensioni *dell'output* del [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) nel passaggio in avanti.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output contenente le sfumature di backpropagated. In genere questo tensore avrebbe le stesse dimensioni *dell'input* del [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) nel passaggio in avanti.

`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di elementi nelle *matrici Strides,* *WindowSize,* *StartPadding* *ed EndPadding.* Questo valore deve essere uguale al conteggio delle dimensioni spaziali. Il numero di dimensioni spaziali è 2 se vengono forniti tensori 4D o 3 se vengono forniti tensori 5D.

`Strides`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

Vedere *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`WindowSize`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

Vedere *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`StartPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

Vedere *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`EndPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

Vedere *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`IncludePadding`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

Vedere *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputGradientTensor* e *OutputGradientTensor* devono avere gli stessi *DataType* *e DimensionCount*.

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Input | Da 4 a 5 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | Da 4 a 5 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |