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
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a><span data-ttu-id="e8ec8-103">DML_NONZERO_COORDINATES_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="e8ec8-103">DML_NONZERO_COORDINATES_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e8ec8-104">Calcola le coordinate N-dimensionali di tutti gli elementi diversi da zero del tensore di input.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-104">Computes the N-dimensional coordinates of all non-zero elements of the input tensor.</span></span>

<span data-ttu-id="e8ec8-105">Questo operatore produce una matrice MxN di valori, in cui ogni riga M contiene una coordinata N-dimensionale di un valore diverso da zero dall'input.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-105">This operator produces an MxN matrix of values, where each row M contains an N-dimensional coordinate of a non-zero value from the input.</span></span> <span data-ttu-id="e8ec8-106">Quando si usano input **FLOAT32** o **FLOAT16,** sia negativi che positivi (0,0f e -0,0f) vengono considerati come zero ai fini di questo operatore.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-106">When using **FLOAT32** or **FLOAT16** inputs, both negative and positive 0 (0.0f and -0.0f) are treated as zero for the purposes of this operator.</span></span>

<span data-ttu-id="e8ec8-107">L'operatore richiede che *OutputCoordinatesTensor* abbia dimensioni sufficienti per supportare uno scenario peggiore in cui ogni elemento dell'input è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-107">The operator requires that the *OutputCoordinatesTensor* has a size large enough to accommodate a worst-case scenario where every element of the input is non-zero.</span></span> <span data-ttu-id="e8ec8-108">Questo operatore restituisce il conteggio degli elementi diversi da zero tramite *OutputCountTensor*, che i chiamanti possono esaminare per determinare il numero di coordinate scritte in *OutputCoordinatesTensor*.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-108">This operator returns the count of of non-zero elements via the *OutputCountTensor*, which callers can inspect to determine the number of coordinates written to the *OutputCoordinatesTensor*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8ec8-109">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="e8ec8-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e8ec8-110">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="e8ec8-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ec8-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8ec8-111">Syntax</span></span>

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a><span data-ttu-id="e8ec8-112">Members</span><span class="sxs-lookup"><span data-stu-id="e8ec8-112">Members</span></span>

`InputTensor`

<span data-ttu-id="e8ec8-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e8ec8-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e8ec8-114">Tensore di input.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-114">An input tensor.</span></span>

`OutputCountTensor`

<span data-ttu-id="e8ec8-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e8ec8-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e8ec8-116">Tensore di output che contiene il numero di elementi diversi da zero nel tensore di input.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-116">An output tensor that holds the count of non-zero elements in the input tensor.</span></span> <span data-ttu-id="e8ec8-117">Questo tensore deve essere scalare, ad esempio le dimensioni di questo &mdash; tensore devono essere tutte 1.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-117">This tensor must be a scalar&mdash;that is, the Sizes of this tensor must all be 1.</span></span> <span data-ttu-id="e8ec8-118">Il tipo di questo tensore deve **essere UINT32.**</span><span class="sxs-lookup"><span data-stu-id="e8ec8-118">The type of this tensor must be **UINT32**.</span></span>

`OutputCoordinatesTensor`

<span data-ttu-id="e8ec8-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e8ec8-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e8ec8-120">Tensore di output che contiene le coordinate N-dimensionali degli elementi di input diversi da zero.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-120">An output tensor that holds the N-dimensional coordinates of the input elements which are non-zero.</span></span> 

<span data-ttu-id="e8ec8-121">Questo tensore  deve avere dimensioni pari a `{1,1,M,N}` (se *DimensionCount* è 4) o `{1,1,1,M,N}` (se *DimensionCount*  è 5), dove M è il numero totale di elementi in *InputTensor* e N è maggiore o uguale alla classificazione effettiva di *InputTensor*, fino a *DimensionCount dell'input.*</span><span class="sxs-lookup"><span data-stu-id="e8ec8-121">This tensor must have *Sizes* of `{1,1,M,N}` (if *DimensionCount* is 4), or `{1,1,1,M,N}` (if *DimensionCount* is 5), where M is the total number of elements in the *InputTensor*, and N is greater or equal to the *effective rank* of *InputTensor*, up to the *DimensionCount* of the input.</span></span>

<span data-ttu-id="e8ec8-122">La classificazione effettiva di un tensore è determinata dal *valore DimensionCount* di tale tensore, escluse le dimensioni iniziali di dimensioni 1.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-122">The effective rank of a tensor is determined by the *DimensionCount* of that tensor excluding leading dimensions of size 1.</span></span> <span data-ttu-id="e8ec8-123">Ad esempio, un tensore con dimensioni di ha una classificazione effettiva 3, così come un `{1,2,3,4}` tensore con dimensioni `{1,1,5,5,5}` di .</span><span class="sxs-lookup"><span data-stu-id="e8ec8-123">For example a tensor with sizes of `{1,2,3,4}` has effective rank 3, as does a tensor with sizes of `{1,1,5,5,5}`.</span></span> <span data-ttu-id="e8ec8-124">Un tensore con dimensioni `{1,1,1,1}` ha una classificazione effettiva 0.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-124">A tensor with sizes `{1,1,1,1}` has effective rank 0.</span></span>

<span data-ttu-id="e8ec8-125">Si *consideri un InputTensor* *con dimensioni* di `{1,1,12,5}` .</span><span class="sxs-lookup"><span data-stu-id="e8ec8-125">Consider an *InputTensor* with *Sizes* of `{1,1,12,5}`.</span></span> <span data-ttu-id="e8ec8-126">Questo tensore di input contiene 60 elementi e ha un rango effettivo di 2.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-126">This input tensor contains 60 elements, and has an effective rank of 2.</span></span> <span data-ttu-id="e8ec8-127">In questo esempio tutte le dimensioni valide di *OutputCoordinatesTensor* sono nel formato , dove N >= 2 ma non maggiore di `{1,1,60,N}` *DimensionCount* (4 in questo esempio).</span><span class="sxs-lookup"><span data-stu-id="e8ec8-127">In this example all valid sizes of *OutputCoordinatesTensor* are of the form `{1,1,60,N}`, where N >= 2 but no greater than the *DimensionCount* (4 in this example).</span></span>

<span data-ttu-id="e8ec8-128">Le coordinate scritte in questo tensore vengono ordinate in base all'indice crescente degli elementi.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-128">The coordinates written into this tensor are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="e8ec8-129">Ad esempio, se il tensore di input ha 3 valori diversi da zero nelle coordinate , e , i valori scritti in {1,0} {1,2} {0,5} *OutputCoordinatesTensor* saranno `[[0,5], [1,0], [1,2]]` .</span><span class="sxs-lookup"><span data-stu-id="e8ec8-129">For example if the input tensor has 3 non-zero values at coordinates {1,0}, {1,2}, and {0,5}, the values written to the *OutputCoordinatesTensor* will be `[[0,5], [1,0], [1,2]]`.</span></span>

<span data-ttu-id="e8ec8-130">Anche se questo tensore richiede che la dimensione M sia uguale al numero di elementi nel tensore di input, questo operatore scriverà solo un massimo di elementi OutputCount in questo tensore.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-130">While this tensor requires its dimension M to equal the number of elements in the input tensor, this operator will only write a maximum of OutputCount elements to this tensor.</span></span> <span data-ttu-id="e8ec8-131">OutputCount viene restituito tramite *l'oggetto scalare OutputCountTensor.*</span><span class="sxs-lookup"><span data-stu-id="e8ec8-131">The OutputCount is returned through the scalar *OutputCountTensor*.</span></span>

> [!NOTE]
> <span data-ttu-id="e8ec8-132">Gli elementi rimanenti di questo tensore oltre OutputCount non sono definiti al termine dell'operatore.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-132">The remaining elements of this tensor beyond the OutputCount are undefined once this operator completes.</span></span> <span data-ttu-id="e8ec8-133">Non è consigliabile basarsi sui valori di questi elementi.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-133">You shouldn't rely on the values of these elements.</span></span>

## <a name="example"></a><span data-ttu-id="e8ec8-134">Esempio</span><span class="sxs-lookup"><span data-stu-id="e8ec8-134">Example</span></span>

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

## <a name="availability"></a><span data-ttu-id="e8ec8-135">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="e8ec8-135">Availability</span></span>
<span data-ttu-id="e8ec8-136">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="e8ec8-136">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e8ec8-137">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="e8ec8-137">Tensor constraints</span></span>
<span data-ttu-id="e8ec8-138">*InputTensor*, *OutputCoordinatesTensor* e `OutputCountTensor` devono avere lo stesso *dimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="e8ec8-138">*InputTensor*, *OutputCoordinatesTensor*, and `OutputCountTensor` must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e8ec8-139">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="e8ec8-139">Tensor support</span></span>
| <span data-ttu-id="e8ec8-140">Tensore</span><span class="sxs-lookup"><span data-stu-id="e8ec8-140">Tensor</span></span> | <span data-ttu-id="e8ec8-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="e8ec8-141">Kind</span></span> | <span data-ttu-id="e8ec8-142">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="e8ec8-142">Dimensions</span></span> | <span data-ttu-id="e8ec8-143">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="e8ec8-143">Supported dimension counts</span></span> | <span data-ttu-id="e8ec8-144">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="e8ec8-144">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="e8ec8-145">InputTensor</span><span class="sxs-lookup"><span data-stu-id="e8ec8-145">InputTensor</span></span> | <span data-ttu-id="e8ec8-146">Input</span><span class="sxs-lookup"><span data-stu-id="e8ec8-146">Input</span></span> | <span data-ttu-id="e8ec8-147">{ [D0], D1, D2, D3, D4 }</span><span class="sxs-lookup"><span data-stu-id="e8ec8-147">{ [D0], D1, D2, D3, D4 }</span></span> | <span data-ttu-id="e8ec8-148">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="e8ec8-148">4 to 5</span></span> | <span data-ttu-id="e8ec8-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e8ec8-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e8ec8-150">OutputCountTensor</span><span class="sxs-lookup"><span data-stu-id="e8ec8-150">OutputCountTensor</span></span> | <span data-ttu-id="e8ec8-151">Output</span><span class="sxs-lookup"><span data-stu-id="e8ec8-151">Output</span></span> | <span data-ttu-id="e8ec8-152">{ [1], 1, 1, 1, 1 }</span><span class="sxs-lookup"><span data-stu-id="e8ec8-152">{ [1], 1, 1, 1, 1 }</span></span> | <span data-ttu-id="e8ec8-153">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="e8ec8-153">4 to 5</span></span> | <span data-ttu-id="e8ec8-154">UINT32</span><span class="sxs-lookup"><span data-stu-id="e8ec8-154">UINT32</span></span> |
| <span data-ttu-id="e8ec8-155">OutputCoordinatesTensor</span><span class="sxs-lookup"><span data-stu-id="e8ec8-155">OutputCoordinatesTensor</span></span> | <span data-ttu-id="e8ec8-156">Output</span><span class="sxs-lookup"><span data-stu-id="e8ec8-156">Output</span></span> | <span data-ttu-id="e8ec8-157">{ [1], 1, 1, M, N }</span><span class="sxs-lookup"><span data-stu-id="e8ec8-157">{ [1], 1, 1, M, N }</span></span> | <span data-ttu-id="e8ec8-158">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="e8ec8-158">4 to 5</span></span> | <span data-ttu-id="e8ec8-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="e8ec8-159">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="e8ec8-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8ec8-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e8ec8-161">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="e8ec8-161">**Header**</span></span> | <span data-ttu-id="e8ec8-162">directml.h</span><span class="sxs-lookup"><span data-stu-id="e8ec8-162">directml.h</span></span> |