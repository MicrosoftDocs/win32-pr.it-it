---
UID: NS:directml.DML_ARGMIN_OPERATOR_DESC
title: DML_ARGMIN_OPERATOR_DESC
description: Restituisce gli indici degli elementi con valore minimo all'interno di una o più dimensioni del tensore di input.
helpviewer_keywords:
- DML_ARGMIN_OPERATOR_DESC
- DML_ARGMIN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMIN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMIN_OPERATOR_DESC, DML_ARGMIN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
- directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
ms.openlocfilehash: 2e12a81593504a4eb7a0917e545bfa20c70647ff
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804077"
---
# <a name="dml_argmin_operator_desc-structure-directmlh"></a><span data-ttu-id="5be03-103">DML_ARGMIN_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="5be03-103">DML_ARGMIN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="5be03-104">Restituisce gli indici degli elementi con valore minimo all'interno di una o più dimensioni del tensore di input.</span><span class="sxs-lookup"><span data-stu-id="5be03-104">Outputs the indices of the minimum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="5be03-105">Ogni elemento di output è il risultato dell'applicazione di *una riduzione argmin* su un subset del tensore di input.</span><span class="sxs-lookup"><span data-stu-id="5be03-105">Each output element is the result of applying an *argmin* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="5be03-106">La *funzione argmin* restituisce l'indice dell'elemento con valore minimo all'interno di un set di elementi di input.</span><span class="sxs-lookup"><span data-stu-id="5be03-106">The *argmin* function outputs the index of the minimum-valued element within a set of input elements.</span></span> <span data-ttu-id="5be03-107">Gli elementi di input coinvolti in ogni riduzione sono determinati dagli assi di input specificati.</span><span class="sxs-lookup"><span data-stu-id="5be03-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="5be03-108">Analogamente, ogni indice di output è rispetto agli assi di input forniti.</span><span class="sxs-lookup"><span data-stu-id="5be03-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="5be03-109">Se vengono specificati tutti gli assi di input, l'operatore applica una singola *riduzione argmin* e produce un singolo elemento di output.</span><span class="sxs-lookup"><span data-stu-id="5be03-109">If all input axes are specified, then the operator applies a single *argmin* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5be03-110">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="5be03-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="5be03-111">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="5be03-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5be03-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5be03-112">Syntax</span></span>
```cpp
struct DML_ARGMIN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="5be03-113">Members</span><span class="sxs-lookup"><span data-stu-id="5be03-113">Members</span></span>

`InputTensor`

<span data-ttu-id="5be03-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5be03-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5be03-115">Tensore da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="5be03-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="5be03-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5be03-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5be03-117">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="5be03-117">The tensor to write the results to.</span></span> <span data-ttu-id="5be03-118">Ogni elemento di output è il risultato di *una riduzione argmin* su un subset di elementi da *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="5be03-118">Each output element is the result of an *argmin* reduction on a subset of elements from the *InputTensor*.</span></span>

- <span data-ttu-id="5be03-119">*DimensionCount deve* corrispondere a *InputTensor.DimensionCount* (viene mantenuta la classificazione del tensore di input).</span><span class="sxs-lookup"><span data-stu-id="5be03-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="5be03-120">*Le* dimensioni devono corrispondere *a InputTensor.Sizes*, ad eccezione delle dimensioni incluse negli assi *ridotti,* che devono essere di dimensioni 1.</span><span class="sxs-lookup"><span data-stu-id="5be03-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="5be03-121">Tipo: **[UINT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5be03-121">Type: **[UINT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="5be03-122">Numero di assi da ridurre.</span><span class="sxs-lookup"><span data-stu-id="5be03-122">The number of axes to reduce.</span></span> <span data-ttu-id="5be03-123">Questo campo determina le dimensioni della *matrice Axes.*</span><span class="sxs-lookup"><span data-stu-id="5be03-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="5be03-124">Tipo: \_ Field_size \_ (AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="5be03-124">Type: \_Field_size\_(AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="5be03-125">Assi lungo i quali eseguire la riduzione.</span><span class="sxs-lookup"><span data-stu-id="5be03-125">The axes along which to reduce.</span></span> <span data-ttu-id="5be03-126">I valori devono essere nell'intervallo `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="5be03-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="5be03-127">DML_AXIS_DIRECTION AxisDirection;</span><span class="sxs-lookup"><span data-stu-id="5be03-127">DML_AXIS_DIRECTION AxisDirection;</span></span>

<span data-ttu-id="5be03-128">Tipo: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="5be03-128">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="5be03-129">Determina l'indice da selezionare quando più elementi di input hanno lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="5be03-129">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="5be03-130">**DML_AXIS_DIRECTION_INCREASING** restituisce l'indice del primo elemento con valore minimo (ad esempio, `argmin({1,2,3,2,1}) = 0` )</span><span class="sxs-lookup"><span data-stu-id="5be03-130">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first minimum-valued element (for example, `argmin({1,2,3,2,1}) = 0`)</span></span>
- <span data-ttu-id="5be03-131">**DML_AXIS_DIRECTION_DECREASING** restituisce l'indice dell'ultimo elemento con valore minimo (ad esempio, `argmin({1,2,3,2,1}) = 4` )</span><span class="sxs-lookup"><span data-stu-id="5be03-131">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last minimum-valued element (for example, `argmin({1,2,3,2,1}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="5be03-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="5be03-132">Examples</span></span>

<span data-ttu-id="5be03-133">Gli esempi in questa sezione usano tutti questo stesso tensore di input bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="5be03-133">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmin-to-columns"></a><span data-ttu-id="5be03-134">Esempio 1.</span><span class="sxs-lookup"><span data-stu-id="5be03-134">Example 1.</span></span> <span data-ttu-id="5be03-135">Applicazione di *argmin* alle colonne</span><span class="sxs-lookup"><span data-stu-id="5be03-135">Applying *argmin* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[0,  // argmin({1, 3, 2})
  1,  // argmin({2, 0, 5})
  2]] // argmin({3, 4, 2})
```

### <a name="example-2-applying-argmin-to-rows"></a><span data-ttu-id="5be03-136">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="5be03-136">Example 2.</span></span> <span data-ttu-id="5be03-137">Applicazione di *argmin* alle righe</span><span class="sxs-lookup"><span data-stu-id="5be03-137">Applying *argmin* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[0], // argmin({1, 2, 3})
 [1], // argmin({3, 0, 4})
 [0]] // argmin({2, 5, 2})
```

### <a name="example-3-applying-argmin-to-all-axes-the-entire-tensor"></a><span data-ttu-id="5be03-138">Esempio 3.</span><span class="sxs-lookup"><span data-stu-id="5be03-138">Example 3.</span></span> <span data-ttu-id="5be03-139">Applicazione di *argmin* a tutti gli assi (l'intero tensore)</span><span class="sxs-lookup"><span data-stu-id="5be03-139">Applying *argmin* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[4]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="5be03-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="5be03-140">Remarks</span></span>
<span data-ttu-id="5be03-141">Le dimensioni del tensore di output devono corrispondere alle dimensioni del tensore di input, ad eccezione degli assi ridotti, che devono essere 1.</span><span class="sxs-lookup"><span data-stu-id="5be03-141">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="5be03-142">Quando *AxisDirection è* [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), questa API equivale a DML_REDUCE_OPERATOR_DESC [con](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="5be03-142">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="5be03-143">Un subset di questa funzionalità viene esposto tramite l'operatore [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) ed è supportato nei livelli di funzionalità DirectML precedenti.</span><span class="sxs-lookup"><span data-stu-id="5be03-143">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="5be03-144">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="5be03-144">Availability</span></span>
<span data-ttu-id="5be03-145">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="5be03-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5be03-146">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="5be03-146">Tensor constraints</span></span>
<span data-ttu-id="5be03-147">*InputTensor* e *OutputTensor* devono avere lo stesso *dimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="5be03-147">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5be03-148">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="5be03-148">Tensor support</span></span>
| <span data-ttu-id="5be03-149">Tensore</span><span class="sxs-lookup"><span data-stu-id="5be03-149">Tensor</span></span> | <span data-ttu-id="5be03-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="5be03-150">Kind</span></span> | <span data-ttu-id="5be03-151">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="5be03-151">Supported dimension counts</span></span> | <span data-ttu-id="5be03-152">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="5be03-152">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5be03-153">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5be03-153">InputTensor</span></span> | <span data-ttu-id="5be03-154">Input</span><span class="sxs-lookup"><span data-stu-id="5be03-154">Input</span></span> | <span data-ttu-id="5be03-155">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="5be03-155">1 to 8</span></span> | <span data-ttu-id="5be03-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5be03-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="5be03-157">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5be03-157">OutputTensor</span></span> | <span data-ttu-id="5be03-158">Output</span><span class="sxs-lookup"><span data-stu-id="5be03-158">Output</span></span> | <span data-ttu-id="5be03-159">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="5be03-159">1 to 8</span></span> | <span data-ttu-id="5be03-160">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="5be03-160">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="5be03-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5be03-161">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5be03-162">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="5be03-162">**Header**</span></span> | <span data-ttu-id="5be03-163">directml.h</span><span class="sxs-lookup"><span data-stu-id="5be03-163">directml.h</span></span> |