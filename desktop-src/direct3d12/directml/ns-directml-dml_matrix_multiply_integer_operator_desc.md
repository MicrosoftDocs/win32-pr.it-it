---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Esegue una funzione di moltiplicazione matrice sui dati integer.
helpviewer_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_matrix_multiply_integer_operator_desc
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
ms.keywords: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC, DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure, direct3d12.dml_matrix_multiply_integer_operator_desc, directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
ms.custom: 19H1
f1_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f498e84208da451b5d25ffef90219c0037ce86fb
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802836"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a>DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC struttura (directml.h)
Esegue una funzione di moltiplicazione matrice sui dati integer.

Questo operatore richiede che i tensori di input di moltiplicazione matrice siano 4D, formattati come `{ BatchCount, ChannelCount, Height, Width }` . L'operatore di moltiplicazione matrice eseguirà BatchCount * ChannelCount numero di moltiplicazioni di matrici indipendenti.

Ad esempio, se *ATensor* ha Dimensioni di e  BTensor ha Dimensioni pari a e OutputTensor ha Dimensioni pari a , l'operatore di moltiplicazione matrice eseguirà BatchCount * ChannelCount moltiplicazioni di matrici indipendenti di dimensioni `{ BatchCount, ChannelCount, M, K }`   `{ BatchCount, ChannelCount, K, N }`   `{ BatchCount, ChannelCount, M, N }` {M,K} x {K,N} = {M,N}.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Members

`ATensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati A. Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, M, K }` .


`AZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore facoltativo contenente i dati ATensor zero point. Le dimensioni previste di `AZeroPointTensor` sono se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o se è necessaria `{ 1, 1, M, 1 }` la quantizzazione per riga. Questi valori di punto zero vengono usati per dequantizzare i *valori di ATensor.*


`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore contenente i dati B. Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, K, N }` .


`BZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore facoltativo contenente i dati del punto zero *BTensor.* Le dimensioni previste di sono `BZeroPointTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o `{ 1, 1, 1, N }` se è necessaria la quantizzazione per colonna. Questi valori di punto zero vengono usati per dequantizzare i valori BTensor.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore in cui scrivere i risultati. Le dimensioni di questo tensore sono `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *ATensor* e `AZeroPointTensor` devono avere lo stesso tipo di *dati*.
* *BTensor* e `BZeroPointTensor` devono avere lo stesso tipo di *dati*.

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Dimensioni | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| ATensor | Input | { BatchCount, ChannelCount, M, K } | 4 | INT8, UINT8 |
| AZeroPointTensor | Input facoltativo | { 1, 1, AZeroPointCount, 1 } | 4 | INT8, UINT8 |
| BTensor | Input | { BatchCount, ChannelCount, K, N } | 4 | INT8, UINT8 |
| BZeroPointTensor | Input facoltativo | { 1, 1, 1, BZeroPointCount } | 4 | INT8, UINT8 |
| OutputTensor | Output | { BatchCount, ChannelCount, M, N } | 4 | INT32 |



## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |