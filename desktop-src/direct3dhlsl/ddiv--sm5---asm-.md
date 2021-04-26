---
title: ddiv (sm5 - asm)
description: Calcola una divisione a precisione doppia per componente.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fc039b222b28a5fb1217d23c78470aff1739f7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999158"
---
# <a name="ddiv-sm5---asm"></a><span data-ttu-id="a8901-103">ddiv (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="a8901-103">ddiv (sm5 - asm)</span></span>

<span data-ttu-id="a8901-104">Calcola una divisione a precisione doppia per componente.</span><span class="sxs-lookup"><span data-stu-id="a8901-104">Computes a component-wise double-precision division.</span></span>



| <span data-ttu-id="a8901-105">ddiv \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a8901-105">ddiv\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a8901-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8901-106">Item</span></span>                                                            | <span data-ttu-id="a8901-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8901-107">Description</span></span>                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8901-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="a8901-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a8901-109">\[in \] Risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a8901-109">\[in\] The result of the operation.</span></span> <span data-ttu-id="a8901-110">Il valore del risultato deve essere preciso a 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="a8901-110">The result value must be accurate to 0.5 ULP.</span></span> <br/> |
| <span data-ttu-id="a8901-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a8901-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a8901-112">\[in \] Dividendo.</span><span class="sxs-lookup"><span data-stu-id="a8901-112">\[in\] The dividend.</span></span><br/>                                                               |
| <span data-ttu-id="a8901-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a8901-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a8901-114">\[in \] Divisore.</span><span class="sxs-lookup"><span data-stu-id="a8901-114">\[in\] The divisor.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="a8901-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8901-115">Remarks</span></span>

<span data-ttu-id="a8901-116">L'istruzione DDIV verrà generata dal compilatore HLSL ogni volta che l'operatore di divisione viene usato con valori double.</span><span class="sxs-lookup"><span data-stu-id="a8901-116">The DDIV instruction will be emitted by the HLSL compiler whenever the division operator is used with doubles.</span></span> <span data-ttu-id="a8901-117">L'accuratezza di questa istruzione deve essere 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="a8901-117">The accuracy of this instruction will be required to be 0.5 ULP.</span></span>

<span data-ttu-id="a8901-118">Gli shader che usano questa istruzione verranno contrassegnati con un flag shader che ne causerà l'associazione a meno che non vengano soddisfatte tutte le condizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="a8901-118">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="a8901-119">Il sistema supporta DirectX 11.1.</span><span class="sxs-lookup"><span data-stu-id="a8901-119">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="a8901-120">Il sistema include un driver WDDM 1.2.</span><span class="sxs-lookup"><span data-stu-id="a8901-120">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="a8901-121">Il driver segnala il supporto per questa istruzione **tramite D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** impostato su **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="a8901-121">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="a8901-122">Nella tabella seguente vengono illustrati i risultati relativi all'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichi alcun overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="a8901-122">The following table shows the results btained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="a8901-123">In questa tabella F indica un numero finito-reale.</span><span class="sxs-lookup"><span data-stu-id="a8901-123">In this table F means finite-real number.</span></span>



| <span data-ttu-id="a8901-124">**src0 src1 ->**</span><span class="sxs-lookup"><span data-stu-id="a8901-124">**src0 src1 ->**</span></span> | <span data-ttu-id="a8901-125">**-inf**</span><span class="sxs-lookup"><span data-stu-id="a8901-125">**-inf**</span></span> | <span data-ttu-id="a8901-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="a8901-126">**-F**</span></span> | <span data-ttu-id="a8901-127">**-1.0**</span><span class="sxs-lookup"><span data-stu-id="a8901-127">**-1.0**</span></span> | <span data-ttu-id="a8901-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="a8901-128">**-0**</span></span> | <span data-ttu-id="a8901-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="a8901-129">**+0**</span></span> | <span data-ttu-id="a8901-130">**+1.0**</span><span class="sxs-lookup"><span data-stu-id="a8901-130">**+1.0**</span></span> | <span data-ttu-id="a8901-131">**+F**</span><span class="sxs-lookup"><span data-stu-id="a8901-131">**+F**</span></span> | <span data-ttu-id="a8901-132">**+inf**</span><span class="sxs-lookup"><span data-stu-id="a8901-132">**+inf**</span></span> | <span data-ttu-id="a8901-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a8901-133">**NaN**</span></span> |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="a8901-134">**-inf**</span><span class="sxs-lookup"><span data-stu-id="a8901-134">**-inf**</span></span>            | <span data-ttu-id="a8901-135">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-135">NaN</span></span>      | <span data-ttu-id="a8901-136">+inf</span><span class="sxs-lookup"><span data-stu-id="a8901-136">+inf</span></span>   | <span data-ttu-id="a8901-137">+inf</span><span class="sxs-lookup"><span data-stu-id="a8901-137">+inf</span></span>     | <span data-ttu-id="a8901-138">+inf</span><span class="sxs-lookup"><span data-stu-id="a8901-138">+inf</span></span>   | <span data-ttu-id="a8901-139">-inf</span><span class="sxs-lookup"><span data-stu-id="a8901-139">-inf</span></span>   | <span data-ttu-id="a8901-140">-inf</span><span class="sxs-lookup"><span data-stu-id="a8901-140">-inf</span></span>     | <span data-ttu-id="a8901-141">-inf</span><span class="sxs-lookup"><span data-stu-id="a8901-141">-inf</span></span>   | <span data-ttu-id="a8901-142">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-142">NaN</span></span>      | <span data-ttu-id="a8901-143">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-143">NaN</span></span>     |
| <span data-ttu-id="a8901-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="a8901-144">**-F**</span></span>              | <span data-ttu-id="a8901-145">+0</span><span class="sxs-lookup"><span data-stu-id="a8901-145">+0</span></span>       | <span data-ttu-id="a8901-146">+F</span><span class="sxs-lookup"><span data-stu-id="a8901-146">+F</span></span>     | <span data-ttu-id="a8901-147">-src0</span><span class="sxs-lookup"><span data-stu-id="a8901-147">-src0</span></span>    | <span data-ttu-id="a8901-148">+inf</span><span class="sxs-lookup"><span data-stu-id="a8901-148">+inf</span></span>   | <span data-ttu-id="a8901-149">-inf</span><span class="sxs-lookup"><span data-stu-id="a8901-149">-inf</span></span>   | <span data-ttu-id="a8901-150">src0</span><span class="sxs-lookup"><span data-stu-id="a8901-150">src0</span></span>     | <span data-ttu-id="a8901-151">-F</span><span class="sxs-lookup"><span data-stu-id="a8901-151">-F</span></span>     | <span data-ttu-id="a8901-152">-0</span><span class="sxs-lookup"><span data-stu-id="a8901-152">-0</span></span>       | <span data-ttu-id="a8901-153">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-153">NaN</span></span>     |
| <span data-ttu-id="a8901-154">**-0**</span><span class="sxs-lookup"><span data-stu-id="a8901-154">**-0**</span></span>              | <span data-ttu-id="a8901-155">+0</span><span class="sxs-lookup"><span data-stu-id="a8901-155">+0</span></span>       | <span data-ttu-id="a8901-156">+0</span><span class="sxs-lookup"><span data-stu-id="a8901-156">+0</span></span>     | <span data-ttu-id="a8901-157">+0</span><span class="sxs-lookup"><span data-stu-id="a8901-157">+0</span></span>       | <span data-ttu-id="a8901-158">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-158">NaN</span></span>    | <span data-ttu-id="a8901-159">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-159">NaN</span></span>    | <span data-ttu-id="a8901-160">-0</span><span class="sxs-lookup"><span data-stu-id="a8901-160">-0</span></span>       | <span data-ttu-id="a8901-161">-0</span><span class="sxs-lookup"><span data-stu-id="a8901-161">-0</span></span>     | <span data-ttu-id="a8901-162">-0</span><span class="sxs-lookup"><span data-stu-id="a8901-162">-0</span></span>       | <span data-ttu-id="a8901-163">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-163">NaN</span></span>     |
| <span data-ttu-id="a8901-164">**+0**</span><span class="sxs-lookup"><span data-stu-id="a8901-164">**+0**</span></span>              | <span data-ttu-id="a8901-165">-0</span><span class="sxs-lookup"><span data-stu-id="a8901-165">-0</span></span>       | <span data-ttu-id="a8901-166">-0</span><span class="sxs-lookup"><span data-stu-id="a8901-166">-0</span></span>     | <span data-ttu-id="a8901-167">-0</span><span class="sxs-lookup"><span data-stu-id="a8901-167">-0</span></span>       | <span data-ttu-id="a8901-168">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-168">NaN</span></span>    | <span data-ttu-id="a8901-169">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-169">NaN</span></span>    | <span data-ttu-id="a8901-170">+0</span><span class="sxs-lookup"><span data-stu-id="a8901-170">+0</span></span>       | <span data-ttu-id="a8901-171">+0</span><span class="sxs-lookup"><span data-stu-id="a8901-171">+0</span></span>     | <span data-ttu-id="a8901-172">+0</span><span class="sxs-lookup"><span data-stu-id="a8901-172">+0</span></span>       | <span data-ttu-id="a8901-173">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-173">NaN</span></span>     |
| <span data-ttu-id="a8901-174">**+F**</span><span class="sxs-lookup"><span data-stu-id="a8901-174">**+F**</span></span>              | <span data-ttu-id="a8901-175">-0</span><span class="sxs-lookup"><span data-stu-id="a8901-175">-0</span></span>       | <span data-ttu-id="a8901-176">-F</span><span class="sxs-lookup"><span data-stu-id="a8901-176">-F</span></span>     | <span data-ttu-id="a8901-177">-src0</span><span class="sxs-lookup"><span data-stu-id="a8901-177">-src0</span></span>    | <span data-ttu-id="a8901-178">-inf</span><span class="sxs-lookup"><span data-stu-id="a8901-178">-inf</span></span>   | <span data-ttu-id="a8901-179">+inf</span><span class="sxs-lookup"><span data-stu-id="a8901-179">+inf</span></span>   | <span data-ttu-id="a8901-180">src0</span><span class="sxs-lookup"><span data-stu-id="a8901-180">src0</span></span>     | <span data-ttu-id="a8901-181">+F</span><span class="sxs-lookup"><span data-stu-id="a8901-181">+F</span></span>     | <span data-ttu-id="a8901-182">+0</span><span class="sxs-lookup"><span data-stu-id="a8901-182">+0</span></span>       | <span data-ttu-id="a8901-183">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-183">NaN</span></span>     |
| <span data-ttu-id="a8901-184">**+inf**</span><span class="sxs-lookup"><span data-stu-id="a8901-184">**+inf**</span></span>            | <span data-ttu-id="a8901-185">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-185">NaN</span></span>      | <span data-ttu-id="a8901-186">-inf</span><span class="sxs-lookup"><span data-stu-id="a8901-186">-inf</span></span>   | <span data-ttu-id="a8901-187">-inf</span><span class="sxs-lookup"><span data-stu-id="a8901-187">-inf</span></span>     | <span data-ttu-id="a8901-188">-inf</span><span class="sxs-lookup"><span data-stu-id="a8901-188">-inf</span></span>   | <span data-ttu-id="a8901-189">+inf</span><span class="sxs-lookup"><span data-stu-id="a8901-189">+inf</span></span>   | <span data-ttu-id="a8901-190">+inf</span><span class="sxs-lookup"><span data-stu-id="a8901-190">+inf</span></span>     | <span data-ttu-id="a8901-191">+inf</span><span class="sxs-lookup"><span data-stu-id="a8901-191">+inf</span></span>   | <span data-ttu-id="a8901-192">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-192">NaN</span></span>      | <span data-ttu-id="a8901-193">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-193">NaN</span></span>     |
| <span data-ttu-id="a8901-194">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a8901-194">**NaN**</span></span>             | <span data-ttu-id="a8901-195">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-195">NaN</span></span>      | <span data-ttu-id="a8901-196">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-196">NaN</span></span>    | <span data-ttu-id="a8901-197">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-197">NaN</span></span>      | <span data-ttu-id="a8901-198">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-198">NaN</span></span>    | <span data-ttu-id="a8901-199">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-199">NaN</span></span>    | <span data-ttu-id="a8901-200">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-200">NaN</span></span>      | <span data-ttu-id="a8901-201">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-201">NaN</span></span>    | <span data-ttu-id="a8901-202">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-202">NaN</span></span>      | <span data-ttu-id="a8901-203">NaN</span><span class="sxs-lookup"><span data-stu-id="a8901-203">NaN</span></span>     |



 

<span data-ttu-id="a8901-204">Questa istruzione si applica alle fasi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a8901-204">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a8901-205">Vertice</span><span class="sxs-lookup"><span data-stu-id="a8901-205">Vertex</span></span> | <span data-ttu-id="a8901-206">Scafo</span><span class="sxs-lookup"><span data-stu-id="a8901-206">Hull</span></span> | <span data-ttu-id="a8901-207">Dominio</span><span class="sxs-lookup"><span data-stu-id="a8901-207">Domain</span></span> | <span data-ttu-id="a8901-208">Geometria</span><span class="sxs-lookup"><span data-stu-id="a8901-208">Geometry</span></span> | <span data-ttu-id="a8901-209">Pixel</span><span class="sxs-lookup"><span data-stu-id="a8901-209">Pixel</span></span> | <span data-ttu-id="a8901-210">Calcolo</span><span class="sxs-lookup"><span data-stu-id="a8901-210">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a8901-211">X</span><span class="sxs-lookup"><span data-stu-id="a8901-211">X</span></span>      | <span data-ttu-id="a8901-212">X</span><span class="sxs-lookup"><span data-stu-id="a8901-212">X</span></span>    | <span data-ttu-id="a8901-213">X</span><span class="sxs-lookup"><span data-stu-id="a8901-213">X</span></span>      | <span data-ttu-id="a8901-214">X</span><span class="sxs-lookup"><span data-stu-id="a8901-214">X</span></span>        | <span data-ttu-id="a8901-215">X</span><span class="sxs-lookup"><span data-stu-id="a8901-215">X</span></span>     | <span data-ttu-id="a8901-216">X</span><span class="sxs-lookup"><span data-stu-id="a8901-216">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a8901-217">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="a8901-217">Minimum Shader Model</span></span>

<span data-ttu-id="a8901-218">Questa istruzione è supportata nei modelli di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a8901-218">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a8901-219">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="a8901-219">Shader Model</span></span>                                              | <span data-ttu-id="a8901-220">Supportato</span><span class="sxs-lookup"><span data-stu-id="a8901-220">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a8901-221">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="a8901-221">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a8901-222">sì</span><span class="sxs-lookup"><span data-stu-id="a8901-222">yes</span></span>       |
| [<span data-ttu-id="a8901-223">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="a8901-223">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a8901-224">no</span><span class="sxs-lookup"><span data-stu-id="a8901-224">no</span></span>        |
| [<span data-ttu-id="a8901-225">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="a8901-225">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a8901-226">no</span><span class="sxs-lookup"><span data-stu-id="a8901-226">no</span></span>        |
| [<span data-ttu-id="a8901-227">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8901-227">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a8901-228">no</span><span class="sxs-lookup"><span data-stu-id="a8901-228">no</span></span>        |
| [<span data-ttu-id="a8901-229">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8901-229">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a8901-230">no</span><span class="sxs-lookup"><span data-stu-id="a8901-230">no</span></span>        |
| [<span data-ttu-id="a8901-231">Modello shader 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8901-231">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a8901-232">no</span><span class="sxs-lookup"><span data-stu-id="a8901-232">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a8901-233">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8901-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8901-234">Assembly del modello shader 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8901-234">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





