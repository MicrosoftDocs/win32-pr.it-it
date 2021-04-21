---
UID: NS:directml.DML_MAX_POOLING_GRAD_OPERATOR_DESC
title: DML_MAX_POOLING_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per il pooling massimo (vedere [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).
helpviewer_keywords:
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- DML_MAX_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_MAX_POOLING_GRAD_OPERATOR_DESC, DML_MAX_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: 3b0b10fa8ee17c9d06e779c3c990f134bc4ae669
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803431"
---
# <a name="dml_max_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="76216-103">DML_MAX_POOLING_GRAD_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="76216-103">DML_MAX_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="76216-104">Calcola le sfumature di backpropagation per il pooling massimo (vedere [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span><span class="sxs-lookup"><span data-stu-id="76216-104">Computes backpropagation gradients for max pooling (see [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span></span>

<span data-ttu-id="76216-105">Si consideri un **DML_MAX_POOLING2_OPERATOR_DESC** 2x2 senza spaziatura interna o dilazioni e uno stride di 1, che esegue le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="76216-105">Consider a 2x2 **DML_MAX_POOLING2_OPERATOR_DESC** without padding nor dilations and a stride of 1, which performs the following.</span></span>

```
InputTensor             OutputTensor    IndicesTensor
[[1, 2, 3],   MaxPool    [[4, 4],        [[4, 4],
 [2, 4, 2],     -->       [6, 7]]         [7, 8]]
 [5, 6, 7]]
```

<span data-ttu-id="76216-106">L'elemento più grande di ogni finestra 2x2 nel tensore di input produce un elemento dell'output.</span><span class="sxs-lookup"><span data-stu-id="76216-106">The largest element of each 2x2 window in the input tensor produces one element of the output.</span></span> <span data-ttu-id="76216-107">Di seguito è riportato un esempio dell'output **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, dati parametri simili.</span><span class="sxs-lookup"><span data-stu-id="76216-107">Below is an example of the output of **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, given similar parameters.</span></span>

```
InputTensor   InputGradientTensor            OutputGradientTensor
[[1, 2, 3],       [[1, 2],     MaxPoolGrad   [[0, 0, 0],
 [2, 4, 2],        [4, 5]]         -->        [0, 3, 0],
 [5, 6, 7]]                                   [0, 4, 5]]
```

<span data-ttu-id="76216-108">In effetti, questo operatore usa *InputTensor* per determinare l'indice dell'elemento più grande da ogni finestra e distribuisce i valori di *InputGradientTensor* in *OutputGradientTensor* in base a questi indici.</span><span class="sxs-lookup"><span data-stu-id="76216-108">In effect, this operator uses the *InputTensor* to determine the index of the largest element from each window, and distributes the values of *InputGradientTensor* into the *OutputGradientTensor* based on these indices.</span></span> <span data-ttu-id="76216-109">Se gli indici si sovrappongono, i valori vengono sommati.</span><span class="sxs-lookup"><span data-stu-id="76216-109">Where indices overlap, the values are summed.</span></span> <span data-ttu-id="76216-110">Qualsiasi elemento di output senza riferimenti viene azzerato.</span><span class="sxs-lookup"><span data-stu-id="76216-110">Any unreferenced output elements are zeroed.</span></span>

<span data-ttu-id="76216-111">Nel caso di un oggetto tie (in cui più di un elemento in una finestra ha lo stesso valore massimo), viene scelto l'elemento con l'indice logico di elemento più basso.</span><span class="sxs-lookup"><span data-stu-id="76216-111">In the case of a tie (where more than one element in a window has the same maximum value), the element with the lowest logical element index is chosen.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76216-112">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="76216-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="76216-113">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="76216-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="76216-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76216-114">Syntax</span></span>

```cpp
struct DML_MAX_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  _Field_size_(DimensionCount) const UINT* Dilations;
};
```

## <a name="members"></a><span data-ttu-id="76216-115">Members</span><span class="sxs-lookup"><span data-stu-id="76216-115">Members</span></span>

`InputTensor`

<span data-ttu-id="76216-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76216-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76216-117">Tensore della funzionalità di input.</span><span class="sxs-lookup"><span data-stu-id="76216-117">The input feature tensor.</span></span> <span data-ttu-id="76216-118">Si tratta in genere dello stesso tensore fornito da *InputTensor* per DML_MAX_POOLING2_OPERATOR_DESC [nel](./ns-directml-dml_max_pooling2_operator_desc.md) passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="76216-118">This is typically the same tensor that was provided as the *InputTensor* to [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="76216-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76216-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76216-120">Tensore sfumatura in ingresso.</span><span class="sxs-lookup"><span data-stu-id="76216-120">The incoming gradient tensor.</span></span> <span data-ttu-id="76216-121">Questa operazione viene in genere ottenuta dall'output della retropropagazione di un livello precedente.</span><span class="sxs-lookup"><span data-stu-id="76216-121">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="76216-122">In genere questo tensore avrebbe le stesse dimensioni *dell'output* del [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) corrispondente nel passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="76216-122">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="76216-123">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76216-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76216-124">Tensore di output contenente le sfumature backpropagate.</span><span class="sxs-lookup"><span data-stu-id="76216-124">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="76216-125">In genere, questo tensore ha le stesse dimensioni *dell'input* del [parametro](./ns-directml-dml_max_pooling2_operator_desc.md) DML_MAX_POOLING2_OPERATOR_DESC nel passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="76216-125">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="76216-126">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="76216-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="76216-127">Numero di elementi nelle matrici *Strides,* *WindowSize,* *StartPadding,* *EndPadding* e *Dilations.*</span><span class="sxs-lookup"><span data-stu-id="76216-127">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, *EndPadding*, and *Dilations* arrays.</span></span> <span data-ttu-id="76216-128">Questo valore deve essere uguale al numero di dimensioni spaziali (DimensionCount - 2 di InputTensor).</span><span class="sxs-lookup"><span data-stu-id="76216-128">This value must equal the spatial dimension count (InputTensor's DimensionCount - 2).</span></span> <span data-ttu-id="76216-129">Poiché questo operatore supporta solo tensori 4D, l'unico valore valido per questo parametro è 2.</span><span class="sxs-lookup"><span data-stu-id="76216-129">As this operator only supports 4D tensors, the only valid value for this parameter is 2.</span></span>

`Strides`

<span data-ttu-id="76216-130">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="76216-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="76216-131">Vedere *Strides* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="76216-131">See *Strides* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`WindowSize`

<span data-ttu-id="76216-132">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="76216-132">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="76216-133">Vedere *WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="76216-133">See *WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`StartPadding`

<span data-ttu-id="76216-134">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="76216-134">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="76216-135">Vedere *StartPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="76216-135">See *StartPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`EndPadding`

<span data-ttu-id="76216-136">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="76216-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="76216-137">Vedere *EndPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="76216-137">See *EndPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`Dilations`

<span data-ttu-id="76216-138">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="76216-138">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="76216-139">Vedere *Dilazioni* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="76216-139">See *Dilations* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

## <a name="availability"></a><span data-ttu-id="76216-140">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="76216-140">Availability</span></span>
<span data-ttu-id="76216-141">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="76216-141">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="76216-142">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="76216-142">Tensor constraints</span></span>
* <span data-ttu-id="76216-143">*InputTensor* e *OutputGradientTensor* devono avere le stesse *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="76216-143">*InputTensor* and *OutputGradientTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="76216-144">*InputGradientTensor,* *InputTensor* e *OutputGradientTensor* devono avere lo stesso *tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="76216-144">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="76216-145">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="76216-145">Tensor support</span></span>
| <span data-ttu-id="76216-146">Tensore</span><span class="sxs-lookup"><span data-stu-id="76216-146">Tensor</span></span> | <span data-ttu-id="76216-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="76216-147">Kind</span></span> | <span data-ttu-id="76216-148">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="76216-148">Dimensions</span></span> | <span data-ttu-id="76216-149">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="76216-149">Supported dimension counts</span></span> | <span data-ttu-id="76216-150">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="76216-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="76216-151">InputTensor</span><span class="sxs-lookup"><span data-stu-id="76216-151">InputTensor</span></span> | <span data-ttu-id="76216-152">Input</span><span class="sxs-lookup"><span data-stu-id="76216-152">Input</span></span> | <span data-ttu-id="76216-153">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="76216-153">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="76216-154">4</span><span class="sxs-lookup"><span data-stu-id="76216-154">4</span></span> | <span data-ttu-id="76216-155">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="76216-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="76216-156">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="76216-156">InputGradientTensor</span></span> | <span data-ttu-id="76216-157">Input</span><span class="sxs-lookup"><span data-stu-id="76216-157">Input</span></span> | <span data-ttu-id="76216-158">{ BatchCount, ChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="76216-158">{ BatchCount, ChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="76216-159">4</span><span class="sxs-lookup"><span data-stu-id="76216-159">4</span></span> | <span data-ttu-id="76216-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="76216-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="76216-161">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="76216-161">OutputGradientTensor</span></span> | <span data-ttu-id="76216-162">Output</span><span class="sxs-lookup"><span data-stu-id="76216-162">Output</span></span> | <span data-ttu-id="76216-163">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="76216-163">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="76216-164">4</span><span class="sxs-lookup"><span data-stu-id="76216-164">4</span></span> | <span data-ttu-id="76216-165">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="76216-165">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="76216-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76216-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="76216-167">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="76216-167">**Header**</span></span> | <span data-ttu-id="76216-168">directml.h</span><span class="sxs-lookup"><span data-stu-id="76216-168">directml.h</span></span> |