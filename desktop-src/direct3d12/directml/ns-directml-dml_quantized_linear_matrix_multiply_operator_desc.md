---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Esegue una funzione di moltiplicazione di matrici sui dati quantizzati. Questo operatore equivale matematicamente alla dequantizzazione degli input, all'esecuzione della moltiplicazione della matrice e alla quantizzazione dell'output.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_matrix_multiply_operator_desc
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.openlocfilehash: 0daeab63559a2d842582087d8874e802645f7809
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417809"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a><span data-ttu-id="04baa-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="04baa-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="04baa-105">Esegue una funzione di moltiplicazione di matrici sui dati quantizzati.</span><span class="sxs-lookup"><span data-stu-id="04baa-105">Performs a matrix multiplication function on quantized data.</span></span> <span data-ttu-id="04baa-106">Questo operatore equivale matematicamente alla dequantizzazione degli input, all'esecuzione della moltiplicazione della matrice e alla quantizzazione dell'output.</span><span class="sxs-lookup"><span data-stu-id="04baa-106">This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.</span></span>

<span data-ttu-id="04baa-107">Questo operatore richiede che i tensori di input di moltiplicazione matrice siano 4D formattati come `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="04baa-107">This operator requires the matrix multiply input tensors to be 4D which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="04baa-108">L'operatore di moltiplicazione matrice eseguirà BatchCount \* ChannelCount numero di moltiplicazioni di matrici indipendenti.</span><span class="sxs-lookup"><span data-stu-id="04baa-108">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span> 

<span data-ttu-id="04baa-109">Ad esempio, se *ATensor* ha dimensioni pari a e  BTensor ha dimensioni pari a e OutputTensor ha Dimensioni pari a , l'operatore di moltiplicazione matrice eseguirà BatchCount \* ChannelCount moltiplicazioni di matrici indipendenti di dimensioni `{ BatchCount, ChannelCount, M, K }`   `{ BatchCount, ChannelCount, K, N }`   `{ BatchCount, ChannelCount, M, N }` {M,K} x {K,N} = {M,N}.</span><span class="sxs-lookup"><span data-stu-id="04baa-109">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span> 

### <a name="dequantize-function"></a><span data-ttu-id="04baa-110">Funzione Dequantize</span><span class="sxs-lookup"><span data-stu-id="04baa-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="04baa-111">Funzione Quantize</span><span class="sxs-lookup"><span data-stu-id="04baa-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="04baa-112">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="04baa-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="04baa-113">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="04baa-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="04baa-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04baa-114">Syntax</span></span>
```cpp
struct DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AScaleTensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BScaleTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="04baa-115">Members</span><span class="sxs-lookup"><span data-stu-id="04baa-115">Members</span></span>

`ATensor`

<span data-ttu-id="04baa-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="04baa-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="04baa-117">Tensore contenente i dati A.</span><span class="sxs-lookup"><span data-stu-id="04baa-117">A tensor containing the A data.</span></span> <span data-ttu-id="04baa-118">Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="04baa-118">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AScaleTensor`

<span data-ttu-id="04baa-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="04baa-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="04baa-120">Tensore contenente i dati di scala ATensor.</span><span class="sxs-lookup"><span data-stu-id="04baa-120">A tensor containing the ATensor scale data.</span></span> <span data-ttu-id="04baa-121">Le dimensioni previste di sono `AScaleTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o `{ 1, 1, M, 1 }` se è necessaria la quantizzazione per riga.</span><span class="sxs-lookup"><span data-stu-id="04baa-121">The expected dimensions of the `AScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="04baa-122">Questi valori di scala vengono usati per dequantizzare i valori A.</span><span class="sxs-lookup"><span data-stu-id="04baa-122">These scale values are used for dequantizing the A values.</span></span>


`AZeroPointTensor`

<span data-ttu-id="04baa-123">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="04baa-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="04baa-124">Tensore facoltativo contenente i *dati ATensor* zero point.</span><span class="sxs-lookup"><span data-stu-id="04baa-124">An optional tensor containing the *ATensor* zero point data.</span></span> <span data-ttu-id="04baa-125">Le dimensioni previste di AZeroPointTensor sono se è necessaria la quantizzazione per tensore o se `{ 1, 1, 1, 1 }` è necessaria la `{ 1, 1, M, 1 }` quantizzazione per riga.</span><span class="sxs-lookup"><span data-stu-id="04baa-125">The expected dimensions of the AZeroPointTensor are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="04baa-126">Questi valori di punto zero vengono usati per dequantizzare i valori di ATensor.</span><span class="sxs-lookup"><span data-stu-id="04baa-126">These zero point values are used for dequantizing the ATensor values.</span></span>


`BTensor`

<span data-ttu-id="04baa-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="04baa-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="04baa-128">Tensore contenente i dati B.</span><span class="sxs-lookup"><span data-stu-id="04baa-128">A tensor containing the B data.</span></span> <span data-ttu-id="04baa-129">Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="04baa-129">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BScaleTensor`

<span data-ttu-id="04baa-130">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="04baa-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="04baa-131">Tensore contenente i *dati di scalabilità BTensor.*</span><span class="sxs-lookup"><span data-stu-id="04baa-131">A tensor containing the *BTensor* scale data.</span></span> <span data-ttu-id="04baa-132">Le dimensioni previste di sono `BScaleTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o `{ 1, 1, 1, N }` se è necessaria la quantizzazione per colonna.</span><span class="sxs-lookup"><span data-stu-id="04baa-132">The expected dimensions of the `BScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="04baa-133">Questi valori di scala vengono usati per dequantizzare i *valori BTensor.*</span><span class="sxs-lookup"><span data-stu-id="04baa-133">These scale values are used for dequantizing the *BTensor* values.</span></span>


`BZeroPointTensor`

<span data-ttu-id="04baa-134">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="04baa-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="04baa-135">Tensore facoltativo contenente i dati del punto zero *BTensor.*</span><span class="sxs-lookup"><span data-stu-id="04baa-135">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="04baa-136">Le dimensioni previste di sono `BZeroPointTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o `{ 1, 1, 1, N }` se è necessaria la quantizzazione per colonna.</span><span class="sxs-lookup"><span data-stu-id="04baa-136">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="04baa-137">Questi valori di punto zero vengono usati per dequantizzare i *valori BTensor.*</span><span class="sxs-lookup"><span data-stu-id="04baa-137">These zero point values are used for dequantizing the *BTensor* values.</span></span>


`OutputScaleTensor`

<span data-ttu-id="04baa-138">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="04baa-138">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="04baa-139">Tensore contenente i dati della scala del filtro.</span><span class="sxs-lookup"><span data-stu-id="04baa-139">A tensor containing the filter scale data.</span></span> <span data-ttu-id="04baa-140">Le dimensioni previste di sono `OutputScaleTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o `{ 1, 1, M, 1 }` se è necessaria la quantizzazione per riga.</span><span class="sxs-lookup"><span data-stu-id="04baa-140">The expected dimensions of the `OutputScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="04baa-141">Questo valore di scala viene usato per dequantizzare i valori di filtro.</span><span class="sxs-lookup"><span data-stu-id="04baa-141">This scale value is used for dequantizing the filter values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="04baa-142">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="04baa-142">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="04baa-143">Tensore facoltativo contenente i dati del punto zero del filtro.</span><span class="sxs-lookup"><span data-stu-id="04baa-143">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="04baa-144">Le dimensioni previste di sono `OutputZeroPointTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o `{ 1, 1, M, 1 }` se è necessaria la quantizzazione per riga.</span><span class="sxs-lookup"><span data-stu-id="04baa-144">The expected dimensions of the `OutputZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="04baa-145">Questo valore del punto zero viene usato per dequantizzare i valori di filtro.</span><span class="sxs-lookup"><span data-stu-id="04baa-145">This zero point value is used for dequantizing the filter values.</span></span>


`OutputTensor`

<span data-ttu-id="04baa-146">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="04baa-146">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="04baa-147">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="04baa-147">A tensor to write the results to.</span></span> <span data-ttu-id="04baa-148">Le dimensioni di questo tensore sono `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="04baa-148">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="04baa-149">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="04baa-149">Availability</span></span>
<span data-ttu-id="04baa-150">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="04baa-150">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="04baa-151">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="04baa-151">Tensor constraints</span></span>
* <span data-ttu-id="04baa-152">*ATensor* e `AZeroPointTensor` devono avere lo stesso tipo di *dati*.</span><span class="sxs-lookup"><span data-stu-id="04baa-152">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="04baa-153">*BTensor* e `BZeroPointTensor` devono avere lo stesso tipo di *dati*.</span><span class="sxs-lookup"><span data-stu-id="04baa-153">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="04baa-154">*OutputTensor* e `OutputZeroPointTensor` devono avere lo stesso *datatype*.</span><span class="sxs-lookup"><span data-stu-id="04baa-154">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="04baa-155">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="04baa-155">Tensor support</span></span>
| <span data-ttu-id="04baa-156">Tensore</span><span class="sxs-lookup"><span data-stu-id="04baa-156">Tensor</span></span> | <span data-ttu-id="04baa-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="04baa-157">Kind</span></span> | <span data-ttu-id="04baa-158">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="04baa-158">Supported dimension counts</span></span> | <span data-ttu-id="04baa-159">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="04baa-159">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="04baa-160">ATensor</span><span class="sxs-lookup"><span data-stu-id="04baa-160">ATensor</span></span> | <span data-ttu-id="04baa-161">Input</span><span class="sxs-lookup"><span data-stu-id="04baa-161">Input</span></span> | <span data-ttu-id="04baa-162">4</span><span class="sxs-lookup"><span data-stu-id="04baa-162">4</span></span> | <span data-ttu-id="04baa-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="04baa-163">INT8, UINT8</span></span> |
| <span data-ttu-id="04baa-164">AScaleTensor</span><span class="sxs-lookup"><span data-stu-id="04baa-164">AScaleTensor</span></span> | <span data-ttu-id="04baa-165">Input</span><span class="sxs-lookup"><span data-stu-id="04baa-165">Input</span></span> | <span data-ttu-id="04baa-166">4</span><span class="sxs-lookup"><span data-stu-id="04baa-166">4</span></span> | <span data-ttu-id="04baa-167">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="04baa-167">FLOAT32</span></span> |
| <span data-ttu-id="04baa-168">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="04baa-168">AZeroPointTensor</span></span> | <span data-ttu-id="04baa-169">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="04baa-169">Optional input</span></span> | <span data-ttu-id="04baa-170">4</span><span class="sxs-lookup"><span data-stu-id="04baa-170">4</span></span> | <span data-ttu-id="04baa-171">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="04baa-171">INT8, UINT8</span></span> |
| <span data-ttu-id="04baa-172">BTensor</span><span class="sxs-lookup"><span data-stu-id="04baa-172">BTensor</span></span> | <span data-ttu-id="04baa-173">Input</span><span class="sxs-lookup"><span data-stu-id="04baa-173">Input</span></span> | <span data-ttu-id="04baa-174">4</span><span class="sxs-lookup"><span data-stu-id="04baa-174">4</span></span> | <span data-ttu-id="04baa-175">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="04baa-175">INT8, UINT8</span></span> |
| <span data-ttu-id="04baa-176">BScaleTensor</span><span class="sxs-lookup"><span data-stu-id="04baa-176">BScaleTensor</span></span> | <span data-ttu-id="04baa-177">Input</span><span class="sxs-lookup"><span data-stu-id="04baa-177">Input</span></span> | <span data-ttu-id="04baa-178">4</span><span class="sxs-lookup"><span data-stu-id="04baa-178">4</span></span> | <span data-ttu-id="04baa-179">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="04baa-179">FLOAT32</span></span> |
| <span data-ttu-id="04baa-180">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="04baa-180">BZeroPointTensor</span></span> | <span data-ttu-id="04baa-181">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="04baa-181">Optional input</span></span> | <span data-ttu-id="04baa-182">4</span><span class="sxs-lookup"><span data-stu-id="04baa-182">4</span></span> | <span data-ttu-id="04baa-183">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="04baa-183">INT8, UINT8</span></span> |
| <span data-ttu-id="04baa-184">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="04baa-184">OutputScaleTensor</span></span> | <span data-ttu-id="04baa-185">Input</span><span class="sxs-lookup"><span data-stu-id="04baa-185">Input</span></span> | <span data-ttu-id="04baa-186">4</span><span class="sxs-lookup"><span data-stu-id="04baa-186">4</span></span> | <span data-ttu-id="04baa-187">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="04baa-187">FLOAT32</span></span> |
| <span data-ttu-id="04baa-188">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="04baa-188">OutputZeroPointTensor</span></span> | <span data-ttu-id="04baa-189">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="04baa-189">Optional input</span></span> | <span data-ttu-id="04baa-190">4</span><span class="sxs-lookup"><span data-stu-id="04baa-190">4</span></span> | <span data-ttu-id="04baa-191">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="04baa-191">INT8, UINT8</span></span> |
| <span data-ttu-id="04baa-192">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="04baa-192">OutputTensor</span></span> | <span data-ttu-id="04baa-193">Output</span><span class="sxs-lookup"><span data-stu-id="04baa-193">Output</span></span> | <span data-ttu-id="04baa-194">4</span><span class="sxs-lookup"><span data-stu-id="04baa-194">4</span></span> | <span data-ttu-id="04baa-195">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="04baa-195">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="04baa-196">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04baa-196">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="04baa-197">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="04baa-197">**Header**</span></span> | <span data-ttu-id="04baa-198">directml.h</span><span class="sxs-lookup"><span data-stu-id="04baa-198">directml.h</span></span> |