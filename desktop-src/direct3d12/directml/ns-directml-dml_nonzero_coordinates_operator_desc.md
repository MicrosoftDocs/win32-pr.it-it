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
ms.openlocfilehash: 39463ba57bc90b35d5ac5dc7fc43993169137221
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803392"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a>DML_NONZERO_COORDINATES_OPERATOR_DESC struttura (directml.h)

Calcola le coordinate N-dimensionali di tutti gli elementi diversi da zero del tensore di input.

Questo operatore produce una matrice MxN di valori, in cui ogni riga M contiene una coordinata N-dimensionale di un valore diverso da zero dall'input. Quando si usano input **FLOAT32** o **FLOAT16,** sia negativi che positivi (0,0f e -0,0f) vengono considerati come zero ai fini di questo operatore.

L'operatore richiede che *OutputCoordinatesTensor* abbia dimensioni sufficienti per supportare uno scenario peggiore in cui ogni elemento dell'input è diverso da zero. Questo operatore restituisce il conteggio degli elementi diversi da zero tramite *OutputCountTensor*, che i chiamanti possono esaminare per determinare il numero di coordinate scritte in *OutputCoordinatesTensor*.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

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

Tensore di input.

`OutputCountTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output che contiene il numero di elementi diversi da zero nel tensore di input. Questo tensore deve essere scalare, ad esempio le dimensioni di questo &mdash; tensore devono essere tutte 1. Il tipo di questo tensore deve **essere UINT32.**

`OutputCoordinatesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensore di output che contiene le coordinate N-dimensionali degli elementi di input diversi da zero. 

Questo tensore  deve avere dimensioni pari a `{1,1,M,N}` (se *DimensionCount* è 4) o `{1,1,1,M,N}` (se *DimensionCount*  è 5), dove M è il numero totale di elementi in *InputTensor* e N è maggiore o uguale alla classificazione effettiva di *InputTensor*, fino a *DimensionCount dell'input.*

La classificazione effettiva di un tensore è determinata dal *valore DimensionCount* di tale tensore, escluse le dimensioni iniziali di dimensioni 1. Ad esempio, un tensore con dimensioni di ha una classificazione effettiva 3, così come un `{1,2,3,4}` tensore con dimensioni `{1,1,5,5,5}` di . Un tensore con dimensioni `{1,1,1,1}` ha una classificazione effettiva 0.

Si *consideri un InputTensor* *con dimensioni* di `{1,1,12,5}` . Questo tensore di input contiene 60 elementi e ha un rango effettivo di 2. In questo esempio tutte le dimensioni valide di *OutputCoordinatesTensor* sono nel formato , dove N >= 2 ma non maggiore di `{1,1,60,N}` *DimensionCount* (4 in questo esempio).

Le coordinate scritte in questo tensore vengono ordinate in base all'indice crescente degli elementi. Ad esempio, se il tensore di input ha 3 valori diversi da zero nelle coordinate , e , i valori scritti in {1,0} {1,2} {0,5} *OutputCoordinatesTensor* saranno `[[0,5], [1,0], [1,2]]` .

Anche se questo tensore richiede che la dimensione M sia uguale al numero di elementi nel tensore di input, questo operatore scriverà solo un massimo di elementi OutputCount in questo tensore. OutputCount viene restituito tramite *l'oggetto scalare OutputCountTensor.*

> [!NOTE]
> Gli elementi rimanenti di questo tensore oltre OutputCount non sono definiti al termine dell'operatore. Non è consigliabile basarsi sui valori di questi elementi.

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
*InputTensor*, *OutputCoordinatesTensor* e `OutputCountTensor` devono avere lo stesso *dimensionCount*.

## <a name="tensor-support"></a>Supporto di Tensor
| Tensore | Tipo | Dimensioni | Conteggi delle dimensioni supportati | Tipi di dati supportati |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | { [D0], D1, D2, D3, D4 } | Da 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputCountTensor | Output | { [1], 1, 1, 1, 1 } | Da 4 a 5 | UINT32 |
| OutputCoordinatesTensor | Output | { [1], 1, 1, M, N } | Da 4 a 5 | UINT32 |

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | directml.h |