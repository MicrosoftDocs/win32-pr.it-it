---
title: dmul (sm5 - asm)
description: Moltiplicazione a precisione doppia per componente.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5d311cb5c958e8b7403197027c9854d1a93a64
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999088"
---
# <a name="dmul-sm5---asm"></a><span data-ttu-id="fd678-103">dmul (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="fd678-103">dmul (sm5 - asm)</span></span>

<span data-ttu-id="fd678-104">Moltiplicazione a precisione doppia per componente.</span><span class="sxs-lookup"><span data-stu-id="fd678-104">Component-wise double-precision multiply.</span></span>



| <span data-ttu-id="fd678-105">dmul \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="fd678-105">dmul\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="fd678-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="fd678-106">Item</span></span>                                                            | <span data-ttu-id="fd678-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd678-107">Description</span></span>                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd678-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="fd678-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="fd678-109">\[in \] Indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fd678-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="fd678-110">*dest*  =  *src0* \* *src1*</span><span class="sxs-lookup"><span data-stu-id="fd678-110">*dest* = *src0* \* *src1*</span></span><br/> |
| <span data-ttu-id="fd678-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="fd678-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="fd678-112">\[in \] I componenti da moltiplicare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="fd678-112">\[in\] The components to multiply with *src1*.</span></span><br/>                                          |
| <span data-ttu-id="fd678-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="fd678-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="fd678-114">\[in \] I componenti da moltiplicare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="fd678-114">\[in\] The components to multiply with *src0*.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="fd678-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd678-115">Remarks</span></span>

<span data-ttu-id="fd678-116">Gli swizzle validi per i parametri di origine sono xyzw, xyxy, zwxy, zwzw.</span><span class="sxs-lookup"><span data-stu-id="fd678-116">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="fd678-117">Le maschere *dest* valide sono xy, zw e xyzw.</span><span class="sxs-lookup"><span data-stu-id="fd678-117">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="fd678-118">I mapping *src* seguenti sono post-swizzle:</span><span class="sxs-lookup"><span data-stu-id="fd678-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="fd678-119">*dest* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="fd678-119">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="fd678-120">*src0* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="fd678-120">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="fd678-121">*src1* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="fd678-121">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="fd678-122">Nella tabella seguente vengono illustrati i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichi alcun overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="fd678-122">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="fd678-123">F indica un numero finito-reale.</span><span class="sxs-lookup"><span data-stu-id="fd678-123">F means finite-real number.</span></span>



| <span data-ttu-id="fd678-124">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="fd678-124">**src0 src1->**</span></span> | <span data-ttu-id="fd678-125">**-inf**</span><span class="sxs-lookup"><span data-stu-id="fd678-125">**-inf**</span></span> | <span data-ttu-id="fd678-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="fd678-126">**-F**</span></span> | <span data-ttu-id="fd678-127">**-1.0**</span><span class="sxs-lookup"><span data-stu-id="fd678-127">**-1.0**</span></span> | <span data-ttu-id="fd678-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="fd678-128">**-0**</span></span> | <span data-ttu-id="fd678-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="fd678-129">**+0**</span></span> | <span data-ttu-id="fd678-130">**+1.0**</span><span class="sxs-lookup"><span data-stu-id="fd678-130">**+1.0**</span></span> | <span data-ttu-id="fd678-131">**+F**</span><span class="sxs-lookup"><span data-stu-id="fd678-131">**+F**</span></span> | <span data-ttu-id="fd678-132">**+inf**</span><span class="sxs-lookup"><span data-stu-id="fd678-132">**+inf**</span></span> | <span data-ttu-id="fd678-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="fd678-133">**NaN**</span></span> |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="fd678-134">**-inf**</span><span class="sxs-lookup"><span data-stu-id="fd678-134">**-inf**</span></span>           | <span data-ttu-id="fd678-135">+inf</span><span class="sxs-lookup"><span data-stu-id="fd678-135">+inf</span></span>     | <span data-ttu-id="fd678-136">+inf</span><span class="sxs-lookup"><span data-stu-id="fd678-136">+inf</span></span>   | <span data-ttu-id="fd678-137">+inf</span><span class="sxs-lookup"><span data-stu-id="fd678-137">+inf</span></span>     | <span data-ttu-id="fd678-138">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-138">NaN</span></span>    | <span data-ttu-id="fd678-139">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-139">NaN</span></span>    | <span data-ttu-id="fd678-140">-inf</span><span class="sxs-lookup"><span data-stu-id="fd678-140">-inf</span></span>     | <span data-ttu-id="fd678-141">-inf</span><span class="sxs-lookup"><span data-stu-id="fd678-141">-inf</span></span>   | <span data-ttu-id="fd678-142">-inf</span><span class="sxs-lookup"><span data-stu-id="fd678-142">-inf</span></span>     | <span data-ttu-id="fd678-143">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-143">NaN</span></span>     |
| <span data-ttu-id="fd678-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="fd678-144">**-F**</span></span>             | <span data-ttu-id="fd678-145">+inf</span><span class="sxs-lookup"><span data-stu-id="fd678-145">+inf</span></span>     | <span data-ttu-id="fd678-146">+F</span><span class="sxs-lookup"><span data-stu-id="fd678-146">+F</span></span>     | <span data-ttu-id="fd678-147">-src0</span><span class="sxs-lookup"><span data-stu-id="fd678-147">-src0</span></span>    | <span data-ttu-id="fd678-148">+0</span><span class="sxs-lookup"><span data-stu-id="fd678-148">+0</span></span>     | <span data-ttu-id="fd678-149">-0</span><span class="sxs-lookup"><span data-stu-id="fd678-149">-0</span></span>     | <span data-ttu-id="fd678-150">src0</span><span class="sxs-lookup"><span data-stu-id="fd678-150">src0</span></span>     | <span data-ttu-id="fd678-151">-F</span><span class="sxs-lookup"><span data-stu-id="fd678-151">-F</span></span>     | <span data-ttu-id="fd678-152">-inf</span><span class="sxs-lookup"><span data-stu-id="fd678-152">-inf</span></span>     | <span data-ttu-id="fd678-153">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-153">NaN</span></span>     |
| <span data-ttu-id="fd678-154">**-1.0F**</span><span class="sxs-lookup"><span data-stu-id="fd678-154">**-1.0F**</span></span>          | <span data-ttu-id="fd678-155">+inf</span><span class="sxs-lookup"><span data-stu-id="fd678-155">+inf</span></span>     | <span data-ttu-id="fd678-156">-src1</span><span class="sxs-lookup"><span data-stu-id="fd678-156">-src1</span></span>  | <span data-ttu-id="fd678-157">+1.0</span><span class="sxs-lookup"><span data-stu-id="fd678-157">+1.0</span></span>     | <span data-ttu-id="fd678-158">+0</span><span class="sxs-lookup"><span data-stu-id="fd678-158">+0</span></span>     | <span data-ttu-id="fd678-159">-0</span><span class="sxs-lookup"><span data-stu-id="fd678-159">-0</span></span>     | <span data-ttu-id="fd678-160">-1.0</span><span class="sxs-lookup"><span data-stu-id="fd678-160">-1.0</span></span>     | <span data-ttu-id="fd678-161">-src1</span><span class="sxs-lookup"><span data-stu-id="fd678-161">-src1</span></span>  | <span data-ttu-id="fd678-162">-inf</span><span class="sxs-lookup"><span data-stu-id="fd678-162">-inf</span></span>     | <span data-ttu-id="fd678-163">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-163">NaN</span></span>     |
| <span data-ttu-id="fd678-164">**-0**</span><span class="sxs-lookup"><span data-stu-id="fd678-164">**-0**</span></span>             | <span data-ttu-id="fd678-165">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-165">NaN</span></span>      | <span data-ttu-id="fd678-166">+0</span><span class="sxs-lookup"><span data-stu-id="fd678-166">+0</span></span>     | <span data-ttu-id="fd678-167">+0</span><span class="sxs-lookup"><span data-stu-id="fd678-167">+0</span></span>       | <span data-ttu-id="fd678-168">+0</span><span class="sxs-lookup"><span data-stu-id="fd678-168">+0</span></span>     | <span data-ttu-id="fd678-169">-0</span><span class="sxs-lookup"><span data-stu-id="fd678-169">-0</span></span>     | <span data-ttu-id="fd678-170">-0</span><span class="sxs-lookup"><span data-stu-id="fd678-170">-0</span></span>       | <span data-ttu-id="fd678-171">-0</span><span class="sxs-lookup"><span data-stu-id="fd678-171">-0</span></span>     | <span data-ttu-id="fd678-172">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-172">NaN</span></span>      | <span data-ttu-id="fd678-173">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-173">NaN</span></span>     |
| <span data-ttu-id="fd678-174">**+0**</span><span class="sxs-lookup"><span data-stu-id="fd678-174">**+0**</span></span>             | <span data-ttu-id="fd678-175">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-175">NaN</span></span>      | <span data-ttu-id="fd678-176">-0</span><span class="sxs-lookup"><span data-stu-id="fd678-176">-0</span></span>     | <span data-ttu-id="fd678-177">-0</span><span class="sxs-lookup"><span data-stu-id="fd678-177">-0</span></span>       | <span data-ttu-id="fd678-178">-0</span><span class="sxs-lookup"><span data-stu-id="fd678-178">-0</span></span>     | <span data-ttu-id="fd678-179">+0</span><span class="sxs-lookup"><span data-stu-id="fd678-179">+0</span></span>     | <span data-ttu-id="fd678-180">+0</span><span class="sxs-lookup"><span data-stu-id="fd678-180">+0</span></span>       | <span data-ttu-id="fd678-181">+0</span><span class="sxs-lookup"><span data-stu-id="fd678-181">+0</span></span>     | <span data-ttu-id="fd678-182">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-182">NaN</span></span>      | <span data-ttu-id="fd678-183">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-183">NaN</span></span>     |
| <span data-ttu-id="fd678-184">**+1.0**</span><span class="sxs-lookup"><span data-stu-id="fd678-184">**+1.0**</span></span>           | <span data-ttu-id="fd678-185">-inf</span><span class="sxs-lookup"><span data-stu-id="fd678-185">-inf</span></span>     | <span data-ttu-id="fd678-186">src1</span><span class="sxs-lookup"><span data-stu-id="fd678-186">src1</span></span>   | <span data-ttu-id="fd678-187">-1.0</span><span class="sxs-lookup"><span data-stu-id="fd678-187">-1.0</span></span>     | <span data-ttu-id="fd678-188">-0</span><span class="sxs-lookup"><span data-stu-id="fd678-188">-0</span></span>     | <span data-ttu-id="fd678-189">+0</span><span class="sxs-lookup"><span data-stu-id="fd678-189">+0</span></span>     | <span data-ttu-id="fd678-190">+1</span><span class="sxs-lookup"><span data-stu-id="fd678-190">+1</span></span>       | <span data-ttu-id="fd678-191">src1</span><span class="sxs-lookup"><span data-stu-id="fd678-191">src1</span></span>   | <span data-ttu-id="fd678-192">+inf</span><span class="sxs-lookup"><span data-stu-id="fd678-192">+inf</span></span>     | <span data-ttu-id="fd678-193">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-193">NaN</span></span>     |
| <span data-ttu-id="fd678-194">**+F**</span><span class="sxs-lookup"><span data-stu-id="fd678-194">**+F**</span></span>             | <span data-ttu-id="fd678-195">-inf</span><span class="sxs-lookup"><span data-stu-id="fd678-195">-inf</span></span>     | <span data-ttu-id="fd678-196">-F</span><span class="sxs-lookup"><span data-stu-id="fd678-196">-F</span></span>     | <span data-ttu-id="fd678-197">-src0</span><span class="sxs-lookup"><span data-stu-id="fd678-197">-src0</span></span>    | <span data-ttu-id="fd678-198">-0</span><span class="sxs-lookup"><span data-stu-id="fd678-198">-0</span></span>     | <span data-ttu-id="fd678-199">+0</span><span class="sxs-lookup"><span data-stu-id="fd678-199">+0</span></span>     | <span data-ttu-id="fd678-200">src0</span><span class="sxs-lookup"><span data-stu-id="fd678-200">src0</span></span>     | <span data-ttu-id="fd678-201">+F</span><span class="sxs-lookup"><span data-stu-id="fd678-201">+F</span></span>     | <span data-ttu-id="fd678-202">+inf</span><span class="sxs-lookup"><span data-stu-id="fd678-202">+inf</span></span>     | <span data-ttu-id="fd678-203">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-203">NaN</span></span>     |
| <span data-ttu-id="fd678-204">**+inf**</span><span class="sxs-lookup"><span data-stu-id="fd678-204">**+inf**</span></span>           | <span data-ttu-id="fd678-205">-inf</span><span class="sxs-lookup"><span data-stu-id="fd678-205">-inf</span></span>     | <span data-ttu-id="fd678-206">-inf</span><span class="sxs-lookup"><span data-stu-id="fd678-206">-inf</span></span>   | <span data-ttu-id="fd678-207">-inf</span><span class="sxs-lookup"><span data-stu-id="fd678-207">-inf</span></span>     | <span data-ttu-id="fd678-208">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-208">NaN</span></span>    | <span data-ttu-id="fd678-209">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-209">NaN</span></span>    | <span data-ttu-id="fd678-210">+inf</span><span class="sxs-lookup"><span data-stu-id="fd678-210">+inf</span></span>     | <span data-ttu-id="fd678-211">+inf</span><span class="sxs-lookup"><span data-stu-id="fd678-211">+inf</span></span>   | <span data-ttu-id="fd678-212">+inf</span><span class="sxs-lookup"><span data-stu-id="fd678-212">+inf</span></span>     | <span data-ttu-id="fd678-213">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-213">NaN</span></span>     |
| <span data-ttu-id="fd678-214">**NaN**</span><span class="sxs-lookup"><span data-stu-id="fd678-214">**NaN**</span></span>            | <span data-ttu-id="fd678-215">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-215">NaN</span></span>      | <span data-ttu-id="fd678-216">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-216">NaN</span></span>    | <span data-ttu-id="fd678-217">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-217">NaN</span></span>      | <span data-ttu-id="fd678-218">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-218">NaN</span></span>    | <span data-ttu-id="fd678-219">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-219">NaN</span></span>    | <span data-ttu-id="fd678-220">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-220">NaN</span></span>      | <span data-ttu-id="fd678-221">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-221">NaN</span></span>    | <span data-ttu-id="fd678-222">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-222">NaN</span></span>      | <span data-ttu-id="fd678-223">NaN</span><span class="sxs-lookup"><span data-stu-id="fd678-223">NaN</span></span>     |



 

<span data-ttu-id="fd678-224">Questa istruzione si applica alle fasi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="fd678-224">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fd678-225">Vertice</span><span class="sxs-lookup"><span data-stu-id="fd678-225">Vertex</span></span> | <span data-ttu-id="fd678-226">Scafo</span><span class="sxs-lookup"><span data-stu-id="fd678-226">Hull</span></span> | <span data-ttu-id="fd678-227">Dominio</span><span class="sxs-lookup"><span data-stu-id="fd678-227">Domain</span></span> | <span data-ttu-id="fd678-228">Geometria</span><span class="sxs-lookup"><span data-stu-id="fd678-228">Geometry</span></span> | <span data-ttu-id="fd678-229">Pixel</span><span class="sxs-lookup"><span data-stu-id="fd678-229">Pixel</span></span> | <span data-ttu-id="fd678-230">Calcolo</span><span class="sxs-lookup"><span data-stu-id="fd678-230">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fd678-231">X</span><span class="sxs-lookup"><span data-stu-id="fd678-231">X</span></span>      | <span data-ttu-id="fd678-232">X</span><span class="sxs-lookup"><span data-stu-id="fd678-232">X</span></span>    | <span data-ttu-id="fd678-233">X</span><span class="sxs-lookup"><span data-stu-id="fd678-233">X</span></span>      | <span data-ttu-id="fd678-234">X</span><span class="sxs-lookup"><span data-stu-id="fd678-234">X</span></span>        | <span data-ttu-id="fd678-235">X</span><span class="sxs-lookup"><span data-stu-id="fd678-235">X</span></span>     | <span data-ttu-id="fd678-236">X</span><span class="sxs-lookup"><span data-stu-id="fd678-236">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fd678-237">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="fd678-237">Minimum Shader Model</span></span>

<span data-ttu-id="fd678-238">Questa istruzione è supportata nei modelli di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="fd678-238">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="fd678-239">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="fd678-239">Shader Model</span></span>                                              | <span data-ttu-id="fd678-240">Supportato</span><span class="sxs-lookup"><span data-stu-id="fd678-240">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fd678-241">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="fd678-241">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fd678-242">sì</span><span class="sxs-lookup"><span data-stu-id="fd678-242">yes</span></span>       |
| [<span data-ttu-id="fd678-243">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="fd678-243">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fd678-244">no</span><span class="sxs-lookup"><span data-stu-id="fd678-244">no</span></span>        |
| [<span data-ttu-id="fd678-245">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="fd678-245">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fd678-246">no</span><span class="sxs-lookup"><span data-stu-id="fd678-246">no</span></span>        |
| [<span data-ttu-id="fd678-247">Modello shader 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd678-247">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fd678-248">no</span><span class="sxs-lookup"><span data-stu-id="fd678-248">no</span></span>        |
| [<span data-ttu-id="fd678-249">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd678-249">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fd678-250">no</span><span class="sxs-lookup"><span data-stu-id="fd678-250">no</span></span>        |
| [<span data-ttu-id="fd678-251">Modello shader 1 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="fd678-251">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fd678-252">no</span><span class="sxs-lookup"><span data-stu-id="fd678-252">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fd678-253">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fd678-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd678-254">Assembly del modello shader 5 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="fd678-254">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





