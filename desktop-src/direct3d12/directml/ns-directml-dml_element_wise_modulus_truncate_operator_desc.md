---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
description: Calcola l'operatore modulo C per ogni coppia di elementi corrispondenti dei tensori di input, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.
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
ms.openlocfilehash: 461a7882e17d86b25cf27e0a28c05673f8899cea
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417615"
---
# <a name="dml_element_wise_modulus_truncate_operator_desc-structure-directmlh"></a><span data-ttu-id="39289-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="39289-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="39289-104">Calcola l'operatore modulo C per ogni coppia di elementi corrispondenti dei tensori di input, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="39289-104">Computes the C modulus operator for each pair of corresponding elements of the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="39289-105">Poiché il quoziente viene arrotondato verso 0, il risultato avrà lo stesso segno del dividendo.</span><span class="sxs-lookup"><span data-stu-id="39289-105">Because the quotient is rounded towards 0, the result will have the same sign as the dividend.</span></span>

```
f(a, b) = a - (b * trunc(a / b))
```

<span data-ttu-id="39289-106">Questo operatore supporta l'esecuzione sul posto, vale a dire che *OutputTensor* è autorizzato a creare un alias di uno dei tensori di input durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="39289-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39289-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="39289-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="39289-108">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="39289-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="39289-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39289-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="39289-110">Members</span><span class="sxs-lookup"><span data-stu-id="39289-110">Members</span></span>

`ATensor`

<span data-ttu-id="39289-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="39289-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="39289-112">Tensore contenente gli input sul lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="39289-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="39289-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="39289-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="39289-114">Tensore contenente gli input sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="39289-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="39289-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="39289-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="39289-116">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="39289-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="39289-117">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="39289-117">Availability</span></span>
<span data-ttu-id="39289-118">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="39289-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="39289-119">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="39289-119">Tensor constraints</span></span>
<span data-ttu-id="39289-120">*ATensor,* *BTensor* e *OutputTensor* devono avere gli stessi *valori di DataType,* *DimensionCount* e *Sizes.*</span><span class="sxs-lookup"><span data-stu-id="39289-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="39289-121">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="39289-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="39289-122">DML_FEATURE_LEVEL_3_0 e successive</span><span class="sxs-lookup"><span data-stu-id="39289-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="39289-123">Tensore</span><span class="sxs-lookup"><span data-stu-id="39289-123">Tensor</span></span> | <span data-ttu-id="39289-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="39289-124">Kind</span></span> | <span data-ttu-id="39289-125">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="39289-125">Supported dimension counts</span></span> | <span data-ttu-id="39289-126">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="39289-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="39289-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="39289-127">ATensor</span></span> | <span data-ttu-id="39289-128">Input</span><span class="sxs-lookup"><span data-stu-id="39289-128">Input</span></span> | <span data-ttu-id="39289-129">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="39289-129">1 to 8</span></span> | <span data-ttu-id="39289-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="39289-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="39289-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="39289-131">BTensor</span></span> | <span data-ttu-id="39289-132">Input</span><span class="sxs-lookup"><span data-stu-id="39289-132">Input</span></span> | <span data-ttu-id="39289-133">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="39289-133">1 to 8</span></span> | <span data-ttu-id="39289-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="39289-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="39289-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="39289-135">OutputTensor</span></span> | <span data-ttu-id="39289-136">Output</span><span class="sxs-lookup"><span data-stu-id="39289-136">Output</span></span> | <span data-ttu-id="39289-137">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="39289-137">1 to 8</span></span> | <span data-ttu-id="39289-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="39289-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="39289-139">DML_FEATURE_LEVEL_2_1 e successive</span><span class="sxs-lookup"><span data-stu-id="39289-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="39289-140">Tensore</span><span class="sxs-lookup"><span data-stu-id="39289-140">Tensor</span></span> | <span data-ttu-id="39289-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="39289-141">Kind</span></span> | <span data-ttu-id="39289-142">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="39289-142">Supported dimension counts</span></span> | <span data-ttu-id="39289-143">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="39289-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="39289-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="39289-144">ATensor</span></span> | <span data-ttu-id="39289-145">Input</span><span class="sxs-lookup"><span data-stu-id="39289-145">Input</span></span> | <span data-ttu-id="39289-146">4</span><span class="sxs-lookup"><span data-stu-id="39289-146">4</span></span> | <span data-ttu-id="39289-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="39289-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="39289-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="39289-148">BTensor</span></span> | <span data-ttu-id="39289-149">Input</span><span class="sxs-lookup"><span data-stu-id="39289-149">Input</span></span> | <span data-ttu-id="39289-150">4</span><span class="sxs-lookup"><span data-stu-id="39289-150">4</span></span> | <span data-ttu-id="39289-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="39289-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="39289-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="39289-152">OutputTensor</span></span> | <span data-ttu-id="39289-153">Output</span><span class="sxs-lookup"><span data-stu-id="39289-153">Output</span></span> | <span data-ttu-id="39289-154">4</span><span class="sxs-lookup"><span data-stu-id="39289-154">4</span></span> | <span data-ttu-id="39289-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="39289-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="39289-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39289-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="39289-157">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="39289-157">**Header**</span></span> | <span data-ttu-id="39289-158">directml.h</span><span class="sxs-lookup"><span data-stu-id="39289-158">directml.h</span></span> |