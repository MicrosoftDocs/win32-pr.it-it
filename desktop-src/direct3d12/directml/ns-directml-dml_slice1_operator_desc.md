---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Estrae una singola sottoarea (una "sezione") di un tensore di input.
helpviewer_keywords:
- DML_SLICE1_OPERATOR_DESC
- DML_SLICE1_OPERATOR_DESC structure
- direct3d12.dml_slice1_operator_desc
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
ms.openlocfilehash: f34525865be9541da879e66e88c29d4a2ab74f00
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417456"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a><span data-ttu-id="588e3-103">DML_SLICE1_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="588e3-103">DML_SLICE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="588e3-104">Estrae una singola sottoarea (una "sezione") di un tensore di input.</span><span class="sxs-lookup"><span data-stu-id="588e3-104">Extracts a single subregion (a "slice") of an input tensor.</span></span>

<span data-ttu-id="588e3-105">La *finestra di input* descrive i limiti del tensore di input da considerare nella sezione.</span><span class="sxs-lookup"><span data-stu-id="588e3-105">The *input window* describes the bounds of the input tensor to consider in the slice.</span></span> <span data-ttu-id="588e3-106">La finestra viene definita usando tre valori per ogni dimensione.</span><span class="sxs-lookup"><span data-stu-id="588e3-106">The window is defined using three values for each dimension.</span></span>

- <span data-ttu-id="588e3-107">*L'offset* *contrassegna l'inizio della finestra* in una dimensione.</span><span class="sxs-lookup"><span data-stu-id="588e3-107">The *offset* marks the *beginning of the window* in a dimension.</span></span>
- <span data-ttu-id="588e3-108">Le *dimensioni* contrassegnano l'estensione della finestra in una dimensione.</span><span class="sxs-lookup"><span data-stu-id="588e3-108">The *size* marks the extent of the window in a dimension.</span></span> <span data-ttu-id="588e3-109">La *fine della finestra in* una dimensione è `offset + size - 1` .</span><span class="sxs-lookup"><span data-stu-id="588e3-109">The *end of the window* in a dimension is `offset + size - 1`.</span></span>
- <span data-ttu-id="588e3-110">Lo *stride* indica come attraversare gli elementi in una dimensione.</span><span class="sxs-lookup"><span data-stu-id="588e3-110">The *stride* indicates how to traverse the elements in a dimension.</span></span>
  - <span data-ttu-id="588e3-111">La grandezza dello stride indica il numero di elementi da avanzare durante la copia all'interno della finestra.</span><span class="sxs-lookup"><span data-stu-id="588e3-111">The magnitude of the stride indicates how many elements to advance when copying within the window.</span></span>
  - <span data-ttu-id="588e3-112">Se uno stride è positivo, gli  elementi vengono copiati a partire dall'inizio della finestra nella dimensione.</span><span class="sxs-lookup"><span data-stu-id="588e3-112">If a stride is positive, elements are copied starting at the *beginning* of the window in the dimension.</span></span>
  - <span data-ttu-id="588e3-113">Se uno stride è negativo, gli elementi vengono copiati a partire dalla *fine* della finestra nella dimensione.</span><span class="sxs-lookup"><span data-stu-id="588e3-113">If a stride is negative, elements are copied starting at the *end* of the window in the dimension.</span></span>

<span data-ttu-id="588e3-114">Lo pseudocodice seguente illustra come vengono copiati gli elementi usando la finestra di input.</span><span class="sxs-lookup"><span data-stu-id="588e3-114">The following pseudo-code illustrates how elements are copied using the input window.</span></span> <span data-ttu-id="588e3-115">Si noti come gli elementi di una dimensione vengono copiati dall'inizio alla fine con uno stride positivo e copiati dall'inizio all'inizio con uno stride negativo.</span><span class="sxs-lookup"><span data-stu-id="588e3-115">Note how elements in a dimension are copied from start to end with a positive stride, and copied from end to start with a negative stride.</span></span>

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

<span data-ttu-id="588e3-116">La finestra di input non deve essere vuota in nessuna dimensione e la finestra non deve estendersi oltre le dimensioni del tensore di input (non sono consentite le operazioni di lettura fuori limite).</span><span class="sxs-lookup"><span data-stu-id="588e3-116">The input window mustn't be empty in any dimension, and the window mustn't extend beyond the dimensions of the input tensor (out-of-bounds reads aren't permitted).</span></span> <span data-ttu-id="588e3-117">Le dimensioni e gli stride della finestra limitano in modo efficace il numero di elementi che possono essere copiati da ogni dimensione `i` del tensore di input.</span><span class="sxs-lookup"><span data-stu-id="588e3-117">The window's size and strides effectively limit the number of elements that may be copied from each dimension `i` of the input tensor.</span></span>

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

<span data-ttu-id="588e3-118">Il tensore di output non è necessario per copiare tutti gli elementi raggiungibili all'interno della finestra.</span><span class="sxs-lookup"><span data-stu-id="588e3-118">The output tensor isn't required to copy all reachable elements within the window.</span></span> <span data-ttu-id="588e3-119">La sezione è valida purché `1 <= OutputSizes[i] <= MaxCopiedElements[i]` .</span><span class="sxs-lookup"><span data-stu-id="588e3-119">The slice is valid so long as `1 <= OutputSizes[i] <= MaxCopiedElements[i]`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="588e3-120">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="588e3-120">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="588e3-121">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="588e3-121">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="588e3-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="588e3-122">Syntax</span></span>
```cpp
struct DML_SLICE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *InputWindowOffsets;
  const UINT            *InputWindowSizes;
  const INT             *InputWindowStrides;
};
```



## <a name="members"></a><span data-ttu-id="588e3-123">Members</span><span class="sxs-lookup"><span data-stu-id="588e3-123">Members</span></span>

`InputTensor`

<span data-ttu-id="588e3-124">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="588e3-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="588e3-125">Tensore da cui estrarre le sezioni.</span><span class="sxs-lookup"><span data-stu-id="588e3-125">The tensor to extract slices from.</span></span>


`OutputTensor`

<span data-ttu-id="588e3-126">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="588e3-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="588e3-127">Tensore in cui scrivere i risultati dei dati sezionati.</span><span class="sxs-lookup"><span data-stu-id="588e3-127">The tensor to write the sliced data results to.</span></span>


`DimensionCount`

<span data-ttu-id="588e3-128">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="588e3-128">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="588e3-129">Numero di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="588e3-129">The number of dimensions.</span></span> <span data-ttu-id="588e3-130">Questo campo determina le dimensioni delle matrici *InputWindowOffsets,* *InputWindowSizes* e *InputWindowStrides.*</span><span class="sxs-lookup"><span data-stu-id="588e3-130">This field determines the size of the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="588e3-131">Questo valore deve corrispondere a *DimensionCount* dei tensori di input e output.</span><span class="sxs-lookup"><span data-stu-id="588e3-131">This value must match the *DimensionCount* of the input and output tensors.</span></span> <span data-ttu-id="588e3-132">Questo valore deve essere compreso tra 1 e 8, in modo inclusivo, a partire da . I livelli di funzionalità precedenti richiedono un valore `DML_FEATURE_LEVEL_3_0` pari a 4 o 5.</span><span class="sxs-lookup"><span data-stu-id="588e3-132">This value must be between 1 and 8, inclusively, starting from `DML_FEATURE_LEVEL_3_0`; earlier feature levels require a value of either 4 or 5.</span></span>


`InputWindowOffsets`

<span data-ttu-id="588e3-133">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="588e3-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="588e3-134">Matrice contenente l'inizio (in elementi) della finestra di input in ogni dimensione.</span><span class="sxs-lookup"><span data-stu-id="588e3-134">An array containing the beginning (in elements) of the input window in each dimension.</span></span> <span data-ttu-id="588e3-135">I valori nella matrice devono soddisfare il vincolo `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span><span class="sxs-lookup"><span data-stu-id="588e3-135">Values in the array must satisfy the constraint `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span></span>


`InputWindowSizes`

<span data-ttu-id="588e3-136">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="588e3-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="588e3-137">Matrice contenente l'extent (in elementi) della finestra di input in ogni dimensione.</span><span class="sxs-lookup"><span data-stu-id="588e3-137">An array containing the extent (in elements) of the input window in each dimension.</span></span> <span data-ttu-id="588e3-138">I valori nella matrice devono soddisfare il vincolo `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span><span class="sxs-lookup"><span data-stu-id="588e3-138">Values in the array must satisfy the constraint `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span></span>


`InputWindowStrides`

<span data-ttu-id="588e3-139">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="588e3-139">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="588e3-140">Matrice contenente lo stride della sezione lungo ogni dimensione del tensore di input, in elementi.</span><span class="sxs-lookup"><span data-stu-id="588e3-140">An array containing the slice's stride along each dimension of the input tensor, in elements.</span></span> <span data-ttu-id="588e3-141">La grandezza dello stride indica il numero di elementi da avanzare durante la copia all'interno della finestra di input.</span><span class="sxs-lookup"><span data-stu-id="588e3-141">The magnitude of the stride indicates how many elements to advance when copying within the input window.</span></span> <span data-ttu-id="588e3-142">Il segno dello stride determina se gli elementi vengono copiati a partire dall'inizio della finestra (stride positivo) o dalla fine della finestra (stride negativo).</span><span class="sxs-lookup"><span data-stu-id="588e3-142">The sign of the stride determines if elements are copied starting at the beginning of the window (positive stride) or end of the window (negative stride).</span></span> <span data-ttu-id="588e3-143">Gli stride non possono essere 0.</span><span class="sxs-lookup"><span data-stu-id="588e3-143">Strides may not be 0.</span></span>

## <a name="examples"></a><span data-ttu-id="588e3-144">Esempio</span><span class="sxs-lookup"><span data-stu-id="588e3-144">Examples</span></span>

<span data-ttu-id="588e3-145">Gli esempi seguenti usano lo stesso tensore di input.</span><span class="sxs-lookup"><span data-stu-id="588e3-145">The following examples use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a><span data-ttu-id="588e3-146">Esempio 1.</span><span class="sxs-lookup"><span data-stu-id="588e3-146">Example 1.</span></span> <span data-ttu-id="588e3-147">Sezione strided con passi positivi</span><span class="sxs-lookup"><span data-stu-id="588e3-147">Strided slice with positive strides</span></span>

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

<span data-ttu-id="588e3-148">Gli elementi copiati vengono calcolati nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="588e3-148">The copied elements are calculated as follows.</span></span> 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a><span data-ttu-id="588e3-149">Esempio 2.</span><span class="sxs-lookup"><span data-stu-id="588e3-149">Example 2.</span></span> <span data-ttu-id="588e3-150">Sezione strided con passi negativi</span><span class="sxs-lookup"><span data-stu-id="588e3-150">Strided slice with negative strides</span></span>

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

<span data-ttu-id="588e3-151">Tenere conto che le dimensioni con gli stride della finestra negativi iniziano a copiare alla fine della finestra di input per tale dimensione; Questa operazione viene eseguita aggiungendo `InputWindowSize[i] - 1` all'offset della finestra.</span><span class="sxs-lookup"><span data-stu-id="588e3-151">Recall that dimensions with negative window strides start copying at the end of the input window for that dimension; this is done by adding `InputWindowSize[i] - 1` to the window offset.</span></span> <span data-ttu-id="588e3-152">Le dimensioni con uno stride positivo iniziano semplicemente da `InputWindowOffset[i]` .</span><span class="sxs-lookup"><span data-stu-id="588e3-152">Dimensions with a positive stride simply start at `InputWindowOffset[i]`.</span></span>
- <span data-ttu-id="588e3-153">L'asse 0 `+1` (stride della finestra) inizia la copia in corrispondenza di `InputWindowOffsets[0] = 0` .</span><span class="sxs-lookup"><span data-stu-id="588e3-153">Axis 0 (`+1` window stride) starts copying at `InputWindowOffsets[0] = 0`.</span></span> 
- <span data-ttu-id="588e3-154">L'asse 1 `+1` (stride della finestra) inizia la copia in corrispondenza di `InputWindowOffsets[1] = 0` .</span><span class="sxs-lookup"><span data-stu-id="588e3-154">Axis 1 (`+1` window stride) starts copying at `InputWindowOffsets[1] = 0`.</span></span> 
- <span data-ttu-id="588e3-155">L'asse 2 `-2` (stride della finestra) inizia la copia in corrispondenza di `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` .</span><span class="sxs-lookup"><span data-stu-id="588e3-155">Axis 2 (`-2` window stride) starts copying at `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3`.</span></span> 
- <span data-ttu-id="588e3-156">L'asse 3 `+2` (stride della finestra) inizia la copia in corrispondenza di `InputWindowOffsets[3] = 1` .</span><span class="sxs-lookup"><span data-stu-id="588e3-156">Axis 3 (`+2` window stride) starts copying at `InputWindowOffsets[3] = 1`.</span></span> 

<span data-ttu-id="588e3-157">Gli elementi copiati vengono calcolati nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="588e3-157">The copied elements are calculated as follows.</span></span> 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a><span data-ttu-id="588e3-158">Commenti</span><span class="sxs-lookup"><span data-stu-id="588e3-158">Remarks</span></span>
<span data-ttu-id="588e3-159">Questo operatore è simile [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), ma differisce in due modi importanti.</span><span class="sxs-lookup"><span data-stu-id="588e3-159">This operator is similar to [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), but it differs in two important ways.</span></span>

- <span data-ttu-id="588e3-160">Gli stride delle sezioni possono essere negativi, che consentono di invertire i valori lungo le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="588e3-160">Slice strides may be negative, which allows reversing values along dimensions.</span></span>
- <span data-ttu-id="588e3-161">Le dimensioni della finestra di input non corrispondono necessariamente alle dimensioni dei tensore di output.</span><span class="sxs-lookup"><span data-stu-id="588e3-161">The input window sizes are not necessarily the same as the output tensor sizes.</span></span>

## <a name="availability"></a><span data-ttu-id="588e3-162">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="588e3-162">Availability</span></span>
<span data-ttu-id="588e3-163">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="588e3-163">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="588e3-164">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="588e3-164">Tensor constraints</span></span>
<span data-ttu-id="588e3-165">*InputTensor* e *OutputTensor* devono avere gli stessi *DataType* *e DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="588e3-165">*InputTensor* and *OutputTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="588e3-166">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="588e3-166">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="588e3-167">DML_FEATURE_LEVEL_3_0 e successive</span><span class="sxs-lookup"><span data-stu-id="588e3-167">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="588e3-168">Tensore</span><span class="sxs-lookup"><span data-stu-id="588e3-168">Tensor</span></span> | <span data-ttu-id="588e3-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="588e3-169">Kind</span></span> | <span data-ttu-id="588e3-170">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="588e3-170">Supported dimension counts</span></span> | <span data-ttu-id="588e3-171">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="588e3-171">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="588e3-172">InputTensor</span><span class="sxs-lookup"><span data-stu-id="588e3-172">InputTensor</span></span> | <span data-ttu-id="588e3-173">Input</span><span class="sxs-lookup"><span data-stu-id="588e3-173">Input</span></span> | <span data-ttu-id="588e3-174">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="588e3-174">1 to 8</span></span> | <span data-ttu-id="588e3-175">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="588e3-175">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="588e3-176">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="588e3-176">OutputTensor</span></span> | <span data-ttu-id="588e3-177">Output</span><span class="sxs-lookup"><span data-stu-id="588e3-177">Output</span></span> | <span data-ttu-id="588e3-178">Da 1 a 8</span><span class="sxs-lookup"><span data-stu-id="588e3-178">1 to 8</span></span> | <span data-ttu-id="588e3-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="588e3-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="588e3-180">DML_FEATURE_LEVEL_2_1 e successive</span><span class="sxs-lookup"><span data-stu-id="588e3-180">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="588e3-181">Tensore</span><span class="sxs-lookup"><span data-stu-id="588e3-181">Tensor</span></span> | <span data-ttu-id="588e3-182">Tipo</span><span class="sxs-lookup"><span data-stu-id="588e3-182">Kind</span></span> | <span data-ttu-id="588e3-183">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="588e3-183">Supported dimension counts</span></span> | <span data-ttu-id="588e3-184">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="588e3-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="588e3-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="588e3-185">InputTensor</span></span> | <span data-ttu-id="588e3-186">Input</span><span class="sxs-lookup"><span data-stu-id="588e3-186">Input</span></span> | <span data-ttu-id="588e3-187">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="588e3-187">4 to 5</span></span> | <span data-ttu-id="588e3-188">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="588e3-188">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="588e3-189">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="588e3-189">OutputTensor</span></span> | <span data-ttu-id="588e3-190">Output</span><span class="sxs-lookup"><span data-stu-id="588e3-190">Output</span></span> | <span data-ttu-id="588e3-191">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="588e3-191">4 to 5</span></span> | <span data-ttu-id="588e3-192">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="588e3-192">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="588e3-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="588e3-193">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="588e3-194">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="588e3-194">**Header**</span></span> | <span data-ttu-id="588e3-195">directml.h</span><span class="sxs-lookup"><span data-stu-id="588e3-195">directml.h</span></span> |