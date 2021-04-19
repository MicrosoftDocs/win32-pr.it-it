---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
description: Esegue uno spostamento a destra logico di ogni elemento di *ATensor* in base a un numero di bit specificato dall'elemento corrispondente di *BTensor*, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure
- direct3d12.dml_element_wise_bit_shift_right_operator_desc
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
ms.openlocfilehash: 447b0f685b51bf8b146644de3b5f65390a492ffd
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320375"
---
# <a name="dml_element_wise_bit_shift_right_operator_desc-structure-directmlh"></a><span data-ttu-id="31a33-103">Struttura DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="31a33-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="31a33-104">Esegue uno spostamento a destra logico di ogni elemento di *ATensor* in base a un numero di bit specificato dall'elemento corrispondente di *BTensor*, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="31a33-104">Performs a logical right shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >> b)
```

<span data-ttu-id="31a33-105">Questo operatore supporta l'esecuzione sul posto, vale a dire che *OutputTensor* è autorizzato a eseguire l'aliasing di uno dei tensori di input durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="31a33-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31a33-106">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="31a33-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="31a33-107">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="31a33-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="31a33-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31a33-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="31a33-109">Members</span><span class="sxs-lookup"><span data-stu-id="31a33-109">Members</span></span>

`ATensor`

<span data-ttu-id="31a33-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="31a33-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="31a33-111">Un tensore contenente gli input sul lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="31a33-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="31a33-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="31a33-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="31a33-113">Un tensore contenente gli input sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="31a33-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="31a33-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="31a33-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="31a33-115">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="31a33-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="31a33-116">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="31a33-116">Availability</span></span>
<span data-ttu-id="31a33-117">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="31a33-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="31a33-118">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="31a33-118">Tensor constraints</span></span>
<span data-ttu-id="31a33-119">*ATensor*, *BTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati, *DimensionCount* e *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="31a33-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="31a33-120">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="31a33-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="31a33-121">DML_FEATURE_LEVEL_3_0 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="31a33-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="31a33-122">Tensore</span><span class="sxs-lookup"><span data-stu-id="31a33-122">Tensor</span></span> | <span data-ttu-id="31a33-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="31a33-123">Kind</span></span> | <span data-ttu-id="31a33-124">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="31a33-124">Supported dimension counts</span></span> | <span data-ttu-id="31a33-125">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="31a33-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="31a33-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="31a33-126">ATensor</span></span> | <span data-ttu-id="31a33-127">Input</span><span class="sxs-lookup"><span data-stu-id="31a33-127">Input</span></span> | <span data-ttu-id="31a33-128">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="31a33-128">1 to 8</span></span> | <span data-ttu-id="31a33-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="31a33-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="31a33-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="31a33-130">BTensor</span></span> | <span data-ttu-id="31a33-131">Input</span><span class="sxs-lookup"><span data-stu-id="31a33-131">Input</span></span> | <span data-ttu-id="31a33-132">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="31a33-132">1 to 8</span></span> | <span data-ttu-id="31a33-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="31a33-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="31a33-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="31a33-134">OutputTensor</span></span> | <span data-ttu-id="31a33-135">Output</span><span class="sxs-lookup"><span data-stu-id="31a33-135">Output</span></span> | <span data-ttu-id="31a33-136">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="31a33-136">1 to 8</span></span> | <span data-ttu-id="31a33-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="31a33-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="31a33-138">DML_FEATURE_LEVEL_2_1 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="31a33-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="31a33-139">Tensore</span><span class="sxs-lookup"><span data-stu-id="31a33-139">Tensor</span></span> | <span data-ttu-id="31a33-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="31a33-140">Kind</span></span> | <span data-ttu-id="31a33-141">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="31a33-141">Supported dimension counts</span></span> | <span data-ttu-id="31a33-142">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="31a33-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="31a33-143">ATensor</span><span class="sxs-lookup"><span data-stu-id="31a33-143">ATensor</span></span> | <span data-ttu-id="31a33-144">Input</span><span class="sxs-lookup"><span data-stu-id="31a33-144">Input</span></span> | <span data-ttu-id="31a33-145">4</span><span class="sxs-lookup"><span data-stu-id="31a33-145">4</span></span> | <span data-ttu-id="31a33-146">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="31a33-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="31a33-147">BTensor</span><span class="sxs-lookup"><span data-stu-id="31a33-147">BTensor</span></span> | <span data-ttu-id="31a33-148">Input</span><span class="sxs-lookup"><span data-stu-id="31a33-148">Input</span></span> | <span data-ttu-id="31a33-149">4</span><span class="sxs-lookup"><span data-stu-id="31a33-149">4</span></span> | <span data-ttu-id="31a33-150">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="31a33-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="31a33-151">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="31a33-151">OutputTensor</span></span> | <span data-ttu-id="31a33-152">Output</span><span class="sxs-lookup"><span data-stu-id="31a33-152">Output</span></span> | <span data-ttu-id="31a33-153">4</span><span class="sxs-lookup"><span data-stu-id="31a33-153">4</span></span> | <span data-ttu-id="31a33-154">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="31a33-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="31a33-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31a33-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="31a33-156">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="31a33-156">**Header**</span></span> | <span data-ttu-id="31a33-157">directml. h</span><span class="sxs-lookup"><span data-stu-id="31a33-157">directml.h</span></span> |