---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: Controlla ogni elemento di *InputTensor* per IEEE-754 -inf, inf o entrambi, a seconda *dell'oggetto InfinityMode* specificato e inserisce il risultato (1 per true, 0 per false) nell'elemento corrispondente di *OutputTensor.*
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: ''
req.dll: ''
req.header: directml.h
req.include-header: ''
req.kmdf-ver: ''
req.lib: ''
req.max-support: ''
req.redist: ''
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: ''
req.umdf-ver: ''
req.unicode-ansi: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- directml.h
api_name:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
f1_keywords:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
dev_langs:
- c++
ms.openlocfilehash: 41be7751b542436b481da784c60ae79ad554cd12
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803103"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a><span data-ttu-id="f4fea-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="f4fea-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="f4fea-104">Controlla ogni elemento di *InputTensor* per IEEE-754 -inf, inf o entrambi, a seconda *dell'oggetto InfinityMode* specificato e inserisce il risultato (1 per true, 0 per false) nell'elemento corrispondente di *OutputTensor.*</span><span class="sxs-lookup"><span data-stu-id="f4fea-104">Checks each element of *InputTensor* for IEEE-754 -inf, inf, or both, depending on the given *InfinityMode*, and places the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> <span data-ttu-id="f4fea-105">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="f4fea-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f4fea-106">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="f4fea-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4fea-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4fea-107">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a><span data-ttu-id="f4fea-108">Members</span><span class="sxs-lookup"><span data-stu-id="f4fea-108">Members</span></span>

`InputTensor`

<span data-ttu-id="f4fea-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f4fea-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f4fea-110">Tensore di input da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="f4fea-110">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="f4fea-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f4fea-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f4fea-112">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="f4fea-112">The output tensor to write the results to.</span></span>


`InfinityMode`

<span data-ttu-id="f4fea-113">Tipo: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span><span class="sxs-lookup"><span data-stu-id="f4fea-113">Type: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span></span>

<span data-ttu-id="f4fea-114">Oggetto [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) il segno dell'infinito da verificare.</span><span class="sxs-lookup"><span data-stu-id="f4fea-114">A [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determining the sign of the infinity to check for.</span></span>

* <span data-ttu-id="f4fea-115">Se **DML_IS_INFINITY_MODE_EITHER**, verrà restituito 1 se l'elemento è -inf o inf, in caso contrario 0.</span><span class="sxs-lookup"><span data-stu-id="f4fea-115">If **DML_IS_INFINITY_MODE_EITHER**, then 1 will be returned if the element is -inf or inf, otherwise 0.</span></span>
* <span data-ttu-id="f4fea-116">Se **DML_IS_INFINITY_MODE_POSITIVE**, verrà restituito 1 se l'elemento è inf; in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="f4fea-116">If **DML_IS_INFINITY_MODE_POSITIVE**, then 1 will be returned if the element is inf, otherwise 0.</span></span>
* <span data-ttu-id="f4fea-117">Se **DML_IS_INFINITY_MODE_NEGATIVE**', verrà restituito 1 se l'elemento è -inf; in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="f4fea-117">If **DML_IS_INFINITY_MODE_NEGATIVE**\`, then 1 will be returned if the element is -inf, otherwise 0.</span></span>


## <a name="remarks"></a><span data-ttu-id="f4fea-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4fea-118">Remarks</span></span>
## <a name="availability"></a><span data-ttu-id="f4fea-119">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="f4fea-119">Availability</span></span>
<span data-ttu-id="f4fea-120">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="f4fea-120">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f4fea-121">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="f4fea-121">Tensor constraints</span></span>
<span data-ttu-id="f4fea-122">*InputTensor* e *OutputTensor* devono avere gli stessi *valori di DimensionCount* *e Sizes.*</span><span class="sxs-lookup"><span data-stu-id="f4fea-122">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f4fea-123">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="f4fea-123">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="f4fea-124">DML_FEATURE_LEVEL_3_0 e successive</span><span class="sxs-lookup"><span data-stu-id="f4fea-124">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="f4fea-125">Tensore</span><span class="sxs-lookup"><span data-stu-id="f4fea-125">Tensor</span></span> | <span data-ttu-id="f4fea-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4fea-126">Kind</span></span> | <span data-ttu-id="f4fea-127">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="f4fea-127">Supported dimension counts</span></span> | <span data-ttu-id="f4fea-128">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="f4fea-128">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f4fea-129">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f4fea-129">InputTensor</span></span> | <span data-ttu-id="f4fea-130">Input</span><span class="sxs-lookup"><span data-stu-id="f4fea-130">Input</span></span> | <span data-ttu-id="f4fea-131">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="f4fea-131">1 to 8</span></span> | <span data-ttu-id="f4fea-132">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f4fea-132">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f4fea-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f4fea-133">OutputTensor</span></span> | <span data-ttu-id="f4fea-134">Output</span><span class="sxs-lookup"><span data-stu-id="f4fea-134">Output</span></span> | <span data-ttu-id="f4fea-135">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="f4fea-135">1 to 8</span></span> | <span data-ttu-id="f4fea-136">UINT8</span><span class="sxs-lookup"><span data-stu-id="f4fea-136">UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="f4fea-137">DML_FEATURE_LEVEL_2_1 e successive</span><span class="sxs-lookup"><span data-stu-id="f4fea-137">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="f4fea-138">Tensore</span><span class="sxs-lookup"><span data-stu-id="f4fea-138">Tensor</span></span> | <span data-ttu-id="f4fea-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4fea-139">Kind</span></span> | <span data-ttu-id="f4fea-140">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="f4fea-140">Supported dimension counts</span></span> | <span data-ttu-id="f4fea-141">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="f4fea-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f4fea-142">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f4fea-142">InputTensor</span></span> | <span data-ttu-id="f4fea-143">Input</span><span class="sxs-lookup"><span data-stu-id="f4fea-143">Input</span></span> | <span data-ttu-id="f4fea-144">4</span><span class="sxs-lookup"><span data-stu-id="f4fea-144">4</span></span> | <span data-ttu-id="f4fea-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f4fea-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f4fea-146">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f4fea-146">OutputTensor</span></span> | <span data-ttu-id="f4fea-147">Output</span><span class="sxs-lookup"><span data-stu-id="f4fea-147">Output</span></span> | <span data-ttu-id="f4fea-148">4</span><span class="sxs-lookup"><span data-stu-id="f4fea-148">4</span></span> | <span data-ttu-id="f4fea-149">UINT8</span><span class="sxs-lookup"><span data-stu-id="f4fea-149">UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="f4fea-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4fea-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f4fea-151">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="f4fea-151">**Minimum supported client**</span></span> | <span data-ttu-id="f4fea-152">Windows 10 versione 2004 (10.0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="f4fea-152">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="f4fea-153">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="f4fea-153">**Minimum supported server**</span></span> | <span data-ttu-id="f4fea-154">Windows Server versione 2004 (10.0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="f4fea-154">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="f4fea-155">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="f4fea-155">**Header**</span></span> | <span data-ttu-id="f4fea-156">directml.h</span><span class="sxs-lookup"><span data-stu-id="f4fea-156">directml.h</span></span> |