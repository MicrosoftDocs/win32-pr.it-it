---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Esegue un'operazione di allineamento del ROI, come descritto nel [documento Mask R-CNN](https://arxiv.org/abs/1703.06870). In breve, l'operazione estrae le colture dal tensore dell'immagine di input e le ridimensiona a una dimensione di output comune specificata dalle ultime 2 dimensioni di *OutputTensor* usando il *InterpolationMode* specificato.
helpviewer_keywords:
- DML_ROI_ALIGN_OPERATOR_DESC
- DML_ROI_ALIGN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ROI_ALIGN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ROI_ALIGN_OPERATOR_DESC, DML_ROI_ALIGN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
- directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
ms.openlocfilehash: 987aef7d7002892b8af3167fb8da2b74dc80a12e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320330"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a><span data-ttu-id="5e6ef-104">Struttura DML_ROI_ALIGN_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="5e6ef-104">DML_ROI_ALIGN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="5e6ef-105">Esegue un'operazione di allineamento del ROI, come descritto nel [documento Mask R-CNN](https://arxiv.org/abs/1703.06870).</span><span class="sxs-lookup"><span data-stu-id="5e6ef-105">Performs an ROI Align operation, as described in the [Mask R-CNN paper](https://arxiv.org/abs/1703.06870).</span></span> <span data-ttu-id="5e6ef-106">In breve, l'operazione estrae le colture dal tensore dell'immagine di input e le ridimensiona a una dimensione di output comune specificata dalle ultime 2 dimensioni di *OutputTensor* usando il *InterpolationMode* specificato.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-106">In summary, the operation extracts crops from the input image tensor and resizes them to a common output size specified by the last 2 dimensions of *OutputTensor* using the specified *InterpolationMode*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e6ef-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="5e6ef-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="5e6ef-108">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="5e6ef-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e6ef-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e6ef-109">Syntax</span></span>

```cpp
struct DML_ROI_ALIGN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* ROITensor;
  const DML_TENSOR_DESC* BatchIndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  DML_REDUCE_FUNCTION ReductionFunction;
  DML_INTERPOLATION_MODE InterpolationMode;
  FLOAT SpatialScaleX;
  FLOAT SpatialScaleY;
  FLOAT OutOfBoundsInputValue;
  UINT MinimumSamplesPerOutput;
  UINT MaximumSamplesPerOutput;
};
```

## <a name="members"></a><span data-ttu-id="5e6ef-110">Members</span><span class="sxs-lookup"><span data-stu-id="5e6ef-110">Members</span></span>

`InputTensor`

<span data-ttu-id="5e6ef-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5e6ef-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5e6ef-112">Un tensore contenente i dati di input con dimensioni `{ BatchCount, ChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="5e6ef-112">A tensor containing the input data with dimensions `{ BatchCount, ChannelCount, InputHeight, InputWidth }`.</span></span>

`ROITensor`

<span data-ttu-id="5e6ef-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5e6ef-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5e6ef-114">Un tensore contenente le aree di interesse (ROI) dati.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-114">A tensor containing the regions of interest (ROI) data.</span></span> <span data-ttu-id="5e6ef-115">Le dimensioni consentite di `ROITensor` sono `{ NumROIs, 4 }` , `{ 1, NumROIs, 4 }` o `{ 1, 1, NumROIs, 4 }` .</span><span class="sxs-lookup"><span data-stu-id="5e6ef-115">The allowed dimensions of `ROITensor` are `{ NumROIs, 4 }`, `{ 1, NumROIs, 4 }`, or `{ 1, 1, NumROIs, 4 }`.</span></span> <span data-ttu-id="5e6ef-116">Per ogni ROI, i valori saranno le coordinate degli angoli superiore sinistro e inferiore destro nell'ordine `[x1, y1, x2, y2]` .</span><span class="sxs-lookup"><span data-stu-id="5e6ef-116">For each ROI, the values will be the coordinates of its top-left and bottom-right corners in the order `[x1, y1, x2, y2]`.</span></span>

`BatchIndicesTensor`

<span data-ttu-id="5e6ef-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5e6ef-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5e6ef-118">Un tensore contenente gli indici di batch per estrarre il ROIs da.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-118">A tensor containing the batch indices to extract the ROIs from.</span></span> <span data-ttu-id="5e6ef-119">Le dimensioni consentite di `BatchIndicesTensor` sono `{ NumROIs }` , `{ 1, NumROIs }` , `{ 1, 1, NumROIs }` o `{ 1, 1, 1, NumROIs }` .</span><span class="sxs-lookup"><span data-stu-id="5e6ef-119">The allowed dimensions of `BatchIndicesTensor` are `{ NumROIs }`, `{ 1, NumROIs }`, `{ 1, 1, NumROIs }`, or `{ 1, 1, 1, NumROIs }`.</span></span> <span data-ttu-id="5e6ef-120">Ogni valore è l'indice di un batch da *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-120">Each value is the index of a batch from *InputTensor*.</span></span> <span data-ttu-id="5e6ef-121">Il comportamento non è definito se i valori non sono compresi nell'intervallo [0, BatchCount).</span><span class="sxs-lookup"><span data-stu-id="5e6ef-121">The behavior is undefined if the values are not in the range [0, BatchCount).</span></span>

`OutputTensor`

<span data-ttu-id="5e6ef-122">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5e6ef-122">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5e6ef-123">Un tensore contenente i dati di output.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-123">A tensor containing the output data.</span></span> <span data-ttu-id="5e6ef-124">Le dimensioni previste di *OutputTensor* sono `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="5e6ef-124">The expected dimensions of *OutputTensor* are `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }`.</span></span>

`ReductionFunction`

<span data-ttu-id="5e6ef-125">Tipo: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span><span class="sxs-lookup"><span data-stu-id="5e6ef-125">Type: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span></span>

<span data-ttu-id="5e6ef-126">Funzione di riduzione da usare quando si riducono tutti gli esempi di input che contribuiscono a un elemento di output ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) o **DML_REDUCE_FUNCTION_MAX**).</span><span class="sxs-lookup"><span data-stu-id="5e6ef-126">The reduction function to use when reducing across all input samples that contribute to an output element ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) or **DML_REDUCE_FUNCTION_MAX**).</span></span> <span data-ttu-id="5e6ef-127">Il numero di campioni di input da ridurre in è limitato da *MinimumSamplesPerOutput* e *MaximumSamplesPerOutput*.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-127">The number of input samples to reduce across is bounded by *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`InterpolationMode`

<span data-ttu-id="5e6ef-128">Tipo: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span><span class="sxs-lookup"><span data-stu-id="5e6ef-128">Type: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span></span>

<span data-ttu-id="5e6ef-129">Modalità di interpolazione da utilizzare quando si ridimensionano le aree.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-129">The interpolation mode to use when resizing the regions.</span></span>

- <span data-ttu-id="5e6ef-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span><span class="sxs-lookup"><span data-stu-id="5e6ef-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span></span> <span data-ttu-id="5e6ef-131">Usa l'algoritmo *adiacente più vicino* , che sceglie l'elemento di input più vicino al centro pixel corrispondente per ogni elemento di output.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-131">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>
- <span data-ttu-id="5e6ef-132">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-132">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="5e6ef-133">Usa l'algoritmo *bilineare* , che calcola l'elemento output eseguendo la media ponderata dei 2 elementi di input adiacenti più vicini per ogni dimensione.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-133">Uses the *Bilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="5e6ef-134">Poiché vengono ridimensionate solo 2 dimensioni, la media ponderata viene calcolata su un totale di 4 elementi di input per ogni elemento di output.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-134">Since only 2 dimensions are resized, the weighted average is computed on a total of 4 input elements for each output element.</span></span>

`SpatialScaleX`

<span data-ttu-id="5e6ef-135">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="5e6ef-135">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="5e6ef-136">Componente X (o larghezza) del fattore di scala per moltiplicare le coordinate *ROITensor* per renderle proporzionali a *InputHeight* e *InputWidth*.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-136">The X (or width) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="5e6ef-137">Se, ad esempio, *ROITensor* contiene Coordinate normalizzate (valori compresi nell'intervallo [0.. 1]), *SpatialScaleX* di solito avrà lo stesso valore di *InputWidth*.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-137">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), then *SpatialScaleX* would usually have the same value as *InputWidth*.</span></span>

`SpatialScaleY`

<span data-ttu-id="5e6ef-138">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="5e6ef-138">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="5e6ef-139">Componente Y (o altezza) del fattore di scala per moltiplicare le coordinate *ROITensor* per renderle proporzionali a *InputHeight* e *InputWidth*.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-139">The Y (or height) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="5e6ef-140">Se, ad esempio, *ROITensor* contiene Coordinate normalizzate (valori compresi nell'intervallo [0.. 1]), *SpatialScaleY* genererà lo stesso valore di *InputHeight*.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-140">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), *SpatialScaleY* would usually have the same value as *InputHeight*.</span></span>

`OutOfBoundsInputValue`

<span data-ttu-id="5e6ef-141">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="5e6ef-141">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="5e6ef-142">Valore da leggere da *InputTensor* quando l'oggetto Rois è esterno ai limiti di *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-142">The value to read from *InputTensor* when the ROIs are outside the bounds of *InputTensor*.</span></span> <span data-ttu-id="5e6ef-143">Questo problema può verificarsi quando i valori ottenuti dopo la scalabilità di *ROITensor* da *SpatialScaleX* e *SpatialScaleY* sono maggiori di *InputWidth* e *InputHeight*.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-143">This can happen when the values obtained after scaling *ROITensor* by *SpatialScaleX* and *SpatialScaleY* are bigger than *InputWidth* and *InputHeight*.</span></span>

`MinimumSamplesPerOutput`

<span data-ttu-id="5e6ef-144">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="5e6ef-144">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="5e6ef-145">Numero minimo di campioni di input da utilizzare per ogni elemento di output.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-145">The minimum number of input samples to use for every output element.</span></span> <span data-ttu-id="5e6ef-146">L'operatore calcolerà il numero di campioni di input eseguendo `ScaledCropSize / OutputSize` , quindi lo clamperà su *MinimumSamplesPerOutput* e *MaximumSamplesPerOutput*.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-146">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`MaximumSamplesPerOutput`

<span data-ttu-id="5e6ef-147">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="5e6ef-147">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="5e6ef-148">Numero massimo di campioni di input da utilizzare per ogni elemento di output.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-148">The maximum number of input samples to use for every output element.</span></span> <span data-ttu-id="5e6ef-149">L'operatore calcolerà il numero di campioni di input eseguendo `ScaledCropSize / OutputSize` , quindi lo clamperà su *MinimumSamplesPerOutput* e *MaximumSamplesPerOutput*.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-149">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

## <a name="availability"></a><span data-ttu-id="5e6ef-150">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="5e6ef-150">Availability</span></span>
<span data-ttu-id="5e6ef-151">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="5e6ef-151">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5e6ef-152">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="5e6ef-152">Tensor constraints</span></span>
<span data-ttu-id="5e6ef-153">*InputTensor*, *OutputTensor* e *ROITensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="5e6ef-153">*InputTensor*, *OutputTensor*, and *ROITensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5e6ef-154">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="5e6ef-154">Tensor support</span></span>
| <span data-ttu-id="5e6ef-155">Tensore</span><span class="sxs-lookup"><span data-stu-id="5e6ef-155">Tensor</span></span> | <span data-ttu-id="5e6ef-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="5e6ef-156">Kind</span></span> | <span data-ttu-id="5e6ef-157">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="5e6ef-157">Supported dimension counts</span></span> | <span data-ttu-id="5e6ef-158">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="5e6ef-158">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5e6ef-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5e6ef-159">InputTensor</span></span> | <span data-ttu-id="5e6ef-160">Input</span><span class="sxs-lookup"><span data-stu-id="5e6ef-160">Input</span></span> | <span data-ttu-id="5e6ef-161">4</span><span class="sxs-lookup"><span data-stu-id="5e6ef-161">4</span></span> | <span data-ttu-id="5e6ef-162">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5e6ef-162">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5e6ef-163">ROITensor</span><span class="sxs-lookup"><span data-stu-id="5e6ef-163">ROITensor</span></span> | <span data-ttu-id="5e6ef-164">Input</span><span class="sxs-lookup"><span data-stu-id="5e6ef-164">Input</span></span> | <span data-ttu-id="5e6ef-165">da 2 a 4</span><span class="sxs-lookup"><span data-stu-id="5e6ef-165">2 to 4</span></span> | <span data-ttu-id="5e6ef-166">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5e6ef-166">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5e6ef-167">BatchIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="5e6ef-167">BatchIndicesTensor</span></span> | <span data-ttu-id="5e6ef-168">Input</span><span class="sxs-lookup"><span data-stu-id="5e6ef-168">Input</span></span> | <span data-ttu-id="5e6ef-169">da 1 a 4</span><span class="sxs-lookup"><span data-stu-id="5e6ef-169">1 to 4</span></span> | <span data-ttu-id="5e6ef-170">UINT32</span><span class="sxs-lookup"><span data-stu-id="5e6ef-170">UINT32</span></span> |
| <span data-ttu-id="5e6ef-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5e6ef-171">OutputTensor</span></span> | <span data-ttu-id="5e6ef-172">Output</span><span class="sxs-lookup"><span data-stu-id="5e6ef-172">Output</span></span> | <span data-ttu-id="5e6ef-173">4</span><span class="sxs-lookup"><span data-stu-id="5e6ef-173">4</span></span> | <span data-ttu-id="5e6ef-174">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5e6ef-174">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="5e6ef-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e6ef-175">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5e6ef-176">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="5e6ef-176">**Header**</span></span> | <span data-ttu-id="5e6ef-177">directml. h</span><span class="sxs-lookup"><span data-stu-id="5e6ef-177">directml.h</span></span> |