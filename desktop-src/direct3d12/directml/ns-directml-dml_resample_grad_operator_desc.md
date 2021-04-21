---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per Resample (vedere [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
helpviewer_keywords:
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- DML_RESAMPLE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RESAMPLE_GRAD_OPERATOR_DESC, DML_RESAMPLE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.openlocfilehash: 0caba1a560b72a94ed04cacd824414964af82c35
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804045"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a>DML_RESAMPLE_GRAD_OPERATOR_DESC struttura (directml.h)

Calcola le sfumature di backpropagation per Resample (vedere [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).

**DML_RESAMPLE1_OPERATOR_DESC** ridimensiona dimensioni arbitrarie del tensore di input usando il campionamento del vicino più prossimo o l'interpolazione bilineare. Dato un *InputGradientTensor* con le stesse dimensioni *dell'output* di un **DML_RESAMPLE1_OPERATOR_DESC equivalente,** questo operatore produce un *OutputGradientTensor* con le stesse dimensioni dell'input del **DML_RESAMPLE1_OPERATOR_DESC**. 

Si consideri ad esempio un **DML_RESAMPLE1_OPERATOR_DESC** che esegue un ridimensionamento del vicino più vicino di 1,5x nella larghezza e 0,5x nell'altezza.

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

Si noti che il primo elemento del tensore di input (con valore 1) contribuisce a due elementi nell'output, il primo elemento (con valore 2) contribuisce a un elemento nell'output e il secondo e il terzo elemento (con i valori 3 e 4) non contribuiscono a nessun elemento dell'output.

**L'DML_RESAMPLE_GRAD_OPERATOR_DESC** esegue le operazioni seguenti.

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

Si noti che i valori in *OutputGradientTensor* rappresentano i contributi ponderati di  tale elemento a *OutputTensor* durante l'operatore DML_RESAMPLE1_OPERATOR_DESC originale.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi

```cpp
struct DML_RESAMPLE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const FLOAT* Scales;
  _Field_size_(DimensionCount) const FLOAT* InputPixelOffsets;
  _Field_size_(DimensionCount) const FLOAT* OutputPixelOffsets;
};
```

## <a name="members"></a>Members

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore sfumatura in ingresso. Questa operazione viene in genere ottenuta dall'output della backpropagazione di un livello precedente. In genere questo tensore ha le stesse dimensioni *dell'output* del [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) nel passaggio in avanti.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output contenente le sfumature backpropagate. In genere, questo tensore ha le stesse dimensioni *dell'input* del [parametro](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) DML_RESAMPLE1_OPERATOR_DESC nel passaggio in avanti.

`InterpolationMode`

Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Vedere *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Numero di elementi nelle *matrici Scales,* *InputPixelOffsets* e *OutputPixelOffsets.* Questo valore deve essere uguale *a DimensionCount* specificato in *InputGradientTensor* e *OutputGradientTensor*.

`Scales`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***

Vedere *Scales* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`InputPixelOffsets`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***

Vedere *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`OutputPixelOffsets`

Tipo: \_ Dimensione \_ campo \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***

Vedere *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputGradientTensor* e *OutputGradientTensor* devono avere lo stesso *Tipo di dati*.

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |