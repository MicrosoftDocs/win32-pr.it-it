---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
description: Calcola il modulo, con gli stessi risultati del modulo Python, per ogni coppia di elementi corrispondenti dai tensori di input, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure
- direct3d12.dml_element_wise_modulus_floor_operator_desc
- directml/DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
ms.openlocfilehash: a732a593fb10a5c8e18ec6dd9416ce8d62f43563
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320272"
---
# <a name="dml_element_wise_modulus_floor_operator_desc-structure-directmlh"></a><span data-ttu-id="fdbcd-103">Struttura DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="fdbcd-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="fdbcd-104">Calcola il modulo, con gli stessi risultati del modulo Python, per ogni coppia di elementi corrispondenti dai tensori di input, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="fdbcd-104">Computes the modulus, with the same results as the Python modulus, for each pair of corresponding elements from the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="fdbcd-105">Poiché il quoziente è arrotondato verso-inf, il risultato avrà lo stesso segno del divisore.</span><span class="sxs-lookup"><span data-stu-id="fdbcd-105">Because the quotient is rounded towards -inf, the result will have the same sign as the divisor.</span></span>

```
f(a, b) = a - (b * floor(a / b))
```

<span data-ttu-id="fdbcd-106">Questo operatore supporta l'esecuzione sul posto, vale a dire che *OutputTensor* è autorizzato a eseguire l'aliasing di uno dei tensori di input durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="fdbcd-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fdbcd-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="fdbcd-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="fdbcd-108">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="fdbcd-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fdbcd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fdbcd-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="fdbcd-110">Members</span><span class="sxs-lookup"><span data-stu-id="fdbcd-110">Members</span></span>

`ATensor`

<span data-ttu-id="fdbcd-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fdbcd-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fdbcd-112">Un tensore contenente gli input sul lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="fdbcd-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="fdbcd-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fdbcd-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fdbcd-114">Un tensore contenente gli input sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="fdbcd-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="fdbcd-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fdbcd-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fdbcd-116">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="fdbcd-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="fdbcd-117">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="fdbcd-117">Availability</span></span>
<span data-ttu-id="fdbcd-118">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="fdbcd-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="fdbcd-119">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="fdbcd-119">Tensor constraints</span></span>
<span data-ttu-id="fdbcd-120">*ATensor*, *BTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati, *DimensionCount* e *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="fdbcd-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="fdbcd-121">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="fdbcd-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="fdbcd-122">DML_FEATURE_LEVEL_3_0 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="fdbcd-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="fdbcd-123">Tensore</span><span class="sxs-lookup"><span data-stu-id="fdbcd-123">Tensor</span></span> | <span data-ttu-id="fdbcd-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="fdbcd-124">Kind</span></span> | <span data-ttu-id="fdbcd-125">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="fdbcd-125">Supported dimension counts</span></span> | <span data-ttu-id="fdbcd-126">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="fdbcd-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fdbcd-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="fdbcd-127">ATensor</span></span> | <span data-ttu-id="fdbcd-128">Input</span><span class="sxs-lookup"><span data-stu-id="fdbcd-128">Input</span></span> | <span data-ttu-id="fdbcd-129">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="fdbcd-129">1 to 8</span></span> | <span data-ttu-id="fdbcd-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fdbcd-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fdbcd-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="fdbcd-131">BTensor</span></span> | <span data-ttu-id="fdbcd-132">Input</span><span class="sxs-lookup"><span data-stu-id="fdbcd-132">Input</span></span> | <span data-ttu-id="fdbcd-133">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="fdbcd-133">1 to 8</span></span> | <span data-ttu-id="fdbcd-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fdbcd-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fdbcd-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="fdbcd-135">OutputTensor</span></span> | <span data-ttu-id="fdbcd-136">Output</span><span class="sxs-lookup"><span data-stu-id="fdbcd-136">Output</span></span> | <span data-ttu-id="fdbcd-137">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="fdbcd-137">1 to 8</span></span> | <span data-ttu-id="fdbcd-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fdbcd-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="fdbcd-139">DML_FEATURE_LEVEL_2_1 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="fdbcd-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="fdbcd-140">Tensore</span><span class="sxs-lookup"><span data-stu-id="fdbcd-140">Tensor</span></span> | <span data-ttu-id="fdbcd-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="fdbcd-141">Kind</span></span> | <span data-ttu-id="fdbcd-142">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="fdbcd-142">Supported dimension counts</span></span> | <span data-ttu-id="fdbcd-143">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="fdbcd-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fdbcd-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="fdbcd-144">ATensor</span></span> | <span data-ttu-id="fdbcd-145">Input</span><span class="sxs-lookup"><span data-stu-id="fdbcd-145">Input</span></span> | <span data-ttu-id="fdbcd-146">4</span><span class="sxs-lookup"><span data-stu-id="fdbcd-146">4</span></span> | <span data-ttu-id="fdbcd-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fdbcd-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fdbcd-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="fdbcd-148">BTensor</span></span> | <span data-ttu-id="fdbcd-149">Input</span><span class="sxs-lookup"><span data-stu-id="fdbcd-149">Input</span></span> | <span data-ttu-id="fdbcd-150">4</span><span class="sxs-lookup"><span data-stu-id="fdbcd-150">4</span></span> | <span data-ttu-id="fdbcd-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fdbcd-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fdbcd-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="fdbcd-152">OutputTensor</span></span> | <span data-ttu-id="fdbcd-153">Output</span><span class="sxs-lookup"><span data-stu-id="fdbcd-153">Output</span></span> | <span data-ttu-id="fdbcd-154">4</span><span class="sxs-lookup"><span data-stu-id="fdbcd-154">4</span></span> | <span data-ttu-id="fdbcd-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fdbcd-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="fdbcd-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdbcd-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fdbcd-157">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="fdbcd-157">**Header**</span></span> | <span data-ttu-id="fdbcd-158">directml. h</span><span class="sxs-lookup"><span data-stu-id="fdbcd-158">directml.h</span></span> |