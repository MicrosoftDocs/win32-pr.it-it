---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Esegue una funzione di normalizzazione della varianza media sul tensore di input. Questo operatore calcolerà la media e la varianza del tensore di input per eseguire la normalizzazione.
helpviewer_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure
- direct3d12.dml_mean_variance_normalization1_operator_desc
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.openlocfilehash: f3302f8081ed4bf64fa858ac3e303519089d01fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320368"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="63e10-104">Struttura DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="63e10-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="63e10-105">Esegue una funzione di normalizzazione della varianza media sul tensore di input.</span><span class="sxs-lookup"><span data-stu-id="63e10-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="63e10-106">Questo operatore calcolerà la media e la varianza del tensore di input per eseguire la normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="63e10-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="63e10-107">Questo operatore esegue il calcolo seguente.</span><span class="sxs-lookup"><span data-stu-id="63e10-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="63e10-108">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="63e10-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="63e10-109">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="63e10-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="63e10-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63e10-110">Syntax</span></span>
```cpp
struct DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC {
  const DML_TENSOR_DESC   *InputTensor;
  const DML_TENSOR_DESC   *ScaleTensor;
  const DML_TENSOR_DESC   *BiasTensor;
  const DML_TENSOR_DESC   *OutputTensor;
  UINT                    AxisCount;
  const UINT              *Axes;
  BOOL                    NormalizeVariance;
  FLOAT                   Epsilon;
  const DML_OPERATOR_DESC *FusedActivation;
};
```



## <a name="members"></a><span data-ttu-id="63e10-111">Members</span><span class="sxs-lookup"><span data-stu-id="63e10-111">Members</span></span>

`InputTensor`

<span data-ttu-id="63e10-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="63e10-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="63e10-113">Un tensore contenente i dati di input.</span><span class="sxs-lookup"><span data-stu-id="63e10-113">A tensor containing the Input data.</span></span> <span data-ttu-id="63e10-114">Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="63e10-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>


`ScaleTensor`

<span data-ttu-id="63e10-115">Tipo: \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="63e10-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="63e10-116">Un tensore facoltativo che contiene i dati della scala.</span><span class="sxs-lookup"><span data-stu-id="63e10-116">An optional tensor containing the Scale data.</span></span> <span data-ttu-id="63e10-117">Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="63e10-117">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="63e10-118">Qualsiasi dimensione può essere sostituita da 1 per la trasmissione in tale dimensione.</span><span class="sxs-lookup"><span data-stu-id="63e10-118">Any dimension can be replaced with 1 to broadcast in that dimension.</span></span> <span data-ttu-id="63e10-119">Questo tensore è obbligatorio se viene usato *BiasTensor* .</span><span class="sxs-lookup"><span data-stu-id="63e10-119">This tensor is required if the *BiasTensor* is used.</span></span>


`BiasTensor`

<span data-ttu-id="63e10-120">Tipo: \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="63e10-120">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="63e10-121">Un tensore facoltativo contenente i dati di distorsione.</span><span class="sxs-lookup"><span data-stu-id="63e10-121">An optional tensor containing the bias data.</span></span> <span data-ttu-id="63e10-122">Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="63e10-122">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="63e10-123">Qualsiasi dimensione può essere sostituita da 1 per la trasmissione in tale dimensione.</span><span class="sxs-lookup"><span data-stu-id="63e10-123">Any dimension can be replaced with 1 to broadcast in that dimension.</span></span> <span data-ttu-id="63e10-124">Questo tensore è obbligatorio se viene usato *ScaleTensor* .</span><span class="sxs-lookup"><span data-stu-id="63e10-124">This tensor is required if the *ScaleTensor* is used.</span></span>


`OutputTensor`

<span data-ttu-id="63e10-125">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="63e10-125">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="63e10-126">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="63e10-126">A tensor to write the results to.</span></span> <span data-ttu-id="63e10-127">Le dimensioni di questo tensore sono `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="63e10-127">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>


`AxisCount`

<span data-ttu-id="63e10-128">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="63e10-128">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="63e10-129">Numero di assi.</span><span class="sxs-lookup"><span data-stu-id="63e10-129">The number of axes.</span></span> <span data-ttu-id="63e10-130">Questo campo determina la dimensione della matrice di *assi* .</span><span class="sxs-lookup"><span data-stu-id="63e10-130">This field determines the size of the *Axes* array.</span></span>


`Axes`

<span data-ttu-id="63e10-131">Tipo: \_ \_ Dimensione campo \_ (AxisCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="63e10-131">Type: \_Field\_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span> 

<span data-ttu-id="63e10-132">Assi lungo i quali calcolare la media e la varianza.</span><span class="sxs-lookup"><span data-stu-id="63e10-132">The axes along which to calculate the Mean and Variance.</span></span>


`NormalizeVariance`

<span data-ttu-id="63e10-133">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="63e10-133">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="63e10-134">**True** se il livello di normalizzazione include la varianza nel calcolo di normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="63e10-134">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="63e10-135">In caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="63e10-135">Otherwise, **FALSE**.</span></span> <span data-ttu-id="63e10-136">Se **false**, l'equazione di normalizzazione è `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="63e10-136">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>


`Epsilon`

<span data-ttu-id="63e10-137">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="63e10-137">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="63e10-138">Valore Epsilon da usare per evitare la divisione per zero.</span><span class="sxs-lookup"><span data-stu-id="63e10-138">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="63e10-139">Per impostazione predefinita, è consigliato un valore di 0,00001.</span><span class="sxs-lookup"><span data-stu-id="63e10-139">A value of 0.00001 is recommended as default.</span></span>


`FusedActivation`

<span data-ttu-id="63e10-140">Tipo: \_ MAYBENULL \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="63e10-140">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="63e10-141">Livello di attivazione con fusibile facoltativo da applicare dopo la normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="63e10-141">An optional fused activation layer to apply after the normalization.</span></span>


## <a name="remarks"></a><span data-ttu-id="63e10-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="63e10-142">Remarks</span></span>
<span data-ttu-id="63e10-143">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** è un superset della funzionalità di [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="63e10-143">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="63e10-144">In questo caso, l'impostazione della matrice degli **assi** su `{ 0, 2, 3 }` è equivalente all'impostazione di *CrossChannel* su **false** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; durante l'impostazione della matrice degli **assi** su `{ 1, 2, 3 }` è equivalente all'impostazione di *Crosschannel* su **true**.</span><span class="sxs-lookup"><span data-stu-id="63e10-144">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="63e10-145">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="63e10-145">Availability</span></span>
<span data-ttu-id="63e10-146">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="63e10-146">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="63e10-147">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="63e10-147">Tensor constraints</span></span>
* <span data-ttu-id="63e10-148">*InputTensor* e *OutputTensor* devono avere le stesse *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="63e10-148">*InputTensor* and *OutputTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="63e10-149">*BiasTensor*, *InputTensor*, *OutputTensor* e *ScaleTensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="63e10-149">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="63e10-150">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="63e10-150">Tensor support</span></span>
| <span data-ttu-id="63e10-151">Tensore</span><span class="sxs-lookup"><span data-stu-id="63e10-151">Tensor</span></span> | <span data-ttu-id="63e10-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="63e10-152">Kind</span></span> | <span data-ttu-id="63e10-153">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="63e10-153">Dimensions</span></span> | <span data-ttu-id="63e10-154">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="63e10-154">Supported dimension counts</span></span> | <span data-ttu-id="63e10-155">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="63e10-155">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="63e10-156">InputTensor</span><span class="sxs-lookup"><span data-stu-id="63e10-156">InputTensor</span></span> | <span data-ttu-id="63e10-157">Input</span><span class="sxs-lookup"><span data-stu-id="63e10-157">Input</span></span> | <span data-ttu-id="63e10-158">{BatchCount, ChannelCount, Height, Width}</span><span class="sxs-lookup"><span data-stu-id="63e10-158">{ BatchCount, ChannelCount, Height, Width }</span></span> | <span data-ttu-id="63e10-159">4</span><span class="sxs-lookup"><span data-stu-id="63e10-159">4</span></span> | <span data-ttu-id="63e10-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="63e10-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="63e10-161">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="63e10-161">ScaleTensor</span></span> | <span data-ttu-id="63e10-162">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="63e10-162">Optional input</span></span> | <span data-ttu-id="63e10-163">{ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth}</span><span class="sxs-lookup"><span data-stu-id="63e10-163">{ ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth }</span></span> | <span data-ttu-id="63e10-164">4</span><span class="sxs-lookup"><span data-stu-id="63e10-164">4</span></span> | <span data-ttu-id="63e10-165">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="63e10-165">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="63e10-166">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="63e10-166">BiasTensor</span></span> | <span data-ttu-id="63e10-167">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="63e10-167">Optional input</span></span> | <span data-ttu-id="63e10-168">{ BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth }</span><span class="sxs-lookup"><span data-stu-id="63e10-168">{ BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth }</span></span> | <span data-ttu-id="63e10-169">4</span><span class="sxs-lookup"><span data-stu-id="63e10-169">4</span></span> | <span data-ttu-id="63e10-170">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="63e10-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="63e10-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="63e10-171">OutputTensor</span></span> | <span data-ttu-id="63e10-172">Output</span><span class="sxs-lookup"><span data-stu-id="63e10-172">Output</span></span> | <span data-ttu-id="63e10-173">{BatchCount, ChannelCount, Height, Width}</span><span class="sxs-lookup"><span data-stu-id="63e10-173">{ BatchCount, ChannelCount, Height, Width }</span></span> | <span data-ttu-id="63e10-174">4</span><span class="sxs-lookup"><span data-stu-id="63e10-174">4</span></span> | <span data-ttu-id="63e10-175">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="63e10-175">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="63e10-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63e10-176">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="63e10-177">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="63e10-177">**Header**</span></span> | <span data-ttu-id="63e10-178">directml. h</span><span class="sxs-lookup"><span data-stu-id="63e10-178">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="63e10-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63e10-179">See also</span></span>

[<span data-ttu-id="63e10-180">Utilizzo di operatori con fusibile per migliorare le prestazioni</span><span class="sxs-lookup"><span data-stu-id="63e10-180">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)