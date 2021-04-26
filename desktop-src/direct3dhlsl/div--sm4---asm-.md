---
title: div (sm4 - asm)
description: Divisione per componente.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d406c5e61b4615990b445abe169619227d22124c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999098"
---
# <a name="div-sm4---asm"></a><span data-ttu-id="66ef8-103">div (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="66ef8-103">div (sm4 - asm)</span></span>

<span data-ttu-id="66ef8-104">Divisione per componente.</span><span class="sxs-lookup"><span data-stu-id="66ef8-104">Component-wise divide.</span></span>



| <span data-ttu-id="66ef8-105">div \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="66ef8-105">div\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="66ef8-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="66ef8-106">Item</span></span>                                                            | <span data-ttu-id="66ef8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66ef8-107">Description</span></span>                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="66ef8-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="66ef8-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="66ef8-109">\[in \] Risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="66ef8-109">\[in\] The result of the operation.</span></span><br/> |
| <span data-ttu-id="66ef8-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="66ef8-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="66ef8-111">\[in \] Dividendo.</span><span class="sxs-lookup"><span data-stu-id="66ef8-111">\[in\] The dividend.</span></span><br/>                |
| <span data-ttu-id="66ef8-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="66ef8-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="66ef8-113">\[in \] Divisore.</span><span class="sxs-lookup"><span data-stu-id="66ef8-113">\[in\] The divisor.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="66ef8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="66ef8-114">Remarks</span></span>

<span data-ttu-id="66ef8-115">Nella tabella seguente vengono illustrati i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichi alcun overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="66ef8-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="66ef8-116">Si notino le due implementazioni consentite di divide: a/b e \* a (1/b).</span><span class="sxs-lookup"><span data-stu-id="66ef8-116">You should note the two allowed implementations of divide: a/b and a\*(1/b).</span></span>

<span data-ttu-id="66ef8-117">Un risultato è che esistono eccezioni alla tabella seguente per valori denominatori di grandi dimensioni (maggiore di 8,5070592e+37), dove 1/denominatore è un nome.</span><span class="sxs-lookup"><span data-stu-id="66ef8-117">One outcome of this is that there are exceptions to the table below for large denominator values (greater than 8.5070592e+37), where 1/denominator is a denorm.</span></span> <span data-ttu-id="66ef8-118">Poiché le implementazioni possono eseguire la divisione come (1/b), invece di a/b direttamente e 1/b valore elevato è un denorm che potrebbe essere scaricato, alcuni casi nella tabella produrrebbe risultati \* \[ \] diversi.</span><span class="sxs-lookup"><span data-stu-id="66ef8-118">Because implementations may perform divide as a\*(1/b), instead of a/b directly, and 1/\[large value\] is a denorm that could get flushed, some cases in the table would produce different results.</span></span> <span data-ttu-id="66ef8-119">Ad esempio, il valore (+/-)INF/ (+/-) \[ > 8,5070592e+37 può produrre NaN in alcune implementazioni, ma \] (+/-) in altre implementazioni</span><span class="sxs-lookup"><span data-stu-id="66ef8-119">For example, (+/-)INF / (+/-)\[value > 8.5070592e+37\] may produce NaN on some implementations, but (+/-)INF on other implementations</span></span>

<span data-ttu-id="66ef8-120">In questa tabella F indica un numero finito-reale.</span><span class="sxs-lookup"><span data-stu-id="66ef8-120">In this table F means finite-real number.</span></span>



| <span data-ttu-id="66ef8-121">**src0 src1 ->**</span><span class="sxs-lookup"><span data-stu-id="66ef8-121">**src0 src1 ->**</span></span> | <span data-ttu-id="66ef8-122">**-inf**</span><span class="sxs-lookup"><span data-stu-id="66ef8-122">**-inf**</span></span> | <span data-ttu-id="66ef8-123">**-F**</span><span class="sxs-lookup"><span data-stu-id="66ef8-123">**-F**</span></span>     | <span data-ttu-id="66ef8-124">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="66ef8-124">**-denorm**</span></span> | <span data-ttu-id="66ef8-125">**-0**</span><span class="sxs-lookup"><span data-stu-id="66ef8-125">**-0**</span></span> | <span data-ttu-id="66ef8-126">**+0**</span><span class="sxs-lookup"><span data-stu-id="66ef8-126">**+0**</span></span> | <span data-ttu-id="66ef8-127">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="66ef8-127">**+denorm**</span></span> | <span data-ttu-id="66ef8-128">**+F**</span><span class="sxs-lookup"><span data-stu-id="66ef8-128">**+F**</span></span>     | <span data-ttu-id="66ef8-129">**+inf**</span><span class="sxs-lookup"><span data-stu-id="66ef8-129">**+inf**</span></span> | <span data-ttu-id="66ef8-130">**Nan**</span><span class="sxs-lookup"><span data-stu-id="66ef8-130">**Nan**</span></span> |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="66ef8-131">**-inf**</span><span class="sxs-lookup"><span data-stu-id="66ef8-131">**-inf**</span></span>            | <span data-ttu-id="66ef8-132">-inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-132">-inf</span></span>     | <span data-ttu-id="66ef8-133">-inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-133">-inf</span></span>       | <span data-ttu-id="66ef8-134">-inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-134">-inf</span></span>        | <span data-ttu-id="66ef8-135">-inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-135">-inf</span></span>   | <span data-ttu-id="66ef8-136">-inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-136">-inf</span></span>   | <span data-ttu-id="66ef8-137">-inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-137">-inf</span></span>        | <span data-ttu-id="66ef8-138">-inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-138">-inf</span></span>       | <span data-ttu-id="66ef8-139">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-139">NaN</span></span>      | <span data-ttu-id="66ef8-140">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-140">NaN</span></span>     |
| <span data-ttu-id="66ef8-141">**-F**</span><span class="sxs-lookup"><span data-stu-id="66ef8-141">**-F**</span></span>              | <span data-ttu-id="66ef8-142">-inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-142">-inf</span></span>     | <span data-ttu-id="66ef8-143">-F</span><span class="sxs-lookup"><span data-stu-id="66ef8-143">-F</span></span>         | <span data-ttu-id="66ef8-144">src0</span><span class="sxs-lookup"><span data-stu-id="66ef8-144">src0</span></span>        | <span data-ttu-id="66ef8-145">src0</span><span class="sxs-lookup"><span data-stu-id="66ef8-145">src0</span></span>   | <span data-ttu-id="66ef8-146">src0</span><span class="sxs-lookup"><span data-stu-id="66ef8-146">src0</span></span>   | <span data-ttu-id="66ef8-147">src0</span><span class="sxs-lookup"><span data-stu-id="66ef8-147">src0</span></span>        | <span data-ttu-id="66ef8-148">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="66ef8-148">+-F or +-0</span></span> | <span data-ttu-id="66ef8-149">+inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-149">+inf</span></span>     | <span data-ttu-id="66ef8-150">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-150">NaN</span></span>     |
| <span data-ttu-id="66ef8-151">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="66ef8-151">**-denorm**</span></span>         | <span data-ttu-id="66ef8-152">-inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-152">-inf</span></span>     | <span data-ttu-id="66ef8-153">src1</span><span class="sxs-lookup"><span data-stu-id="66ef8-153">src1</span></span>       | <span data-ttu-id="66ef8-154">-0</span><span class="sxs-lookup"><span data-stu-id="66ef8-154">-0</span></span>          | <span data-ttu-id="66ef8-155">-0</span><span class="sxs-lookup"><span data-stu-id="66ef8-155">-0</span></span>     | <span data-ttu-id="66ef8-156">+0</span><span class="sxs-lookup"><span data-stu-id="66ef8-156">+0</span></span>     | <span data-ttu-id="66ef8-157">+0</span><span class="sxs-lookup"><span data-stu-id="66ef8-157">+0</span></span>          | <span data-ttu-id="66ef8-158">src1</span><span class="sxs-lookup"><span data-stu-id="66ef8-158">src1</span></span>       | <span data-ttu-id="66ef8-159">+inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-159">+inf</span></span>     | <span data-ttu-id="66ef8-160">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-160">NaN</span></span>     |
| <span data-ttu-id="66ef8-161">**-0**</span><span class="sxs-lookup"><span data-stu-id="66ef8-161">**-0**</span></span>              | <span data-ttu-id="66ef8-162">-inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-162">-inf</span></span>     | <span data-ttu-id="66ef8-163">src1</span><span class="sxs-lookup"><span data-stu-id="66ef8-163">src1</span></span>       | <span data-ttu-id="66ef8-164">-0</span><span class="sxs-lookup"><span data-stu-id="66ef8-164">-0</span></span>          | <span data-ttu-id="66ef8-165">-0</span><span class="sxs-lookup"><span data-stu-id="66ef8-165">-0</span></span>     | <span data-ttu-id="66ef8-166">+0</span><span class="sxs-lookup"><span data-stu-id="66ef8-166">+0</span></span>     | <span data-ttu-id="66ef8-167">+0</span><span class="sxs-lookup"><span data-stu-id="66ef8-167">+0</span></span>          | <span data-ttu-id="66ef8-168">src1</span><span class="sxs-lookup"><span data-stu-id="66ef8-168">src1</span></span>       | <span data-ttu-id="66ef8-169">+inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-169">+inf</span></span>     | <span data-ttu-id="66ef8-170">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-170">NaN</span></span>     |
| <span data-ttu-id="66ef8-171">**+0**</span><span class="sxs-lookup"><span data-stu-id="66ef8-171">**+0**</span></span>              | <span data-ttu-id="66ef8-172">-inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-172">-inf</span></span>     | <span data-ttu-id="66ef8-173">src1</span><span class="sxs-lookup"><span data-stu-id="66ef8-173">src1</span></span>       | <span data-ttu-id="66ef8-174">+0</span><span class="sxs-lookup"><span data-stu-id="66ef8-174">+0</span></span>          | <span data-ttu-id="66ef8-175">+0</span><span class="sxs-lookup"><span data-stu-id="66ef8-175">+0</span></span>     | <span data-ttu-id="66ef8-176">+0</span><span class="sxs-lookup"><span data-stu-id="66ef8-176">+0</span></span>     | <span data-ttu-id="66ef8-177">+0</span><span class="sxs-lookup"><span data-stu-id="66ef8-177">+0</span></span>          | <span data-ttu-id="66ef8-178">src1</span><span class="sxs-lookup"><span data-stu-id="66ef8-178">src1</span></span>       | <span data-ttu-id="66ef8-179">+inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-179">+inf</span></span>     | <span data-ttu-id="66ef8-180">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-180">NaN</span></span>     |
| <span data-ttu-id="66ef8-181">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="66ef8-181">**+denorm**</span></span>         | <span data-ttu-id="66ef8-182">-inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-182">-inf</span></span>     | <span data-ttu-id="66ef8-183">src1</span><span class="sxs-lookup"><span data-stu-id="66ef8-183">src1</span></span>       | <span data-ttu-id="66ef8-184">+0</span><span class="sxs-lookup"><span data-stu-id="66ef8-184">+0</span></span>          | <span data-ttu-id="66ef8-185">+0</span><span class="sxs-lookup"><span data-stu-id="66ef8-185">+0</span></span>     | <span data-ttu-id="66ef8-186">+0</span><span class="sxs-lookup"><span data-stu-id="66ef8-186">+0</span></span>     | <span data-ttu-id="66ef8-187">+0</span><span class="sxs-lookup"><span data-stu-id="66ef8-187">+0</span></span>          | <span data-ttu-id="66ef8-188">src1</span><span class="sxs-lookup"><span data-stu-id="66ef8-188">src1</span></span>       | <span data-ttu-id="66ef8-189">+inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-189">+inf</span></span>     | <span data-ttu-id="66ef8-190">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-190">NaN</span></span>     |
| <span data-ttu-id="66ef8-191">**+F**</span><span class="sxs-lookup"><span data-stu-id="66ef8-191">**+F**</span></span>              | <span data-ttu-id="66ef8-192">-inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-192">-inf</span></span>     | <span data-ttu-id="66ef8-193">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="66ef8-193">+-F or +-0</span></span> | <span data-ttu-id="66ef8-194">src0</span><span class="sxs-lookup"><span data-stu-id="66ef8-194">src0</span></span>        | <span data-ttu-id="66ef8-195">src0</span><span class="sxs-lookup"><span data-stu-id="66ef8-195">src0</span></span>   | <span data-ttu-id="66ef8-196">src0</span><span class="sxs-lookup"><span data-stu-id="66ef8-196">src0</span></span>   | <span data-ttu-id="66ef8-197">src0</span><span class="sxs-lookup"><span data-stu-id="66ef8-197">src0</span></span>        | <span data-ttu-id="66ef8-198">+F</span><span class="sxs-lookup"><span data-stu-id="66ef8-198">+F</span></span>         | <span data-ttu-id="66ef8-199">+inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-199">+inf</span></span>     | <span data-ttu-id="66ef8-200">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-200">NaN</span></span>     |
| <span data-ttu-id="66ef8-201">**+inf**</span><span class="sxs-lookup"><span data-stu-id="66ef8-201">**+inf**</span></span>            | <span data-ttu-id="66ef8-202">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-202">NaN</span></span>      | <span data-ttu-id="66ef8-203">+inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-203">+inf</span></span>       | <span data-ttu-id="66ef8-204">+inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-204">+inf</span></span>        | <span data-ttu-id="66ef8-205">+inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-205">+inf</span></span>   | <span data-ttu-id="66ef8-206">+inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-206">+inf</span></span>   | <span data-ttu-id="66ef8-207">+inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-207">+inf</span></span>        | <span data-ttu-id="66ef8-208">+inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-208">+inf</span></span>       | <span data-ttu-id="66ef8-209">+inf</span><span class="sxs-lookup"><span data-stu-id="66ef8-209">+inf</span></span>     | <span data-ttu-id="66ef8-210">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-210">NaN</span></span>     |
| <span data-ttu-id="66ef8-211">**NaN**</span><span class="sxs-lookup"><span data-stu-id="66ef8-211">**NaN**</span></span>             | <span data-ttu-id="66ef8-212">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-212">NaN</span></span>      | <span data-ttu-id="66ef8-213">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-213">NaN</span></span>        | <span data-ttu-id="66ef8-214">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-214">NaN</span></span>         | <span data-ttu-id="66ef8-215">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-215">NaN</span></span>    | <span data-ttu-id="66ef8-216">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-216">NaN</span></span>    | <span data-ttu-id="66ef8-217">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-217">NaN</span></span>         | <span data-ttu-id="66ef8-218">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-218">NaN</span></span>        | <span data-ttu-id="66ef8-219">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-219">NaN</span></span>      | <span data-ttu-id="66ef8-220">NaN</span><span class="sxs-lookup"><span data-stu-id="66ef8-220">NaN</span></span>     |



 

<span data-ttu-id="66ef8-221">Questa istruzione si applica alle fasi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="66ef8-221">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="66ef8-222">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="66ef8-222">Vertex Shader</span></span> | <span data-ttu-id="66ef8-223">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="66ef8-223">Geometry Shader</span></span> | <span data-ttu-id="66ef8-224">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="66ef8-224">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="66ef8-225">x</span><span class="sxs-lookup"><span data-stu-id="66ef8-225">x</span></span>             | <span data-ttu-id="66ef8-226">x</span><span class="sxs-lookup"><span data-stu-id="66ef8-226">x</span></span>               | <span data-ttu-id="66ef8-227">x</span><span class="sxs-lookup"><span data-stu-id="66ef8-227">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="66ef8-228">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="66ef8-228">Minimum Shader Model</span></span>

<span data-ttu-id="66ef8-229">Questa funzione è supportata nei modelli di shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="66ef8-229">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="66ef8-230">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="66ef8-230">Shader Model</span></span>                                              | <span data-ttu-id="66ef8-231">Supportato</span><span class="sxs-lookup"><span data-stu-id="66ef8-231">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="66ef8-232">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="66ef8-232">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="66ef8-233">sì</span><span class="sxs-lookup"><span data-stu-id="66ef8-233">yes</span></span>       |
| [<span data-ttu-id="66ef8-234">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="66ef8-234">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="66ef8-235">sì</span><span class="sxs-lookup"><span data-stu-id="66ef8-235">yes</span></span>       |
| [<span data-ttu-id="66ef8-236">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="66ef8-236">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="66ef8-237">sì</span><span class="sxs-lookup"><span data-stu-id="66ef8-237">yes</span></span>       |
| [<span data-ttu-id="66ef8-238">Modello shader 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="66ef8-238">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="66ef8-239">no</span><span class="sxs-lookup"><span data-stu-id="66ef8-239">no</span></span>        |
| [<span data-ttu-id="66ef8-240">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="66ef8-240">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="66ef8-241">no</span><span class="sxs-lookup"><span data-stu-id="66ef8-241">no</span></span>        |
| [<span data-ttu-id="66ef8-242">Modello shader 1 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="66ef8-242">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="66ef8-243">no</span><span class="sxs-lookup"><span data-stu-id="66ef8-243">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="66ef8-244">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66ef8-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66ef8-245">Assembly del modello shader 4 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="66ef8-245">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





