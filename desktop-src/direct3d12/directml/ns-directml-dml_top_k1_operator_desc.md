---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Seleziona gli elementi *K* più grandi o più piccoli di ogni sequenza lungo un asse di *InputTensor* e restituisce rispettivamente i valori e gli indici di tali elementi in *OutputValueTensor* e *OutputIndexTensor*.
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
ms.openlocfilehash: 8c5b9bf58a8582588d19878c7e06c602584777fa
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320359"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a><span data-ttu-id="2d1b7-103">Struttura DML_TOP_K1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="2d1b7-103">DML_TOP_K1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="2d1b7-104">Seleziona gli elementi *K* più grandi o più piccoli di ogni sequenza lungo un asse di *InputTensor* e restituisce rispettivamente i valori e gli indici di tali elementi in *OutputValueTensor* e *OutputIndexTensor*.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-104">Selects the largest or smallest *K* elements from each sequence along an axis of the *InputTensor*, and returns the values and indices of those elements in the *OutputValueTensor* and *OutputIndexTensor*, respectively.</span></span> <span data-ttu-id="2d1b7-105">Una *sequenza* fa riferimento a uno dei set di elementi presenti lungo la dimensione dell' *asse* del *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-105">A *sequence* refers to one of the sets of elements that exist along the *Axis* dimension of the *InputTensor*.</span></span>

<span data-ttu-id="2d1b7-106">La scelta di selezionare gli elementi K più grandi o gli elementi K più piccoli può essere controllata usando *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-106">The choice of whether to select the largest K elements or the smallest K elements can be controlled using *AxisDirection*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d1b7-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="2d1b7-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="2d1b7-108">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="2d1b7-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d1b7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d1b7-109">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="2d1b7-110">Members</span><span class="sxs-lookup"><span data-stu-id="2d1b7-110">Members</span></span>

`InputTensor`

<span data-ttu-id="2d1b7-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2d1b7-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2d1b7-112">Il tensore di input contenente gli elementi da selezionare.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-112">The input tensor containing elements to select.</span></span>


`OutputValueTensor`

<span data-ttu-id="2d1b7-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2d1b7-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2d1b7-114">Tensore di output in cui scrivere i valori dei primi *K* elementi.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-114">The output tensor to write the values of the top *K* elements to.</span></span> <span data-ttu-id="2d1b7-115">I primi *K* elementi vengono selezionati in base al fatto che siano il più grande o il più piccolo, a seconda del valore di *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-115">The top *K* elements are selected based on whether they are the largest or the smallest, depending on the value of *AxisDirection*.</span></span> <span data-ttu-id="2d1b7-116">Questo tensore deve avere dimensioni uguali a *InputTensor*, *ad eccezione* della dimensione specificata dal parametro *Axis* , che deve avere una dimensione uguale a *K*.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-116">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="2d1b7-117">È garantito che i valori *K* selezionati da ogni sequenza di input siano ordinati in ordine decrescente (dal più grande al più piccolo) se *AxisDirection* è [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span><span class="sxs-lookup"><span data-stu-id="2d1b7-117">The *K* values selected from each input sequence are guaranteed to be sorted descending (largest to smallest) if *AxisDirection* is [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span></span> <span data-ttu-id="2d1b7-118">In caso contrario, il valore opposto è true e i valori selezionati sono ordinati in ordine crescente (dal più piccolo al più grande).</span><span class="sxs-lookup"><span data-stu-id="2d1b7-118">Otherwise, the opposite is true and the values selected are guaranteed to be sorted ascending (smallest to largest).</span></span>


`OutputIndexTensor`

<span data-ttu-id="2d1b7-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2d1b7-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2d1b7-120">Il tensore di output in cui scrivere gli indici degli elementi principali *K* .</span><span class="sxs-lookup"><span data-stu-id="2d1b7-120">The output tensor to write the indices of the top *K* elements to.</span></span> <span data-ttu-id="2d1b7-121">Questo tensore deve avere dimensioni uguali a *InputTensor*, *ad eccezione* della dimensione specificata dal parametro *Axis* , che deve avere una dimensione uguale a *K*.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-121">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="2d1b7-122">Gli indici restituiti in questo tensore sono misurati in relazione all'inizio della relativa sequenza (anziché all'inizio del tensore).</span><span class="sxs-lookup"><span data-stu-id="2d1b7-122">The indices returned in this tensor are measured relative to the beginning of their sequence (as opposed to the beginning of the tensor).</span></span> <span data-ttu-id="2d1b7-123">Un indice 0, ad esempio, fa sempre riferimento al primo elemento per tutte le sequenze in un asse.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-123">For example, an index of 0 always refers to the first element for all sequences in an axis.</span></span>

<span data-ttu-id="2d1b7-124">Nei casi in cui due o più elementi nella parte superiore del K hanno lo stesso valore (ovvero, quando è presente un vincolo), gli indici di entrambi gli elementi sono inclusi e sono sicuramente ordinati in base all'indice dell'elemento crescente.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-124">In cases where two or more elements in the top-K have the same value (that is, when there is a tie), the indices of both elements are included, and are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="2d1b7-125">Si noti che questo vale indipendentemente dal valore di *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-125">Note that this is true irrespective of the value of *AxisDirection*.</span></span>


`Axis`

<span data-ttu-id="2d1b7-126">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="2d1b7-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="2d1b7-127">Indice della dimensione in cui selezionare gli elementi.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-127">The index of the dimension to select elements across.</span></span> <span data-ttu-id="2d1b7-128">Questo valore deve essere minore del valore di *DimensionCount* di *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-128">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>


`K`

<span data-ttu-id="2d1b7-129">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="2d1b7-129">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="2d1b7-130">Numero di elementi da selezionare.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-130">The number of elements to select.</span></span> <span data-ttu-id="2d1b7-131">*K* deve essere maggiore di 0, ma minore del numero di elementi in *InputTensor* lungo la dimensione specificata da *Axis*.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-131">*K* must be greater than 0, but less than the number of elements in the *InputTensor* along the dimension specified by *Axis*.</span></span>


`AxisDirection`

<span data-ttu-id="2d1b7-132">Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="2d1b7-132">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="2d1b7-133">Valore dell'enumerazione [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="2d1b7-133">A value from the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="2d1b7-134">Se impostato su **DML_AXIS_DIRECTION_INCREASING**, questo operatore restituisce gli elementi *K* *più piccoli* in ordine di valore crescente.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-134">If set to **DML_AXIS_DIRECTION_INCREASING**, then this operator returns the *smallest* *K* elements in order of increasing value.</span></span> <span data-ttu-id="2d1b7-135">In caso contrario, restituisce gli elementi *K* *più grandi* in ordine decrescente.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-135">Otherwise, it returns the *largest* *K* elements in decreasing order.</span></span>

## <a name="examples"></a><span data-ttu-id="2d1b7-136">Esempi</span><span class="sxs-lookup"><span data-stu-id="2d1b7-136">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="2d1b7-137">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2d1b7-137">Example 1</span></span>

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

### <a name="example-2-using-a-different-axis"></a><span data-ttu-id="2d1b7-138">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-138">Example 2.</span></span> <span data-ttu-id="2d1b7-139">Uso di un asse diverso</span><span class="sxs-lookup"><span data-stu-id="2d1b7-139">Using a different axis</span></span>

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

### <a name="example-3-tied-values"></a><span data-ttu-id="2d1b7-140">Esempio 3.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-140">Example 3.</span></span> <span data-ttu-id="2d1b7-141">Valori associati</span><span class="sxs-lookup"><span data-stu-id="2d1b7-141">Tied values</span></span>

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

### <a name="example-4-increasing-axis-direction"></a><span data-ttu-id="2d1b7-142">Esempio 4.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-142">Example 4.</span></span> <span data-ttu-id="2d1b7-143">Aumento della direzione dell'asse</span><span class="sxs-lookup"><span data-stu-id="2d1b7-143">Increasing axis direction</span></span>

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


## <a name="remarks"></a><span data-ttu-id="2d1b7-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d1b7-144">Remarks</span></span>
<span data-ttu-id="2d1b7-145">Quando *AxisDirection* è impostato su [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), questo operatore è equivalente a [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="2d1b7-145">When *AxisDirection* is set to [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), this operator is equivalent to [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="2d1b7-146">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="2d1b7-146">Availability</span></span>
<span data-ttu-id="2d1b7-147">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="2d1b7-147">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="2d1b7-148">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="2d1b7-148">Tensor constraints</span></span>
* <span data-ttu-id="2d1b7-149">*InputTensor* e *OutputValueTensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-149">*InputTensor* and *OutputValueTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="2d1b7-150">*OutputIndexTensor* e *OutputValueTensor* devono avere le stesse *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-150">*OutputIndexTensor* and *OutputValueTensor* must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="2d1b7-151">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="2d1b7-151">Tensor support</span></span>
| <span data-ttu-id="2d1b7-152">Tensore</span><span class="sxs-lookup"><span data-stu-id="2d1b7-152">Tensor</span></span> | <span data-ttu-id="2d1b7-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d1b7-153">Kind</span></span> | <span data-ttu-id="2d1b7-154">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="2d1b7-154">Dimensions</span></span> | <span data-ttu-id="2d1b7-155">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="2d1b7-155">Supported dimension counts</span></span> | <span data-ttu-id="2d1b7-156">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="2d1b7-156">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="2d1b7-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="2d1b7-157">InputTensor</span></span> | <span data-ttu-id="2d1b7-158">Input</span><span class="sxs-lookup"><span data-stu-id="2d1b7-158">Input</span></span> | <span data-ttu-id="2d1b7-159">{IN0, IN1, IN2, IN3}</span><span class="sxs-lookup"><span data-stu-id="2d1b7-159">{ In0, In1, In2, In3 }</span></span> | <span data-ttu-id="2d1b7-160">4</span><span class="sxs-lookup"><span data-stu-id="2d1b7-160">4</span></span> | <span data-ttu-id="2d1b7-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2d1b7-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="2d1b7-162">OutputValueTensor</span><span class="sxs-lookup"><span data-stu-id="2d1b7-162">OutputValueTensor</span></span> | <span data-ttu-id="2d1b7-163">Output</span><span class="sxs-lookup"><span data-stu-id="2d1b7-163">Output</span></span> | <span data-ttu-id="2d1b7-164">{Out0, OUT1, OUT2, OUT3}</span><span class="sxs-lookup"><span data-stu-id="2d1b7-164">{ Out0, Out1, Out2, Out3 }</span></span> | <span data-ttu-id="2d1b7-165">4</span><span class="sxs-lookup"><span data-stu-id="2d1b7-165">4</span></span> | <span data-ttu-id="2d1b7-166">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2d1b7-166">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="2d1b7-167">OutputIndexTensor</span><span class="sxs-lookup"><span data-stu-id="2d1b7-167">OutputIndexTensor</span></span> | <span data-ttu-id="2d1b7-168">Output</span><span class="sxs-lookup"><span data-stu-id="2d1b7-168">Output</span></span> | <span data-ttu-id="2d1b7-169">{Out0, OUT1, OUT2, OUT3}</span><span class="sxs-lookup"><span data-stu-id="2d1b7-169">{ Out0, Out1, Out2, Out3 }</span></span> | <span data-ttu-id="2d1b7-170">4</span><span class="sxs-lookup"><span data-stu-id="2d1b7-170">4</span></span> | <span data-ttu-id="2d1b7-171">UINT32</span><span class="sxs-lookup"><span data-stu-id="2d1b7-171">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="2d1b7-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d1b7-172">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2d1b7-173">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="2d1b7-173">**Header**</span></span> | <span data-ttu-id="2d1b7-174">directml. h</span><span class="sxs-lookup"><span data-stu-id="2d1b7-174">directml.h</span></span> |