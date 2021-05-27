---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Ricampiona gli elementi dal tensore di origine al tensore di destinazione, usando i fattori di scala per calcolare le dimensioni del tensore di destinazione. È possibile usare una modalità di interpolazione lineare o più vicina.
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
- DML_RESAMPLE1_OPERATOR_DESC
f1_keywords:
- DML_RESAMPLE1_OPERATOR_DESC
- directml/DML_RESAMPLE1_OPERATOR_DESC
ms.openlocfilehash: 3cf5a49f5c92b835646e146b631abd18b4b19e6b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550396"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a><span data-ttu-id="df9c3-104">DML_RESAMPLE1_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="df9c3-104">DML_RESAMPLE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="df9c3-105">Ricampiona gli elementi dal tensore di origine al tensore di destinazione, usando i fattori di scala per calcolare le dimensioni del tensore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="df9c3-105">Resamples elements from the source to the destination tensor, using the scale factors to compute the destination tensor size.</span></span> <span data-ttu-id="df9c3-106">È possibile usare una modalità di interpolazione lineare o più vicina.</span><span class="sxs-lookup"><span data-stu-id="df9c3-106">You can use a linear or nearest-neighbor interpolation mode.</span></span> <span data-ttu-id="df9c3-107">L'operatore supporta l'interpolazione su più dimensioni, non solo 2D.</span><span class="sxs-lookup"><span data-stu-id="df9c3-107">The operator supports interpolation across multiple dimensions, not just 2D.</span></span> <span data-ttu-id="df9c3-108">È quindi possibile mantenere le stesse dimensioni spaziali, ma interpolare tra i canali o tra batch.</span><span class="sxs-lookup"><span data-stu-id="df9c3-108">So you can keep the same spatial size, but interpolate across channels or across batches.</span></span> <span data-ttu-id="df9c3-109">La relazione tra le coordinate di input e output è la seguente.</span><span class="sxs-lookup"><span data-stu-id="df9c3-109">The relationship between the input and output coordinates is the following.</span></span>

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> <span data-ttu-id="df9c3-110">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="df9c3-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="df9c3-111">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="df9c3-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="df9c3-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df9c3-112">Syntax</span></span>
```cpp
struct DML_RESAMPLE1_OPERATOR_DESC {
  const DML_TENSOR_DESC  *InputTensor;
  const DML_TENSOR_DESC  *OutputTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT                   DimensionCount;
  const FLOAT            *Scales;
  const FLOAT            *InputPixelOffsets;
  const FLOAT            *OutputPixelOffsets;
};
```



## <a name="members"></a><span data-ttu-id="df9c3-113">Members</span><span class="sxs-lookup"><span data-stu-id="df9c3-113">Members</span></span>

`InputTensor`

<span data-ttu-id="df9c3-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="df9c3-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="df9c3-115">Tensore contenente i dati di input.</span><span class="sxs-lookup"><span data-stu-id="df9c3-115">The tensor containing the input data.</span></span>


`OutputTensor`

<span data-ttu-id="df9c3-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="df9c3-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="df9c3-117">Tensore in cui scrivere i dati di output.</span><span class="sxs-lookup"><span data-stu-id="df9c3-117">The tensor to write the output data to.</span></span>


`InterpolationMode`

<span data-ttu-id="df9c3-118">Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="df9c3-118">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="df9c3-119">Questo campo determina il tipo di interpolazione usata per scegliere i pixel di output.</span><span class="sxs-lookup"><span data-stu-id="df9c3-119">This field determines the kind of interpolation used to choose output pixels.</span></span>

- <span data-ttu-id="df9c3-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span><span class="sxs-lookup"><span data-stu-id="df9c3-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span></span> <span data-ttu-id="df9c3-121">Usa *l'algoritmo Nearest Neighbor,* che sceglie l'elemento di input più vicino al centro pixel corrispondente per ogni elemento di output.</span><span class="sxs-lookup"><span data-stu-id="df9c3-121">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>

- <span data-ttu-id="df9c3-122">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="df9c3-122">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="df9c3-123">Usa *l'algoritmo Quadrilineare,* che calcola l'elemento di output eseguendo la media ponderata dei 2 elementi di input adiacenti più vicini per ogni dimensione.</span><span class="sxs-lookup"><span data-stu-id="df9c3-123">Uses the *Quadrilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="df9c3-124">Poiché è possibile ricampionare tutte e 4 le dimensioni, la media ponderata viene calcolata su un totale di 16 elementi di input per ogni elemento di output.</span><span class="sxs-lookup"><span data-stu-id="df9c3-124">Since all 4 dimensions can be resampled, the weighted average is computed on a total of 16 input elements for each output element.</span></span>


`DimensionCount`

<span data-ttu-id="df9c3-125">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="df9c3-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="df9c3-126">Numero di valori nelle matrici a cui puntano *Scales,* *InputPixelOffsets* e *OutputPixelOffsets.*</span><span class="sxs-lookup"><span data-stu-id="df9c3-126">The number of values in the arrays that *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* point to.</span></span> <span data-ttu-id="df9c3-127">Questo valore deve corrispondere al numero di dimensioni *di InputTensor* e *OutputTensor*, che deve essere 4.</span><span class="sxs-lookup"><span data-stu-id="df9c3-127">This value must match the dimension count of *InputTensor* and *OutputTensor*, which has to be 4.</span></span>


`Scales`

<span data-ttu-id="df9c3-128">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="df9c3-128">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="df9c3-129">Le scale da applicare quando si ricampiona l'input, in cui le scale > 1 ridimensionano l'immagine e < 1 ridimensionano l'immagine per tale dimensione.</span><span class="sxs-lookup"><span data-stu-id="df9c3-129">The scales to apply when resampling the input, where scales > 1 scale up the image and scales < 1 scale down the image for that dimension.</span></span> <span data-ttu-id="df9c3-130">Si noti che le scale non devono essere esattamente `OutputSize / InputSize` .</span><span class="sxs-lookup"><span data-stu-id="df9c3-130">Note that the scales don't need to be exactly `OutputSize / InputSize`.</span></span> <span data-ttu-id="df9c3-131">Se l'input dopo il ridimensionamento è maggiore del limite di output, viene ritagliato in base alle dimensioni di output.</span><span class="sxs-lookup"><span data-stu-id="df9c3-131">If the input after scaling is larger than the output bound, then we crop it to the output size.</span></span> <span data-ttu-id="df9c3-132">D'altra parte, se l'input dopo il ridimensionamento è più piccolo del limite di output, i bordi di output sono vincolati.</span><span class="sxs-lookup"><span data-stu-id="df9c3-132">On the other hand, if the input after scaling is smaller than the output bound, the output edges are clamped.</span></span>


`InputPixelOffsets`

<span data-ttu-id="df9c3-133">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="df9c3-133">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="df9c3-134">Offset da applicare ai pixel di input prima del ricampionamento.</span><span class="sxs-lookup"><span data-stu-id="df9c3-134">The offsets to apply to the input pixels before resampling.</span></span> <span data-ttu-id="df9c3-135">Quando questo valore è , viene usato l'angolo superiore sinistro del pixel anziché il relativo centro, che in genere non dà `0` il risultato previsto.</span><span class="sxs-lookup"><span data-stu-id="df9c3-135">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="df9c3-136">Per ricampionare l'immagine usando il centro dei pixel e ottenere lo stesso comportamento DML_RESAMPLE_OPERATOR_DESC [,](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)questo valore deve essere `0.5` .</span><span class="sxs-lookup"><span data-stu-id="df9c3-136">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `0.5`.</span></span>


`OutputPixelOffsets`

<span data-ttu-id="df9c3-137">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="df9c3-137">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="df9c3-138">Offset da applicare ai pixel di output dopo il ricampionamento.</span><span class="sxs-lookup"><span data-stu-id="df9c3-138">The offsets to apply to the output pixels after resampling.</span></span> <span data-ttu-id="df9c3-139">Quando questo valore è , viene usato l'angolo superiore sinistro del pixel anziché il relativo centro, che in genere non dà `0` il risultato previsto.</span><span class="sxs-lookup"><span data-stu-id="df9c3-139">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="df9c3-140">Per ricampionare l'immagine usando il centro dei pixel e ottenere lo stesso comportamento DML_RESAMPLE_OPERATOR_DESC [,](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)questo valore deve essere `-0.5` .</span><span class="sxs-lookup"><span data-stu-id="df9c3-140">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `-0.5`.</span></span>


## <a name="remarks"></a><span data-ttu-id="df9c3-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="df9c3-141">Remarks</span></span>
<span data-ttu-id="df9c3-142">Quando *InputPixelOffsets* è impostato su 0,5 e *OutputPixelOffsets* è impostato su -0,5, questo operatore equivale a [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="df9c3-142">When the *InputPixelOffsets* are set to 0.5, and the *OutputPixelOffsets* are set to -0.5, this operator is equivalent to [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="df9c3-143">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="df9c3-143">Availability</span></span>
<span data-ttu-id="df9c3-144">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="df9c3-144">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="df9c3-145">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="df9c3-145">Tensor constraints</span></span>
<span data-ttu-id="df9c3-146">*InputTensor* e *OutputTensor* devono avere lo stesso *tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="df9c3-146">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="df9c3-147">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="df9c3-147">Tensor support</span></span>
| <span data-ttu-id="df9c3-148">Tensore</span><span class="sxs-lookup"><span data-stu-id="df9c3-148">Tensor</span></span> | <span data-ttu-id="df9c3-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="df9c3-149">Kind</span></span> | <span data-ttu-id="df9c3-150">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="df9c3-150">Supported dimension counts</span></span> | <span data-ttu-id="df9c3-151">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="df9c3-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="df9c3-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="df9c3-152">InputTensor</span></span> | <span data-ttu-id="df9c3-153">Input</span><span class="sxs-lookup"><span data-stu-id="df9c3-153">Input</span></span> | <span data-ttu-id="df9c3-154">4</span><span class="sxs-lookup"><span data-stu-id="df9c3-154">4</span></span> | <span data-ttu-id="df9c3-155">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="df9c3-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="df9c3-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="df9c3-156">OutputTensor</span></span> | <span data-ttu-id="df9c3-157">Output</span><span class="sxs-lookup"><span data-stu-id="df9c3-157">Output</span></span> | <span data-ttu-id="df9c3-158">4</span><span class="sxs-lookup"><span data-stu-id="df9c3-158">4</span></span> | <span data-ttu-id="df9c3-159">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="df9c3-159">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="df9c3-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df9c3-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="df9c3-161">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="df9c3-161">**Header**</span></span> | <span data-ttu-id="df9c3-162">directml.h</span><span class="sxs-lookup"><span data-stu-id="df9c3-162">directml.h</span></span> |