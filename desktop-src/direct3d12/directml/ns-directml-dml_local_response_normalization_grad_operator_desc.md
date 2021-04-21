---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per la [normalizzazione della risposta locale.](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)
helpviewer_keywords:
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_local_response_normalization_grad_operator_desc
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: eecf849a06ee8e99ac9c015ecd4568496120b2d9
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804470"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a>DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)

Calcola le sfumature di backpropagation per la [normalizzazione della risposta locale.](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)

Il tipo di dati e le dimensioni di tutti i tensori devono essere uguali.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.5 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    BOOL CrossChannel;
    UINT LocalSize;
    FLOAT Alpha;
    FLOAT Beta;
    FLOAT Bias;
};
```

## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati di input. Le dimensioni di *questo* tensore devono essere `{ BatchCount, ChannelCount, Height, Width }` .

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore sfumatura in ingresso. Questa operazione viene in genere ottenuta dall'output della backpropagazione di un livello precedente.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output contenente le sfumature backpropagate.

`CrossChannel`

Tipo: **[BOOL](/windows/win32/winprog/windows-data-types)**

**TRUE** se il livello LRN viene sommato tra canali; **FALSE** se il livello LRN somma le dimensioni spaziali.

`LocalSize`

Tipo: **[UINT](/windows/win32/winprog/windows-data-types)**

Numero massimo di elementi da sommare per ogni dimensione (l'area locale viene ritagliata in modo che tutti gli elementi siano entro limiti). Se *CrossChannel* è **TRUE,** si tratta della larghezza e dell'altezza dell'area locale. Se *CrossChannel* è **FALSE,** questo è il numero di elementi nell'area locale. Il valore deve essere almeno 1.

`Alpha`

Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**

Valore del parametro di ridimensionamento. È consigliabile impostare il valore predefinito su 0,0001.

`Beta`

Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**

Valore dell'esponente. È consigliabile impostare il valore predefinito su 0,75.

`Bias`

Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**

Valore della distorsione. È consigliabile impostare il valore predefinito su 1.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputGradientTensor,* *InputTensor* e *OutputGradientTensor* devono avere gli stessi *valori di DataType* *e Sizes.*

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| InputGradientTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |
