---
UID: NS:directml.DML_GATHER_ND1_OPERATOR_DESC
title: DML_GATHER_ND1_OPERATOR_DESC
description: Raccoglie gli elementi dal tensore di input, usando il tensore degli indici per eseguire il mapping degli indici a interi sottoblocco dell'input. | DML_GATHER_ND1_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND1_OPERATOR_DESC
- DML_GATHER_ND1_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_GATHER_ND1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_GATHER_ND1_OPERATOR_DESC, DML_GATHER_ND1_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
- directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
ms.openlocfilehash: b92c8aece88d8466357bb8e48fd3ce5a3b73d2e3
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417614"
---
# <a name="dml_gather_nd1_operator_desc-structure-directmlh"></a><span data-ttu-id="4159f-104">DML_GATHER_ND1_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="4159f-104">DML_GATHER_ND1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="4159f-105">Raccoglie gli elementi dal tensore di input, usando il tensore degli indici per eseguire il mapping degli indici a interi sottoblocco dell'input.</span><span class="sxs-lookup"><span data-stu-id="4159f-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="4159f-106">Questo operatore esegue lo pseudocodice seguente, dove "..." rappresenta una serie di coordinate, con il comportamento esatto dipendente dal numero di dimensioni batch, input e indici.</span><span class="sxs-lookup"><span data-stu-id="4159f-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the batch, input, and indices dimension count.</span></span>

```
output[batch, ...] = input[batch, indices[batch, ...], ...]
```

> [!IMPORTANT]
> <span data-ttu-id="4159f-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="4159f-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="4159f-108">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="4159f-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4159f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4159f-109">Syntax</span></span>

```cpp
struct DML_GATHER_ND1_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* IndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT InputDimensionCount;
  UINT IndicesDimensionCount;
  UINT BatchDimensionCount;
};
```

## <a name="members"></a><span data-ttu-id="4159f-110">Members</span><span class="sxs-lookup"><span data-stu-id="4159f-110">Members</span></span>

`InputTensor`

<span data-ttu-id="4159f-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4159f-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4159f-112">Tensore da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="4159f-112">The tensor to read from.</span></span>

`IndicesTensor`

<span data-ttu-id="4159f-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4159f-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4159f-114">Tensore contenente gli indici.</span><span class="sxs-lookup"><span data-stu-id="4159f-114">The tensor containing the indices.</span></span> <span data-ttu-id="4159f-115">*DimensionCount di* questo tensore deve corrispondere a *InputTensor.DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="4159f-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="4159f-116">L'ultima dimensione di *IndicesTensor* è in realtà il numero di coordinate per ogni tupla di indice e non può superare *InputTensor.DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="4159f-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="4159f-117">Ad esempio, un tensore di indici di *dimensioni* con `{1,4,5,2}` *IndicesDimensionCount* = 3 indica una matrice 4x5 di tuple a 2 coordinate che indicizzano in *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="4159f-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="4159f-118">A partire `DML_FEATURE_LEVEL_3_0` da , questo operatore supporta valori di indice negativi quando si usa un tipo integrale con segno con questo tensore.</span><span class="sxs-lookup"><span data-stu-id="4159f-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="4159f-119">Gli indici negativi vengono interpretati come relativi alla fine della rispettiva dimensione.</span><span class="sxs-lookup"><span data-stu-id="4159f-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="4159f-120">Ad esempio, un indice -1 fa riferimento all'ultimo elemento lungo tale dimensione.</span><span class="sxs-lookup"><span data-stu-id="4159f-120">For example, an index of -1 refers to the last element along that dimension.</span></span>

`OutputTensor`

<span data-ttu-id="4159f-121">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4159f-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4159f-122">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="4159f-122">The tensor to write the results to.</span></span> <span data-ttu-id="4159f-123">*DimensionCount e* *DataType di* questo tensore devono corrispondere a *InputTensor.DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="4159f-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="4159f-124">*OutputTensor.Sizes* previsto è la concatenazione dei segmenti iniziali *IndicesTensor.Sizes* e del segmento finale *InputTensor.Sizes,* che restituisce quanto segue.</span><span class="sxs-lookup"><span data-stu-id="4159f-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment, which yields the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="4159f-125">Le dimensioni sono allineate a destra, con i valori iniziali 1 anteposti se necessario per soddisfare *OutputTensor.DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="4159f-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="4159f-126">Ecco un esempio.</span><span class="sxs-lookup"><span data-stu-id="4159f-126">Here's an example.</span></span>

```
InputTensor.Sizes = {3,4,5,6,7}
InputDimensionCount = 5
IndicesTensor.Sizes = {1,1, 1,2,3}
IndicesDimensionCount = 3 // can be thought of as a {1,2} array of 3-coordinate tuples

// The {1,2} comes from the indices tensor (ignoring last dimension which is the tuple size),
// and the {6,7} comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
OutputTensor.Sizes = {1, 1,2,6,7}
```

`InputDimensionCount`

<span data-ttu-id="4159f-127">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4159f-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4159f-128">Numero di dimensioni di input effettive all'interno di *InputTensor* dopo aver ignorato eventuali dimensioni iniziali irrilevanti, ad esempio `[1, *InputTensor.DimensionCount*]` .</span><span class="sxs-lookup"><span data-stu-id="4159f-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="4159f-129">Ad esempio, dati *InputTensor.Sizes*  =  `{1,1,4,6}` e = `InputDimensionCount` 3, gli indici significativi effettivi sono `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="4159f-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`IndicesDimensionCount`

<span data-ttu-id="4159f-130">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4159f-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4159f-131">Numero di dimensioni di indice effettive all'interno di *IndicesTensor* dopo aver ignorato le eventuali dimensioni iniziali irrilevanti, ad esempio [1, *IndicesTensor.DimensionCount*].</span><span class="sxs-lookup"><span data-stu-id="4159f-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="4159f-132">Ad esempio, dati *IndicisTensor.Sizes*  =  `{1,1,4,6}` e *IndicesDimensionCount* = 3, gli indici significativi effettivi sono `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="4159f-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`BatchDimensionCount`

<span data-ttu-id="4159f-133">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4159f-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4159f-134">Numero di dimensioni all'interno di ogni tensore (*InputTensor*, *IndicesTensor*, *OutputTensor*) considerate batch indipendenti, compresi tra [0, *InputTensor.DimensionCount*) e [0, *IndicesTensor.DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="4159f-134">The number of dimensions within each tensor (*InputTensor*, *IndicesTensor*, *OutputTensor*) that are considered independent batches, ranging within both [0, *InputTensor.DimensionCount*) and [0, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="4159f-135">Il numero di batch può essere 0, implicando un singolo batch.</span><span class="sxs-lookup"><span data-stu-id="4159f-135">The batch count can be 0, implying a single batch.</span></span> <span data-ttu-id="4159f-136">Ad esempio, dati *IndicisTensor.Sizes*  =  `{1,3,4,5,6,7}` e *IndicesDimensionCount* = 5 e `BatchDimensionCount` = 2, sono presenti batch e `{3,4}` indici `{5,6,7}` significativi.</span><span class="sxs-lookup"><span data-stu-id="4159f-136">For example, given *IndicesTensor.Sizes* = `{1,3,4,5,6,7}`, and *IndicesDimensionCount* = 5 and `BatchDimensionCount` = 2, there are batches `{3,4}` and meaningful indices `{5,6,7}`.</span></span>

## <a name="remarks"></a><span data-ttu-id="4159f-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="4159f-137">Remarks</span></span>
<span data-ttu-id="4159f-138">**DML_GATHER_ND1_OPERATOR_DESC** aggiunge *BatchDimensionCount* ed è equivalente [](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) a DML_GATHER_ND_OPERATOR_DESC *batchDimensionCount* = 0.</span><span class="sxs-lookup"><span data-stu-id="4159f-138">**DML_GATHER_ND1_OPERATOR_DESC** adds *BatchDimensionCount*, and is equivalent to [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) when *BatchDimensionCount* = 0.</span></span>

## <a name="examples"></a><span data-ttu-id="4159f-139">Esempi</span><span class="sxs-lookup"><span data-stu-id="4159f-139">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="4159f-140">Esempio 1.</span><span class="sxs-lookup"><span data-stu-id="4159f-140">Example 1.</span></span> <span data-ttu-id="4159f-141">Ridefinire il mapping 1D</span><span class="sxs-lookup"><span data-stu-id="4159f-141">1D remapping</span></span>

```
InputDimensionCount: 2
IndicesDimensionCount: 2
BatchDimensionCount: 0

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping-with-batch-count"></a><span data-ttu-id="4159f-142">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="4159f-142">Example 2.</span></span> <span data-ttu-id="4159f-143">Ridefinire il mapping 2D con il numero di batch</span><span class="sxs-lookup"><span data-stu-id="4159f-143">2D remapping with batch count</span></span>

```
InputDimensionCount: 3
IndicesDimensionCount: 3
BatchDimensionCount: 1

// 3 batches.
InputTensor: (Sizes:{1, 3,2,2}, DataType:FLOAT32)
    [
        [[[0,1],[2,3]],   // batch 0
         [[4,5],[6,7]],   // batch 1
         [[8,9],[10,11]]] // batch 2
    ]

// A 3x2 array of 2D tuples indexing into InputTensor.
// e.g. a tuple of <1,0> in batch 1 corresponds to input value 6.
IndicesTensor: (Sizes:{1, 3,2,2}, DataType:UINT32)
    [
        [[[0,0],[1,1]],
         [[1,1],[0,0]],
         [[0,1],[1,0]]]
    ]

// output[batch, x] = input[batch, indices[batch, x, 0], indices[batch, x, 1]]
OutputTensor: (Sizes:{1,1, 3,2}, DataType:FLOAT32)
    [[
        [[0,3],
         [7,4],
         [9,10]]
    ]]
```

## <a name="availability"></a><span data-ttu-id="4159f-144">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="4159f-144">Availability</span></span>
<span data-ttu-id="4159f-145">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="4159f-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="4159f-146">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="4159f-146">Tensor constraints</span></span>
* <span data-ttu-id="4159f-147">*IndicisTensor,* *InputTensor* e *OutputTensor* devono avere lo stesso *DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="4159f-147">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="4159f-148">*InputTensor* e *OutputTensor* devono avere lo stesso *Tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="4159f-148">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="4159f-149">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="4159f-149">Tensor support</span></span>
| <span data-ttu-id="4159f-150">Tensore</span><span class="sxs-lookup"><span data-stu-id="4159f-150">Tensor</span></span> | <span data-ttu-id="4159f-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="4159f-151">Kind</span></span> | <span data-ttu-id="4159f-152">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="4159f-152">Supported dimension counts</span></span> | <span data-ttu-id="4159f-153">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="4159f-153">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="4159f-154">InputTensor</span><span class="sxs-lookup"><span data-stu-id="4159f-154">InputTensor</span></span> | <span data-ttu-id="4159f-155">Input</span><span class="sxs-lookup"><span data-stu-id="4159f-155">Input</span></span> | <span data-ttu-id="4159f-156">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="4159f-156">1 to 8</span></span> | <span data-ttu-id="4159f-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="4159f-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="4159f-158">IndicisTensor</span><span class="sxs-lookup"><span data-stu-id="4159f-158">IndicesTensor</span></span> | <span data-ttu-id="4159f-159">Input</span><span class="sxs-lookup"><span data-stu-id="4159f-159">Input</span></span> | <span data-ttu-id="4159f-160">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="4159f-160">1 to 8</span></span> | <span data-ttu-id="4159f-161">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="4159f-161">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="4159f-162">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="4159f-162">OutputTensor</span></span> | <span data-ttu-id="4159f-163">Output</span><span class="sxs-lookup"><span data-stu-id="4159f-163">Output</span></span> | <span data-ttu-id="4159f-164">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="4159f-164">1 to 8</span></span> | <span data-ttu-id="4159f-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="4159f-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="4159f-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4159f-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4159f-167">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="4159f-167">**Header**</span></span> | <span data-ttu-id="4159f-168">directml.h</span><span class="sxs-lookup"><span data-stu-id="4159f-168">directml.h</span></span> |
