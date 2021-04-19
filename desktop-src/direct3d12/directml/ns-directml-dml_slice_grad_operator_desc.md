---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Calcola le sfumature di propagazione per slice (vedere [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
helpviewer_keywords:
- DML_SLICE_GRAD_OPERATOR_DESC
- DML_SLICE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_SLICE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_SLICE_GRAD_OPERATOR_DESC, DML_SLICE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
- directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
ms.openlocfilehash: 63ea67454965d976247c3cdd50aa183f6a676138
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320327"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="47bdd-103">Struttura DML_SLICE_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="47bdd-103">DML_SLICE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="47bdd-104">Calcola le sfumature di propagazione per slice (vedere [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="47bdd-104">Computes backpropagation gradients for Slice (see [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span></span>

<span data-ttu-id="47bdd-105">Si ricordi che [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) estrae un'area secondaria di un tensore di input.</span><span class="sxs-lookup"><span data-stu-id="47bdd-105">Recall that [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extracts a subregion of an input tensor.</span></span> <span data-ttu-id="47bdd-106">Dato un *InputGradientTensor* con le stesse dimensioni dell' *output* di un **DML_SLICE1_OPERATOR_DESC** equivalente, questo operatore produce un *OutputGradientTensor* con le stesse dimensioni dell' *input* di **DML_SLICE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="47bdd-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_SLICE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of **DML_SLICE1_OPERATOR_DESC**.</span></span> <span data-ttu-id="47bdd-107">Gli elementi sezionati vengono propagati all'output e tutti gli altri elementi vengono impostati su 0.</span><span class="sxs-lookup"><span data-stu-id="47bdd-107">The sliced elements are propagated to the output, and all other elements are set to 0.</span></span>

<span data-ttu-id="47bdd-108">Si consideri ad esempio un **DML_SLICE1_OPERATOR_DESC** che estrae gli elementi seguenti da un tensore:</span><span class="sxs-lookup"><span data-stu-id="47bdd-108">As an example, consider a **DML_SLICE1_OPERATOR_DESC** that extracts the following elements from a tensor:</span></span>

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

<span data-ttu-id="47bdd-109">Se vengono fornite le stesse dimensioni di *InputWindowOffsets* /  /  come nell'esempio precedente, questo operatore eseguirà la trasformazione seguente.</span><span class="sxs-lookup"><span data-stu-id="47bdd-109">If provided the same *InputWindowOffsets*/*Sizes*/*Strides* as in the above example, this operator would then perform the following transform.</span></span>

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> <span data-ttu-id="47bdd-110">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="47bdd-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="47bdd-111">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="47bdd-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="47bdd-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47bdd-112">Syntax</span></span>

```cpp
struct DML_SLICE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* InputWindowOffsets;
  _Field_size_(DimensionCount) const UINT* InputWindowSizes;
  _Field_size_(DimensionCount) const INT* InputWindowStrides;
};
```

## <a name="members"></a><span data-ttu-id="47bdd-113">Members</span><span class="sxs-lookup"><span data-stu-id="47bdd-113">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="47bdd-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="47bdd-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="47bdd-115">Tensore di sfumatura in ingresso.</span><span class="sxs-lookup"><span data-stu-id="47bdd-115">The incoming gradient tensor.</span></span> <span data-ttu-id="47bdd-116">Questa operazione viene in genere ottenuta dall'output di propagation di un livello precedente.</span><span class="sxs-lookup"><span data-stu-id="47bdd-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="47bdd-117">In genere, questo tensore avrebbe le stesse dimensioni dell' *output* del [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) corrispondente nel passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="47bdd-117">Typically, this tensor would have the same sizes as the *output* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="47bdd-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="47bdd-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="47bdd-119">Un tensore di output contenente le sfumature ripropagate.</span><span class="sxs-lookup"><span data-stu-id="47bdd-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="47bdd-120">In genere, questo tensore avrebbe le stesse dimensioni dell' *input* del [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) corrispondente nel passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="47bdd-120">Typically, this tensor would have the same sizes as the *input* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="47bdd-121">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="47bdd-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="47bdd-122">Il numero di elementi nelle matrici *InputWindowOffsets*, *InputWindowSizes* e *InputWindowStrides* .</span><span class="sxs-lookup"><span data-stu-id="47bdd-122">The number of elements in the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="47bdd-123">Questo valore deve essere uguale a *DimensionCount* specificato in *InputGradientTensor* e *OutputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="47bdd-123">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`InputWindowOffsets`

<span data-ttu-id="47bdd-124">Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="47bdd-124">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="47bdd-125">Vedere *InputWindowOffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="47bdd-125">See *InputWindowOffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowSizes`

<span data-ttu-id="47bdd-126">Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="47bdd-126">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="47bdd-127">Vedere *InputWindowSizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="47bdd-127">See *InputWindowSizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowStrides`

<span data-ttu-id="47bdd-128">Tipo: \_ \_ Dimensione campo \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="47bdd-128">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="47bdd-129">Vedere *InputWindowStrides* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="47bdd-129">See *InputWindowStrides* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

<span data-ttu-id="47bdd-130">Si noti che a differenza di **DML_SLICE1_OPERATOR_DESC**, questo operatore richiede stride diversi da zero.</span><span class="sxs-lookup"><span data-stu-id="47bdd-130">Note that unlike **DML_SLICE1_OPERATOR_DESC**, this operator requires non-zero strides.</span></span> <span data-ttu-id="47bdd-131">Questo è dovuto al fatto che, con uno stride zero, è ambiguo per quale elemento di input deve essere mappato a ogni elemento di output e pertanto non è possibile eseguire la propagazione.</span><span class="sxs-lookup"><span data-stu-id="47bdd-131">That's because with a zero stride, it's ambiguous as to which input element should map to each output element, and therefore backpropagation can't be performed.</span></span> <span data-ttu-id="47bdd-132">Come **DML_SLICE1_OPERATOR_DESC**, gli stride negativi rivolgono la direzione della finestra di input lungo tale asse.</span><span class="sxs-lookup"><span data-stu-id="47bdd-132">Like **DML_SLICE1_OPERATOR_DESC**, negative strides flip the input window direction along that axis.</span></span>

## <a name="availability"></a><span data-ttu-id="47bdd-133">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="47bdd-133">Availability</span></span>
<span data-ttu-id="47bdd-134">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="47bdd-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="47bdd-135">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="47bdd-135">Tensor constraints</span></span>
<span data-ttu-id="47bdd-136">*InputGradientTensor* e *OutputGradientTensor* devono avere lo stesso *tipo* di dati e *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="47bdd-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="47bdd-137">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="47bdd-137">Tensor support</span></span>
| <span data-ttu-id="47bdd-138">Tensore</span><span class="sxs-lookup"><span data-stu-id="47bdd-138">Tensor</span></span> | <span data-ttu-id="47bdd-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="47bdd-139">Kind</span></span> | <span data-ttu-id="47bdd-140">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="47bdd-140">Supported dimension counts</span></span> | <span data-ttu-id="47bdd-141">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="47bdd-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="47bdd-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="47bdd-142">InputGradientTensor</span></span> | <span data-ttu-id="47bdd-143">Input</span><span class="sxs-lookup"><span data-stu-id="47bdd-143">Input</span></span> | <span data-ttu-id="47bdd-144">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="47bdd-144">1 to 8</span></span> | <span data-ttu-id="47bdd-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="47bdd-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="47bdd-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="47bdd-146">OutputGradientTensor</span></span> | <span data-ttu-id="47bdd-147">Output</span><span class="sxs-lookup"><span data-stu-id="47bdd-147">Output</span></span> | <span data-ttu-id="47bdd-148">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="47bdd-148">1 to 8</span></span> | <span data-ttu-id="47bdd-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="47bdd-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="47bdd-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47bdd-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="47bdd-151">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="47bdd-151">**Header**</span></span> | <span data-ttu-id="47bdd-152">directml. h</span><span class="sxs-lookup"><span data-stu-id="47bdd-152">directml.h</span></span> |