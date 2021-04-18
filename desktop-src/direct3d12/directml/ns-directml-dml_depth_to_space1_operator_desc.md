---
UID: NS:directml.DML_DEPTH_TO_SPACE1_OPERATOR_DESC
title: DML_DEPTH_TO_SPACE1_OPERATOR_DESC
description: Riorganizza i dati (permuta) dalla profondità in blocchi di dati spaziali. L'operatore restituisce una copia del tensore di input in cui i valori della dimensione di profondità vengono spostati in blocchi spaziali fino alle dimensioni di altezza e larghezza.
helpviewer_keywords:
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure
- direct3d12.dml_depth_to_space1_operator_desc
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.openlocfilehash: 639bda0b8d398d24b01649635d3cfcbd2301a211
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320409"
---
# <a name="dml_depth_to_space1_operator_desc-structure-directmlh"></a><span data-ttu-id="9a5a2-104">Struttura DML_DEPTH_TO_SPACE1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="9a5a2-104">DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="9a5a2-105">Riorganizza i dati (permuta) dalla profondità in blocchi di dati spaziali.</span><span class="sxs-lookup"><span data-stu-id="9a5a2-105">Rearranges (permutes) data from depth into blocks of spatial data.</span></span> <span data-ttu-id="9a5a2-106">L'operatore restituisce una copia del tensore di input in cui i valori della dimensione di profondità vengono spostati in blocchi spaziali fino alle dimensioni di altezza e larghezza.</span><span class="sxs-lookup"><span data-stu-id="9a5a2-106">The operator outputs a copy of the input tensor where values from the depth dimension are moved in spatial blocks to the height and width dimensions.</span></span>

<span data-ttu-id="9a5a2-107">Si tratta della trasformazione inversa del [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="9a5a2-107">This is the inverse transformation of [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a5a2-108">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="9a5a2-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="9a5a2-109">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="9a5a2-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9a5a2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a5a2-110">Syntax</span></span>
```cpp
struct DML_DEPTH_TO_SPACE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a><span data-ttu-id="9a5a2-111">Members</span><span class="sxs-lookup"><span data-stu-id="9a5a2-111">Members</span></span>

`InputTensor`

<span data-ttu-id="9a5a2-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9a5a2-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9a5a2-113">Tensore da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="9a5a2-113">The tensor to read from.</span></span> <span data-ttu-id="9a5a2-114">Le dimensioni del tensore di input sono `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="9a5a2-114">The input tensor's dimensions are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`OutputTensor`

<span data-ttu-id="9a5a2-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9a5a2-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9a5a2-116">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="9a5a2-116">The tensor to write the results to.</span></span> <span data-ttu-id="9a5a2-117">Le dimensioni del tensore di output sono `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` , dove:</span><span class="sxs-lookup"><span data-stu-id="9a5a2-117">The output tensor's dimensions are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`, where:</span></span>

* <span data-ttu-id="9a5a2-118">OutputChannelCount viene calcolato come InputChannelCount/( `BlockSize`  \*  `BlockSize` )</span><span class="sxs-lookup"><span data-stu-id="9a5a2-118">OutputChannelCount is computed as InputChannelCount / (`BlockSize` \* `BlockSize`)</span></span>
* <span data-ttu-id="9a5a2-119">OutputHeight viene calcolato come InputHeight \* `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="9a5a2-119">OutputHeight is computed as InputHeight \* `BlockSize`</span></span>
* <span data-ttu-id="9a5a2-120">OutputWidth viene calcolato come InputWidth \* `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="9a5a2-120">OutputWidth is computed as InputWidth \* `BlockSize`</span></span>


`BlockSize`

<span data-ttu-id="9a5a2-121">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="9a5a2-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="9a5a2-122">Larghezza e altezza dei blocchi spostati.</span><span class="sxs-lookup"><span data-stu-id="9a5a2-122">The width and height of the blocks that are moved.</span></span>


`Order`

<span data-ttu-id="9a5a2-123">Tipo: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span><span class="sxs-lookup"><span data-stu-id="9a5a2-123">Type: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span></span>

<span data-ttu-id="9a5a2-124">Vedere [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span><span class="sxs-lookup"><span data-stu-id="9a5a2-124">See [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9a5a2-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="9a5a2-125">Examples</span></span>

<span data-ttu-id="9a5a2-126">Gli esempi in questa sezione usano tutti l'input riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="9a5a2-126">The examples in this section all use the input below.</span></span>

```
InputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
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

### <a name="example-1-depth-column-row-order"></a><span data-ttu-id="9a5a2-127">Esempio 1.</span><span class="sxs-lookup"><span data-stu-id="9a5a2-127">Example 1.</span></span> <span data-ttu-id="9a5a2-128">Ordine della riga di colonna Depth</span><span class="sxs-lookup"><span data-stu-id="9a5a2-128">Depth-column-row order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]
```

### <a name="example-2-column-row-depth-order"></a><span data-ttu-id="9a5a2-129">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="9a5a2-129">Example 2.</span></span> <span data-ttu-id="9a5a2-130">Ordine di profondità colonna-riga</span><span class="sxs-lookup"><span data-stu-id="9a5a2-130">Column-row-depth order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
[[[[ 0,  9,  1, 10,  2, 11],
   [18, 27, 19, 28, 20, 29],
   [ 3, 12,  4, 13,  5, 14],
   [21, 30, 22, 31, 23, 32]],
  [[36, 45, 37, 46, 38, 47],
   [54, 63, 55, 64, 56, 65],
   [39, 48, 40, 49, 41, 50],
   [57, 66, 58, 67, 59, 68]]]]
```


## <a name="remarks"></a><span data-ttu-id="9a5a2-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a5a2-131">Remarks</span></span>
<span data-ttu-id="9a5a2-132">Quando *Order* è impostato su [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** è equivalente a [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span><span class="sxs-lookup"><span data-stu-id="9a5a2-132">When *Order* is set to [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** is equivalent to [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span></span>

## <a name="availability"></a><span data-ttu-id="9a5a2-133">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="9a5a2-133">Availability</span></span>
<span data-ttu-id="9a5a2-134">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="9a5a2-134">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="9a5a2-135">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="9a5a2-135">Tensor constraints</span></span>
<span data-ttu-id="9a5a2-136">*InputTensor* e *OutputTensor* devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="9a5a2-136">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="9a5a2-137">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="9a5a2-137">Tensor support</span></span>
| <span data-ttu-id="9a5a2-138">Tensore</span><span class="sxs-lookup"><span data-stu-id="9a5a2-138">Tensor</span></span> | <span data-ttu-id="9a5a2-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a5a2-139">Kind</span></span> | <span data-ttu-id="9a5a2-140">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="9a5a2-140">Dimensions</span></span> | <span data-ttu-id="9a5a2-141">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="9a5a2-141">Supported dimension counts</span></span> | <span data-ttu-id="9a5a2-142">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="9a5a2-142">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="9a5a2-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="9a5a2-143">InputTensor</span></span> | <span data-ttu-id="9a5a2-144">Input</span><span class="sxs-lookup"><span data-stu-id="9a5a2-144">Input</span></span> | <span data-ttu-id="9a5a2-145">{BatchCount, InputChannelCount, InputHeight, InputWidth}</span><span class="sxs-lookup"><span data-stu-id="9a5a2-145">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="9a5a2-146">4</span><span class="sxs-lookup"><span data-stu-id="9a5a2-146">4</span></span> | <span data-ttu-id="9a5a2-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="9a5a2-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="9a5a2-148">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="9a5a2-148">OutputTensor</span></span> | <span data-ttu-id="9a5a2-149">Output</span><span class="sxs-lookup"><span data-stu-id="9a5a2-149">Output</span></span> | <span data-ttu-id="9a5a2-150">{BatchCount, OutputChannelCount, OutputHeight, OutputWidth}</span><span class="sxs-lookup"><span data-stu-id="9a5a2-150">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="9a5a2-151">4</span><span class="sxs-lookup"><span data-stu-id="9a5a2-151">4</span></span> | <span data-ttu-id="9a5a2-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="9a5a2-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="9a5a2-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a5a2-153">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9a5a2-154">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="9a5a2-154">**Header**</span></span> | <span data-ttu-id="9a5a2-155">directml. h</span><span class="sxs-lookup"><span data-stu-id="9a5a2-155">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="9a5a2-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a5a2-156">See also</span></span>

* [<span data-ttu-id="9a5a2-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="9a5a2-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_depth_to_space_operator_desc)
* [<span data-ttu-id="9a5a2-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="9a5a2-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)