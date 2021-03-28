---
title: ddiv (SM5-ASM)
description: Calcola una divisione a precisione doppia a livello di componente.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56f5c3aae9d416d24f41de8d8308c5a69be9d016
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993016"
---
# <a name="ddiv-sm5---asm"></a><span data-ttu-id="3a2de-103">ddiv (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="3a2de-103">ddiv (sm5 - asm)</span></span>

<span data-ttu-id="3a2de-104">Calcola una divisione a precisione doppia a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="3a2de-104">Computes a component-wise double-precision division.</span></span>



| <span data-ttu-id="3a2de-105">ddiv \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="3a2de-105">ddiv\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="3a2de-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="3a2de-106">Item</span></span>                                                            | <span data-ttu-id="3a2de-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a2de-107">Description</span></span>                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2de-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3a2de-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3a2de-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3a2de-109">\[in\] The result of the operation.</span></span> <span data-ttu-id="3a2de-110">Il valore del risultato deve essere accurato per 0,5 ULP rispetto.</span><span class="sxs-lookup"><span data-stu-id="3a2de-110">The result value must be accurate to 0.5 ULP.</span></span> <br/> |
| <span data-ttu-id="3a2de-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3a2de-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3a2de-112">\[nel \] dividendo.</span><span class="sxs-lookup"><span data-stu-id="3a2de-112">\[in\] The dividend.</span></span><br/>                                                               |
| <span data-ttu-id="3a2de-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="3a2de-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="3a2de-114">\[nel \] divisore.</span><span class="sxs-lookup"><span data-stu-id="3a2de-114">\[in\] The divisor.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="3a2de-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a2de-115">Remarks</span></span>

<span data-ttu-id="3a2de-116">L'istruzione DDIV verrà generata dal compilatore HLSL ogni volta che viene usato l'operatore di divisione con i valori Double.</span><span class="sxs-lookup"><span data-stu-id="3a2de-116">The DDIV instruction will be emitted by the HLSL compiler whenever the division operator is used with doubles.</span></span> <span data-ttu-id="3a2de-117">L'accuratezza di questa istruzione sarà obbligatoria per 0,5 ULP rispetto.</span><span class="sxs-lookup"><span data-stu-id="3a2de-117">The accuracy of this instruction will be required to be 0.5 ULP.</span></span>

<span data-ttu-id="3a2de-118">Gli shader che usano questa istruzione verranno contrassegnati con un flag shader che ne causerà la mancata associazione a meno che non vengano soddisfatte tutte le condizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a2de-118">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="3a2de-119">Il sistema supporta DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="3a2de-119">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="3a2de-120">Il sistema include un driver WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="3a2de-120">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="3a2de-121">Il driver segnala il supporto per questa istruzione tramite le **\_ \_ Opzioni d3d11 dei dati della funzionalità d3d11 \_ \_ . ExtendedDoublesShaderInstructions** impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="3a2de-121">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="3a2de-122">Nella tabella seguente vengono illustrati i risultati btained durante l'esecuzione dell'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="3a2de-122">The following table shows the results btained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="3a2de-123">In questa tabella F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="3a2de-123">In this table F means finite-real number.</span></span>



|                     |          |        |          |        |        |          |        |          |         |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="3a2de-124">**src1 src0->**</span><span class="sxs-lookup"><span data-stu-id="3a2de-124">**src0 src1 ->**</span></span> | <span data-ttu-id="3a2de-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="3a2de-125">**-inf**</span></span> | <span data-ttu-id="3a2de-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="3a2de-126">**-F**</span></span> | <span data-ttu-id="3a2de-127">**-1,0**</span><span class="sxs-lookup"><span data-stu-id="3a2de-127">**-1.0**</span></span> | <span data-ttu-id="3a2de-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="3a2de-128">**-0**</span></span> | <span data-ttu-id="3a2de-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="3a2de-129">**+0**</span></span> | <span data-ttu-id="3a2de-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="3a2de-130">**+1.0**</span></span> | <span data-ttu-id="3a2de-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="3a2de-131">**+F**</span></span> | <span data-ttu-id="3a2de-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="3a2de-132">**+inf**</span></span> | <span data-ttu-id="3a2de-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="3a2de-133">**NaN**</span></span> |
| <span data-ttu-id="3a2de-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="3a2de-134">**-inf**</span></span>            | <span data-ttu-id="3a2de-135">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-135">NaN</span></span>      | <span data-ttu-id="3a2de-136">+inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-136">+inf</span></span>   | <span data-ttu-id="3a2de-137">+inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-137">+inf</span></span>     | <span data-ttu-id="3a2de-138">+inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-138">+inf</span></span>   | <span data-ttu-id="3a2de-139">-inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-139">-inf</span></span>   | <span data-ttu-id="3a2de-140">-inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-140">-inf</span></span>     | <span data-ttu-id="3a2de-141">-inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-141">-inf</span></span>   | <span data-ttu-id="3a2de-142">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-142">NaN</span></span>      | <span data-ttu-id="3a2de-143">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-143">NaN</span></span>     |
| <span data-ttu-id="3a2de-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="3a2de-144">**-F**</span></span>              | <span data-ttu-id="3a2de-145">+0</span><span class="sxs-lookup"><span data-stu-id="3a2de-145">+0</span></span>       | <span data-ttu-id="3a2de-146">+ F</span><span class="sxs-lookup"><span data-stu-id="3a2de-146">+F</span></span>     | <span data-ttu-id="3a2de-147">-src0</span><span class="sxs-lookup"><span data-stu-id="3a2de-147">-src0</span></span>    | <span data-ttu-id="3a2de-148">+inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-148">+inf</span></span>   | <span data-ttu-id="3a2de-149">-inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-149">-inf</span></span>   | <span data-ttu-id="3a2de-150">src0</span><span class="sxs-lookup"><span data-stu-id="3a2de-150">src0</span></span>     | <span data-ttu-id="3a2de-151">-F</span><span class="sxs-lookup"><span data-stu-id="3a2de-151">-F</span></span>     | <span data-ttu-id="3a2de-152">-0</span><span class="sxs-lookup"><span data-stu-id="3a2de-152">-0</span></span>       | <span data-ttu-id="3a2de-153">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-153">NaN</span></span>     |
| <span data-ttu-id="3a2de-154">**-0**</span><span class="sxs-lookup"><span data-stu-id="3a2de-154">**-0**</span></span>              | <span data-ttu-id="3a2de-155">+0</span><span class="sxs-lookup"><span data-stu-id="3a2de-155">+0</span></span>       | <span data-ttu-id="3a2de-156">+0</span><span class="sxs-lookup"><span data-stu-id="3a2de-156">+0</span></span>     | <span data-ttu-id="3a2de-157">+0</span><span class="sxs-lookup"><span data-stu-id="3a2de-157">+0</span></span>       | <span data-ttu-id="3a2de-158">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-158">NaN</span></span>    | <span data-ttu-id="3a2de-159">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-159">NaN</span></span>    | <span data-ttu-id="3a2de-160">-0</span><span class="sxs-lookup"><span data-stu-id="3a2de-160">-0</span></span>       | <span data-ttu-id="3a2de-161">-0</span><span class="sxs-lookup"><span data-stu-id="3a2de-161">-0</span></span>     | <span data-ttu-id="3a2de-162">-0</span><span class="sxs-lookup"><span data-stu-id="3a2de-162">-0</span></span>       | <span data-ttu-id="3a2de-163">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-163">NaN</span></span>     |
| <span data-ttu-id="3a2de-164">**+0**</span><span class="sxs-lookup"><span data-stu-id="3a2de-164">**+0**</span></span>              | <span data-ttu-id="3a2de-165">-0</span><span class="sxs-lookup"><span data-stu-id="3a2de-165">-0</span></span>       | <span data-ttu-id="3a2de-166">-0</span><span class="sxs-lookup"><span data-stu-id="3a2de-166">-0</span></span>     | <span data-ttu-id="3a2de-167">-0</span><span class="sxs-lookup"><span data-stu-id="3a2de-167">-0</span></span>       | <span data-ttu-id="3a2de-168">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-168">NaN</span></span>    | <span data-ttu-id="3a2de-169">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-169">NaN</span></span>    | <span data-ttu-id="3a2de-170">+0</span><span class="sxs-lookup"><span data-stu-id="3a2de-170">+0</span></span>       | <span data-ttu-id="3a2de-171">+0</span><span class="sxs-lookup"><span data-stu-id="3a2de-171">+0</span></span>     | <span data-ttu-id="3a2de-172">+0</span><span class="sxs-lookup"><span data-stu-id="3a2de-172">+0</span></span>       | <span data-ttu-id="3a2de-173">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-173">NaN</span></span>     |
| <span data-ttu-id="3a2de-174">**+ F**</span><span class="sxs-lookup"><span data-stu-id="3a2de-174">**+F**</span></span>              | <span data-ttu-id="3a2de-175">-0</span><span class="sxs-lookup"><span data-stu-id="3a2de-175">-0</span></span>       | <span data-ttu-id="3a2de-176">-F</span><span class="sxs-lookup"><span data-stu-id="3a2de-176">-F</span></span>     | <span data-ttu-id="3a2de-177">-src0</span><span class="sxs-lookup"><span data-stu-id="3a2de-177">-src0</span></span>    | <span data-ttu-id="3a2de-178">-inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-178">-inf</span></span>   | <span data-ttu-id="3a2de-179">+inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-179">+inf</span></span>   | <span data-ttu-id="3a2de-180">src0</span><span class="sxs-lookup"><span data-stu-id="3a2de-180">src0</span></span>     | <span data-ttu-id="3a2de-181">+ F</span><span class="sxs-lookup"><span data-stu-id="3a2de-181">+F</span></span>     | <span data-ttu-id="3a2de-182">+0</span><span class="sxs-lookup"><span data-stu-id="3a2de-182">+0</span></span>       | <span data-ttu-id="3a2de-183">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-183">NaN</span></span>     |
| <span data-ttu-id="3a2de-184">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="3a2de-184">**+inf**</span></span>            | <span data-ttu-id="3a2de-185">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-185">NaN</span></span>      | <span data-ttu-id="3a2de-186">-inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-186">-inf</span></span>   | <span data-ttu-id="3a2de-187">-inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-187">-inf</span></span>     | <span data-ttu-id="3a2de-188">-inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-188">-inf</span></span>   | <span data-ttu-id="3a2de-189">+inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-189">+inf</span></span>   | <span data-ttu-id="3a2de-190">+inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-190">+inf</span></span>     | <span data-ttu-id="3a2de-191">+inf</span><span class="sxs-lookup"><span data-stu-id="3a2de-191">+inf</span></span>   | <span data-ttu-id="3a2de-192">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-192">NaN</span></span>      | <span data-ttu-id="3a2de-193">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-193">NaN</span></span>     |
| <span data-ttu-id="3a2de-194">**NaN**</span><span class="sxs-lookup"><span data-stu-id="3a2de-194">**NaN**</span></span>             | <span data-ttu-id="3a2de-195">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-195">NaN</span></span>      | <span data-ttu-id="3a2de-196">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-196">NaN</span></span>    | <span data-ttu-id="3a2de-197">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-197">NaN</span></span>      | <span data-ttu-id="3a2de-198">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-198">NaN</span></span>    | <span data-ttu-id="3a2de-199">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-199">NaN</span></span>    | <span data-ttu-id="3a2de-200">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-200">NaN</span></span>      | <span data-ttu-id="3a2de-201">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-201">NaN</span></span>    | <span data-ttu-id="3a2de-202">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-202">NaN</span></span>      | <span data-ttu-id="3a2de-203">NaN</span><span class="sxs-lookup"><span data-stu-id="3a2de-203">NaN</span></span>     |



 

<span data-ttu-id="3a2de-204">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a2de-204">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3a2de-205">Vertice</span><span class="sxs-lookup"><span data-stu-id="3a2de-205">Vertex</span></span> | <span data-ttu-id="3a2de-206">Hull</span><span class="sxs-lookup"><span data-stu-id="3a2de-206">Hull</span></span> | <span data-ttu-id="3a2de-207">Dominio</span><span class="sxs-lookup"><span data-stu-id="3a2de-207">Domain</span></span> | <span data-ttu-id="3a2de-208">Geometria</span><span class="sxs-lookup"><span data-stu-id="3a2de-208">Geometry</span></span> | <span data-ttu-id="3a2de-209">Pixel</span><span class="sxs-lookup"><span data-stu-id="3a2de-209">Pixel</span></span> | <span data-ttu-id="3a2de-210">Calcolo</span><span class="sxs-lookup"><span data-stu-id="3a2de-210">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3a2de-211">X</span><span class="sxs-lookup"><span data-stu-id="3a2de-211">X</span></span>      | <span data-ttu-id="3a2de-212">X</span><span class="sxs-lookup"><span data-stu-id="3a2de-212">X</span></span>    | <span data-ttu-id="3a2de-213">X</span><span class="sxs-lookup"><span data-stu-id="3a2de-213">X</span></span>      | <span data-ttu-id="3a2de-214">X</span><span class="sxs-lookup"><span data-stu-id="3a2de-214">X</span></span>        | <span data-ttu-id="3a2de-215">X</span><span class="sxs-lookup"><span data-stu-id="3a2de-215">X</span></span>     | <span data-ttu-id="3a2de-216">X</span><span class="sxs-lookup"><span data-stu-id="3a2de-216">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3a2de-217">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="3a2de-217">Minimum Shader Model</span></span>

<span data-ttu-id="3a2de-218">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a2de-218">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="3a2de-219">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="3a2de-219">Shader Model</span></span>                                              | <span data-ttu-id="3a2de-220">Supportato</span><span class="sxs-lookup"><span data-stu-id="3a2de-220">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3a2de-221">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="3a2de-221">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3a2de-222">sì</span><span class="sxs-lookup"><span data-stu-id="3a2de-222">yes</span></span>       |
| [<span data-ttu-id="3a2de-223">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="3a2de-223">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3a2de-224">no</span><span class="sxs-lookup"><span data-stu-id="3a2de-224">no</span></span>        |
| [<span data-ttu-id="3a2de-225">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="3a2de-225">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3a2de-226">no</span><span class="sxs-lookup"><span data-stu-id="3a2de-226">no</span></span>        |
| [<span data-ttu-id="3a2de-227">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a2de-227">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3a2de-228">no</span><span class="sxs-lookup"><span data-stu-id="3a2de-228">no</span></span>        |
| [<span data-ttu-id="3a2de-229">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a2de-229">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3a2de-230">no</span><span class="sxs-lookup"><span data-stu-id="3a2de-230">no</span></span>        |
| [<span data-ttu-id="3a2de-231">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a2de-231">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3a2de-232">no</span><span class="sxs-lookup"><span data-stu-id="3a2de-232">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3a2de-233">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a2de-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a2de-234">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a2de-234">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





