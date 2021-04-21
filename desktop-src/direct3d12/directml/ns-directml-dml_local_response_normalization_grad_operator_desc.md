---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per la [normalizzazione della risposta locale.](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)
helpviewer_keywords:
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_local_response_normalization_grad_operator_desc
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: eecf849a06ee8e99ac9c015ecd4568496120b2d9
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804470"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="30592-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="30592-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="30592-104">Calcola le sfumature di backpropagation per la [normalizzazione della risposta locale.](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="30592-104">Computes backpropagation gradients for [local response normalization](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).</span></span>

<span data-ttu-id="30592-105">Il tipo di dati e le dimensioni di tutti i tensori devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="30592-105">The data type and size of all tensors must be the same.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30592-106">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.5 e successive).</span><span class="sxs-lookup"><span data-stu-id="30592-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="30592-107">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="30592-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="30592-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30592-108">Syntax</span></span>
```cpp
struct DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    BOOL CrossChannel;
    UINT LocalSize;
    FLOAT Alpha;
    FLOAT Beta;
    FLOAT Bias;
};
```

## <a name="members"></a><span data-ttu-id="30592-109">Members</span><span class="sxs-lookup"><span data-stu-id="30592-109">Members</span></span>

`InputTensor`

<span data-ttu-id="30592-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="30592-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="30592-111">Tensore contenente i dati di input.</span><span class="sxs-lookup"><span data-stu-id="30592-111">The tensor containing the input data.</span></span> <span data-ttu-id="30592-112">Le dimensioni di *questo* tensore devono essere `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="30592-112">This tensor's *Sizes* should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`InputGradientTensor`

<span data-ttu-id="30592-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="30592-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="30592-114">Tensore sfumatura in ingresso.</span><span class="sxs-lookup"><span data-stu-id="30592-114">The incoming gradient tensor.</span></span> <span data-ttu-id="30592-115">Questa operazione viene in genere ottenuta dall'output della backpropagazione di un livello precedente.</span><span class="sxs-lookup"><span data-stu-id="30592-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span>

`OutputGradientTensor`

<span data-ttu-id="30592-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="30592-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="30592-117">Tensore di output contenente le sfumature backpropagate.</span><span class="sxs-lookup"><span data-stu-id="30592-117">An output tensor containing the backpropagated gradients.</span></span>

`CrossChannel`

<span data-ttu-id="30592-118">Tipo: **[BOOL](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="30592-118">Type: **[BOOL](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="30592-119">**TRUE** se il livello LRN viene sommato tra canali; **FALSE** se il livello LRN somma le dimensioni spaziali.</span><span class="sxs-lookup"><span data-stu-id="30592-119">**TRUE** if the LRN layer sums across channels; **FALSE** if the LRN layer sums across spatial dimensions.</span></span>

`LocalSize`

<span data-ttu-id="30592-120">Tipo: **[UINT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="30592-120">Type: **[UINT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="30592-121">Numero massimo di elementi da sommare per ogni dimensione (l'area locale viene ritagliata in modo che tutti gli elementi siano entro limiti).</span><span class="sxs-lookup"><span data-stu-id="30592-121">The maximum number of elements to sum over per dimension (the local region is clipped so that all elements are within bounds).</span></span> <span data-ttu-id="30592-122">Se *CrossChannel* è **TRUE,** si tratta della larghezza e dell'altezza dell'area locale.</span><span class="sxs-lookup"><span data-stu-id="30592-122">If *CrossChannel* is **TRUE**, then this is the width and height of the local region.</span></span> <span data-ttu-id="30592-123">Se *CrossChannel* è **FALSE,** questo è il numero di elementi nell'area locale.</span><span class="sxs-lookup"><span data-stu-id="30592-123">If *CrossChannel* is **FALSE**, then this is the number of elements in the local region.</span></span> <span data-ttu-id="30592-124">Il valore deve essere almeno 1.</span><span class="sxs-lookup"><span data-stu-id="30592-124">This value must be at least 1.</span></span>

`Alpha`

<span data-ttu-id="30592-125">Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="30592-125">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="30592-126">Valore del parametro di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="30592-126">The value of the scaling parameter.</span></span> <span data-ttu-id="30592-127">È consigliabile impostare il valore predefinito su 0,0001.</span><span class="sxs-lookup"><span data-stu-id="30592-127">We recommend a value of 0.0001 as default.</span></span>

`Beta`

<span data-ttu-id="30592-128">Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="30592-128">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="30592-129">Valore dell'esponente.</span><span class="sxs-lookup"><span data-stu-id="30592-129">The value of the exponent.</span></span> <span data-ttu-id="30592-130">È consigliabile impostare il valore predefinito su 0,75.</span><span class="sxs-lookup"><span data-stu-id="30592-130">We recommend a value of 0.75 as default.</span></span>

`Bias`

<span data-ttu-id="30592-131">Tipo: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="30592-131">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="30592-132">Valore della distorsione.</span><span class="sxs-lookup"><span data-stu-id="30592-132">The value of bias.</span></span> <span data-ttu-id="30592-133">È consigliabile impostare il valore predefinito su 1.</span><span class="sxs-lookup"><span data-stu-id="30592-133">We recommend a value of 1 as default.</span></span>

## <a name="availability"></a><span data-ttu-id="30592-134">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="30592-134">Availability</span></span>
<span data-ttu-id="30592-135">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="30592-135">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="30592-136">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="30592-136">Tensor constraints</span></span>
<span data-ttu-id="30592-137">*InputGradientTensor,* *InputTensor* e *OutputGradientTensor* devono avere gli stessi *valori di DataType* *e Sizes.*</span><span class="sxs-lookup"><span data-stu-id="30592-137">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="30592-138">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="30592-138">Tensor support</span></span>
| <span data-ttu-id="30592-139">Tensore</span><span class="sxs-lookup"><span data-stu-id="30592-139">Tensor</span></span> | <span data-ttu-id="30592-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="30592-140">Kind</span></span> | <span data-ttu-id="30592-141">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="30592-141">Supported dimension counts</span></span> | <span data-ttu-id="30592-142">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="30592-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="30592-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="30592-143">InputTensor</span></span> | <span data-ttu-id="30592-144">Input</span><span class="sxs-lookup"><span data-stu-id="30592-144">Input</span></span> | <span data-ttu-id="30592-145">4</span><span class="sxs-lookup"><span data-stu-id="30592-145">4</span></span> | <span data-ttu-id="30592-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="30592-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="30592-147">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="30592-147">InputGradientTensor</span></span> | <span data-ttu-id="30592-148">Input</span><span class="sxs-lookup"><span data-stu-id="30592-148">Input</span></span> | <span data-ttu-id="30592-149">4</span><span class="sxs-lookup"><span data-stu-id="30592-149">4</span></span> | <span data-ttu-id="30592-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="30592-150">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="30592-151">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="30592-151">OutputGradientTensor</span></span> | <span data-ttu-id="30592-152">Output</span><span class="sxs-lookup"><span data-stu-id="30592-152">Output</span></span> | <span data-ttu-id="30592-153">4</span><span class="sxs-lookup"><span data-stu-id="30592-153">4</span></span> | <span data-ttu-id="30592-154">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="30592-154">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="30592-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30592-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="30592-156">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="30592-156">**Header**</span></span> | <span data-ttu-id="30592-157">directml.h</span><span class="sxs-lookup"><span data-stu-id="30592-157">directml.h</span></span> |
