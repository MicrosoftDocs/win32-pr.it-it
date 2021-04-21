---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: Inverte gli elementi di una o più *sottosequenze* di un tensore. Il set di sottosequenze da invertire viene scelto in base all'asse e alle lunghezze di sequenza specificati.
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
ms.openlocfilehash: 3deddea3d60db1a8689ceabfac92ff17393b7606
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803997"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a><span data-ttu-id="2d0f5-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="2d0f5-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="2d0f5-105">Inverte gli elementi di una o più *sottosequenze di* un tensore.</span><span class="sxs-lookup"><span data-stu-id="2d0f5-105">Reverses the elements of one or more *subsequences* of a tensor.</span></span> <span data-ttu-id="2d0f5-106">Il set di sottosequenze da invertire viene scelto in base all'asse e alle lunghezze di sequenza specificati.</span><span class="sxs-lookup"><span data-stu-id="2d0f5-106">The set of subsequences to be reversed is chosen based on the provided axis and sequence lengths.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d0f5-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="2d0f5-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="2d0f5-108">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="2d0f5-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d0f5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d0f5-109">Syntax</span></span>
```cpp
struct DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *SequenceLengthsTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="2d0f5-110">Members</span><span class="sxs-lookup"><span data-stu-id="2d0f5-110">Members</span></span>

`InputTensor`

<span data-ttu-id="2d0f5-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2d0f5-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2d0f5-112">Tensore di input contenente gli elementi da invertire.</span><span class="sxs-lookup"><span data-stu-id="2d0f5-112">The input tensor containing elements to be reversed.</span></span>


`SequenceLengthsTensor`

<span data-ttu-id="2d0f5-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2d0f5-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2d0f5-114">Tensore contenente un valore per ogni sottosequenza da invertire, indicando la lunghezza negli elementi di tale sottosequenza.</span><span class="sxs-lookup"><span data-stu-id="2d0f5-114">A tensor containing a value for each subsequence to be reversed, denoting the length in elements of that subsequence.</span></span> <span data-ttu-id="2d0f5-115">Vengono invertiti solo gli elementi all'interno della lunghezza della sottosequenza. gli elementi rimanenti lungo tale asse vengono copiati nell'output senza modifiche.</span><span class="sxs-lookup"><span data-stu-id="2d0f5-115">Only the elements within the length of the subsequence are reversed; the remaining elements along that axis are copied to the output unchanged.</span></span>

<span data-ttu-id="2d0f5-116">Questo tensore deve avere dimensioni e conteggio delle dimensioni uguali a *InputTensor* *,* ad eccezione della dimensione specificata dal *parametro Axis.*</span><span class="sxs-lookup"><span data-stu-id="2d0f5-116">This tensor must have dimension count and sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter.</span></span> <span data-ttu-id="2d0f5-117">Le dimensioni della *dimensione Asse* devono essere 1.</span><span class="sxs-lookup"><span data-stu-id="2d0f5-117">The size of the *Axis* dimension must be 1.</span></span> <span data-ttu-id="2d0f5-118">Ad esempio, se *InputTensor* ha dimensioni e Axis è 1, le dimensioni di `{2,3,4,5}` *SequenceLengthsTensor* devono essere  `{2,1,4,5}` .</span><span class="sxs-lookup"><span data-stu-id="2d0f5-118">For example if the *InputTensor* has sizes of `{2,3,4,5}`, and *Axis* is 1, then the sizes of the *SequenceLengthsTensor* must be `{2,1,4,5}`.</span></span>

<span data-ttu-id="2d0f5-119">Se la lunghezza di una sottosequenza supera il numero massimo di elementi lungo tale asse, questo operatore si comporta come se il valore fosse limitato al massimo.</span><span class="sxs-lookup"><span data-stu-id="2d0f5-119">If the length of a subsequence exceeds the maximum number of elements along that axis, then this operator behaves as if the value were clamped to the maximum.</span></span>


`OutputTensor`

<span data-ttu-id="2d0f5-120">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2d0f5-120">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2d0f5-121">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="2d0f5-121">The output tensor to write the results to.</span></span> <span data-ttu-id="2d0f5-122">Questo tensore deve avere le stesse dimensioni e tipo di dati di *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="2d0f5-122">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="2d0f5-123">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="2d0f5-123">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="2d0f5-124">Indice della dimensione su cui invertire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="2d0f5-124">The index of the dimension to reverse elements over.</span></span> <span data-ttu-id="2d0f5-125">Questo valore deve essere minore di DimensionCount di *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="2d0f5-125">This value must be less than the DimensionCount of the *InputTensor*.</span></span>

## <a name="examples"></a><span data-ttu-id="2d0f5-126">Esempi</span><span class="sxs-lookup"><span data-stu-id="2d0f5-126">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="2d0f5-127">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2d0f5-127">Example 1</span></span>

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

### <a name="example-2-reversing-along-a-different-axis"></a><span data-ttu-id="2d0f5-128">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="2d0f5-128">Example 2.</span></span> <span data-ttu-id="2d0f5-129">Invertimento lungo un asse diverso</span><span class="sxs-lookup"><span data-stu-id="2d0f5-129">Reversing along a different axis</span></span>

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

## <a name="availability"></a><span data-ttu-id="2d0f5-130">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="2d0f5-130">Availability</span></span>
<span data-ttu-id="2d0f5-131">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="2d0f5-131">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="2d0f5-132">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="2d0f5-132">Tensor constraints</span></span>
* <span data-ttu-id="2d0f5-133">*InputTensor,* *OutputTensor* e *SequenceLengthsTensor* devono avere lo stesso *dimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="2d0f5-133">*InputTensor*, *OutputTensor*, and *SequenceLengthsTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="2d0f5-134">*InputTensor* e *OutputTensor* devono avere lo stesso *tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="2d0f5-134">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="2d0f5-135">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="2d0f5-135">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="2d0f5-136">DML_FEATURE_LEVEL_3_0 e successive</span><span class="sxs-lookup"><span data-stu-id="2d0f5-136">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="2d0f5-137">Tensore</span><span class="sxs-lookup"><span data-stu-id="2d0f5-137">Tensor</span></span> | <span data-ttu-id="2d0f5-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d0f5-138">Kind</span></span> | <span data-ttu-id="2d0f5-139">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="2d0f5-139">Supported dimension counts</span></span> | <span data-ttu-id="2d0f5-140">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="2d0f5-140">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="2d0f5-141">InputTensor</span><span class="sxs-lookup"><span data-stu-id="2d0f5-141">InputTensor</span></span> | <span data-ttu-id="2d0f5-142">Input</span><span class="sxs-lookup"><span data-stu-id="2d0f5-142">Input</span></span> | <span data-ttu-id="2d0f5-143">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="2d0f5-143">4 to 5</span></span> | <span data-ttu-id="2d0f5-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2d0f5-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="2d0f5-145">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="2d0f5-145">SequenceLengthsTensor</span></span> | <span data-ttu-id="2d0f5-146">Input</span><span class="sxs-lookup"><span data-stu-id="2d0f5-146">Input</span></span> | <span data-ttu-id="2d0f5-147">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="2d0f5-147">4 to 5</span></span> | <span data-ttu-id="2d0f5-148">UINT32</span><span class="sxs-lookup"><span data-stu-id="2d0f5-148">UINT32</span></span> |
| <span data-ttu-id="2d0f5-149">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="2d0f5-149">OutputTensor</span></span> | <span data-ttu-id="2d0f5-150">Output</span><span class="sxs-lookup"><span data-stu-id="2d0f5-150">Output</span></span> | <span data-ttu-id="2d0f5-151">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="2d0f5-151">4 to 5</span></span> | <span data-ttu-id="2d0f5-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2d0f5-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="2d0f5-153">DML_FEATURE_LEVEL_2_1 e successive</span><span class="sxs-lookup"><span data-stu-id="2d0f5-153">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="2d0f5-154">Tensore</span><span class="sxs-lookup"><span data-stu-id="2d0f5-154">Tensor</span></span> | <span data-ttu-id="2d0f5-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d0f5-155">Kind</span></span> | <span data-ttu-id="2d0f5-156">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="2d0f5-156">Supported dimension counts</span></span> | <span data-ttu-id="2d0f5-157">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="2d0f5-157">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="2d0f5-158">InputTensor</span><span class="sxs-lookup"><span data-stu-id="2d0f5-158">InputTensor</span></span> | <span data-ttu-id="2d0f5-159">Input</span><span class="sxs-lookup"><span data-stu-id="2d0f5-159">Input</span></span> | <span data-ttu-id="2d0f5-160">4</span><span class="sxs-lookup"><span data-stu-id="2d0f5-160">4</span></span> | <span data-ttu-id="2d0f5-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2d0f5-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="2d0f5-162">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="2d0f5-162">SequenceLengthsTensor</span></span> | <span data-ttu-id="2d0f5-163">Input</span><span class="sxs-lookup"><span data-stu-id="2d0f5-163">Input</span></span> | <span data-ttu-id="2d0f5-164">4</span><span class="sxs-lookup"><span data-stu-id="2d0f5-164">4</span></span> | <span data-ttu-id="2d0f5-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="2d0f5-165">UINT32</span></span> |
| <span data-ttu-id="2d0f5-166">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="2d0f5-166">OutputTensor</span></span> | <span data-ttu-id="2d0f5-167">Output</span><span class="sxs-lookup"><span data-stu-id="2d0f5-167">Output</span></span> | <span data-ttu-id="2d0f5-168">4</span><span class="sxs-lookup"><span data-stu-id="2d0f5-168">4</span></span> | <span data-ttu-id="2d0f5-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2d0f5-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="2d0f5-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d0f5-170">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2d0f5-171">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="2d0f5-171">**Header**</span></span> | <span data-ttu-id="2d0f5-172">directml.h</span><span class="sxs-lookup"><span data-stu-id="2d0f5-172">directml.h</span></span> |