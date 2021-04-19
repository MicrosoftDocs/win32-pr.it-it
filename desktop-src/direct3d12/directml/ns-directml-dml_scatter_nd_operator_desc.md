---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Copia l'intero tensore di input nell'output, quindi sovrascrive gli indici selezionati con i valori corrispondenti dal tensore degli aggiornamenti.
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
- DML_SCATTER_ND_OPERATOR_DESC
f1_keywords:
- DML_SCATTER_ND_OPERATOR_DESC
- directml/DML_SCATTER_ND_OPERATOR_DESC
ms.openlocfilehash: ae9a3022a7070bbf0253e71550f2ca1ceced6768
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320397"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="c050c-103">Struttura DML_SCATTER_ND_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="c050c-103">DML_SCATTER_ND_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="c050c-104">Copia l'intero tensore di input nell'output, quindi sovrascrive gli indici selezionati con i valori corrispondenti dal tensore degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="c050c-104">Copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor.</span></span> <span data-ttu-id="c050c-105">Questo operatore esegue lo pseudocodice seguente, dove "..." rappresenta una serie di coordinate, con il comportamento esatto determinato dall'asse e dalle dimensioni degli indici.</span><span class="sxs-lookup"><span data-stu-id="c050c-105">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior determined by the axis and indices size.</span></span>

```
output = input
output[indices[...]] = updates[...]
```

<span data-ttu-id="c050c-106">Se due indici di elementi di output si sovrappongono (che non è valido), non esiste alcuna garanzia di quale sia l'ultima scrittura WINS.</span><span class="sxs-lookup"><span data-stu-id="c050c-106">If two output element indices overlap (which is invalid), there is no guarantee of which last write wins.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c050c-107">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="c050c-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="c050c-108">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="c050c-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c050c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c050c-109">Syntax</span></span>
```cpp
struct DML_SCATTER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *UpdatesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="c050c-110">Members</span><span class="sxs-lookup"><span data-stu-id="c050c-110">Members</span></span>

`InputTensor`

<span data-ttu-id="c050c-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c050c-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c050c-112">Tensore da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="c050c-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="c050c-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c050c-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c050c-114">Un tensore contenente gli indici.</span><span class="sxs-lookup"><span data-stu-id="c050c-114">A tensor containing the indices.</span></span> <span data-ttu-id="c050c-115">Il *DimensionCount* di questo tensore deve corrispondere a *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="c050c-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="c050c-116">L'ultima dimensione di *IndicesTensor* è in realtà il numero di coordinate per tupla dell'indice e non deve superare *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="c050c-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it mustn't exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="c050c-117">Ad esempio, un tensore indici di dimensioni `{1,4,5,2}` con *IndicesDimensionCount* = 3 indica una matrice 4x5 di Tuple coordinate a 2 valori che indicizzano in *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="c050c-117">For example, an indices tensor of size `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-value coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="c050c-118">A partire da `DML_FEATURE_LEVEL_3_0` , questo operatore supporta valori di indice negativi quando si usa un tipo integrale con segno con questo tensore.</span><span class="sxs-lookup"><span data-stu-id="c050c-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="c050c-119">Gli indici negativi vengono interpretati come relativi alla fine della rispettiva dimensione.</span><span class="sxs-lookup"><span data-stu-id="c050c-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="c050c-120">Ad esempio, un indice di-1 si riferisce all'ultimo elemento lungo la dimensione.</span><span class="sxs-lookup"><span data-stu-id="c050c-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`UpdatesTensor`

<span data-ttu-id="c050c-121">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c050c-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c050c-122">Un tensore contenente i nuovi valori per sostituire i valori di input esistenti in corrispondenza degli indici corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="c050c-122">A tensor containing the new values to replace the existing input values at the corresponding indices.</span></span> <span data-ttu-id="c050c-123">Il *DimensionCount* di questo tensore deve corrispondere a *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="c050c-123">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="c050c-124">Il *UpdatesTensor. sizes* previsto è la concatenazione dei segmenti iniziali *IndicesTensor. sizes* e del segmento finale *InputTensor. sizes* per produrre quanto segue.</span><span class="sxs-lookup"><span data-stu-id="c050c-124">The expected *UpdatesTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

<span data-ttu-id="c050c-125">Le dimensioni sono allineate a destra, con 1 valori iniziali anteposti se necessario per soddisfare *UpdatesTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="c050c-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *UpdatesTensor.DimensionCount*.</span></span>

<span data-ttu-id="c050c-126">Ecco un esempio.</span><span class="sxs-lookup"><span data-stu-id="c050c-126">Here's an example.</span></span>

```
InputTensor.Sizes = [3,4,5,6,7]
InputDimensionCount = 5
IndicesTensor.Sizes = [1,1, 1,2,3]
IndicesDimensionCount = 3 // can be thought of as a [1,2] array of 3-coordinate tuples

// The [1,2] comes from the indices tensor (ignoring last dimension, which is the tuple size),
// and the [6,7] comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
UpdatesTensor.Sizes = [1, 1,2,6,7]
```


`OutputTensor`

<span data-ttu-id="c050c-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c050c-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c050c-128">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="c050c-128">The tensor to write the results to.</span></span> <span data-ttu-id="c050c-129">Le *dimensioni* e il *tipo* di dati di questo tensore devono corrispondere a *InputTensor. sizes*.</span><span class="sxs-lookup"><span data-stu-id="c050c-129">The *Sizes* and *DataType* of this tensor must match *InputTensor.Sizes*.</span></span>


`InputDimensionCount`

<span data-ttu-id="c050c-130">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c050c-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="c050c-131">Il numero di dimensioni di input effettive all'interno di *InputTensor* dopo aver ignorato gli eventuali primitivi irrilevanti, che includono [1, *InputTensor. DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="c050c-131">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging [1, *InputTensor.DimensionCount*).</span></span> <span data-ttu-id="c050c-132">Ad esempio, dato *InputTensor. sizes* = {1,1,4,6} e *InputDimensionCount* = 3, gli indici significativi effettivi sono {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="c050c-132">For example, given *InputTensor.Sizes* = {1,1,4,6} and *InputDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="c050c-133">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c050c-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="c050c-134">Il numero di dimensioni effettive dell'indice all'interno di *IndicesTensor* dopo aver ignorato gli eventuali primitivi irrilevanti, che vanno da [1, *IndicesTensor. DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="c050c-134">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="c050c-135">Ad esempio, dato *IndicesTensor. sizes* = {1,1,4,6} e *IndicesDimensionCount* = 3, gli indici significativi effettivi sono {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="c050c-135">For example, given *IndicesTensor.Sizes* = {1,1,4,6} and *IndicesDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>

## <a name="examples"></a><span data-ttu-id="c050c-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="c050c-136">Examples</span></span>

```
InputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 2, 3, 4, 5, 6, 7, 8]

IndicesTensor: (Sizes:{4,1}, DataType:FLOAT32)
    [[4], [3], [1], [7]]

UpdatesTensor: (Sizes:{4}, DataType:FLOAT32)
    [9, 10, 11, 12]

// output = input
// output[indices[x, 0]] = updates[x]
OutputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 11, 3, 10, 9, 6, 7, 12]
```

## <a name="availability"></a><span data-ttu-id="c050c-137">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="c050c-137">Availability</span></span>
<span data-ttu-id="c050c-138">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="c050c-138">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="c050c-139">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="c050c-139">Tensor constraints</span></span>
* <span data-ttu-id="c050c-140">*IndicesTensor*, *InputTensor*, *OutputTensor* e `UpdatesTensor` devono avere lo stesso *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="c050c-140">*IndicesTensor*, *InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="c050c-141">*InputTensor*, *OutputTensor* e `UpdatesTensor` devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="c050c-141">*InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="c050c-142">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="c050c-142">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="c050c-143">DML_FEATURE_LEVEL_3_0 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="c050c-143">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="c050c-144">Tensore</span><span class="sxs-lookup"><span data-stu-id="c050c-144">Tensor</span></span> | <span data-ttu-id="c050c-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="c050c-145">Kind</span></span> | <span data-ttu-id="c050c-146">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="c050c-146">Supported dimension counts</span></span> | <span data-ttu-id="c050c-147">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="c050c-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c050c-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="c050c-148">InputTensor</span></span> | <span data-ttu-id="c050c-149">Input</span><span class="sxs-lookup"><span data-stu-id="c050c-149">Input</span></span> | <span data-ttu-id="c050c-150">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="c050c-150">1 to 8</span></span> | <span data-ttu-id="c050c-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c050c-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c050c-152">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="c050c-152">IndicesTensor</span></span> | <span data-ttu-id="c050c-153">Input</span><span class="sxs-lookup"><span data-stu-id="c050c-153">Input</span></span> | <span data-ttu-id="c050c-154">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="c050c-154">1 to 8</span></span> | <span data-ttu-id="c050c-155">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="c050c-155">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="c050c-156">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="c050c-156">UpdatesTensor</span></span> | <span data-ttu-id="c050c-157">Input</span><span class="sxs-lookup"><span data-stu-id="c050c-157">Input</span></span> | <span data-ttu-id="c050c-158">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="c050c-158">1 to 8</span></span> | <span data-ttu-id="c050c-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c050c-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c050c-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="c050c-160">OutputTensor</span></span> | <span data-ttu-id="c050c-161">Output</span><span class="sxs-lookup"><span data-stu-id="c050c-161">Output</span></span> | <span data-ttu-id="c050c-162">da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="c050c-162">1 to 8</span></span> | <span data-ttu-id="c050c-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c050c-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="c050c-164">DML_FEATURE_LEVEL_2_1 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="c050c-164">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="c050c-165">Tensore</span><span class="sxs-lookup"><span data-stu-id="c050c-165">Tensor</span></span> | <span data-ttu-id="c050c-166">Tipo</span><span class="sxs-lookup"><span data-stu-id="c050c-166">Kind</span></span> | <span data-ttu-id="c050c-167">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="c050c-167">Supported dimension counts</span></span> | <span data-ttu-id="c050c-168">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="c050c-168">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c050c-169">InputTensor</span><span class="sxs-lookup"><span data-stu-id="c050c-169">InputTensor</span></span> | <span data-ttu-id="c050c-170">Input</span><span class="sxs-lookup"><span data-stu-id="c050c-170">Input</span></span> | <span data-ttu-id="c050c-171">4</span><span class="sxs-lookup"><span data-stu-id="c050c-171">4</span></span> | <span data-ttu-id="c050c-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c050c-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c050c-173">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="c050c-173">IndicesTensor</span></span> | <span data-ttu-id="c050c-174">Input</span><span class="sxs-lookup"><span data-stu-id="c050c-174">Input</span></span> | <span data-ttu-id="c050c-175">4</span><span class="sxs-lookup"><span data-stu-id="c050c-175">4</span></span> | <span data-ttu-id="c050c-176">UINT32</span><span class="sxs-lookup"><span data-stu-id="c050c-176">UINT32</span></span> |
| <span data-ttu-id="c050c-177">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="c050c-177">UpdatesTensor</span></span> | <span data-ttu-id="c050c-178">Input</span><span class="sxs-lookup"><span data-stu-id="c050c-178">Input</span></span> | <span data-ttu-id="c050c-179">4</span><span class="sxs-lookup"><span data-stu-id="c050c-179">4</span></span> | <span data-ttu-id="c050c-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c050c-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c050c-181">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="c050c-181">OutputTensor</span></span> | <span data-ttu-id="c050c-182">Output</span><span class="sxs-lookup"><span data-stu-id="c050c-182">Output</span></span> | <span data-ttu-id="c050c-183">4</span><span class="sxs-lookup"><span data-stu-id="c050c-183">4</span></span> | <span data-ttu-id="c050c-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c050c-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="c050c-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c050c-185">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c050c-186">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="c050c-186">**Header**</span></span> | <span data-ttu-id="c050c-187">directml. h</span><span class="sxs-lookup"><span data-stu-id="c050c-187">directml.h</span></span> |