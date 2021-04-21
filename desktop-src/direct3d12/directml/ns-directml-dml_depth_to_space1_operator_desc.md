---
UID: NS:directml.DML_DEPTH_TO_SPACE1_OPERATOR_DESC
title: DML_DEPTH_TO_SPACE1_OPERATOR_DESC
description: Ridispone (permuta) i dati dalla profondità in blocchi di dati spaziali. L'operatore restituisce una copia del tensore di input in cui i valori della dimensione di profondità vengono spostati in blocchi spaziali alle dimensioni di altezza e larghezza.
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
ms.openlocfilehash: 89b62a9916ee77dd6907d01710624d6e9a40a20a
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803271"
---
# <a name="dml_depth_to_space1_operator_desc-structure-directmlh"></a><span data-ttu-id="42cd5-104">DML_DEPTH_TO_SPACE1_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="42cd5-104">DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="42cd5-105">Ridispone (permuta) i dati dalla profondità in blocchi di dati spaziali.</span><span class="sxs-lookup"><span data-stu-id="42cd5-105">Rearranges (permutes) data from depth into blocks of spatial data.</span></span> <span data-ttu-id="42cd5-106">L'operatore restituisce una copia del tensore di input in cui i valori della dimensione di profondità vengono spostati in blocchi spaziali alle dimensioni di altezza e larghezza.</span><span class="sxs-lookup"><span data-stu-id="42cd5-106">The operator outputs a copy of the input tensor where values from the depth dimension are moved in spatial blocks to the height and width dimensions.</span></span>

<span data-ttu-id="42cd5-107">Si tratta della trasformazione inversa di [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="42cd5-107">This is the inverse transformation of [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="42cd5-108">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="42cd5-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="42cd5-109">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="42cd5-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="42cd5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42cd5-110">Syntax</span></span>
```cpp
struct DML_DEPTH_TO_SPACE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a><span data-ttu-id="42cd5-111">Members</span><span class="sxs-lookup"><span data-stu-id="42cd5-111">Members</span></span>

`InputTensor`

<span data-ttu-id="42cd5-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="42cd5-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="42cd5-113">Tensore da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="42cd5-113">The tensor to read from.</span></span> <span data-ttu-id="42cd5-114">Le dimensioni del tensore di input sono `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="42cd5-114">The input tensor's dimensions are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`OutputTensor`

<span data-ttu-id="42cd5-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="42cd5-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="42cd5-116">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="42cd5-116">The tensor to write the results to.</span></span> <span data-ttu-id="42cd5-117">Le dimensioni del tensore di output sono `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` , dove:</span><span class="sxs-lookup"><span data-stu-id="42cd5-117">The output tensor's dimensions are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`, where:</span></span>

* <span data-ttu-id="42cd5-118">OutputChannelCount viene calcolato come InputChannelCount / ( `BlockSize`  \*  `BlockSize` )</span><span class="sxs-lookup"><span data-stu-id="42cd5-118">OutputChannelCount is computed as InputChannelCount / (`BlockSize` \* `BlockSize`)</span></span>
* <span data-ttu-id="42cd5-119">OutputHeight viene calcolato come InputHeight \* `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="42cd5-119">OutputHeight is computed as InputHeight \* `BlockSize`</span></span>
* <span data-ttu-id="42cd5-120">OutputWidth viene calcolato come InputWidth \* `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="42cd5-120">OutputWidth is computed as InputWidth \* `BlockSize`</span></span>


`BlockSize`

<span data-ttu-id="42cd5-121">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="42cd5-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="42cd5-122">Larghezza e altezza dei blocchi spostati.</span><span class="sxs-lookup"><span data-stu-id="42cd5-122">The width and height of the blocks that are moved.</span></span>


`Order`

<span data-ttu-id="42cd5-123">Tipo: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span><span class="sxs-lookup"><span data-stu-id="42cd5-123">Type: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span></span>

<span data-ttu-id="42cd5-124">Vedere [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span><span class="sxs-lookup"><span data-stu-id="42cd5-124">See [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span></span>

## <a name="examples"></a><span data-ttu-id="42cd5-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="42cd5-125">Examples</span></span>

<span data-ttu-id="42cd5-126">Gli esempi in questa sezione usano tutti l'input seguente.</span><span class="sxs-lookup"><span data-stu-id="42cd5-126">The examples in this section all use the input below.</span></span>

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

### <a name="example-1-depth-column-row-order"></a><span data-ttu-id="42cd5-127">Esempio 1.</span><span class="sxs-lookup"><span data-stu-id="42cd5-127">Example 1.</span></span> <span data-ttu-id="42cd5-128">Depth-column-row order</span><span class="sxs-lookup"><span data-stu-id="42cd5-128">Depth-column-row order</span></span>

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

### <a name="example-2-column-row-depth-order"></a><span data-ttu-id="42cd5-129">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="42cd5-129">Example 2.</span></span> <span data-ttu-id="42cd5-130">Ordine di profondità delle righe di colonna</span><span class="sxs-lookup"><span data-stu-id="42cd5-130">Column-row-depth order</span></span>

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


## <a name="remarks"></a><span data-ttu-id="42cd5-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="42cd5-131">Remarks</span></span>
<span data-ttu-id="42cd5-132">Quando *Order* è impostato su [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** equivale a [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span><span class="sxs-lookup"><span data-stu-id="42cd5-132">When *Order* is set to [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** is equivalent to [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span></span>

## <a name="availability"></a><span data-ttu-id="42cd5-133">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="42cd5-133">Availability</span></span>
<span data-ttu-id="42cd5-134">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="42cd5-134">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="42cd5-135">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="42cd5-135">Tensor constraints</span></span>
<span data-ttu-id="42cd5-136">*InputTensor* e *OutputTensor* devono avere lo stesso *tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="42cd5-136">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="42cd5-137">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="42cd5-137">Tensor support</span></span>
| <span data-ttu-id="42cd5-138">Tensore</span><span class="sxs-lookup"><span data-stu-id="42cd5-138">Tensor</span></span> | <span data-ttu-id="42cd5-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="42cd5-139">Kind</span></span> | <span data-ttu-id="42cd5-140">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="42cd5-140">Dimensions</span></span> | <span data-ttu-id="42cd5-141">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="42cd5-141">Supported dimension counts</span></span> | <span data-ttu-id="42cd5-142">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="42cd5-142">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="42cd5-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="42cd5-143">InputTensor</span></span> | <span data-ttu-id="42cd5-144">Input</span><span class="sxs-lookup"><span data-stu-id="42cd5-144">Input</span></span> | <span data-ttu-id="42cd5-145">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="42cd5-145">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="42cd5-146">4</span><span class="sxs-lookup"><span data-stu-id="42cd5-146">4</span></span> | <span data-ttu-id="42cd5-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="42cd5-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="42cd5-148">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="42cd5-148">OutputTensor</span></span> | <span data-ttu-id="42cd5-149">Output</span><span class="sxs-lookup"><span data-stu-id="42cd5-149">Output</span></span> | <span data-ttu-id="42cd5-150">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="42cd5-150">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="42cd5-151">4</span><span class="sxs-lookup"><span data-stu-id="42cd5-151">4</span></span> | <span data-ttu-id="42cd5-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="42cd5-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="42cd5-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42cd5-153">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="42cd5-154">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="42cd5-154">**Header**</span></span> | <span data-ttu-id="42cd5-155">directml.h</span><span class="sxs-lookup"><span data-stu-id="42cd5-155">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="42cd5-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42cd5-156">See also</span></span>

* [<span data-ttu-id="42cd5-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="42cd5-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_depth_to_space_operator_desc)
* [<span data-ttu-id="42cd5-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="42cd5-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)