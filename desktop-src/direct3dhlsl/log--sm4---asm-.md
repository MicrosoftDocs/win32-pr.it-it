---
title: log (SM4-ASM)
description: Logaritmo in base 2 per componenti.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf99949e278ca302543437da346188b690789604
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046094"
---
# <a name="log-sm4---asm"></a><span data-ttu-id="b231a-103">log (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b231a-103">log (sm4 - asm)</span></span>

<span data-ttu-id="b231a-104">Logaritmo in base 2 per componenti.</span><span class="sxs-lookup"><span data-stu-id="b231a-104">Component-wise log base 2.</span></span>



| <span data-ttu-id="b231a-105">log \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle</span><span class="sxs-lookup"><span data-stu-id="b231a-105">log\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="b231a-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="b231a-106">Item</span></span>                                                            | <span data-ttu-id="b231a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b231a-107">Description</span></span>                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b231a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b231a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b231a-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b231a-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="b231a-110">dest = log2 (src0)</span><span class="sxs-lookup"><span data-stu-id="b231a-110">dest = log2(src0)</span></span><br/> |
| <span data-ttu-id="b231a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b231a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b231a-112">\[nel \] valore per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b231a-112">\[in\] The value for the operation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="b231a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b231a-113">Remarks</span></span>

### <a name="restrictions"></a><span data-ttu-id="b231a-114">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="b231a-114">Restrictions</span></span>

-   <span data-ttu-id="b231a-115">Segue la teoria del limite.</span><span class="sxs-lookup"><span data-stu-id="b231a-115">Follows limit theory.</span></span>
-   <span data-ttu-id="b231a-116">Tolleranza di errore: se *src0* è \[ 0,5.. 2 \] , l'errore Absolue non deve essere superiore a 2-21.</span><span class="sxs-lookup"><span data-stu-id="b231a-116">Error tolerance: If *src0* is \[0.5..2\], absolue error must be no more than 2-21.</span></span> <span data-ttu-id="b231a-117">Se *src0* è (0.. 0,5) o (2.. + inf \] , l'errore relativo non deve essere superiore a 2-21.</span><span class="sxs-lookup"><span data-stu-id="b231a-117">If *src0* is (0..0.5) or (2..+INF\], relative error must be no more than 2-21.</span></span>

<span data-ttu-id="b231a-118">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="b231a-118">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="b231a-119">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="b231a-119">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="b231a-120">**src**</span><span class="sxs-lookup"><span data-stu-id="b231a-120">**src**</span></span>  | <span data-ttu-id="b231a-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="b231a-121">**-inf**</span></span> | <span data-ttu-id="b231a-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="b231a-122">**-F**</span></span> | <span data-ttu-id="b231a-123">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="b231a-123">**-denorm**</span></span> | <span data-ttu-id="b231a-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="b231a-124">**-0**</span></span> | <span data-ttu-id="b231a-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="b231a-125">**+0**</span></span> | <span data-ttu-id="b231a-126">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="b231a-126">**+denorm**</span></span> | <span data-ttu-id="b231a-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="b231a-127">**+F**</span></span> | <span data-ttu-id="b231a-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="b231a-128">**+inf**</span></span> | <span data-ttu-id="b231a-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="b231a-129">**NaN**</span></span> |
| <span data-ttu-id="b231a-130">**dest**</span><span class="sxs-lookup"><span data-stu-id="b231a-130">**dest**</span></span> | <span data-ttu-id="b231a-131">NaN</span><span class="sxs-lookup"><span data-stu-id="b231a-131">NaN</span></span>      | <span data-ttu-id="b231a-132">NaN</span><span class="sxs-lookup"><span data-stu-id="b231a-132">NaN</span></span>    | <span data-ttu-id="b231a-133">-inf</span><span class="sxs-lookup"><span data-stu-id="b231a-133">-inf</span></span>        | <span data-ttu-id="b231a-134">-inf</span><span class="sxs-lookup"><span data-stu-id="b231a-134">-inf</span></span>   | <span data-ttu-id="b231a-135">-inf</span><span class="sxs-lookup"><span data-stu-id="b231a-135">-inf</span></span>   | <span data-ttu-id="b231a-136">-inf</span><span class="sxs-lookup"><span data-stu-id="b231a-136">-inf</span></span>        | <span data-ttu-id="b231a-137">F</span><span class="sxs-lookup"><span data-stu-id="b231a-137">F</span></span>      | <span data-ttu-id="b231a-138">+inf</span><span class="sxs-lookup"><span data-stu-id="b231a-138">+inf</span></span>     | <span data-ttu-id="b231a-139">NaN</span><span class="sxs-lookup"><span data-stu-id="b231a-139">NaN</span></span>     |



 

<span data-ttu-id="b231a-140">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b231a-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b231a-141">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="b231a-141">Vertex Shader</span></span> | <span data-ttu-id="b231a-142">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="b231a-142">Geometry Shader</span></span> | <span data-ttu-id="b231a-143">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="b231a-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b231a-144">x</span><span class="sxs-lookup"><span data-stu-id="b231a-144">x</span></span>             | <span data-ttu-id="b231a-145">x</span><span class="sxs-lookup"><span data-stu-id="b231a-145">x</span></span>               | <span data-ttu-id="b231a-146">x</span><span class="sxs-lookup"><span data-stu-id="b231a-146">x</span></span>            |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="b231a-147">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b231a-147">Minimum Shader Model</span></span>

<span data-ttu-id="b231a-148">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="b231a-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b231a-149">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b231a-149">Shader Model</span></span>                                              | <span data-ttu-id="b231a-150">Supportato</span><span class="sxs-lookup"><span data-stu-id="b231a-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b231a-151">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b231a-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b231a-152">sì</span><span class="sxs-lookup"><span data-stu-id="b231a-152">yes</span></span>       |
| [<span data-ttu-id="b231a-153">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="b231a-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b231a-154">sì</span><span class="sxs-lookup"><span data-stu-id="b231a-154">yes</span></span>       |
| [<span data-ttu-id="b231a-155">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="b231a-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b231a-156">sì</span><span class="sxs-lookup"><span data-stu-id="b231a-156">yes</span></span>       |
| [<span data-ttu-id="b231a-157">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b231a-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b231a-158">no</span><span class="sxs-lookup"><span data-stu-id="b231a-158">no</span></span>        |
| [<span data-ttu-id="b231a-159">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b231a-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b231a-160">no</span><span class="sxs-lookup"><span data-stu-id="b231a-160">no</span></span>        |
| [<span data-ttu-id="b231a-161">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b231a-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b231a-162">no</span><span class="sxs-lookup"><span data-stu-id="b231a-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b231a-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b231a-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b231a-164">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b231a-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





