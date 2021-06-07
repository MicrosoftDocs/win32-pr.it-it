---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Esegue una convoluzione di *FilterTensor* con *InputTensor.* Questo operatore esegue la convoluzione in avanti sui dati quantizzati. Questo operatore equivale matematicamente alla dequantizzazione degli input, alla evoluzione e alla quantizzazione dell'output.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_convolution_operator_desc
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.openlocfilehash: 5b98e1f57268cab70c2fb672991bce3d67419db8
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417529"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a><span data-ttu-id="cd637-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="cd637-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="cd637-106">Esegue una convoluzione di *FilterTensor* con *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="cd637-106">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="cd637-107">Questo operatore esegue la convoluzione in avanti sui dati quantizzati.</span><span class="sxs-lookup"><span data-stu-id="cd637-107">This operator performs forward convolution on quantized data.</span></span> <span data-ttu-id="cd637-108">Questo operatore equivale matematicamente alla dequantizzazione degli input, alla evoluzione e alla quantizzazione dell'output.</span><span class="sxs-lookup"><span data-stu-id="cd637-108">This operator is mathematically equivalent to dequantizing the inputs, convolving, and then quantizing the output.</span></span> 

<span data-ttu-id="cd637-109">Le funzioni lineari quantizzate usate da questo operatore sono le funzioni di quantizzazione lineare</span><span class="sxs-lookup"><span data-stu-id="cd637-109">The quantize linear functions used by this operator are the linear quantization functions</span></span>

### <a name="dequantize-function"></a><span data-ttu-id="cd637-110">Funzione Dequantize</span><span class="sxs-lookup"><span data-stu-id="cd637-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="cd637-111">Funzione Quantize</span><span class="sxs-lookup"><span data-stu-id="cd637-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="cd637-112">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="cd637-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="cd637-113">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="cd637-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd637-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd637-114">Syntax</span></span>
```cpp
struct DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputScaleTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterScaleTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *BiasTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```



## <a name="members"></a><span data-ttu-id="cd637-115">Members</span><span class="sxs-lookup"><span data-stu-id="cd637-115">Members</span></span>

`InputTensor`

<span data-ttu-id="cd637-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd637-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd637-117">Tensore contenente i dati di input.</span><span class="sxs-lookup"><span data-stu-id="cd637-117">A tensor containing the input data.</span></span> <span data-ttu-id="cd637-118">Le dimensioni previste di *InputTensor* sono `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="cd637-118">The expected dimensions of the *InputTensor* are `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputScaleTensor`

<span data-ttu-id="cd637-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd637-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd637-120">Tensore contenente i dati della scala di input.</span><span class="sxs-lookup"><span data-stu-id="cd637-120">A tensor containing the input scale data.</span></span> <span data-ttu-id="cd637-121">Le dimensioni previste di `InputScaleTensor` sono `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="cd637-121">The expected dimensions of the `InputScaleTensor` are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="cd637-122">Questo valore di scala viene usato per dequantizzare i valori di input.</span><span class="sxs-lookup"><span data-stu-id="cd637-122">This scale value is used for dequantizing the input values.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="cd637-123">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd637-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd637-124">Tensore facoltativo contenente i dati del punto zero di input.</span><span class="sxs-lookup"><span data-stu-id="cd637-124">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="cd637-125">Le dimensioni previste di *InputZeroPointTensor* sono `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="cd637-125">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="cd637-126">Questo valore del punto zero viene usato per dequantizzare i valori di input.</span><span class="sxs-lookup"><span data-stu-id="cd637-126">This zero point value is used for dequantizing the input values.</span></span>


`FilterTensor`

<span data-ttu-id="cd637-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd637-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd637-128">Tensore contenente i dati del filtro.</span><span class="sxs-lookup"><span data-stu-id="cd637-128">A tensor containing the filter data.</span></span> <span data-ttu-id="cd637-129">Le dimensioni previste di *FilterTensor* sono `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="cd637-129">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterScaleTensor`

<span data-ttu-id="cd637-130">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd637-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd637-131">Tensore contenente i dati della scala del filtro.</span><span class="sxs-lookup"><span data-stu-id="cd637-131">A tensor containing the filter scale data.</span></span> <span data-ttu-id="cd637-132">Le dimensioni previste di sono `FilterScaleTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o `{ 1, OutputChannelCount, 1, 1 }` se è necessaria la quantizzazione per canale.</span><span class="sxs-lookup"><span data-stu-id="cd637-132">The expected dimensions of the `FilterScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="cd637-133">Questo valore di scala viene usato per dequantizzare i valori di filtro.</span><span class="sxs-lookup"><span data-stu-id="cd637-133">This scale value is used for dequantizing the filter values.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="cd637-134">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd637-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd637-135">Tensore facoltativo contenente i dati del punto zero del filtro.</span><span class="sxs-lookup"><span data-stu-id="cd637-135">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="cd637-136">Le dimensioni previste di *FilterZeroPointTensor* sono se è necessaria la quantizzazione per tensore o se `{ 1, 1, 1, 1 }` è necessaria la `{ 1, OutputChannelCount, 1, 1 }` quantizzazione per canale.</span><span class="sxs-lookup"><span data-stu-id="cd637-136">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="cd637-137">Questo valore del punto zero viene usato per dequantizzare i valori di filtro.</span><span class="sxs-lookup"><span data-stu-id="cd637-137">This zero point value is used for dequantizing the filter values.</span></span>


`BiasTensor`

<span data-ttu-id="cd637-138">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd637-138">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd637-139">Tensore contenente i dati di distorsione.</span><span class="sxs-lookup"><span data-stu-id="cd637-139">A tensor containing the bias data.</span></span> <span data-ttu-id="cd637-140">Il tensore di distorsione è un tensore contenente dati che vengono trasmessi attraverso il tensore di output alla fine della convoluzione che viene aggiunto al risultato.</span><span class="sxs-lookup"><span data-stu-id="cd637-140">The bias tensor is a tensor containing data which is broadcasted across the output tensor at the end of the convolution which is added to the result.</span></span> <span data-ttu-id="cd637-141">Le dimensioni previste di BiasTensor sono `{ 1, OutputChannelCount, 1, 1 }` per 4D.</span><span class="sxs-lookup"><span data-stu-id="cd637-141">The expected dimensions of the BiasTensor are `{ 1, OutputChannelCount, 1, 1 }` for 4D.</span></span>


`OutputScaleTensor`

<span data-ttu-id="cd637-142">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd637-142">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd637-143">Tensore contenente i dati della scala di output.</span><span class="sxs-lookup"><span data-stu-id="cd637-143">A tensor containing the output scale data.</span></span> <span data-ttu-id="cd637-144">Le dimensioni previste di OutputScaleTensor sono `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="cd637-144">The expected dimensions of the OutputScaleTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="cd637-145">Questo valore di scala di input viene usato per quantificare i valori di output della convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd637-145">This input scale value is used for quantizing the convolution output values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="cd637-146">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd637-146">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd637-147">Tensore facoltativo contenente i dati del punto zero del filtro.</span><span class="sxs-lookup"><span data-stu-id="cd637-147">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="cd637-148">Le dimensioni previste di OutputZeroPointTensor sono `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="cd637-148">The expected dimensions of the OutputZeroPointTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="cd637-149">Questo valore del punto zero di input viene usato per quantificare la convoluzione dei valori di output.</span><span class="sxs-lookup"><span data-stu-id="cd637-149">This input zero point value is used for quantizing the convolution the output values.</span></span>


`OutputTensor`

<span data-ttu-id="cd637-150">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd637-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd637-151">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="cd637-151">A tensor to write the results to.</span></span> <span data-ttu-id="cd637-152">Le dimensioni previste di OutputTensor sono `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="cd637-152">The expected dimensions of the OutputTensor are `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="cd637-153">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="cd637-153">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="cd637-154">Numero di dimensioni spaziali per l'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd637-154">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="cd637-155">Le dimensioni spaziali sono le dimensioni inferiori del tensore filtro convoluzione *FilterTensor*.</span><span class="sxs-lookup"><span data-stu-id="cd637-155">Spatial dimensions are the lower dimensions of the convolution filter tensor *FilterTensor*.</span></span> <span data-ttu-id="cd637-156">Questo valore determina anche le dimensioni delle matrici *Strides,* *Dilations,* *StartPadding* ed *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="cd637-156">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="cd637-157">È supportato solo il valore 2.</span><span class="sxs-lookup"><span data-stu-id="cd637-157">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="cd637-158">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd637-158">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cd637-159">Stride dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd637-159">The strides of the convolution operation.</span></span> <span data-ttu-id="cd637-160">Questi stride vengono applicati al filtro di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd637-160">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="cd637-161">Sono separati dagli stride del tensore inclusi in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="cd637-161">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="cd637-162">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd637-162">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cd637-163">Dilations dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd637-163">The Dilations of the convolution operation.</span></span> <span data-ttu-id="cd637-164">Le dilazioni sono stride applicati agli elementi del kernel di filtro.</span><span class="sxs-lookup"><span data-stu-id="cd637-164">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="cd637-165">Ciò ha l'effetto di simulare un kernel di filtro più grande tramite il riempimento degli elementi interni del kernel del filtro con zeri.</span><span class="sxs-lookup"><span data-stu-id="cd637-165">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="cd637-166">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd637-166">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cd637-167">Valori di riempimento da applicare all'inizio di ogni dimensione spaziale del filtro e del tensore di input dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd637-167">The padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="cd637-168">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd637-168">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cd637-169">Valori di riempimento da applicare alla fine di ogni dimensione spaziale del filtro e del tensore di input dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd637-169">The padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="cd637-170">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="cd637-170">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="cd637-171">Numero di gruppi in cui dividere l'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd637-171">The number of groups which to divide the convolution operation into.</span></span> <span data-ttu-id="cd637-172">*GroupCount* può essere usato per ottenere una convoluzione a livello di profondità impostando *GroupCount* su un valore uguale al numero di canali di input.</span><span class="sxs-lookup"><span data-stu-id="cd637-172">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="cd637-173">In questo modo la convoluzione viene suddivisa in una convoluzione separata per canale di input.</span><span class="sxs-lookup"><span data-stu-id="cd637-173">This divides the convolution up into a separate convolution per input channel.</span></span> 

## <a name="availability"></a><span data-ttu-id="cd637-174">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="cd637-174">Availability</span></span>
<span data-ttu-id="cd637-175">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="cd637-175">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="cd637-176">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="cd637-176">Tensor constraints</span></span>
* <span data-ttu-id="cd637-177">*FilterTensor* e *FilterZeroPointTensor* devono avere lo stesso *tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="cd637-177">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="cd637-178">*InputTensor* e *InputZeroPointTensor* devono avere lo stesso *tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="cd637-178">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="cd637-179">*OutputTensor* e `OutputZeroPointTensor` devono avere lo stesso *datatype*.</span><span class="sxs-lookup"><span data-stu-id="cd637-179">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="cd637-180">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="cd637-180">Tensor support</span></span>
| <span data-ttu-id="cd637-181">Tensore</span><span class="sxs-lookup"><span data-stu-id="cd637-181">Tensor</span></span> | <span data-ttu-id="cd637-182">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd637-182">Kind</span></span> | <span data-ttu-id="cd637-183">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="cd637-183">Supported dimension counts</span></span> | <span data-ttu-id="cd637-184">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="cd637-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="cd637-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="cd637-185">InputTensor</span></span> | <span data-ttu-id="cd637-186">Input</span><span class="sxs-lookup"><span data-stu-id="cd637-186">Input</span></span> | <span data-ttu-id="cd637-187">4</span><span class="sxs-lookup"><span data-stu-id="cd637-187">4</span></span> | <span data-ttu-id="cd637-188">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cd637-188">INT8, UINT8</span></span> |
| <span data-ttu-id="cd637-189">InputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cd637-189">InputScaleTensor</span></span> | <span data-ttu-id="cd637-190">Input</span><span class="sxs-lookup"><span data-stu-id="cd637-190">Input</span></span> | <span data-ttu-id="cd637-191">4</span><span class="sxs-lookup"><span data-stu-id="cd637-191">4</span></span> | <span data-ttu-id="cd637-192">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="cd637-192">FLOAT32</span></span> |
| <span data-ttu-id="cd637-193">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="cd637-193">InputZeroPointTensor</span></span> | <span data-ttu-id="cd637-194">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="cd637-194">Optional input</span></span> | <span data-ttu-id="cd637-195">4</span><span class="sxs-lookup"><span data-stu-id="cd637-195">4</span></span> | <span data-ttu-id="cd637-196">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cd637-196">INT8, UINT8</span></span> |
| <span data-ttu-id="cd637-197">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="cd637-197">FilterTensor</span></span> | <span data-ttu-id="cd637-198">Input</span><span class="sxs-lookup"><span data-stu-id="cd637-198">Input</span></span> | <span data-ttu-id="cd637-199">4</span><span class="sxs-lookup"><span data-stu-id="cd637-199">4</span></span> | <span data-ttu-id="cd637-200">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cd637-200">INT8, UINT8</span></span> |
| <span data-ttu-id="cd637-201">FilterScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cd637-201">FilterScaleTensor</span></span> | <span data-ttu-id="cd637-202">Input</span><span class="sxs-lookup"><span data-stu-id="cd637-202">Input</span></span> | <span data-ttu-id="cd637-203">4</span><span class="sxs-lookup"><span data-stu-id="cd637-203">4</span></span> | <span data-ttu-id="cd637-204">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="cd637-204">FLOAT32</span></span> |
| <span data-ttu-id="cd637-205">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="cd637-205">FilterZeroPointTensor</span></span> | <span data-ttu-id="cd637-206">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="cd637-206">Optional input</span></span> | <span data-ttu-id="cd637-207">4</span><span class="sxs-lookup"><span data-stu-id="cd637-207">4</span></span> | <span data-ttu-id="cd637-208">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cd637-208">INT8, UINT8</span></span> |
| <span data-ttu-id="cd637-209">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="cd637-209">BiasTensor</span></span> | <span data-ttu-id="cd637-210">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="cd637-210">Optional input</span></span> | <span data-ttu-id="cd637-211">4</span><span class="sxs-lookup"><span data-stu-id="cd637-211">4</span></span> | <span data-ttu-id="cd637-212">INT32</span><span class="sxs-lookup"><span data-stu-id="cd637-212">INT32</span></span> |
| <span data-ttu-id="cd637-213">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cd637-213">OutputScaleTensor</span></span> | <span data-ttu-id="cd637-214">Input</span><span class="sxs-lookup"><span data-stu-id="cd637-214">Input</span></span> | <span data-ttu-id="cd637-215">4</span><span class="sxs-lookup"><span data-stu-id="cd637-215">4</span></span> | <span data-ttu-id="cd637-216">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="cd637-216">FLOAT32</span></span> |
| <span data-ttu-id="cd637-217">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="cd637-217">OutputZeroPointTensor</span></span> | <span data-ttu-id="cd637-218">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="cd637-218">Optional input</span></span> | <span data-ttu-id="cd637-219">4</span><span class="sxs-lookup"><span data-stu-id="cd637-219">4</span></span> | <span data-ttu-id="cd637-220">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cd637-220">INT8, UINT8</span></span> |
| <span data-ttu-id="cd637-221">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="cd637-221">OutputTensor</span></span> | <span data-ttu-id="cd637-222">Output</span><span class="sxs-lookup"><span data-stu-id="cd637-222">Output</span></span> | <span data-ttu-id="cd637-223">4</span><span class="sxs-lookup"><span data-stu-id="cd637-223">4</span></span> | <span data-ttu-id="cd637-224">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cd637-224">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="cd637-225">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd637-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cd637-226">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="cd637-226">**Header**</span></span> | <span data-ttu-id="cd637-227">directml.h</span><span class="sxs-lookup"><span data-stu-id="cd637-227">directml.h</span></span> |