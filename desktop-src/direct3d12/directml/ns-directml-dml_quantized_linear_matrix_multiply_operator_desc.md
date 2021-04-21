---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Esegue una funzione di moltiplicazione matrice sui dati quantizzati. Questo operatore equivale matematicamente alla dequantizzazione degli input, quindi all'esecuzione della moltiplicazione della matrice e alla quantificazione dell'output.
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
ms.openlocfilehash: 0daeab63559a2d842582087d8874e802645f7809
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803572"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a>DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC struttura (directml.h)
Esegue una funzione di moltiplicazione matrice sui dati quantizzati. Questo operatore equivale matematicamente alla dequantizzazione degli input, quindi all'esecuzione della moltiplicazione della matrice e alla quantificazione dell'output.

Questo operatore richiede che i tensori di input di moltiplicazione matrice siano 4D formattati come `{ BatchCount, ChannelCount, Height, Width }` . L'operatore di moltiplicazione matrice eseguirà BatchCount * ChannelCount numero di moltiplicazioni di matrici indipendenti. 

Ad esempio, se *ATensor* ha Dimensioni pari a e  BTensor ha Dimensioni pari a e OutputTensor ha Dimensioni pari a , l'operatore di moltiplicazione matrice eseguirà batchCount * Moltiplicazioni di matrici indipendenti ChannelCount delle dimensioni `{ BatchCount, ChannelCount, M, K }`   `{ BatchCount, ChannelCount, K, N }`   `{ BatchCount, ChannelCount, M, N }` {M,K} x {K,N} = {M,N}. 

### <a name="dequantize-function"></a>Funzione Dequantize

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a>Funzione Quantize

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

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

Tensore contenente i dati A. Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, M, K }` .


`AScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati di scala ATensor. Le dimensioni previste di sono `AScaleTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o se è necessaria `{ 1, 1, M, 1 }` la quantizzazione per riga. Questi valori di scala vengono usati per dequantizzare i valori A.


`AZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore facoltativo contenente i *dati ATensor* zero point. Le dimensioni previste di AZeroPointTensor sono se è necessaria la quantizzazione per tensore o se `{ 1, 1, 1, 1 }` è necessaria la `{ 1, 1, M, 1 }` quantizzazione per riga. Questi valori di punto zero vengono usati per dequantizzare i valori di ATensor.


`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati B. Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, K, N }` .


`BScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i *dati di scalabilità BTensor.* Le dimensioni previste di sono `BScaleTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o `{ 1, 1, 1, N }` se è necessaria la quantizzazione per colonna. Questi valori di scala vengono usati per dequantizzare i *valori BTensor.*


`BZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore facoltativo contenente i dati del punto zero *BTensor.* Le dimensioni previste di sono `BZeroPointTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o `{ 1, 1, 1, N }` se è necessaria la quantizzazione per colonna. Questi valori di punto zero vengono usati per dequantizzare i *valori BTensor.*


`OutputScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati della scala del filtro. Le dimensioni previste di sono `OutputScaleTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o `{ 1, 1, M, 1 }` se è necessaria la quantizzazione per riga. Questo valore di scala viene usato per dequantizzare i valori di filtro.


`OutputZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore facoltativo contenente i dati del filtro zero punti. Le dimensioni previste di sono `OutputZeroPointTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o se è necessaria `{ 1, 1, M, 1 }` la quantizzazione per riga. Questo valore di punto zero viene usato per dequantizzare i valori di filtro.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore in cui scrivere i risultati. Le dimensioni di questo tensore sono `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *ATensor* e `AZeroPointTensor` devono avere lo stesso Tipo di *dati*.
* *BTensor* e `BZeroPointTensor` devono avere lo stesso Tipo di *dati*.
* *OutputTensor* e `OutputZeroPointTensor` devono avere lo stesso Tipo di *dati*.

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Conteggi delle dimensioni supportati | Tipi di dati supportati |
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
| **Intestazione** | directml.h |