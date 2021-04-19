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
ms.openlocfilehash: bb42be1e1f00fcf749ed271d55a7958b43464f1a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320341"
---
# <a name="dml_element_wise_bit_not_operator_desc-structure-directmlh"></a><span data-ttu-id="f21fb-103">Struttura DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="f21fb-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="f21fb-104">Calcola l'operatore NOT bit per bit per ogni elemento del tensore di input e scrive il risultato nel tensore di output.</span><span class="sxs-lookup"><span data-stu-id="f21fb-104">Computes the bitwise NOT for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="f21fb-105">Il tensore di input e di output deve avere lo stesso *DimensionCount*, le *dimensioni* e il *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="f21fb-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="f21fb-106">Questo operatore supporta l'esecuzione sul posto, vale a dire che il tensore di output è autorizzato a eseguire l'alias del tensore di input durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="f21fb-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias the input tensor during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f21fb-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="f21fb-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="f21fb-108">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="f21fb-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f21fb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f21fb-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="f21fb-110">Members</span><span class="sxs-lookup"><span data-stu-id="f21fb-110">Members</span></span>

`InputTensor`

<span data-ttu-id="f21fb-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f21fb-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f21fb-112">Tensore di input da cui eseguire la lettura.</span><span class="sxs-lookup"><span data-stu-id="f21fb-112">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="f21fb-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f21fb-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f21fb-114">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="f21fb-114">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="f21fb-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="f21fb-115">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="f21fb-116">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="f21fb-116">Availability</span></span>
<span data-ttu-id="f21fb-117">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="f21fb-117">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f21fb-118">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="f21fb-118">Tensor constraints</span></span>
<span data-ttu-id="f21fb-119">*InputTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati, *DimensionCount* e *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="f21fb-119">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f21fb-120">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="f21fb-120">Tensor support</span></span>
| <span data-ttu-id="f21fb-121">Tensore</span><span class="sxs-lookup"><span data-stu-id="f21fb-121">Tensor</span></span> | <span data-ttu-id="f21fb-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="f21fb-122">Kind</span></span> | <span data-ttu-id="f21fb-123">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="f21fb-123">Supported dimension counts</span></span> | <span data-ttu-id="f21fb-124">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="f21fb-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f21fb-125">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f21fb-125">InputTensor</span></span> | <span data-ttu-id="f21fb-126">Input</span><span class="sxs-lookup"><span data-stu-id="f21fb-126">Input</span></span> | <span data-ttu-id="f21fb-127">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="f21fb-127">1 to 8</span></span> | <span data-ttu-id="f21fb-128">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f21fb-128">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="f21fb-129">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f21fb-129">OutputTensor</span></span> | <span data-ttu-id="f21fb-130">Output</span><span class="sxs-lookup"><span data-stu-id="f21fb-130">Output</span></span> | <span data-ttu-id="f21fb-131">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="f21fb-131">1 to 8</span></span> | <span data-ttu-id="f21fb-132">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f21fb-132">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="f21fb-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f21fb-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f21fb-134">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="f21fb-134">**Header**</span></span> | <span data-ttu-id="f21fb-135">directml. h</span><span class="sxs-lookup"><span data-stu-id="f21fb-135">directml.h</span></span> |