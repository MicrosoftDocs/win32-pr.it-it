---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Esegue una convoluzione di *FilterTensor* con *InputTensor.* Questo operatore esegue la convoluzione in avanti sui dati integer.
helpviewer_keywords:
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CONVOLUTION_INTEGER_OPERATOR_DESC, DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f4045598dd1aa050479fec8e5732fe5c0a4e77ee
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550417"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="f7cee-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="f7cee-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="f7cee-105">Esegue una convoluzione di *FilterTensor* con *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="f7cee-105">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="f7cee-106">Questo operatore esegue la convoluzione in avanti sui dati integer.</span><span class="sxs-lookup"><span data-stu-id="f7cee-106">This operator performs forward convolution on integer data.</span></span> <span data-ttu-id="f7cee-107">I tensori zero point facoltativi possono essere usati anche per sottrarre valori di zero punti dal tensore di input e filtro.</span><span class="sxs-lookup"><span data-stu-id="f7cee-107">Optional zero point tensors can also be used to subtract zero point values from the input and filter tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7cee-108">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="f7cee-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f7cee-109">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="f7cee-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7cee-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7cee-110">Syntax</span></span>
```cpp
struct DML_CONVOLUTION_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```

## <a name="members"></a><span data-ttu-id="f7cee-111">Members</span><span class="sxs-lookup"><span data-stu-id="f7cee-111">Members</span></span>

`InputTensor`

<span data-ttu-id="f7cee-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f7cee-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f7cee-113">Tensore contenente i dati di input.</span><span class="sxs-lookup"><span data-stu-id="f7cee-113">A tensor containing the input data.</span></span> <span data-ttu-id="f7cee-114">Le dimensioni previste di *InputTensor* sono `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="f7cee-114">The expected dimensions of the *InputTensor* are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="f7cee-115">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f7cee-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f7cee-116">Tensore facoltativo contenente i dati del punto zero di input.</span><span class="sxs-lookup"><span data-stu-id="f7cee-116">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="f7cee-117">Le dimensioni previste di *InputZeroPointTensor* sono `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="f7cee-117">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span>


`FilterTensor`

<span data-ttu-id="f7cee-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f7cee-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f7cee-119">Tensore contenente i dati del filtro.</span><span class="sxs-lookup"><span data-stu-id="f7cee-119">A tensor containing the filter data.</span></span> <span data-ttu-id="f7cee-120">Le dimensioni previste di *FilterTensor* sono `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="f7cee-120">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="f7cee-121">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f7cee-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f7cee-122">Tensore facoltativo contenente i dati del punto zero del filtro.</span><span class="sxs-lookup"><span data-stu-id="f7cee-122">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="f7cee-123">Le dimensioni previste di *FilterZeroPointTensor* sono se è necessaria la quantizzazione per tensore o se è necessaria `{ 1, 1, 1, 1 }` `{ 1, OutputChannelCount, 1, 1 }` la quantizzazione per canale.</span><span class="sxs-lookup"><span data-stu-id="f7cee-123">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per-channel quantization is required.</span></span>


`OutputTensor`

<span data-ttu-id="f7cee-124">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f7cee-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f7cee-125">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="f7cee-125">The tensor to write the results to.</span></span> <span data-ttu-id="f7cee-126">Le dimensioni previste di *OutputTensor* sono `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="f7cee-126">The expected dimensions of the *OutputTensor* are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="f7cee-127">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f7cee-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="f7cee-128">Numero di dimensioni spaziali per l'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="f7cee-128">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="f7cee-129">Le dimensioni spaziali sono le dimensioni inferiori dell'oggetto *FilterTensor* di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="f7cee-129">Spatial dimensions are the lower dimensions of the convolution *FilterTensor*.</span></span> <span data-ttu-id="f7cee-130">Questo valore determina anche le dimensioni delle matrici *Strides,* *Dilations,* *StartPadding* ed *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="f7cee-130">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="f7cee-131">È supportato solo il valore 2.</span><span class="sxs-lookup"><span data-stu-id="f7cee-131">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="f7cee-132">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7cee-132">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f7cee-133">Matrice contenente gli stride dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="f7cee-133">An array containing the strides of the convolution operation.</span></span> <span data-ttu-id="f7cee-134">Questi passi vengono applicati al filtro di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="f7cee-134">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="f7cee-135">Sono separati dai passi del tensore inclusi in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="f7cee-135">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="f7cee-136">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7cee-136">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f7cee-137">Matrice contenente le dilazioni dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="f7cee-137">An array containing the dilations of the convolution operation.</span></span> <span data-ttu-id="f7cee-138">Le dilatazioni sono passi applicati agli elementi del kernel di filtro.</span><span class="sxs-lookup"><span data-stu-id="f7cee-138">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="f7cee-139">Ciò ha l'effetto di simulare un kernel di filtro più grande tramite il riempimento degli elementi del kernel del filtro interno con zeri.</span><span class="sxs-lookup"><span data-stu-id="f7cee-139">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="f7cee-140">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7cee-140">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f7cee-141">Matrice contenente i valori di spaziatura interna da applicare all'inizio di ogni dimensione spaziale del filtro e del tensore di input dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="f7cee-141">An array containing the padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="f7cee-142">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7cee-142">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f7cee-143">Matrice contenente i valori di riempimento da applicare alla fine di ogni dimensione spaziale del filtro e del tensore di input dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="f7cee-143">An array containing the padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="f7cee-144">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f7cee-144">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="f7cee-145">Numero di gruppi in cui dividere l'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="f7cee-145">The number of groups which to divide the convolution operation up into.</span></span> <span data-ttu-id="f7cee-146">*GroupCount* può essere usato per ottenere una convoluzione a livello di profondità impostando *GroupCount* su un valore uguale al numero di canali di input.</span><span class="sxs-lookup"><span data-stu-id="f7cee-146">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="f7cee-147">In questo modo la convoluzione viene suddivisa in una convoluzione separata per canale di input.</span><span class="sxs-lookup"><span data-stu-id="f7cee-147">This divides the convolution up into a separate convolution per input channel.</span></span>

## <a name="availability"></a><span data-ttu-id="f7cee-148">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="f7cee-148">Availability</span></span>
<span data-ttu-id="f7cee-149">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="f7cee-149">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f7cee-150">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="f7cee-150">Tensor constraints</span></span>
* <span data-ttu-id="f7cee-151">*FilterTensor* e *FilterZeroPointTensor* devono avere lo stesso *tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="f7cee-151">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="f7cee-152">*InputTensor* e *InputZeroPointTensor* devono avere lo stesso *tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="f7cee-152">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f7cee-153">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="f7cee-153">Tensor support</span></span>
| <span data-ttu-id="f7cee-154">Tensore</span><span class="sxs-lookup"><span data-stu-id="f7cee-154">Tensor</span></span> | <span data-ttu-id="f7cee-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="f7cee-155">Kind</span></span> | <span data-ttu-id="f7cee-156">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="f7cee-156">Dimensions</span></span> | <span data-ttu-id="f7cee-157">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="f7cee-157">Supported dimension counts</span></span> | <span data-ttu-id="f7cee-158">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="f7cee-158">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="f7cee-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f7cee-159">InputTensor</span></span> | <span data-ttu-id="f7cee-160">Input</span><span class="sxs-lookup"><span data-stu-id="f7cee-160">Input</span></span> | <span data-ttu-id="f7cee-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="f7cee-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="f7cee-162">4</span><span class="sxs-lookup"><span data-stu-id="f7cee-162">4</span></span> | <span data-ttu-id="f7cee-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="f7cee-163">INT8, UINT8</span></span> |
| <span data-ttu-id="f7cee-164">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="f7cee-164">InputZeroPointTensor</span></span> | <span data-ttu-id="f7cee-165">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="f7cee-165">Optional input</span></span> | <span data-ttu-id="f7cee-166">{ 1, 1, 1, 1 }</span><span class="sxs-lookup"><span data-stu-id="f7cee-166">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="f7cee-167">4</span><span class="sxs-lookup"><span data-stu-id="f7cee-167">4</span></span> | <span data-ttu-id="f7cee-168">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="f7cee-168">INT8, UINT8</span></span> |
| <span data-ttu-id="f7cee-169">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="f7cee-169">FilterTensor</span></span> | <span data-ttu-id="f7cee-170">Input</span><span class="sxs-lookup"><span data-stu-id="f7cee-170">Input</span></span> | <span data-ttu-id="f7cee-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span><span class="sxs-lookup"><span data-stu-id="f7cee-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span></span> | <span data-ttu-id="f7cee-172">4</span><span class="sxs-lookup"><span data-stu-id="f7cee-172">4</span></span> | <span data-ttu-id="f7cee-173">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="f7cee-173">INT8, UINT8</span></span> |
| <span data-ttu-id="f7cee-174">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="f7cee-174">FilterZeroPointTensor</span></span> | <span data-ttu-id="f7cee-175">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="f7cee-175">Optional input</span></span> | <span data-ttu-id="f7cee-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span><span class="sxs-lookup"><span data-stu-id="f7cee-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span></span> | <span data-ttu-id="f7cee-177">4</span><span class="sxs-lookup"><span data-stu-id="f7cee-177">4</span></span> | <span data-ttu-id="f7cee-178">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="f7cee-178">INT8, UINT8</span></span> |
| <span data-ttu-id="f7cee-179">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f7cee-179">OutputTensor</span></span> | <span data-ttu-id="f7cee-180">Output</span><span class="sxs-lookup"><span data-stu-id="f7cee-180">Output</span></span> | <span data-ttu-id="f7cee-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="f7cee-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="f7cee-182">4</span><span class="sxs-lookup"><span data-stu-id="f7cee-182">4</span></span> | <span data-ttu-id="f7cee-183">INT32</span><span class="sxs-lookup"><span data-stu-id="f7cee-183">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="f7cee-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7cee-184">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f7cee-185">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="f7cee-185">**Header**</span></span> | <span data-ttu-id="f7cee-186">directml.h</span><span class="sxs-lookup"><span data-stu-id="f7cee-186">directml.h</span></span> |