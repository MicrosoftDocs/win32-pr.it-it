---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Esegue una funzione di moltiplicazione di matrici per i dati quantizzati. Questo operatore è matematicamente equivalente a dequantizzare gli input, quindi a eseguire la moltiplicazione della matrice e quindi a quantizzare l'output.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_matrix_multiply_operator_desc
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.openlocfilehash: d0b20a37bca6ddf6083b116b53290a6b6b2084f4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320403"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a>Struttura DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC (directml. h)
Esegue una funzione di moltiplicazione di matrici per i dati quantizzati. Questo operatore è matematicamente equivalente a dequantizzare gli input, quindi a eseguire la moltiplicazione della matrice e quindi a quantizzare l'output.

Questo operatore richiede che i tensori di input della matrice moltiplichino il formato 4D, formattato come `{ BatchCount, ChannelCount, Height, Width }` . L'operatore Matrix Multiply eseguirà il BatchCount * ChannelCount numero di moltiplicazioni di matrici indipendenti. 

Se, ad esempio, *ATensor* dispone di *dimensioni* pari a `{ BatchCount, ChannelCount, M, K }` e  *BTensor* ha dimensioni `{ BatchCount, ChannelCount, K, N }` e *OutputTensor* ha *dimensioni* pari a `{ BatchCount, ChannelCount, M, N }` , l'operatore di moltiplicazione della matrice eseguirà BatchCount * ChannelCount le moltiplicazioni di matrici indipendenti di dimensioni {m, K} x {K, n} = {m, n}. 

### <a name="dequantize-function"></a>Funzione dequantizzate

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a>Funzione quantizzate

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintassi
```cpp
struct DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AScaleTensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BScaleTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Members

`ATensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore contenente i dati di un oggetto. Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, M, K }` .


`AScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore contenente i dati della scala ATensor. Le dimensioni previste di `AScaleTensor` sono `{ 1, 1, 1, 1 }` se è necessaria la quantizzazione del tensore o `{ 1, 1, M, 1 }` se è richiesta la quantizzazione per riga. Questi valori di scala vengono utilizzati per la dequantizzazione dei valori A.


`AZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore facoltativo contenente i dati del punto zero *ATensor* . Le dimensioni previste di AZeroPointTensor sono `{ 1, 1, 1, 1 }` se è richiesta la quantizzazione del tensore o `{ 1, 1, M, 1 }` se è necessaria una quantizzazione per riga. Questi valori a virgola zero vengono utilizzati per la dequantizzazione dei valori ATensor.


`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore contenente i dati B. Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, K, N }` .


`BScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore contenente i dati della scala *BTensor* . Le dimensioni previste di `BScaleTensor` sono `{ 1, 1, 1, 1 }` se è necessaria la quantizzazione del tensore o `{ 1, 1, 1, N }` se è richiesta la quantizzazione per colonna. Questi valori di scala vengono utilizzati per la dequantizzazione dei valori *BTensor* .


`BZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore facoltativo contenente i dati del punto zero *BTensor* . Le dimensioni previste di `BZeroPointTensor` sono `{ 1, 1, 1, 1 }` se è necessaria la quantizzazione del tensore o `{ 1, 1, 1, N }` se è richiesta la quantizzazione per colonna. Questi valori a virgola zero vengono utilizzati per la dequantizzazione dei valori *BTensor* .


`OutputScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore contenente i dati sulla scala del filtro. Le dimensioni previste di `OutputScaleTensor` sono `{ 1, 1, 1, 1 }` se è necessaria la quantizzazione del tensore o `{ 1, 1, M, 1 }` se è richiesta la quantizzazione per riga. Questo valore di scala viene utilizzato per dequantizzare i valori di filtro.


`OutputZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore facoltativo contenente i dati del punto zero del filtro. Le dimensioni previste di `OutputZeroPointTensor` sono `{ 1, 1, 1, 1 }` se la quantizzazione del tensore è obbligatoria o `{ 1, 1, M, 1 }` se è necessaria la quantizzazione per riga. Questo valore del punto zero viene usato per la dequantizzazione dei valori di filtro.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore in cui scrivere i risultati. Le dimensioni di questo tensore sono `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *ATensor* e `AZeroPointTensor` devono avere lo stesso *tipo* di dati.
* *BTensor* e `BZeroPointTensor` devono avere lo stesso *tipo* di dati.
* *OutputTensor* e `OutputZeroPointTensor` devono avere lo stesso *tipo* di dati.

## <a name="tensor-support"></a>Supporto tensore
| Tensore | Tipo | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 4 | INT8, UINT8 |
| AScaleTensor | Input | 4 | FLOAT32 |
| AZeroPointTensor | Input facoltativo | 4 | INT8, UINT8 |
| BTensor | Input | 4 | INT8, UINT8 |
| BScaleTensor | Input | 4 | FLOAT32 |
| BZeroPointTensor | Input facoltativo | 4 | INT8, UINT8 |
| OutputScaleTensor | Input | 4 | FLOAT32 |
| OutputZeroPointTensor | Input facoltativo | 4 | INT8, UINT8 |
| OutputTensor | Output | 4 | INT8, UINT8 |



## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |