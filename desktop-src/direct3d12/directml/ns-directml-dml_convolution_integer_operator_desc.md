---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Esegue una convoluzione di *FilterTensor* con *InputTensor*. Questo operatore esegue la convoluzione in avanti su dati Integer.
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
ms.openlocfilehash: c16690ea1e3049ffeba398bbbaca2003f965a832
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320381"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="4966c-104">Struttura DML_CONVOLUTION_INTEGER_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="4966c-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="4966c-105">Esegue una convoluzione di *FilterTensor* con *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="4966c-105">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="4966c-106">Questo operatore esegue la convoluzione in avanti su dati Integer.</span><span class="sxs-lookup"><span data-stu-id="4966c-106">This operator performs forward convolution on integer data.</span></span> <span data-ttu-id="4966c-107">I tensori di punti zero facoltativi possono essere usati anche per sottrarre i valori del punto zero dal tensore di input e filtro.</span><span class="sxs-lookup"><span data-stu-id="4966c-107">Optional zero point tensors can also be used to subtract zero point values from the input and filter tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4966c-108">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="4966c-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="4966c-109">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="4966c-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4966c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4966c-110">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="4966c-111">Members</span><span class="sxs-lookup"><span data-stu-id="4966c-111">Members</span></span>

`InputTensor`

<span data-ttu-id="4966c-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4966c-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4966c-113">Un tensore contenente i dati di input.</span><span class="sxs-lookup"><span data-stu-id="4966c-113">A tensor containing the input data.</span></span> <span data-ttu-id="4966c-114">Le dimensioni previste di *InputTensor* sono `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="4966c-114">The expected dimensions of the *InputTensor* are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="4966c-115">Tipo: \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4966c-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4966c-116">Un tensore facoltativo contenente i dati del punto zero di input.</span><span class="sxs-lookup"><span data-stu-id="4966c-116">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="4966c-117">Le dimensioni previste di *InputZeroPointTensor* sono `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="4966c-117">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span>


`FilterTensor`

<span data-ttu-id="4966c-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4966c-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4966c-119">Un tensore contenente i dati del filtro.</span><span class="sxs-lookup"><span data-stu-id="4966c-119">A tensor containing the filter data.</span></span> <span data-ttu-id="4966c-120">Le dimensioni previste di *FilterTensor* sono `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="4966c-120">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="4966c-121">Tipo: \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4966c-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4966c-122">Un tensore facoltativo contenente i dati del punto zero del filtro.</span><span class="sxs-lookup"><span data-stu-id="4966c-122">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="4966c-123">Le dimensioni previste di *FilterZeroPointTensor* sono `{ 1, 1, 1, 1 }` se è necessaria la quantizzazione del tensore o `{ 1, OutputChannelCount, 1, 1 }` se è richiesta la quantizzazione per canale.</span><span class="sxs-lookup"><span data-stu-id="4966c-123">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per-channel quantization is required.</span></span>


`OutputTensor`

<span data-ttu-id="4966c-124">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4966c-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4966c-125">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="4966c-125">The tensor to write the results to.</span></span> <span data-ttu-id="4966c-126">Le dimensioni previste di *OutputTensor* sono `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="4966c-126">The expected dimensions of the *OutputTensor* are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="4966c-127">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4966c-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4966c-128">Numero di dimensioni spaziali per l'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="4966c-128">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="4966c-129">Le dimensioni spaziali sono le dimensioni inferiori del *FilterTensor* di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="4966c-129">Spatial dimensions are the lower dimensions of the convolution *FilterTensor*.</span></span> <span data-ttu-id="4966c-130">Questo valore determina anche le dimensioni delle matrici *Strides*, *dilatations*, *StartPadding* e *EndPadding* .</span><span class="sxs-lookup"><span data-stu-id="4966c-130">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="4966c-131">È supportato solo il valore 2.</span><span class="sxs-lookup"><span data-stu-id="4966c-131">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="4966c-132">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="4966c-132">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="4966c-133">Matrice contenente gli stride dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="4966c-133">An array containing the strides of the convolution operation.</span></span> <span data-ttu-id="4966c-134">Questi stride vengono applicati al filtro di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="4966c-134">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="4966c-135">Sono separate dagli stride di tensori inclusi nel [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="4966c-135">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="4966c-136">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="4966c-136">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="4966c-137">Matrice contenente le dilatazioni dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="4966c-137">An array containing the dilations of the convolution operation.</span></span> <span data-ttu-id="4966c-138">Le dilatazioni sono gli stride applicati agli elementi del kernel del filtro.</span><span class="sxs-lookup"><span data-stu-id="4966c-138">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="4966c-139">Questo ha l'effetto di simulare un kernel di filtro di dimensioni maggiori riempiendo gli elementi del kernel di filtro interni con zeri.</span><span class="sxs-lookup"><span data-stu-id="4966c-139">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="4966c-140">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="4966c-140">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="4966c-141">Matrice contenente i valori di spaziatura interna da applicare all'inizio di ogni dimensione spaziale del filtro e del tensore di input dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="4966c-141">An array containing the padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="4966c-142">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="4966c-142">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="4966c-143">Matrice contenente i valori di spaziatura interna da applicare alla fine di ogni dimensione spaziale del filtro e del tensore di input dell'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="4966c-143">An array containing the padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="4966c-144">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4966c-144">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4966c-145">Numero di gruppi in cui dividere l'operazione di convoluzione.</span><span class="sxs-lookup"><span data-stu-id="4966c-145">The number of groups which to divide the convolution operation up into.</span></span> <span data-ttu-id="4966c-146">*GroupCount* può essere usato per ottenere una convoluzione a livello di profondità impostando *GroupCount* uguale al numero di canali di input.</span><span class="sxs-lookup"><span data-stu-id="4966c-146">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="4966c-147">Questa operazione divide la convoluzione in una convoluzione separata per ogni canale di input.</span><span class="sxs-lookup"><span data-stu-id="4966c-147">This divides the convolution up into a separate convolution per input channel.</span></span>

## <a name="availability"></a><span data-ttu-id="4966c-148">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="4966c-148">Availability</span></span>
<span data-ttu-id="4966c-149">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="4966c-149">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="4966c-150">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="4966c-150">Tensor constraints</span></span>
* <span data-ttu-id="4966c-151">*FilterTensor* e *FilterZeroPointTensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="4966c-151">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="4966c-152">*InputTensor* e *InputZeroPointTensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="4966c-152">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="4966c-153">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="4966c-153">Tensor support</span></span>
| <span data-ttu-id="4966c-154">Tensore</span><span class="sxs-lookup"><span data-stu-id="4966c-154">Tensor</span></span> | <span data-ttu-id="4966c-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="4966c-155">Kind</span></span> | <span data-ttu-id="4966c-156">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="4966c-156">Dimensions</span></span> | <span data-ttu-id="4966c-157">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="4966c-157">Supported dimension counts</span></span> | <span data-ttu-id="4966c-158">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="4966c-158">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="4966c-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="4966c-159">InputTensor</span></span> | <span data-ttu-id="4966c-160">Input</span><span class="sxs-lookup"><span data-stu-id="4966c-160">Input</span></span> | <span data-ttu-id="4966c-161">{BatchCount, InputChannelCount, InputHeight, InputWidth}</span><span class="sxs-lookup"><span data-stu-id="4966c-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="4966c-162">4</span><span class="sxs-lookup"><span data-stu-id="4966c-162">4</span></span> | <span data-ttu-id="4966c-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="4966c-163">INT8, UINT8</span></span> |
| <span data-ttu-id="4966c-164">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="4966c-164">InputZeroPointTensor</span></span> | <span data-ttu-id="4966c-165">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="4966c-165">Optional input</span></span> | <span data-ttu-id="4966c-166">{1, 1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="4966c-166">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="4966c-167">4</span><span class="sxs-lookup"><span data-stu-id="4966c-167">4</span></span> | <span data-ttu-id="4966c-168">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="4966c-168">INT8, UINT8</span></span> |
| <span data-ttu-id="4966c-169">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="4966c-169">FilterTensor</span></span> | <span data-ttu-id="4966c-170">Input</span><span class="sxs-lookup"><span data-stu-id="4966c-170">Input</span></span> | <span data-ttu-id="4966c-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span><span class="sxs-lookup"><span data-stu-id="4966c-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span></span> | <span data-ttu-id="4966c-172">4</span><span class="sxs-lookup"><span data-stu-id="4966c-172">4</span></span> | <span data-ttu-id="4966c-173">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="4966c-173">INT8, UINT8</span></span> |
| <span data-ttu-id="4966c-174">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="4966c-174">FilterZeroPointTensor</span></span> | <span data-ttu-id="4966c-175">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="4966c-175">Optional input</span></span> | <span data-ttu-id="4966c-176">{1, FilterZeroPointChannelCount, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="4966c-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span></span> | <span data-ttu-id="4966c-177">4</span><span class="sxs-lookup"><span data-stu-id="4966c-177">4</span></span> | <span data-ttu-id="4966c-178">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="4966c-178">INT8, UINT8</span></span> |
| <span data-ttu-id="4966c-179">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="4966c-179">OutputTensor</span></span> | <span data-ttu-id="4966c-180">Output</span><span class="sxs-lookup"><span data-stu-id="4966c-180">Output</span></span> | <span data-ttu-id="4966c-181">{BatchCount, OutputChannelCount, OutputHeight, OutputWidth}</span><span class="sxs-lookup"><span data-stu-id="4966c-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="4966c-182">4</span><span class="sxs-lookup"><span data-stu-id="4966c-182">4</span></span> | <span data-ttu-id="4966c-183">INT32</span><span class="sxs-lookup"><span data-stu-id="4966c-183">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="4966c-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4966c-184">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4966c-185">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="4966c-185">**Header**</span></span> | <span data-ttu-id="4966c-186">directml. h</span><span class="sxs-lookup"><span data-stu-id="4966c-186">directml.h</span></span> |