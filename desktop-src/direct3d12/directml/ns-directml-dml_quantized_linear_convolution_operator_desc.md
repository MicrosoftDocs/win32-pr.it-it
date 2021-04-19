---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Esegue una convoluzione di *FilterTensor* con *InputTensor*. Questo operatore esegue la convoluzione in avanti sui dati quantizzati. Questo operatore è matematicamente equivalente a dequantizzare gli input, convolving, e quindi a quantizzare l'output.
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
ms.openlocfilehash: 01193b19744f413690a3cb5ecccbb8fa60626cb0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320361"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a><span data-ttu-id="cd554-105">Struttura DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="cd554-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="cd554-106">Esegue una convoluzione di *FilterTensor* con *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="cd554-106">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="cd554-107">Questo operatore esegue la convoluzione in avanti sui dati quantizzati.</span><span class="sxs-lookup"><span data-stu-id="cd554-107">This operator performs forward convolution on quantized data.</span></span> <span data-ttu-id="cd554-108">Questo operatore è matematicamente equivalente a dequantizzare gli input, convolving, e quindi a quantizzare l'output.</span><span class="sxs-lookup"><span data-stu-id="cd554-108">This operator is mathematically equivalent to dequantizing the inputs, convolving, and then quantizing the output.</span></span> 

<span data-ttu-id="cd554-109">Le funzioni lineari quantizzate utilizzate da questo operatore sono le funzioni di quantizzazione lineare</span><span class="sxs-lookup"><span data-stu-id="cd554-109">The quantize linear functions used by this operator are the linear quantization functions</span></span>

### <a name="dequantize-function"></a><span data-ttu-id="cd554-110">Funzione dequantizzate</span><span class="sxs-lookup"><span data-stu-id="cd554-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="cd554-111">Funzione quantizzate</span><span class="sxs-lookup"><span data-stu-id="cd554-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="cd554-112">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="cd554-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="cd554-113">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="cd554-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd554-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd554-114">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="cd554-115">Members</span><span class="sxs-lookup"><span data-stu-id="cd554-115">Members</span></span>

`InputTensor`

<span data-ttu-id="cd554-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd554-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd554-117">Un tensore contenente i dati di input.</span><span class="sxs-lookup"><span data-stu-id="cd554-117">A tensor containing the input data.</span></span> <span data-ttu-id="cd554-118">Le dimensioni previste di *InputTensor* sono `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="cd554-118">The expected dimensions of the *InputTensor* are `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputScaleTensor`

<span data-ttu-id="cd554-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd554-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd554-120">Un tensore contenente i dati della scala di input.</span><span class="sxs-lookup"><span data-stu-id="cd554-120">A tensor containing the input scale data.</span></span> <span data-ttu-id="cd554-121">Le dimensioni previste di `InputScaleTensor` sono `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="cd554-121">The expected dimensions of the `InputScaleTensor` are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="cd554-122">Questo valore di scala viene utilizzato per dequantizzare i valori di input.</span><span class="sxs-lookup"><span data-stu-id="cd554-122">This scale value is used for dequantizing the input values.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="cd554-123">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd554-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd554-124">Un tensore facoltativo contenente i dati del punto zero di input.</span><span class="sxs-lookup"><span data-stu-id="cd554-124">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="cd554-125">Le dimensioni previste di *InputZeroPointTensor* sono `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="cd554-125">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="cd554-126">Questo valore del punto zero viene usato per la dequantizzazione dei valori di input.</span><span class="sxs-lookup"><span data-stu-id="cd554-126">This zero point value is used for dequantizing the input values.</span></span>


`FilterTensor`

<span data-ttu-id="cd554-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd554-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd554-128">Un tensore contenente i dati del filtro.</span><span class="sxs-lookup"><span data-stu-id="cd554-128">A tensor containing the filter data.</span></span> <span data-ttu-id="cd554-129">Le dimensioni previste di *FilterTensor* sono `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="cd554-129">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterScaleTensor`

<span data-ttu-id="cd554-130">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd554-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd554-131">Un tensore contenente i dati sulla scala del filtro.</span><span class="sxs-lookup"><span data-stu-id="cd554-131">A tensor containing the filter scale data.</span></span> <span data-ttu-id="cd554-132">Le dimensioni previste di `FilterScaleTensor` sono `{ 1, 1, 1, 1 }` se la quantizzazione del tensore è obbligatoria o `{ 1, OutputChannelCount, 1, 1 }` se è richiesta la quantizzazione per canale.</span><span class="sxs-lookup"><span data-stu-id="cd554-132">The expected dimensions of the `FilterScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="cd554-133">Questo valore di scala viene utilizzato per dequantizzare i valori di filtro.</span><span class="sxs-lookup"><span data-stu-id="cd554-133">This scale value is used for dequantizing the filter values.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="cd554-134">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd554-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd554-135">Un tensore facoltativo contenente i dati del punto zero del filtro.</span><span class="sxs-lookup"><span data-stu-id="cd554-135">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="cd554-136">Le dimensioni previste di *FilterZeroPointTensor* sono `{ 1, 1, 1, 1 }` se è richiesta la quantizzazione del tensore o `{ 1, OutputChannelCount, 1, 1 }` se è necessaria la quantizzazione per canale.</span><span class="sxs-lookup"><span data-stu-id="cd554-136">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="cd554-137">Questo valore del punto zero viene usato per la dequantizzazione dei valori di filtro.</span><span class="sxs-lookup"><span data-stu-id="cd554-137">This zero point value is used for dequantizing the filter values.</span></span>


`BiasTensor`

<span data-ttu-id="cd554-138">Tipo: \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd554-138">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd554-139">Un tensore contenente i dati di distorsione.</span><span class="sxs-lookup"><span data-stu-id="cd554-139">A tensor containing the bias data.</span></span> <span data-ttu-id="cd554-140">Il tensore di distorsione è un tensore che contiene dati trasmessi attraverso il tensore di output alla fine della convoluzione che viene aggiunta al risultato.</span><span class="sxs-lookup"><span data-stu-id="cd554-140">The bias tensor is a tensor containing data which is broadcasted across the output tensor at the end of the convolution which is added to the result.</span></span> <span data-ttu-id="cd554-141">Le dimensioni previste di BiasTensor sono `{ 1, OutputChannelCount, 1, 1 }` per 4D.</span><span class="sxs-lookup"><span data-stu-id="cd554-141">The expected dimensions of the BiasTensor are `{ 1, OutputChannelCount, 1, 1 }` for 4D.</span></span>


`OutputScaleTensor`

<span data-ttu-id="cd554-142">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd554-142">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd554-143">Un tensore contenente i dati della scala di output.</span><span class="sxs-lookup"><span data-stu-id="cd554-143">A tensor containing the output scale data.</span></span> <span data-ttu-id="cd554-144">Le dimensioni previste di OutputScaleTensor sono `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="cd554-144">The expected dimensions of the OutputScaleTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="cd554-145">Questo valore di scala di input viene usato per quantizzare i valori di output della convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd554-145">This input scale value is used for quantizing the convolution output values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="cd554-146">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd554-146">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd554-147">Un tensore facoltativo contenente i dati del punto zero del filtro.</span><span class="sxs-lookup"><span data-stu-id="cd554-147">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="cd554-148">Le dimensioni previste di OutputZeroPointTensor sono `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="cd554-148">The expected dimensions of the OutputZeroPointTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="cd554-149">Questo valore del punto zero di input viene usato per quantizzare i valori di output.</span><span class="sxs-lookup"><span data-stu-id="cd554-149">This input zero point value is used for quantizing the convolution the output values.</span></span>


`OutputTensor`

<span data-ttu-id="cd554-150">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd554-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd554-151">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="cd554-151">A tensor to write the results to.</span></span> <span data-ttu-id="cd554-152">Le dimensioni previste di OutputTensor sono `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="cd554-152">The expected dimensions of the OutputTensor are `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="cd554-153">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="cd554-153">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="cd554-154">Numero di dimensioni spaziali per l'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd554-154">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="cd554-155">Le dimensioni spaziali sono le dimensioni inferiori del tensore del filtro di convoluzione *FilterTensor*.</span><span class="sxs-lookup"><span data-stu-id="cd554-155">Spatial dimensions are the lower dimensions of the convolution filter tensor *FilterTensor*.</span></span> <span data-ttu-id="cd554-156">Questo valore determina anche le dimensioni delle matrici *Strides*, *dilatations*, *StartPadding* e *EndPadding* .</span><span class="sxs-lookup"><span data-stu-id="cd554-156">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="cd554-157">È supportato solo il valore 2.</span><span class="sxs-lookup"><span data-stu-id="cd554-157">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="cd554-158">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="cd554-158">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="cd554-159">Stride dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd554-159">The strides of the convolution operation.</span></span> <span data-ttu-id="cd554-160">Questi stride vengono applicati al filtro di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd554-160">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="cd554-161">Sono separate dagli stride di tensori inclusi nel [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="cd554-161">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="cd554-162">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="cd554-162">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="cd554-163">Dilatazioni dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd554-163">The Dilations of the convolution operation.</span></span> <span data-ttu-id="cd554-164">Le dilatazioni sono gli stride applicati agli elementi del kernel del filtro.</span><span class="sxs-lookup"><span data-stu-id="cd554-164">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="cd554-165">Questo ha l'effetto di simulare un kernel di filtro di dimensioni maggiori riempiendo gli elementi del kernel di filtro interni con zeri.</span><span class="sxs-lookup"><span data-stu-id="cd554-165">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="cd554-166">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="cd554-166">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="cd554-167">Valori di riempimento da applicare all'inizio di ogni dimensione spaziale del filtro e del tensore di input dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd554-167">The padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="cd554-168">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="cd554-168">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="cd554-169">Valori di riempimento da applicare alla fine di ogni dimensione spaziale del filtro e del tensore di input dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd554-169">The padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="cd554-170">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="cd554-170">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="cd554-171">Numero di gruppi in cui dividere l'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="cd554-171">The number of groups which to divide the convolution operation into.</span></span> <span data-ttu-id="cd554-172">*GroupCount* può essere usato per ottenere una convoluzione a livello di profondità impostando *GroupCount* uguale al numero di canali di input.</span><span class="sxs-lookup"><span data-stu-id="cd554-172">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="cd554-173">Questa operazione divide la convoluzione in una convoluzione separata per ogni canale di input.</span><span class="sxs-lookup"><span data-stu-id="cd554-173">This divides the convolution up into a separate convolution per input channel.</span></span> 

## <a name="availability"></a><span data-ttu-id="cd554-174">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="cd554-174">Availability</span></span>
<span data-ttu-id="cd554-175">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="cd554-175">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="cd554-176">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="cd554-176">Tensor constraints</span></span>
* <span data-ttu-id="cd554-177">*FilterTensor* e *FilterZeroPointTensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="cd554-177">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="cd554-178">*InputTensor* e *InputZeroPointTensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="cd554-178">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="cd554-179">*OutputTensor* e `OutputZeroPointTensor` devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="cd554-179">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="cd554-180">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="cd554-180">Tensor support</span></span>
| <span data-ttu-id="cd554-181">Tensore</span><span class="sxs-lookup"><span data-stu-id="cd554-181">Tensor</span></span> | <span data-ttu-id="cd554-182">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd554-182">Kind</span></span> | <span data-ttu-id="cd554-183">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="cd554-183">Supported dimension counts</span></span> | <span data-ttu-id="cd554-184">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="cd554-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="cd554-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="cd554-185">InputTensor</span></span> | <span data-ttu-id="cd554-186">Input</span><span class="sxs-lookup"><span data-stu-id="cd554-186">Input</span></span> | <span data-ttu-id="cd554-187">4</span><span class="sxs-lookup"><span data-stu-id="cd554-187">4</span></span> | <span data-ttu-id="cd554-188">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cd554-188">INT8, UINT8</span></span> |
| <span data-ttu-id="cd554-189">InputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cd554-189">InputScaleTensor</span></span> | <span data-ttu-id="cd554-190">Input</span><span class="sxs-lookup"><span data-stu-id="cd554-190">Input</span></span> | <span data-ttu-id="cd554-191">4</span><span class="sxs-lookup"><span data-stu-id="cd554-191">4</span></span> | <span data-ttu-id="cd554-192">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="cd554-192">FLOAT32</span></span> |
| <span data-ttu-id="cd554-193">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="cd554-193">InputZeroPointTensor</span></span> | <span data-ttu-id="cd554-194">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="cd554-194">Optional input</span></span> | <span data-ttu-id="cd554-195">4</span><span class="sxs-lookup"><span data-stu-id="cd554-195">4</span></span> | <span data-ttu-id="cd554-196">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cd554-196">INT8, UINT8</span></span> |
| <span data-ttu-id="cd554-197">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="cd554-197">FilterTensor</span></span> | <span data-ttu-id="cd554-198">Input</span><span class="sxs-lookup"><span data-stu-id="cd554-198">Input</span></span> | <span data-ttu-id="cd554-199">4</span><span class="sxs-lookup"><span data-stu-id="cd554-199">4</span></span> | <span data-ttu-id="cd554-200">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cd554-200">INT8, UINT8</span></span> |
| <span data-ttu-id="cd554-201">FilterScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cd554-201">FilterScaleTensor</span></span> | <span data-ttu-id="cd554-202">Input</span><span class="sxs-lookup"><span data-stu-id="cd554-202">Input</span></span> | <span data-ttu-id="cd554-203">4</span><span class="sxs-lookup"><span data-stu-id="cd554-203">4</span></span> | <span data-ttu-id="cd554-204">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="cd554-204">FLOAT32</span></span> |
| <span data-ttu-id="cd554-205">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="cd554-205">FilterZeroPointTensor</span></span> | <span data-ttu-id="cd554-206">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="cd554-206">Optional input</span></span> | <span data-ttu-id="cd554-207">4</span><span class="sxs-lookup"><span data-stu-id="cd554-207">4</span></span> | <span data-ttu-id="cd554-208">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cd554-208">INT8, UINT8</span></span> |
| <span data-ttu-id="cd554-209">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="cd554-209">BiasTensor</span></span> | <span data-ttu-id="cd554-210">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="cd554-210">Optional input</span></span> | <span data-ttu-id="cd554-211">4</span><span class="sxs-lookup"><span data-stu-id="cd554-211">4</span></span> | <span data-ttu-id="cd554-212">INT32</span><span class="sxs-lookup"><span data-stu-id="cd554-212">INT32</span></span> |
| <span data-ttu-id="cd554-213">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cd554-213">OutputScaleTensor</span></span> | <span data-ttu-id="cd554-214">Input</span><span class="sxs-lookup"><span data-stu-id="cd554-214">Input</span></span> | <span data-ttu-id="cd554-215">4</span><span class="sxs-lookup"><span data-stu-id="cd554-215">4</span></span> | <span data-ttu-id="cd554-216">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="cd554-216">FLOAT32</span></span> |
| <span data-ttu-id="cd554-217">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="cd554-217">OutputZeroPointTensor</span></span> | <span data-ttu-id="cd554-218">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="cd554-218">Optional input</span></span> | <span data-ttu-id="cd554-219">4</span><span class="sxs-lookup"><span data-stu-id="cd554-219">4</span></span> | <span data-ttu-id="cd554-220">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cd554-220">INT8, UINT8</span></span> |
| <span data-ttu-id="cd554-221">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="cd554-221">OutputTensor</span></span> | <span data-ttu-id="cd554-222">Output</span><span class="sxs-lookup"><span data-stu-id="cd554-222">Output</span></span> | <span data-ttu-id="cd554-223">4</span><span class="sxs-lookup"><span data-stu-id="cd554-223">4</span></span> | <span data-ttu-id="cd554-224">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cd554-224">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="cd554-225">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd554-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cd554-226">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="cd554-226">**Header**</span></span> | <span data-ttu-id="cd554-227">directml. h</span><span class="sxs-lookup"><span data-stu-id="cd554-227">directml.h</span></span> |