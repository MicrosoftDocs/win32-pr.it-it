---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per la [normalizzazione batch.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)
helpviewer_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_batch_normalization_grad_operator_desc
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: ba12541514c8121d483236afa2163a04bd991288
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804519"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="2f1dd-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="2f1dd-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="2f1dd-104">Calcola le sfumature di backpropagation per la [normalizzazione batch.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="2f1dd-104">Computes backpropagation gradients for [batch normalization](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).</span></span> <span data-ttu-id="2f1dd-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** esegue più calcoli, che sono dettagliati nelle descrizioni di output separate.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** performs multiple computations, which are detailed in the separate output descriptions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f1dd-106">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.5 e successive).</span><span class="sxs-lookup"><span data-stu-id="2f1dd-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="2f1dd-107">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="2f1dd-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f1dd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f1dd-108">Syntax</span></span>
```cpp
struct DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* MeanTensor;
    const DML_TENSOR_DESC* VarianceTensor;
    const DML_TENSOR_DESC* ScaleTensor;

    const DML_TENSOR_DESC* OutputGradientTensor;
    const DML_TENSOR_DESC* OutputScaleGradientTensor;
    const DML_TENSOR_DESC* OutputBiasGradientTensor;

    FLOAT Epsilon;
};
```

## <a name="members"></a><span data-ttu-id="2f1dd-109">Members</span><span class="sxs-lookup"><span data-stu-id="2f1dd-109">Members</span></span>

`InputTensor`

<span data-ttu-id="2f1dd-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2f1dd-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2f1dd-111">Tensore contenente i dati di input.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-111">A tensor containing the input data.</span></span> <span data-ttu-id="2f1dd-112">Si tratta in genere dello stesso tensore fornito da *InputTensor* DML_BATCH_NORMALIZATION_OPERATOR_DESC [**nel**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-112">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="2f1dd-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2f1dd-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2f1dd-114">Tensore sfumatura in ingresso.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-114">The incoming gradient tensor.</span></span> <span data-ttu-id="2f1dd-115">Questa operazione viene in genere ottenuta dall'output della backpropagazione di un livello precedente.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="2f1dd-116">Questo tensore deve avere le stesse dimensioni delle dimensioni *di InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-116">This tensor must have the same dimension sizes as *InputTensor*.</span></span>

`MeanTensor`

<span data-ttu-id="2f1dd-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2f1dd-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2f1dd-118">Tensore contenente i dati medio.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-118">A tensor containing the mean data.</span></span> <span data-ttu-id="2f1dd-119">Questo è in genere lo stesso tensore fornito dal *MeanTensor* per DML_BATCH_NORMALIZATION_OPERATOR_DESC [**nel**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-119">This is typically the same tensor that was provided as the *MeanTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="2f1dd-120">Tutte le dimensioni che non hanno le stesse dimensioni della dimensione corrispondente di *InputTensor* devono avere una dimensione di 1 in modo che possano essere trasmesse in modo che corrispondano all'input.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-120">Any dimensions that don't have the same size as the corresponding dimension of *InputTensor* must have a size of 1 so that they can be broadcast to match the input.</span></span>

<span data-ttu-id="2f1dd-121">Ad esempio, le dimensioni seguenti sono accettabili.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-121">For example, the following sizes are acceptable.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

<span data-ttu-id="2f1dd-122">Di seguito è riportato un errore perché, per essere compatibili con la trasmissione, le dimensioni che non corrispondono devono essere di dimensioni 1.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-122">The following is an error since, in order to be broadcast compatible, any dimensions that don't match must be size 1.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

<span data-ttu-id="2f1dd-123">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2f1dd-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2f1dd-124">Tensore contenente i dati di varianza.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-124">A tensor containing the variance data.</span></span> <span data-ttu-id="2f1dd-125">Si tratta in genere dello stesso tensore fornito da *VarianceTensor* per DML_BATCH_NORMALIZATION_OPERATOR_DESC [**nel**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-125">This is typically the same tensor that was provided as the *VarianceTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="2f1dd-126">Questo tensore deve avere le stesse dimensioni di *MeanTensor.*</span><span class="sxs-lookup"><span data-stu-id="2f1dd-126">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`ScaleTensor`

<span data-ttu-id="2f1dd-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2f1dd-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2f1dd-128">Tensore contenente i dati della scala.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-128">A tensor containing the scale data.</span></span> <span data-ttu-id="2f1dd-129">Si tratta in genere dello stesso tensore fornito da *ScaleTensor* per DML_BATCH_NORMALIZATION_OPERATOR_DESC [**nel**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-129">This is typically the same tensor that was provided as the *ScaleTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="2f1dd-130">Questo tensore deve avere le stesse dimensioni di *MeanTensor.*</span><span class="sxs-lookup"><span data-stu-id="2f1dd-130">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`OutputGradientTensor`

<span data-ttu-id="2f1dd-131">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2f1dd-131">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2f1dd-132">Per ogni valore corrispondente negli input, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` .</span><span class="sxs-lookup"><span data-stu-id="2f1dd-132">For every corresponding value in the inputs, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))`.</span></span>

<span data-ttu-id="2f1dd-133">Questo tensore deve avere le stesse dimensioni di *InputTensor* / *InputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-133">This tensor must have the same dimension sizes as *InputTensor*/*InputGradientTensor*.</span></span>

`OutputScaleGradientTensor`

<span data-ttu-id="2f1dd-134">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2f1dd-134">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2f1dd-135">Questo tensore deve avere le stesse dimensioni delle *dimensioni di MeanTensor* / *VarianceTensor* / *ScaleTensor'.*</span><span class="sxs-lookup"><span data-stu-id="2f1dd-135">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="2f1dd-136">Viene eseguito il calcolo seguente o ogni valore corrispondente negli input.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-136">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

<span data-ttu-id="2f1dd-137">`sum`l'oggetto viene calcolato in tutte le dimensioni che devono essere trasmesse.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-137">The `sum` is computed across any dimensions that need to be broadcast.</span></span> <span data-ttu-id="2f1dd-138">Se non è necessaria alcuna trasmissione, non è necessaria alcuna somma.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-138">If there is no broadcast needed, then no sum is needed.</span></span>

<span data-ttu-id="2f1dd-139">Ecco un esempio.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-139">Here's an example.</span></span>

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

<span data-ttu-id="2f1dd-140">L'elemento **[0, 0**, 0, 0] di è la somma di per tutti i `OutputScaleGradientTensor` `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` 90 (3 \* 5 \* 6) elementi [[0,2], **0**, [0,4], [0,5]].</span><span class="sxs-lookup"><span data-stu-id="2f1dd-140">Element [0, **0**, 0, 0] of `OutputScaleGradientTensor` is the sum of `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` for all 90 (3\*5\*6) elements [[0,2], **0**, [0,4], [0,5]].</span></span>

`OutputBiasGradientTensor`

<span data-ttu-id="2f1dd-141">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2f1dd-141">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2f1dd-142">Questo tensore deve avere le stesse dimensioni di *MeanTensor* / *VarianceTensor* / *ScaleTensor'*.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-142">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="2f1dd-143">Viene eseguito il calcolo seguente o ogni valore corrispondente negli input.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-143">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputBiasGradient = sum(InputGradient)`  

<span data-ttu-id="2f1dd-144">L'oggetto viene calcolato in tutte le dimensioni che `sum` devono essere trasmesse (vedere l'esempio per *OutputScaleGradientTensor*).</span><span class="sxs-lookup"><span data-stu-id="2f1dd-144">The `sum` is computed across any dimensions that need to be broadcast (see the example for *OutputScaleGradientTensor*).</span></span> <span data-ttu-id="2f1dd-145">Se non è necessaria alcuna trasmissione, non è necessaria alcuna somma.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-145">If there is no broadcast needed, then no sum is needed.</span></span>

`Epsilon`

<span data-ttu-id="2f1dd-146">Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2f1dd-146">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="2f1dd-147">Valore piccolo aggiunto alla varianza per evitare zero.</span><span class="sxs-lookup"><span data-stu-id="2f1dd-147">A small value added to the variance to avoid zero.</span></span>

## <a name="availability"></a><span data-ttu-id="2f1dd-148">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="2f1dd-148">Availability</span></span>
<span data-ttu-id="2f1dd-149">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="2f1dd-149">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="2f1dd-150">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="2f1dd-150">Tensor constraints</span></span>
<span data-ttu-id="2f1dd-151">*InputGradientTensor,* *InputTensor,* *MeanTensor,* *OutputBiasGradientTensor,* *OutputGradientTensor,* *OutputScaleGradientTensor,* *ScaleTensor* e *VarianceTensor* devono avere gli stessi *DataType* *e DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="2f1dd-151">*InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor*, and *VarianceTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="2f1dd-152">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="2f1dd-152">Tensor support</span></span>
| <span data-ttu-id="2f1dd-153">Tensore</span><span class="sxs-lookup"><span data-stu-id="2f1dd-153">Tensor</span></span> | <span data-ttu-id="2f1dd-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="2f1dd-154">Kind</span></span> | <span data-ttu-id="2f1dd-155">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="2f1dd-155">Supported dimension counts</span></span> | <span data-ttu-id="2f1dd-156">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="2f1dd-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="2f1dd-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="2f1dd-157">InputTensor</span></span> | <span data-ttu-id="2f1dd-158">Input</span><span class="sxs-lookup"><span data-stu-id="2f1dd-158">Input</span></span> | <span data-ttu-id="2f1dd-159">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="2f1dd-159">1 to 8</span></span> | <span data-ttu-id="2f1dd-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2f1dd-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2f1dd-161">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="2f1dd-161">InputGradientTensor</span></span> | <span data-ttu-id="2f1dd-162">Input</span><span class="sxs-lookup"><span data-stu-id="2f1dd-162">Input</span></span> | <span data-ttu-id="2f1dd-163">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="2f1dd-163">1 to 8</span></span> | <span data-ttu-id="2f1dd-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2f1dd-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2f1dd-165">MeanTensor</span><span class="sxs-lookup"><span data-stu-id="2f1dd-165">MeanTensor</span></span> | <span data-ttu-id="2f1dd-166">Input</span><span class="sxs-lookup"><span data-stu-id="2f1dd-166">Input</span></span> | <span data-ttu-id="2f1dd-167">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="2f1dd-167">1 to 8</span></span> | <span data-ttu-id="2f1dd-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2f1dd-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2f1dd-169">VarianceTensor</span><span class="sxs-lookup"><span data-stu-id="2f1dd-169">VarianceTensor</span></span> | <span data-ttu-id="2f1dd-170">Input</span><span class="sxs-lookup"><span data-stu-id="2f1dd-170">Input</span></span> | <span data-ttu-id="2f1dd-171">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="2f1dd-171">1 to 8</span></span> | <span data-ttu-id="2f1dd-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2f1dd-172">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2f1dd-173">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="2f1dd-173">ScaleTensor</span></span> | <span data-ttu-id="2f1dd-174">Input</span><span class="sxs-lookup"><span data-stu-id="2f1dd-174">Input</span></span> | <span data-ttu-id="2f1dd-175">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="2f1dd-175">1 to 8</span></span> | <span data-ttu-id="2f1dd-176">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2f1dd-176">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2f1dd-177">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="2f1dd-177">OutputGradientTensor</span></span> | <span data-ttu-id="2f1dd-178">Output</span><span class="sxs-lookup"><span data-stu-id="2f1dd-178">Output</span></span> | <span data-ttu-id="2f1dd-179">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="2f1dd-179">1 to 8</span></span> | <span data-ttu-id="2f1dd-180">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2f1dd-180">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2f1dd-181">OutputScaleGradientTensor</span><span class="sxs-lookup"><span data-stu-id="2f1dd-181">OutputScaleGradientTensor</span></span> | <span data-ttu-id="2f1dd-182">Output</span><span class="sxs-lookup"><span data-stu-id="2f1dd-182">Output</span></span> | <span data-ttu-id="2f1dd-183">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="2f1dd-183">1 to 8</span></span> | <span data-ttu-id="2f1dd-184">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2f1dd-184">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="2f1dd-185">OutputBiasGradientTensor</span><span class="sxs-lookup"><span data-stu-id="2f1dd-185">OutputBiasGradientTensor</span></span> | <span data-ttu-id="2f1dd-186">Output</span><span class="sxs-lookup"><span data-stu-id="2f1dd-186">Output</span></span> | <span data-ttu-id="2f1dd-187">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="2f1dd-187">1 to 8</span></span> | <span data-ttu-id="2f1dd-188">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2f1dd-188">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="2f1dd-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f1dd-189">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2f1dd-190">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="2f1dd-190">**Header**</span></span> | <span data-ttu-id="2f1dd-191">directml.h</span><span class="sxs-lookup"><span data-stu-id="2f1dd-191">directml.h</span></span> |
