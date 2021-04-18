---
UID: NS:directml.DML_SPACE_TO_DEPTH1_OPERATOR_DESC
title: DML_SPACE_TO_DEPTH1_OPERATOR_DESC
description: Riorganizza i blocchi di dati spaziali in profondità. L'operatore restituisce una copia del tensore di input in cui i valori delle dimensioni Height e Width vengono spostati nella dimensione Depth.
helpviewer_keywords:
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC structure
- direct3d12.dml_space_to_depth1_operator_desc
- directml/DML_SPACE_TO_DEPTH1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
- directml/DML_SPACE_TO_DEPTH1_OPERATOR_DESC
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
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
ms.openlocfilehash: 9c5033440e65dacdcb815edd08994b79a5fae41a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320376"
---
# <a name="dml_space_to_depth1_operator_desc-structure-directmlh"></a><span data-ttu-id="e1f0b-104">Struttura DML_SPACE_TO_DEPTH1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="e1f0b-104">DML_SPACE_TO_DEPTH1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="e1f0b-105">Riorganizza i blocchi di dati spaziali in profondità.</span><span class="sxs-lookup"><span data-stu-id="e1f0b-105">Rearranges blocks of spatial data into depth.</span></span> <span data-ttu-id="e1f0b-106">L'operatore restituisce una copia del tensore di input in cui i valori delle dimensioni Height e Width vengono spostati nella dimensione Depth.</span><span class="sxs-lookup"><span data-stu-id="e1f0b-106">The operator outputs a copy of the input tensor where values from the height and width dimensions are moved to the depth dimension.</span></span>

<span data-ttu-id="e1f0b-107">Si tratta della trasformazione inversa del [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="e1f0b-107">This is the inverse transformation of [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e1f0b-108">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="e1f0b-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="e1f0b-109">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e1f0b-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e1f0b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1f0b-110">Syntax</span></span>
```cpp
struct DML_SPACE_TO_DEPTH1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a><span data-ttu-id="e1f0b-111">Members</span><span class="sxs-lookup"><span data-stu-id="e1f0b-111">Members</span></span>

`InputTensor`

<span data-ttu-id="e1f0b-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e1f0b-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e1f0b-113">Tensore da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="e1f0b-113">The tensor to read from.</span></span> <span data-ttu-id="e1f0b-114">Le dimensioni del tensore di input sono `{ Batch, Channels, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="e1f0b-114">The input tensor's dimensions are `{ Batch, Channels, Height, Width }`.</span></span>


`OutputTensor`

<span data-ttu-id="e1f0b-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e1f0b-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e1f0b-116">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="e1f0b-116">The tensor to write the results to.</span></span> <span data-ttu-id="e1f0b-117">Le dimensioni del tensore di output sono `{ Batch, Channels / (BlockSize * BlockSize), Height * BlockSize, Width * BlockSize }` .</span><span class="sxs-lookup"><span data-stu-id="e1f0b-117">The output tensor's dimensions are `{ Batch, Channels / (BlockSize * BlockSize), Height * BlockSize, Width * BlockSize }`.</span></span>


`BlockSize`

<span data-ttu-id="e1f0b-118">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="e1f0b-118">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="e1f0b-119">Larghezza e altezza dei blocchi spostati.</span><span class="sxs-lookup"><span data-stu-id="e1f0b-119">The width and height of the Blocks that are moved.</span></span>


`Order`

<span data-ttu-id="e1f0b-120">Tipo: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span><span class="sxs-lookup"><span data-stu-id="e1f0b-120">Type: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span></span>

<span data-ttu-id="e1f0b-121">Vedere [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span><span class="sxs-lookup"><span data-stu-id="e1f0b-121">See [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e1f0b-122">Esempi</span><span class="sxs-lookup"><span data-stu-id="e1f0b-122">Examples</span></span>

### <a name="example-1-depth-column-row-order"></a><span data-ttu-id="e1f0b-123">Esempio 1.</span><span class="sxs-lookup"><span data-stu-id="e1f0b-123">Example 1.</span></span> <span data-ttu-id="e1f0b-124">Ordine della riga di colonna Depth</span><span class="sxs-lookup"><span data-stu-id="e1f0b-124">Depth-column-row order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW
InputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]

OutputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```

### <a name="example-2-column-row-depth-order"></a><span data-ttu-id="e1f0b-125">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="e1f0b-125">Example 2.</span></span> <span data-ttu-id="e1f0b-126">Ordine di profondità colonna-riga</span><span class="sxs-lookup"><span data-stu-id="e1f0b-126">Column-row-depth order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
InputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
[[[[ 0,  9,  1, 10,  2, 11],
   [18, 27, 19, 28, 20, 29],
   [ 3, 12,  4, 13,  5, 14],
   [21, 30, 22, 31, 23, 32]],
  [[36, 45, 37, 46, 38, 47],
   [54, 63, 55, 64, 56, 65],
   [39, 48, 40, 49, 41, 50],
   [57, 66, 58, 67, 59, 68]]]]
OutputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```


## <a name="remarks"></a><span data-ttu-id="e1f0b-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1f0b-127">Remarks</span></span>
<span data-ttu-id="e1f0b-128">Quando il parametro *Order* è impostato su [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), questo operatore è equivalente a [DML_SPACE_TO_DEPTH_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="e1f0b-128">When the *Order* parameter is set to [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), this operator is equivalent to [DML_SPACE_TO_DEPTH_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="e1f0b-129">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="e1f0b-129">Availability</span></span>
<span data-ttu-id="e1f0b-130">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="e1f0b-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e1f0b-131">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="e1f0b-131">Tensor constraints</span></span>
<span data-ttu-id="e1f0b-132">*InputTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="e1f0b-132">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e1f0b-133">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="e1f0b-133">Tensor support</span></span>
| <span data-ttu-id="e1f0b-134">Tensore</span><span class="sxs-lookup"><span data-stu-id="e1f0b-134">Tensor</span></span> | <span data-ttu-id="e1f0b-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1f0b-135">Kind</span></span> | <span data-ttu-id="e1f0b-136">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="e1f0b-136">Dimensions</span></span> | <span data-ttu-id="e1f0b-137">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="e1f0b-137">Supported dimension counts</span></span> | <span data-ttu-id="e1f0b-138">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="e1f0b-138">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="e1f0b-139">InputTensor</span><span class="sxs-lookup"><span data-stu-id="e1f0b-139">InputTensor</span></span> | <span data-ttu-id="e1f0b-140">Input</span><span class="sxs-lookup"><span data-stu-id="e1f0b-140">Input</span></span> | <span data-ttu-id="e1f0b-141">{BatchCount, InputChannelCount, InputHeight, InputWidth}</span><span class="sxs-lookup"><span data-stu-id="e1f0b-141">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="e1f0b-142">4</span><span class="sxs-lookup"><span data-stu-id="e1f0b-142">4</span></span> | <span data-ttu-id="e1f0b-143">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e1f0b-143">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e1f0b-144">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e1f0b-144">OutputTensor</span></span> | <span data-ttu-id="e1f0b-145">Output</span><span class="sxs-lookup"><span data-stu-id="e1f0b-145">Output</span></span> | <span data-ttu-id="e1f0b-146">{BatchCount, OutputChannelCount, OutputHeight, OutputWidth}</span><span class="sxs-lookup"><span data-stu-id="e1f0b-146">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="e1f0b-147">4</span><span class="sxs-lookup"><span data-stu-id="e1f0b-147">4</span></span> | <span data-ttu-id="e1f0b-148">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e1f0b-148">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="e1f0b-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1f0b-149">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e1f0b-150">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="e1f0b-150">**Header**</span></span> | <span data-ttu-id="e1f0b-151">directml. h</span><span class="sxs-lookup"><span data-stu-id="e1f0b-151">directml.h</span></span> |