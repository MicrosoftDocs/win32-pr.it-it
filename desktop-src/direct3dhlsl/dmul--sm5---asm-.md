---
title: dmul (SM5-ASM)
description: Moltiplicazione a precisione doppia per componente.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18cce59ae237610b1038d90e02dff429812b4f00
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993053"
---
# <a name="dmul-sm5---asm"></a><span data-ttu-id="2a050-103">dmul (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2a050-103">dmul (sm5 - asm)</span></span>

<span data-ttu-id="2a050-104">Moltiplicazione a precisione doppia per componente.</span><span class="sxs-lookup"><span data-stu-id="2a050-104">Component-wise double-precision multiply.</span></span>



| <span data-ttu-id="2a050-105">dmul \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2a050-105">dmul\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2a050-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="2a050-106">Item</span></span>                                                            | <span data-ttu-id="2a050-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a050-107">Description</span></span>                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a050-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2a050-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2a050-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2a050-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="2a050-110">*dest*  =  *src0* \* *src1*</span><span class="sxs-lookup"><span data-stu-id="2a050-110">*dest* = *src0* \* *src1*</span></span><br/> |
| <span data-ttu-id="2a050-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2a050-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2a050-112">\[nei \] componenti da moltiplicare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="2a050-112">\[in\] The components to multiply with *src1*.</span></span><br/>                                          |
| <span data-ttu-id="2a050-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="2a050-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="2a050-114">\[nei \] componenti da moltiplicare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="2a050-114">\[in\] The components to multiply with *src0*.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="2a050-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a050-115">Remarks</span></span>

<span data-ttu-id="2a050-116">I swizzles validi per i parametri di origine sono xyzw, Xyxy, zwxy, zwzw.</span><span class="sxs-lookup"><span data-stu-id="2a050-116">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="2a050-117">Le maschere *dest* valide sono. XY,. ZW e. xyzw.</span><span class="sxs-lookup"><span data-stu-id="2a050-117">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="2a050-118">I mapping *src* seguenti sono post-swizzle:</span><span class="sxs-lookup"><span data-stu-id="2a050-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="2a050-119">*dest* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="2a050-119">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="2a050-120">*src0* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="2a050-120">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="2a050-121">*src1* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="2a050-121">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="2a050-122">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="2a050-122">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="2a050-123">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="2a050-123">F means finite-real number.</span></span>



|                    |          |        |          |        |        |          |        |          |         |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="2a050-124">**src1 src0->**</span><span class="sxs-lookup"><span data-stu-id="2a050-124">**src0 src1->**</span></span> | <span data-ttu-id="2a050-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="2a050-125">**-inf**</span></span> | <span data-ttu-id="2a050-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="2a050-126">**-F**</span></span> | <span data-ttu-id="2a050-127">**-1,0**</span><span class="sxs-lookup"><span data-stu-id="2a050-127">**-1.0**</span></span> | <span data-ttu-id="2a050-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="2a050-128">**-0**</span></span> | <span data-ttu-id="2a050-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="2a050-129">**+0**</span></span> | <span data-ttu-id="2a050-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="2a050-130">**+1.0**</span></span> | <span data-ttu-id="2a050-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="2a050-131">**+F**</span></span> | <span data-ttu-id="2a050-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="2a050-132">**+inf**</span></span> | <span data-ttu-id="2a050-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="2a050-133">**NaN**</span></span> |
| <span data-ttu-id="2a050-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="2a050-134">**-inf**</span></span>           | <span data-ttu-id="2a050-135">+inf</span><span class="sxs-lookup"><span data-stu-id="2a050-135">+inf</span></span>     | <span data-ttu-id="2a050-136">+inf</span><span class="sxs-lookup"><span data-stu-id="2a050-136">+inf</span></span>   | <span data-ttu-id="2a050-137">+inf</span><span class="sxs-lookup"><span data-stu-id="2a050-137">+inf</span></span>     | <span data-ttu-id="2a050-138">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-138">NaN</span></span>    | <span data-ttu-id="2a050-139">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-139">NaN</span></span>    | <span data-ttu-id="2a050-140">-inf</span><span class="sxs-lookup"><span data-stu-id="2a050-140">-inf</span></span>     | <span data-ttu-id="2a050-141">-inf</span><span class="sxs-lookup"><span data-stu-id="2a050-141">-inf</span></span>   | <span data-ttu-id="2a050-142">-inf</span><span class="sxs-lookup"><span data-stu-id="2a050-142">-inf</span></span>     | <span data-ttu-id="2a050-143">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-143">NaN</span></span>     |
| <span data-ttu-id="2a050-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="2a050-144">**-F**</span></span>             | <span data-ttu-id="2a050-145">+inf</span><span class="sxs-lookup"><span data-stu-id="2a050-145">+inf</span></span>     | <span data-ttu-id="2a050-146">+ F</span><span class="sxs-lookup"><span data-stu-id="2a050-146">+F</span></span>     | <span data-ttu-id="2a050-147">-src0</span><span class="sxs-lookup"><span data-stu-id="2a050-147">-src0</span></span>    | <span data-ttu-id="2a050-148">+0</span><span class="sxs-lookup"><span data-stu-id="2a050-148">+0</span></span>     | <span data-ttu-id="2a050-149">-0</span><span class="sxs-lookup"><span data-stu-id="2a050-149">-0</span></span>     | <span data-ttu-id="2a050-150">src0</span><span class="sxs-lookup"><span data-stu-id="2a050-150">src0</span></span>     | <span data-ttu-id="2a050-151">-F</span><span class="sxs-lookup"><span data-stu-id="2a050-151">-F</span></span>     | <span data-ttu-id="2a050-152">-inf</span><span class="sxs-lookup"><span data-stu-id="2a050-152">-inf</span></span>     | <span data-ttu-id="2a050-153">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-153">NaN</span></span>     |
| <span data-ttu-id="2a050-154">**-1.0 f**</span><span class="sxs-lookup"><span data-stu-id="2a050-154">**-1.0F**</span></span>          | <span data-ttu-id="2a050-155">+inf</span><span class="sxs-lookup"><span data-stu-id="2a050-155">+inf</span></span>     | <span data-ttu-id="2a050-156">-src1</span><span class="sxs-lookup"><span data-stu-id="2a050-156">-src1</span></span>  | <span data-ttu-id="2a050-157">+ 1,0</span><span class="sxs-lookup"><span data-stu-id="2a050-157">+1.0</span></span>     | <span data-ttu-id="2a050-158">+0</span><span class="sxs-lookup"><span data-stu-id="2a050-158">+0</span></span>     | <span data-ttu-id="2a050-159">-0</span><span class="sxs-lookup"><span data-stu-id="2a050-159">-0</span></span>     | <span data-ttu-id="2a050-160">-1.0</span><span class="sxs-lookup"><span data-stu-id="2a050-160">-1.0</span></span>     | <span data-ttu-id="2a050-161">-src1</span><span class="sxs-lookup"><span data-stu-id="2a050-161">-src1</span></span>  | <span data-ttu-id="2a050-162">-inf</span><span class="sxs-lookup"><span data-stu-id="2a050-162">-inf</span></span>     | <span data-ttu-id="2a050-163">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-163">NaN</span></span>     |
| <span data-ttu-id="2a050-164">**-0**</span><span class="sxs-lookup"><span data-stu-id="2a050-164">**-0**</span></span>             | <span data-ttu-id="2a050-165">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-165">NaN</span></span>      | <span data-ttu-id="2a050-166">+0</span><span class="sxs-lookup"><span data-stu-id="2a050-166">+0</span></span>     | <span data-ttu-id="2a050-167">+0</span><span class="sxs-lookup"><span data-stu-id="2a050-167">+0</span></span>       | <span data-ttu-id="2a050-168">+0</span><span class="sxs-lookup"><span data-stu-id="2a050-168">+0</span></span>     | <span data-ttu-id="2a050-169">-0</span><span class="sxs-lookup"><span data-stu-id="2a050-169">-0</span></span>     | <span data-ttu-id="2a050-170">-0</span><span class="sxs-lookup"><span data-stu-id="2a050-170">-0</span></span>       | <span data-ttu-id="2a050-171">-0</span><span class="sxs-lookup"><span data-stu-id="2a050-171">-0</span></span>     | <span data-ttu-id="2a050-172">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-172">NaN</span></span>      | <span data-ttu-id="2a050-173">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-173">NaN</span></span>     |
| <span data-ttu-id="2a050-174">**+0**</span><span class="sxs-lookup"><span data-stu-id="2a050-174">**+0**</span></span>             | <span data-ttu-id="2a050-175">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-175">NaN</span></span>      | <span data-ttu-id="2a050-176">-0</span><span class="sxs-lookup"><span data-stu-id="2a050-176">-0</span></span>     | <span data-ttu-id="2a050-177">-0</span><span class="sxs-lookup"><span data-stu-id="2a050-177">-0</span></span>       | <span data-ttu-id="2a050-178">-0</span><span class="sxs-lookup"><span data-stu-id="2a050-178">-0</span></span>     | <span data-ttu-id="2a050-179">+0</span><span class="sxs-lookup"><span data-stu-id="2a050-179">+0</span></span>     | <span data-ttu-id="2a050-180">+0</span><span class="sxs-lookup"><span data-stu-id="2a050-180">+0</span></span>       | <span data-ttu-id="2a050-181">+0</span><span class="sxs-lookup"><span data-stu-id="2a050-181">+0</span></span>     | <span data-ttu-id="2a050-182">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-182">NaN</span></span>      | <span data-ttu-id="2a050-183">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-183">NaN</span></span>     |
| <span data-ttu-id="2a050-184">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="2a050-184">**+1.0**</span></span>           | <span data-ttu-id="2a050-185">-inf</span><span class="sxs-lookup"><span data-stu-id="2a050-185">-inf</span></span>     | <span data-ttu-id="2a050-186">src1</span><span class="sxs-lookup"><span data-stu-id="2a050-186">src1</span></span>   | <span data-ttu-id="2a050-187">-1.0</span><span class="sxs-lookup"><span data-stu-id="2a050-187">-1.0</span></span>     | <span data-ttu-id="2a050-188">-0</span><span class="sxs-lookup"><span data-stu-id="2a050-188">-0</span></span>     | <span data-ttu-id="2a050-189">+0</span><span class="sxs-lookup"><span data-stu-id="2a050-189">+0</span></span>     | <span data-ttu-id="2a050-190">+1</span><span class="sxs-lookup"><span data-stu-id="2a050-190">+1</span></span>       | <span data-ttu-id="2a050-191">src1</span><span class="sxs-lookup"><span data-stu-id="2a050-191">src1</span></span>   | <span data-ttu-id="2a050-192">+inf</span><span class="sxs-lookup"><span data-stu-id="2a050-192">+inf</span></span>     | <span data-ttu-id="2a050-193">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-193">NaN</span></span>     |
| <span data-ttu-id="2a050-194">**+ F**</span><span class="sxs-lookup"><span data-stu-id="2a050-194">**+F**</span></span>             | <span data-ttu-id="2a050-195">-inf</span><span class="sxs-lookup"><span data-stu-id="2a050-195">-inf</span></span>     | <span data-ttu-id="2a050-196">-F</span><span class="sxs-lookup"><span data-stu-id="2a050-196">-F</span></span>     | <span data-ttu-id="2a050-197">-src0</span><span class="sxs-lookup"><span data-stu-id="2a050-197">-src0</span></span>    | <span data-ttu-id="2a050-198">-0</span><span class="sxs-lookup"><span data-stu-id="2a050-198">-0</span></span>     | <span data-ttu-id="2a050-199">+0</span><span class="sxs-lookup"><span data-stu-id="2a050-199">+0</span></span>     | <span data-ttu-id="2a050-200">src0</span><span class="sxs-lookup"><span data-stu-id="2a050-200">src0</span></span>     | <span data-ttu-id="2a050-201">+ F</span><span class="sxs-lookup"><span data-stu-id="2a050-201">+F</span></span>     | <span data-ttu-id="2a050-202">+inf</span><span class="sxs-lookup"><span data-stu-id="2a050-202">+inf</span></span>     | <span data-ttu-id="2a050-203">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-203">NaN</span></span>     |
| <span data-ttu-id="2a050-204">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="2a050-204">**+inf**</span></span>           | <span data-ttu-id="2a050-205">-inf</span><span class="sxs-lookup"><span data-stu-id="2a050-205">-inf</span></span>     | <span data-ttu-id="2a050-206">-inf</span><span class="sxs-lookup"><span data-stu-id="2a050-206">-inf</span></span>   | <span data-ttu-id="2a050-207">-inf</span><span class="sxs-lookup"><span data-stu-id="2a050-207">-inf</span></span>     | <span data-ttu-id="2a050-208">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-208">NaN</span></span>    | <span data-ttu-id="2a050-209">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-209">NaN</span></span>    | <span data-ttu-id="2a050-210">+inf</span><span class="sxs-lookup"><span data-stu-id="2a050-210">+inf</span></span>     | <span data-ttu-id="2a050-211">+inf</span><span class="sxs-lookup"><span data-stu-id="2a050-211">+inf</span></span>   | <span data-ttu-id="2a050-212">+inf</span><span class="sxs-lookup"><span data-stu-id="2a050-212">+inf</span></span>     | <span data-ttu-id="2a050-213">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-213">NaN</span></span>     |
| <span data-ttu-id="2a050-214">**NaN**</span><span class="sxs-lookup"><span data-stu-id="2a050-214">**NaN**</span></span>            | <span data-ttu-id="2a050-215">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-215">NaN</span></span>      | <span data-ttu-id="2a050-216">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-216">NaN</span></span>    | <span data-ttu-id="2a050-217">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-217">NaN</span></span>      | <span data-ttu-id="2a050-218">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-218">NaN</span></span>    | <span data-ttu-id="2a050-219">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-219">NaN</span></span>    | <span data-ttu-id="2a050-220">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-220">NaN</span></span>      | <span data-ttu-id="2a050-221">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-221">NaN</span></span>    | <span data-ttu-id="2a050-222">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-222">NaN</span></span>      | <span data-ttu-id="2a050-223">NaN</span><span class="sxs-lookup"><span data-stu-id="2a050-223">NaN</span></span>     |



 

<span data-ttu-id="2a050-224">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a050-224">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2a050-225">Vertice</span><span class="sxs-lookup"><span data-stu-id="2a050-225">Vertex</span></span> | <span data-ttu-id="2a050-226">Hull</span><span class="sxs-lookup"><span data-stu-id="2a050-226">Hull</span></span> | <span data-ttu-id="2a050-227">Dominio</span><span class="sxs-lookup"><span data-stu-id="2a050-227">Domain</span></span> | <span data-ttu-id="2a050-228">Geometria</span><span class="sxs-lookup"><span data-stu-id="2a050-228">Geometry</span></span> | <span data-ttu-id="2a050-229">Pixel</span><span class="sxs-lookup"><span data-stu-id="2a050-229">Pixel</span></span> | <span data-ttu-id="2a050-230">Calcolo</span><span class="sxs-lookup"><span data-stu-id="2a050-230">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2a050-231">X</span><span class="sxs-lookup"><span data-stu-id="2a050-231">X</span></span>      | <span data-ttu-id="2a050-232">X</span><span class="sxs-lookup"><span data-stu-id="2a050-232">X</span></span>    | <span data-ttu-id="2a050-233">X</span><span class="sxs-lookup"><span data-stu-id="2a050-233">X</span></span>      | <span data-ttu-id="2a050-234">X</span><span class="sxs-lookup"><span data-stu-id="2a050-234">X</span></span>        | <span data-ttu-id="2a050-235">X</span><span class="sxs-lookup"><span data-stu-id="2a050-235">X</span></span>     | <span data-ttu-id="2a050-236">X</span><span class="sxs-lookup"><span data-stu-id="2a050-236">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2a050-237">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="2a050-237">Minimum Shader Model</span></span>

<span data-ttu-id="2a050-238">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a050-238">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2a050-239">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2a050-239">Shader Model</span></span>                                              | <span data-ttu-id="2a050-240">Supportato</span><span class="sxs-lookup"><span data-stu-id="2a050-240">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2a050-241">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2a050-241">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2a050-242">sì</span><span class="sxs-lookup"><span data-stu-id="2a050-242">yes</span></span>       |
| [<span data-ttu-id="2a050-243">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="2a050-243">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2a050-244">no</span><span class="sxs-lookup"><span data-stu-id="2a050-244">no</span></span>        |
| [<span data-ttu-id="2a050-245">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="2a050-245">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2a050-246">no</span><span class="sxs-lookup"><span data-stu-id="2a050-246">no</span></span>        |
| [<span data-ttu-id="2a050-247">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a050-247">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2a050-248">no</span><span class="sxs-lookup"><span data-stu-id="2a050-248">no</span></span>        |
| [<span data-ttu-id="2a050-249">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a050-249">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2a050-250">no</span><span class="sxs-lookup"><span data-stu-id="2a050-250">no</span></span>        |
| [<span data-ttu-id="2a050-251">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a050-251">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2a050-252">no</span><span class="sxs-lookup"><span data-stu-id="2a050-252">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2a050-253">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a050-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a050-254">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a050-254">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





