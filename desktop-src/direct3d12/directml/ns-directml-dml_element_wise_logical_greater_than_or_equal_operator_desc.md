---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
description: Esegue un *valore logico maggiore o uguale a* in ogni coppia di elementi corrispondenti dei tensori di input, inserendo il risultato (1 per true, 0 per false) nell'elemento corrispondente di *OutputTensor*.
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
ms.openlocfilehash: bfe3c3abbabf0bd4f5dfa4d8393f3ed7d74a210f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320276"
---
# <a name="dml_element_wise_logical_greater_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="2fb6b-103">Struttura DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="2fb6b-103">DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="2fb6b-104">Esegue un *valore logico maggiore o uguale a* in ogni coppia di elementi corrispondenti dei tensori di input, inserendo il risultato (1 per true, 0 per false) nell'elemento corrispondente di *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="2fb6b-104">Performs a logical *greater than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >= b)
```

> [!IMPORTANT]
> <span data-ttu-id="2fb6b-105">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="2fb6b-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="2fb6b-106">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="2fb6b-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2fb6b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fb6b-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="2fb6b-108">Members</span><span class="sxs-lookup"><span data-stu-id="2fb6b-108">Members</span></span>

`ATensor`

<span data-ttu-id="2fb6b-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2fb6b-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2fb6b-110">Un tensore contenente gli input sul lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="2fb6b-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="2fb6b-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2fb6b-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2fb6b-112">Un tensore contenente gli input sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="2fb6b-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="2fb6b-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2fb6b-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2fb6b-114">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="2fb6b-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="2fb6b-115">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="2fb6b-115">Availability</span></span>
<span data-ttu-id="2fb6b-116">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="2fb6b-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="2fb6b-117">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="2fb6b-117">Tensor constraints</span></span>
* <span data-ttu-id="2fb6b-118">*ATensor* e *BTensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="2fb6b-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="2fb6b-119">*ATensor*, *BTensor* e *OutputTensor* devono avere lo stesso *DimensionCount* e le stesse *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="2fb6b-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="2fb6b-120">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="2fb6b-120">Tensor support</span></span>
| <span data-ttu-id="2fb6b-121">Tensore</span><span class="sxs-lookup"><span data-stu-id="2fb6b-121">Tensor</span></span> | <span data-ttu-id="2fb6b-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fb6b-122">Kind</span></span> | <span data-ttu-id="2fb6b-123">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="2fb6b-123">Supported dimension counts</span></span> | <span data-ttu-id="2fb6b-124">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="2fb6b-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="2fb6b-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="2fb6b-125">ATensor</span></span> | <span data-ttu-id="2fb6b-126">Input</span><span class="sxs-lookup"><span data-stu-id="2fb6b-126">Input</span></span> | <span data-ttu-id="2fb6b-127">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="2fb6b-127">1 to 8</span></span> | <span data-ttu-id="2fb6b-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2fb6b-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="2fb6b-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="2fb6b-129">BTensor</span></span> | <span data-ttu-id="2fb6b-130">Input</span><span class="sxs-lookup"><span data-stu-id="2fb6b-130">Input</span></span> | <span data-ttu-id="2fb6b-131">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="2fb6b-131">1 to 8</span></span> | <span data-ttu-id="2fb6b-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2fb6b-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="2fb6b-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="2fb6b-133">OutputTensor</span></span> | <span data-ttu-id="2fb6b-134">Output</span><span class="sxs-lookup"><span data-stu-id="2fb6b-134">Output</span></span> | <span data-ttu-id="2fb6b-135">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="2fb6b-135">1 to 8</span></span> | <span data-ttu-id="2fb6b-136">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="2fb6b-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="2fb6b-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fb6b-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2fb6b-138">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="2fb6b-138">**Header**</span></span> | <span data-ttu-id="2fb6b-139">directml. h</span><span class="sxs-lookup"><span data-stu-id="2fb6b-139">directml.h</span></span> |