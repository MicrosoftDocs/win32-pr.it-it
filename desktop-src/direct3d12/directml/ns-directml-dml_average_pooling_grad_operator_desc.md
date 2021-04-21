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
ms.openlocfilehash: 5c2803fc300ca862d54a74aee1c864e9097e3d8e
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803356"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="05d56-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="05d56-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="05d56-104">Calcola le sfumature di backpropagation per il pooling medio (vedere [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="05d56-104">Computes backpropagation gradients for average pooling (see [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span></span>

<span data-ttu-id="05d56-105">Si consideri un DML_AVERAGE_POOLING_OPERATOR_DESC 2x2, senza spaziatura interna e uno stride di 1, che esegue le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="05d56-105">Consider a 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, without padding and a stride of 1, that performs the following.</span></span>

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

<span data-ttu-id="05d56-106">Ogni finestra 2x2 nel tensore di input viene mediata per produrre un elemento dell'output (lettura degli zeri per gli elementi oltre il bordo).</span><span class="sxs-lookup"><span data-stu-id="05d56-106">Each 2x2 window in the input tensor is averaged to produce one element of the output (reading zeros for elements beyond the edge).</span></span> <span data-ttu-id="05d56-107">Di seguito è riportato un esempio dell'output **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** parametri simili.</span><span class="sxs-lookup"><span data-stu-id="05d56-107">Here's an example of the output of **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** given similar parameters.</span></span>

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

<span data-ttu-id="05d56-108">Si noti che i valori in *OutputGradientTensor* rappresentano i contributi ponderati di [](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) tale elemento a *OutputTensor* durante l'operatore DML_AVERAGE_POOLING_OPERATOR_DESC originale.</span><span class="sxs-lookup"><span data-stu-id="05d56-108">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05d56-109">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="05d56-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="05d56-110">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="05d56-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="05d56-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05d56-111">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="05d56-112">Members</span><span class="sxs-lookup"><span data-stu-id="05d56-112">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="05d56-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="05d56-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="05d56-114">Tensore sfumatura in ingresso.</span><span class="sxs-lookup"><span data-stu-id="05d56-114">The incoming gradient tensor.</span></span> <span data-ttu-id="05d56-115">Questa operazione viene in genere ottenuta dall'output della retropropagazione di un livello precedente.</span><span class="sxs-lookup"><span data-stu-id="05d56-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="05d56-116">In genere questo tensore avrebbe le stesse dimensioni *dell'output* del [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) nel passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="05d56-116">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="05d56-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="05d56-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="05d56-118">Tensore di output contenente le sfumature di backpropagated.</span><span class="sxs-lookup"><span data-stu-id="05d56-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="05d56-119">In genere questo tensore avrebbe le stesse dimensioni *dell'input* del [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) nel passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="05d56-119">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="05d56-120">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="05d56-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="05d56-121">Numero di elementi nelle *matrici Strides,* *WindowSize,* *StartPadding* *ed EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="05d56-121">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="05d56-122">Questo valore deve essere uguale al conteggio delle dimensioni spaziali.</span><span class="sxs-lookup"><span data-stu-id="05d56-122">This value must equal the spatial dimension count.</span></span> <span data-ttu-id="05d56-123">Il numero di dimensioni spaziali è 2 se vengono forniti tensori 4D o 3 se vengono forniti tensori 5D.</span><span class="sxs-lookup"><span data-stu-id="05d56-123">The spatial dimension count is 2 if 4D tensors are provided, or 3 if 5D tensors are provided.</span></span>

`Strides`

<span data-ttu-id="05d56-124">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="05d56-124">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="05d56-125">Vedere *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="05d56-125">See *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`WindowSize`

<span data-ttu-id="05d56-126">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="05d56-126">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="05d56-127">Vedere *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="05d56-127">See *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`StartPadding`

<span data-ttu-id="05d56-128">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="05d56-128">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="05d56-129">Vedere *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="05d56-129">See *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`EndPadding`

<span data-ttu-id="05d56-130">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="05d56-130">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="05d56-131">Vedere *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="05d56-131">See *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`IncludePadding`

<span data-ttu-id="05d56-132">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="05d56-132">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="05d56-133">Vedere *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="05d56-133">See *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="05d56-134">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="05d56-134">Availability</span></span>
<span data-ttu-id="05d56-135">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="05d56-135">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="05d56-136">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="05d56-136">Tensor constraints</span></span>
<span data-ttu-id="05d56-137">*InputGradientTensor* e *OutputGradientTensor* devono avere gli stessi *DataType* *e DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="05d56-137">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="05d56-138">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="05d56-138">Tensor support</span></span>
| <span data-ttu-id="05d56-139">Tensore</span><span class="sxs-lookup"><span data-stu-id="05d56-139">Tensor</span></span> | <span data-ttu-id="05d56-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="05d56-140">Kind</span></span> | <span data-ttu-id="05d56-141">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="05d56-141">Supported dimension counts</span></span> | <span data-ttu-id="05d56-142">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="05d56-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="05d56-143">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="05d56-143">InputGradientTensor</span></span> | <span data-ttu-id="05d56-144">Input</span><span class="sxs-lookup"><span data-stu-id="05d56-144">Input</span></span> | <span data-ttu-id="05d56-145">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="05d56-145">4 to 5</span></span> | <span data-ttu-id="05d56-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="05d56-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="05d56-147">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="05d56-147">OutputGradientTensor</span></span> | <span data-ttu-id="05d56-148">Output</span><span class="sxs-lookup"><span data-stu-id="05d56-148">Output</span></span> | <span data-ttu-id="05d56-149">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="05d56-149">4 to 5</span></span> | <span data-ttu-id="05d56-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="05d56-150">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="05d56-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05d56-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="05d56-152">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="05d56-152">**Header**</span></span> | <span data-ttu-id="05d56-153">directml.h</span><span class="sxs-lookup"><span data-stu-id="05d56-153">directml.h</span></span> |