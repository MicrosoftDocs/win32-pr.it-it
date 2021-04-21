---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Calcola il valore massimo tra gli elementi all'interno della finestra temporale scorrevole sul tensore di input e, facoltativamente, restituisce gli indici dei valori massimi selezionati.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
api_name:
- DML_MAX_POOLING2_OPERATOR_DESC
f1_keywords:
- DML_MAX_POOLING2_OPERATOR_DESC
- directml/DML_MAX_POOLING2_OPERATOR_DESC
ms.openlocfilehash: 06e4d7eb01abab9c412238e353a73607df02b219
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803666"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a><span data-ttu-id="8a331-103">DML_MAX_POOLING2_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="8a331-103">DML_MAX_POOLING2_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="8a331-104">Calcola il valore massimo tra gli elementi all'interno della finestra temporale scorrevole sul tensore di input e, facoltativamente, restituisce gli indici dei valori massimi selezionati.</span><span class="sxs-lookup"><span data-stu-id="8a331-104">Computes the maximum value across the elements within the sliding window over the input tensor, and optionally returns the indices of the maximum values selected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a331-105">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="8a331-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="8a331-106">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="8a331-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a331-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a331-107">Syntax</span></span>
```cpp
struct DML_MAX_POOLING2_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  const DML_TENSOR_DESC *OutputIndicesTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *WindowSize;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  const UINT            *Dilations;
};
```



## <a name="members"></a><span data-ttu-id="8a331-108">Members</span><span class="sxs-lookup"><span data-stu-id="8a331-108">Members</span></span>

`InputTensor`

<span data-ttu-id="8a331-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8a331-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8a331-110">Tensore di input *di Sizes* `{ BatchCount, ChannelCount, Height, Width }` se *InputTensor.DimensionCount* è 4 e `{ BatchCount, ChannelCount, Depth, Height, Weight } ` se *InputTensor.DimensionCount* è 5.</span><span class="sxs-lookup"><span data-stu-id="8a331-110">An input tensor of *Sizes* `{ BatchCount, ChannelCount, Height, Width }` if *InputTensor.DimensionCount* is 4, and `{ BatchCount, ChannelCount, Depth, Height, Weight } `if *InputTensor.DimensionCount* is 5.</span></span>


`OutputTensor`

<span data-ttu-id="8a331-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8a331-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8a331-112">Tensore di output in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="8a331-112">An output tensor to write the results to.</span></span> <span data-ttu-id="8a331-113">Le dimensioni del tensore di output possono essere calcolate come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="8a331-113">The sizes of the output tensor can be computed as follows.</span></span>

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

<span data-ttu-id="8a331-114">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8a331-114">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8a331-115">Tensore di output facoltativo di indici per il tensore di input *InputTensor* dei valori massimi prodotti e archiviati in *OutputTensor.*</span><span class="sxs-lookup"><span data-stu-id="8a331-115">An optional output tensor of indices to the input tensor *InputTensor* of the maximum values produced and stored in the *OutputTensor*.</span></span> <span data-ttu-id="8a331-116">Questi valori di indice sono in base zero e trattano il tensore di input come matrice unidimensionale contigua.</span><span class="sxs-lookup"><span data-stu-id="8a331-116">These index values are zero-based and treat the input tensor as a contiguous one-dimensional array.</span></span> <span data-ttu-id="8a331-117">Quando più elementi all'interno della finestra temporale scorrevole hanno lo stesso valore, i valori uguali successivi vengono ignorati e l'indice punta al primo valore rilevato.</span><span class="sxs-lookup"><span data-stu-id="8a331-117">When multiple elements within the sliding window have the same value, the later equal values are ignored and the index points to the first value encountered.</span></span> <span data-ttu-id="8a331-118">Sia *OutputTensor che* *OutputIndicesTensor* hanno le stesse dimensioni del tensore.</span><span class="sxs-lookup"><span data-stu-id="8a331-118">Both the *OutputTensor* and *OutputIndicesTensor* have the same tensor sizes.</span></span>


`DimensionCount`

<span data-ttu-id="8a331-119">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="8a331-119">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="8a331-120">Numero di dimensioni spaziali del tensore di input *InputTensor*, che corrisponde anche al numero di dimensioni della finestra temporale *scorrevole WindowSize.*</span><span class="sxs-lookup"><span data-stu-id="8a331-120">The number of spatial dimensions of the input tensor *InputTensor*, which also corresponds to the number of dimensions of the sliding window *WindowSize*.</span></span> <span data-ttu-id="8a331-121">Questo valore determina anche le dimensioni delle matrici *Strides,* *StartPadding* *ed EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="8a331-121">This value also determines the size of the *Strides*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="8a331-122">Deve essere impostato su 2 quando *InputTensor* è 4D e su 3 quando si tratta di un tensore 5D.</span><span class="sxs-lookup"><span data-stu-id="8a331-122">It should be set to 2 when *InputTensor* is 4D, and 3 when it's a 5D tensor.</span></span>


`Strides`

<span data-ttu-id="8a331-123">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="8a331-123">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="8a331-124">Gli stride per le dimensioni della finestra scorrevole delle dimensioni `{ Height, Width }` quando *DimensionCount* è impostato su 2 o `{ Depth, Height, Width }` su 3.</span><span class="sxs-lookup"><span data-stu-id="8a331-124">The strides for the sliding window dimensions of sizes `{ Height, Width }` when the *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`WindowSize`

<span data-ttu-id="8a331-125">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="8a331-125">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="8a331-126">Dimensioni della finestra scorrevole in `{ Height, Width }` quando *DimensionCount* è impostato su 2 o `{ Depth, Height, Width }` su 3.</span><span class="sxs-lookup"><span data-stu-id="8a331-126">The dimensions of the sliding window in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`StartPadding`

<span data-ttu-id="8a331-127">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="8a331-127">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="8a331-128">Numero di elementi di spaziatura interna da applicare all'inizio di ogni dimensione spaziale del tensore *input InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="8a331-128">The number of padding elements to be applied to the beginning of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="8a331-129">I valori sono in `{ Height, Width }` quando *DimensionCount* è impostato su 2 o `{ Depth, Height, Width }` quando è impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="8a331-129">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`EndPadding`

<span data-ttu-id="8a331-130">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="8a331-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="8a331-131">Numero di elementi di spaziatura interna da applicare alla fine di ogni dimensione spaziale del tensore *input InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="8a331-131">The number of padding elements to be applied to the end of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="8a331-132">I valori sono in `{ Height, Width }` quando *DimensionCount* è impostato su 2 o `{ Depth, Height, Width }` quando è impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="8a331-132">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`Dilations`

<span data-ttu-id="8a331-133">Tipo: \_ Dimensione \_ campo \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="8a331-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="8a331-134">Valori per ogni dimensione spaziale del tensore di input *InputTensor* in base al quale un elemento all'interno della finestra scorrevole viene selezionato per ogni elemento di tale valore.</span><span class="sxs-lookup"><span data-stu-id="8a331-134">The values for each spatial dimension of the input tensor *InputTensor* by which an element within the sliding window is selected for every elements of that value.</span></span> <span data-ttu-id="8a331-135">I valori sono in `{ Height, Width }` quando *DimensionCount* è impostato su 2 o `{ Depth, Height, Width }` quando è impostato su 3.</span><span class="sxs-lookup"><span data-stu-id="8a331-135">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


## <a name="remarks"></a><span data-ttu-id="8a331-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a331-136">Remarks</span></span>
<span data-ttu-id="8a331-137">**DML_MAX_POOLING2_OPERATOR_DESC** sostituisce la versione precedente DML_MAX_POOLING_OPERATOR1_DESC [con](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) una matrice costante aggiuntiva *Dilations*.</span><span class="sxs-lookup"><span data-stu-id="8a331-137">**DML_MAX_POOLING2_OPERATOR_DESC** supersedes the earlier version [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) with an additional constant array *Dilations*.</span></span> <span data-ttu-id="8a331-138">Le due versioni sono equivalenti quando *Dilations* è impostato su per `{ 1,1 }` l'input 4D o `{ 1,1,1 }` per le funzionalità di input 5D.</span><span class="sxs-lookup"><span data-stu-id="8a331-138">The two versions are equivalent when *Dilations* is set to `{ 1,1 }` for 4D input, or `{ 1,1,1 }` for 5D input features.</span></span>

## <a name="availability"></a><span data-ttu-id="8a331-139">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="8a331-139">Availability</span></span>
<span data-ttu-id="8a331-140">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="8a331-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="8a331-141">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="8a331-141">Tensor constraints</span></span>
* <span data-ttu-id="8a331-142">*InputTensor,* *OutputIndicesTensor* e *OutputTensor* devono avere lo stesso *dimensioncount.*</span><span class="sxs-lookup"><span data-stu-id="8a331-142">*InputTensor*, *OutputIndicesTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="8a331-143">*InputTensor* e *OutputTensor* devono avere lo stesso *Tipo di dati*.</span><span class="sxs-lookup"><span data-stu-id="8a331-143">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="8a331-144">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="8a331-144">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="8a331-145">DML_FEATURE_LEVEL_3_0 e successive</span><span class="sxs-lookup"><span data-stu-id="8a331-145">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="8a331-146">Tensore</span><span class="sxs-lookup"><span data-stu-id="8a331-146">Tensor</span></span> | <span data-ttu-id="8a331-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a331-147">Kind</span></span> | <span data-ttu-id="8a331-148">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="8a331-148">Supported dimension counts</span></span> | <span data-ttu-id="8a331-149">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="8a331-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8a331-150">InputTensor</span><span class="sxs-lookup"><span data-stu-id="8a331-150">InputTensor</span></span> | <span data-ttu-id="8a331-151">Input</span><span class="sxs-lookup"><span data-stu-id="8a331-151">Input</span></span> | <span data-ttu-id="8a331-152">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="8a331-152">4 to 5</span></span> | <span data-ttu-id="8a331-153">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="8a331-153">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="8a331-154">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8a331-154">OutputTensor</span></span> | <span data-ttu-id="8a331-155">Output</span><span class="sxs-lookup"><span data-stu-id="8a331-155">Output</span></span> | <span data-ttu-id="8a331-156">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="8a331-156">4 to 5</span></span> | <span data-ttu-id="8a331-157">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="8a331-157">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="8a331-158">OutputIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="8a331-158">OutputIndicesTensor</span></span> | <span data-ttu-id="8a331-159">Output facoltativo</span><span class="sxs-lookup"><span data-stu-id="8a331-159">Optional output</span></span> | <span data-ttu-id="8a331-160">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="8a331-160">4 to 5</span></span> | <span data-ttu-id="8a331-161">UINT32</span><span class="sxs-lookup"><span data-stu-id="8a331-161">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="8a331-162">DML_FEATURE_LEVEL_2_1 e successive</span><span class="sxs-lookup"><span data-stu-id="8a331-162">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="8a331-163">Tensore</span><span class="sxs-lookup"><span data-stu-id="8a331-163">Tensor</span></span> | <span data-ttu-id="8a331-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a331-164">Kind</span></span> | <span data-ttu-id="8a331-165">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="8a331-165">Supported dimension counts</span></span> | <span data-ttu-id="8a331-166">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="8a331-166">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8a331-167">InputTensor</span><span class="sxs-lookup"><span data-stu-id="8a331-167">InputTensor</span></span> | <span data-ttu-id="8a331-168">Input</span><span class="sxs-lookup"><span data-stu-id="8a331-168">Input</span></span> | <span data-ttu-id="8a331-169">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="8a331-169">4 to 5</span></span> | <span data-ttu-id="8a331-170">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="8a331-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="8a331-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8a331-171">OutputTensor</span></span> | <span data-ttu-id="8a331-172">Output</span><span class="sxs-lookup"><span data-stu-id="8a331-172">Output</span></span> | <span data-ttu-id="8a331-173">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="8a331-173">4 to 5</span></span> | <span data-ttu-id="8a331-174">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="8a331-174">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="8a331-175">OutputIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="8a331-175">OutputIndicesTensor</span></span> | <span data-ttu-id="8a331-176">Output facoltativo</span><span class="sxs-lookup"><span data-stu-id="8a331-176">Optional output</span></span> | <span data-ttu-id="8a331-177">Da 4 a 5</span><span class="sxs-lookup"><span data-stu-id="8a331-177">4 to 5</span></span> | <span data-ttu-id="8a331-178">UINT32</span><span class="sxs-lookup"><span data-stu-id="8a331-178">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="8a331-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a331-179">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8a331-180">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="8a331-180">**Minimum supported client**</span></span> | <span data-ttu-id="8a331-181">Windows 10 versione 2004 (10.0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="8a331-181">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="8a331-182">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="8a331-182">**Minimum supported server**</span></span> | <span data-ttu-id="8a331-183">Windows Server versione 2004 (10.0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="8a331-183">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="8a331-184">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="8a331-184">**Header**</span></span> | <span data-ttu-id="8a331-185">directml.h</span><span class="sxs-lookup"><span data-stu-id="8a331-185">directml.h</span></span> |