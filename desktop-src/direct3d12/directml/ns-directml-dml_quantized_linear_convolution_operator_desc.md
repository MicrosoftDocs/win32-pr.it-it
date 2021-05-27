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
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549785"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a><span data-ttu-id="e9f5b-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="e9f5b-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="e9f5b-106">Esegue una convoluzione di *FilterTensor* con *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="e9f5b-106">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="e9f5b-107">Questo operatore esegue la convoluzione in avanti sui dati quantizzati.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-107">This operator performs forward convolution on quantized data.</span></span> <span data-ttu-id="e9f5b-108">Questo operatore equivale matematicamente alla dequantizzazione degli input, alla evoluzione e alla quantizzazione dell'output.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-108">This operator is mathematically equivalent to dequantizing the inputs, convolving, and then quantizing the output.</span></span> 

<span data-ttu-id="e9f5b-109">Le funzioni lineari quantizzate usate da questo operatore sono le funzioni di quantizzazione lineare</span><span class="sxs-lookup"><span data-stu-id="e9f5b-109">The quantize linear functions used by this operator are the linear quantization functions</span></span>

### <a name="dequantize-function"></a><span data-ttu-id="e9f5b-110">Funzione Dequantize</span><span class="sxs-lookup"><span data-stu-id="e9f5b-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="e9f5b-111">Funzione Quantize</span><span class="sxs-lookup"><span data-stu-id="e9f5b-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="e9f5b-112">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="e9f5b-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e9f5b-113">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="e9f5b-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f5b-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9f5b-114">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="e9f5b-115">Members</span><span class="sxs-lookup"><span data-stu-id="e9f5b-115">Members</span></span>

`InputTensor`

<span data-ttu-id="e9f5b-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e9f5b-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e9f5b-117">Tensore contenente i dati di input.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-117">A tensor containing the input data.</span></span> <span data-ttu-id="e9f5b-118">Le dimensioni previste di *InputTensor* sono `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="e9f5b-118">The expected dimensions of the *InputTensor* are `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputScaleTensor`

<span data-ttu-id="e9f5b-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e9f5b-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e9f5b-120">Tensore contenente i dati della scala di input.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-120">A tensor containing the input scale data.</span></span> <span data-ttu-id="e9f5b-121">Le dimensioni previste di `InputScaleTensor` sono `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="e9f5b-121">The expected dimensions of the `InputScaleTensor` are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="e9f5b-122">Questo valore di scala viene usato per dequantizzare i valori di input.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-122">This scale value is used for dequantizing the input values.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="e9f5b-123">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e9f5b-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e9f5b-124">Tensore facoltativo contenente i dati del punto zero di input.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-124">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="e9f5b-125">Le dimensioni previste di *InputZeroPointTensor* sono `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="e9f5b-125">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="e9f5b-126">Questo valore di punto zero viene usato per dequantizzare i valori di input.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-126">This zero point value is used for dequantizing the input values.</span></span>


`FilterTensor`

<span data-ttu-id="e9f5b-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e9f5b-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e9f5b-128">Tensore contenente i dati del filtro.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-128">A tensor containing the filter data.</span></span> <span data-ttu-id="e9f5b-129">Le dimensioni previste di *FilterTensor* sono `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="e9f5b-129">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterScaleTensor`

<span data-ttu-id="e9f5b-130">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e9f5b-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e9f5b-131">Tensore contenente i dati di scala del filtro.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-131">A tensor containing the filter scale data.</span></span> <span data-ttu-id="e9f5b-132">Le dimensioni previste di sono `FilterScaleTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o se è necessaria `{ 1, OutputChannelCount, 1, 1 }` la quantizzazione per canale.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-132">The expected dimensions of the `FilterScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="e9f5b-133">Questo valore di scala viene usato per dequantizzare i valori di filtro.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-133">This scale value is used for dequantizing the filter values.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="e9f5b-134">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e9f5b-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e9f5b-135">Tensore facoltativo contenente i dati del filtro zero punti.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-135">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="e9f5b-136">Le dimensioni previste di *FilterZeroPointTensor* sono se è necessaria `{ 1, 1, 1, 1 }` la quantizzazione per tensore o se è necessaria `{ 1, OutputChannelCount, 1, 1 }` la quantizzazione per canale.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-136">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="e9f5b-137">Questo valore di punto zero viene usato per dequantizzare i valori di filtro.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-137">This zero point value is used for dequantizing the filter values.</span></span>


`BiasTensor`

<span data-ttu-id="e9f5b-138">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e9f5b-138">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e9f5b-139">Tensore contenente i dati di distorsione.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-139">A tensor containing the bias data.</span></span> <span data-ttu-id="e9f5b-140">Il tensore di distorsione è un tensore contenente dati trasmessi attraverso il tensore di output alla fine della convoluzione che viene aggiunto al risultato.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-140">The bias tensor is a tensor containing data which is broadcasted across the output tensor at the end of the convolution which is added to the result.</span></span> <span data-ttu-id="e9f5b-141">Le dimensioni previste di BiasTensor sono `{ 1, OutputChannelCount, 1, 1 }` per 4D.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-141">The expected dimensions of the BiasTensor are `{ 1, OutputChannelCount, 1, 1 }` for 4D.</span></span>


`OutputScaleTensor`

<span data-ttu-id="e9f5b-142">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e9f5b-142">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e9f5b-143">Tensore contenente i dati della scala di output.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-143">A tensor containing the output scale data.</span></span> <span data-ttu-id="e9f5b-144">Le dimensioni previste di OutputScaleTensor sono `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="e9f5b-144">The expected dimensions of the OutputScaleTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="e9f5b-145">Questo valore di scala di input viene usato per quantificare i valori di output della convoluzione.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-145">This input scale value is used for quantizing the convolution output values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="e9f5b-146">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e9f5b-146">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e9f5b-147">Tensore facoltativo contenente i dati del punto zero del filtro.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-147">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="e9f5b-148">Le dimensioni previste di OutputZeroPointTensor sono `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="e9f5b-148">The expected dimensions of the OutputZeroPointTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="e9f5b-149">Questo valore del punto zero di input viene usato per quantificare la convoluzione dei valori di output.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-149">This input zero point value is used for quantizing the convolution the output values.</span></span>


`OutputTensor`

<span data-ttu-id="e9f5b-150">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e9f5b-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e9f5b-151">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-151">A tensor to write the results to.</span></span> <span data-ttu-id="e9f5b-152">Le dimensioni previste di OutputTensor sono `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="e9f5b-152">The expected dimensions of the OutputTensor are `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="e9f5b-153">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="e9f5b-153">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="e9f5b-154">Numero di dimensioni spaziali per l'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-154">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="e9f5b-155">Le dimensioni spaziali sono le dimensioni inferiori del tensore filtro convoluzione *FilterTensor*.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-155">Spatial dimensions are the lower dimensions of the convolution filter tensor *FilterTensor*.</span></span> <span data-ttu-id="e9f5b-156">Questo valore determina anche le dimensioni delle matrici *Strides,* *Dilations,* *StartPadding* ed *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="e9f5b-156">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="e9f5b-157">È supportato solo il valore 2.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-157">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="e9f5b-158">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e9f5b-158">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e9f5b-159">Stride dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-159">The strides of the convolution operation.</span></span> <span data-ttu-id="e9f5b-160">Questi stride vengono applicati al filtro di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-160">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="e9f5b-161">Sono separati dagli stride del tensore inclusi in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="e9f5b-161">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="e9f5b-162">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e9f5b-162">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e9f5b-163">Dilatazioni dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-163">The Dilations of the convolution operation.</span></span> <span data-ttu-id="e9f5b-164">Le dilatazioni sono passi applicati agli elementi del kernel di filtro.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-164">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="e9f5b-165">Ciò ha l'effetto di simulare un kernel di filtro più grande tramite il riempimento degli elementi del kernel del filtro interno con zeri.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-165">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="e9f5b-166">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e9f5b-166">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e9f5b-167">Valori di spaziatura interna da applicare all'inizio di ogni dimensione spaziale del filtro e del tensore di input dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-167">The padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="e9f5b-168">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e9f5b-168">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e9f5b-169">Valori di spaziatura interna da applicare alla fine di ogni dimensione spaziale del filtro e del tensore di input dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-169">The padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="e9f5b-170">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="e9f5b-170">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="e9f5b-171">Numero di gruppi in cui dividere l'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-171">The number of groups which to divide the convolution operation into.</span></span> <span data-ttu-id="e9f5b-172">*GroupCount* può essere usato per ottenere una convoluzione approfondita impostando *GroupCount* uguale al conteggio dei canali di input.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-172">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="e9f5b-173">In questo modo la convoluzione viene suddivisa in una convoluzione separata per canale di input.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-173">This divides the convolution up into a separate convolution per input channel.</span></span> 

## <a name="availability"></a><span data-ttu-id="e9f5b-174">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="e9f5b-174">Availability</span></span>
<span data-ttu-id="e9f5b-175">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="e9f5b-175">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e9f5b-176">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="e9f5b-176">Tensor constraints</span></span>
* <span data-ttu-id="e9f5b-177">*FilterTensor* e *FilterZeroPointTensor* devono avere lo stesso *Tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-177">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="e9f5b-178">*InputTensor* e *InputZeroPointTensor* devono avere lo stesso *Tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-178">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="e9f5b-179">*OutputTensor* e `OutputZeroPointTensor` devono avere lo stesso Tipo di *dati*.</span><span class="sxs-lookup"><span data-stu-id="e9f5b-179">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e9f5b-180">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="e9f5b-180">Tensor support</span></span>
| <span data-ttu-id="e9f5b-181">Tensore</span><span class="sxs-lookup"><span data-stu-id="e9f5b-181">Tensor</span></span> | <span data-ttu-id="e9f5b-182">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9f5b-182">Kind</span></span> | <span data-ttu-id="e9f5b-183">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="e9f5b-183">Supported dimension counts</span></span> | <span data-ttu-id="e9f5b-184">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="e9f5b-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e9f5b-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="e9f5b-185">InputTensor</span></span> | <span data-ttu-id="e9f5b-186">Input</span><span class="sxs-lookup"><span data-stu-id="e9f5b-186">Input</span></span> | <span data-ttu-id="e9f5b-187">4</span><span class="sxs-lookup"><span data-stu-id="e9f5b-187">4</span></span> | <span data-ttu-id="e9f5b-188">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="e9f5b-188">INT8, UINT8</span></span> |
| <span data-ttu-id="e9f5b-189">InputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="e9f5b-189">InputScaleTensor</span></span> | <span data-ttu-id="e9f5b-190">Input</span><span class="sxs-lookup"><span data-stu-id="e9f5b-190">Input</span></span> | <span data-ttu-id="e9f5b-191">4</span><span class="sxs-lookup"><span data-stu-id="e9f5b-191">4</span></span> | <span data-ttu-id="e9f5b-192">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="e9f5b-192">FLOAT32</span></span> |
| <span data-ttu-id="e9f5b-193">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="e9f5b-193">InputZeroPointTensor</span></span> | <span data-ttu-id="e9f5b-194">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="e9f5b-194">Optional input</span></span> | <span data-ttu-id="e9f5b-195">4</span><span class="sxs-lookup"><span data-stu-id="e9f5b-195">4</span></span> | <span data-ttu-id="e9f5b-196">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="e9f5b-196">INT8, UINT8</span></span> |
| <span data-ttu-id="e9f5b-197">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="e9f5b-197">FilterTensor</span></span> | <span data-ttu-id="e9f5b-198">Input</span><span class="sxs-lookup"><span data-stu-id="e9f5b-198">Input</span></span> | <span data-ttu-id="e9f5b-199">4</span><span class="sxs-lookup"><span data-stu-id="e9f5b-199">4</span></span> | <span data-ttu-id="e9f5b-200">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="e9f5b-200">INT8, UINT8</span></span> |
| <span data-ttu-id="e9f5b-201">FilterScaleTensor</span><span class="sxs-lookup"><span data-stu-id="e9f5b-201">FilterScaleTensor</span></span> | <span data-ttu-id="e9f5b-202">Input</span><span class="sxs-lookup"><span data-stu-id="e9f5b-202">Input</span></span> | <span data-ttu-id="e9f5b-203">4</span><span class="sxs-lookup"><span data-stu-id="e9f5b-203">4</span></span> | <span data-ttu-id="e9f5b-204">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="e9f5b-204">FLOAT32</span></span> |
| <span data-ttu-id="e9f5b-205">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="e9f5b-205">FilterZeroPointTensor</span></span> | <span data-ttu-id="e9f5b-206">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="e9f5b-206">Optional input</span></span> | <span data-ttu-id="e9f5b-207">4</span><span class="sxs-lookup"><span data-stu-id="e9f5b-207">4</span></span> | <span data-ttu-id="e9f5b-208">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="e9f5b-208">INT8, UINT8</span></span> |
| <span data-ttu-id="e9f5b-209">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="e9f5b-209">BiasTensor</span></span> | <span data-ttu-id="e9f5b-210">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="e9f5b-210">Optional input</span></span> | <span data-ttu-id="e9f5b-211">4</span><span class="sxs-lookup"><span data-stu-id="e9f5b-211">4</span></span> | <span data-ttu-id="e9f5b-212">INT32</span><span class="sxs-lookup"><span data-stu-id="e9f5b-212">INT32</span></span> |
| <span data-ttu-id="e9f5b-213">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="e9f5b-213">OutputScaleTensor</span></span> | <span data-ttu-id="e9f5b-214">Input</span><span class="sxs-lookup"><span data-stu-id="e9f5b-214">Input</span></span> | <span data-ttu-id="e9f5b-215">4</span><span class="sxs-lookup"><span data-stu-id="e9f5b-215">4</span></span> | <span data-ttu-id="e9f5b-216">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="e9f5b-216">FLOAT32</span></span> |
| <span data-ttu-id="e9f5b-217">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="e9f5b-217">OutputZeroPointTensor</span></span> | <span data-ttu-id="e9f5b-218">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="e9f5b-218">Optional input</span></span> | <span data-ttu-id="e9f5b-219">4</span><span class="sxs-lookup"><span data-stu-id="e9f5b-219">4</span></span> | <span data-ttu-id="e9f5b-220">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="e9f5b-220">INT8, UINT8</span></span> |
| <span data-ttu-id="e9f5b-221">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e9f5b-221">OutputTensor</span></span> | <span data-ttu-id="e9f5b-222">Output</span><span class="sxs-lookup"><span data-stu-id="e9f5b-222">Output</span></span> | <span data-ttu-id="e9f5b-223">4</span><span class="sxs-lookup"><span data-stu-id="e9f5b-223">4</span></span> | <span data-ttu-id="e9f5b-224">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="e9f5b-224">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="e9f5b-225">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9f5b-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e9f5b-226">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="e9f5b-226">**Header**</span></span> | <span data-ttu-id="e9f5b-227">directml.h</span><span class="sxs-lookup"><span data-stu-id="e9f5b-227">directml.h</span></span> |