---
title: add (sm4 - asm)
description: Aggiunta di 2 vettori a livello di componente.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e34f0a95ad9ee9ae4bdeed317eef133e3773311
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994978"
---
# <a name="add-sm4---asm"></a><span data-ttu-id="b6358-103">add (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="b6358-103">add (sm4 - asm)</span></span>

<span data-ttu-id="b6358-104">Aggiunta di 2 vettori a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="b6358-104">Component-wise add of 2 vectors.</span></span>



| <span data-ttu-id="b6358-105">add \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b6358-105">add\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b6358-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="b6358-106">Item</span></span>                                                            | <span data-ttu-id="b6358-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6358-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b6358-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="b6358-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b6358-109">\[in \] Indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b6358-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="b6358-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b6358-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b6358-111">\[in \] Vettore da aggiungere a *src1.*</span><span class="sxs-lookup"><span data-stu-id="b6358-111">\[in\] The vector to add to *src1*.</span></span><br/>                |
| <span data-ttu-id="b6358-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="b6358-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b6358-113">\[in \] Vettore da aggiungere a *src0*.</span><span class="sxs-lookup"><span data-stu-id="b6358-113">\[in\] The vector to add to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="b6358-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6358-114">Remarks</span></span>

<span data-ttu-id="b6358-115">La tabella seguente mostra i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="b6358-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="b6358-116">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="b6358-116">F means finite real number.</span></span>



| <span data-ttu-id="b6358-117">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="b6358-117">**src0 src1->**</span></span> | <span data-ttu-id="b6358-118">**-inf**</span><span class="sxs-lookup"><span data-stu-id="b6358-118">**-inf**</span></span> | <span data-ttu-id="b6358-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="b6358-119">**-F**</span></span>     | <span data-ttu-id="b6358-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="b6358-120">**-denorm**</span></span> | <span data-ttu-id="b6358-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="b6358-121">**-0**</span></span> | <span data-ttu-id="b6358-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="b6358-122">**+0**</span></span> | <span data-ttu-id="b6358-123">**denorm**</span><span class="sxs-lookup"><span data-stu-id="b6358-123">**denorm**</span></span> | <span data-ttu-id="b6358-124">**+F**</span><span class="sxs-lookup"><span data-stu-id="b6358-124">**+F**</span></span>     | <span data-ttu-id="b6358-125">**+inf**</span><span class="sxs-lookup"><span data-stu-id="b6358-125">**+inf**</span></span> | <span data-ttu-id="b6358-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="b6358-126">**NaN**</span></span> |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| <span data-ttu-id="b6358-127">**-inf**</span><span class="sxs-lookup"><span data-stu-id="b6358-127">**-inf**</span></span>           | <span data-ttu-id="b6358-128">-inf</span><span class="sxs-lookup"><span data-stu-id="b6358-128">-inf</span></span>     | <span data-ttu-id="b6358-129">-inf</span><span class="sxs-lookup"><span data-stu-id="b6358-129">-inf</span></span>       | <span data-ttu-id="b6358-130">-inf</span><span class="sxs-lookup"><span data-stu-id="b6358-130">-inf</span></span>        | <span data-ttu-id="b6358-131">-inf</span><span class="sxs-lookup"><span data-stu-id="b6358-131">-inf</span></span>   | <span data-ttu-id="b6358-132">-inf</span><span class="sxs-lookup"><span data-stu-id="b6358-132">-inf</span></span>   | <span data-ttu-id="b6358-133">-inf</span><span class="sxs-lookup"><span data-stu-id="b6358-133">-inf</span></span>       | <span data-ttu-id="b6358-134">-inf</span><span class="sxs-lookup"><span data-stu-id="b6358-134">-inf</span></span>       | <span data-ttu-id="b6358-135">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-135">NaN</span></span>      | <span data-ttu-id="b6358-136">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-136">NaN</span></span>     |
| <span data-ttu-id="b6358-137">**-F**</span><span class="sxs-lookup"><span data-stu-id="b6358-137">**-F**</span></span>             | <span data-ttu-id="b6358-138">-inf</span><span class="sxs-lookup"><span data-stu-id="b6358-138">-inf</span></span>     | <span data-ttu-id="b6358-139">-F</span><span class="sxs-lookup"><span data-stu-id="b6358-139">-F</span></span>         | <span data-ttu-id="b6358-140">src0</span><span class="sxs-lookup"><span data-stu-id="b6358-140">src0</span></span>        | <span data-ttu-id="b6358-141">src0</span><span class="sxs-lookup"><span data-stu-id="b6358-141">src0</span></span>   | <span data-ttu-id="b6358-142">src0</span><span class="sxs-lookup"><span data-stu-id="b6358-142">src0</span></span>   | <span data-ttu-id="b6358-143">src0</span><span class="sxs-lookup"><span data-stu-id="b6358-143">src0</span></span>       | <span data-ttu-id="b6358-144">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="b6358-144">+-F or +-0</span></span> | <span data-ttu-id="b6358-145">+inf</span><span class="sxs-lookup"><span data-stu-id="b6358-145">+inf</span></span>     | <span data-ttu-id="b6358-146">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-146">NaN</span></span>     |
| <span data-ttu-id="b6358-147">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="b6358-147">**-denorm**</span></span>        | <span data-ttu-id="b6358-148">-inf</span><span class="sxs-lookup"><span data-stu-id="b6358-148">-inf</span></span>     | <span data-ttu-id="b6358-149">src1</span><span class="sxs-lookup"><span data-stu-id="b6358-149">src1</span></span>       | <span data-ttu-id="b6358-150">-0</span><span class="sxs-lookup"><span data-stu-id="b6358-150">-0</span></span>          | <span data-ttu-id="b6358-151">-0</span><span class="sxs-lookup"><span data-stu-id="b6358-151">-0</span></span>     | <span data-ttu-id="b6358-152">+0</span><span class="sxs-lookup"><span data-stu-id="b6358-152">+0</span></span>     | <span data-ttu-id="b6358-153">+0</span><span class="sxs-lookup"><span data-stu-id="b6358-153">+0</span></span>         | <span data-ttu-id="b6358-154">src1</span><span class="sxs-lookup"><span data-stu-id="b6358-154">src1</span></span>       | <span data-ttu-id="b6358-155">+inf</span><span class="sxs-lookup"><span data-stu-id="b6358-155">+inf</span></span>     | <span data-ttu-id="b6358-156">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-156">NaN</span></span>     |
| <span data-ttu-id="b6358-157">**-0**</span><span class="sxs-lookup"><span data-stu-id="b6358-157">**-0**</span></span>             | <span data-ttu-id="b6358-158">-inf</span><span class="sxs-lookup"><span data-stu-id="b6358-158">-inf</span></span>     | <span data-ttu-id="b6358-159">src1</span><span class="sxs-lookup"><span data-stu-id="b6358-159">src1</span></span>       | <span data-ttu-id="b6358-160">-0</span><span class="sxs-lookup"><span data-stu-id="b6358-160">-0</span></span>          | <span data-ttu-id="b6358-161">-0</span><span class="sxs-lookup"><span data-stu-id="b6358-161">-0</span></span>     | <span data-ttu-id="b6358-162">+0</span><span class="sxs-lookup"><span data-stu-id="b6358-162">+0</span></span>     | <span data-ttu-id="b6358-163">+0</span><span class="sxs-lookup"><span data-stu-id="b6358-163">+0</span></span>         | <span data-ttu-id="b6358-164">src1</span><span class="sxs-lookup"><span data-stu-id="b6358-164">src1</span></span>       | <span data-ttu-id="b6358-165">+inf</span><span class="sxs-lookup"><span data-stu-id="b6358-165">+inf</span></span>     | <span data-ttu-id="b6358-166">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-166">NaN</span></span>     |
| <span data-ttu-id="b6358-167">**+0**</span><span class="sxs-lookup"><span data-stu-id="b6358-167">**+0**</span></span>             | <span data-ttu-id="b6358-168">i-inf</span><span class="sxs-lookup"><span data-stu-id="b6358-168">i-inf</span></span>    | <span data-ttu-id="b6358-169">src1</span><span class="sxs-lookup"><span data-stu-id="b6358-169">src1</span></span>       | <span data-ttu-id="b6358-170">+0</span><span class="sxs-lookup"><span data-stu-id="b6358-170">+0</span></span>          | <span data-ttu-id="b6358-171">+0</span><span class="sxs-lookup"><span data-stu-id="b6358-171">+0</span></span>     | <span data-ttu-id="b6358-172">+0</span><span class="sxs-lookup"><span data-stu-id="b6358-172">+0</span></span>     | <span data-ttu-id="b6358-173">+0</span><span class="sxs-lookup"><span data-stu-id="b6358-173">+0</span></span>         | <span data-ttu-id="b6358-174">src1</span><span class="sxs-lookup"><span data-stu-id="b6358-174">src1</span></span>       | <span data-ttu-id="b6358-175">+inf</span><span class="sxs-lookup"><span data-stu-id="b6358-175">+inf</span></span>     | <span data-ttu-id="b6358-176">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-176">NaN</span></span>     |
| <span data-ttu-id="b6358-177">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="b6358-177">**+denorm**</span></span>        | <span data-ttu-id="b6358-178">-inf</span><span class="sxs-lookup"><span data-stu-id="b6358-178">-inf</span></span>     | <span data-ttu-id="b6358-179">src1</span><span class="sxs-lookup"><span data-stu-id="b6358-179">src1</span></span>       | <span data-ttu-id="b6358-180">+0</span><span class="sxs-lookup"><span data-stu-id="b6358-180">+0</span></span>          | <span data-ttu-id="b6358-181">+0</span><span class="sxs-lookup"><span data-stu-id="b6358-181">+0</span></span>     | <span data-ttu-id="b6358-182">+0</span><span class="sxs-lookup"><span data-stu-id="b6358-182">+0</span></span>     | <span data-ttu-id="b6358-183">+0</span><span class="sxs-lookup"><span data-stu-id="b6358-183">+0</span></span>         | <span data-ttu-id="b6358-184">src1</span><span class="sxs-lookup"><span data-stu-id="b6358-184">src1</span></span>       | <span data-ttu-id="b6358-185">+inf</span><span class="sxs-lookup"><span data-stu-id="b6358-185">+inf</span></span>     | <span data-ttu-id="b6358-186">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-186">NaN</span></span>     |
| <span data-ttu-id="b6358-187">**+F**</span><span class="sxs-lookup"><span data-stu-id="b6358-187">**+F**</span></span>             | <span data-ttu-id="b6358-188">-inf</span><span class="sxs-lookup"><span data-stu-id="b6358-188">-inf</span></span>     | <span data-ttu-id="b6358-189">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="b6358-189">+-F or +-0</span></span> | <span data-ttu-id="b6358-190">src0</span><span class="sxs-lookup"><span data-stu-id="b6358-190">src0</span></span>        | <span data-ttu-id="b6358-191">src0</span><span class="sxs-lookup"><span data-stu-id="b6358-191">src0</span></span>   | <span data-ttu-id="b6358-192">src0</span><span class="sxs-lookup"><span data-stu-id="b6358-192">src0</span></span>   | <span data-ttu-id="b6358-193">src0</span><span class="sxs-lookup"><span data-stu-id="b6358-193">src0</span></span>       | <span data-ttu-id="b6358-194">+F</span><span class="sxs-lookup"><span data-stu-id="b6358-194">+F</span></span>         | <span data-ttu-id="b6358-195">+inf</span><span class="sxs-lookup"><span data-stu-id="b6358-195">+inf</span></span>     | <span data-ttu-id="b6358-196">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-196">NaN</span></span>     |
| <span data-ttu-id="b6358-197">**+inf**</span><span class="sxs-lookup"><span data-stu-id="b6358-197">**+inf**</span></span>           | <span data-ttu-id="b6358-198">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-198">NaN</span></span>      | <span data-ttu-id="b6358-199">+inf</span><span class="sxs-lookup"><span data-stu-id="b6358-199">+inf</span></span>       | <span data-ttu-id="b6358-200">+inf</span><span class="sxs-lookup"><span data-stu-id="b6358-200">+inf</span></span>        | <span data-ttu-id="b6358-201">+inf</span><span class="sxs-lookup"><span data-stu-id="b6358-201">+inf</span></span>   | <span data-ttu-id="b6358-202">+inf</span><span class="sxs-lookup"><span data-stu-id="b6358-202">+inf</span></span>   | <span data-ttu-id="b6358-203">+inf</span><span class="sxs-lookup"><span data-stu-id="b6358-203">+inf</span></span>       | <span data-ttu-id="b6358-204">+inf</span><span class="sxs-lookup"><span data-stu-id="b6358-204">+inf</span></span>       | <span data-ttu-id="b6358-205">+inf</span><span class="sxs-lookup"><span data-stu-id="b6358-205">+inf</span></span>     | <span data-ttu-id="b6358-206">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-206">NaN</span></span>     |
| <span data-ttu-id="b6358-207">**NaN**</span><span class="sxs-lookup"><span data-stu-id="b6358-207">**NaN**</span></span>            | <span data-ttu-id="b6358-208">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-208">NaN</span></span>      | <span data-ttu-id="b6358-209">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-209">NaN</span></span>        | <span data-ttu-id="b6358-210">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-210">NaN</span></span>         | <span data-ttu-id="b6358-211">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-211">NaN</span></span>    | <span data-ttu-id="b6358-212">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-212">NaN</span></span>    | <span data-ttu-id="b6358-213">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-213">NaN</span></span>        | <span data-ttu-id="b6358-214">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-214">NaN</span></span>        | <span data-ttu-id="b6358-215">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-215">NaN</span></span>      | <span data-ttu-id="b6358-216">NaN</span><span class="sxs-lookup"><span data-stu-id="b6358-216">NaN</span></span>     |



 

<span data-ttu-id="b6358-217">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b6358-217">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b6358-218">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="b6358-218">Vertex Shader</span></span> | <span data-ttu-id="b6358-219">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="b6358-219">Geometry Shader</span></span> | <span data-ttu-id="b6358-220">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="b6358-220">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b6358-221">x</span><span class="sxs-lookup"><span data-stu-id="b6358-221">x</span></span>             | <span data-ttu-id="b6358-222">x</span><span class="sxs-lookup"><span data-stu-id="b6358-222">x</span></span>               | <span data-ttu-id="b6358-223">x</span><span class="sxs-lookup"><span data-stu-id="b6358-223">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b6358-224">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="b6358-224">Minimum Shader Model</span></span>

<span data-ttu-id="b6358-225">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="b6358-225">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b6358-226">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b6358-226">Shader Model</span></span>                                              | <span data-ttu-id="b6358-227">Supportato</span><span class="sxs-lookup"><span data-stu-id="b6358-227">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b6358-228">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="b6358-228">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b6358-229">sì</span><span class="sxs-lookup"><span data-stu-id="b6358-229">yes</span></span>       |
| [<span data-ttu-id="b6358-230">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="b6358-230">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b6358-231">sì</span><span class="sxs-lookup"><span data-stu-id="b6358-231">yes</span></span>       |
| [<span data-ttu-id="b6358-232">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="b6358-232">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b6358-233">sì</span><span class="sxs-lookup"><span data-stu-id="b6358-233">yes</span></span>       |
| [<span data-ttu-id="b6358-234">Modello shader 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6358-234">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b6358-235">no</span><span class="sxs-lookup"><span data-stu-id="b6358-235">no</span></span>        |
| [<span data-ttu-id="b6358-236">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6358-236">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b6358-237">no</span><span class="sxs-lookup"><span data-stu-id="b6358-237">no</span></span>        |
| [<span data-ttu-id="b6358-238">Modello shader 1 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="b6358-238">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b6358-239">no</span><span class="sxs-lookup"><span data-stu-id="b6358-239">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b6358-240">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b6358-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6358-241">Assembly del modello shader 4 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="b6358-241">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





