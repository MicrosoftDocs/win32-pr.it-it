---
title: Aggiungi (SM4-ASM)
description: Aggiunta di 2 vettori a livello di componente.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5630b983c88da3ba512b5fece6202e0217b2ed39
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516507"
---
# <a name="add-sm4---asm"></a><span data-ttu-id="c0fa7-103">Aggiungi (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c0fa7-103">add (sm4 - asm)</span></span>

<span data-ttu-id="c0fa7-104">Aggiunta di 2 vettori a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-104">Component-wise add of 2 vectors.</span></span>



| <span data-ttu-id="c0fa7-105">aggiungere \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c0fa7-105">add\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c0fa7-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="c0fa7-106">Item</span></span>                                                            | <span data-ttu-id="c0fa7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0fa7-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c0fa7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c0fa7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c0fa7-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="c0fa7-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c0fa7-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c0fa7-111">\[nel \] vettore da aggiungere a *src1*.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-111">\[in\] The vector to add to *src1*.</span></span><br/>                |
| <span data-ttu-id="c0fa7-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="c0fa7-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c0fa7-113">\[nel \] vettore da aggiungere a *src0*.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-113">\[in\] The vector to add to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="c0fa7-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0fa7-114">Remarks</span></span>

<span data-ttu-id="c0fa7-115">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="c0fa7-116">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-116">F means finite real number.</span></span>



|                    |          |            |             |        |        |            |            |          |         |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| <span data-ttu-id="c0fa7-117">**src1 src0->**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-117">**src0 src1->**</span></span> | <span data-ttu-id="c0fa7-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-118">**-inf**</span></span> | <span data-ttu-id="c0fa7-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-119">**-F**</span></span>     | <span data-ttu-id="c0fa7-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-120">**-denorm**</span></span> | <span data-ttu-id="c0fa7-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-121">**-0**</span></span> | <span data-ttu-id="c0fa7-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-122">**+0**</span></span> | <span data-ttu-id="c0fa7-123">**denorm**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-123">**denorm**</span></span> | <span data-ttu-id="c0fa7-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-124">**+F**</span></span>     | <span data-ttu-id="c0fa7-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-125">**+inf**</span></span> | <span data-ttu-id="c0fa7-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-126">**NaN**</span></span> |
| <span data-ttu-id="c0fa7-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-127">**-inf**</span></span>           | <span data-ttu-id="c0fa7-128">-inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-128">-inf</span></span>     | <span data-ttu-id="c0fa7-129">-inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-129">-inf</span></span>       | <span data-ttu-id="c0fa7-130">-inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-130">-inf</span></span>        | <span data-ttu-id="c0fa7-131">-inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-131">-inf</span></span>   | <span data-ttu-id="c0fa7-132">-inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-132">-inf</span></span>   | <span data-ttu-id="c0fa7-133">-inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-133">-inf</span></span>       | <span data-ttu-id="c0fa7-134">-inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-134">-inf</span></span>       | <span data-ttu-id="c0fa7-135">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-135">NaN</span></span>      | <span data-ttu-id="c0fa7-136">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-136">NaN</span></span>     |
| <span data-ttu-id="c0fa7-137">**-F**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-137">**-F**</span></span>             | <span data-ttu-id="c0fa7-138">-inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-138">-inf</span></span>     | <span data-ttu-id="c0fa7-139">-F</span><span class="sxs-lookup"><span data-stu-id="c0fa7-139">-F</span></span>         | <span data-ttu-id="c0fa7-140">src0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-140">src0</span></span>        | <span data-ttu-id="c0fa7-141">src0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-141">src0</span></span>   | <span data-ttu-id="c0fa7-142">src0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-142">src0</span></span>   | <span data-ttu-id="c0fa7-143">src0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-143">src0</span></span>       | <span data-ttu-id="c0fa7-144">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-144">+-F or +-0</span></span> | <span data-ttu-id="c0fa7-145">+inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-145">+inf</span></span>     | <span data-ttu-id="c0fa7-146">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-146">NaN</span></span>     |
| <span data-ttu-id="c0fa7-147">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-147">**-denorm**</span></span>        | <span data-ttu-id="c0fa7-148">-inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-148">-inf</span></span>     | <span data-ttu-id="c0fa7-149">src1</span><span class="sxs-lookup"><span data-stu-id="c0fa7-149">src1</span></span>       | <span data-ttu-id="c0fa7-150">-0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-150">-0</span></span>          | <span data-ttu-id="c0fa7-151">-0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-151">-0</span></span>     | <span data-ttu-id="c0fa7-152">+0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-152">+0</span></span>     | <span data-ttu-id="c0fa7-153">+0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-153">+0</span></span>         | <span data-ttu-id="c0fa7-154">src1</span><span class="sxs-lookup"><span data-stu-id="c0fa7-154">src1</span></span>       | <span data-ttu-id="c0fa7-155">+inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-155">+inf</span></span>     | <span data-ttu-id="c0fa7-156">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-156">NaN</span></span>     |
| <span data-ttu-id="c0fa7-157">**-0**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-157">**-0**</span></span>             | <span data-ttu-id="c0fa7-158">-inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-158">-inf</span></span>     | <span data-ttu-id="c0fa7-159">src1</span><span class="sxs-lookup"><span data-stu-id="c0fa7-159">src1</span></span>       | <span data-ttu-id="c0fa7-160">-0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-160">-0</span></span>          | <span data-ttu-id="c0fa7-161">-0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-161">-0</span></span>     | <span data-ttu-id="c0fa7-162">+0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-162">+0</span></span>     | <span data-ttu-id="c0fa7-163">+0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-163">+0</span></span>         | <span data-ttu-id="c0fa7-164">src1</span><span class="sxs-lookup"><span data-stu-id="c0fa7-164">src1</span></span>       | <span data-ttu-id="c0fa7-165">+inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-165">+inf</span></span>     | <span data-ttu-id="c0fa7-166">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-166">NaN</span></span>     |
| <span data-ttu-id="c0fa7-167">**+0**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-167">**+0**</span></span>             | <span data-ttu-id="c0fa7-168">i-INF</span><span class="sxs-lookup"><span data-stu-id="c0fa7-168">i-inf</span></span>    | <span data-ttu-id="c0fa7-169">src1</span><span class="sxs-lookup"><span data-stu-id="c0fa7-169">src1</span></span>       | <span data-ttu-id="c0fa7-170">+0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-170">+0</span></span>          | <span data-ttu-id="c0fa7-171">+0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-171">+0</span></span>     | <span data-ttu-id="c0fa7-172">+0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-172">+0</span></span>     | <span data-ttu-id="c0fa7-173">+0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-173">+0</span></span>         | <span data-ttu-id="c0fa7-174">src1</span><span class="sxs-lookup"><span data-stu-id="c0fa7-174">src1</span></span>       | <span data-ttu-id="c0fa7-175">+inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-175">+inf</span></span>     | <span data-ttu-id="c0fa7-176">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-176">NaN</span></span>     |
| <span data-ttu-id="c0fa7-177">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-177">**+denorm**</span></span>        | <span data-ttu-id="c0fa7-178">-inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-178">-inf</span></span>     | <span data-ttu-id="c0fa7-179">src1</span><span class="sxs-lookup"><span data-stu-id="c0fa7-179">src1</span></span>       | <span data-ttu-id="c0fa7-180">+0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-180">+0</span></span>          | <span data-ttu-id="c0fa7-181">+0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-181">+0</span></span>     | <span data-ttu-id="c0fa7-182">+0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-182">+0</span></span>     | <span data-ttu-id="c0fa7-183">+0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-183">+0</span></span>         | <span data-ttu-id="c0fa7-184">src1</span><span class="sxs-lookup"><span data-stu-id="c0fa7-184">src1</span></span>       | <span data-ttu-id="c0fa7-185">+inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-185">+inf</span></span>     | <span data-ttu-id="c0fa7-186">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-186">NaN</span></span>     |
| <span data-ttu-id="c0fa7-187">**+ F**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-187">**+F**</span></span>             | <span data-ttu-id="c0fa7-188">-inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-188">-inf</span></span>     | <span data-ttu-id="c0fa7-189">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-189">+-F or +-0</span></span> | <span data-ttu-id="c0fa7-190">src0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-190">src0</span></span>        | <span data-ttu-id="c0fa7-191">src0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-191">src0</span></span>   | <span data-ttu-id="c0fa7-192">src0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-192">src0</span></span>   | <span data-ttu-id="c0fa7-193">src0</span><span class="sxs-lookup"><span data-stu-id="c0fa7-193">src0</span></span>       | <span data-ttu-id="c0fa7-194">+ F</span><span class="sxs-lookup"><span data-stu-id="c0fa7-194">+F</span></span>         | <span data-ttu-id="c0fa7-195">+inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-195">+inf</span></span>     | <span data-ttu-id="c0fa7-196">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-196">NaN</span></span>     |
| <span data-ttu-id="c0fa7-197">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-197">**+inf**</span></span>           | <span data-ttu-id="c0fa7-198">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-198">NaN</span></span>      | <span data-ttu-id="c0fa7-199">+inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-199">+inf</span></span>       | <span data-ttu-id="c0fa7-200">+inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-200">+inf</span></span>        | <span data-ttu-id="c0fa7-201">+inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-201">+inf</span></span>   | <span data-ttu-id="c0fa7-202">+inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-202">+inf</span></span>   | <span data-ttu-id="c0fa7-203">+inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-203">+inf</span></span>       | <span data-ttu-id="c0fa7-204">+inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-204">+inf</span></span>       | <span data-ttu-id="c0fa7-205">+inf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-205">+inf</span></span>     | <span data-ttu-id="c0fa7-206">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-206">NaN</span></span>     |
| <span data-ttu-id="c0fa7-207">**NaN**</span><span class="sxs-lookup"><span data-stu-id="c0fa7-207">**NaN**</span></span>            | <span data-ttu-id="c0fa7-208">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-208">NaN</span></span>      | <span data-ttu-id="c0fa7-209">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-209">NaN</span></span>        | <span data-ttu-id="c0fa7-210">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-210">NaN</span></span>         | <span data-ttu-id="c0fa7-211">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-211">NaN</span></span>    | <span data-ttu-id="c0fa7-212">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-212">NaN</span></span>    | <span data-ttu-id="c0fa7-213">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-213">NaN</span></span>        | <span data-ttu-id="c0fa7-214">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-214">NaN</span></span>        | <span data-ttu-id="c0fa7-215">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-215">NaN</span></span>      | <span data-ttu-id="c0fa7-216">NaN</span><span class="sxs-lookup"><span data-stu-id="c0fa7-216">NaN</span></span>     |



 

<span data-ttu-id="c0fa7-217">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="c0fa7-217">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c0fa7-218">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="c0fa7-218">Vertex Shader</span></span> | <span data-ttu-id="c0fa7-219">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="c0fa7-219">Geometry Shader</span></span> | <span data-ttu-id="c0fa7-220">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="c0fa7-220">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c0fa7-221">x</span><span class="sxs-lookup"><span data-stu-id="c0fa7-221">x</span></span>             | <span data-ttu-id="c0fa7-222">x</span><span class="sxs-lookup"><span data-stu-id="c0fa7-222">x</span></span>               | <span data-ttu-id="c0fa7-223">x</span><span class="sxs-lookup"><span data-stu-id="c0fa7-223">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c0fa7-224">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="c0fa7-224">Minimum Shader Model</span></span>

<span data-ttu-id="c0fa7-225">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-225">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c0fa7-226">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="c0fa7-226">Shader Model</span></span>                                              | <span data-ttu-id="c0fa7-227">Supportato</span><span class="sxs-lookup"><span data-stu-id="c0fa7-227">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c0fa7-228">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="c0fa7-228">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c0fa7-229">sì</span><span class="sxs-lookup"><span data-stu-id="c0fa7-229">yes</span></span>       |
| [<span data-ttu-id="c0fa7-230">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="c0fa7-230">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c0fa7-231">sì</span><span class="sxs-lookup"><span data-stu-id="c0fa7-231">yes</span></span>       |
| [<span data-ttu-id="c0fa7-232">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="c0fa7-232">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c0fa7-233">sì</span><span class="sxs-lookup"><span data-stu-id="c0fa7-233">yes</span></span>       |
| [<span data-ttu-id="c0fa7-234">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0fa7-234">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c0fa7-235">no</span><span class="sxs-lookup"><span data-stu-id="c0fa7-235">no</span></span>        |
| [<span data-ttu-id="c0fa7-236">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0fa7-236">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c0fa7-237">no</span><span class="sxs-lookup"><span data-stu-id="c0fa7-237">no</span></span>        |
| [<span data-ttu-id="c0fa7-238">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0fa7-238">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c0fa7-239">no</span><span class="sxs-lookup"><span data-stu-id="c0fa7-239">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c0fa7-240">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c0fa7-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0fa7-241">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0fa7-241">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





