---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Esegue una funzione di moltiplicazione di matrici sui dati Integer.
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
ms.openlocfilehash: f6ecccf49b0d7123e6f41321c7ba1bf8e8d4ad87
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320311"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a>Struttura DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC (directml. h)
Esegue una funzione di moltiplicazione di matrici sui dati Integer.

Questo operatore richiede che i tensori di input della matrice moltiplichino il formato 4D, formattato come `{ BatchCount, ChannelCount, Height, Width }` . L'operatore Matrix Multiply eseguirà il BatchCount * ChannelCount numero di moltiplicazioni di matrici indipendenti.

Se, ad esempio, *ATensor* dispone di *dimensioni* pari a `{ BatchCount, ChannelCount, M, K }` e  *BTensor* ha dimensioni `{ BatchCount, ChannelCount, K, N }` e *OutputTensor* ha *dimensioni* pari a `{ BatchCount, ChannelCount, M, N }` , l'operatore di moltiplicazione della matrice eseguirà BatchCount * ChannelCount le moltiplicazioni di matrici indipendenti di dimensioni {m, K} x {K, n} = {m, n}.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

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

Un tensore contenente i dati di un oggetto. Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, M, K }` .


`AZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore facoltativo contenente i dati del punto zero ATensor. Le dimensioni previste di `AZeroPointTensor` sono `{ 1, 1, 1, 1 }` se è necessaria la quantizzazione del tensore o `{ 1, 1, M, 1 }` se è richiesta la quantizzazione per riga. Questi valori a virgola zero vengono utilizzati per la dequantizzazione dei valori *ATensor* .


`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore contenente i dati B. Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, K, N }` .


`BZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore facoltativo contenente i dati del punto zero *BTensor* . Le dimensioni previste di `BZeroPointTensor` sono `{ 1, 1, 1, 1 }` se è necessaria la quantizzazione del tensore o `{ 1, 1, 1, N }` se è richiesta la quantizzazione per colonna. Questi valori a virgola zero vengono utilizzati per la dequantizzazione dei valori BTensor.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore in cui scrivere i risultati. Le dimensioni di questo tensore sono `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Vincoli tensore
* *ATensor* e `AZeroPointTensor` devono avere lo stesso *tipo* di dati.
* *BTensor* e `BZeroPointTensor` devono avere lo stesso *tipo* di dati.

## <a name="tensor-support"></a>Supporto tensore
| Tensore | Tipo | Dimensioni | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| ATensor | Input | {BatchCount, ChannelCount, M, K} | 4 | INT8, UINT8 |
| AZeroPointTensor | Input facoltativo | {1, 1, AZeroPointCount, 1} | 4 | INT8, UINT8 |
| BTensor | Input | {BatchCount, ChannelCount, K, N} | 4 | INT8, UINT8 |
| BZeroPointTensor | Input facoltativo | {1, 1, 1, BZeroPointCount} | 4 | INT8, UINT8 |
| OutputTensor | Output | {BatchCount, ChannelCount, M, N} | 4 | INT32 |



## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |