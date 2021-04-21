---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
description: Esegue uno spostamento logico a destra di ogni elemento di *ATensor* di un numero di bit specificato dall'elemento corrispondente di *BTensor*, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.
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
ms.openlocfilehash: 5803b40520e3735d24d00eb7260eb527ab857c33
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803195"
---
# <a name="dml_element_wise_bit_shift_right_operator_desc-structure-directmlh"></a><span data-ttu-id="91bc0-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="91bc0-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="91bc0-104">Esegue uno spostamento logico a destra di ogni elemento di *ATensor* di un numero di bit specificato dall'elemento corrispondente di *BTensor*, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="91bc0-104">Performs a logical right shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >> b)
```

<span data-ttu-id="91bc0-105">Questo operatore supporta l'esecuzione sul posto, vale a dire che *OutputTensor* è autorizzato a creare un alias di uno dei tensori di input durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="91bc0-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91bc0-106">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="91bc0-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="91bc0-107">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="91bc0-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="91bc0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91bc0-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="91bc0-109">Members</span><span class="sxs-lookup"><span data-stu-id="91bc0-109">Members</span></span>

`ATensor`

<span data-ttu-id="91bc0-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="91bc0-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="91bc0-111">Tensore contenente gli input sul lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="91bc0-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="91bc0-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="91bc0-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="91bc0-113">Tensore contenente gli input sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="91bc0-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="91bc0-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="91bc0-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="91bc0-115">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="91bc0-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="91bc0-116">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="91bc0-116">Availability</span></span>
<span data-ttu-id="91bc0-117">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="91bc0-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="91bc0-118">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="91bc0-118">Tensor constraints</span></span>
<span data-ttu-id="91bc0-119">*ATensor,* *BTensor* e *OutputTensor* devono avere gli stessi *DataType,* *DimensionCount* e *Sizes*.</span><span class="sxs-lookup"><span data-stu-id="91bc0-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="91bc0-120">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="91bc0-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="91bc0-121">DML_FEATURE_LEVEL_3_0 e successive</span><span class="sxs-lookup"><span data-stu-id="91bc0-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="91bc0-122">Tensore</span><span class="sxs-lookup"><span data-stu-id="91bc0-122">Tensor</span></span> | <span data-ttu-id="91bc0-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="91bc0-123">Kind</span></span> | <span data-ttu-id="91bc0-124">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="91bc0-124">Supported dimension counts</span></span> | <span data-ttu-id="91bc0-125">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="91bc0-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="91bc0-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="91bc0-126">ATensor</span></span> | <span data-ttu-id="91bc0-127">Input</span><span class="sxs-lookup"><span data-stu-id="91bc0-127">Input</span></span> | <span data-ttu-id="91bc0-128">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="91bc0-128">1 to 8</span></span> | <span data-ttu-id="91bc0-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="91bc0-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="91bc0-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="91bc0-130">BTensor</span></span> | <span data-ttu-id="91bc0-131">Input</span><span class="sxs-lookup"><span data-stu-id="91bc0-131">Input</span></span> | <span data-ttu-id="91bc0-132">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="91bc0-132">1 to 8</span></span> | <span data-ttu-id="91bc0-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="91bc0-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="91bc0-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="91bc0-134">OutputTensor</span></span> | <span data-ttu-id="91bc0-135">Output</span><span class="sxs-lookup"><span data-stu-id="91bc0-135">Output</span></span> | <span data-ttu-id="91bc0-136">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="91bc0-136">1 to 8</span></span> | <span data-ttu-id="91bc0-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="91bc0-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="91bc0-138">DML_FEATURE_LEVEL_2_1 e successive</span><span class="sxs-lookup"><span data-stu-id="91bc0-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="91bc0-139">Tensore</span><span class="sxs-lookup"><span data-stu-id="91bc0-139">Tensor</span></span> | <span data-ttu-id="91bc0-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="91bc0-140">Kind</span></span> | <span data-ttu-id="91bc0-141">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="91bc0-141">Supported dimension counts</span></span> | <span data-ttu-id="91bc0-142">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="91bc0-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="91bc0-143">ATensor</span><span class="sxs-lookup"><span data-stu-id="91bc0-143">ATensor</span></span> | <span data-ttu-id="91bc0-144">Input</span><span class="sxs-lookup"><span data-stu-id="91bc0-144">Input</span></span> | <span data-ttu-id="91bc0-145">4</span><span class="sxs-lookup"><span data-stu-id="91bc0-145">4</span></span> | <span data-ttu-id="91bc0-146">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="91bc0-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="91bc0-147">BTensor</span><span class="sxs-lookup"><span data-stu-id="91bc0-147">BTensor</span></span> | <span data-ttu-id="91bc0-148">Input</span><span class="sxs-lookup"><span data-stu-id="91bc0-148">Input</span></span> | <span data-ttu-id="91bc0-149">4</span><span class="sxs-lookup"><span data-stu-id="91bc0-149">4</span></span> | <span data-ttu-id="91bc0-150">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="91bc0-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="91bc0-151">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="91bc0-151">OutputTensor</span></span> | <span data-ttu-id="91bc0-152">Output</span><span class="sxs-lookup"><span data-stu-id="91bc0-152">Output</span></span> | <span data-ttu-id="91bc0-153">4</span><span class="sxs-lookup"><span data-stu-id="91bc0-153">4</span></span> | <span data-ttu-id="91bc0-154">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="91bc0-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="91bc0-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91bc0-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="91bc0-156">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="91bc0-156">**Header**</span></span> | <span data-ttu-id="91bc0-157">directml.h</span><span class="sxs-lookup"><span data-stu-id="91bc0-157">directml.h</span></span> |