---
UID: NS:directml.DML_ARGMAX_OPERATOR_DESC
title: DML_ARGMAX_OPERATOR_DESC
description: Restituisce gli indici degli elementi con valori massimi all'interno di una o più dimensioni del tensore di input.
helpviewer_keywords:
- DML_ARGMAX_OPERATOR_DESC
- DML_ARGMAX_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMAX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMAX_OPERATOR_DESC, DML_ARGMAX_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
- directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
ms.openlocfilehash: 17ccadc1228ea833ea1f1b3235e97430ac000514
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320343"
---
# <a name="dml_argmax_operator_desc-structure-directmlh"></a><span data-ttu-id="b4857-103">Struttura DML_ARGMAX_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="b4857-103">DML_ARGMAX_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b4857-104">Restituisce gli indici degli elementi con valori massimi all'interno di una o più dimensioni del tensore di input.</span><span class="sxs-lookup"><span data-stu-id="b4857-104">Outputs the indices of the maximum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="b4857-105">Ogni elemento di output è il risultato dell'applicazione di una riduzione *argmax* su un subset del tensore di input.</span><span class="sxs-lookup"><span data-stu-id="b4857-105">Each output element is the result of applying an *argmax* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="b4857-106">La funzione *argmax* restituisce l'indice dell'elemento con valori massimi all'interno di un set di elementi di input.</span><span class="sxs-lookup"><span data-stu-id="b4857-106">The *argmax* function outputs the index of the maximum-valued element within a set of input elements.</span></span> <span data-ttu-id="b4857-107">Gli elementi di input interessati da ogni riduzione sono determinati dagli assi di input specificati.</span><span class="sxs-lookup"><span data-stu-id="b4857-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="b4857-108">Analogamente, ogni indice di output è relativo agli assi di input specificati.</span><span class="sxs-lookup"><span data-stu-id="b4857-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="b4857-109">Se vengono specificati tutti gli assi di input, l'operatore applica una sola riduzione *argmax* e produce un singolo elemento output.</span><span class="sxs-lookup"><span data-stu-id="b4857-109">If all input axes are specified, then the operator applies a single *argmax* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b4857-110">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="b4857-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="b4857-111">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b4857-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b4857-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4857-112">Syntax</span></span>
```cpp
struct DML_ARGMAX_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="b4857-113">Members</span><span class="sxs-lookup"><span data-stu-id="b4857-113">Members</span></span>

`InputTensor`

<span data-ttu-id="b4857-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b4857-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b4857-115">Tensore da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="b4857-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="b4857-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b4857-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b4857-117">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="b4857-117">The tensor to write the results to.</span></span> <span data-ttu-id="b4857-118">Ogni elemento di output è il risultato di una riduzione *argmax* su un subset di elementi di *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="b4857-118">Each output element is the result of an *argmax* reduction on a subset of elements from the *InputTensor*.</span></span> 

- <span data-ttu-id="b4857-119">*DimensionCount* deve corrispondere a *InputTensor. DimensionCount* (il rango del tensore di input viene mantenuto).</span><span class="sxs-lookup"><span data-stu-id="b4857-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="b4857-120">Le *dimensioni* devono corrispondere a *InputTensor.* sizes, ad eccezione delle dimensioni incluse negli *assi* ridotti, che devono essere di dimensioni pari a 1.</span><span class="sxs-lookup"><span data-stu-id="b4857-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="b4857-121">Tipo: **[uint](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b4857-121">Type: **[UINT](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b4857-122">Numero di assi da ridurre.</span><span class="sxs-lookup"><span data-stu-id="b4857-122">The number of axes to reduce.</span></span> <span data-ttu-id="b4857-123">Questo campo determina la dimensione della matrice di *assi* .</span><span class="sxs-lookup"><span data-stu-id="b4857-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="b4857-124">Tipo: \_ Field_size \_ (AxisCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="b4857-124">Type: \_Field_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="b4857-125">Assi lungo i quali ridurre.</span><span class="sxs-lookup"><span data-stu-id="b4857-125">The axes along which to reduce.</span></span> <span data-ttu-id="b4857-126">I valori devono essere compresi nell'intervallo `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="b4857-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="b4857-127">Tipo: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="b4857-127">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="b4857-128">Determina quale indice selezionare quando più elementi di input hanno lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="b4857-128">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="b4857-129">**DML_AXIS_DIRECTION_INCREASING** restituisce l'indice del primo elemento con valori massimi (ad esempio, `argmax({3,2,1,2,3}) = 0` )</span><span class="sxs-lookup"><span data-stu-id="b4857-129">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first maximum-valued element (for example, `argmax({3,2,1,2,3}) = 0`)</span></span>
- <span data-ttu-id="b4857-130">**DML_AXIS_DIRECTION_DECREASING** restituisce l'indice dell'ultimo elemento con valori massimi (ad esempio, `argmax({3,2,1,2,3}) = 4` )</span><span class="sxs-lookup"><span data-stu-id="b4857-130">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last maximum-valued element (for example, `argmax({3,2,1,2,3}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="b4857-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="b4857-131">Examples</span></span>

<span data-ttu-id="b4857-132">Gli esempi in questa sezione usano tutti questo stesso tensore di input bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="b4857-132">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmax-to-columns"></a><span data-ttu-id="b4857-133">Esempio 1.</span><span class="sxs-lookup"><span data-stu-id="b4857-133">Example 1.</span></span> <span data-ttu-id="b4857-134">Applicazione di *argmax* alle colonne</span><span class="sxs-lookup"><span data-stu-id="b4857-134">Applying *argmax* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[1,  // argmax({1, 3, 2})
  2,  // argmax({2, 0, 5})
  1]] // argmax({3, 4, 2})
```

### <a name="example-2-applying-argmax-to-rows"></a><span data-ttu-id="b4857-135">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="b4857-135">Example 2.</span></span> <span data-ttu-id="b4857-136">Applicazione di *argmax* alle righe</span><span class="sxs-lookup"><span data-stu-id="b4857-136">Applying *argmax* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[2], // argmax({1, 2, 3})
 [2], // argmax({3, 0, 4})
 [1]] // argmax({2, 5, 2})
```

### <a name="example-3-applying-argmax-to-all-axes-the-entire-tensor"></a><span data-ttu-id="b4857-137">Esempio 3.</span><span class="sxs-lookup"><span data-stu-id="b4857-137">Example 3.</span></span> <span data-ttu-id="b4857-138">Applicazione di *argmax* a tutti gli assi (l'intero tensore)</span><span class="sxs-lookup"><span data-stu-id="b4857-138">Applying *argmax* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[7]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="b4857-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4857-139">Remarks</span></span>
<span data-ttu-id="b4857-140">Le dimensioni del tensore di output devono corrispondere alle dimensioni del tensore di input, ad eccezione degli assi ridotti, che devono essere 1.</span><span class="sxs-lookup"><span data-stu-id="b4857-140">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="b4857-141">Quando *AxisDirection* è [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), questa API è equivalente a [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) con [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="b4857-141">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="b4857-142">Un subset di questa funzionalità viene esposto tramite l'operatore [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) ed è supportato nei livelli di funzionalità DirectML precedenti.</span><span class="sxs-lookup"><span data-stu-id="b4857-142">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="b4857-143">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="b4857-143">Availability</span></span>
<span data-ttu-id="b4857-144">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="b4857-144">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b4857-145">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="b4857-145">Tensor constraints</span></span>
<span data-ttu-id="b4857-146">*InputTensor* e *OutputTensor* devono avere lo stesso *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="b4857-146">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b4857-147">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="b4857-147">Tensor support</span></span>
| <span data-ttu-id="b4857-148">Tensore</span><span class="sxs-lookup"><span data-stu-id="b4857-148">Tensor</span></span> | <span data-ttu-id="b4857-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4857-149">Kind</span></span> | <span data-ttu-id="b4857-150">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="b4857-150">Supported dimension counts</span></span> | <span data-ttu-id="b4857-151">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="b4857-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b4857-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="b4857-152">InputTensor</span></span> | <span data-ttu-id="b4857-153">Input</span><span class="sxs-lookup"><span data-stu-id="b4857-153">Input</span></span> | <span data-ttu-id="b4857-154">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="b4857-154">1 to 8</span></span> | <span data-ttu-id="b4857-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b4857-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b4857-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b4857-156">OutputTensor</span></span> | <span data-ttu-id="b4857-157">Output</span><span class="sxs-lookup"><span data-stu-id="b4857-157">Output</span></span> | <span data-ttu-id="b4857-158">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="b4857-158">1 to 8</span></span> | <span data-ttu-id="b4857-159">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="b4857-159">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="b4857-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4857-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b4857-161">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="b4857-161">**Header**</span></span> | <span data-ttu-id="b4857-162">directml. h</span><span class="sxs-lookup"><span data-stu-id="b4857-162">directml.h</span></span> |