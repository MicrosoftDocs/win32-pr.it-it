---
UID: NS:directml.DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
description: Calcola l'operatore XOR bit per bit (OR eXclusive) tra ogni elemento corrispondente dei tensori di input e scrive il risultato nel tensore di output.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
ms.openlocfilehash: fcedb2c33f1c63196a9e6783daaa9f2d863e99f0
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803191"
---
# <a name="dml_element_wise_bit_xor_operator_desc-structure-directmlh"></a><span data-ttu-id="a10bf-103">DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="a10bf-103">DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="a10bf-104">Calcola l'operatore XOR bit per bit (OR eXclusive) tra ogni elemento corrispondente dei tensori di input e scrive il risultato nel tensore di output.</span><span class="sxs-lookup"><span data-stu-id="a10bf-104">Computes the bitwise XOR (eXclusive OR) between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="a10bf-105">Il tensore di input e output deve avere gli stessi *valori di DimensionCount,* *Sizes* e *DataType.*</span><span class="sxs-lookup"><span data-stu-id="a10bf-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="a10bf-106">Questo operatore supporta l'esecuzione sul posto, vale a dire che il tensore di output può creare un alias per uno o più tensori di input durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="a10bf-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a10bf-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="a10bf-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="a10bf-108">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="a10bf-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a10bf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a10bf-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="a10bf-110">Members</span><span class="sxs-lookup"><span data-stu-id="a10bf-110">Members</span></span>

`ATensor`

<span data-ttu-id="a10bf-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a10bf-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a10bf-112">Tensore contenente gli input sul lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="a10bf-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="a10bf-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a10bf-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a10bf-114">Tensore contenente gli input sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="a10bf-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="a10bf-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a10bf-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a10bf-116">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="a10bf-116">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="a10bf-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="a10bf-117">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="a10bf-118">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="a10bf-118">Availability</span></span>
<span data-ttu-id="a10bf-119">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="a10bf-119">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a10bf-120">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="a10bf-120">Tensor constraints</span></span>
<span data-ttu-id="a10bf-121">*ATensor,* *BTensor* e *OutputTensor* devono avere gli stessi *valori di DataType,* *DimensionCount* e *Sizes.*</span><span class="sxs-lookup"><span data-stu-id="a10bf-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a10bf-122">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="a10bf-122">Tensor support</span></span>
| <span data-ttu-id="a10bf-123">Tensore</span><span class="sxs-lookup"><span data-stu-id="a10bf-123">Tensor</span></span> | <span data-ttu-id="a10bf-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="a10bf-124">Kind</span></span> | <span data-ttu-id="a10bf-125">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="a10bf-125">Supported dimension counts</span></span> | <span data-ttu-id="a10bf-126">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="a10bf-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a10bf-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="a10bf-127">ATensor</span></span> | <span data-ttu-id="a10bf-128">Input</span><span class="sxs-lookup"><span data-stu-id="a10bf-128">Input</span></span> | <span data-ttu-id="a10bf-129">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a10bf-129">1 to 8</span></span> | <span data-ttu-id="a10bf-130">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a10bf-130">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a10bf-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="a10bf-131">BTensor</span></span> | <span data-ttu-id="a10bf-132">Input</span><span class="sxs-lookup"><span data-stu-id="a10bf-132">Input</span></span> | <span data-ttu-id="a10bf-133">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a10bf-133">1 to 8</span></span> | <span data-ttu-id="a10bf-134">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a10bf-134">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a10bf-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a10bf-135">OutputTensor</span></span> | <span data-ttu-id="a10bf-136">Output</span><span class="sxs-lookup"><span data-stu-id="a10bf-136">Output</span></span> | <span data-ttu-id="a10bf-137">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a10bf-137">1 to 8</span></span> | <span data-ttu-id="a10bf-138">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a10bf-138">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="a10bf-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a10bf-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a10bf-140">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="a10bf-140">**Header**</span></span> | <span data-ttu-id="a10bf-141">directml.h</span><span class="sxs-lookup"><span data-stu-id="a10bf-141">directml.h</span></span> |