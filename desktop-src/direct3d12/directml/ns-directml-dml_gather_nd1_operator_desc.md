---
UID: NS:directml.DML_GATHER_ND1_OPERATOR_DESC
title: DML_GATHER_ND1_OPERATOR_DESC
description: Raccoglie gli elementi dal tensore di input, usando il tensore indici per eseguire il mapping degli indici a interi sottoblocchi dell'input. | DML_GATHER_ND1_OPERATOR_DESC
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
ms.openlocfilehash: dc7f33f50fa6a0c1cd2850b8e02aad30d75afeb1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321868"
---
# <a name="dml_gather_nd1_operator_desc-structure-directmlh"></a><span data-ttu-id="44fc7-104">Struttura DML_GATHER_ND1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="44fc7-104">DML_GATHER_ND1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="44fc7-105">Raccoglie gli elementi dal tensore di input, usando il tensore indici per eseguire il mapping degli indici a interi sottoblocchi dell'input.</span><span class="sxs-lookup"><span data-stu-id="44fc7-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="44fc7-106">Questo operatore esegue lo pseudocodice seguente, dove "..." rappresenta una serie di coordinate, con il comportamento esatto dipendente dal conteggio delle dimensioni del batch, dell'input e degli indici.</span><span class="sxs-lookup"><span data-stu-id="44fc7-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the batch, input, and indices dimension count.</span></span>

```
output[batch, ...] = input[batch, indices[batch, ...], ...]
```

> [!IMPORTANT]
> <span data-ttu-id="44fc7-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="44fc7-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="44fc7-108">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="44fc7-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="44fc7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44fc7-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="44fc7-110">Members</span><span class="sxs-lookup"><span data-stu-id="44fc7-110">Members</span></span>

`InputTensor`

<span data-ttu-id="44fc7-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="44fc7-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="44fc7-112">Tensore da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="44fc7-112">The tensor to read from.</span></span>

`IndicesTensor`

<span data-ttu-id="44fc7-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="44fc7-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="44fc7-114">Il tensore contenente gli indici.</span><span class="sxs-lookup"><span data-stu-id="44fc7-114">The tensor containing the indices.</span></span> <span data-ttu-id="44fc7-115">Il *DimensionCount* di questo tensore deve corrispondere a *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="44fc7-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="44fc7-116">L'ultima dimensione di *IndicesTensor* è in realtà il numero di coordinate per tupla dell'indice e non può superare *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="44fc7-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="44fc7-117">Ad esempio, un tensore indici di *dimensioni* `{1,4,5,2}` con *IndicesDimensionCount* = 3 indica una matrice 4x5 di tuple a 2 Coordinate che indicizzano in *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="44fc7-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="44fc7-118">A partire da `DML_FEATURE_LEVEL_3_0` , questo operatore supporta valori di indice negativi quando si usa un tipo integrale con segno con questo tensore.</span><span class="sxs-lookup"><span data-stu-id="44fc7-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="44fc7-119">Gli indici negativi vengono interpretati come relativi alla fine della rispettiva dimensione.</span><span class="sxs-lookup"><span data-stu-id="44fc7-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="44fc7-120">Ad esempio, un indice di-1 si riferisce all'ultimo elemento lungo la dimensione.</span><span class="sxs-lookup"><span data-stu-id="44fc7-120">For example, an index of -1 refers to the last element along that dimension.</span></span>

`OutputTensor`

<span data-ttu-id="44fc7-121">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="44fc7-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="44fc7-122">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="44fc7-122">The tensor to write the results to.</span></span> <span data-ttu-id="44fc7-123">Il *DimensionCount* e il *tipo* di dati di questo tensore devono corrispondere a *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="44fc7-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="44fc7-124">Il *OutputTensor. sizes* previsto è la concatenazione dei segmenti iniziali *IndicesTensor. sizes* e del segmento finale *InputTensor. sizes* , che produce quanto segue.</span><span class="sxs-lookup"><span data-stu-id="44fc7-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment, which yields the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="44fc7-125">Le dimensioni sono allineate a destra, con 1 valori iniziali anteposti se necessario per soddisfare *OutputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="44fc7-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="44fc7-126">Ecco un esempio.</span><span class="sxs-lookup"><span data-stu-id="44fc7-126">Here's an example.</span></span>

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

<span data-ttu-id="44fc7-127">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="44fc7-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="44fc7-128">Il numero di dimensioni di input effettive all'interno di *InputTensor* dopo aver ignorato gli eventuali valori iniziali irrilevanti `[1, *InputTensor.DimensionCount*]` .</span><span class="sxs-lookup"><span data-stu-id="44fc7-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="44fc7-129">Ad esempio, dato *InputTensor. sizes*  =  `{1,1,4,6}` e `InputDimensionCount` = 3, gli indici significativi effettivi sono `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="44fc7-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`IndicesDimensionCount`

<span data-ttu-id="44fc7-130">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="44fc7-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="44fc7-131">Il numero di dimensioni effettive dell'indice all'interno di *IndicesTensor* dopo aver ignorato gli eventuali primitivi irrilevanti, che vanno da [1, *IndicesTensor. DimensionCount*].</span><span class="sxs-lookup"><span data-stu-id="44fc7-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="44fc7-132">Ad esempio, dato *IndicesTensor. sizes*  =  `{1,1,4,6}` e *IndicesDimensionCount* = 3, gli indici significativi effettivi sono `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="44fc7-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`BatchDimensionCount`

<span data-ttu-id="44fc7-133">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="44fc7-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="44fc7-134">Il numero di dimensioni all'interno di ogni tensore (*InputTensor*, *IndicesTensor*, *OutputTensor*) che sono considerati batch indipendenti, compresi tra [0, *InputTensor. DimensionCount*) e [0, *IndicesTensor. DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="44fc7-134">The number of dimensions within each tensor (*InputTensor*, *IndicesTensor*, *OutputTensor*) that are considered independent batches, ranging within both [0, *InputTensor.DimensionCount*) and [0, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="44fc7-135">Il numero di batch può essere 0, che implica un singolo batch.</span><span class="sxs-lookup"><span data-stu-id="44fc7-135">The batch count can be 0, implying a single batch.</span></span> <span data-ttu-id="44fc7-136">Ad esempio, date *IndicesTensor. sizes*  =  `{1,3,4,5,6,7}` e *IndicesDimensionCount* = 5 e `BatchDimensionCount` = 2, sono presenti batch `{3,4}` e indici significativi `{5,6,7}` .</span><span class="sxs-lookup"><span data-stu-id="44fc7-136">For example, given *IndicesTensor.Sizes* = `{1,3,4,5,6,7}`, and *IndicesDimensionCount* = 5 and `BatchDimensionCount` = 2, there are batches `{3,4}` and meaningful indices `{5,6,7}`.</span></span>

## <a name="remarks"></a><span data-ttu-id="44fc7-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="44fc7-137">Remarks</span></span>
<span data-ttu-id="44fc7-138">**DML_GATHER_ND1_OPERATOR_DESC** aggiunge *BatchDimensionCount* ed è equivalente a [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) quando *BatchDimensionCount* = 0.</span><span class="sxs-lookup"><span data-stu-id="44fc7-138">**DML_GATHER_ND1_OPERATOR_DESC** adds *BatchDimensionCount*, and is equivalent to [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) when *BatchDimensionCount* = 0.</span></span>

## <a name="examples"></a><span data-ttu-id="44fc7-139">Esempi</span><span class="sxs-lookup"><span data-stu-id="44fc7-139">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="44fc7-140">Esempio 1.</span><span class="sxs-lookup"><span data-stu-id="44fc7-140">Example 1.</span></span> <span data-ttu-id="44fc7-141">1D (nuovo mapping)</span><span class="sxs-lookup"><span data-stu-id="44fc7-141">1D remapping</span></span>

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

### <a name="example-2-2d-remapping-with-batch-count"></a><span data-ttu-id="44fc7-142">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="44fc7-142">Example 2.</span></span> <span data-ttu-id="44fc7-143">rimappatura 2D con conteggio batch</span><span class="sxs-lookup"><span data-stu-id="44fc7-143">2D remapping with batch count</span></span>

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

## <a name="availability"></a><span data-ttu-id="44fc7-144">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="44fc7-144">Availability</span></span>
<span data-ttu-id="44fc7-145">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="44fc7-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="44fc7-146">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="44fc7-146">Tensor constraints</span></span>
* <span data-ttu-id="44fc7-147">*IndicesTensor*, *InputTensor* e *OutputTensor* devono avere lo stesso *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="44fc7-147">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="44fc7-148">*InputTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="44fc7-148">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="44fc7-149">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="44fc7-149">Tensor support</span></span>
| <span data-ttu-id="44fc7-150">Tensore</span><span class="sxs-lookup"><span data-stu-id="44fc7-150">Tensor</span></span> | <span data-ttu-id="44fc7-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="44fc7-151">Kind</span></span> | <span data-ttu-id="44fc7-152">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="44fc7-152">Supported dimension counts</span></span> | <span data-ttu-id="44fc7-153">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="44fc7-153">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="44fc7-154">InputTensor</span><span class="sxs-lookup"><span data-stu-id="44fc7-154">InputTensor</span></span> | <span data-ttu-id="44fc7-155">Input</span><span class="sxs-lookup"><span data-stu-id="44fc7-155">Input</span></span> | <span data-ttu-id="44fc7-156">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="44fc7-156">1 to 8</span></span> | <span data-ttu-id="44fc7-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="44fc7-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="44fc7-158">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="44fc7-158">IndicesTensor</span></span> | <span data-ttu-id="44fc7-159">Input</span><span class="sxs-lookup"><span data-stu-id="44fc7-159">Input</span></span> | <span data-ttu-id="44fc7-160">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="44fc7-160">1 to 8</span></span> | <span data-ttu-id="44fc7-161">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="44fc7-161">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="44fc7-162">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="44fc7-162">OutputTensor</span></span> | <span data-ttu-id="44fc7-163">Output</span><span class="sxs-lookup"><span data-stu-id="44fc7-163">Output</span></span> | <span data-ttu-id="44fc7-164">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="44fc7-164">1 to 8</span></span> | <span data-ttu-id="44fc7-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="44fc7-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="44fc7-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44fc7-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="44fc7-167">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="44fc7-167">**Header**</span></span> | <span data-ttu-id="44fc7-168">directml. h</span><span class="sxs-lookup"><span data-stu-id="44fc7-168">directml.h</span></span> |
