---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: Calcola le coordinate N-dimensionali di tutti gli elementi diversi da zero del tensore di input.
helpviewer_keywords:
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- DML_NONZERO_COORDINATES_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_NONZERO_COORDINATES_OPERATOR_DESC, DML_NONZERO_COORDINATES_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.openlocfilehash: a662ac3b341c07e512e11dcc15cbc9b11ec5f405
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320364"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a>Struttura DML_NONZERO_COORDINATES_OPERATOR_DESC (directml. h)

Calcola le coordinate N-dimensionali di tutti gli elementi diversi da zero del tensore di input.

Questo operatore produce una matrice MxN di valori, dove ogni riga M contiene una coordinata N-dimensionale di un valore diverso da zero dall'input. Quando si usano gli input **FLOAT32** o **FLOAT16** , entrambi gli elementi negativi e positivi 0 (0,0 f e-0,0 f) vengono considerati come zero ai fini di questo operatore.

L'operatore richiede che la dimensione di *OutputCoordinatesTensor* sia sufficientemente grande da contenere uno scenario peggiore in cui ogni elemento dell'input è diverso da zero. Questo operatore restituisce il conteggio di di elementi diversi da zero tramite *OutputCountTensor*, che i chiamanti possono controllare per determinare il numero di coordinate scritte in *OutputCoordinatesTensor*.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintassi

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore di input.

`OutputCountTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore di output che include il conteggio di elementi diversi da zero nel tensore di input. Questo tensore deve essere un valore scalare &mdash; , ovvero le dimensioni di questo tensore devono essere tutte pari a 1. Il tipo di questo tensore deve essere **UInt32**.

`OutputCoordinatesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensore di output che include le coordinate N-dimensionali degli elementi di input che sono diverse da zero. 

Questo tensore deve avere *dimensioni* pari a `{1,1,M,N}` (se *DimensionCount* è 4) `{1,1,1,M,N}` o (se *DimensionCount* è 5), dove M è il numero totale di elementi in *InputTensor* e N è maggiore o uguale al *rango effettivo* di *InputTensor*, fino al *DimensionCount* dell'input.

Il rango effettivo di un tensore è determinato dal *DimensionCount* di tale tensore, escluse le dimensioni iniziali delle dimensioni 1. Ad esempio, un tensore con dimensioni di `{1,2,3,4}` ha un rango 3 effettivo, così come un tensore con dimensioni pari a `{1,1,5,5,5}` . Un tensore con dimensioni `{1,1,1,1}` ha un rango effettivo 0.

Si consideri un *InputTensor* con *dimensioni* pari a `{1,1,12,5}` . Questo tensore di input contiene 60 elementi e ha un rango effettivo pari a 2. In questo esempio tutte le dimensioni valide di *OutputCoordinatesTensor* sono nel formato `{1,1,60,N}` , dove N >= 2 ma non maggiore di *DimensionCount* (4 in questo esempio).

Le coordinate scritte in questo tensore sono sicuramente ordinate in base all'indice dell'elemento crescente. Se, ad esempio, il tensore di input presenta 3 valori diversi da zero alle coordinate {1,0} , {1,2} , e {0,5} , i valori scritti in *OutputCoordinatesTensor* saranno `[[0,5], [1,0], [1,2]]` .

Sebbene questo tensore richieda che la dimensione M sia uguale al numero di elementi nel tensore di input, questo operatore scriverà solo un massimo di elementi OutputCount in questo tensore. OutputCount viene restituito tramite il *OutputCountTensor* scalare.

> [!NOTE]
> Gli elementi rimanenti di questo tensore oltre il OutputCount non sono definiti dopo il completamento di questo operatore. Non è necessario basarsi sui valori di questi elementi.

## <a name="example"></a>Esempio

```
InputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[1.0f,  0.0f, 0.0f,  2.0f],
 [-0.0f, 3.5f, 0.0f, -5.2f]]

OutputCountTensor: (Sizes:{1,1,1,1}, DataType:UINT32)
[4]

OutputCoordinatesTensor: (Sizes:{1,1,8,3}, DataType:UINT32)
[[0, 0, 0],
 [0, 0, 3],
 [0, 1, 1],
 [0, 1, 3],
 [0, 0, 0], // 
 [0, 0, 0], // Values in rows >= OutputCountTensor (4 in
 [0, 0, 0], // this case) are left undefined
 [0, 0, 0]] // 
```

## <a name="availability"></a>Disponibilità
Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Vincoli tensore
*InputTensor*, *OutputCoordinatesTensor* e `OutputCountTensor` devono avere lo stesso *DimensionCount*.

## <a name="tensor-support"></a>Supporto tensore
| Tensore | Tipo | Dimensioni | Conteggi dimensione supportati | Tipi di dati supportati |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | {[D0], D1, D2, D3, D4} | da 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputCountTensor | Output | {[1], 1, 1, 1, 1} | da 4 a 5 | UINT32 |
| OutputCoordinatesTensor | Output | {[1], 1, 1, M, N} | da 4 a 5 | UINT32 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml. h |