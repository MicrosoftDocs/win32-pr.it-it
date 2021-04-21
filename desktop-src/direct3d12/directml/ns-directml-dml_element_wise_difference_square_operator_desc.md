---
UID: NS:directml.DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
title: DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
description: Sottrae ogni elemento di *BTensor* dall'elemento corrispondente di *ATensor,* moltiplica il risultato per se stesso e inserisce il risultato nell'elemento corrispondente di *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
ms.openlocfilehash: 3e3e7ab8f222f42def82a168ed861e58347f3b20
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804480"
---
# <a name="dml_element_wise_difference_square_operator_desc-directmlh"></a><span data-ttu-id="770de-103">DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="770de-103">DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="770de-104">Sottrae ogni elemento di *BTensor* dall'elemento corrispondente di *ATensor,* moltiplica il risultato per se stesso e inserisce il risultato nell'elemento corrispondente di *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="770de-104">Subtracts each element of *BTensor* from the corresponding element of *ATensor*, multiplies the result by itself, and places the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a - b) * (a - b)
```

<span data-ttu-id="770de-105">Questo operatore supporta l'esecuzione sul posto, ovvero *OutputTensor* è autorizzato ad aggiungere alias *ad ATensor* o *BTensor* durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="770de-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *ATensor* or *BTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="770de-106">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.5 e successive).</span><span class="sxs-lookup"><span data-stu-id="770de-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="770de-107">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="770de-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="770de-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="770de-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="770de-109">Members</span><span class="sxs-lookup"><span data-stu-id="770de-109">Members</span></span>

`ATensor`

<span data-ttu-id="770de-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="770de-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="770de-111">Tensore contenente gli input sul lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="770de-111">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="770de-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="770de-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="770de-113">Tensore contenente gli input sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="770de-113">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="770de-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="770de-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="770de-115">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="770de-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="770de-116">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="770de-116">Availability</span></span>
<span data-ttu-id="770de-117">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="770de-117">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="770de-118">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="770de-118">Tensor constraints</span></span>
<span data-ttu-id="770de-119">*ATensor,* *BTensor* e *OutputTensor* devono avere gli stessi *datatype*, *DimensionCount* e *Sizes*.</span><span class="sxs-lookup"><span data-stu-id="770de-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="770de-120">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="770de-120">Tensor support</span></span>
| <span data-ttu-id="770de-121">Tensore</span><span class="sxs-lookup"><span data-stu-id="770de-121">Tensor</span></span> | <span data-ttu-id="770de-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="770de-122">Kind</span></span> | <span data-ttu-id="770de-123">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="770de-123">Supported dimension counts</span></span> | <span data-ttu-id="770de-124">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="770de-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="770de-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="770de-125">ATensor</span></span> | <span data-ttu-id="770de-126">Input</span><span class="sxs-lookup"><span data-stu-id="770de-126">Input</span></span> | <span data-ttu-id="770de-127">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="770de-127">1 to 8</span></span> | <span data-ttu-id="770de-128">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="770de-128">FLOAT32, FLOAT16, INT32, UINT32</span></span> |
| <span data-ttu-id="770de-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="770de-129">BTensor</span></span> | <span data-ttu-id="770de-130">Input</span><span class="sxs-lookup"><span data-stu-id="770de-130">Input</span></span> | <span data-ttu-id="770de-131">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="770de-131">1 to 8</span></span> | <span data-ttu-id="770de-132">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="770de-132">FLOAT32, FLOAT16, INT32, UINT32</span></span> |
| <span data-ttu-id="770de-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="770de-133">OutputTensor</span></span> | <span data-ttu-id="770de-134">Output</span><span class="sxs-lookup"><span data-stu-id="770de-134">Output</span></span> | <span data-ttu-id="770de-135">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="770de-135">1 to 8</span></span> | <span data-ttu-id="770de-136">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="770de-136">FLOAT32, FLOAT16, INT32, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="770de-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="770de-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="770de-138">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="770de-138">**Header**</span></span> | <span data-ttu-id="770de-139">directml.h</span><span class="sxs-lookup"><span data-stu-id="770de-139">directml.h</span></span> |
