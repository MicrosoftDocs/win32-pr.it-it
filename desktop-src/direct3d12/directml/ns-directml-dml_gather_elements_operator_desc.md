---
UID: NS:directml.DML_GATHER_ELEMENTS_OPERATOR_DESC
title: DML_GATHER_ELEMENTS_OPERATOR_DESC
description: Raccoglie gli elementi dal tensore di input lungo l'asse specificato usando il tensore degli indici per eseguire di nuovo il mapping all'input.
helpviewer_keywords:
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- DML_GATHER_ELEMENTS_OPERATOR_DESC structure
- direct3d12.dml_gather_elements_operator_desc
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.openlocfilehash: 89a4f2017f6adec8cce206e9261eb0fa6563e94c
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417720"
---
# <a name="dml_gather_elements_operator_desc-structure-directmlh"></a><span data-ttu-id="e2ca0-103">DML_GATHER_ELEMENTS_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="e2ca0-103">DML_GATHER_ELEMENTS_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e2ca0-104">Raccoglie gli elementi dal tensore di input lungo l'asse specificato usando il tensore degli indici per eseguire di nuovo il mapping all'input.</span><span class="sxs-lookup"><span data-stu-id="e2ca0-104">Gathers elements from the input tensor along the given axis using the indices tensor to remap into the input.</span></span> <span data-ttu-id="e2ca0-105">Questo operatore esegue lo pseudocodice seguente, con il comportamento esatto dipendente dall'asse, dal conteggio delle dimensioni di input e dal conteggio delle dimensioni degli indici.</span><span class="sxs-lookup"><span data-stu-id="e2ca0-105">This operator performs the following pseudocode, with the exact behavior dependent on the axis, input dimension count, and indices dimension count.</span></span>

```
output[i, j, k, ...] = input[index[i, j, k, ...], j, k, ...] // if axis == 0
output[i, j, k, ...] = input[i, index[i, j, k, ...], k, ...] // if axis == 1
output[i, j, k, ...] = input[i, j, index[i, j, k, ...], ...] // if axis == 2
...
```

> [!IMPORTANT]
> <span data-ttu-id="e2ca0-106">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="e2ca0-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e2ca0-107">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="e2ca0-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2ca0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2ca0-108">Syntax</span></span>
```cpp
struct DML_GATHER_ELEMENTS_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="e2ca0-109">Members</span><span class="sxs-lookup"><span data-stu-id="e2ca0-109">Members</span></span>

`InputTensor`

<span data-ttu-id="e2ca0-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e2ca0-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e2ca0-111">Tensore da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="e2ca0-111">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="e2ca0-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e2ca0-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e2ca0-113">Indici nel tensore di input lungo l'asse attivo.</span><span class="sxs-lookup"><span data-stu-id="e2ca0-113">The indices into the input tensor along the active axis.</span></span> <span data-ttu-id="e2ca0-114">Le *dimensioni devono* corrispondere a *InputTensor.Sizes per* ogni dimensione ad eccezione di *Axis.*</span><span class="sxs-lookup"><span data-stu-id="e2ca0-114">The *Sizes* must match *InputTensor.Sizes* for every dimension except *Axis*.</span></span>

<span data-ttu-id="e2ca0-115">A partire `DML_FEATURE_LEVEL_3_0` da , questo operatore supporta valori di indice negativi quando si usa un tipo integrale con segno con questo tensore.</span><span class="sxs-lookup"><span data-stu-id="e2ca0-115">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="e2ca0-116">Gli indici negativi vengono interpretati come relativi alla fine della dimensione dell'asse.</span><span class="sxs-lookup"><span data-stu-id="e2ca0-116">Negative indices are interpreted as being relative to the end of the axis dimension.</span></span> <span data-ttu-id="e2ca0-117">Ad esempio, un indice -1 fa riferimento all'ultimo elemento lungo tale dimensione.</span><span class="sxs-lookup"><span data-stu-id="e2ca0-117">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="e2ca0-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e2ca0-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e2ca0-119">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="e2ca0-119">The tensor to write the results to.</span></span> <span data-ttu-id="e2ca0-120">Le *dimensioni* devono corrispondere *a IndicesTensor.Sizes e* *DataType* deve corrispondere *a InputTensor.DataType*.</span><span class="sxs-lookup"><span data-stu-id="e2ca0-120">The *Sizes* must match *IndicesTensor.Sizes*, and *DataType* must match *InputTensor.DataType*.</span></span>


`Axis`

<span data-ttu-id="e2ca0-121">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="e2ca0-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="e2ca0-122">Dimensione dell'asse *di InputTensor* da raccogliere, che va da `[0, *InputTensor.DimensionCount*)` .</span><span class="sxs-lookup"><span data-stu-id="e2ca0-122">The axis dimension of *InputTensor* to gather along, ranging `[0, *InputTensor.DimensionCount*)`.</span></span>

## <a name="examples"></a><span data-ttu-id="e2ca0-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="e2ca0-123">Examples</span></span>

```
Axis = 0

InputTensor: (Sizes:{3,3}, DataType:FLOAT32)
    [[1, 2, 3],
     [4, 5, 6],
     [7, 8, 9]]

IndicesTensor: (Sizes:{2,3}, DataType:UINT32)
    [[1, 2, 0],
     [2, 0, 0]]

// output[y, x] = input[indices[y, x], x]
OutputTensor: (Sizes:{2,3}, DataType:UINT32)
    [[4, 8, 3], // select elements vertically from data
     [7, 2, 3]]
```

## <a name="availability"></a><span data-ttu-id="e2ca0-124">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="e2ca0-124">Availability</span></span>
<span data-ttu-id="e2ca0-125">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="e2ca0-125">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e2ca0-126">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="e2ca0-126">Tensor constraints</span></span>
* <span data-ttu-id="e2ca0-127">`IndicesTensor`, *InputTensor* e *OutputTensor* devono avere lo stesso *valore di DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="e2ca0-127">`IndicesTensor`, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="e2ca0-128">*InputTensor* e *OutputTensor* devono avere lo stesso *tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="e2ca0-128">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e2ca0-129">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="e2ca0-129">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="e2ca0-130">DML_FEATURE_LEVEL_3_0 e successive</span><span class="sxs-lookup"><span data-stu-id="e2ca0-130">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="e2ca0-131">Tensore</span><span class="sxs-lookup"><span data-stu-id="e2ca0-131">Tensor</span></span> | <span data-ttu-id="e2ca0-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2ca0-132">Kind</span></span> | <span data-ttu-id="e2ca0-133">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="e2ca0-133">Supported dimension counts</span></span> | <span data-ttu-id="e2ca0-134">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="e2ca0-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e2ca0-135">InputTensor</span><span class="sxs-lookup"><span data-stu-id="e2ca0-135">InputTensor</span></span> | <span data-ttu-id="e2ca0-136">Input</span><span class="sxs-lookup"><span data-stu-id="e2ca0-136">Input</span></span> | <span data-ttu-id="e2ca0-137">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e2ca0-137">1 to 8</span></span> | <span data-ttu-id="e2ca0-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e2ca0-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e2ca0-139">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="e2ca0-139">IndicesTensor</span></span> | <span data-ttu-id="e2ca0-140">Input</span><span class="sxs-lookup"><span data-stu-id="e2ca0-140">Input</span></span> | <span data-ttu-id="e2ca0-141">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e2ca0-141">1 to 8</span></span> | <span data-ttu-id="e2ca0-142">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="e2ca0-142">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="e2ca0-143">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e2ca0-143">OutputTensor</span></span> | <span data-ttu-id="e2ca0-144">Output</span><span class="sxs-lookup"><span data-stu-id="e2ca0-144">Output</span></span> | <span data-ttu-id="e2ca0-145">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e2ca0-145">1 to 8</span></span> | <span data-ttu-id="e2ca0-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e2ca0-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="e2ca0-147">DML_FEATURE_LEVEL_2_1 e successive</span><span class="sxs-lookup"><span data-stu-id="e2ca0-147">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="e2ca0-148">Tensore</span><span class="sxs-lookup"><span data-stu-id="e2ca0-148">Tensor</span></span> | <span data-ttu-id="e2ca0-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2ca0-149">Kind</span></span> | <span data-ttu-id="e2ca0-150">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="e2ca0-150">Supported dimension counts</span></span> | <span data-ttu-id="e2ca0-151">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="e2ca0-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e2ca0-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="e2ca0-152">InputTensor</span></span> | <span data-ttu-id="e2ca0-153">Input</span><span class="sxs-lookup"><span data-stu-id="e2ca0-153">Input</span></span> | <span data-ttu-id="e2ca0-154">4</span><span class="sxs-lookup"><span data-stu-id="e2ca0-154">4</span></span> | <span data-ttu-id="e2ca0-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e2ca0-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e2ca0-156">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="e2ca0-156">IndicesTensor</span></span> | <span data-ttu-id="e2ca0-157">Input</span><span class="sxs-lookup"><span data-stu-id="e2ca0-157">Input</span></span> | <span data-ttu-id="e2ca0-158">4</span><span class="sxs-lookup"><span data-stu-id="e2ca0-158">4</span></span> | <span data-ttu-id="e2ca0-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="e2ca0-159">UINT32</span></span> |
| <span data-ttu-id="e2ca0-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e2ca0-160">OutputTensor</span></span> | <span data-ttu-id="e2ca0-161">Output</span><span class="sxs-lookup"><span data-stu-id="e2ca0-161">Output</span></span> | <span data-ttu-id="e2ca0-162">4</span><span class="sxs-lookup"><span data-stu-id="e2ca0-162">4</span></span> | <span data-ttu-id="e2ca0-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e2ca0-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="e2ca0-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2ca0-164">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e2ca0-165">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="e2ca0-165">**Header**</span></span> | <span data-ttu-id="e2ca0-166">directml.h</span><span class="sxs-lookup"><span data-stu-id="e2ca0-166">directml.h</span></span> |