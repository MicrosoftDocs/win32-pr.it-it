---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
description: Calcola l'operatore di modulo C per ogni coppia di elementi corrispondenti dei tensori di input, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_modulus_truncate_operator_desc
- directml/DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
ms.openlocfilehash: f7cbfbf8613fb4309c6d336ccd807565d0dae53c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320273"
---
# <a name="dml_element_wise_modulus_truncate_operator_desc-structure-directmlh"></a><span data-ttu-id="8f862-103">Struttura DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="8f862-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="8f862-104">Calcola l'operatore di modulo C per ogni coppia di elementi corrispondenti dei tensori di input, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="8f862-104">Computes the C modulus operator for each pair of corresponding elements of the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="8f862-105">Poiché il quoziente è arrotondato verso 0, il risultato avrà lo stesso segno del dividendo.</span><span class="sxs-lookup"><span data-stu-id="8f862-105">Because the quotient is rounded towards 0, the result will have the same sign as the dividend.</span></span>

```
f(a, b) = a - (b * trunc(a / b))
```

<span data-ttu-id="8f862-106">Questo operatore supporta l'esecuzione sul posto, vale a dire che *OutputTensor* è autorizzato a eseguire l'aliasing di uno dei tensori di input durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="8f862-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f862-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="8f862-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="8f862-108">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="8f862-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f862-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f862-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="8f862-110">Members</span><span class="sxs-lookup"><span data-stu-id="8f862-110">Members</span></span>

`ATensor`

<span data-ttu-id="8f862-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8f862-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8f862-112">Un tensore contenente gli input sul lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="8f862-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="8f862-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8f862-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8f862-114">Un tensore contenente gli input sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="8f862-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="8f862-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8f862-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8f862-116">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="8f862-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="8f862-117">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="8f862-117">Availability</span></span>
<span data-ttu-id="8f862-118">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="8f862-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="8f862-119">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="8f862-119">Tensor constraints</span></span>
<span data-ttu-id="8f862-120">*ATensor*, *BTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati, *DimensionCount* e *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="8f862-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="8f862-121">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="8f862-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="8f862-122">DML_FEATURE_LEVEL_3_0 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="8f862-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="8f862-123">Tensore</span><span class="sxs-lookup"><span data-stu-id="8f862-123">Tensor</span></span> | <span data-ttu-id="8f862-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f862-124">Kind</span></span> | <span data-ttu-id="8f862-125">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="8f862-125">Supported dimension counts</span></span> | <span data-ttu-id="8f862-126">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="8f862-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8f862-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="8f862-127">ATensor</span></span> | <span data-ttu-id="8f862-128">Input</span><span class="sxs-lookup"><span data-stu-id="8f862-128">Input</span></span> | <span data-ttu-id="8f862-129">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="8f862-129">1 to 8</span></span> | <span data-ttu-id="8f862-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8f862-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="8f862-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="8f862-131">BTensor</span></span> | <span data-ttu-id="8f862-132">Input</span><span class="sxs-lookup"><span data-stu-id="8f862-132">Input</span></span> | <span data-ttu-id="8f862-133">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="8f862-133">1 to 8</span></span> | <span data-ttu-id="8f862-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8f862-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="8f862-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8f862-135">OutputTensor</span></span> | <span data-ttu-id="8f862-136">Output</span><span class="sxs-lookup"><span data-stu-id="8f862-136">Output</span></span> | <span data-ttu-id="8f862-137">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="8f862-137">1 to 8</span></span> | <span data-ttu-id="8f862-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8f862-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="8f862-139">DML_FEATURE_LEVEL_2_1 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="8f862-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="8f862-140">Tensore</span><span class="sxs-lookup"><span data-stu-id="8f862-140">Tensor</span></span> | <span data-ttu-id="8f862-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f862-141">Kind</span></span> | <span data-ttu-id="8f862-142">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="8f862-142">Supported dimension counts</span></span> | <span data-ttu-id="8f862-143">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="8f862-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8f862-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="8f862-144">ATensor</span></span> | <span data-ttu-id="8f862-145">Input</span><span class="sxs-lookup"><span data-stu-id="8f862-145">Input</span></span> | <span data-ttu-id="8f862-146">4</span><span class="sxs-lookup"><span data-stu-id="8f862-146">4</span></span> | <span data-ttu-id="8f862-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8f862-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="8f862-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="8f862-148">BTensor</span></span> | <span data-ttu-id="8f862-149">Input</span><span class="sxs-lookup"><span data-stu-id="8f862-149">Input</span></span> | <span data-ttu-id="8f862-150">4</span><span class="sxs-lookup"><span data-stu-id="8f862-150">4</span></span> | <span data-ttu-id="8f862-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8f862-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="8f862-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8f862-152">OutputTensor</span></span> | <span data-ttu-id="8f862-153">Output</span><span class="sxs-lookup"><span data-stu-id="8f862-153">Output</span></span> | <span data-ttu-id="8f862-154">4</span><span class="sxs-lookup"><span data-stu-id="8f862-154">4</span></span> | <span data-ttu-id="8f862-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8f862-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="8f862-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f862-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8f862-157">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="8f862-157">**Header**</span></span> | <span data-ttu-id="8f862-158">directml. h</span><span class="sxs-lookup"><span data-stu-id="8f862-158">directml.h</span></span> |