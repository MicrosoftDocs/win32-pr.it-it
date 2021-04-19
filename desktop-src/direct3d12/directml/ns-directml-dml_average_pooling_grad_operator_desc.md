---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Calcola le sfumature di propagazione per il pooling medio (vedere [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: 79a43e93f504e8d6f36553a4f672ef7e5845610f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320295"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="3dff8-103">Struttura DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="3dff8-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="3dff8-104">Calcola le sfumature di propagazione per il pooling medio (vedere [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="3dff8-104">Computes backpropagation gradients for average pooling (see [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span></span>

<span data-ttu-id="3dff8-105">Si consideri un **DML_AVERAGE_POOLING_OPERATOR_DESC** 2x2, senza riempimento e un stride di 1, che esegue le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3dff8-105">Consider a 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, without padding and a stride of 1, that performs the following.</span></span>

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

<span data-ttu-id="3dff8-106">Ogni finestra 2x2 nel tensore di input è media per produrre un elemento dell'output (leggendo gli zeri per gli elementi oltre il bordo).</span><span class="sxs-lookup"><span data-stu-id="3dff8-106">Each 2x2 window in the input tensor is averaged to produce one element of the output (reading zeros for elements beyond the edge).</span></span> <span data-ttu-id="3dff8-107">Di seguito è riportato un esempio dell'output di **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** dati parametri simili.</span><span class="sxs-lookup"><span data-stu-id="3dff8-107">Here's an example of the output of **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** given similar parameters.</span></span>

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

<span data-ttu-id="3dff8-108">Si noti che i valori in *OutputGradientTensor* rappresentano i contributi ponderati di tale elemento al *OutputTensor* durante l'operatore [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) originale.</span><span class="sxs-lookup"><span data-stu-id="3dff8-108">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3dff8-109">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="3dff8-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="3dff8-110">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="3dff8-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3dff8-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3dff8-111">Syntax</span></span>

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a><span data-ttu-id="3dff8-112">Members</span><span class="sxs-lookup"><span data-stu-id="3dff8-112">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="3dff8-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3dff8-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3dff8-114">Tensore di sfumatura in ingresso.</span><span class="sxs-lookup"><span data-stu-id="3dff8-114">The incoming gradient tensor.</span></span> <span data-ttu-id="3dff8-115">Questa operazione viene in genere ottenuta dall'output di propagation di un livello precedente.</span><span class="sxs-lookup"><span data-stu-id="3dff8-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="3dff8-116">In genere, questo tensore avrebbe le stesse dimensioni dell' *output* del [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) corrispondente nel passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="3dff8-116">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="3dff8-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3dff8-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3dff8-118">Un tensore di output contenente le sfumature ripropagate.</span><span class="sxs-lookup"><span data-stu-id="3dff8-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="3dff8-119">In genere, questo tensore avrebbe le stesse dimensioni dell' *input* del [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) corrispondente nel passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="3dff8-119">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="3dff8-120">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="3dff8-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="3dff8-121">Il numero di elementi nelle matrici *Strides*, *WindowSize*, *StartPadding* e *EndPadding* .</span><span class="sxs-lookup"><span data-stu-id="3dff8-121">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="3dff8-122">Questo valore deve essere uguale al numero di dimensioni spaziali.</span><span class="sxs-lookup"><span data-stu-id="3dff8-122">This value must equal the spatial dimension count.</span></span> <span data-ttu-id="3dff8-123">Il numero di dimensioni spaziali è 2 Se vengono forniti i tensori 4D oppure 3 Se vengono forniti i tensori 5D.</span><span class="sxs-lookup"><span data-stu-id="3dff8-123">The spatial dimension count is 2 if 4D tensors are provided, or 3 if 5D tensors are provided.</span></span>

`Strides`

<span data-ttu-id="3dff8-124">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="3dff8-124">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="3dff8-125">Vedere *stride* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="3dff8-125">See *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`WindowSize`

<span data-ttu-id="3dff8-126">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="3dff8-126">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="3dff8-127">Vedere *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="3dff8-127">See *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`StartPadding`

<span data-ttu-id="3dff8-128">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="3dff8-128">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="3dff8-129">Vedere *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="3dff8-129">See *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`EndPadding`

<span data-ttu-id="3dff8-130">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="3dff8-130">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="3dff8-131">Vedere *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="3dff8-131">See *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`IncludePadding`

<span data-ttu-id="3dff8-132">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="3dff8-132">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="3dff8-133">Vedere *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="3dff8-133">See *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="3dff8-134">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="3dff8-134">Availability</span></span>
<span data-ttu-id="3dff8-135">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="3dff8-135">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="3dff8-136">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="3dff8-136">Tensor constraints</span></span>
<span data-ttu-id="3dff8-137">*InputGradientTensor* e *OutputGradientTensor* devono avere lo stesso *tipo* di dati e *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="3dff8-137">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="3dff8-138">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="3dff8-138">Tensor support</span></span>
| <span data-ttu-id="3dff8-139">Tensore</span><span class="sxs-lookup"><span data-stu-id="3dff8-139">Tensor</span></span> | <span data-ttu-id="3dff8-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="3dff8-140">Kind</span></span> | <span data-ttu-id="3dff8-141">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="3dff8-141">Supported dimension counts</span></span> | <span data-ttu-id="3dff8-142">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="3dff8-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="3dff8-143">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="3dff8-143">InputGradientTensor</span></span> | <span data-ttu-id="3dff8-144">Input</span><span class="sxs-lookup"><span data-stu-id="3dff8-144">Input</span></span> | <span data-ttu-id="3dff8-145">da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="3dff8-145">4 to 5</span></span> | <span data-ttu-id="3dff8-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="3dff8-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="3dff8-147">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="3dff8-147">OutputGradientTensor</span></span> | <span data-ttu-id="3dff8-148">Output</span><span class="sxs-lookup"><span data-stu-id="3dff8-148">Output</span></span> | <span data-ttu-id="3dff8-149">da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="3dff8-149">4 to 5</span></span> | <span data-ttu-id="3dff8-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="3dff8-150">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="3dff8-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3dff8-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3dff8-152">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="3dff8-152">**Header**</span></span> | <span data-ttu-id="3dff8-153">directml. h</span><span class="sxs-lookup"><span data-stu-id="3dff8-153">directml.h</span></span> |