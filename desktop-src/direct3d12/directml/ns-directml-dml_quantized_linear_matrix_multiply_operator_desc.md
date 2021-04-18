---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Esegue una funzione di moltiplicazione di matrici per i dati quantizzati. Questo operatore è matematicamente equivalente a dequantizzare gli input, quindi a eseguire la moltiplicazione della matrice e quindi a quantizzare l'output.
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
ms.openlocfilehash: d0b20a37bca6ddf6083b116b53290a6b6b2084f4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320403"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a><span data-ttu-id="41098-104">Struttura DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="41098-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="41098-105">Esegue una funzione di moltiplicazione di matrici per i dati quantizzati.</span><span class="sxs-lookup"><span data-stu-id="41098-105">Performs a matrix multiplication function on quantized data.</span></span> <span data-ttu-id="41098-106">Questo operatore è matematicamente equivalente a dequantizzare gli input, quindi a eseguire la moltiplicazione della matrice e quindi a quantizzare l'output.</span><span class="sxs-lookup"><span data-stu-id="41098-106">This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.</span></span>

<span data-ttu-id="41098-107">Questo operatore richiede che i tensori di input della matrice moltiplichino il formato 4D, formattato come `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="41098-107">This operator requires the matrix multiply input tensors to be 4D which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="41098-108">L'operatore Matrix Multiply eseguirà il BatchCount \* ChannelCount numero di moltiplicazioni di matrici indipendenti.</span><span class="sxs-lookup"><span data-stu-id="41098-108">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span> 

<span data-ttu-id="41098-109">Se, ad esempio, *ATensor* dispone di *dimensioni* pari a `{ BatchCount, ChannelCount, M, K }` e  *BTensor* ha dimensioni `{ BatchCount, ChannelCount, K, N }` e *OutputTensor* ha *dimensioni* pari a `{ BatchCount, ChannelCount, M, N }` , l'operatore di moltiplicazione della matrice eseguirà BatchCount \* ChannelCount le moltiplicazioni di matrici indipendenti di dimensioni {m, K} x {K, n} = {m, n}.</span><span class="sxs-lookup"><span data-stu-id="41098-109">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span> 

### <a name="dequantize-function"></a><span data-ttu-id="41098-110">Funzione dequantizzate</span><span class="sxs-lookup"><span data-stu-id="41098-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="41098-111">Funzione quantizzate</span><span class="sxs-lookup"><span data-stu-id="41098-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="41098-112">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="41098-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="41098-113">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="41098-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="41098-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41098-114">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="41098-115">Members</span><span class="sxs-lookup"><span data-stu-id="41098-115">Members</span></span>

`ATensor`

<span data-ttu-id="41098-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="41098-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="41098-117">Un tensore contenente i dati di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="41098-117">A tensor containing the A data.</span></span> <span data-ttu-id="41098-118">Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="41098-118">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AScaleTensor`

<span data-ttu-id="41098-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="41098-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="41098-120">Un tensore contenente i dati della scala ATensor.</span><span class="sxs-lookup"><span data-stu-id="41098-120">A tensor containing the ATensor scale data.</span></span> <span data-ttu-id="41098-121">Le dimensioni previste di `AScaleTensor` sono `{ 1, 1, 1, 1 }` se è necessaria la quantizzazione del tensore o `{ 1, 1, M, 1 }` se è richiesta la quantizzazione per riga.</span><span class="sxs-lookup"><span data-stu-id="41098-121">The expected dimensions of the `AScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="41098-122">Questi valori di scala vengono utilizzati per la dequantizzazione dei valori A.</span><span class="sxs-lookup"><span data-stu-id="41098-122">These scale values are used for dequantizing the A values.</span></span>


`AZeroPointTensor`

<span data-ttu-id="41098-123">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="41098-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="41098-124">Un tensore facoltativo contenente i dati del punto zero *ATensor* .</span><span class="sxs-lookup"><span data-stu-id="41098-124">An optional tensor containing the *ATensor* zero point data.</span></span> <span data-ttu-id="41098-125">Le dimensioni previste di AZeroPointTensor sono `{ 1, 1, 1, 1 }` se è richiesta la quantizzazione del tensore o `{ 1, 1, M, 1 }` se è necessaria una quantizzazione per riga.</span><span class="sxs-lookup"><span data-stu-id="41098-125">The expected dimensions of the AZeroPointTensor are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="41098-126">Questi valori a virgola zero vengono utilizzati per la dequantizzazione dei valori ATensor.</span><span class="sxs-lookup"><span data-stu-id="41098-126">These zero point values are used for dequantizing the ATensor values.</span></span>


`BTensor`

<span data-ttu-id="41098-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="41098-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="41098-128">Un tensore contenente i dati B.</span><span class="sxs-lookup"><span data-stu-id="41098-128">A tensor containing the B data.</span></span> <span data-ttu-id="41098-129">Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="41098-129">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BScaleTensor`

<span data-ttu-id="41098-130">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="41098-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="41098-131">Un tensore contenente i dati della scala *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="41098-131">A tensor containing the *BTensor* scale data.</span></span> <span data-ttu-id="41098-132">Le dimensioni previste di `BScaleTensor` sono `{ 1, 1, 1, 1 }` se è necessaria la quantizzazione del tensore o `{ 1, 1, 1, N }` se è richiesta la quantizzazione per colonna.</span><span class="sxs-lookup"><span data-stu-id="41098-132">The expected dimensions of the `BScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="41098-133">Questi valori di scala vengono utilizzati per la dequantizzazione dei valori *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="41098-133">These scale values are used for dequantizing the *BTensor* values.</span></span>


`BZeroPointTensor`

<span data-ttu-id="41098-134">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="41098-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="41098-135">Un tensore facoltativo contenente i dati del punto zero *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="41098-135">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="41098-136">Le dimensioni previste di `BZeroPointTensor` sono `{ 1, 1, 1, 1 }` se è necessaria la quantizzazione del tensore o `{ 1, 1, 1, N }` se è richiesta la quantizzazione per colonna.</span><span class="sxs-lookup"><span data-stu-id="41098-136">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="41098-137">Questi valori a virgola zero vengono utilizzati per la dequantizzazione dei valori *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="41098-137">These zero point values are used for dequantizing the *BTensor* values.</span></span>


`OutputScaleTensor`

<span data-ttu-id="41098-138">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="41098-138">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="41098-139">Un tensore contenente i dati sulla scala del filtro.</span><span class="sxs-lookup"><span data-stu-id="41098-139">A tensor containing the filter scale data.</span></span> <span data-ttu-id="41098-140">Le dimensioni previste di `OutputScaleTensor` sono `{ 1, 1, 1, 1 }` se è necessaria la quantizzazione del tensore o `{ 1, 1, M, 1 }` se è richiesta la quantizzazione per riga.</span><span class="sxs-lookup"><span data-stu-id="41098-140">The expected dimensions of the `OutputScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="41098-141">Questo valore di scala viene utilizzato per dequantizzare i valori di filtro.</span><span class="sxs-lookup"><span data-stu-id="41098-141">This scale value is used for dequantizing the filter values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="41098-142">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="41098-142">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="41098-143">Un tensore facoltativo contenente i dati del punto zero del filtro.</span><span class="sxs-lookup"><span data-stu-id="41098-143">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="41098-144">Le dimensioni previste di `OutputZeroPointTensor` sono `{ 1, 1, 1, 1 }` se la quantizzazione del tensore è obbligatoria o `{ 1, 1, M, 1 }` se è necessaria la quantizzazione per riga.</span><span class="sxs-lookup"><span data-stu-id="41098-144">The expected dimensions of the `OutputZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="41098-145">Questo valore del punto zero viene usato per la dequantizzazione dei valori di filtro.</span><span class="sxs-lookup"><span data-stu-id="41098-145">This zero point value is used for dequantizing the filter values.</span></span>


`OutputTensor`

<span data-ttu-id="41098-146">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="41098-146">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="41098-147">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="41098-147">A tensor to write the results to.</span></span> <span data-ttu-id="41098-148">Le dimensioni di questo tensore sono `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="41098-148">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="41098-149">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="41098-149">Availability</span></span>
<span data-ttu-id="41098-150">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="41098-150">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="41098-151">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="41098-151">Tensor constraints</span></span>
* <span data-ttu-id="41098-152">*ATensor* e `AZeroPointTensor` devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="41098-152">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="41098-153">*BTensor* e `BZeroPointTensor` devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="41098-153">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="41098-154">*OutputTensor* e `OutputZeroPointTensor` devono avere lo stesso *tipo* di dati.</span><span class="sxs-lookup"><span data-stu-id="41098-154">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="41098-155">Supporto tensore</span><span class="sxs-lookup"><span data-stu-id="41098-155">Tensor support</span></span>
| <span data-ttu-id="41098-156">Tensore</span><span class="sxs-lookup"><span data-stu-id="41098-156">Tensor</span></span> | <span data-ttu-id="41098-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="41098-157">Kind</span></span> | <span data-ttu-id="41098-158">Conteggi dimensione supportati</span><span class="sxs-lookup"><span data-stu-id="41098-158">Supported dimension counts</span></span> | <span data-ttu-id="41098-159">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="41098-159">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="41098-160">ATensor</span><span class="sxs-lookup"><span data-stu-id="41098-160">ATensor</span></span> | <span data-ttu-id="41098-161">Input</span><span class="sxs-lookup"><span data-stu-id="41098-161">Input</span></span> | <span data-ttu-id="41098-162">4</span><span class="sxs-lookup"><span data-stu-id="41098-162">4</span></span> | <span data-ttu-id="41098-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="41098-163">INT8, UINT8</span></span> |
| <span data-ttu-id="41098-164">AScaleTensor</span><span class="sxs-lookup"><span data-stu-id="41098-164">AScaleTensor</span></span> | <span data-ttu-id="41098-165">Input</span><span class="sxs-lookup"><span data-stu-id="41098-165">Input</span></span> | <span data-ttu-id="41098-166">4</span><span class="sxs-lookup"><span data-stu-id="41098-166">4</span></span> | <span data-ttu-id="41098-167">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="41098-167">FLOAT32</span></span> |
| <span data-ttu-id="41098-168">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="41098-168">AZeroPointTensor</span></span> | <span data-ttu-id="41098-169">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="41098-169">Optional input</span></span> | <span data-ttu-id="41098-170">4</span><span class="sxs-lookup"><span data-stu-id="41098-170">4</span></span> | <span data-ttu-id="41098-171">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="41098-171">INT8, UINT8</span></span> |
| <span data-ttu-id="41098-172">BTensor</span><span class="sxs-lookup"><span data-stu-id="41098-172">BTensor</span></span> | <span data-ttu-id="41098-173">Input</span><span class="sxs-lookup"><span data-stu-id="41098-173">Input</span></span> | <span data-ttu-id="41098-174">4</span><span class="sxs-lookup"><span data-stu-id="41098-174">4</span></span> | <span data-ttu-id="41098-175">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="41098-175">INT8, UINT8</span></span> |
| <span data-ttu-id="41098-176">BScaleTensor</span><span class="sxs-lookup"><span data-stu-id="41098-176">BScaleTensor</span></span> | <span data-ttu-id="41098-177">Input</span><span class="sxs-lookup"><span data-stu-id="41098-177">Input</span></span> | <span data-ttu-id="41098-178">4</span><span class="sxs-lookup"><span data-stu-id="41098-178">4</span></span> | <span data-ttu-id="41098-179">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="41098-179">FLOAT32</span></span> |
| <span data-ttu-id="41098-180">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="41098-180">BZeroPointTensor</span></span> | <span data-ttu-id="41098-181">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="41098-181">Optional input</span></span> | <span data-ttu-id="41098-182">4</span><span class="sxs-lookup"><span data-stu-id="41098-182">4</span></span> | <span data-ttu-id="41098-183">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="41098-183">INT8, UINT8</span></span> |
| <span data-ttu-id="41098-184">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="41098-184">OutputScaleTensor</span></span> | <span data-ttu-id="41098-185">Input</span><span class="sxs-lookup"><span data-stu-id="41098-185">Input</span></span> | <span data-ttu-id="41098-186">4</span><span class="sxs-lookup"><span data-stu-id="41098-186">4</span></span> | <span data-ttu-id="41098-187">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="41098-187">FLOAT32</span></span> |
| <span data-ttu-id="41098-188">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="41098-188">OutputZeroPointTensor</span></span> | <span data-ttu-id="41098-189">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="41098-189">Optional input</span></span> | <span data-ttu-id="41098-190">4</span><span class="sxs-lookup"><span data-stu-id="41098-190">4</span></span> | <span data-ttu-id="41098-191">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="41098-191">INT8, UINT8</span></span> |
| <span data-ttu-id="41098-192">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="41098-192">OutputTensor</span></span> | <span data-ttu-id="41098-193">Output</span><span class="sxs-lookup"><span data-stu-id="41098-193">Output</span></span> | <span data-ttu-id="41098-194">4</span><span class="sxs-lookup"><span data-stu-id="41098-194">4</span></span> | <span data-ttu-id="41098-195">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="41098-195">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="41098-196">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41098-196">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="41098-197">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="41098-197">**Header**</span></span> | <span data-ttu-id="41098-198">directml. h</span><span class="sxs-lookup"><span data-stu-id="41098-198">directml.h</span></span> |