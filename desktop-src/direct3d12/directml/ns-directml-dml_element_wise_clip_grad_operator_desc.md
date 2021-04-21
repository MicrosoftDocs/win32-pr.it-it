---
UID: NS:directml.DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
title: DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per [un clip per elemento.](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)
helpviewer_keywords:
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC structure
- direct3d12.dml_element_wise_clip_grad_operator_desc
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
ms.openlocfilehash: 224fbacdb8816a6aed6a7779c5c8ff991736ee6c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804490"
---
# <a name="dml_element_wise_clip_grad_operator_desc-directmlh"></a><span data-ttu-id="280b3-103">DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="280b3-103">DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="280b3-104">Calcola le sfumature di backpropagation per [il clip per elemento.](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="280b3-104">Computes backpropagation gradients for [element-wise clip](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).</span></span>

```
f(x, gradient) = if x <= Min then 0
                 if x >= Max then 0
                 else        then gradient
```

<span data-ttu-id="280b3-105">Questo operatore supporta l'esecuzione sul posto, ovvero è `OutputTensor` consentito creare un alias di *InputTensor durante* l'associazione.</span><span class="sxs-lookup"><span data-stu-id="280b3-105">This operator supports in-place execution, meaning `OutputTensor` is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="280b3-106">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.5 e successive).</span><span class="sxs-lookup"><span data-stu-id="280b3-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="280b3-107">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="280b3-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="280b3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="280b3-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    FLOAT Min;
    FLOAT Max;
};
```

## <a name="members"></a><span data-ttu-id="280b3-109">Members</span><span class="sxs-lookup"><span data-stu-id="280b3-109">Members</span></span>

`InputTensor`

<span data-ttu-id="280b3-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="280b3-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="280b3-111">Tensore della funzionalità di input.</span><span class="sxs-lookup"><span data-stu-id="280b3-111">The input feature tensor.</span></span> <span data-ttu-id="280b3-112">Si tratta in genere dello stesso tensore fornito da *InputTensor* DML_ELEMENT_WISE_CLIP_OPERATOR_DESC [nel](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="280b3-112">This is typically the same tensor that was provided as the *InputTensor* to [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="280b3-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="280b3-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="280b3-114">Tensore sfumatura in ingresso.</span><span class="sxs-lookup"><span data-stu-id="280b3-114">The incoming gradient tensor.</span></span> <span data-ttu-id="280b3-115">Questa operazione viene in genere ottenuta dall'output della backpropagazione di un livello precedente.</span><span class="sxs-lookup"><span data-stu-id="280b3-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="280b3-116">In genere questo tensore ha le stesse dimensioni *dell'output* dell'oggetto **DML_OPERATOR_ELEMENT_WISE_CLIP** nel passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="280b3-116">Typically this tensor would have the same sizes as the *output* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="280b3-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="280b3-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="280b3-118">Tensore di output contenente le sfumature backpropagate.</span><span class="sxs-lookup"><span data-stu-id="280b3-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="280b3-119">In genere, questo tensore ha le stesse dimensioni *dell'input* del **DML_OPERATOR_ELEMENT_WISE_CLIP** nel passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="280b3-119">Typically this tensor would have the same sizes as the *input* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.</span></span>

`Min`

<span data-ttu-id="280b3-120">Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="280b3-120">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="280b3-121">Valore minimo.</span><span class="sxs-lookup"><span data-stu-id="280b3-121">The minimum value.</span></span> <span data-ttu-id="280b3-122">Se x è in corrispondenza o al di sotto di questo valore, il risultato della sfumatura è 0.</span><span class="sxs-lookup"><span data-stu-id="280b3-122">If x is at or below this value, then the gradient result is 0.</span></span>

`Max`

<span data-ttu-id="280b3-123">Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="280b3-123">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="280b3-124">Valore massimo.</span><span class="sxs-lookup"><span data-stu-id="280b3-124">The maximum value.</span></span> <span data-ttu-id="280b3-125">Se x è al di sopra di questo valore, il risultato della sfumatura è 0.</span><span class="sxs-lookup"><span data-stu-id="280b3-125">If x is at or above this value, then the gradient result is 0.</span></span>

## <a name="availability"></a><span data-ttu-id="280b3-126">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="280b3-126">Availability</span></span>
<span data-ttu-id="280b3-127">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="280b3-127">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="280b3-128">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="280b3-128">Tensor constraints</span></span>
<span data-ttu-id="280b3-129">*InputGradientTensor,* *InputTensor* e *OutputGradientTensor* devono avere gli stessi *valori di DataType,* *DimensionCount* e *Sizes.*</span><span class="sxs-lookup"><span data-stu-id="280b3-129">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="280b3-130">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="280b3-130">Tensor support</span></span>
| <span data-ttu-id="280b3-131">Tensore</span><span class="sxs-lookup"><span data-stu-id="280b3-131">Tensor</span></span> | <span data-ttu-id="280b3-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="280b3-132">Kind</span></span> | <span data-ttu-id="280b3-133">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="280b3-133">Supported dimension counts</span></span> | <span data-ttu-id="280b3-134">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="280b3-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="280b3-135">InputTensor</span><span class="sxs-lookup"><span data-stu-id="280b3-135">InputTensor</span></span> | <span data-ttu-id="280b3-136">Input</span><span class="sxs-lookup"><span data-stu-id="280b3-136">Input</span></span> | <span data-ttu-id="280b3-137">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="280b3-137">1 to 8</span></span> | <span data-ttu-id="280b3-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="280b3-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="280b3-139">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="280b3-139">InputGradientTensor</span></span> | <span data-ttu-id="280b3-140">Input</span><span class="sxs-lookup"><span data-stu-id="280b3-140">Input</span></span> | <span data-ttu-id="280b3-141">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="280b3-141">1 to 8</span></span> | <span data-ttu-id="280b3-142">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="280b3-142">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="280b3-143">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="280b3-143">OutputGradientTensor</span></span> | <span data-ttu-id="280b3-144">Output</span><span class="sxs-lookup"><span data-stu-id="280b3-144">Output</span></span> | <span data-ttu-id="280b3-145">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="280b3-145">1 to 8</span></span> | <span data-ttu-id="280b3-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="280b3-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="280b3-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="280b3-147">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="280b3-148">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="280b3-148">**Header**</span></span> | <span data-ttu-id="280b3-149">directml.h</span><span class="sxs-lookup"><span data-stu-id="280b3-149">directml.h</span></span> |
