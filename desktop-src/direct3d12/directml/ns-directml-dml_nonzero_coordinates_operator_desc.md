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
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a><span data-ttu-id="377e5-103">Struttura DML_NONZERO_COORDINATES_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="377e5-103">DML_NONZERO_COORDINATES_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="377e5-104">Calcola le coordinate N-dimensionali di tutti gli elementi diversi da zero del tensore di input.</span><span class="sxs-lookup"><span data-stu-id="377e5-104">Computes the N-dimensional coordinates of all non-zero elements of the input tensor.</span></span>

<span data-ttu-id="377e5-105">Questo operatore produce una matrice MxN di valori, dove ogni riga M contiene una coordinata N-dimensionale di un valore diverso da zero dall'input.</span><span class="sxs-lookup"><span data-stu-id="377e5-105">This operator produces an MxN matrix of values, where each row M contains an N-dimensional coordinate of a non-zero value from the input.</span></span> <span data-ttu-id="377e5-106">Quando si usano gli input **FLOAT32** o **FLOAT16** , entrambi gli elementi negativi e positivi 0 (0,0 f e-0,0 f) vengono considerati come zero ai fini di questo operatore.</span><span class="sxs-lookup"><span data-stu-id="377e5-106">When using **FLOAT32** or **FLOAT16** inputs, both negative and positive 0 (0.0f and -0.0f) are treated as zero for the purposes of this operator.</span></span>

<span data-ttu-id="377e5-107">L'operatore richiede che la dimensione di *OutputCoordinatesTensor* sia sufficientemente grande da contenere uno scenario peggiore in cui ogni elemento dell'input è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="377e5-107">The operator requires that the *OutputCoordinatesTensor* has a size large enough to accommodate a worst-case scenario where every element of the input is non-zero.</span></span> <span data-ttu-id="377e5-108">Questo operatore restituisce il conteggio di di elementi diversi da zero tramite *OutputCountTensor*, che i chiamanti possono controllare per determinare il numero di coordinate scritte in *OutputCoordinatesTensor*.</span><span class="sxs-lookup"><span data-stu-id="377e5-108">This operator returns the count of of non-zero elements via the *OutputCountTensor*, which callers can inspect to determine the number of coordinates written to the *OutputCoordinatesTensor*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="377e5-109">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="377e5-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="377e5-110">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="377e5-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="377e5-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="377e5-111">Syntax</span></span>

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a><span data-ttu-id="377e5-112">Members</span><span class="sxs-lookup"><span data-stu-id="377e5-112">Members</span></span>

`InputTensor`

<span data-ttu-id="377e5-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="377e5-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="377e5-114">Un tensore di input.</span><span class="sxs-lookup"><span data-stu-id="377e5-114">An input tensor.</span></span>

`OutputCountTensor`

<span data-ttu-id="377e5-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="377e5-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="377e5-116">Un tensore di output che include il conteggio di elementi diversi da zero nel tensore di input.</span><span class="sxs-lookup"><span data-stu-id="377e5-116">An output tensor that holds the count of non-zero elements in the input tensor.</span></span> <span data-ttu-id="377e5-117">Questo tensore deve essere un valore scalare &mdash; , ovvero le dimensioni di questo tensore devono essere tutte pari a 1.</span><span class="sxs-lookup"><span data-stu-id="377e5-117">This tensor must be a scalar&mdash;that is, the Sizes of this tensor must all be 1.</span></span> <span data-ttu-id="377e5-118">Il tipo di questo tensore deve essere **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="377e5-118">The type of this tensor must be **UINT32**.</span></span>

`OutputCoordinatesTensor`

<span data-ttu-id="377e5-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="377e5-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="377e5-120">Un tensore di output che include le coordinate N-dimensionali degli elementi di input che sono diverse da zero.</span><span class="sxs-lookup"><span data-stu-id="377e5-120">An output tensor that holds the N-dimensional coordinates of the input elements which are non-zero.</span></span> 

<span data-ttu-id="377e5-121">Questo tensore deve avere *dimensioni* pari a `{1,1,M,N}` (se *DimensionCount* è 4) `{1,1,1,M,N}` o (se *DimensionCount* è 5), dove M è il numero totale di elementi in *InputTensor* e N è maggiore o uguale al *rango effettivo* di *InputTensor*, fino al *DimensionCount* dell'input.</span><span class="sxs-lookup"><span data-stu-id="377e5-121">This tensor must have *Sizes* of `{1,1,M,N}` (if *DimensionCount* is 4), or `{1,1,1,M,N}` (if *DimensionCount* is 5), where M is the total number of elements in the *InputTensor*, and N is greater or equal to the *effective rank* of *InputTensor*, up to the *DimensionCount* of the input.</span></span>

<span data-ttu-id="377e5-122">Il rango effettivo di un tensore è determinato dal *DimensionCount* di tale tensore, escluse le dimensioni iniziali delle dimensioni 1.</span><span class="sxs-lookup"><span data-stu-id="377e5-122">The effective rank of a tensor is determined by the *DimensionCount* of that tensor excluding leading dimensions of size 1.</span></span> <span data-ttu-id="377e5-123">Ad esempio, un tensore con dimensioni di `{1,2,3,4}` ha un rango 3 effettivo, così come un tensore con dimensioni pari a `{1,1,5,5,5}` .</span><span class="sxs-lookup"><span data-stu-id="377e5-123">For example a tensor with sizes of `{1,2,3,4}` has effective rank 3, as does a tensor with sizes of `{1,1,5,5,5}`.</span></span> <span data-ttu-id="377e5-124">Un tensore con dimensioni `{1,1,1,1}` ha un rango effettivo 0.</span><span class="sxs-lookup"><span data-stu-id="377e5-124">A tensor with sizes `{1,1,1,1}` has effective rank 0.</span></span>

<span data-ttu-id="377e5-125">Si consideri un *InputTensor* con *dimensioni* pari a `{1,1,12,5}` .</span><span class="sxs-lookup"><span data-stu-id="377e5-125">Consider an *InputTensor* with *Sizes* of `{1,1,12,5}`.</span></span> <span data-ttu-id="377e5-126">Questo tensore di input contiene 60 elementi e ha un rango effettivo pari a 2.</span><span class="sxs-lookup"><span data-stu-id="377e5-126">This input tensor contains 60 elements, and has an effective rank of 2.</span></span> <span data-ttu-id="377e5-127">In questo esempio tutte le dimensioni valide di *OutputCoordinatesTensor* sono nel formato `{1,1,60,N}` , dove N >= 2 ma non maggiore di *DimensionCount* (4 in questo esempio).</span><span class="sxs-lookup"><span data-stu-id="377e5-127">In this example all valid sizes of *OutputCoordinatesTensor* are of the form `{1,1,60,N}`, where N >= 2 but no greater than the *DimensionCount* (4 in this example).</span></span>

<span data-ttu-id="377e5-128">Le coordinate scritte in questo tensore sono sicuramente ordinate in base all'indice dell'elemento crescente.</span><span class="sxs-lookup"><span data-stu-id="377e5-128">The coordinates written into this tensor are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="377e5-129">Se, ad esempio, il tensore di input presenta 3 valori diversi da zero alle coordinate {1,0} , {1,2} , e {0,5} , i valori scritti in *OutputCoordinatesTensor* saranno `[[0,5], [1,0], [1,2]]` .</span><span class="sxs-lookup"><span data-stu-id="377e5-129">For example if the input tensor has 3 non-zero values at coordinates {1,0}, {1,2}, and {0,5}, the values written to the *OutputCoordinatesTensor* will be `[[0,5], [1,0], [1,2]]`.</span></span>

<span data-ttu-id="377e5-130">Sebbene questo tensore richieda che la dimensione M sia uguale al numero di elementi nel tensore di input, questo operatore scriverà solo un massimo di elementi OutputCount in questo tensore.</span><span class="sxs-lookup"><span data-stu-id="377e5-130">While this tensor requires its dimension M to equal the number of elements in the input tensor, this operator will only write a maximum of OutputCount elements to this tensor.</span></span> <span data-ttu-id="377e5-131">OutputCount viene restituito tramite il *OutputCountTensor* scalare.</span><span class="sxs-lookup"><span data-stu-id="377e5-131">The OutputCount is returned through the scalar *OutputCountTensor*.</span></span>

> [!NOTE]
> <span data-ttu-id="377e5-132">Gli elementi rimanenti di questo tensore oltre il OutputCount non sono definiti dopo il completamento di questo operatore.</span><span class="sxs-lookup"><span data-stu-id="377e5-132">The remaining elements of this tensor beyond the OutputCount are undefined once this operator completes.</span></span> <span data-ttu-id="377e5-133">Non è necessario basarsi sui valori di questi elementi.</span><span class="sxs-lookup"><span data-stu-id="377e5-133">You shouldn't rely on the values of these elements.</span></span>

## <a name="example"></a><span data-ttu-id="377e5-134">Esempio</span><span class="sxs-lookup"><span data-stu-id="377e5-134">Example</span></span>

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

## <a name="availability"></a><span data-ttu-id="377e5-135">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="377e5-135">Availability</span></span>
<span data-ttu-id="377e5-136">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="377e5-136">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="377e5-137">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="377e5-137">Tensor constraints</span></span>
<span data-ttu-id="377e5-138">*InputTensor*, *OutputCoordinatesTensor* e `OutputCountTensor` devono avere lo stesso *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="377e5-138">*InputTensor*, *OutputCoordinatesTensor*, and `OutputCountTensor` must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="377e5-139">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="377e5-139">Tensor support</span></span>
| <span data-ttu-id="377e5-140">Tensore</span><span class="sxs-lookup"><span data-stu-id="377e5-140">Tensor</span></span> | <span data-ttu-id="377e5-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="377e5-141">Kind</span></span> | <span data-ttu-id="377e5-142">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="377e5-142">Dimensions</span></span> | <span data-ttu-id="377e5-143">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="377e5-143">Supported dimension counts</span></span> | <span data-ttu-id="377e5-144">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="377e5-144">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="377e5-145">InputTensor</span><span class="sxs-lookup"><span data-stu-id="377e5-145">InputTensor</span></span> | <span data-ttu-id="377e5-146">Input</span><span class="sxs-lookup"><span data-stu-id="377e5-146">Input</span></span> | <span data-ttu-id="377e5-147">{[D0], D1, D2, D3, D4}</span><span class="sxs-lookup"><span data-stu-id="377e5-147">{ [D0], D1, D2, D3, D4 }</span></span> | <span data-ttu-id="377e5-148">da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="377e5-148">4 to 5</span></span> | <span data-ttu-id="377e5-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="377e5-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="377e5-150">OutputCountTensor</span><span class="sxs-lookup"><span data-stu-id="377e5-150">OutputCountTensor</span></span> | <span data-ttu-id="377e5-151">Output</span><span class="sxs-lookup"><span data-stu-id="377e5-151">Output</span></span> | <span data-ttu-id="377e5-152">{[1], 1, 1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="377e5-152">{ [1], 1, 1, 1, 1 }</span></span> | <span data-ttu-id="377e5-153">da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="377e5-153">4 to 5</span></span> | <span data-ttu-id="377e5-154">UINT32</span><span class="sxs-lookup"><span data-stu-id="377e5-154">UINT32</span></span> |
| <span data-ttu-id="377e5-155">OutputCoordinatesTensor</span><span class="sxs-lookup"><span data-stu-id="377e5-155">OutputCoordinatesTensor</span></span> | <span data-ttu-id="377e5-156">Output</span><span class="sxs-lookup"><span data-stu-id="377e5-156">Output</span></span> | <span data-ttu-id="377e5-157">{[1], 1, 1, M, N}</span><span class="sxs-lookup"><span data-stu-id="377e5-157">{ [1], 1, 1, M, N }</span></span> | <span data-ttu-id="377e5-158">da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="377e5-158">4 to 5</span></span> | <span data-ttu-id="377e5-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="377e5-159">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="377e5-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="377e5-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="377e5-161">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="377e5-161">**Header**</span></span> | <span data-ttu-id="377e5-162">directml. h</span><span class="sxs-lookup"><span data-stu-id="377e5-162">directml.h</span></span> |