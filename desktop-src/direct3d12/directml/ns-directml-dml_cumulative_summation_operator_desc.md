---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Somma gli elementi di un tensore lungo un asse, scrivendo il totale di esecuzione della somma nel tensore di output.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 2862a2add207b0bb6c41f5c1aabbc390797cba23
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803348"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a><span data-ttu-id="d0832-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="d0832-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="d0832-104">Somma gli elementi di un tensore lungo un asse, scrivendo il totale di esecuzione della somma nel tensore di output.</span><span class="sxs-lookup"><span data-stu-id="d0832-104">Sums the elements of a tensor along an axis, writing the running tally of the summation into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0832-105">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="d0832-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="d0832-106">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="d0832-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0832-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0832-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```

## <a name="members"></a><span data-ttu-id="d0832-108">Members</span><span class="sxs-lookup"><span data-stu-id="d0832-108">Members</span></span>

`InputTensor`

<span data-ttu-id="d0832-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d0832-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d0832-110">Tensore di input contenente gli elementi da sommare.</span><span class="sxs-lookup"><span data-stu-id="d0832-110">The input tensor containing elements to be summed.</span></span>

`OutputTensor`

<span data-ttu-id="d0832-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d0832-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d0832-112">Tensore di output in cui scrivere le sommazioni cumulative risultanti.</span><span class="sxs-lookup"><span data-stu-id="d0832-112">The output tensor to write the resulting cumulative summations to.</span></span> <span data-ttu-id="d0832-113">Questo tensore deve avere le stesse dimensioni e lo stesso tipo di dati di *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="d0832-113">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="d0832-114">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d0832-114">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="d0832-115">Indice della dimensione su cui sommare gli elementi.</span><span class="sxs-lookup"><span data-stu-id="d0832-115">The index of the dimension to sum elements over.</span></span> <span data-ttu-id="d0832-116">Questo valore deve essere minore di *DimensionCount* di *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="d0832-116">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="d0832-117">Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="d0832-117">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="d0832-118">Uno dei valori [dell'enumerazione DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="d0832-118">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="d0832-119">Se impostato su **DML_AXIS_DIRECTION_INCREASING**, la somma si verifica attraversando il tensore lungo l'asse specificato tramite l'indice degli elementi crescente.</span><span class="sxs-lookup"><span data-stu-id="d0832-119">If set to **DML_AXIS_DIRECTION_INCREASING**, then the summation occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="d0832-120">Se impostato su **DML_AXIS_DIRECTION_DECREASING**, il contrario è true e la somma si verifica attraversando gli elementi in base all'indice decrescente.</span><span class="sxs-lookup"><span data-stu-id="d0832-120">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true, and the summation occurs by traversing elements by descending index.</span></span>

`HasExclusiveSum`

<span data-ttu-id="d0832-121">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="d0832-121">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="d0832-122">Se **TRUE,** il valore dell'elemento corrente viene escluso durante la scrittura del numero di esecuzione nel tensore di output.</span><span class="sxs-lookup"><span data-stu-id="d0832-122">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="d0832-123">Se **FALSE,** il valore dell'elemento corrente viene incluso nel numero in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d0832-123">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="d0832-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="d0832-124">Examples</span></span>

<span data-ttu-id="d0832-125">Gli esempi in questa sezione usano tutti un tensore di input con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="d0832-125">The examples in this section all use an input tensor with the following properties.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-summation-across-horizontal-slivers"></a><span data-ttu-id="d0832-126">Esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d0832-126">Example 1.</span></span> <span data-ttu-id="d0832-127">Somma cumulativa tra sliver orizzontali</span><span class="sxs-lookup"><span data-stu-id="d0832-127">Cumulative summation across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  3,  6, 11],     // i.e. [2, 2+1, 2+1+3, 2+1+3+5]
   [3, 11, 18, 21],     //      [...                   ]
   [9, 15, 17, 21]]]]   //      [...                   ]
```

### <a name="example-2-exclusive-sums"></a><span data-ttu-id="d0832-128">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="d0832-128">Example 2.</span></span> <span data-ttu-id="d0832-129">Somme esclusive</span><span class="sxs-lookup"><span data-stu-id="d0832-129">Exclusive sums</span></span>

<span data-ttu-id="d0832-130">*L'impostazione di HasExclusiveSum* su **TRUE** ha l'effetto di escludere il valore dell'elemento corrente dal valore in esecuzione durante la scrittura nel tensore di output.</span><span class="sxs-lookup"><span data-stu-id="d0832-130">Setting *HasExclusiveSum* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[0, 2,  3,  6],      // Notice the sum is written before adding the input,
   [0, 3, 11, 18],      // and the final total is not written to any output.
   [0, 9, 15, 17]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="d0832-131">Esempio 3.</span><span class="sxs-lookup"><span data-stu-id="d0832-131">Example 3.</span></span> <span data-ttu-id="d0832-132">Direzione dell'asse</span><span class="sxs-lookup"><span data-stu-id="d0832-132">Axis direction</span></span>

<span data-ttu-id="d0832-133">*L'impostazione di AxisDirection* [su DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) ha l'effetto di invertire l'ordine di attraversamento degli elementi durante il calcolo del numero in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d0832-133">Setting the *AxisDirection* to [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[11,  9,  8,  5],    // i.e. [2+1+3+5, 1+3+5, 3+5, 5]
   [21, 18, 10,  3],    //      [...                   ]
   [21, 12,  6,  4]]]]  //      [...                   ]
```

### <a name="example-4-summing-along-a-different-axis"></a><span data-ttu-id="d0832-134">Esempio 4.</span><span class="sxs-lookup"><span data-stu-id="d0832-134">Example 4.</span></span> <span data-ttu-id="d0832-135">Somma lungo un asse diverso</span><span class="sxs-lookup"><span data-stu-id="d0832-135">Summing along a different axis</span></span>

<span data-ttu-id="d0832-136">In questo esempio la somma viene eseguita verticalmente, lungo l'asse dell'altezza (seconda dimensione).</span><span class="sxs-lookup"><span data-stu-id="d0832-136">In this example, the summation occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 5,  9, 10,  8],   //      [2+3,  ...]
   [14, 15, 12, 12]]]] //      [2+3+9 ...]
```

## <a name="remarks"></a><span data-ttu-id="d0832-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0832-137">Remarks</span></span>
<span data-ttu-id="d0832-138">Questo operatore supporta l'esecuzione sul posto, ovvero *outputTensor* è autorizzato a creare un alias di *InputTensor* durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="d0832-138">This operator supports in-place execution, meaning that the *OutputTensor* is permitted to alias the *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="d0832-139">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="d0832-139">Availability</span></span>
<span data-ttu-id="d0832-140">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="d0832-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d0832-141">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="d0832-141">Tensor constraints</span></span>
<span data-ttu-id="d0832-142">*InputTensor* e *OutputTensor* devono avere gli stessi *Tipi di dati* e *Dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="d0832-142">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="d0832-143">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="d0832-143">Tensor support</span></span>
| <span data-ttu-id="d0832-144">Tensore</span><span class="sxs-lookup"><span data-stu-id="d0832-144">Tensor</span></span> | <span data-ttu-id="d0832-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0832-145">Kind</span></span> | <span data-ttu-id="d0832-146">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="d0832-146">Supported dimension counts</span></span> | <span data-ttu-id="d0832-147">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="d0832-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d0832-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="d0832-148">InputTensor</span></span> | <span data-ttu-id="d0832-149">Input</span><span class="sxs-lookup"><span data-stu-id="d0832-149">Input</span></span> | <span data-ttu-id="d0832-150">4</span><span class="sxs-lookup"><span data-stu-id="d0832-150">4</span></span> | <span data-ttu-id="d0832-151">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="d0832-151">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="d0832-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d0832-152">OutputTensor</span></span> | <span data-ttu-id="d0832-153">Output</span><span class="sxs-lookup"><span data-stu-id="d0832-153">Output</span></span> | <span data-ttu-id="d0832-154">4</span><span class="sxs-lookup"><span data-stu-id="d0832-154">4</span></span> | <span data-ttu-id="d0832-155">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="d0832-155">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="d0832-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0832-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d0832-157">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="d0832-157">**Header**</span></span> | <span data-ttu-id="d0832-158">directml.h</span><span class="sxs-lookup"><span data-stu-id="d0832-158">directml.h</span></span> |
