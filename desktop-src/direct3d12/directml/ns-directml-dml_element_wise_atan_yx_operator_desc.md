---
UID: NS:directml.DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
title: DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
description: Calcola l'arcotangente a 2 argomenti per ogni elemento di *ATensor* e *BTensor*, dove *ATensor* è l'asse *Y* e *BTensor* è l'asse *X*, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
ms.openlocfilehash: 6031f08dc99db943d26ab5212896b4fb44987269
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804499"
---
# <a name="dml_element_wise_atan_yx_operator_desc-directmlh"></a><span data-ttu-id="e8233-103">DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="e8233-103">DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="e8233-104">Calcola l'arcotangente a 2 argomenti per ogni elemento di *ATensor* e *BTensor*, dove *ATensor* è l'asse *Y* e *BTensor* è l'asse *X*, inserendo il risultato nell'elemento corrispondente di *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="e8233-104">Computes the 2-argument arctangent for each element of *ATensor* and *BTensor*, where *ATensor* is the *Y-axis* and *BTensor* is the *X-axis*, placing the result into the corresponding element of *OutputTensor*.</span></span> <span data-ttu-id="e8233-105">Questo operatore non è definito per l'origine, ovvero quando *ATensor* e *BTensor* sono entrambi 0 per gli elementi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="e8233-105">This operator is undefined for the origin (that is, when *ATensor* and *BTensor* are both 0 for corresponding elements).</span></span>

![GRU_Forward](../images/atan2.png)

```
f(y, x) = atan2(y, x)
```

<span data-ttu-id="e8233-107">Questo operatore supporta l'esecuzione sul posto, vale a dire che al tensore di output è consentito l'alias *ATensor* o *BTensor* durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="e8233-107">This operator supports in-place execution, meaning that the output tensor is permitted to alias *ATensor* or *BTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8233-108">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.5 e successive).</span><span class="sxs-lookup"><span data-stu-id="e8233-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="e8233-109">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="e8233-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8233-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8233-110">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="e8233-111">Members</span><span class="sxs-lookup"><span data-stu-id="e8233-111">Members</span></span>

`ATensor`

<span data-ttu-id="e8233-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e8233-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e8233-113">Tensore di input da cui leggere i valori dell'asse Y.</span><span class="sxs-lookup"><span data-stu-id="e8233-113">The input tensor to read the Y-axis values from.</span></span>

`BTensor`

<span data-ttu-id="e8233-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e8233-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e8233-115">Tensore di input da cui leggere i valori dell'asse X.</span><span class="sxs-lookup"><span data-stu-id="e8233-115">The input tensor to read the X-axis values from.</span></span>

`OutputTensor`

<span data-ttu-id="e8233-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e8233-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e8233-117">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="e8233-117">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="e8233-118">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="e8233-118">Availability</span></span>
<span data-ttu-id="e8233-119">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="e8233-119">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e8233-120">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="e8233-120">Tensor constraints</span></span>
<span data-ttu-id="e8233-121">*ATensor,* *BTensor* e *OutputTensor* devono avere gli stessi *datatype*, *DimensionCount* e *Sizes*.</span><span class="sxs-lookup"><span data-stu-id="e8233-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e8233-122">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="e8233-122">Tensor support</span></span>
| <span data-ttu-id="e8233-123">Tensore</span><span class="sxs-lookup"><span data-stu-id="e8233-123">Tensor</span></span> | <span data-ttu-id="e8233-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="e8233-124">Kind</span></span> | <span data-ttu-id="e8233-125">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="e8233-125">Supported dimension counts</span></span> | <span data-ttu-id="e8233-126">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="e8233-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e8233-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="e8233-127">ATensor</span></span> | <span data-ttu-id="e8233-128">Input</span><span class="sxs-lookup"><span data-stu-id="e8233-128">Input</span></span> | <span data-ttu-id="e8233-129">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e8233-129">1 to 8</span></span> | <span data-ttu-id="e8233-130">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e8233-130">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e8233-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="e8233-131">BTensor</span></span> | <span data-ttu-id="e8233-132">Input</span><span class="sxs-lookup"><span data-stu-id="e8233-132">Input</span></span> | <span data-ttu-id="e8233-133">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e8233-133">1 to 8</span></span> | <span data-ttu-id="e8233-134">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e8233-134">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e8233-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e8233-135">OutputTensor</span></span> | <span data-ttu-id="e8233-136">Output</span><span class="sxs-lookup"><span data-stu-id="e8233-136">Output</span></span> | <span data-ttu-id="e8233-137">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e8233-137">1 to 8</span></span> | <span data-ttu-id="e8233-138">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e8233-138">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="e8233-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8233-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e8233-140">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="e8233-140">**Header**</span></span> | <span data-ttu-id="e8233-141">directml.h</span><span class="sxs-lookup"><span data-stu-id="e8233-141">directml.h</span></span> |
