---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: Controlla ogni elemento di *InputTensor* per IEEE-754-inf, inf o entrambi, a seconda del *InfinityMode* specificato e inserisce il risultato (1 per true, 0 per false) nell'elemento corrispondente di *OutputTensor*.
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
ms.openlocfilehash: b4f3f07fcbe303e86b422206a8f07eb75fb09d70
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320275"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a><span data-ttu-id="03c12-103">Struttura DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="03c12-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="03c12-104">Controlla ogni elemento di *InputTensor* per IEEE-754-inf, inf o entrambi, a seconda del *InfinityMode* specificato e inserisce il risultato (1 per true, 0 per false) nell'elemento corrispondente di *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="03c12-104">Checks each element of *InputTensor* for IEEE-754 -inf, inf, or both, depending on the given *InfinityMode*, and places the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> <span data-ttu-id="03c12-105">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="03c12-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="03c12-106">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="03c12-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="03c12-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03c12-107">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a><span data-ttu-id="03c12-108">Members</span><span class="sxs-lookup"><span data-stu-id="03c12-108">Members</span></span>

`InputTensor`

<span data-ttu-id="03c12-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="03c12-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="03c12-110">Tensore di input da cui eseguire la lettura.</span><span class="sxs-lookup"><span data-stu-id="03c12-110">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="03c12-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="03c12-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="03c12-112">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="03c12-112">The output tensor to write the results to.</span></span>


`InfinityMode`

<span data-ttu-id="03c12-113">Tipo: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span><span class="sxs-lookup"><span data-stu-id="03c12-113">Type: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span></span>

<span data-ttu-id="03c12-114">[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) che determina il segno dell'infinito da verificare.</span><span class="sxs-lookup"><span data-stu-id="03c12-114">A [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determining the sign of the infinity to check for.</span></span>

* <span data-ttu-id="03c12-115">Se **DML_IS_INFINITY_MODE_EITHER**, viene restituito 1 se l'elemento è-inf o inf, in caso contrario 0.</span><span class="sxs-lookup"><span data-stu-id="03c12-115">If **DML_IS_INFINITY_MODE_EITHER**, then 1 will be returned if the element is -inf or inf, otherwise 0.</span></span>
* <span data-ttu-id="03c12-116">Se **DML_IS_INFINITY_MODE_POSITIVE**, viene restituito 1 se l'elemento è inf, in caso contrario 0.</span><span class="sxs-lookup"><span data-stu-id="03c12-116">If **DML_IS_INFINITY_MODE_POSITIVE**, then 1 will be returned if the element is inf, otherwise 0.</span></span>
* <span data-ttu-id="03c12-117">Se **DML_IS_INFINITY_MODE_NEGATIVE**', viene restituito 1 se l'elemento è-inf, in caso contrario 0.</span><span class="sxs-lookup"><span data-stu-id="03c12-117">If **DML_IS_INFINITY_MODE_NEGATIVE**\`, then 1 will be returned if the element is -inf, otherwise 0.</span></span>


## <a name="remarks"></a><span data-ttu-id="03c12-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="03c12-118">Remarks</span></span>
## <a name="availability"></a><span data-ttu-id="03c12-119">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="03c12-119">Availability</span></span>
<span data-ttu-id="03c12-120">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="03c12-120">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="03c12-121">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="03c12-121">Tensor constraints</span></span>
<span data-ttu-id="03c12-122">*InputTensor* e *OutputTensor* devono avere lo stesso *DimensionCount* e le stesse *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="03c12-122">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="03c12-123">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="03c12-123">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="03c12-124">DML_FEATURE_LEVEL_3_0 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="03c12-124">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="03c12-125">Tensore</span><span class="sxs-lookup"><span data-stu-id="03c12-125">Tensor</span></span> | <span data-ttu-id="03c12-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="03c12-126">Kind</span></span> | <span data-ttu-id="03c12-127">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="03c12-127">Supported dimension counts</span></span> | <span data-ttu-id="03c12-128">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="03c12-128">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="03c12-129">InputTensor</span><span class="sxs-lookup"><span data-stu-id="03c12-129">InputTensor</span></span> | <span data-ttu-id="03c12-130">Input</span><span class="sxs-lookup"><span data-stu-id="03c12-130">Input</span></span> | <span data-ttu-id="03c12-131">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="03c12-131">1 to 8</span></span> | <span data-ttu-id="03c12-132">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="03c12-132">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="03c12-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="03c12-133">OutputTensor</span></span> | <span data-ttu-id="03c12-134">Output</span><span class="sxs-lookup"><span data-stu-id="03c12-134">Output</span></span> | <span data-ttu-id="03c12-135">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="03c12-135">1 to 8</span></span> | <span data-ttu-id="03c12-136">UINT8</span><span class="sxs-lookup"><span data-stu-id="03c12-136">UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="03c12-137">DML_FEATURE_LEVEL_2_1 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="03c12-137">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="03c12-138">Tensore</span><span class="sxs-lookup"><span data-stu-id="03c12-138">Tensor</span></span> | <span data-ttu-id="03c12-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="03c12-139">Kind</span></span> | <span data-ttu-id="03c12-140">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="03c12-140">Supported dimension counts</span></span> | <span data-ttu-id="03c12-141">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="03c12-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="03c12-142">InputTensor</span><span class="sxs-lookup"><span data-stu-id="03c12-142">InputTensor</span></span> | <span data-ttu-id="03c12-143">Input</span><span class="sxs-lookup"><span data-stu-id="03c12-143">Input</span></span> | <span data-ttu-id="03c12-144">4</span><span class="sxs-lookup"><span data-stu-id="03c12-144">4</span></span> | <span data-ttu-id="03c12-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="03c12-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="03c12-146">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="03c12-146">OutputTensor</span></span> | <span data-ttu-id="03c12-147">Output</span><span class="sxs-lookup"><span data-stu-id="03c12-147">Output</span></span> | <span data-ttu-id="03c12-148">4</span><span class="sxs-lookup"><span data-stu-id="03c12-148">4</span></span> | <span data-ttu-id="03c12-149">UINT8</span><span class="sxs-lookup"><span data-stu-id="03c12-149">UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="03c12-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03c12-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="03c12-151">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="03c12-151">**Minimum supported client**</span></span> | <span data-ttu-id="03c12-152">Windows 10, versione 2004 (10,0; Compilazione 19041)</span><span class="sxs-lookup"><span data-stu-id="03c12-152">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="03c12-153">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="03c12-153">**Minimum supported server**</span></span> | <span data-ttu-id="03c12-154">Windows Server, versione 2004 (10,0; Compilazione 19041)</span><span class="sxs-lookup"><span data-stu-id="03c12-154">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="03c12-155">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="03c12-155">**Header**</span></span> | <span data-ttu-id="03c12-156">directml. h</span><span class="sxs-lookup"><span data-stu-id="03c12-156">directml.h</span></span> |