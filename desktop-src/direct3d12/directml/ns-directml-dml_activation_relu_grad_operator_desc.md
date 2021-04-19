---
UID: NS:directml.DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
title: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
description: Calcola le sfumature di propagazione per un'unità lineare rettificata (ReLU).
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
ms.openlocfilehash: 567a1de50c1c91de83a9fda2978f83af8daf1a6e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320303"
---
# <a name="dml_activation_relu_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="41453-103">Struttura DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="41453-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="41453-104">Calcola le sfumature di propagazione per un'unità lineare rettificata (ReLU).</span><span class="sxs-lookup"><span data-stu-id="41453-104">Computes backpropagation gradients for a rectified linear unit (ReLU).</span></span> <span data-ttu-id="41453-105">Questo operatore esegue il seguente calcolo a livello di elemento.</span><span class="sxs-lookup"><span data-stu-id="41453-105">This operator performs the following element-wise computation.</span></span>

```
X = InputTensor
dY = InputGradientTensor

OutputGradientTensor = (X > 0 ? dY : 0)
```

<span data-ttu-id="41453-106">L'operatore di avanzamento passa corrispondente è [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="41453-106">The corresponding forward-pass operator is [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41453-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="41453-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="41453-108">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="41453-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="41453-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41453-109">Syntax</span></span>
```cpp
struct DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
};
```

## <a name="members"></a><span data-ttu-id="41453-110">Members</span><span class="sxs-lookup"><span data-stu-id="41453-110">Members</span></span>

`InputTensor`

<span data-ttu-id="41453-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="41453-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="41453-112">Tensore di input (Feature).</span><span class="sxs-lookup"><span data-stu-id="41453-112">The input (feature) tensor.</span></span> <span data-ttu-id="41453-113">Si tratta in genere dello stesso input fornito durante il passaggio di avanzamento (vedere [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="41453-113">This is typically the same input as was provided during the forward pass (see [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span></span>

`InputGradientTensor`

<span data-ttu-id="41453-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="41453-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="41453-115">Tensore di sfumatura in ingresso.</span><span class="sxs-lookup"><span data-stu-id="41453-115">The incoming gradient tensor.</span></span> <span data-ttu-id="41453-116">Questa operazione viene in genere ottenuta dall'output di propagation di un livello precedente.</span><span class="sxs-lookup"><span data-stu-id="41453-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="41453-117">Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere esattamente a quelli di *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="41453-117">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

`OutputTensor`

<span data-ttu-id="41453-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="41453-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="41453-119">Un tensore di output contenente le sfumature ripropagate.</span><span class="sxs-lookup"><span data-stu-id="41453-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="41453-120">Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere esattamente a quelli di *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="41453-120">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

## <a name="availability"></a><span data-ttu-id="41453-121">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="41453-121">Availability</span></span>
<span data-ttu-id="41453-122">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="41453-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="41453-123">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="41453-123">Tensor constraints</span></span>
<span data-ttu-id="41453-124">*InputGradientTensor*, *InputTensor* e *OutputGradientTensor* devono avere lo stesso *tipo* di dati, *DimensionCount* e *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="41453-124">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="41453-125">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="41453-125">Tensor support</span></span>
| <span data-ttu-id="41453-126">Tensore</span><span class="sxs-lookup"><span data-stu-id="41453-126">Tensor</span></span> | <span data-ttu-id="41453-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="41453-127">Kind</span></span> | <span data-ttu-id="41453-128">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="41453-128">Supported dimension counts</span></span> | <span data-ttu-id="41453-129">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="41453-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="41453-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="41453-130">InputTensor</span></span> | <span data-ttu-id="41453-131">Input</span><span class="sxs-lookup"><span data-stu-id="41453-131">Input</span></span> | <span data-ttu-id="41453-132">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="41453-132">1 to 8</span></span> | <span data-ttu-id="41453-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="41453-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="41453-134">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="41453-134">InputGradientTensor</span></span> | <span data-ttu-id="41453-135">Input</span><span class="sxs-lookup"><span data-stu-id="41453-135">Input</span></span> | <span data-ttu-id="41453-136">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="41453-136">1 to 8</span></span> | <span data-ttu-id="41453-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="41453-137">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="41453-138">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="41453-138">OutputGradientTensor</span></span> | <span data-ttu-id="41453-139">Output</span><span class="sxs-lookup"><span data-stu-id="41453-139">Output</span></span> | <span data-ttu-id="41453-140">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="41453-140">1 to 8</span></span> | <span data-ttu-id="41453-141">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="41453-141">FLOAT32, FLOAT16</span></span> |

## <a name="see-also"></a><span data-ttu-id="41453-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41453-142">See also</span></span>
[<span data-ttu-id="41453-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="41453-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)

## <a name="requirements"></a><span data-ttu-id="41453-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41453-144">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="41453-145">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="41453-145">**Header**</span></span> | <span data-ttu-id="41453-146">directml. h</span><span class="sxs-lookup"><span data-stu-id="41453-146">directml.h</span></span> |