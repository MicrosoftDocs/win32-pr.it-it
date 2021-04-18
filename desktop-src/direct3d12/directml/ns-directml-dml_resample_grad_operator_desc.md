---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Calcola le sfumature di propagazione per il ricampionamento (vedere [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
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
ms.openlocfilehash: 5808381f2e812ac20399b46672e51acd063bc6a5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320401"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="554f8-103">Struttura DML_RESAMPLE_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="554f8-103">DML_RESAMPLE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="554f8-104">Calcola le sfumature di propagazione per il ricampionamento (vedere [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="554f8-104">Computes backpropagation gradients for Resample (see [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span></span>

<span data-ttu-id="554f8-105">**DML_RESAMPLE1_OPERATOR_DESC** ridimensiona le dimensioni arbitrarie del tensore di input usando il campionamento più vicino o l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="554f8-105">**DML_RESAMPLE1_OPERATOR_DESC** rescales arbitrary dimensions of the input tensor using either nearest-neighbor sampling or bilinear interpolation.</span></span> <span data-ttu-id="554f8-106">Dato un *InputGradientTensor* con le stesse dimensioni dell' *output* di un **DML_RESAMPLE1_OPERATOR_DESC** equivalente, questo operatore produce un *OutputGradientTensor* con le stesse dimensioni dell' *input* della **DML_RESAMPLE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="554f8-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_RESAMPLE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of the **DML_RESAMPLE1_OPERATOR_DESC**.</span></span>

<span data-ttu-id="554f8-107">Si consideri, ad esempio, un **DML_RESAMPLE1_OPERATOR_DESC** che esegue un ridimensionamento adiacente più vicino di 1.5 x nella larghezza e 0,5 x nell'altezza.</span><span class="sxs-lookup"><span data-stu-id="554f8-107">As an example, consider a **DML_RESAMPLE1_OPERATOR_DESC** that performs a nearest-neighbor scaling of 1.5x in the width, and 0.5x in the height.</span></span>

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

<span data-ttu-id="554f8-108">Si noti che l'elemento 0A del tensore di input (con valore 1) contribuisce a due elementi nell'output, il primo elemento (con valore 2) contribuisce a un elemento nell'output, mentre il secondo e il terzo elementi (con valori 3 e 4) contribuiscono a nessun elemento dell'output.</span><span class="sxs-lookup"><span data-stu-id="554f8-108">Notice how the 0th element of the input tensor (with value 1) contributes to two elements in the output, the 1st element (with value 2) contributes to one element in the output, and the 2nd and 3rd elements (with values 3 and 4) contribute to no elements of the output.</span></span>

<span data-ttu-id="554f8-109">Il **DML_RESAMPLE_GRAD_OPERATOR_DESC** corrispondente eseguirà le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="554f8-109">The corresponding **DML_RESAMPLE_GRAD_OPERATOR_DESC** would perform the following.</span></span>

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

<span data-ttu-id="554f8-110">Si noti che i valori in *OutputGradientTensor* rappresentano i contributi ponderati di tale elemento al *OutputTensor* durante l'operatore **DML_RESAMPLE1_OPERATOR_DESC** originale.</span><span class="sxs-lookup"><span data-stu-id="554f8-110">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original **DML_RESAMPLE1_OPERATOR_DESC** operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="554f8-111">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="554f8-111">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="554f8-112">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="554f8-112">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="554f8-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="554f8-113">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="554f8-114">Members</span><span class="sxs-lookup"><span data-stu-id="554f8-114">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="554f8-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="554f8-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="554f8-116">Tensore di sfumatura in ingresso.</span><span class="sxs-lookup"><span data-stu-id="554f8-116">The incoming gradient tensor.</span></span> <span data-ttu-id="554f8-117">Questa operazione viene in genere ottenuta dall'output di propagation di un livello precedente.</span><span class="sxs-lookup"><span data-stu-id="554f8-117">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="554f8-118">In genere, questo tensore avrebbe le stesse dimensioni dell' *output* del [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) corrispondente nel passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="554f8-118">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="554f8-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="554f8-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="554f8-120">Un tensore di output contenente le sfumature ripropagate.</span><span class="sxs-lookup"><span data-stu-id="554f8-120">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="554f8-121">In genere, questo tensore avrebbe le stesse dimensioni dell' *input* del [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) corrispondente nel passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="554f8-121">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`InterpolationMode`

<span data-ttu-id="554f8-122">Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="554f8-122">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="554f8-123">Vedere *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="554f8-123">See *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`DimensionCount`

<span data-ttu-id="554f8-124">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="554f8-124">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="554f8-125">Il numero di elementi nelle matrici *Scales*, *InputPixelOffsets* e *OutputPixelOffsets* .</span><span class="sxs-lookup"><span data-stu-id="554f8-125">The number of elements in the *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* arrays.</span></span> <span data-ttu-id="554f8-126">Questo valore deve essere uguale a *DimensionCount* specificato in *InputGradientTensor* e *OutputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="554f8-126">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`Scales`

<span data-ttu-id="554f8-127">Tipo: \_ \_ Dimensione campo \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="554f8-127">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="554f8-128">Vedere *scale* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="554f8-128">See *Scales* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`InputPixelOffsets`

<span data-ttu-id="554f8-129">Tipo: \_ \_ Dimensione campo \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="554f8-129">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="554f8-130">Vedere *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="554f8-130">See *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`OutputPixelOffsets`

<span data-ttu-id="554f8-131">Tipo: \_ \_ Dimensione campo \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="554f8-131">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="554f8-132">Vedere *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="554f8-132">See *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="554f8-133">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="554f8-133">Availability</span></span>
<span data-ttu-id="554f8-134">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="554f8-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="554f8-135">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="554f8-135">Tensor constraints</span></span>
<span data-ttu-id="554f8-136">*InputGradientTensor* e *OutputGradientTensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="554f8-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="554f8-137">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="554f8-137">Tensor support</span></span>
| <span data-ttu-id="554f8-138">Tensore</span><span class="sxs-lookup"><span data-stu-id="554f8-138">Tensor</span></span> | <span data-ttu-id="554f8-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="554f8-139">Kind</span></span> | <span data-ttu-id="554f8-140">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="554f8-140">Supported dimension counts</span></span> | <span data-ttu-id="554f8-141">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="554f8-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="554f8-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="554f8-142">InputGradientTensor</span></span> | <span data-ttu-id="554f8-143">Input</span><span class="sxs-lookup"><span data-stu-id="554f8-143">Input</span></span> | <span data-ttu-id="554f8-144">4</span><span class="sxs-lookup"><span data-stu-id="554f8-144">4</span></span> | <span data-ttu-id="554f8-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="554f8-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="554f8-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="554f8-146">OutputGradientTensor</span></span> | <span data-ttu-id="554f8-147">Output</span><span class="sxs-lookup"><span data-stu-id="554f8-147">Output</span></span> | <span data-ttu-id="554f8-148">4</span><span class="sxs-lookup"><span data-stu-id="554f8-148">4</span></span> | <span data-ttu-id="554f8-149">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="554f8-149">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="554f8-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="554f8-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="554f8-151">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="554f8-151">**Header**</span></span> | <span data-ttu-id="554f8-152">directml. h</span><span class="sxs-lookup"><span data-stu-id="554f8-152">directml.h</span></span> |