---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per il pooling medio (vedere [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: aaa2b5d2becac421214afe7c643426c1c93cf899
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417736"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="b528a-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="b528a-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b528a-104">Calcola le sfumature di backpropagation per il pooling medio (vedere [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="b528a-104">Computes backpropagation gradients for average pooling (see [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span></span>

<span data-ttu-id="b528a-105">Si consideri un DML_AVERAGE_POOLING_OPERATOR_DESC 2x2, senza spaziatura interna e uno stride di 1, che esegue le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b528a-105">Consider a 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, without padding and a stride of 1, that performs the following.</span></span>

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

<span data-ttu-id="b528a-106">Ogni finestra 2x2 nel tensore di input viene mediata per produrre un elemento dell'output (la lettura degli zeri per gli elementi oltre il bordo).</span><span class="sxs-lookup"><span data-stu-id="b528a-106">Each 2x2 window in the input tensor is averaged to produce one element of the output (reading zeros for elements beyond the edge).</span></span> <span data-ttu-id="b528a-107">Di seguito è riportato un esempio dell'output **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** parametri simili.</span><span class="sxs-lookup"><span data-stu-id="b528a-107">Here's an example of the output of **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** given similar parameters.</span></span>

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

<span data-ttu-id="b528a-108">Si noti che i valori in *OutputGradientTensor* rappresentano i contributi ponderati di tale elemento *all'elemento OutputTensor* durante l'operatore DML_AVERAGE_POOLING_OPERATOR_DESC originale. [](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="b528a-108">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b528a-109">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="b528a-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b528a-110">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="b528a-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b528a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b528a-111">Syntax</span></span>

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a><span data-ttu-id="b528a-112">Members</span><span class="sxs-lookup"><span data-stu-id="b528a-112">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="b528a-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b528a-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b528a-114">Tensore sfumatura in ingresso.</span><span class="sxs-lookup"><span data-stu-id="b528a-114">The incoming gradient tensor.</span></span> <span data-ttu-id="b528a-115">Questa operazione viene in genere ottenuta dall'output della backpropagazione di un livello precedente.</span><span class="sxs-lookup"><span data-stu-id="b528a-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="b528a-116">In genere questo tensore ha le stesse dimensioni *dell'output* dell'DML_AVERAGE_POOLING_OPERATOR_DESC [nel](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="b528a-116">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="b528a-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b528a-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b528a-118">Tensore di output contenente le sfumature backpropagate.</span><span class="sxs-lookup"><span data-stu-id="b528a-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="b528a-119">In genere, questo tensore ha le stesse dimensioni *dell'input* del [valore](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) DML_AVERAGE_POOLING_OPERATOR_DESC nel passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="b528a-119">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="b528a-120">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b528a-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b528a-121">Numero di elementi nelle *matrici Strides,* *WindowSize,* *StartPadding* ed *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="b528a-121">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="b528a-122">Questo valore deve essere uguale al numero di dimensioni spaziali.</span><span class="sxs-lookup"><span data-stu-id="b528a-122">This value must equal the spatial dimension count.</span></span> <span data-ttu-id="b528a-123">Il numero di dimensioni spaziali è 2 se vengono forniti tensori 4D oppure 3 se vengono forniti tensori 5D.</span><span class="sxs-lookup"><span data-stu-id="b528a-123">The spatial dimension count is 2 if 4D tensors are provided, or 3 if 5D tensors are provided.</span></span>

`Strides`

<span data-ttu-id="b528a-124">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b528a-124">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b528a-125">Vedere *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b528a-125">See *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`WindowSize`

<span data-ttu-id="b528a-126">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b528a-126">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b528a-127">Vedere *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b528a-127">See *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`StartPadding`

<span data-ttu-id="b528a-128">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b528a-128">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b528a-129">Vedere *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b528a-129">See *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`EndPadding`

<span data-ttu-id="b528a-130">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b528a-130">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b528a-131">Vedere *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b528a-131">See *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`IncludePadding`

<span data-ttu-id="b528a-132">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="b528a-132">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="b528a-133">Vedere *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b528a-133">See *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="b528a-134">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="b528a-134">Availability</span></span>
<span data-ttu-id="b528a-135">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="b528a-135">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b528a-136">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="b528a-136">Tensor constraints</span></span>
<span data-ttu-id="b528a-137">*InputGradientTensor* e *OutputGradientTensor* devono avere gli stessi *DataType* *e DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="b528a-137">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b528a-138">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="b528a-138">Tensor support</span></span>
| <span data-ttu-id="b528a-139">Tensore</span><span class="sxs-lookup"><span data-stu-id="b528a-139">Tensor</span></span> | <span data-ttu-id="b528a-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="b528a-140">Kind</span></span> | <span data-ttu-id="b528a-141">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="b528a-141">Supported dimension counts</span></span> | <span data-ttu-id="b528a-142">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="b528a-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b528a-143">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="b528a-143">InputGradientTensor</span></span> | <span data-ttu-id="b528a-144">Input</span><span class="sxs-lookup"><span data-stu-id="b528a-144">Input</span></span> | <span data-ttu-id="b528a-145">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="b528a-145">4 to 5</span></span> | <span data-ttu-id="b528a-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b528a-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="b528a-147">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="b528a-147">OutputGradientTensor</span></span> | <span data-ttu-id="b528a-148">Output</span><span class="sxs-lookup"><span data-stu-id="b528a-148">Output</span></span> | <span data-ttu-id="b528a-149">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="b528a-149">4 to 5</span></span> | <span data-ttu-id="b528a-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b528a-150">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="b528a-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b528a-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b528a-152">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="b528a-152">**Header**</span></span> | <span data-ttu-id="b528a-153">directml.h</span><span class="sxs-lookup"><span data-stu-id="b528a-153">directml.h</span></span> |