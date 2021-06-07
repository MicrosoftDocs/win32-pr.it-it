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
ms.openlocfilehash: 8c70bd4649a57270807ac408802fe07edd36d98e
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417873"
---
# <a name="dml_element_wise_modulus_floor_operator_desc-structure-directmlh"></a><span data-ttu-id="449ef-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="449ef-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="449ef-104">Calcola il modulo, con gli stessi risultati del modulo Python, per ogni coppia di elementi corrispondenti dai tensori di input, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="449ef-104">Computes the modulus, with the same results as the Python modulus, for each pair of corresponding elements from the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="449ef-105">Poiché il quoziente viene arrotondato verso -inf, il risultato avrà lo stesso segno del divisore.</span><span class="sxs-lookup"><span data-stu-id="449ef-105">Because the quotient is rounded towards -inf, the result will have the same sign as the divisor.</span></span>

```
f(a, b) = a - (b * floor(a / b))
```

<span data-ttu-id="449ef-106">Questo operatore supporta l'esecuzione sul posto, vale a dire che *OutputTensor* è autorizzato a creare un alias di uno dei tensori di input durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="449ef-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="449ef-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="449ef-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="449ef-108">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="449ef-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="449ef-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="449ef-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="449ef-110">Members</span><span class="sxs-lookup"><span data-stu-id="449ef-110">Members</span></span>

`ATensor`

<span data-ttu-id="449ef-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="449ef-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="449ef-112">Tensore contenente gli input sul lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="449ef-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="449ef-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="449ef-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="449ef-114">Tensore contenente gli input sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="449ef-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="449ef-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="449ef-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="449ef-116">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="449ef-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="449ef-117">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="449ef-117">Availability</span></span>
<span data-ttu-id="449ef-118">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="449ef-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="449ef-119">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="449ef-119">Tensor constraints</span></span>
<span data-ttu-id="449ef-120">*ATensor,* *BTensor* e *OutputTensor* devono avere gli stessi *valori di DataType,* *DimensionCount* e *Sizes.*</span><span class="sxs-lookup"><span data-stu-id="449ef-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="449ef-121">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="449ef-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="449ef-122">DML_FEATURE_LEVEL_3_0 e successive</span><span class="sxs-lookup"><span data-stu-id="449ef-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="449ef-123">Tensore</span><span class="sxs-lookup"><span data-stu-id="449ef-123">Tensor</span></span> | <span data-ttu-id="449ef-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="449ef-124">Kind</span></span> | <span data-ttu-id="449ef-125">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="449ef-125">Supported dimension counts</span></span> | <span data-ttu-id="449ef-126">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="449ef-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="449ef-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="449ef-127">ATensor</span></span> | <span data-ttu-id="449ef-128">Input</span><span class="sxs-lookup"><span data-stu-id="449ef-128">Input</span></span> | <span data-ttu-id="449ef-129">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="449ef-129">1 to 8</span></span> | <span data-ttu-id="449ef-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="449ef-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="449ef-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="449ef-131">BTensor</span></span> | <span data-ttu-id="449ef-132">Input</span><span class="sxs-lookup"><span data-stu-id="449ef-132">Input</span></span> | <span data-ttu-id="449ef-133">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="449ef-133">1 to 8</span></span> | <span data-ttu-id="449ef-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="449ef-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="449ef-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="449ef-135">OutputTensor</span></span> | <span data-ttu-id="449ef-136">Output</span><span class="sxs-lookup"><span data-stu-id="449ef-136">Output</span></span> | <span data-ttu-id="449ef-137">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="449ef-137">1 to 8</span></span> | <span data-ttu-id="449ef-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="449ef-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="449ef-139">DML_FEATURE_LEVEL_2_1 e successive</span><span class="sxs-lookup"><span data-stu-id="449ef-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="449ef-140">Tensore</span><span class="sxs-lookup"><span data-stu-id="449ef-140">Tensor</span></span> | <span data-ttu-id="449ef-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="449ef-141">Kind</span></span> | <span data-ttu-id="449ef-142">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="449ef-142">Supported dimension counts</span></span> | <span data-ttu-id="449ef-143">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="449ef-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="449ef-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="449ef-144">ATensor</span></span> | <span data-ttu-id="449ef-145">Input</span><span class="sxs-lookup"><span data-stu-id="449ef-145">Input</span></span> | <span data-ttu-id="449ef-146">4</span><span class="sxs-lookup"><span data-stu-id="449ef-146">4</span></span> | <span data-ttu-id="449ef-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="449ef-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="449ef-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="449ef-148">BTensor</span></span> | <span data-ttu-id="449ef-149">Input</span><span class="sxs-lookup"><span data-stu-id="449ef-149">Input</span></span> | <span data-ttu-id="449ef-150">4</span><span class="sxs-lookup"><span data-stu-id="449ef-150">4</span></span> | <span data-ttu-id="449ef-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="449ef-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="449ef-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="449ef-152">OutputTensor</span></span> | <span data-ttu-id="449ef-153">Output</span><span class="sxs-lookup"><span data-stu-id="449ef-153">Output</span></span> | <span data-ttu-id="449ef-154">4</span><span class="sxs-lookup"><span data-stu-id="449ef-154">4</span></span> | <span data-ttu-id="449ef-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="449ef-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="449ef-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="449ef-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="449ef-157">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="449ef-157">**Header**</span></span> | <span data-ttu-id="449ef-158">directml.h</span><span class="sxs-lookup"><span data-stu-id="449ef-158">directml.h</span></span> |