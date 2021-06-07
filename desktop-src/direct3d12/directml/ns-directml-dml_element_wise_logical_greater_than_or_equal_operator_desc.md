---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
description: Esegue un  valore logico maggiore o uguale a in ogni coppia di elementi corrispondenti dei tensori di input, inserendo il risultato (1 per true, 0 per false) nell'elemento corrispondente di *OutputTensor.*
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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417857"
---
# <a name="dml_element_wise_logical_greater_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="a1a30-103">DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="a1a30-103">DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="a1a30-104">Esegue un  valore logico maggiore o uguale a in ogni coppia di elementi corrispondenti dei tensori di input, inserendo il risultato (1 per true, 0 per false) nell'elemento corrispondente di *OutputTensor.*</span><span class="sxs-lookup"><span data-stu-id="a1a30-104">Performs a logical *greater than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >= b)
```

> [!IMPORTANT]
> <span data-ttu-id="a1a30-105">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="a1a30-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="a1a30-106">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="a1a30-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1a30-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1a30-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="a1a30-108">Members</span><span class="sxs-lookup"><span data-stu-id="a1a30-108">Members</span></span>

`ATensor`

<span data-ttu-id="a1a30-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a1a30-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a1a30-110">Tensore contenente gli input sul lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="a1a30-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="a1a30-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a1a30-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a1a30-112">Tensore contenente gli input sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="a1a30-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="a1a30-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a1a30-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a1a30-114">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="a1a30-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="a1a30-115">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="a1a30-115">Availability</span></span>
<span data-ttu-id="a1a30-116">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="a1a30-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a1a30-117">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="a1a30-117">Tensor constraints</span></span>
* <span data-ttu-id="a1a30-118">*ATensor* e *BTensor* devono avere lo stesso *tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="a1a30-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="a1a30-119">*ATensor,* *BTensor* e *OutputTensor* devono avere gli stessi *valori DimensionCount* e *Sizes*.</span><span class="sxs-lookup"><span data-stu-id="a1a30-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a1a30-120">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="a1a30-120">Tensor support</span></span>
| <span data-ttu-id="a1a30-121">Tensore</span><span class="sxs-lookup"><span data-stu-id="a1a30-121">Tensor</span></span> | <span data-ttu-id="a1a30-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1a30-122">Kind</span></span> | <span data-ttu-id="a1a30-123">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="a1a30-123">Supported dimension counts</span></span> | <span data-ttu-id="a1a30-124">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="a1a30-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a1a30-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="a1a30-125">ATensor</span></span> | <span data-ttu-id="a1a30-126">Input</span><span class="sxs-lookup"><span data-stu-id="a1a30-126">Input</span></span> | <span data-ttu-id="a1a30-127">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a1a30-127">1 to 8</span></span> | <span data-ttu-id="a1a30-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a1a30-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a1a30-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="a1a30-129">BTensor</span></span> | <span data-ttu-id="a1a30-130">Input</span><span class="sxs-lookup"><span data-stu-id="a1a30-130">Input</span></span> | <span data-ttu-id="a1a30-131">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a1a30-131">1 to 8</span></span> | <span data-ttu-id="a1a30-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a1a30-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a1a30-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a1a30-133">OutputTensor</span></span> | <span data-ttu-id="a1a30-134">Output</span><span class="sxs-lookup"><span data-stu-id="a1a30-134">Output</span></span> | <span data-ttu-id="a1a30-135">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a1a30-135">1 to 8</span></span> | <span data-ttu-id="a1a30-136">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="a1a30-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="a1a30-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1a30-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a1a30-138">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="a1a30-138">**Header**</span></span> | <span data-ttu-id="a1a30-139">directml.h</span><span class="sxs-lookup"><span data-stu-id="a1a30-139">directml.h</span></span> |