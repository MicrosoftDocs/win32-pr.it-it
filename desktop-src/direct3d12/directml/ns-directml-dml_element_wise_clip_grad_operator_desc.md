---
UID: NS:directml.DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
title: DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per [un clip per elemento.](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)
helpviewer_keywords:
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC structure
- direct3d12.dml_element_wise_clip_grad_operator_desc
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
ms.openlocfilehash: 224fbacdb8816a6aed6a7779c5c8ff991736ee6c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804490"
---
# <a name="dml_element_wise_clip_grad_operator_desc-directmlh"></a>DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml.h)

Calcola le sfumature di backpropagation per [il clip per elemento.](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)

```
f(x, gradient) = if x <= Min then 0
                 if x >= Max then 0
                 else        then gradient
```

Questo operatore supporta l'esecuzione sul posto, ovvero è `OutputTensor` consentito creare un alias di *InputTensor durante* l'associazione.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.5 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    FLOAT Min;
    FLOAT Max;
};
```

## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore della funzionalità di input. Si tratta in genere dello stesso tensore fornito da *InputTensor* DML_ELEMENT_WISE_CLIP_OPERATOR_DESC [nel](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) passaggio in avanti.

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore sfumatura in ingresso. Questa operazione viene in genere ottenuta dall'output della backpropagazione di un livello precedente. In genere questo tensore ha le stesse dimensioni *dell'output* dell'oggetto **DML_OPERATOR_ELEMENT_WISE_CLIP** nel passaggio in avanti.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output contenente le sfumature backpropagate. In genere, questo tensore ha le stesse dimensioni *dell'input* del **DML_OPERATOR_ELEMENT_WISE_CLIP** nel passaggio in avanti.

`Min`

Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**

Valore minimo. Se x è in corrispondenza o al di sotto di questo valore, il risultato della sfumatura è 0.

`Max`

Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**

Valore massimo. Se x è al di sopra di questo valore, il risultato della sfumatura è 0.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputGradientTensor,* *InputTensor* e *OutputGradientTensor* devono avere gli stessi *valori di DataType,* *DimensionCount* e *Sizes.*

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| InputGradientTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputGradientTensor | Output | Da 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |
