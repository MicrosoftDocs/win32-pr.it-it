---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Somma gli elementi di un tensore lungo un asse, scrivendo il conteggio di esecuzione della sommatoria nel tensore di output.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 955e70a8cfbb57995d77d73567238d082b96999b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320380"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a><span data-ttu-id="8fa3f-103">Struttura DML_CUMULATIVE_SUMMATION_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="8fa3f-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="8fa3f-104">Somma gli elementi di un tensore lungo un asse, scrivendo il conteggio di esecuzione della sommatoria nel tensore di output.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-104">Sums the elements of a tensor along an axis, writing the running tally of the summation into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8fa3f-105">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="8fa3f-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="8fa3f-106">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="8fa3f-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8fa3f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fa3f-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```



## <a name="members"></a><span data-ttu-id="8fa3f-108">Members</span><span class="sxs-lookup"><span data-stu-id="8fa3f-108">Members</span></span>

`InputTensor`

<span data-ttu-id="8fa3f-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8fa3f-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8fa3f-110">Il tensore di input contenente gli elementi da sommare.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-110">The input tensor containing elements to be summed.</span></span>


`OutputTensor`

<span data-ttu-id="8fa3f-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8fa3f-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8fa3f-112">Tensore di output in cui scrivere le sommatoria cumulative risultanti.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-112">The output tensor to write the resulting cumulative summations to.</span></span> <span data-ttu-id="8fa3f-113">Questo tensore deve avere le stesse dimensioni e il tipo di dati di *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-113">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="8fa3f-114">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="8fa3f-114">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="8fa3f-115">Indice della dimensione su cui sommare gli elementi.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-115">The index of the dimension to sum elements over.</span></span> <span data-ttu-id="8fa3f-116">Questo valore deve essere minore del valore di *DimensionCount* di *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-116">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>


`AxisDirection`

<span data-ttu-id="8fa3f-117">Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="8fa3f-117">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="8fa3f-118">Uno dei valori dell'enumerazione [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="8fa3f-118">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="8fa3f-119">Se è impostato su **DML_AXIS_DIRECTION_INCREASING**, la sommatoria si verifica attraversando il tensore lungo l'asse specificato in base all'indice dell'elemento crescente.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-119">If set to **DML_AXIS_DIRECTION_INCREASING**, then the summation occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="8fa3f-120">Se impostato su **DML_AXIS_DIRECTION_DECREASING**, il contrario è true e la sommatoria viene eseguita attraversando gli elementi in base all'indice decrescente.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-120">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true, and the summation occurs by traversing elements by descending index.</span></span>


`HasExclusiveSum`




## <a name="remarks"></a><span data-ttu-id="8fa3f-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fa3f-121">Remarks</span></span>
<span data-ttu-id="8fa3f-122">Questo operatore supporta l'esecuzione sul posto, vale a dire che *OutputTensor* è autorizzato a eseguire l'aliasing di *InputTensor* durante l'associazione.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-122">This operator supports in-place execution, meaning that the *OutputTensor* is permitted to alias the *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="8fa3f-123">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="8fa3f-123">Availability</span></span>
<span data-ttu-id="8fa3f-124">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="8fa3f-124">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="8fa3f-125">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="8fa3f-125">Tensor constraints</span></span>
<span data-ttu-id="8fa3f-126">*InputTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati e le stesse *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="8fa3f-126">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="8fa3f-127">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="8fa3f-127">Tensor support</span></span>
| <span data-ttu-id="8fa3f-128">Tensore</span><span class="sxs-lookup"><span data-stu-id="8fa3f-128">Tensor</span></span> | <span data-ttu-id="8fa3f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="8fa3f-129">Kind</span></span> | <span data-ttu-id="8fa3f-130">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="8fa3f-130">Supported dimension counts</span></span> | <span data-ttu-id="8fa3f-131">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="8fa3f-131">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8fa3f-132">InputTensor</span><span class="sxs-lookup"><span data-stu-id="8fa3f-132">InputTensor</span></span> | <span data-ttu-id="8fa3f-133">Input</span><span class="sxs-lookup"><span data-stu-id="8fa3f-133">Input</span></span> | <span data-ttu-id="8fa3f-134">4</span><span class="sxs-lookup"><span data-stu-id="8fa3f-134">4</span></span> | <span data-ttu-id="8fa3f-135">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="8fa3f-135">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="8fa3f-136">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8fa3f-136">OutputTensor</span></span> | <span data-ttu-id="8fa3f-137">Output</span><span class="sxs-lookup"><span data-stu-id="8fa3f-137">Output</span></span> | <span data-ttu-id="8fa3f-138">4</span><span class="sxs-lookup"><span data-stu-id="8fa3f-138">4</span></span> | <span data-ttu-id="8fa3f-139">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="8fa3f-139">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="8fa3f-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fa3f-140">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8fa3f-141">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="8fa3f-141">**Header**</span></span> | <span data-ttu-id="8fa3f-142">directml. h</span><span class="sxs-lookup"><span data-stu-id="8fa3f-142">directml.h</span></span> |