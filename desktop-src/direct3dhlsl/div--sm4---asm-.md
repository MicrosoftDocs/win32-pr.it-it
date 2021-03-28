---
title: div (SM4-ASM)
description: Divisione a livello di componente.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 332d494adc2cc9bebe2e714b47ff2c5a6b299966
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046080"
---
# <a name="div-sm4---asm"></a><span data-ttu-id="8fddd-103">div (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8fddd-103">div (sm4 - asm)</span></span>

<span data-ttu-id="8fddd-104">Divisione a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="8fddd-104">Component-wise divide.</span></span>



| <span data-ttu-id="8fddd-105">div \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="8fddd-105">div\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="8fddd-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="8fddd-106">Item</span></span>                                                            | <span data-ttu-id="8fddd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fddd-107">Description</span></span>                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="8fddd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="8fddd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="8fddd-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8fddd-109">\[in\] The result of the operation.</span></span><br/> |
| <span data-ttu-id="8fddd-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8fddd-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="8fddd-111">\[nel \] dividendo.</span><span class="sxs-lookup"><span data-stu-id="8fddd-111">\[in\] The dividend.</span></span><br/>                |
| <span data-ttu-id="8fddd-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="8fddd-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="8fddd-113">\[nel \] divisore.</span><span class="sxs-lookup"><span data-stu-id="8fddd-113">\[in\] The divisor.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="8fddd-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fddd-114">Remarks</span></span>

<span data-ttu-id="8fddd-115">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="8fddd-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="8fddd-116">Si notino le due implementazioni consentite di divide: a/b e a \* (1/b).</span><span class="sxs-lookup"><span data-stu-id="8fddd-116">You should note the two allowed implementations of divide: a/b and a\*(1/b).</span></span>

<span data-ttu-id="8fddd-117">Un risultato è che sono presenti eccezioni alla tabella seguente per i valori del denominatore di grandi dimensioni (maggiore di 8.5070592 e + 37), dove 1/denominatore è una denorma.</span><span class="sxs-lookup"><span data-stu-id="8fddd-117">One outcome of this is that there are exceptions to the table below for large denominator values (greater than 8.5070592e+37), where 1/denominator is a denorm.</span></span> <span data-ttu-id="8fddd-118">Poiché le implementazioni possono eseguire la divisione come \* (1/b), anziché a/b direttamente e 1/ \[ grande valore \] è una denorma che può essere scaricata, alcuni casi nella tabella produrrebbe risultati diversi.</span><span class="sxs-lookup"><span data-stu-id="8fddd-118">Because implementations may perform divide as a\*(1/b), instead of a/b directly, and 1/\[large value\] is a denorm that could get flushed, some cases in the table would produce different results.</span></span> <span data-ttu-id="8fddd-119">Ad esempio, il valore (+/-) INF/(+/-) \[ > 8.5070592 e + 37 \] può produrre Nan in alcune implementazioni, ma (+/-) inf in altre implementazioni</span><span class="sxs-lookup"><span data-stu-id="8fddd-119">For example, (+/-)INF / (+/-)\[value > 8.5070592e+37\] may produce NaN on some implementations, but (+/-)INF on other implementations</span></span>

<span data-ttu-id="8fddd-120">In questa tabella F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="8fddd-120">In this table F means finite-real number.</span></span>



|                     |          |            |             |        |        |             |            |          |         |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="8fddd-121">**src1 src0->**</span><span class="sxs-lookup"><span data-stu-id="8fddd-121">**src0 src1 ->**</span></span> | <span data-ttu-id="8fddd-122">**-INF**</span><span class="sxs-lookup"><span data-stu-id="8fddd-122">**-inf**</span></span> | <span data-ttu-id="8fddd-123">**-F**</span><span class="sxs-lookup"><span data-stu-id="8fddd-123">**-F**</span></span>     | <span data-ttu-id="8fddd-124">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="8fddd-124">**-denorm**</span></span> | <span data-ttu-id="8fddd-125">**-0**</span><span class="sxs-lookup"><span data-stu-id="8fddd-125">**-0**</span></span> | <span data-ttu-id="8fddd-126">**+0**</span><span class="sxs-lookup"><span data-stu-id="8fddd-126">**+0**</span></span> | <span data-ttu-id="8fddd-127">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="8fddd-127">**+denorm**</span></span> | <span data-ttu-id="8fddd-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="8fddd-128">**+F**</span></span>     | <span data-ttu-id="8fddd-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="8fddd-129">**+inf**</span></span> | <span data-ttu-id="8fddd-130">**Nan**</span><span class="sxs-lookup"><span data-stu-id="8fddd-130">**Nan**</span></span> |
| <span data-ttu-id="8fddd-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="8fddd-131">**-inf**</span></span>            | <span data-ttu-id="8fddd-132">-inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-132">-inf</span></span>     | <span data-ttu-id="8fddd-133">-inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-133">-inf</span></span>       | <span data-ttu-id="8fddd-134">-inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-134">-inf</span></span>        | <span data-ttu-id="8fddd-135">-inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-135">-inf</span></span>   | <span data-ttu-id="8fddd-136">-inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-136">-inf</span></span>   | <span data-ttu-id="8fddd-137">-inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-137">-inf</span></span>        | <span data-ttu-id="8fddd-138">-inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-138">-inf</span></span>       | <span data-ttu-id="8fddd-139">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-139">NaN</span></span>      | <span data-ttu-id="8fddd-140">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-140">NaN</span></span>     |
| <span data-ttu-id="8fddd-141">**-F**</span><span class="sxs-lookup"><span data-stu-id="8fddd-141">**-F**</span></span>              | <span data-ttu-id="8fddd-142">-inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-142">-inf</span></span>     | <span data-ttu-id="8fddd-143">-F</span><span class="sxs-lookup"><span data-stu-id="8fddd-143">-F</span></span>         | <span data-ttu-id="8fddd-144">src0</span><span class="sxs-lookup"><span data-stu-id="8fddd-144">src0</span></span>        | <span data-ttu-id="8fddd-145">src0</span><span class="sxs-lookup"><span data-stu-id="8fddd-145">src0</span></span>   | <span data-ttu-id="8fddd-146">src0</span><span class="sxs-lookup"><span data-stu-id="8fddd-146">src0</span></span>   | <span data-ttu-id="8fddd-147">src0</span><span class="sxs-lookup"><span data-stu-id="8fddd-147">src0</span></span>        | <span data-ttu-id="8fddd-148">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="8fddd-148">+-F or +-0</span></span> | <span data-ttu-id="8fddd-149">+inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-149">+inf</span></span>     | <span data-ttu-id="8fddd-150">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-150">NaN</span></span>     |
| <span data-ttu-id="8fddd-151">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="8fddd-151">**-denorm**</span></span>         | <span data-ttu-id="8fddd-152">-inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-152">-inf</span></span>     | <span data-ttu-id="8fddd-153">src1</span><span class="sxs-lookup"><span data-stu-id="8fddd-153">src1</span></span>       | <span data-ttu-id="8fddd-154">-0</span><span class="sxs-lookup"><span data-stu-id="8fddd-154">-0</span></span>          | <span data-ttu-id="8fddd-155">-0</span><span class="sxs-lookup"><span data-stu-id="8fddd-155">-0</span></span>     | <span data-ttu-id="8fddd-156">+0</span><span class="sxs-lookup"><span data-stu-id="8fddd-156">+0</span></span>     | <span data-ttu-id="8fddd-157">+0</span><span class="sxs-lookup"><span data-stu-id="8fddd-157">+0</span></span>          | <span data-ttu-id="8fddd-158">src1</span><span class="sxs-lookup"><span data-stu-id="8fddd-158">src1</span></span>       | <span data-ttu-id="8fddd-159">+inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-159">+inf</span></span>     | <span data-ttu-id="8fddd-160">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-160">NaN</span></span>     |
| <span data-ttu-id="8fddd-161">**-0**</span><span class="sxs-lookup"><span data-stu-id="8fddd-161">**-0**</span></span>              | <span data-ttu-id="8fddd-162">-inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-162">-inf</span></span>     | <span data-ttu-id="8fddd-163">src1</span><span class="sxs-lookup"><span data-stu-id="8fddd-163">src1</span></span>       | <span data-ttu-id="8fddd-164">-0</span><span class="sxs-lookup"><span data-stu-id="8fddd-164">-0</span></span>          | <span data-ttu-id="8fddd-165">-0</span><span class="sxs-lookup"><span data-stu-id="8fddd-165">-0</span></span>     | <span data-ttu-id="8fddd-166">+0</span><span class="sxs-lookup"><span data-stu-id="8fddd-166">+0</span></span>     | <span data-ttu-id="8fddd-167">+0</span><span class="sxs-lookup"><span data-stu-id="8fddd-167">+0</span></span>          | <span data-ttu-id="8fddd-168">src1</span><span class="sxs-lookup"><span data-stu-id="8fddd-168">src1</span></span>       | <span data-ttu-id="8fddd-169">+inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-169">+inf</span></span>     | <span data-ttu-id="8fddd-170">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-170">NaN</span></span>     |
| <span data-ttu-id="8fddd-171">**+0**</span><span class="sxs-lookup"><span data-stu-id="8fddd-171">**+0**</span></span>              | <span data-ttu-id="8fddd-172">-inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-172">-inf</span></span>     | <span data-ttu-id="8fddd-173">src1</span><span class="sxs-lookup"><span data-stu-id="8fddd-173">src1</span></span>       | <span data-ttu-id="8fddd-174">+0</span><span class="sxs-lookup"><span data-stu-id="8fddd-174">+0</span></span>          | <span data-ttu-id="8fddd-175">+0</span><span class="sxs-lookup"><span data-stu-id="8fddd-175">+0</span></span>     | <span data-ttu-id="8fddd-176">+0</span><span class="sxs-lookup"><span data-stu-id="8fddd-176">+0</span></span>     | <span data-ttu-id="8fddd-177">+0</span><span class="sxs-lookup"><span data-stu-id="8fddd-177">+0</span></span>          | <span data-ttu-id="8fddd-178">src1</span><span class="sxs-lookup"><span data-stu-id="8fddd-178">src1</span></span>       | <span data-ttu-id="8fddd-179">+inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-179">+inf</span></span>     | <span data-ttu-id="8fddd-180">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-180">NaN</span></span>     |
| <span data-ttu-id="8fddd-181">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="8fddd-181">**+denorm**</span></span>         | <span data-ttu-id="8fddd-182">-inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-182">-inf</span></span>     | <span data-ttu-id="8fddd-183">src1</span><span class="sxs-lookup"><span data-stu-id="8fddd-183">src1</span></span>       | <span data-ttu-id="8fddd-184">+0</span><span class="sxs-lookup"><span data-stu-id="8fddd-184">+0</span></span>          | <span data-ttu-id="8fddd-185">+0</span><span class="sxs-lookup"><span data-stu-id="8fddd-185">+0</span></span>     | <span data-ttu-id="8fddd-186">+0</span><span class="sxs-lookup"><span data-stu-id="8fddd-186">+0</span></span>     | <span data-ttu-id="8fddd-187">+0</span><span class="sxs-lookup"><span data-stu-id="8fddd-187">+0</span></span>          | <span data-ttu-id="8fddd-188">src1</span><span class="sxs-lookup"><span data-stu-id="8fddd-188">src1</span></span>       | <span data-ttu-id="8fddd-189">+inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-189">+inf</span></span>     | <span data-ttu-id="8fddd-190">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-190">NaN</span></span>     |
| <span data-ttu-id="8fddd-191">**+ F**</span><span class="sxs-lookup"><span data-stu-id="8fddd-191">**+F**</span></span>              | <span data-ttu-id="8fddd-192">-inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-192">-inf</span></span>     | <span data-ttu-id="8fddd-193">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="8fddd-193">+-F or +-0</span></span> | <span data-ttu-id="8fddd-194">src0</span><span class="sxs-lookup"><span data-stu-id="8fddd-194">src0</span></span>        | <span data-ttu-id="8fddd-195">src0</span><span class="sxs-lookup"><span data-stu-id="8fddd-195">src0</span></span>   | <span data-ttu-id="8fddd-196">src0</span><span class="sxs-lookup"><span data-stu-id="8fddd-196">src0</span></span>   | <span data-ttu-id="8fddd-197">src0</span><span class="sxs-lookup"><span data-stu-id="8fddd-197">src0</span></span>        | <span data-ttu-id="8fddd-198">+ F</span><span class="sxs-lookup"><span data-stu-id="8fddd-198">+F</span></span>         | <span data-ttu-id="8fddd-199">+inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-199">+inf</span></span>     | <span data-ttu-id="8fddd-200">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-200">NaN</span></span>     |
| <span data-ttu-id="8fddd-201">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="8fddd-201">**+inf**</span></span>            | <span data-ttu-id="8fddd-202">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-202">NaN</span></span>      | <span data-ttu-id="8fddd-203">+inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-203">+inf</span></span>       | <span data-ttu-id="8fddd-204">+inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-204">+inf</span></span>        | <span data-ttu-id="8fddd-205">+inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-205">+inf</span></span>   | <span data-ttu-id="8fddd-206">+inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-206">+inf</span></span>   | <span data-ttu-id="8fddd-207">+inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-207">+inf</span></span>        | <span data-ttu-id="8fddd-208">+inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-208">+inf</span></span>       | <span data-ttu-id="8fddd-209">+inf</span><span class="sxs-lookup"><span data-stu-id="8fddd-209">+inf</span></span>     | <span data-ttu-id="8fddd-210">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-210">NaN</span></span>     |
| <span data-ttu-id="8fddd-211">**NaN**</span><span class="sxs-lookup"><span data-stu-id="8fddd-211">**NaN**</span></span>             | <span data-ttu-id="8fddd-212">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-212">NaN</span></span>      | <span data-ttu-id="8fddd-213">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-213">NaN</span></span>        | <span data-ttu-id="8fddd-214">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-214">NaN</span></span>         | <span data-ttu-id="8fddd-215">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-215">NaN</span></span>    | <span data-ttu-id="8fddd-216">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-216">NaN</span></span>    | <span data-ttu-id="8fddd-217">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-217">NaN</span></span>         | <span data-ttu-id="8fddd-218">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-218">NaN</span></span>        | <span data-ttu-id="8fddd-219">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-219">NaN</span></span>      | <span data-ttu-id="8fddd-220">NaN</span><span class="sxs-lookup"><span data-stu-id="8fddd-220">NaN</span></span>     |



 

<span data-ttu-id="8fddd-221">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="8fddd-221">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8fddd-222">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="8fddd-222">Vertex Shader</span></span> | <span data-ttu-id="8fddd-223">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="8fddd-223">Geometry Shader</span></span> | <span data-ttu-id="8fddd-224">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="8fddd-224">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8fddd-225">x</span><span class="sxs-lookup"><span data-stu-id="8fddd-225">x</span></span>             | <span data-ttu-id="8fddd-226">x</span><span class="sxs-lookup"><span data-stu-id="8fddd-226">x</span></span>               | <span data-ttu-id="8fddd-227">x</span><span class="sxs-lookup"><span data-stu-id="8fddd-227">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8fddd-228">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="8fddd-228">Minimum Shader Model</span></span>

<span data-ttu-id="8fddd-229">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="8fddd-229">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8fddd-230">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="8fddd-230">Shader Model</span></span>                                              | <span data-ttu-id="8fddd-231">Supportato</span><span class="sxs-lookup"><span data-stu-id="8fddd-231">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8fddd-232">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="8fddd-232">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8fddd-233">sì</span><span class="sxs-lookup"><span data-stu-id="8fddd-233">yes</span></span>       |
| [<span data-ttu-id="8fddd-234">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="8fddd-234">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8fddd-235">sì</span><span class="sxs-lookup"><span data-stu-id="8fddd-235">yes</span></span>       |
| [<span data-ttu-id="8fddd-236">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="8fddd-236">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8fddd-237">sì</span><span class="sxs-lookup"><span data-stu-id="8fddd-237">yes</span></span>       |
| [<span data-ttu-id="8fddd-238">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8fddd-238">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8fddd-239">no</span><span class="sxs-lookup"><span data-stu-id="8fddd-239">no</span></span>        |
| [<span data-ttu-id="8fddd-240">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8fddd-240">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8fddd-241">no</span><span class="sxs-lookup"><span data-stu-id="8fddd-241">no</span></span>        |
| [<span data-ttu-id="8fddd-242">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8fddd-242">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8fddd-243">no</span><span class="sxs-lookup"><span data-stu-id="8fddd-243">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8fddd-244">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8fddd-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fddd-245">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8fddd-245">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





