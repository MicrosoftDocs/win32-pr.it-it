---
UID: NS:directml.DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
title: DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
description: Riempie un tensore con la costante *Value specificata.*
helpviewer_keywords:
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure
- direct3d12.dml_fill_value_constant_operator_desc
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
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
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
ms.openlocfilehash: 4fe9f766fc48a4b1ca0d32082dcd8a5f67591195
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803026"
---
# <a name="dml_fill_value_constant_operator_desc-structure-directmlh"></a><span data-ttu-id="b9504-103">DML_FILL_VALUE_CONSTANT_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="b9504-103">DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b9504-104">Riempie un tensore con la costante *Value specificata.*</span><span class="sxs-lookup"><span data-stu-id="b9504-104">Fills a tensor with the given constant *Value*.</span></span> <span data-ttu-id="b9504-105">Questo operatore esegue lo pseudocodice seguente.</span><span class="sxs-lookup"><span data-stu-id="b9504-105">This operator performs the following pseudocode.</span></span>

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
endfor
```

> [!IMPORTANT]
> <span data-ttu-id="b9504-106">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="b9504-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b9504-107">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="b9504-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9504-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9504-108">Syntax</span></span>
```cpp
struct DML_FILL_VALUE_CONSTANT_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      Value;
};
```



## <a name="members"></a><span data-ttu-id="b9504-109">Members</span><span class="sxs-lookup"><span data-stu-id="b9504-109">Members</span></span>

`OutputTensor`

<span data-ttu-id="b9504-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b9504-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b9504-111">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="b9504-111">The tensor to write the results to.</span></span> <span data-ttu-id="b9504-112">Questo tensore può avere qualsiasi dimensione.</span><span class="sxs-lookup"><span data-stu-id="b9504-112">This tensor may have any size.</span></span>


`ValueDataType`

<span data-ttu-id="b9504-113">Tipo: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span><span class="sxs-lookup"><span data-stu-id="b9504-113">Type: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span></span>

<span data-ttu-id="b9504-114">Tipo di dati del *campo Value,* che deve corrispondere *a OutputTensor.DataType*.</span><span class="sxs-lookup"><span data-stu-id="b9504-114">The data type of the *Value* field, which must match *OutputTensor.DataType*.</span></span>


`Value`

<span data-ttu-id="b9504-115">Tipo: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="b9504-115">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="b9504-116">Valore costante per riempire l'output, con *ValueDataType che* determina come interpretare il campo.</span><span class="sxs-lookup"><span data-stu-id="b9504-116">A constant value to fill the output, with *ValueDataType* determining how to interpret the field.</span></span>

## <a name="examples"></a><span data-ttu-id="b9504-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="b9504-117">Examples</span></span>

```
Value = 13.0

OutputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
    [[[[13.0f, 13.0f, 13.0f, 13.0f],
       [13.0f, 13.0f, 13.0f, 13.0f]]]]
```

## <a name="availability"></a><span data-ttu-id="b9504-118">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="b9504-118">Availability</span></span>
<span data-ttu-id="b9504-119">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="b9504-119">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b9504-120">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="b9504-120">Tensor support</span></span>
| <span data-ttu-id="b9504-121">Tensore</span><span class="sxs-lookup"><span data-stu-id="b9504-121">Tensor</span></span> | <span data-ttu-id="b9504-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9504-122">Kind</span></span> | <span data-ttu-id="b9504-123">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="b9504-123">Supported dimension counts</span></span> | <span data-ttu-id="b9504-124">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="b9504-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b9504-125">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b9504-125">OutputTensor</span></span> | <span data-ttu-id="b9504-126">Output</span><span class="sxs-lookup"><span data-stu-id="b9504-126">Output</span></span> | <span data-ttu-id="b9504-127">4</span><span class="sxs-lookup"><span data-stu-id="b9504-127">4</span></span> | <span data-ttu-id="b9504-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b9504-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="b9504-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9504-129">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b9504-130">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="b9504-130">**Header**</span></span> | <span data-ttu-id="b9504-131">directml.h</span><span class="sxs-lookup"><span data-stu-id="b9504-131">directml.h</span></span> |