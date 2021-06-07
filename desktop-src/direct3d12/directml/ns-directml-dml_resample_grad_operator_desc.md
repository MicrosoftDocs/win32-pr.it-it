---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per Resample (vedere [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
helpviewer_keywords:
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- DML_RESAMPLE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RESAMPLE_GRAD_OPERATOR_DESC, DML_RESAMPLE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.openlocfilehash: ff2660257fa619edb72f10efb419f3c15f43fbde
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417808"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="b9617-103">DML_RESAMPLE_GRAD_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="b9617-103">DML_RESAMPLE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b9617-104">Calcola le sfumature di backpropagation per Resample (vedere [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="b9617-104">Computes backpropagation gradients for Resample (see [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span></span>

<span data-ttu-id="b9617-105">**DML_RESAMPLE1_OPERATOR_DESC** ridimensiona dimensioni arbitrarie del tensore di input usando il campionamento del vicino più prossimo o l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="b9617-105">**DML_RESAMPLE1_OPERATOR_DESC** rescales arbitrary dimensions of the input tensor using either nearest-neighbor sampling or bilinear interpolation.</span></span> <span data-ttu-id="b9617-106">Dato un *InputGradientTensor* con le stesse dimensioni *dell'output* di un **DML_RESAMPLE1_OPERATOR_DESC equivalente,** questo operatore produce un *OutputGradientTensor* con le stesse dimensioni dell'input del **DML_RESAMPLE1_OPERATOR_DESC**. </span><span class="sxs-lookup"><span data-stu-id="b9617-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_RESAMPLE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of the **DML_RESAMPLE1_OPERATOR_DESC**.</span></span>

<span data-ttu-id="b9617-107">Si consideri ad esempio un **DML_RESAMPLE1_OPERATOR_DESC** che esegue un ridimensionamento del vicino più vicino di 1,5x nella larghezza e 0,5x nell'altezza.</span><span class="sxs-lookup"><span data-stu-id="b9617-107">As an example, consider a **DML_RESAMPLE1_OPERATOR_DESC** that performs a nearest-neighbor scaling of 1.5x in the width, and 0.5x in the height.</span></span>

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

<span data-ttu-id="b9617-108">Si noti che il primo elemento del tensore di input (con valore 1) contribuisce a due elementi nell'output, il primo elemento (con valore 2) contribuisce a un elemento nell'output e il secondo e il terzo elemento (con i valori 3 e 4) non contribuiscono a nessun elemento dell'output.</span><span class="sxs-lookup"><span data-stu-id="b9617-108">Notice how the 0th element of the input tensor (with value 1) contributes to two elements in the output, the 1st element (with value 2) contributes to one element in the output, and the 2nd and 3rd elements (with values 3 and 4) contribute to no elements of the output.</span></span>

<span data-ttu-id="b9617-109">**L'DML_RESAMPLE_GRAD_OPERATOR_DESC** esegue le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b9617-109">The corresponding **DML_RESAMPLE_GRAD_OPERATOR_DESC** would perform the following.</span></span>

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

<span data-ttu-id="b9617-110">Si noti che i valori in *OutputGradientTensor* rappresentano i contributi ponderati di  tale elemento a *OutputTensor* durante l'operatore DML_RESAMPLE1_OPERATOR_DESC originale.</span><span class="sxs-lookup"><span data-stu-id="b9617-110">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original **DML_RESAMPLE1_OPERATOR_DESC** operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9617-111">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="b9617-111">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b9617-112">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="b9617-112">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9617-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9617-113">Syntax</span></span>

```cpp
struct DML_RESAMPLE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const FLOAT* Scales;
  _Field_size_(DimensionCount) const FLOAT* InputPixelOffsets;
  _Field_size_(DimensionCount) const FLOAT* OutputPixelOffsets;
};
```

## <a name="members"></a><span data-ttu-id="b9617-114">Members</span><span class="sxs-lookup"><span data-stu-id="b9617-114">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="b9617-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b9617-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b9617-116">Tensore sfumatura in ingresso.</span><span class="sxs-lookup"><span data-stu-id="b9617-116">The incoming gradient tensor.</span></span> <span data-ttu-id="b9617-117">Questa operazione viene in genere ottenuta dall'output della retropropagazione di un livello precedente.</span><span class="sxs-lookup"><span data-stu-id="b9617-117">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="b9617-118">In genere questo tensore ha le stesse dimensioni *dell'output* del [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) nel passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="b9617-118">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="b9617-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b9617-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b9617-120">Tensore di output contenente le sfumature di backpropagated.</span><span class="sxs-lookup"><span data-stu-id="b9617-120">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="b9617-121">In genere questo tensore avrebbe le stesse dimensioni *dell'input* del [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) corrispondente nel passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="b9617-121">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`InterpolationMode`

<span data-ttu-id="b9617-122">Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="b9617-122">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="b9617-123">Vedere *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b9617-123">See *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`DimensionCount`

<span data-ttu-id="b9617-124">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b9617-124">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b9617-125">Numero di elementi nelle matrici *Scales,* *InputPixelOffsets* e *OutputPixelOffsets.*</span><span class="sxs-lookup"><span data-stu-id="b9617-125">The number of elements in the *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* arrays.</span></span> <span data-ttu-id="b9617-126">Questo valore deve essere uguale *a DimensionCount* specificato in *InputGradientTensor* e *OutputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="b9617-126">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`Scales`

<span data-ttu-id="b9617-127">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b9617-127">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b9617-128">Vedere *Scales* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b9617-128">See *Scales* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`InputPixelOffsets`

<span data-ttu-id="b9617-129">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b9617-129">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b9617-130">Vedere *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b9617-130">See *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`OutputPixelOffsets`

<span data-ttu-id="b9617-131">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b9617-131">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b9617-132">Vedere *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b9617-132">See *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="b9617-133">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="b9617-133">Availability</span></span>
<span data-ttu-id="b9617-134">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="b9617-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b9617-135">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="b9617-135">Tensor constraints</span></span>
<span data-ttu-id="b9617-136">*InputGradientTensor* e *OutputGradientTensor* devono avere lo stesso *datatype*.</span><span class="sxs-lookup"><span data-stu-id="b9617-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b9617-137">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="b9617-137">Tensor support</span></span>
| <span data-ttu-id="b9617-138">Tensore</span><span class="sxs-lookup"><span data-stu-id="b9617-138">Tensor</span></span> | <span data-ttu-id="b9617-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9617-139">Kind</span></span> | <span data-ttu-id="b9617-140">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="b9617-140">Supported dimension counts</span></span> | <span data-ttu-id="b9617-141">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="b9617-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b9617-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="b9617-142">InputGradientTensor</span></span> | <span data-ttu-id="b9617-143">Input</span><span class="sxs-lookup"><span data-stu-id="b9617-143">Input</span></span> | <span data-ttu-id="b9617-144">4</span><span class="sxs-lookup"><span data-stu-id="b9617-144">4</span></span> | <span data-ttu-id="b9617-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b9617-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="b9617-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="b9617-146">OutputGradientTensor</span></span> | <span data-ttu-id="b9617-147">Output</span><span class="sxs-lookup"><span data-stu-id="b9617-147">Output</span></span> | <span data-ttu-id="b9617-148">4</span><span class="sxs-lookup"><span data-stu-id="b9617-148">4</span></span> | <span data-ttu-id="b9617-149">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b9617-149">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="b9617-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9617-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b9617-151">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="b9617-151">**Header**</span></span> | <span data-ttu-id="b9617-152">directml.h</span><span class="sxs-lookup"><span data-stu-id="b9617-152">directml.h</span></span> |