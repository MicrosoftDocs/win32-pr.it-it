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
ms.openlocfilehash: 759bf25d4b6a97e70c6de7708a5c9fd0bccae439
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803402"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="e3dbd-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="e3dbd-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e3dbd-105">Esegue una funzione di normalizzazione della varianza media sul tensore di input.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="e3dbd-106">Questo operatore calcolerà la media e la varianza del tensore di input per eseguire la normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="e3dbd-107">Questo operatore esegue il calcolo seguente.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="e3dbd-108">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="e3dbd-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e3dbd-109">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="e3dbd-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3dbd-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3dbd-110">Syntax</span></span>
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
## <a name="members"></a><span data-ttu-id="e3dbd-111">Members</span><span class="sxs-lookup"><span data-stu-id="e3dbd-111">Members</span></span>

`InputTensor`

<span data-ttu-id="e3dbd-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e3dbd-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e3dbd-113">Tensore contenente i dati di input.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-113">A tensor containing the Input data.</span></span> <span data-ttu-id="e3dbd-114">Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="e3dbd-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`ScaleTensor`

<span data-ttu-id="e3dbd-115">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e3dbd-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e3dbd-116">Tensore facoltativo contenente i dati di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-116">An optional tensor containing the Scale data.</span></span>

<span data-ttu-id="e3dbd-117">Se **DML_FEATURE_LEVEL** è minore di **DML_FEATURE_LEVEL_4_0**, le dimensioni di questo tensore devono essere `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` .</span><span class="sxs-lookup"><span data-stu-id="e3dbd-117">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }`.</span></span> <span data-ttu-id="e3dbd-118">Le dimensioni ScaleBatchCount, ScaleHeight e ScaleWidth devono corrispondere a *InputTensor* o essere impostate su 1 per trasmettere automaticamente tali dimensioni nell'input.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-118">The dimensions ScaleBatchCount, ScaleHeight, and ScaleWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="e3dbd-119">Se **DML_FEATURE_LEVEL** è maggiore o uguale **a DML_FEATURE_LEVEL_4_0**, qualsiasi dimensione può essere impostata su 1 e trasmessa automaticamente in modo che corrisponda a *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-119">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="e3dbd-120">Questo tensore è necessario se *si usa BiasTensor.*</span><span class="sxs-lookup"><span data-stu-id="e3dbd-120">This tensor is required if the *BiasTensor* is used.</span></span>

`BiasTensor`

<span data-ttu-id="e3dbd-121">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e3dbd-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>


<span data-ttu-id="e3dbd-122">Tensore facoltativo contenente i dati di Bias.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-122">An optional tensor containing the Bias data.</span></span>

<span data-ttu-id="e3dbd-123">Se **DML_FEATURE_LEVEL** è minore di **DML_FEATURE_LEVEL_4_0**, le dimensioni di questo tensore devono essere `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` .</span><span class="sxs-lookup"><span data-stu-id="e3dbd-123">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }`.</span></span> <span data-ttu-id="e3dbd-124">Le dimensioni BiasBatchCount, BiasHeight e BiasWidth devono corrispondere a *InputTensor* o essere impostate su 1 per trasmettere automaticamente tali dimensioni nell'input.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-124">The dimensions BiasBatchCount, BiasHeight, and BiasWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="e3dbd-125">Se **DML_FEATURE_LEVEL** è maggiore o uguale a **DML_FEATURE_LEVEL_4_0**, qualsiasi dimensione può essere impostata su 1 e trasmessa automaticamente in modo che corrisponda a *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-125">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="e3dbd-126">Questo tensore è obbligatorio se *si usa ScaleTensor.*</span><span class="sxs-lookup"><span data-stu-id="e3dbd-126">This tensor is required if the *ScaleTensor* is used.</span></span>

`OutputTensor`

<span data-ttu-id="e3dbd-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e3dbd-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e3dbd-128">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-128">A tensor to write the results to.</span></span> <span data-ttu-id="e3dbd-129">Le dimensioni di questo tensore sono `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="e3dbd-129">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`AxisCount`

<span data-ttu-id="e3dbd-130">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span><span class="sxs-lookup"><span data-stu-id="e3dbd-130">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="e3dbd-131">Numero di assi.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-131">The number of axes.</span></span> <span data-ttu-id="e3dbd-132">Questo campo determina le dimensioni della *matrice Axes.*</span><span class="sxs-lookup"><span data-stu-id="e3dbd-132">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="e3dbd-133">Tipo: \_ Dimensione \_ campo \_ (AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="e3dbd-133">Type: \_Field\_size\_(AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span> 

<span data-ttu-id="e3dbd-134">Assi lungo i quali calcolare la media e la varianza.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-134">The axes along which to calculate the Mean and Variance.</span></span>

`NormalizeVariance`

<span data-ttu-id="e3dbd-135">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="e3dbd-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="e3dbd-136">**TRUE** se il livello di normalizzazione include Varianza nel calcolo della normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-136">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="e3dbd-137">In caso contrario, **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="e3dbd-137">Otherwise, **FALSE**.</span></span> <span data-ttu-id="e3dbd-138">Se **FALSE,** l'equazione di normalizzazione è `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="e3dbd-138">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>

`Epsilon`

<span data-ttu-id="e3dbd-139">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="e3dbd-139">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="e3dbd-140">Valore epsilon da utilizzare per evitare la divisione per zero.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-140">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="e3dbd-141">Il valore predefinito è 0,00001.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-141">A value of 0.00001 is recommended as default.</span></span>

`FusedActivation`

<span data-ttu-id="e3dbd-142">Tipo: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e3dbd-142">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="e3dbd-143">Livello di attivazione fuso facoltativo da applicare dopo la normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-143">An optional fused activation layer to apply after the normalization.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3dbd-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3dbd-144">Remarks</span></span>
<span data-ttu-id="e3dbd-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** è un superset di funzionalità di [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="e3dbd-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="e3dbd-146">In questo caso, l'impostazione della matrice **Axes** su equivale all'impostazione di CrossChannel su FALSE in DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC , mentre l'impostazione della matrice Axes su equivale all'impostazione di `{ 0, 2, 3 }`     `{ 1, 2, 3 }` *CrossChannel* su **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="e3dbd-146">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="e3dbd-147">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="e3dbd-147">Availability</span></span>
<span data-ttu-id="e3dbd-148">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="e3dbd-148">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e3dbd-149">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="e3dbd-149">Tensor constraints</span></span>

<span data-ttu-id="e3dbd-150">*BiasTensor,* *InputTensor,* *OutputTensor* e *ScaleTensor* devono avere gli stessi *valori di DataType* *e DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="e3dbd-150">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e3dbd-151">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="e3dbd-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="e3dbd-152">DML_FEATURE_LEVEL_3_1 e successive</span><span class="sxs-lookup"><span data-stu-id="e3dbd-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="e3dbd-153">Tensore</span><span class="sxs-lookup"><span data-stu-id="e3dbd-153">Tensor</span></span> | <span data-ttu-id="e3dbd-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3dbd-154">Kind</span></span> | <span data-ttu-id="e3dbd-155">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="e3dbd-155">Supported dimension counts</span></span> | <span data-ttu-id="e3dbd-156">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="e3dbd-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e3dbd-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="e3dbd-157">InputTensor</span></span> | <span data-ttu-id="e3dbd-158">Input</span><span class="sxs-lookup"><span data-stu-id="e3dbd-158">Input</span></span> | <span data-ttu-id="e3dbd-159">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e3dbd-159">1 to 8</span></span> | <span data-ttu-id="e3dbd-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e3dbd-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e3dbd-161">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="e3dbd-161">ScaleTensor</span></span> | <span data-ttu-id="e3dbd-162">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="e3dbd-162">Optional input</span></span> | <span data-ttu-id="e3dbd-163">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e3dbd-163">1 to 8</span></span> | <span data-ttu-id="e3dbd-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e3dbd-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e3dbd-165">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="e3dbd-165">BiasTensor</span></span> | <span data-ttu-id="e3dbd-166">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="e3dbd-166">Optional input</span></span> | <span data-ttu-id="e3dbd-167">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e3dbd-167">1 to 8</span></span> | <span data-ttu-id="e3dbd-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e3dbd-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e3dbd-169">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e3dbd-169">OutputTensor</span></span> | <span data-ttu-id="e3dbd-170">Output</span><span class="sxs-lookup"><span data-stu-id="e3dbd-170">Output</span></span> | <span data-ttu-id="e3dbd-171">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e3dbd-171">1 to 8</span></span> | <span data-ttu-id="e3dbd-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e3dbd-172">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="e3dbd-173">DML_FEATURE_LEVEL_2_1 e successive</span><span class="sxs-lookup"><span data-stu-id="e3dbd-173">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="e3dbd-174">Tensore</span><span class="sxs-lookup"><span data-stu-id="e3dbd-174">Tensor</span></span> | <span data-ttu-id="e3dbd-175">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3dbd-175">Kind</span></span> | <span data-ttu-id="e3dbd-176">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="e3dbd-176">Supported dimension counts</span></span> | <span data-ttu-id="e3dbd-177">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="e3dbd-177">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e3dbd-178">InputTensor</span><span class="sxs-lookup"><span data-stu-id="e3dbd-178">InputTensor</span></span> | <span data-ttu-id="e3dbd-179">Input</span><span class="sxs-lookup"><span data-stu-id="e3dbd-179">Input</span></span> | <span data-ttu-id="e3dbd-180">4</span><span class="sxs-lookup"><span data-stu-id="e3dbd-180">4</span></span> | <span data-ttu-id="e3dbd-181">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e3dbd-181">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e3dbd-182">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="e3dbd-182">ScaleTensor</span></span> | <span data-ttu-id="e3dbd-183">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="e3dbd-183">Optional input</span></span> | <span data-ttu-id="e3dbd-184">4</span><span class="sxs-lookup"><span data-stu-id="e3dbd-184">4</span></span> | <span data-ttu-id="e3dbd-185">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e3dbd-185">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e3dbd-186">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="e3dbd-186">BiasTensor</span></span> | <span data-ttu-id="e3dbd-187">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="e3dbd-187">Optional input</span></span> | <span data-ttu-id="e3dbd-188">4</span><span class="sxs-lookup"><span data-stu-id="e3dbd-188">4</span></span> | <span data-ttu-id="e3dbd-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e3dbd-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e3dbd-190">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e3dbd-190">OutputTensor</span></span> | <span data-ttu-id="e3dbd-191">Output</span><span class="sxs-lookup"><span data-stu-id="e3dbd-191">Output</span></span> | <span data-ttu-id="e3dbd-192">4</span><span class="sxs-lookup"><span data-stu-id="e3dbd-192">4</span></span> | <span data-ttu-id="e3dbd-193">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e3dbd-193">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="e3dbd-194">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3dbd-194">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e3dbd-195">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="e3dbd-195">**Header**</span></span> | <span data-ttu-id="e3dbd-196">directml.h</span><span class="sxs-lookup"><span data-stu-id="e3dbd-196">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="e3dbd-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3dbd-197">See also</span></span>

[<span data-ttu-id="e3dbd-198">Uso di operatori fusibili per migliorare le prestazioni</span><span class="sxs-lookup"><span data-stu-id="e3dbd-198">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)
