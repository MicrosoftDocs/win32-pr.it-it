---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Seleziona gli elementi *K* più grandi o più piccoli da ogni sequenza lungo un asse di *InputTensor* e restituisce rispettivamente i valori e gli indici di tali elementi in *OutputValueTensor* e *OutputIndexTensor.*
helpviewer_keywords:
- DML_TOP_K1_OPERATOR_DESC
- DML_TOP_K1_OPERATOR_DESC structure
- direct3d12.dml_top_k1_operator_desc
- directml/DML_TOP_K1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_TOP_K1_OPERATOR_DESC
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
ms.openlocfilehash: 599541032e0f1711c0e747a4ca5906391849a932
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803823"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a><span data-ttu-id="4fa82-103">DML_TOP_K1_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="4fa82-103">DML_TOP_K1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="4fa82-104">Seleziona gli elementi *K* più grandi o più piccoli da ogni sequenza lungo un asse di *InputTensor* e restituisce rispettivamente i valori e gli indici di tali elementi in *OutputValueTensor* e *OutputIndexTensor.*</span><span class="sxs-lookup"><span data-stu-id="4fa82-104">Selects the largest or smallest *K* elements from each sequence along an axis of the *InputTensor*, and returns the values and indices of those elements in the *OutputValueTensor* and *OutputIndexTensor*, respectively.</span></span> <span data-ttu-id="4fa82-105">Una *sequenza* fa riferimento a uno dei set di elementi esistenti lungo la *dimensione Axis* di *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="4fa82-105">A *sequence* refers to one of the sets of elements that exist along the *Axis* dimension of the *InputTensor*.</span></span>

<span data-ttu-id="4fa82-106">È possibile scegliere se selezionare gli elementi K più grandi o gli elementi K più piccoli usando *AxisDirection.*</span><span class="sxs-lookup"><span data-stu-id="4fa82-106">The choice of whether to select the largest K elements or the smallest K elements can be controlled using *AxisDirection*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4fa82-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="4fa82-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="4fa82-108">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="4fa82-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4fa82-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4fa82-109">Syntax</span></span>
```cpp
struct DML_TOP_K1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputValueTensor;
  const DML_TENSOR_DESC *OutputIndexTensor;
  UINT                  Axis;
  UINT                  K;
  DML_AXIS_DIRECTION    AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="4fa82-110">Members</span><span class="sxs-lookup"><span data-stu-id="4fa82-110">Members</span></span>

`InputTensor`

<span data-ttu-id="4fa82-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4fa82-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4fa82-112">Tensore di input contenente gli elementi da selezionare.</span><span class="sxs-lookup"><span data-stu-id="4fa82-112">The input tensor containing elements to select.</span></span>

`OutputValueTensor`

<span data-ttu-id="4fa82-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4fa82-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4fa82-114">Tensore di output in cui scrivere i valori dei *primi K* elementi.</span><span class="sxs-lookup"><span data-stu-id="4fa82-114">The output tensor to write the values of the top *K* elements to.</span></span> <span data-ttu-id="4fa82-115">I primi *K* elementi vengono selezionati a seconda che siano il più grande o il più piccolo, a seconda del valore di *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="4fa82-115">The top *K* elements are selected based on whether they are the largest or the smallest, depending on the value of *AxisDirection*.</span></span> <span data-ttu-id="4fa82-116">Questo tensore deve avere dimensioni uguali a *InputTensor* *,* ad eccezione della dimensione specificata dal parametro *Axis,* che deve avere una dimensione uguale a *K*.</span><span class="sxs-lookup"><span data-stu-id="4fa82-116">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="4fa82-117">È *garantito* che i valori K selezionati da ogni sequenza di input siano ordinati in ordine decrescente (dal più grande al più piccolo) se *AxisDirection* è [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span><span class="sxs-lookup"><span data-stu-id="4fa82-117">The *K* values selected from each input sequence are guaranteed to be sorted descending (largest to smallest) if *AxisDirection* is [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span></span> <span data-ttu-id="4fa82-118">In caso contrario, è vero il contrario e viene garantito l'ordinamento crescente dei valori selezionati (dal più piccolo al più grande).</span><span class="sxs-lookup"><span data-stu-id="4fa82-118">Otherwise, the opposite is true and the values selected are guaranteed to be sorted ascending (smallest to largest).</span></span>

`OutputIndexTensor`

<span data-ttu-id="4fa82-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4fa82-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4fa82-120">Tensore di output in cui scrivere gli indici dei primi *K* elementi.</span><span class="sxs-lookup"><span data-stu-id="4fa82-120">The output tensor to write the indices of the top *K* elements to.</span></span> <span data-ttu-id="4fa82-121">Questo tensore deve avere dimensioni uguali a *InputTensor* *,* ad eccezione della dimensione specificata dal parametro *Axis,* che deve avere dimensioni uguali a *K*.</span><span class="sxs-lookup"><span data-stu-id="4fa82-121">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="4fa82-122">Gli indici restituiti in questo tensore vengono misurati rispetto all'inizio della sequenza (anziché all'inizio del tensore).</span><span class="sxs-lookup"><span data-stu-id="4fa82-122">The indices returned in this tensor are measured relative to the beginning of their sequence (as opposed to the beginning of the tensor).</span></span> <span data-ttu-id="4fa82-123">Ad esempio, un indice 0 fa sempre riferimento al primo elemento per tutte le sequenze in un asse.</span><span class="sxs-lookup"><span data-stu-id="4fa82-123">For example, an index of 0 always refers to the first element for all sequences in an axis.</span></span>

<span data-ttu-id="4fa82-124">Nei casi in cui due o più elementi nella parte superiore K hanno lo stesso valore ,ovvero quando è presente un'aezione, vengono inclusi gli indici di entrambi gli elementi e viene garantito l'ordinamento in base all'indice crescente degli elementi.</span><span class="sxs-lookup"><span data-stu-id="4fa82-124">In cases where two or more elements in the top-K have the same value (that is, when there is a tie), the indices of both elements are included, and are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="4fa82-125">Si noti che questo è vero indipendentemente dal valore di *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="4fa82-125">Note that this is true irrespective of the value of *AxisDirection*.</span></span>

`Axis`

<span data-ttu-id="4fa82-126">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4fa82-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4fa82-127">Indice della dimensione in cui selezionare gli elementi.</span><span class="sxs-lookup"><span data-stu-id="4fa82-127">The index of the dimension to select elements across.</span></span> <span data-ttu-id="4fa82-128">Questo valore deve essere minore di *DimensionCount* di *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="4fa82-128">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`K`

<span data-ttu-id="4fa82-129">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4fa82-129">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4fa82-130">Numero di elementi da selezionare.</span><span class="sxs-lookup"><span data-stu-id="4fa82-130">The number of elements to select.</span></span> <span data-ttu-id="4fa82-131">*K* deve essere maggiore di 0, ma minore del numero di elementi in *InputTensor* lungo la dimensione specificata da *Axis*.</span><span class="sxs-lookup"><span data-stu-id="4fa82-131">*K* must be greater than 0, but less than the number of elements in the *InputTensor* along the dimension specified by *Axis*.</span></span>

`AxisDirection`

<span data-ttu-id="4fa82-132">Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="4fa82-132">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="4fa82-133">Valore [dell'enumerazione DML_AXIS_DIRECTION.](./ne-directml-dml_axis_direction.md)</span><span class="sxs-lookup"><span data-stu-id="4fa82-133">A value from the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="4fa82-134">Se impostato su **DML_AXIS_DIRECTION_INCREASING**, questo operatore restituisce gli *elementi* K più *piccoli* in ordine di valore crescente.</span><span class="sxs-lookup"><span data-stu-id="4fa82-134">If set to **DML_AXIS_DIRECTION_INCREASING**, then this operator returns the *smallest* *K* elements in order of increasing value.</span></span> <span data-ttu-id="4fa82-135">In caso contrario, restituisce gli *elementi* K *più grandi* in ordine decrescente.</span><span class="sxs-lookup"><span data-stu-id="4fa82-135">Otherwise, it returns the *largest* *K* elements in decreasing order.</span></span>

## <a name="examples"></a><span data-ttu-id="4fa82-136">Esempi</span><span class="sxs-lookup"><span data-stu-id="4fa82-136">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="4fa82-137">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4fa82-137">Example 1</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 3
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
[[[[11, 10],
   [ 9,  8],
   [ 7,  6]]]]

OutputIndexTensor: (Sizes:{1,1,3,2}, DataType:UINT32)
[[[[3, 2],
   [2, 3],
   [3, 2]]]]
```

### <a name="example-2-using-a-different-axis"></a><span data-ttu-id="4fa82-138">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="4fa82-138">Example 2.</span></span> <span data-ttu-id="4fa82-139">Uso di un asse diverso</span><span class="sxs-lookup"><span data-stu-id="4fa82-139">Using a different axis</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 2
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[[[ 4,  5, 10, 11],
   [ 3,  2,  9,  8]]]]

OutputIndexTensor: (Sizes:{1,1,2,4}, DataType:UINT32)
[[[[2, 2, 0, 0],
   [1, 1, 1, 1]]]]
```

### <a name="example-3-tied-values"></a><span data-ttu-id="4fa82-140">Esempio 3.</span><span class="sxs-lookup"><span data-stu-id="4fa82-140">Example 3.</span></span> <span data-ttu-id="4fa82-141">Valori associati</span><span class="sxs-lookup"><span data-stu-id="4fa82-141">Tied values</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[3, 2, 2],
   [5, 5, 4],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[3, 1, 2],
   [2, 3, 1],
   [0, 1, 2]]]]
```

### <a name="example-4-increasing-axis-direction"></a><span data-ttu-id="4fa82-142">Esempio 4.</span><span class="sxs-lookup"><span data-stu-id="4fa82-142">Example 4.</span></span> <span data-ttu-id="4fa82-143">Aumento della direzione dell'asse</span><span class="sxs-lookup"><span data-stu-id="4fa82-143">Increasing axis direction</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[1, 2, 2],
   [3, 4, 5],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[0, 1, 2],
   [0, 1, 2],
   [0, 1, 2]]]]
```


## <a name="remarks"></a><span data-ttu-id="4fa82-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="4fa82-144">Remarks</span></span>
<span data-ttu-id="4fa82-145">Quando *AxisDirection è* impostato su [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), questo operatore equivale a [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="4fa82-145">When *AxisDirection* is set to [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), this operator is equivalent to [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="4fa82-146">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="4fa82-146">Availability</span></span>
<span data-ttu-id="4fa82-147">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="4fa82-147">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="4fa82-148">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="4fa82-148">Tensor constraints</span></span>

* <span data-ttu-id="4fa82-149">*InputTensor,* *OutputIndexTensor* e *OutputValueTensor* devono avere lo stesso *valore di DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="4fa82-149">*InputTensor*, *OutputIndexTensor*, and *OutputValueTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="4fa82-150">*InputTensor* e *OutputValueTensor* devono avere lo stesso *tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="4fa82-150">*InputTensor* and *OutputValueTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="4fa82-151">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="4fa82-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="4fa82-152">DML_FEATURE_LEVEL_3_1 e successive</span><span class="sxs-lookup"><span data-stu-id="4fa82-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="4fa82-153">Tensore</span><span class="sxs-lookup"><span data-stu-id="4fa82-153">Tensor</span></span> | <span data-ttu-id="4fa82-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="4fa82-154">Kind</span></span> | <span data-ttu-id="4fa82-155">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="4fa82-155">Supported dimension counts</span></span> | <span data-ttu-id="4fa82-156">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="4fa82-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="4fa82-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="4fa82-157">InputTensor</span></span> | <span data-ttu-id="4fa82-158">Input</span><span class="sxs-lookup"><span data-stu-id="4fa82-158">Input</span></span> | <span data-ttu-id="4fa82-159">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="4fa82-159">1 to 8</span></span> | <span data-ttu-id="4fa82-160">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="4fa82-160">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="4fa82-161">OutputValueTensor</span><span class="sxs-lookup"><span data-stu-id="4fa82-161">OutputValueTensor</span></span> | <span data-ttu-id="4fa82-162">Output</span><span class="sxs-lookup"><span data-stu-id="4fa82-162">Output</span></span> | <span data-ttu-id="4fa82-163">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="4fa82-163">1 to 8</span></span> | <span data-ttu-id="4fa82-164">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="4fa82-164">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="4fa82-165">OutputIndexTensor</span><span class="sxs-lookup"><span data-stu-id="4fa82-165">OutputIndexTensor</span></span> | <span data-ttu-id="4fa82-166">Output</span><span class="sxs-lookup"><span data-stu-id="4fa82-166">Output</span></span> | <span data-ttu-id="4fa82-167">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="4fa82-167">1 to 8</span></span> | <span data-ttu-id="4fa82-168">UINT32</span><span class="sxs-lookup"><span data-stu-id="4fa82-168">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="4fa82-169">DML_FEATURE_LEVEL_2_1 e successive</span><span class="sxs-lookup"><span data-stu-id="4fa82-169">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="4fa82-170">Tensore</span><span class="sxs-lookup"><span data-stu-id="4fa82-170">Tensor</span></span> | <span data-ttu-id="4fa82-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="4fa82-171">Kind</span></span> | <span data-ttu-id="4fa82-172">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="4fa82-172">Supported dimension counts</span></span> | <span data-ttu-id="4fa82-173">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="4fa82-173">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="4fa82-174">InputTensor</span><span class="sxs-lookup"><span data-stu-id="4fa82-174">InputTensor</span></span> | <span data-ttu-id="4fa82-175">Input</span><span class="sxs-lookup"><span data-stu-id="4fa82-175">Input</span></span> | <span data-ttu-id="4fa82-176">4</span><span class="sxs-lookup"><span data-stu-id="4fa82-176">4</span></span> | <span data-ttu-id="4fa82-177">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="4fa82-177">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="4fa82-178">OutputValueTensor</span><span class="sxs-lookup"><span data-stu-id="4fa82-178">OutputValueTensor</span></span> | <span data-ttu-id="4fa82-179">Output</span><span class="sxs-lookup"><span data-stu-id="4fa82-179">Output</span></span> | <span data-ttu-id="4fa82-180">4</span><span class="sxs-lookup"><span data-stu-id="4fa82-180">4</span></span> | <span data-ttu-id="4fa82-181">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="4fa82-181">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="4fa82-182">OutputIndexTensor</span><span class="sxs-lookup"><span data-stu-id="4fa82-182">OutputIndexTensor</span></span> | <span data-ttu-id="4fa82-183">Output</span><span class="sxs-lookup"><span data-stu-id="4fa82-183">Output</span></span> | <span data-ttu-id="4fa82-184">4</span><span class="sxs-lookup"><span data-stu-id="4fa82-184">4</span></span> | <span data-ttu-id="4fa82-185">UINT32</span><span class="sxs-lookup"><span data-stu-id="4fa82-185">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="4fa82-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4fa82-186">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4fa82-187">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="4fa82-187">**Header**</span></span> | <span data-ttu-id="4fa82-188">directml.h</span><span class="sxs-lookup"><span data-stu-id="4fa82-188">directml.h</span></span> |
