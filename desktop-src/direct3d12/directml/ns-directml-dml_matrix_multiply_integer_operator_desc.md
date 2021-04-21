---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Esegue una funzione di moltiplicazione matrice sui dati integer.
helpviewer_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_matrix_multiply_integer_operator_desc
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
ms.keywords: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC, DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure, direct3d12.dml_matrix_multiply_integer_operator_desc, directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
ms.custom: 19H1
f1_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f498e84208da451b5d25ffef90219c0037ce86fb
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802836"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="32131-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC struttura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="32131-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="32131-104">Esegue una funzione di moltiplicazione matrice sui dati integer.</span><span class="sxs-lookup"><span data-stu-id="32131-104">Performs a matrix multiplication function on integer data.</span></span>

<span data-ttu-id="32131-105">Questo operatore richiede che i tensori di input di moltiplicazione matrice siano 4D, formattati come `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="32131-105">This operator requires the matrix multiply input tensors to be 4D, which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="32131-106">L'operatore di moltiplicazione matrice eseguirà BatchCount \* ChannelCount numero di moltiplicazioni di matrici indipendenti.</span><span class="sxs-lookup"><span data-stu-id="32131-106">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span>

<span data-ttu-id="32131-107">Ad esempio, se *ATensor* ha Dimensioni di e  BTensor ha Dimensioni pari a e OutputTensor ha Dimensioni pari a , l'operatore di moltiplicazione matrice eseguirà BatchCount \* ChannelCount moltiplicazioni di matrici indipendenti di dimensioni `{ BatchCount, ChannelCount, M, K }`   `{ BatchCount, ChannelCount, K, N }`   `{ BatchCount, ChannelCount, M, N }` {M,K} x {K,N} = {M,N}.</span><span class="sxs-lookup"><span data-stu-id="32131-107">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32131-108">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="32131-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="32131-109">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="32131-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="32131-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32131-110">Syntax</span></span>
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="32131-111">Members</span><span class="sxs-lookup"><span data-stu-id="32131-111">Members</span></span>

`ATensor`

<span data-ttu-id="32131-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="32131-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="32131-113">Tensore contenente i dati A.</span><span class="sxs-lookup"><span data-stu-id="32131-113">A tensor containing the A data.</span></span> <span data-ttu-id="32131-114">Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="32131-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AZeroPointTensor`

<span data-ttu-id="32131-115">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="32131-115">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="32131-116">Tensore facoltativo contenente i dati ATensor zero point.</span><span class="sxs-lookup"><span data-stu-id="32131-116">An optional tensor containing the ATensor zero point data.</span></span> <span data-ttu-id="32131-117">Le dimensioni previste di `AZeroPointTensor` sono se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o se è necessaria `{ 1, 1, M, 1 }` la quantizzazione per riga.</span><span class="sxs-lookup"><span data-stu-id="32131-117">The expected dimensions of the `AZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per-row quantization is required.</span></span> <span data-ttu-id="32131-118">Questi valori di punto zero vengono usati per dequantizzare i *valori di ATensor.*</span><span class="sxs-lookup"><span data-stu-id="32131-118">These zero point values are used for dequantizing the *ATensor* values.</span></span>


`BTensor`

<span data-ttu-id="32131-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="32131-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="32131-120">Tensore contenente i dati B.</span><span class="sxs-lookup"><span data-stu-id="32131-120">A tensor containing the B data.</span></span> <span data-ttu-id="32131-121">Le dimensioni di questo tensore devono essere `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="32131-121">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BZeroPointTensor`

<span data-ttu-id="32131-122">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="32131-122">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="32131-123">Tensore facoltativo contenente i dati del punto zero *BTensor.*</span><span class="sxs-lookup"><span data-stu-id="32131-123">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="32131-124">Le dimensioni previste di sono `BZeroPointTensor` se è necessaria la `{ 1, 1, 1, 1 }` quantizzazione per tensore o `{ 1, 1, 1, N }` se è necessaria la quantizzazione per colonna.</span><span class="sxs-lookup"><span data-stu-id="32131-124">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="32131-125">Questi valori di punto zero vengono usati per dequantizzare i valori BTensor.</span><span class="sxs-lookup"><span data-stu-id="32131-125">These zero point values are used for dequantizing the BTensor values.</span></span>


`OutputTensor`

<span data-ttu-id="32131-126">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="32131-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="32131-127">Tensore in cui scrivere i risultati.</span><span class="sxs-lookup"><span data-stu-id="32131-127">A tensor with which to write the results to.</span></span> <span data-ttu-id="32131-128">Le dimensioni di questo tensore sono `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="32131-128">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="32131-129">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="32131-129">Availability</span></span>
<span data-ttu-id="32131-130">Questo operatore è stato introdotto in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="32131-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="32131-131">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="32131-131">Tensor constraints</span></span>
* <span data-ttu-id="32131-132">*ATensor* e `AZeroPointTensor` devono avere lo stesso tipo di *dati*.</span><span class="sxs-lookup"><span data-stu-id="32131-132">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="32131-133">*BTensor* e `BZeroPointTensor` devono avere lo stesso tipo di *dati*.</span><span class="sxs-lookup"><span data-stu-id="32131-133">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="32131-134">Supporto di Tensor</span><span class="sxs-lookup"><span data-stu-id="32131-134">Tensor support</span></span>
| <span data-ttu-id="32131-135">Tensore</span><span class="sxs-lookup"><span data-stu-id="32131-135">Tensor</span></span> | <span data-ttu-id="32131-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="32131-136">Kind</span></span> | <span data-ttu-id="32131-137">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="32131-137">Dimensions</span></span> | <span data-ttu-id="32131-138">Conteggi delle dimensioni supportati</span><span class="sxs-lookup"><span data-stu-id="32131-138">Supported dimension counts</span></span> | <span data-ttu-id="32131-139">Tipi di dati supportati</span><span class="sxs-lookup"><span data-stu-id="32131-139">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="32131-140">ATensor</span><span class="sxs-lookup"><span data-stu-id="32131-140">ATensor</span></span> | <span data-ttu-id="32131-141">Input</span><span class="sxs-lookup"><span data-stu-id="32131-141">Input</span></span> | <span data-ttu-id="32131-142">{ BatchCount, ChannelCount, M, K }</span><span class="sxs-lookup"><span data-stu-id="32131-142">{ BatchCount, ChannelCount, M, K }</span></span> | <span data-ttu-id="32131-143">4</span><span class="sxs-lookup"><span data-stu-id="32131-143">4</span></span> | <span data-ttu-id="32131-144">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="32131-144">INT8, UINT8</span></span> |
| <span data-ttu-id="32131-145">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="32131-145">AZeroPointTensor</span></span> | <span data-ttu-id="32131-146">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="32131-146">Optional input</span></span> | <span data-ttu-id="32131-147">{ 1, 1, AZeroPointCount, 1 }</span><span class="sxs-lookup"><span data-stu-id="32131-147">{ 1, 1, AZeroPointCount, 1 }</span></span> | <span data-ttu-id="32131-148">4</span><span class="sxs-lookup"><span data-stu-id="32131-148">4</span></span> | <span data-ttu-id="32131-149">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="32131-149">INT8, UINT8</span></span> |
| <span data-ttu-id="32131-150">BTensor</span><span class="sxs-lookup"><span data-stu-id="32131-150">BTensor</span></span> | <span data-ttu-id="32131-151">Input</span><span class="sxs-lookup"><span data-stu-id="32131-151">Input</span></span> | <span data-ttu-id="32131-152">{ BatchCount, ChannelCount, K, N }</span><span class="sxs-lookup"><span data-stu-id="32131-152">{ BatchCount, ChannelCount, K, N }</span></span> | <span data-ttu-id="32131-153">4</span><span class="sxs-lookup"><span data-stu-id="32131-153">4</span></span> | <span data-ttu-id="32131-154">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="32131-154">INT8, UINT8</span></span> |
| <span data-ttu-id="32131-155">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="32131-155">BZeroPointTensor</span></span> | <span data-ttu-id="32131-156">Input facoltativo</span><span class="sxs-lookup"><span data-stu-id="32131-156">Optional input</span></span> | <span data-ttu-id="32131-157">{ 1, 1, 1, BZeroPointCount }</span><span class="sxs-lookup"><span data-stu-id="32131-157">{ 1, 1, 1, BZeroPointCount }</span></span> | <span data-ttu-id="32131-158">4</span><span class="sxs-lookup"><span data-stu-id="32131-158">4</span></span> | <span data-ttu-id="32131-159">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="32131-159">INT8, UINT8</span></span> |
| <span data-ttu-id="32131-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="32131-160">OutputTensor</span></span> | <span data-ttu-id="32131-161">Output</span><span class="sxs-lookup"><span data-stu-id="32131-161">Output</span></span> | <span data-ttu-id="32131-162">{ BatchCount, ChannelCount, M, N }</span><span class="sxs-lookup"><span data-stu-id="32131-162">{ BatchCount, ChannelCount, M, N }</span></span> | <span data-ttu-id="32131-163">4</span><span class="sxs-lookup"><span data-stu-id="32131-163">4</span></span> | <span data-ttu-id="32131-164">INT32</span><span class="sxs-lookup"><span data-stu-id="32131-164">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="32131-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32131-165">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="32131-166">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="32131-166">**Header**</span></span> | <span data-ttu-id="32131-167">directml.h</span><span class="sxs-lookup"><span data-stu-id="32131-167">directml.h</span></span> |