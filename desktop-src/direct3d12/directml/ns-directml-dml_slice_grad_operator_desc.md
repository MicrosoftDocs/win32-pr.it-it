---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Calcola le sfumature di backpropagation per Slice (vedere [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
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
ms.openlocfilehash: a22efe9b0b74f5fdc7b498b97784086f40f243b9
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417654"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="f1a7d-103">DML_SLICE_GRAD_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="f1a7d-103">DML_SLICE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="f1a7d-104">Calcola le sfumature di backpropagation per Slice (vedere [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="f1a7d-104">Computes backpropagation gradients for Slice (see [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span></span>

<span data-ttu-id="f1a7d-105">Tenere presente [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) estrae una sottoarea di un tensore di input.</span><span class="sxs-lookup"><span data-stu-id="f1a7d-105">Recall that [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extracts a subregion of an input tensor.</span></span> <span data-ttu-id="f1a7d-106">Dato un *InputGradientTensor* con le stesse dimensioni *dell'output* di un **DML_SLICE1_OPERATOR_DESC equivalente,** questo operatore produce un *OutputGradientTensor* con le stesse dimensioni dell'input di **DML_SLICE1_OPERATOR_DESC**. </span><span class="sxs-lookup"><span data-stu-id="f1a7d-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_SLICE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of **DML_SLICE1_OPERATOR_DESC**.</span></span> <span data-ttu-id="f1a7d-107">Gli elementi sezionati vengono propagati all'output e tutti gli altri elementi vengono impostati su 0.</span><span class="sxs-lookup"><span data-stu-id="f1a7d-107">The sliced elements are propagated to the output, and all other elements are set to 0.</span></span>

<span data-ttu-id="f1a7d-108">Si consideri ad esempio un **DML_SLICE1_OPERATOR_DESC** che estrae gli elementi seguenti da un tensore:</span><span class="sxs-lookup"><span data-stu-id="f1a7d-108">As an example, consider a **DML_SLICE1_OPERATOR_DESC** that extracts the following elements from a tensor:</span></span>

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

<span data-ttu-id="f1a7d-109">Se si specificano gli stessi stride di dimensioni di *InputWindowOffsets* dell'esempio precedente, questo /  /  operatore eseguirà la trasformazione seguente.</span><span class="sxs-lookup"><span data-stu-id="f1a7d-109">If provided the same *InputWindowOffsets*/*Sizes*/*Strides* as in the above example, this operator would then perform the following transform.</span></span>

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> <span data-ttu-id="f1a7d-110">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="f1a7d-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f1a7d-111">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="f1a7d-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1a7d-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1a7d-112">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="f1a7d-113">Members</span><span class="sxs-lookup"><span data-stu-id="f1a7d-113">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="f1a7d-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f1a7d-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f1a7d-115">Tensore sfumatura in ingresso.</span><span class="sxs-lookup"><span data-stu-id="f1a7d-115">The incoming gradient tensor.</span></span> <span data-ttu-id="f1a7d-116">Questa operazione viene in genere ottenuta dall'output della retropropagazione di un livello precedente.</span><span class="sxs-lookup"><span data-stu-id="f1a7d-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="f1a7d-117">In genere, questo tensore avrebbe le stesse dimensioni *dell'output* del DML_SLICE1_OPERATOR_DESC [corrispondente](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) nel passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="f1a7d-117">Typically, this tensor would have the same sizes as the *output* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="f1a7d-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f1a7d-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f1a7d-119">Tensore di output contenente le sfumature di backpropagated.</span><span class="sxs-lookup"><span data-stu-id="f1a7d-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="f1a7d-120">In genere, questo tensore avrebbe le stesse dimensioni *dell'input* del valore [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) nel passaggio in avanti.</span><span class="sxs-lookup"><span data-stu-id="f1a7d-120">Typically, this tensor would have the same sizes as the *input* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="f1a7d-121">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f1a7d-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="f1a7d-122">Numero di elementi nelle matrici *InputWindowOffsets,* *InputWindowSizes* e *InputWindowStrides.*</span><span class="sxs-lookup"><span data-stu-id="f1a7d-122">The number of elements in the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="f1a7d-123">Questo valore deve essere uguale *a DimensionCount* specificato in *InputGradientTensor* e *OutputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="f1a7d-123">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`InputWindowOffsets`

<span data-ttu-id="f1a7d-124">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="f1a7d-124">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="f1a7d-125">Vedere *InputWindowOffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="f1a7d-125">See *InputWindowOffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowSizes`

<span data-ttu-id="f1a7d-126">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="f1a7d-126">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="f1a7d-127">Vedere *InputWindowSizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="f1a7d-127">See *InputWindowSizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowStrides`

<span data-ttu-id="f1a7d-128">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="f1a7d-128">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="f1a7d-129">Vedere *InputWindowStrides* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="f1a7d-129">See *InputWindowStrides* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

<span data-ttu-id="f1a7d-130">Si noti che **a DML_SLICE1_OPERATOR_DESC**, questo operatore richiede stride diversi da zero.</span><span class="sxs-lookup"><span data-stu-id="f1a7d-130">Note that unlike **DML_SLICE1_OPERATOR_DESC**, this operator requires non-zero strides.</span></span> <span data-ttu-id="f1a7d-131">Ciò è dovuto al fatto che con uno stride zero, è ambiguo l'elemento di input di cui eseguire il mapping a ogni elemento di output e pertanto non è possibile eseguire la backpropagation.</span><span class="sxs-lookup"><span data-stu-id="f1a7d-131">That's because with a zero stride, it's ambiguous as to which input element should map to each output element, and therefore backpropagation can't be performed.</span></span> <span data-ttu-id="f1a7d-132">Come **DML_SLICE1_OPERATOR_DESC**, gli stride negativi capovolgeno la direzione della finestra di input lungo tale asse.</span><span class="sxs-lookup"><span data-stu-id="f1a7d-132">Like **DML_SLICE1_OPERATOR_DESC**, negative strides flip the input window direction along that axis.</span></span>

## <a name="availability"></a><span data-ttu-id="f1a7d-133">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="f1a7d-133">Availability</span></span>
<span data-ttu-id="f1a7d-134">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="f1a7d-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f1a7d-135">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="f1a7d-135">Tensor constraints</span></span>
<span data-ttu-id="f1a7d-136">*InputGradientTensor* e *OutputGradientTensor* devono avere gli stessi *valori di DataType* *e DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="f1a7d-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f1a7d-137">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="f1a7d-137">Tensor support</span></span>
| <span data-ttu-id="f1a7d-138">Tensore</span><span class="sxs-lookup"><span data-stu-id="f1a7d-138">Tensor</span></span> | <span data-ttu-id="f1a7d-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1a7d-139">Kind</span></span> | <span data-ttu-id="f1a7d-140">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="f1a7d-140">Supported dimension counts</span></span> | <span data-ttu-id="f1a7d-141">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="f1a7d-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f1a7d-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="f1a7d-142">InputGradientTensor</span></span> | <span data-ttu-id="f1a7d-143">Input</span><span class="sxs-lookup"><span data-stu-id="f1a7d-143">Input</span></span> | <span data-ttu-id="f1a7d-144">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="f1a7d-144">1 to 8</span></span> | <span data-ttu-id="f1a7d-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f1a7d-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="f1a7d-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="f1a7d-146">OutputGradientTensor</span></span> | <span data-ttu-id="f1a7d-147">Output</span><span class="sxs-lookup"><span data-stu-id="f1a7d-147">Output</span></span> | <span data-ttu-id="f1a7d-148">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="f1a7d-148">1 to 8</span></span> | <span data-ttu-id="f1a7d-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f1a7d-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="f1a7d-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1a7d-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f1a7d-151">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="f1a7d-151">**Header**</span></span> | <span data-ttu-id="f1a7d-152">directml.h</span><span class="sxs-lookup"><span data-stu-id="f1a7d-152">directml.h</span></span> |