---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per la [normalizzazione batch.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)
helpviewer_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_batch_normalization_grad_operator_desc
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: 2b94ac1dcf389d424aaf74d615f36cdf7acc804c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550436"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a>DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)

Calcola le sfumature di backpropagation per la [normalizzazione batch.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) **DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** esegue più calcoli, che sono dettagliati nelle descrizioni di output separate.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.5 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* MeanTensor;
    const DML_TENSOR_DESC* VarianceTensor;
    const DML_TENSOR_DESC* ScaleTensor;

    const DML_TENSOR_DESC* OutputGradientTensor;
    const DML_TENSOR_DESC* OutputScaleGradientTensor;
    const DML_TENSOR_DESC* OutputBiasGradientTensor;

    FLOAT Epsilon;
};
```

## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati di input. Si tratta in genere dello stesso tensore fornito da *InputTensor* per DML_BATCH_NORMALIZATION_OPERATOR_DESC [**nel**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passaggio in avanti.

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore sfumatura in ingresso. Questa operazione viene in genere ottenuta dall'output della retropropagazione di un livello precedente. Questo tensore deve avere le stesse dimensioni di *InputTensor.*

`MeanTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati della media. Si tratta in genere dello stesso tensore fornito da *MeanTensor* per DML_BATCH_NORMALIZATION_OPERATOR_DESC [**nel**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passaggio in avanti.

Le dimensioni che non hanno le stesse dimensioni della dimensione corrispondente di *InputTensor* devono avere una dimensione di 1 in modo che possano essere trasmesse in modo che corrispondano all'input.

Ad esempio, le dimensioni seguenti sono accettabili.

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

Di seguito è riportato un errore perché, per essere compatibile con la trasmissione, le dimensioni che non corrispondono devono essere di dimensioni 1.

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati di varianza. Si tratta in genere dello stesso tensore fornito da *VarianceTensor* DML_BATCH_NORMALIZATION_OPERATOR_DESC [**nel**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passaggio in avanti. Questo tensore deve avere le stesse dimensioni delle dimensioni *di MeanTensor*.

`ScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati di scala. Si tratta in genere dello stesso tensore fornito da *ScaleTensor* DML_BATCH_NORMALIZATION_OPERATOR_DESC [**nel**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passaggio in avanti. Questo tensore deve avere le stesse dimensioni delle dimensioni *di MeanTensor*.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Per ogni valore corrispondente negli input, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` .

Questo tensore deve avere le stesse dimensioni delle dimensioni *di InputTensor* / *InputGradientTensor*.

`OutputScaleGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Questo tensore deve avere le stesse dimensioni delle dimensioni *di MeanTensor* / *VarianceTensor* / *ScaleTensor'*.

Il calcolo seguente viene eseguito o ogni valore corrispondente negli input.

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

`sum`L'oggetto viene calcolato in tutte le dimensioni che devono essere trasmesse. Se non è necessaria alcuna trasmissione, non è necessaria alcuna somma.

Ecco un esempio.

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

L'elemento **[0, 0,** 0, 0] di è la somma di per tutti i `OutputScaleGradientTensor` `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` 90 (3 \* 5 \* 6) elementi [[0,2], **0**, [0,4], [0,5]].

`OutputBiasGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Questo tensore deve avere le stesse dimensioni delle dimensioni *di MeanTensor* / *VarianceTensor* / *ScaleTensor'*.

Viene eseguito il calcolo seguente o ogni valore corrispondente negli input.

`OutputBiasGradient = sum(InputGradient)`  

L'oggetto viene calcolato in tutte le dimensioni `sum` che devono essere trasmesse (vedere l'esempio *per OutputScaleGradientTensor).* Se non è necessaria alcuna trasmissione, non è necessaria alcuna somma.

`Epsilon`

Tipo: **[FLOAT](../../winprog/windows-data-types.md)**

Valore piccolo aggiunto alla varianza per evitare zero.

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputGradientTensor,* *InputTensor,* *MeanTensor,* *OutputBiasGradientTensor,* *OutputGradientTensor,* *OutputScaleGradientTensor,* *ScaleTensor* e *VarianceTensor* devono avere gli stessi *Valori DataType* *e DimensionCount.*

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16 |
| InputGradientTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16 |
| MeanTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16 |
| VarianceTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16 |
| ScaleTensor | Input | Da 1 a 8 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | Da 1 a 8 | FLOAT32, FLOAT16 |
| OutputScaleGradientTensor | Output | Da 1 a 8 | FLOAT32, FLOAT16 |
| OutputBiasGradientTensor | Output | Da 1 a 8 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |