---
title: log (sm4 - asm)
description: Log per componente in base 2.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e4b89b4dcc085cf4fd4fda762d96fb71271af2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998318"
---
# <a name="log-sm4---asm"></a><span data-ttu-id="9cd5e-103">log (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="9cd5e-103">log (sm4 - asm)</span></span>

<span data-ttu-id="9cd5e-104">Log per componente in base 2.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-104">Component-wise log base 2.</span></span>



| <span data-ttu-id="9cd5e-105">log \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle</span><span class="sxs-lookup"><span data-stu-id="9cd5e-105">log\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="9cd5e-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="9cd5e-106">Item</span></span>                                                            | <span data-ttu-id="9cd5e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cd5e-107">Description</span></span>                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd5e-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="9cd5e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9cd5e-109">\[in \] Indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="9cd5e-110">dest = log2(src0)</span><span class="sxs-lookup"><span data-stu-id="9cd5e-110">dest = log2(src0)</span></span><br/> |
| <span data-ttu-id="9cd5e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9cd5e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9cd5e-112">\[in \] Valore per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-112">\[in\] The value for the operation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="9cd5e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cd5e-113">Remarks</span></span>

### <a name="restrictions"></a><span data-ttu-id="9cd5e-114">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="9cd5e-114">Restrictions</span></span>

-   <span data-ttu-id="9cd5e-115">Segue la teoria dei limiti.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-115">Follows limit theory.</span></span>
-   <span data-ttu-id="9cd5e-116">Tolleranza di errore: se *src0* è \[ 0.5..2, l'errore absolue non deve essere \] maggiore di 2-21.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-116">Error tolerance: If *src0* is \[0.5..2\], absolue error must be no more than 2-21.</span></span> <span data-ttu-id="9cd5e-117">Se *src0* è (0..0.5) o (2..+INF), l'errore relativo non deve essere \] maggiore di 2-21.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-117">If *src0* is (0..0.5) or (2..+INF\], relative error must be no more than 2-21.</span></span>

<span data-ttu-id="9cd5e-118">Nella tabella seguente vengono illustrati i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichi alcun overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-118">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="9cd5e-119">F indica un numero finito-reale.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-119">F means finite-real number.</span></span>



| <span data-ttu-id="9cd5e-120">**src**</span><span class="sxs-lookup"><span data-stu-id="9cd5e-120">**src**</span></span>  | <span data-ttu-id="9cd5e-121">**-inf**</span><span class="sxs-lookup"><span data-stu-id="9cd5e-121">**-inf**</span></span> | <span data-ttu-id="9cd5e-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="9cd5e-122">**-F**</span></span> | <span data-ttu-id="9cd5e-123">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="9cd5e-123">**-denorm**</span></span> | <span data-ttu-id="9cd5e-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="9cd5e-124">**-0**</span></span> | <span data-ttu-id="9cd5e-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="9cd5e-125">**+0**</span></span> | <span data-ttu-id="9cd5e-126">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="9cd5e-126">**+denorm**</span></span> | <span data-ttu-id="9cd5e-127">**+F**</span><span class="sxs-lookup"><span data-stu-id="9cd5e-127">**+F**</span></span> | <span data-ttu-id="9cd5e-128">**+inf**</span><span class="sxs-lookup"><span data-stu-id="9cd5e-128">**+inf**</span></span> | <span data-ttu-id="9cd5e-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="9cd5e-129">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="9cd5e-130">**Dest**</span><span class="sxs-lookup"><span data-stu-id="9cd5e-130">**dest**</span></span> | <span data-ttu-id="9cd5e-131">NaN</span><span class="sxs-lookup"><span data-stu-id="9cd5e-131">NaN</span></span>      | <span data-ttu-id="9cd5e-132">NaN</span><span class="sxs-lookup"><span data-stu-id="9cd5e-132">NaN</span></span>    | <span data-ttu-id="9cd5e-133">-inf</span><span class="sxs-lookup"><span data-stu-id="9cd5e-133">-inf</span></span>        | <span data-ttu-id="9cd5e-134">-inf</span><span class="sxs-lookup"><span data-stu-id="9cd5e-134">-inf</span></span>   | <span data-ttu-id="9cd5e-135">-inf</span><span class="sxs-lookup"><span data-stu-id="9cd5e-135">-inf</span></span>   | <span data-ttu-id="9cd5e-136">-inf</span><span class="sxs-lookup"><span data-stu-id="9cd5e-136">-inf</span></span>        | <span data-ttu-id="9cd5e-137">F</span><span class="sxs-lookup"><span data-stu-id="9cd5e-137">F</span></span>      | <span data-ttu-id="9cd5e-138">+inf</span><span class="sxs-lookup"><span data-stu-id="9cd5e-138">+inf</span></span>     | <span data-ttu-id="9cd5e-139">NaN</span><span class="sxs-lookup"><span data-stu-id="9cd5e-139">NaN</span></span>     |



 

<span data-ttu-id="9cd5e-140">Questa istruzione si applica alle fasi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="9cd5e-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9cd5e-141">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="9cd5e-141">Vertex Shader</span></span> | <span data-ttu-id="9cd5e-142">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="9cd5e-142">Geometry Shader</span></span> | <span data-ttu-id="9cd5e-143">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="9cd5e-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9cd5e-144">x</span><span class="sxs-lookup"><span data-stu-id="9cd5e-144">x</span></span>             | <span data-ttu-id="9cd5e-145">x</span><span class="sxs-lookup"><span data-stu-id="9cd5e-145">x</span></span>               | <span data-ttu-id="9cd5e-146">x</span><span class="sxs-lookup"><span data-stu-id="9cd5e-146">x</span></span>            |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="9cd5e-147">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="9cd5e-147">Minimum Shader Model</span></span>

<span data-ttu-id="9cd5e-148">Questa funzione è supportata nei modelli di shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9cd5e-149">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="9cd5e-149">Shader Model</span></span>                                              | <span data-ttu-id="9cd5e-150">Supportato</span><span class="sxs-lookup"><span data-stu-id="9cd5e-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9cd5e-151">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="9cd5e-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9cd5e-152">sì</span><span class="sxs-lookup"><span data-stu-id="9cd5e-152">yes</span></span>       |
| [<span data-ttu-id="9cd5e-153">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="9cd5e-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9cd5e-154">sì</span><span class="sxs-lookup"><span data-stu-id="9cd5e-154">yes</span></span>       |
| [<span data-ttu-id="9cd5e-155">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="9cd5e-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9cd5e-156">sì</span><span class="sxs-lookup"><span data-stu-id="9cd5e-156">yes</span></span>       |
| [<span data-ttu-id="9cd5e-157">Modello shader 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9cd5e-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9cd5e-158">no</span><span class="sxs-lookup"><span data-stu-id="9cd5e-158">no</span></span>        |
| [<span data-ttu-id="9cd5e-159">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9cd5e-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9cd5e-160">no</span><span class="sxs-lookup"><span data-stu-id="9cd5e-160">no</span></span>        |
| [<span data-ttu-id="9cd5e-161">Modello shader 1 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="9cd5e-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9cd5e-162">no</span><span class="sxs-lookup"><span data-stu-id="9cd5e-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9cd5e-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9cd5e-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cd5e-164">Assembly del modello shader 4 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="9cd5e-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





