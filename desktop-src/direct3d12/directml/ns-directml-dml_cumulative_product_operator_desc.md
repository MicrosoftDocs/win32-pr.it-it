---
UID: NS:directml.DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
title: DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
description: Moltiplica gli elementi di un tensore lungo un asse, scrivendo il numero di esecuzione del prodotto nel tensore di output.
helpviewer_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC structure
- direct3d12.dml_cumulative_product_operator_desc
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.openlocfilehash: 71a078ad0f47c19ad1964d8d21f22e06822b5d01
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550216"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a><span data-ttu-id="f4c7b-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="f4c7b-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="f4c7b-104">Moltiplica gli elementi di un tensore lungo un asse, scrivendo il numero di esecuzione del prodotto nel tensore di output.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-104">Multiplies the elements of a tensor along an axis, writing the running tally of the product into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4c7b-105">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.5 e successive).</span><span class="sxs-lookup"><span data-stu-id="f4c7b-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="f4c7b-106">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="f4c7b-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c7b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4c7b-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* OutputTensor;
    UINT Axis;
    DML_AXIS_DIRECTION AxisDirection;
    BOOL HasExclusiveProduct;
};
```

## <a name="members"></a><span data-ttu-id="f4c7b-108">Members</span><span class="sxs-lookup"><span data-stu-id="f4c7b-108">Members</span></span>

`InputTensor`

<span data-ttu-id="f4c7b-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f4c7b-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f4c7b-110">Tensore contenente i dati di input.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-110">A tensor containing the input data.</span></span> <span data-ttu-id="f4c7b-111">Si tratta in genere dello stesso tensore fornito da *InputTensor* per DML_BATCH_NORMALIZATION_OPERATOR_DESC [**nel**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-111">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="f4c7b-112">Tensore di input contenente gli elementi da moltiplicare.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-112">The input tensor containing elements to be multiplied.</span></span>

`OutputTensor`

<span data-ttu-id="f4c7b-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f4c7b-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f4c7b-114">Tensore di output in cui scrivere i prodotti cumulativi risultanti.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-114">The output tensor to write the resulting cumulative products to.</span></span> <span data-ttu-id="f4c7b-115">Questo tensore deve avere le stesse dimensioni e lo stesso tipo di dati di *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="f4c7b-115">This tensor must have the same sizes and data type as *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="f4c7b-116">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f4c7b-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="f4c7b-117">Indice della dimensione su cui moltiplicare gli elementi.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-117">The index of the dimension to multiply elements over.</span></span> <span data-ttu-id="f4c7b-118">Questo valore deve essere minore di *DimensionCount* di *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="f4c7b-118">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="f4c7b-119">Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="f4c7b-119">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="f4c7b-120">Uno dei valori [dell'enumerazione DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="f4c7b-120">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="f4c7b-121">Se impostato su **DML_AXIS_DIRECTION_INCREASING**, il prodotto si verifica attraversando il tensore lungo l'asse specificato tramite l'indice degli elementi crescente.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-121">If set to **DML_AXIS_DIRECTION_INCREASING**, then the product occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="f4c7b-122">Se impostato su DML_AXIS_DIRECTION_DECREASING , **il** contrario è true e il prodotto si verifica attraversando gli elementi in base all'indice decrescente.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-122">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true and the product occurs by traversing elements by descending index.</span></span>

`HasExclusiveProduct`

<span data-ttu-id="f4c7b-123">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="f4c7b-123">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="f4c7b-124">Se **TRUE,** il valore dell'elemento corrente viene escluso durante la scrittura del numero in esecuzione nel tensore di output.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-124">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="f4c7b-125">Se **FALSE,** il valore dell'elemento corrente viene incluso nel numero in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-125">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="f4c7b-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="f4c7b-126">Examples</span></span>

<span data-ttu-id="f4c7b-127">Gli esempi in questa sezione usano tutti lo stesso tensore di input.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-127">The examples in this section all use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a><span data-ttu-id="f4c7b-128">Esempio 1.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-128">Example 1.</span></span> <span data-ttu-id="f4c7b-129">Prodotto cumulativo tra frammenti orizzontali</span><span class="sxs-lookup"><span data-stu-id="f4c7b-129">Cumulative product across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a><span data-ttu-id="f4c7b-130">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-130">Example 2.</span></span> <span data-ttu-id="f4c7b-131">Prodotti esclusivi</span><span class="sxs-lookup"><span data-stu-id="f4c7b-131">Exclusive products</span></span>

<span data-ttu-id="f4c7b-132">*L'impostazione di HasExclusiveProduct* su **TRUE** ha l'effetto di escludere il valore dell'elemento corrente dal valore in esecuzione durante la scrittura nel tensore di output.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-132">Setting *HasExclusiveProduct* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="f4c7b-133">Esempio 3.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-133">Example 3.</span></span> <span data-ttu-id="f4c7b-134">Direzione dell'asse</span><span class="sxs-lookup"><span data-stu-id="f4c7b-134">Axis direction</span></span>

<span data-ttu-id="f4c7b-135">*L'impostazione di AxisDirection* [**su DML_AXIS_DIRECTION_DECREASING**](./ne-directml-dml_axis_direction.md) ha l'effetto di invertire l'ordine di attraversamento degli elementi durante il calcolo del numero in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-135">Setting the *AxisDirection* to [**DML_AXIS_DIRECTION_DECREASING**](./ne-directml-dml_axis_direction.md) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a><span data-ttu-id="f4c7b-136">Esempio 4.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-136">Example 4.</span></span> <span data-ttu-id="f4c7b-137">Moltiplicazione lungo un asse diverso</span><span class="sxs-lookup"><span data-stu-id="f4c7b-137">Multiplying along a different axis</span></span>

<span data-ttu-id="f4c7b-138">In questo esempio il prodotto si verifica verticalmente lungo l'asse dell'altezza (seconda dimensione).</span><span class="sxs-lookup"><span data-stu-id="f4c7b-138">In this example, the product occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a><span data-ttu-id="f4c7b-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4c7b-139">Remarks</span></span>
<span data-ttu-id="f4c7b-140">Questo operatore supporta l'esecuzione sul posto, vale a dire che il tensore di output è autorizzato a creare un alias *di InputTensor* durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-140">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="f4c7b-141">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="f4c7b-141">Availability</span></span>
<span data-ttu-id="f4c7b-142">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="f4c7b-142">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f4c7b-143">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="f4c7b-143">Tensor constraints</span></span>
<span data-ttu-id="f4c7b-144">*InputTensor* e *OutputTensor* devono avere gli stessi *Tipi di dati* e *Dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="f4c7b-144">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f4c7b-145">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="f4c7b-145">Tensor support</span></span>
| <span data-ttu-id="f4c7b-146">Tensore</span><span class="sxs-lookup"><span data-stu-id="f4c7b-146">Tensor</span></span> | <span data-ttu-id="f4c7b-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4c7b-147">Kind</span></span> | <span data-ttu-id="f4c7b-148">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="f4c7b-148">Supported dimension counts</span></span> | <span data-ttu-id="f4c7b-149">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="f4c7b-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f4c7b-150">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f4c7b-150">InputTensor</span></span> | <span data-ttu-id="f4c7b-151">Input</span><span class="sxs-lookup"><span data-stu-id="f4c7b-151">Input</span></span> | <span data-ttu-id="f4c7b-152">4</span><span class="sxs-lookup"><span data-stu-id="f4c7b-152">4</span></span> | <span data-ttu-id="f4c7b-153">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="f4c7b-153">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="f4c7b-154">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f4c7b-154">OutputTensor</span></span> | <span data-ttu-id="f4c7b-155">Output</span><span class="sxs-lookup"><span data-stu-id="f4c7b-155">Output</span></span> | <span data-ttu-id="f4c7b-156">4</span><span class="sxs-lookup"><span data-stu-id="f4c7b-156">4</span></span> | <span data-ttu-id="f4c7b-157">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="f4c7b-157">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="f4c7b-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4c7b-158">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f4c7b-159">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="f4c7b-159">**Header**</span></span> | <span data-ttu-id="f4c7b-160">directml.h</span><span class="sxs-lookup"><span data-stu-id="f4c7b-160">directml.h</span></span> |