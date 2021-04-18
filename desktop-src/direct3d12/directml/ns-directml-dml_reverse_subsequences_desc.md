---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: Inverte gli elementi di una o più *sottosequenze* di un tensore. Il set di sottosequenze da invertire viene scelto in base all'asse e alle lunghezze della sequenza specificati.
helpviewer_keywords:
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure
- direct3d12.dml_reverse_subsequences_operator_desc
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.openlocfilehash: 5baf16c5acd1ce5c5f44e68420e93aabaa276ea7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320400"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a><span data-ttu-id="0b493-104">Struttura DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="0b493-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="0b493-105">Inverte gli elementi di una o più *sottosequenze* di un tensore.</span><span class="sxs-lookup"><span data-stu-id="0b493-105">Reverses the elements of one or more *subsequences* of a tensor.</span></span> <span data-ttu-id="0b493-106">Il set di sottosequenze da invertire viene scelto in base all'asse e alle lunghezze della sequenza specificati.</span><span class="sxs-lookup"><span data-stu-id="0b493-106">The set of subsequences to be reversed is chosen based on the provided axis and sequence lengths.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b493-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="0b493-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="0b493-108">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="0b493-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b493-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b493-109">Syntax</span></span>
```cpp
struct DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *SequenceLengthsTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="0b493-110">Members</span><span class="sxs-lookup"><span data-stu-id="0b493-110">Members</span></span>

`InputTensor`

<span data-ttu-id="0b493-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0b493-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0b493-112">Il tensore di input contenente gli elementi da invertire.</span><span class="sxs-lookup"><span data-stu-id="0b493-112">The input tensor containing elements to be reversed.</span></span>


`SequenceLengthsTensor`

<span data-ttu-id="0b493-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0b493-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0b493-114">Un tensore contenente un valore per ogni sottosequenza da invertire, che indica la lunghezza in elementi della sottosequenza.</span><span class="sxs-lookup"><span data-stu-id="0b493-114">A tensor containing a value for each subsequence to be reversed, denoting the length in elements of that subsequence.</span></span> <span data-ttu-id="0b493-115">Solo gli elementi all'interno della lunghezza della sottosequenza vengono invertiti; gli elementi rimanenti lungo tale asse vengono copiati nell'output senza modifiche.</span><span class="sxs-lookup"><span data-stu-id="0b493-115">Only the elements within the length of the subsequence are reversed; the remaining elements along that axis are copied to the output unchanged.</span></span>

<span data-ttu-id="0b493-116">Questo tensore deve avere un numero di dimensioni e dimensioni uguali a *InputTensor*, *ad eccezione* della dimensione specificata dal parametro *Axis* .</span><span class="sxs-lookup"><span data-stu-id="0b493-116">This tensor must have dimension count and sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter.</span></span> <span data-ttu-id="0b493-117">La dimensione della dimensione dell' *asse* deve essere 1.</span><span class="sxs-lookup"><span data-stu-id="0b493-117">The size of the *Axis* dimension must be 1.</span></span> <span data-ttu-id="0b493-118">Se, ad esempio, il *InputTensor* ha dimensioni di `{2,3,4,5}` e *Axis* è 1, le dimensioni di *SequenceLengthsTensor* devono essere `{2,1,4,5}` .</span><span class="sxs-lookup"><span data-stu-id="0b493-118">For example if the *InputTensor* has sizes of `{2,3,4,5}`, and *Axis* is 1, then the sizes of the *SequenceLengthsTensor* must be `{2,1,4,5}`.</span></span>

<span data-ttu-id="0b493-119">Se la lunghezza di una sottosequenza supera il numero massimo di elementi lungo tale asse, questo operatore si comporta come se il valore fosse stato fissato al massimo.</span><span class="sxs-lookup"><span data-stu-id="0b493-119">If the length of a subsequence exceeds the maximum number of elements along that axis, then this operator behaves as if the value were clamped to the maximum.</span></span>


`OutputTensor`

<span data-ttu-id="0b493-120">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0b493-120">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0b493-121">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="0b493-121">The output tensor to write the results to.</span></span> <span data-ttu-id="0b493-122">Questo tensore deve avere le stesse dimensioni e il tipo di dati di *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="0b493-122">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="0b493-123">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="0b493-123">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="0b493-124">Indice della dimensione su cui invertire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="0b493-124">The index of the dimension to reverse elements over.</span></span> <span data-ttu-id="0b493-125">Questo valore deve essere minore del valore di DimensionCount di *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="0b493-125">This value must be less than the DimensionCount of the *InputTensor*.</span></span>

## <a name="examples"></a><span data-ttu-id="0b493-126">Esempi</span><span class="sxs-lookup"><span data-stu-id="0b493-126">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="0b493-127">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0b493-127">Example 1</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,3,1}, DataType:UINT32)
[[[[2],
   [4],
   [3]]]]

Axis: 3

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  4],
   [ 8,  7,  6,  5],
   [11, 10,  9, 12]]]]
```

### <a name="example-2-reversing-along-a-different-axis"></a><span data-ttu-id="0b493-128">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="0b493-128">Example 2.</span></span> <span data-ttu-id="0b493-129">Inversione lungo un asse diverso</span><span class="sxs-lookup"><span data-stu-id="0b493-129">Reversing along a different axis</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,1,4}, DataType:UINT32)
[[[[2, 3, 1, 0]]]]

Axis: 2

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[5, 10,  3,  4], // Notice that sequence lengths of 1 and 0 are effective nops
   [1,  6,  7,  8],
   [9,  2, 11, 12]]]]
```

## <a name="availability"></a><span data-ttu-id="0b493-130">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="0b493-130">Availability</span></span>
<span data-ttu-id="0b493-131">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="0b493-131">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="0b493-132">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="0b493-132">Tensor constraints</span></span>
* <span data-ttu-id="0b493-133">*InputTensor*, *OutputTensor* e *SequenceLengthsTensor* devono avere lo stesso *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="0b493-133">*InputTensor*, *OutputTensor*, and *SequenceLengthsTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="0b493-134">*InputTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="0b493-134">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="0b493-135">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="0b493-135">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="0b493-136">DML_FEATURE_LEVEL_3_0 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="0b493-136">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="0b493-137">Tensore</span><span class="sxs-lookup"><span data-stu-id="0b493-137">Tensor</span></span> | <span data-ttu-id="0b493-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b493-138">Kind</span></span> | <span data-ttu-id="0b493-139">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="0b493-139">Supported dimension counts</span></span> | <span data-ttu-id="0b493-140">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="0b493-140">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="0b493-141">InputTensor</span><span class="sxs-lookup"><span data-stu-id="0b493-141">InputTensor</span></span> | <span data-ttu-id="0b493-142">Input</span><span class="sxs-lookup"><span data-stu-id="0b493-142">Input</span></span> | <span data-ttu-id="0b493-143">da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="0b493-143">4 to 5</span></span> | <span data-ttu-id="0b493-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="0b493-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="0b493-145">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="0b493-145">SequenceLengthsTensor</span></span> | <span data-ttu-id="0b493-146">Input</span><span class="sxs-lookup"><span data-stu-id="0b493-146">Input</span></span> | <span data-ttu-id="0b493-147">da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="0b493-147">4 to 5</span></span> | <span data-ttu-id="0b493-148">UINT32</span><span class="sxs-lookup"><span data-stu-id="0b493-148">UINT32</span></span> |
| <span data-ttu-id="0b493-149">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="0b493-149">OutputTensor</span></span> | <span data-ttu-id="0b493-150">Output</span><span class="sxs-lookup"><span data-stu-id="0b493-150">Output</span></span> | <span data-ttu-id="0b493-151">da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="0b493-151">4 to 5</span></span> | <span data-ttu-id="0b493-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="0b493-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="0b493-153">DML_FEATURE_LEVEL_2_1 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="0b493-153">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="0b493-154">Tensore</span><span class="sxs-lookup"><span data-stu-id="0b493-154">Tensor</span></span> | <span data-ttu-id="0b493-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b493-155">Kind</span></span> | <span data-ttu-id="0b493-156">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="0b493-156">Supported dimension counts</span></span> | <span data-ttu-id="0b493-157">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="0b493-157">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="0b493-158">InputTensor</span><span class="sxs-lookup"><span data-stu-id="0b493-158">InputTensor</span></span> | <span data-ttu-id="0b493-159">Input</span><span class="sxs-lookup"><span data-stu-id="0b493-159">Input</span></span> | <span data-ttu-id="0b493-160">4</span><span class="sxs-lookup"><span data-stu-id="0b493-160">4</span></span> | <span data-ttu-id="0b493-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="0b493-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="0b493-162">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="0b493-162">SequenceLengthsTensor</span></span> | <span data-ttu-id="0b493-163">Input</span><span class="sxs-lookup"><span data-stu-id="0b493-163">Input</span></span> | <span data-ttu-id="0b493-164">4</span><span class="sxs-lookup"><span data-stu-id="0b493-164">4</span></span> | <span data-ttu-id="0b493-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="0b493-165">UINT32</span></span> |
| <span data-ttu-id="0b493-166">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="0b493-166">OutputTensor</span></span> | <span data-ttu-id="0b493-167">Output</span><span class="sxs-lookup"><span data-stu-id="0b493-167">Output</span></span> | <span data-ttu-id="0b493-168">4</span><span class="sxs-lookup"><span data-stu-id="0b493-168">4</span></span> | <span data-ttu-id="0b493-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="0b493-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="0b493-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b493-170">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0b493-171">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="0b493-171">**Header**</span></span> | <span data-ttu-id="0b493-172">directml. h</span><span class="sxs-lookup"><span data-stu-id="0b493-172">directml.h</span></span> |