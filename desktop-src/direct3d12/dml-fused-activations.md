---
title: Utilizzo di operatori con fusibile per migliorare le prestazioni
description: Alcuni operatori DirectML supportano un concetto noto come *Fusion*. Operator Fusion è un modo per migliorare le prestazioni unendo un operatore (in genere una funzione di attivazione) in un operatore diverso in modo che vengano eseguiti insieme senza richiedere un round trip alla memoria.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: b692727d52e252bb3752573e692bcf5beda794e2
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548912"
---
# <a name="using-fused-operators-to-improve-performance"></a><span data-ttu-id="5b61d-104">Utilizzo di operatori con fusibile per migliorare le prestazioni</span><span class="sxs-lookup"><span data-stu-id="5b61d-104">Using fused operators to improve performance</span></span>

<span data-ttu-id="5b61d-105">Alcuni operatori DirectML supportano un concetto noto come *Fusion*.</span><span class="sxs-lookup"><span data-stu-id="5b61d-105">Some DirectML operators support a concept known as *fusion*.</span></span> <span data-ttu-id="5b61d-106">Operator Fusion è un modo per migliorare le prestazioni unendo un operatore (in genere una funzione di attivazione) in un operatore diverso in modo che vengano eseguiti insieme senza richiedere un round trip alla memoria.</span><span class="sxs-lookup"><span data-stu-id="5b61d-106">Operator fusion is a way to improve performance by merging one operator (typically, an activation function) into a different operator so that they are executed together without requiring a roundtrip to memory.</span></span>

## <a name="when-to-fuse-activations"></a><span data-ttu-id="5b61d-107">Quando è possibile fondere le attivazioni</span><span class="sxs-lookup"><span data-stu-id="5b61d-107">When to fuse activations</span></span>

<span data-ttu-id="5b61d-108">Le attivazioni fuse sono un'ottimizzazione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5b61d-108">Fused activations are a performance optimization.</span></span> <span data-ttu-id="5b61d-109">Uno scenario estremamente comune in molti modelli di Machine Learning (ML) consiste nell'applicare una non linearità (funzione di attivazione) all'output di ogni livello nel modello.</span><span class="sxs-lookup"><span data-stu-id="5b61d-109">An extremely common scenario in many machine learning (ML) models is to apply a nonlinearity (an activation function) to the output of each layer in the model.</span></span>

<span data-ttu-id="5b61d-110">In genere, è necessario un round trip alla memoria grafica.</span><span class="sxs-lookup"><span data-stu-id="5b61d-110">Ordinarily, this requires a roundtrip to graphics memory.</span></span> <span data-ttu-id="5b61d-111">Se, ad esempio, una convoluzione è seguita da un'attivazione relu non fusa, la GPU deve attendere che i risultati della convoluzione vengano scritti nella memoria GPU prima di poter iniziare a calcolare il livello di attivazione di relu.</span><span class="sxs-lookup"><span data-stu-id="5b61d-111">For example if a Convolution is followed by a non-fused Relu activation, then the GPU must wait for the results of the Convolution to be written into GPU memory before it can begin computing the Relu activation layer.</span></span> <span data-ttu-id="5b61d-112">Poiché il carico di lavoro di calcolo della maggior parte delle funzioni di attivazione tende a essere ridotto, questo round trip alla memoria grafica può costituire un collo di bottiglia delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5b61d-112">As the compute workload of most activation functions tends to be small, this roundtrip to graphics memory can be a major performance bottleneck.</span></span>

<span data-ttu-id="5b61d-113">Operator Fusion consente la funzione di attivazione (relu nell'esempio precedente) da eseguire come parte dell'operatore precedente (ad esempio, convoluzione).</span><span class="sxs-lookup"><span data-stu-id="5b61d-113">Operator fusion allows the activation function (Relu in the above example) to be performed as part of the preceding operator (Convolution, for example).</span></span> <span data-ttu-id="5b61d-114">Questo consente alla GPU di calcolare la funzione di attivazione senza attendere che i risultati dell'operatore precedente vengano scritti in memoria &mdash; e che migliorino le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5b61d-114">This allows the GPU to compute the activation function without waiting for the results of the preceding operator to be written into memory&mdash;and that improves performance.</span></span>

<span data-ttu-id="5b61d-115">Poiché le attivazioni fuse producono lo stesso risultato, ma sono più veloci in molti casi, è consigliabile eliminare i livelli di attivazione fondendoli nell'operatore precedente laddove possibile.</span><span class="sxs-lookup"><span data-stu-id="5b61d-115">Because fused activations produce the same result, but are faster in many cases, we recommend that you eliminate activation layers by fusing them into their preceding operator wherever possible.</span></span>

## <a name="how-to-fuse-activations"></a><span data-ttu-id="5b61d-116">Come fondere le attivazioni</span><span class="sxs-lookup"><span data-stu-id="5b61d-116">How to fuse activations</span></span>

<span data-ttu-id="5b61d-117">Gli operatori che supportano le attivazioni fuse hanno un parametro facoltativo aggiuntivo nel rispettivo struct operator, `const DML_OPERATOR_DESC* FusedActivation` .</span><span class="sxs-lookup"><span data-stu-id="5b61d-117">Operators that support fused activations have an additional optional parameter in their operator struct, `const DML_OPERATOR_DESC* FusedActivation`.</span></span> <span data-ttu-id="5b61d-118">La convoluzione, ad esempio, supporta l'attivazione con fusibile e un *FusedActivation* corrispondente nella descrizione dell'operatore (vedere [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="5b61d-118">Convolution, for example, supports fused activation, and it has a corresponding *FusedActivation* in its operator description (see [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span></span>

```cpp
struct DML_CONVOLUTION_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* FilterTensor;
    \_Maybenull\_ const DML_TENSOR_DESC* BiasTensor;
    const DML_TENSOR_DESC* OutputTensor;
    DML_CONVOLUTION_MODE Mode;
    DML_CONVOLUTION_DIRECTION Direction;
    UINT DimensionCount;
    _Field_size_(DimensionCount) const UINT* Strides;
    _Field_size_(DimensionCount) const UINT* Dilations;
    _Field_size_(DimensionCount) const UINT* StartPadding;
    _Field_size_(DimensionCount) const UINT* EndPadding;
    _Field_size_(DimensionCount) const UINT* OutputPadding;
    UINT GroupCount;
    \_Maybenull\_ const DML_OPERATOR_DESC* FusedActivation;
};
```

<span data-ttu-id="5b61d-119">Per fondere un'attivazione, costruire un [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) che descriva il tipo di attivazione da fondere.</span><span class="sxs-lookup"><span data-stu-id="5b61d-119">To fuse an activation, construct a [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) that describes the type of activation to be fused.</span></span> <span data-ttu-id="5b61d-120">Ad esempio, per fondere una funzione Relu, il tipo di operatore corretto verrebbe [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="5b61d-120">For example to fuse a Relu function, the correct operator type would be [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

> [!NOTE]
> <span data-ttu-id="5b61d-121">Quando si crea la descrizione dell'operatore per la funzione di attivazione, è necessario impostare i parametri *InputTensor* e *OutputTensor* per la funzione Activation su **null**.</span><span class="sxs-lookup"><span data-stu-id="5b61d-121">When constructing the operator description for the activation function, you must set the *InputTensor* and *OutputTensor* parameters for the activation function to **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="5b61d-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="5b61d-122">Example</span></span>

```cpp
DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC leakyReluDesc;
leakyReluDesc.InputTensor = nullptr;
leakyReluDesc.OutputTensor = nullptr;
leakyReluDesc.Alpha = 0.01f;

DML_OPERATOR_DESC activationDesc = { DML_OPERATOR_ACTIVATION_LEAKY_RELU, &leakyReluDesc };

DML_CONVOLUTION_OPERATOR_DESC convDesc;
// ...
convDesc.FusedActivation = &activationDesc;
```

<span data-ttu-id="5b61d-123">Per un esempio completo, l'esempio [DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples) usa attivazioni fuse per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5b61d-123">For a complete example, the [DirectMLSuperResolution sample](https://github.com/microsoft/DirectML/tree/master/Samples) utilizes fused activations to improve performance.</span></span>

## <a name="operators-that-support-fused-activation"></a><span data-ttu-id="5b61d-124">Operatori che supportano l'attivazione con fusibile</span><span class="sxs-lookup"><span data-stu-id="5b61d-124">Operators that support fused activation</span></span>

* [<span data-ttu-id="5b61d-125">DML_OPERATOR_CONVOLUTION</span><span class="sxs-lookup"><span data-stu-id="5b61d-125">DML_OPERATOR_CONVOLUTION</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="5b61d-126">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="5b61d-126">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="5b61d-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="5b61d-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="5b61d-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** e **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="5b61d-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** and **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="5b61d-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="5b61d-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>

## <a name="activations-that-are-supported-for-fusion"></a><span data-ttu-id="5b61d-130">Attivazioni supportate per Fusion</span><span class="sxs-lookup"><span data-stu-id="5b61d-130">Activations that are supported for fusion</span></span>

* [<span data-ttu-id="5b61d-131">DML_OPERATOR_ACTIVATION_ELU</span><span class="sxs-lookup"><span data-stu-id="5b61d-131">DML_OPERATOR_ACTIVATION_ELU</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="5b61d-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="5b61d-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span></span>
* <span data-ttu-id="5b61d-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="5b61d-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span></span>
* <span data-ttu-id="5b61d-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span><span class="sxs-lookup"><span data-stu-id="5b61d-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span></span>
* <span data-ttu-id="5b61d-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="5b61d-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span></span>
* <span data-ttu-id="5b61d-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="5b61d-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span></span>
* <span data-ttu-id="5b61d-137">**DML_OPERATOR_ACTIVATION_RELU**</span><span class="sxs-lookup"><span data-stu-id="5b61d-137">**DML_OPERATOR_ACTIVATION_RELU**</span></span>
* <span data-ttu-id="5b61d-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span><span class="sxs-lookup"><span data-stu-id="5b61d-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span></span>
* <span data-ttu-id="5b61d-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span><span class="sxs-lookup"><span data-stu-id="5b61d-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span></span>
* <span data-ttu-id="5b61d-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="5b61d-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span></span>
* <span data-ttu-id="5b61d-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="5b61d-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span></span>
* <span data-ttu-id="5b61d-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span><span class="sxs-lookup"><span data-stu-id="5b61d-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span></span>
* <span data-ttu-id="5b61d-143">**DML_OPERATOR_ACTIVATION_TANH**</span><span class="sxs-lookup"><span data-stu-id="5b61d-143">**DML_OPERATOR_ACTIVATION_TANH**</span></span>
* <span data-ttu-id="5b61d-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span><span class="sxs-lookup"><span data-stu-id="5b61d-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span></span>
* <span data-ttu-id="5b61d-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="5b61d-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="5b61d-146">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="5b61d-146">**DML_OPERATOR_ACTIVATION_CELU**</span></span>

<span data-ttu-id="5b61d-147">Gli operatori non inclusi nell'elenco non sono supportati per l'attivazione con fusione.</span><span class="sxs-lookup"><span data-stu-id="5b61d-147">Any operators not in this list are not supported for fused activation.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b61d-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b61d-148">See also</span></span>

<span data-ttu-id="5b61d-149">[Esempio DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples)  </span><span class="sxs-lookup"><span data-stu-id="5b61d-149">[DirectMLSuperResolution sample](https://github.com/microsoft/DirectML/tree/master/Samples)  </span></span>  
[<span data-ttu-id="5b61d-150">DML_CONVOLUTION_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="5b61d-150">DML_CONVOLUTION_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
