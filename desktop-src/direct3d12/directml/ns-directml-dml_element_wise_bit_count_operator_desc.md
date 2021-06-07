---
UID: NS:directml.DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
description: Calcola l'operatore NOT bit per bit per ogni elemento del tensore di input e scrive il risultato nel tensore di output.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.openlocfilehash: 070fc901c006ce1f18429e79eab635a5360c4af7
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417634"
---
# <a name="dml_element_wise_bit_not_operator_desc-structure-directmlh"></a><span data-ttu-id="5b7b4-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="5b7b4-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="5b7b4-104">Calcola l'operatore NOT bit per bit per ogni elemento del tensore di input e scrive il risultato nel tensore di output.</span><span class="sxs-lookup"><span data-stu-id="5b7b4-104">Computes the bitwise NOT for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="5b7b4-105">Il tensore di input e output deve avere gli stessi *valori di DimensionCount,* *Sizes* e *DataType.*</span><span class="sxs-lookup"><span data-stu-id="5b7b4-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="5b7b4-106">Questo operatore supporta l'esecuzione sul posto, ovvero il tensore di output può creare un alias del tensore di input durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="5b7b4-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias the input tensor during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b7b4-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="5b7b4-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="5b7b4-108">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="5b7b4-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b7b4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b7b4-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="5b7b4-110">Members</span><span class="sxs-lookup"><span data-stu-id="5b7b4-110">Members</span></span>

`InputTensor`

<span data-ttu-id="5b7b4-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b7b4-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b7b4-112">Tensore di input da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="5b7b4-112">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="5b7b4-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b7b4-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b7b4-114">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="5b7b4-114">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="5b7b4-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="5b7b4-115">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="5b7b4-116">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="5b7b4-116">Availability</span></span>
<span data-ttu-id="5b7b4-117">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="5b7b4-117">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5b7b4-118">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="5b7b4-118">Tensor constraints</span></span>
<span data-ttu-id="5b7b4-119">*InputTensor* e *OutputTensor* devono avere gli stessi *valori di DataType,* *DimensionCount* e *Sizes.*</span><span class="sxs-lookup"><span data-stu-id="5b7b4-119">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5b7b4-120">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="5b7b4-120">Tensor support</span></span>
| <span data-ttu-id="5b7b4-121">Tensore</span><span class="sxs-lookup"><span data-stu-id="5b7b4-121">Tensor</span></span> | <span data-ttu-id="5b7b4-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="5b7b4-122">Kind</span></span> | <span data-ttu-id="5b7b4-123">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="5b7b4-123">Supported dimension counts</span></span> | <span data-ttu-id="5b7b4-124">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="5b7b4-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5b7b4-125">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5b7b4-125">InputTensor</span></span> | <span data-ttu-id="5b7b4-126">Input</span><span class="sxs-lookup"><span data-stu-id="5b7b4-126">Input</span></span> | <span data-ttu-id="5b7b4-127">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="5b7b4-127">1 to 8</span></span> | <span data-ttu-id="5b7b4-128">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5b7b4-128">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="5b7b4-129">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5b7b4-129">OutputTensor</span></span> | <span data-ttu-id="5b7b4-130">Output</span><span class="sxs-lookup"><span data-stu-id="5b7b4-130">Output</span></span> | <span data-ttu-id="5b7b4-131">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="5b7b4-131">1 to 8</span></span> | <span data-ttu-id="5b7b4-132">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5b7b4-132">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="5b7b4-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b7b4-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5b7b4-134">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="5b7b4-134">**Header**</span></span> | <span data-ttu-id="5b7b4-135">directml.h</span><span class="sxs-lookup"><span data-stu-id="5b7b4-135">directml.h</span></span> |