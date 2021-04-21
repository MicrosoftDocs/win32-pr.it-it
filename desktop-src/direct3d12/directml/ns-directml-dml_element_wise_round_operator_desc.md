---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: Arrotonda ogni elemento di *InputTensor* a un valore intero, inserendo il risultato nell'elemento corrispondente di *OutputTensor.*
helpviewer_keywords:
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure
- direct3d12.dml_element_wise_round_operator_desc
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
ms.openlocfilehash: cb9414d0c3e628fa95784480c7402b242d12095b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803051"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a><span data-ttu-id="55e95-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="55e95-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="55e95-104">Arrotonda ogni elemento di *InputTensor* a un valore intero, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="55e95-104">Rounds each element of *InputTensor* to an integer value, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="55e95-105">Questo operatore supporta l'esecuzione sul posto, vale a dire che *OutputTensor* è autorizzato a creare un alias *di InputTensor durante* l'associazione.</span><span class="sxs-lookup"><span data-stu-id="55e95-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55e95-106">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="55e95-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="55e95-107">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="55e95-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="55e95-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55e95-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ROUND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_ROUNDING_MODE     RoundingMode;
};
```



## <a name="members"></a><span data-ttu-id="55e95-109">Members</span><span class="sxs-lookup"><span data-stu-id="55e95-109">Members</span></span>

`InputTensor`

<span data-ttu-id="55e95-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="55e95-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="55e95-111">Tensore di input da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="55e95-111">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="55e95-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="55e95-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="55e95-113">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="55e95-113">The output tensor to write the results to.</span></span>


`RoundingMode`

<span data-ttu-id="55e95-114">Tipo: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span><span class="sxs-lookup"><span data-stu-id="55e95-114">Type: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span></span>

<span data-ttu-id="55e95-115">Oggetto [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) la direzione verso cui eseguire l'arrotondamento.</span><span class="sxs-lookup"><span data-stu-id="55e95-115">A [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determining the direction to round towards.</span></span>

* <span data-ttu-id="55e95-116">Se **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: i valori vengono arrotondati all'intero più vicino, con i valori a metà (ad esempio, 0,5) arrotondati al numero intero pari più vicino.</span><span class="sxs-lookup"><span data-stu-id="55e95-116">If **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded toward the nearest even integer.</span></span>
* <span data-ttu-id="55e95-117">Se **DML_ROUNDING_MODE_TOWARD_ZERO**: i valori vengono arrotondati a zero.</span><span class="sxs-lookup"><span data-stu-id="55e95-117">If **DML_ROUNDING_MODE_TOWARD_ZERO**: values are rounded toward zero.</span></span> <span data-ttu-id="55e95-118">In questo modo la parte frazionaria viene troncata in modo efficace.</span><span class="sxs-lookup"><span data-stu-id="55e95-118">This effectively truncates the fractional part.</span></span>
* <span data-ttu-id="55e95-119">Se **DML_ROUNDING_MODE_TOWARD_INFINITY**: i valori vengono arrotondati all'intero più vicino, con i valori a metà (ad esempio, 0,5) arrotondati da zero (verso l'infinito positivo o negativo, a seconda del segno del valore).</span><span class="sxs-lookup"><span data-stu-id="55e95-119">If **DML_ROUNDING_MODE_TOWARD_INFINITY**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded away from zero (toward positive or negative infinity, depending on the sign of the value).</span></span>

## <a name="availability"></a><span data-ttu-id="55e95-120">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="55e95-120">Availability</span></span>
<span data-ttu-id="55e95-121">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="55e95-121">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="55e95-122">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="55e95-122">Tensor constraints</span></span>
<span data-ttu-id="55e95-123">*InputTensor* e *OutputTensor* devono avere gli stessi *valori di DataType,* *DimensionCount* e *Sizes.*</span><span class="sxs-lookup"><span data-stu-id="55e95-123">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="55e95-124">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="55e95-124">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="55e95-125">DML_FEATURE_LEVEL_3_0 e successive</span><span class="sxs-lookup"><span data-stu-id="55e95-125">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="55e95-126">Tensore</span><span class="sxs-lookup"><span data-stu-id="55e95-126">Tensor</span></span> | <span data-ttu-id="55e95-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="55e95-127">Kind</span></span> | <span data-ttu-id="55e95-128">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="55e95-128">Supported dimension counts</span></span> | <span data-ttu-id="55e95-129">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="55e95-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="55e95-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="55e95-130">InputTensor</span></span> | <span data-ttu-id="55e95-131">Input</span><span class="sxs-lookup"><span data-stu-id="55e95-131">Input</span></span> | <span data-ttu-id="55e95-132">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="55e95-132">1 to 8</span></span> | <span data-ttu-id="55e95-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="55e95-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="55e95-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="55e95-134">OutputTensor</span></span> | <span data-ttu-id="55e95-135">Output</span><span class="sxs-lookup"><span data-stu-id="55e95-135">Output</span></span> | <span data-ttu-id="55e95-136">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="55e95-136">1 to 8</span></span> | <span data-ttu-id="55e95-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="55e95-137">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="55e95-138">DML_FEATURE_LEVEL_2_1 e successive</span><span class="sxs-lookup"><span data-stu-id="55e95-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="55e95-139">Tensore</span><span class="sxs-lookup"><span data-stu-id="55e95-139">Tensor</span></span> | <span data-ttu-id="55e95-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="55e95-140">Kind</span></span> | <span data-ttu-id="55e95-141">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="55e95-141">Supported dimension counts</span></span> | <span data-ttu-id="55e95-142">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="55e95-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="55e95-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="55e95-143">InputTensor</span></span> | <span data-ttu-id="55e95-144">Input</span><span class="sxs-lookup"><span data-stu-id="55e95-144">Input</span></span> | <span data-ttu-id="55e95-145">4</span><span class="sxs-lookup"><span data-stu-id="55e95-145">4</span></span> | <span data-ttu-id="55e95-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="55e95-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="55e95-147">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="55e95-147">OutputTensor</span></span> | <span data-ttu-id="55e95-148">Output</span><span class="sxs-lookup"><span data-stu-id="55e95-148">Output</span></span> | <span data-ttu-id="55e95-149">4</span><span class="sxs-lookup"><span data-stu-id="55e95-149">4</span></span> | <span data-ttu-id="55e95-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="55e95-150">FLOAT32, FLOAT16</span></span> |



## <a name="requirements"></a><span data-ttu-id="55e95-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55e95-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="55e95-152">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="55e95-152">**Header**</span></span> | <span data-ttu-id="55e95-153">directml.h</span><span class="sxs-lookup"><span data-stu-id="55e95-153">directml.h</span></span> |