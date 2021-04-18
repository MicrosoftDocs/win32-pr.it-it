---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Calcola le sfumature di propagazione per il ricampionamento (vedere [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
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
ms.openlocfilehash: 5808381f2e812ac20399b46672e51acd063bc6a5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320401"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a>Struttura DML_RESAMPLE_GRAD_OPERATOR_DESC (directml. h)

Calcola le sfumature di propagazione per il ricampionamento (vedere [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).

**DML_RESAMPLE1_OPERATOR_DESC** ridimensiona le dimensioni arbitrarie del tensore di input usando il campionamento più vicino o l'interpolazione bilineare. Dato un *InputGradientTensor* con le stesse dimensioni dell' *output* di un **DML_RESAMPLE1_OPERATOR_DESC** equivalente, questo operatore produce un *OutputGradientTensor* con le stesse dimensioni dell' *input* della **DML_RESAMPLE1_OPERATOR_DESC**.

Si consideri, ad esempio, un **DML_RESAMPLE1_OPERATOR_DESC** che esegue un ridimensionamento adiacente più vicino di 1.5 x nella larghezza e 0,5 x nell'altezza.

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

Si noti che l'elemento 0A del tensore di input (con valore 1) contribuisce a due elementi nell'output, il primo elemento (con valore 2) contribuisce a un elemento nell'output, mentre il secondo e il terzo elementi (con valori 3 e 4) contribuiscono a nessun elemento dell'output.

Il **DML_RESAMPLE_GRAD_OPERATOR_DESC** corrispondente eseguirà le operazioni seguenti.

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

Si noti che i valori in *OutputGradientTensor* rappresentano i contributi ponderati di tale elemento al *OutputTensor* durante l'operatore **DML_RESAMPLE1_OPERATOR_DESC** originale.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

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

Tensore di sfumatura in ingresso. Questa operazione viene in genere ottenuta dall'output di propagation di un livello precedente. In genere, questo tensore avrebbe le stesse dimensioni dell' *output* del [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) corrispondente nel passaggio successivo.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore di output contenente le sfumature ripropagate. In genere, questo tensore avrebbe le stesse dimensioni dell' *input* del [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) corrispondente nel passaggio successivo.

`InterpolationMode`

Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Vedere *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Il numero di elementi nelle matrici *Scales*, *InputPixelOffsets* e *OutputPixelOffsets* . Questo valore deve essere uguale a *DimensionCount* specificato in *InputGradientTensor* e *OutputGradientTensor*.

`Scales`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Vedere *scale* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`InputPixelOffsets`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Vedere *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`OutputPixelOffsets`

Tipo: \_ \_ Dimensione campo \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Vedere *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputGradientTensor* e *OutputGradientTensor* devono avere lo stesso *tipo* di dati.

## <a name="tensor-support"></a>Supporto tensore
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |