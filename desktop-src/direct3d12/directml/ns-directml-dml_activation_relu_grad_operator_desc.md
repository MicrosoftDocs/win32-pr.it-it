---
UID: NS:directml.DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
title: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per un'unità lineare rettificata (ReLU).
helpviewer_keywords:
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC, DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.openlocfilehash: dea89f0e3366a07ee98f47703f07e2f5a9d4009d
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803677"
---
# <a name="dml_activation_relu_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="78e10-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="78e10-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="78e10-104">Calcola le sfumature di backpropagation per un'unità lineare rettificata (ReLU).</span><span class="sxs-lookup"><span data-stu-id="78e10-104">Computes backpropagation gradients for a rectified linear unit (ReLU).</span></span> <span data-ttu-id="78e10-105">Questo operatore esegue il calcolo per elemento seguente.</span><span class="sxs-lookup"><span data-stu-id="78e10-105">This operator performs the following element-wise computation.</span></span>

```
X = InputTensor
dY = InputGradientTensor

OutputGradientTensor = (X > 0 ? dY : 0)
```

<span data-ttu-id="78e10-106">L'operatore forward-pass corrispondente è [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="78e10-106">The corresponding forward-pass operator is [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78e10-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="78e10-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="78e10-108">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="78e10-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="78e10-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78e10-109">Syntax</span></span>
```cpp
struct DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
};
```

## <a name="members"></a><span data-ttu-id="78e10-110">Members</span><span class="sxs-lookup"><span data-stu-id="78e10-110">Members</span></span>

`InputTensor`

<span data-ttu-id="78e10-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="78e10-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="78e10-112">Tensore di input (funzionalità).</span><span class="sxs-lookup"><span data-stu-id="78e10-112">The input (feature) tensor.</span></span> <span data-ttu-id="78e10-113">Si tratta in genere dello stesso input fornito durante il passaggio in avanti [(vedere DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="78e10-113">This is typically the same input as was provided during the forward pass (see [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span></span>

`InputGradientTensor`

<span data-ttu-id="78e10-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="78e10-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="78e10-115">Tensore sfumatura in ingresso.</span><span class="sxs-lookup"><span data-stu-id="78e10-115">The incoming gradient tensor.</span></span> <span data-ttu-id="78e10-116">Questa operazione viene in genere ottenuta dall'output della backpropagazione di un livello precedente.</span><span class="sxs-lookup"><span data-stu-id="78e10-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="78e10-117">Le *dimensioni* *e il tipo di* dati di questo tensore devono corrispondere esattamente a quelli di *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="78e10-117">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

`OutputTensor`

<span data-ttu-id="78e10-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="78e10-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="78e10-119">Tensore di output contenente le sfumature backpropagate.</span><span class="sxs-lookup"><span data-stu-id="78e10-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="78e10-120">Le *dimensioni* *e il tipo di* dati di questo tensore devono corrispondere esattamente a quelli di *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="78e10-120">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

## <a name="availability"></a><span data-ttu-id="78e10-121">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="78e10-121">Availability</span></span>
<span data-ttu-id="78e10-122">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="78e10-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="78e10-123">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="78e10-123">Tensor constraints</span></span>
<span data-ttu-id="78e10-124">*InputGradientTensor,* *InputTensor* e *OutputGradientTensor* devono avere gli stessi *valori di DataType,* *DimensionCount* e *Sizes.*</span><span class="sxs-lookup"><span data-stu-id="78e10-124">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="78e10-125">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="78e10-125">Tensor support</span></span>
| <span data-ttu-id="78e10-126">Tensore</span><span class="sxs-lookup"><span data-stu-id="78e10-126">Tensor</span></span> | <span data-ttu-id="78e10-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="78e10-127">Kind</span></span> | <span data-ttu-id="78e10-128">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="78e10-128">Supported dimension counts</span></span> | <span data-ttu-id="78e10-129">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="78e10-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="78e10-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="78e10-130">InputTensor</span></span> | <span data-ttu-id="78e10-131">Input</span><span class="sxs-lookup"><span data-stu-id="78e10-131">Input</span></span> | <span data-ttu-id="78e10-132">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="78e10-132">1 to 8</span></span> | <span data-ttu-id="78e10-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="78e10-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="78e10-134">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="78e10-134">InputGradientTensor</span></span> | <span data-ttu-id="78e10-135">Input</span><span class="sxs-lookup"><span data-stu-id="78e10-135">Input</span></span> | <span data-ttu-id="78e10-136">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="78e10-136">1 to 8</span></span> | <span data-ttu-id="78e10-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="78e10-137">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="78e10-138">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="78e10-138">OutputGradientTensor</span></span> | <span data-ttu-id="78e10-139">Output</span><span class="sxs-lookup"><span data-stu-id="78e10-139">Output</span></span> | <span data-ttu-id="78e10-140">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="78e10-140">1 to 8</span></span> | <span data-ttu-id="78e10-141">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="78e10-141">FLOAT32, FLOAT16</span></span> |

## <a name="see-also"></a><span data-ttu-id="78e10-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78e10-142">See also</span></span>
[<span data-ttu-id="78e10-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="78e10-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)

## <a name="requirements"></a><span data-ttu-id="78e10-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78e10-144">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="78e10-145">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="78e10-145">**Header**</span></span> | <span data-ttu-id="78e10-146">directml.h</span><span class="sxs-lookup"><span data-stu-id="78e10-146">directml.h</span></span> |