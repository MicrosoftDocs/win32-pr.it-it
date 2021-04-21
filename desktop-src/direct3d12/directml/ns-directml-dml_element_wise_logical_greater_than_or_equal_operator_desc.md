---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
description: Esegue un  valore logico maggiore o uguale a su ogni coppia di elementi corrispondenti dei tensori di input, inserendo il risultato (1 per true, 0 per false) nell'elemento corrispondente di *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC, DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
ms.openlocfilehash: 4c20580a67117e6a605dfb0bf6611aca5cfd9e56
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803092"
---
# <a name="dml_element_wise_logical_greater_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="676ca-103">DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="676ca-103">DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="676ca-104">Esegue un  valore logico maggiore o uguale a su ogni coppia di elementi corrispondenti dei tensori di input, inserendo il risultato (1 per true, 0 per false) nell'elemento corrispondente di *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="676ca-104">Performs a logical *greater than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >= b)
```

> [!IMPORTANT]
> <span data-ttu-id="676ca-105">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="676ca-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="676ca-106">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="676ca-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="676ca-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="676ca-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="676ca-108">Members</span><span class="sxs-lookup"><span data-stu-id="676ca-108">Members</span></span>

`ATensor`

<span data-ttu-id="676ca-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="676ca-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="676ca-110">Tensore contenente gli input sul lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="676ca-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="676ca-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="676ca-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="676ca-112">Tensore contenente gli input sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="676ca-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="676ca-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="676ca-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="676ca-114">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="676ca-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="676ca-115">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="676ca-115">Availability</span></span>
<span data-ttu-id="676ca-116">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="676ca-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="676ca-117">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="676ca-117">Tensor constraints</span></span>
* <span data-ttu-id="676ca-118">*ATensor* e *BTensor* devono avere lo stesso *Tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="676ca-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="676ca-119">*ATensor,* *BTensor* e *OutputTensor* devono avere gli stessi *valori DimensionCount* e *Sizes*.</span><span class="sxs-lookup"><span data-stu-id="676ca-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="676ca-120">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="676ca-120">Tensor support</span></span>
| <span data-ttu-id="676ca-121">Tensore</span><span class="sxs-lookup"><span data-stu-id="676ca-121">Tensor</span></span> | <span data-ttu-id="676ca-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="676ca-122">Kind</span></span> | <span data-ttu-id="676ca-123">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="676ca-123">Supported dimension counts</span></span> | <span data-ttu-id="676ca-124">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="676ca-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="676ca-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="676ca-125">ATensor</span></span> | <span data-ttu-id="676ca-126">Input</span><span class="sxs-lookup"><span data-stu-id="676ca-126">Input</span></span> | <span data-ttu-id="676ca-127">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="676ca-127">1 to 8</span></span> | <span data-ttu-id="676ca-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="676ca-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="676ca-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="676ca-129">BTensor</span></span> | <span data-ttu-id="676ca-130">Input</span><span class="sxs-lookup"><span data-stu-id="676ca-130">Input</span></span> | <span data-ttu-id="676ca-131">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="676ca-131">1 to 8</span></span> | <span data-ttu-id="676ca-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="676ca-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="676ca-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="676ca-133">OutputTensor</span></span> | <span data-ttu-id="676ca-134">Output</span><span class="sxs-lookup"><span data-stu-id="676ca-134">Output</span></span> | <span data-ttu-id="676ca-135">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="676ca-135">1 to 8</span></span> | <span data-ttu-id="676ca-136">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="676ca-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="676ca-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="676ca-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="676ca-138">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="676ca-138">**Header**</span></span> | <span data-ttu-id="676ca-139">directml.h</span><span class="sxs-lookup"><span data-stu-id="676ca-139">directml.h</span></span> |