---
UID: NS:directml.DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
description: Calcola l'operatore AND bit per bit tra ogni elemento corrispondente dei tensori di input e scrive il risultato nel tensore di output.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
ms.openlocfilehash: 9e8730eef1b2d98c2f3094fb2fa29ecfc571d877
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320407"
---
# <a name="dml_element_wise_bit_and_operator_desc-structure-directmlh"></a><span data-ttu-id="788d1-103">Struttura DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="788d1-103">DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="788d1-104">Calcola l'operatore AND bit per bit tra ogni elemento corrispondente dei tensori di input e scrive il risultato nel tensore di output.</span><span class="sxs-lookup"><span data-stu-id="788d1-104">Computes the bitwise AND between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="788d1-105">Il tensore di input e di output deve avere lo stesso *DimensionCount*, le *dimensioni* e il *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="788d1-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="788d1-106">Questo operatore supporta l'esecuzione sul posto, vale a dire che il tensore di output è autorizzato a eseguire l'alias di uno o più dei tensori di input durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="788d1-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="788d1-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="788d1-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="788d1-108">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="788d1-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="788d1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="788d1-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="788d1-110">Members</span><span class="sxs-lookup"><span data-stu-id="788d1-110">Members</span></span>

`ATensor`

<span data-ttu-id="788d1-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="788d1-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="788d1-112">Un tensore contenente gli input sul lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="788d1-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="788d1-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="788d1-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="788d1-114">Un tensore contenente gli input sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="788d1-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="788d1-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="788d1-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="788d1-116">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="788d1-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="788d1-117">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="788d1-117">Availability</span></span>
<span data-ttu-id="788d1-118">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="788d1-118">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="788d1-119">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="788d1-119">Tensor constraints</span></span>
<span data-ttu-id="788d1-120">*ATensor*, *BTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati, *DimensionCount* e *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="788d1-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="788d1-121">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="788d1-121">Tensor support</span></span>
| <span data-ttu-id="788d1-122">Tensore</span><span class="sxs-lookup"><span data-stu-id="788d1-122">Tensor</span></span> | <span data-ttu-id="788d1-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="788d1-123">Kind</span></span> | <span data-ttu-id="788d1-124">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="788d1-124">Supported dimension counts</span></span> | <span data-ttu-id="788d1-125">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="788d1-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="788d1-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="788d1-126">ATensor</span></span> | <span data-ttu-id="788d1-127">Input</span><span class="sxs-lookup"><span data-stu-id="788d1-127">Input</span></span> | <span data-ttu-id="788d1-128">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="788d1-128">1 to 8</span></span> | <span data-ttu-id="788d1-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="788d1-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="788d1-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="788d1-130">BTensor</span></span> | <span data-ttu-id="788d1-131">Input</span><span class="sxs-lookup"><span data-stu-id="788d1-131">Input</span></span> | <span data-ttu-id="788d1-132">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="788d1-132">1 to 8</span></span> | <span data-ttu-id="788d1-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="788d1-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="788d1-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="788d1-134">OutputTensor</span></span> | <span data-ttu-id="788d1-135">Output</span><span class="sxs-lookup"><span data-stu-id="788d1-135">Output</span></span> | <span data-ttu-id="788d1-136">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="788d1-136">1 to 8</span></span> | <span data-ttu-id="788d1-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="788d1-137">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="788d1-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="788d1-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="788d1-139">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="788d1-139">**Header**</span></span> | <span data-ttu-id="788d1-140">directml. h</span><span class="sxs-lookup"><span data-stu-id="788d1-140">directml.h</span></span> |