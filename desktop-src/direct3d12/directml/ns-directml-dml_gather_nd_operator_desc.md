---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Raccoglie gli elementi dal tensore di input, usando il tensore indici per eseguire il mapping degli indici a interi sottoblocchi dell'input. | DML_GATHER_ND_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND_OPERATOR_DESC
- DML_GATHER_ND_OPERATOR_DESC structure
- direct3d12.dml_gather_nd_operator_desc
- directml/DML_GATHER_ND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/31/2020
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
- DML_GATHER_ND_OPERATOR_DESC
- directml/DML_GATHER_ND_OPERATOR_DESC
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
- DML_GATHER_ND_OPERATOR_DESC
ms.openlocfilehash: 6a48fd19621bed100a13412dbb1992974d125323
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321867"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="bed83-104">Struttura DML_GATHER_ND_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="bed83-104">DML_GATHER_ND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="bed83-105">Raccoglie gli elementi dal tensore di input, usando il tensore indici per eseguire il mapping degli indici a interi sottoblocchi dell'input.</span><span class="sxs-lookup"><span data-stu-id="bed83-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="bed83-106">Questo operatore esegue lo pseudocodice seguente, dove "..." rappresenta una serie di coordinate, con il comportamento esatto dipendente dal conteggio delle dimensioni di input e indici.</span><span class="sxs-lookup"><span data-stu-id="bed83-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the input and indices dimension count.</span></span>

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> <span data-ttu-id="bed83-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="bed83-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="bed83-108">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="bed83-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bed83-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bed83-109">Syntax</span></span>
```cpp
struct DML_GATHER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="bed83-110">Members</span><span class="sxs-lookup"><span data-stu-id="bed83-110">Members</span></span>

`InputTensor`

<span data-ttu-id="bed83-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bed83-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bed83-112">Tensore da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="bed83-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="bed83-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bed83-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bed83-114">Il tensore contenente gli indici.</span><span class="sxs-lookup"><span data-stu-id="bed83-114">The tensor containing the indices.</span></span> <span data-ttu-id="bed83-115">Il *DimensionCount* di questo tensore deve corrispondere a *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="bed83-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="bed83-116">L'ultima dimensione di *IndicesTensor* è in realtà il numero di coordinate per tupla dell'indice e non può superare *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="bed83-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="bed83-117">Ad esempio, un tensore indici di *dimensioni* `{1,4,5,2}` con *IndicesDimensionCount* = 3 indica una matrice 4x5 di tuple a 2 Coordinate che indicizzano in *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="bed83-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="bed83-118">A partire da `DML_FEATURE_LEVEL_3_0` , questo operatore supporta valori di indice negativi quando si usa un tipo integrale con segno con questo tensore.</span><span class="sxs-lookup"><span data-stu-id="bed83-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="bed83-119">Gli indici negativi vengono interpretati come relativi alla fine della rispettiva dimensione.</span><span class="sxs-lookup"><span data-stu-id="bed83-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="bed83-120">Ad esempio, un indice di-1 si riferisce all'ultimo elemento lungo la dimensione.</span><span class="sxs-lookup"><span data-stu-id="bed83-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="bed83-121">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bed83-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bed83-122">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="bed83-122">The tensor to write the results to.</span></span> <span data-ttu-id="bed83-123">Il *DimensionCount* e il *tipo* di dati di questo tensore devono corrispondere a *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="bed83-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="bed83-124">Il *OutputTensor. sizes* previsto è la concatenazione dei segmenti iniziali *IndicesTensor. sizes* e del segmento finale *InputTensor. sizes* da produrre:</span><span class="sxs-lookup"><span data-stu-id="bed83-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield:</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="bed83-125">Le dimensioni di output sono allineate a destra, con 1 valori iniziali anteposti, se necessario, per soddisfare fino a *OutputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="bed83-125">The output dimensions are right-aligned, with leading 1 values prepended if needed to satisfy up to *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="bed83-126">Ecco un esempio.</span><span class="sxs-lookup"><span data-stu-id="bed83-126">Here's an example.</span></span>

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

<span data-ttu-id="bed83-127">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="bed83-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="bed83-128">Il numero di dimensioni di input effettive all'interno di *InputTensor* dopo aver ignorato gli eventuali valori iniziali irrilevanti `[1, *InputTensor.DimensionCount*]` .</span><span class="sxs-lookup"><span data-stu-id="bed83-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="bed83-129">Ad esempio, dato *InputTensor. sizes*  =  `{1,1,4,6}` e `InputDimensionCount` = 3, gli indici significativi effettivi sono `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="bed83-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="bed83-130">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="bed83-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="bed83-131">Il numero di dimensioni effettive dell'indice all'interno di *IndicesTensor* dopo aver ignorato gli eventuali primitivi irrilevanti, che vanno da [1, *IndicesTensor. DimensionCount*].</span><span class="sxs-lookup"><span data-stu-id="bed83-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="bed83-132">Ad esempio, dato *IndicesTensor. sizes*  =  `{1,1,4,6}` e *IndicesDimensionCount* = 3, gli indici significativi effettivi sono `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="bed83-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

## <a name="examples"></a><span data-ttu-id="bed83-133">Esempi</span><span class="sxs-lookup"><span data-stu-id="bed83-133">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="bed83-134">Esempio 1.</span><span class="sxs-lookup"><span data-stu-id="bed83-134">Example 1.</span></span> <span data-ttu-id="bed83-135">1D (nuovo mapping)</span><span class="sxs-lookup"><span data-stu-id="bed83-135">1D remapping</span></span>

```
InputDimensionCount: 2
IndicesDimensionCount: 2

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping"></a><span data-ttu-id="bed83-136">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="bed83-136">Example 2.</span></span> <span data-ttu-id="bed83-137">rimappatura 2D</span><span class="sxs-lookup"><span data-stu-id="bed83-137">2D remapping</span></span>

```
InputDimensionCount: 3
IndicesDimensionCount: 2

InputTensor: (Sizes:{1, 2,2,2}, DataType:FLOAT32)
    [ [[[0,1],[2,3]],[[4,5],[6,7]]] ]

IndicesTensor: (Sizes:{1,1, 2,2}, DataType:UINT32)
    [[ [[0,1],[1,0]] ]]

// output[y, x] = input[indices[y, 0], indices[y, 1], x]
OutputTensor: (Sizes:{1,1, 2,2}, DataType:FLOAT32)
    [[ [[2,3],[4,5]] ]]
```


## <a name="remarks"></a><span data-ttu-id="bed83-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="bed83-138">Remarks</span></span>
<span data-ttu-id="bed83-139">Una versione più recente di questo operatore, `DML_OPERATOR_GATHER_ND1` , è stata introdotta in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="bed83-139">A newer version of this operator, `DML_OPERATOR_GATHER_ND1`, was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="availability"></a><span data-ttu-id="bed83-140">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="bed83-140">Availability</span></span>
<span data-ttu-id="bed83-141">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="bed83-141">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="bed83-142">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="bed83-142">Tensor constraints</span></span>
* <span data-ttu-id="bed83-143">*IndicesTensor*, *InputTensor* e *OutputTensor* devono avere lo stesso *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="bed83-143">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="bed83-144">*InputTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="bed83-144">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="bed83-145">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="bed83-145">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="bed83-146">DML_FEATURE_LEVEL_3_0 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="bed83-146">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="bed83-147">Tensore</span><span class="sxs-lookup"><span data-stu-id="bed83-147">Tensor</span></span> | <span data-ttu-id="bed83-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="bed83-148">Kind</span></span> | <span data-ttu-id="bed83-149">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="bed83-149">Supported dimension counts</span></span> | <span data-ttu-id="bed83-150">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="bed83-150">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="bed83-151">InputTensor</span><span class="sxs-lookup"><span data-stu-id="bed83-151">InputTensor</span></span> | <span data-ttu-id="bed83-152">Input</span><span class="sxs-lookup"><span data-stu-id="bed83-152">Input</span></span> | <span data-ttu-id="bed83-153">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="bed83-153">1 to 8</span></span> | <span data-ttu-id="bed83-154">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bed83-154">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bed83-155">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="bed83-155">IndicesTensor</span></span> | <span data-ttu-id="bed83-156">Input</span><span class="sxs-lookup"><span data-stu-id="bed83-156">Input</span></span> | <span data-ttu-id="bed83-157">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="bed83-157">1 to 8</span></span> | <span data-ttu-id="bed83-158">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="bed83-158">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="bed83-159">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="bed83-159">OutputTensor</span></span> | <span data-ttu-id="bed83-160">Output</span><span class="sxs-lookup"><span data-stu-id="bed83-160">Output</span></span> | <span data-ttu-id="bed83-161">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="bed83-161">1 to 8</span></span> | <span data-ttu-id="bed83-162">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bed83-162">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="bed83-163">DML_FEATURE_LEVEL_2_1 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="bed83-163">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="bed83-164">Tensore</span><span class="sxs-lookup"><span data-stu-id="bed83-164">Tensor</span></span> | <span data-ttu-id="bed83-165">Tipo</span><span class="sxs-lookup"><span data-stu-id="bed83-165">Kind</span></span> | <span data-ttu-id="bed83-166">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="bed83-166">Supported dimension counts</span></span> | <span data-ttu-id="bed83-167">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="bed83-167">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="bed83-168">InputTensor</span><span class="sxs-lookup"><span data-stu-id="bed83-168">InputTensor</span></span> | <span data-ttu-id="bed83-169">Input</span><span class="sxs-lookup"><span data-stu-id="bed83-169">Input</span></span> | <span data-ttu-id="bed83-170">4</span><span class="sxs-lookup"><span data-stu-id="bed83-170">4</span></span> | <span data-ttu-id="bed83-171">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bed83-171">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bed83-172">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="bed83-172">IndicesTensor</span></span> | <span data-ttu-id="bed83-173">Input</span><span class="sxs-lookup"><span data-stu-id="bed83-173">Input</span></span> | <span data-ttu-id="bed83-174">4</span><span class="sxs-lookup"><span data-stu-id="bed83-174">4</span></span> | <span data-ttu-id="bed83-175">UINT32</span><span class="sxs-lookup"><span data-stu-id="bed83-175">UINT32</span></span> |
| <span data-ttu-id="bed83-176">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="bed83-176">OutputTensor</span></span> | <span data-ttu-id="bed83-177">Output</span><span class="sxs-lookup"><span data-stu-id="bed83-177">Output</span></span> | <span data-ttu-id="bed83-178">4</span><span class="sxs-lookup"><span data-stu-id="bed83-178">4</span></span> | <span data-ttu-id="bed83-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bed83-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="bed83-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bed83-180">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="bed83-181">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="bed83-181">**Header**</span></span> | <span data-ttu-id="bed83-182">directml. h</span><span class="sxs-lookup"><span data-stu-id="bed83-182">directml.h</span></span> |
