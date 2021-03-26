---
title: Dadd (SM5-ASM)
description: Aggiunta a precisione doppia a livello di componente.
ms.assetid: 416F1103-E27B-4AFC-9ED1-492FF8A93492
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e217a03a5ba9e4da0d365bbfd15e4283f1a69cb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398203"
---
# <a name="dadd-sm5---asm"></a><span data-ttu-id="2c5b5-103">Dadd (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2c5b5-103">dadd (sm5 - asm)</span></span>

<span data-ttu-id="2c5b5-104">Aggiunta a precisione doppia a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="2c5b5-104">Component-wise double-precision add.</span></span>



| <span data-ttu-id="2c5b5-105">Dadd \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2c5b5-105">dadd\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2c5b5-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c5b5-106">Item</span></span>                                                            | <span data-ttu-id="2c5b5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c5b5-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2c5b5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2c5b5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2c5b5-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2c5b5-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="2c5b5-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2c5b5-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2c5b5-111">\[nei \] componenti da aggiungere con *src1*.</span><span class="sxs-lookup"><span data-stu-id="2c5b5-111">\[in\] The components to add with *src1*.</span></span><br/>          |
| <span data-ttu-id="2c5b5-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="2c5b5-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="2c5b5-113">\[nei \] componenti da aggiungere con *src0*</span><span class="sxs-lookup"><span data-stu-id="2c5b5-113">\[in\] The components to add with *src0*</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="2c5b5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c5b5-114">Remarks</span></span>

<span data-ttu-id="2c5b5-115">I swizzles validi per i parametri di origine sono xyzw, Xyxy, zwxy, zwzw.</span><span class="sxs-lookup"><span data-stu-id="2c5b5-115">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="2c5b5-116">Le maschere *dest* valide sono. XY,. ZW e. xyzw.</span><span class="sxs-lookup"><span data-stu-id="2c5b5-116">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="2c5b5-117">I mapping seguenti sono post-swizzle:</span><span class="sxs-lookup"><span data-stu-id="2c5b5-117">The following mappings are post-swizzle:</span></span>

-   <span data-ttu-id="2c5b5-118">*dest* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="2c5b5-118">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="2c5b5-119">*src0* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="2c5b5-119">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="2c5b5-120">*src1* è un vec2 doppio tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="2c5b5-120">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="2c5b5-121">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="2c5b5-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="2c5b5-122">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="2c5b5-122">F means finite-real number.</span></span>



<table>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="2c5b5-123"><strong>src0</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-123"><strong>src0</strong></span></span><br /><span data-ttu-id="2c5b5-124">
<strong>src1-></strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-124">
<strong>src1-></strong></span></span><br />
</dl></td>
<td><span data-ttu-id="2c5b5-125"><strong>-INF</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-125"><strong>-inf</strong></span></span></td>
<td><span data-ttu-id="2c5b5-126"><strong>-F</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-126"><strong>-F</strong></span></span></td>
<td><span data-ttu-id="2c5b5-127"><strong>-0</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-127"><strong>-0</strong></span></span></td>
<td><span data-ttu-id="2c5b5-128"><strong>+0</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-128"><strong>+0</strong></span></span></td>
<td><span data-ttu-id="2c5b5-129"><strong>+ F</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-129"><strong>+F</strong></span></span></td>
<td><span data-ttu-id="2c5b5-130"><strong>+ INF</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-130"><strong>+inf</strong></span></span></td>
<td><span data-ttu-id="2c5b5-131"><strong>NaN</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-131"><strong>NaN</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c5b5-132"><strong>-INF</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-132"><strong>-inf</strong></span></span></td>
<td><span data-ttu-id="2c5b5-133">-inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-133">-inf</span></span></td>
<td><span data-ttu-id="2c5b5-134">-inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-134">-inf</span></span></td>
<td><span data-ttu-id="2c5b5-135">-inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-135">-inf</span></span></td>
<td><span data-ttu-id="2c5b5-136">-inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-136">-inf</span></span></td>
<td><span data-ttu-id="2c5b5-137">-inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-137">-inf</span></span></td>
<td><span data-ttu-id="2c5b5-138">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-138">NaN</span></span></td>
<td><span data-ttu-id="2c5b5-139">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-139">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c5b5-140"><strong>-F</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-140"><strong>-F</strong></span></span></td>
<td><span data-ttu-id="2c5b5-141">-inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-141">-inf</span></span></td>
<td><span data-ttu-id="2c5b5-142">-F</span><span class="sxs-lookup"><span data-stu-id="2c5b5-142">-F</span></span></td>
<td><span data-ttu-id="2c5b5-143">src0</span><span class="sxs-lookup"><span data-stu-id="2c5b5-143">src0</span></span></td>
<td><span data-ttu-id="2c5b5-144">src0</span><span class="sxs-lookup"><span data-stu-id="2c5b5-144">src0</span></span></td>
<td><span data-ttu-id="2c5b5-145">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="2c5b5-145">+-F or +-0</span></span></td>
<td><span data-ttu-id="2c5b5-146">+inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-146">+inf</span></span></td>
<td><span data-ttu-id="2c5b5-147">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-147">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c5b5-148"><strong>-0</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-148"><strong>-0</strong></span></span></td>
<td><span data-ttu-id="2c5b5-149">-inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-149">-inf</span></span></td>
<td><span data-ttu-id="2c5b5-150">src1</span><span class="sxs-lookup"><span data-stu-id="2c5b5-150">src1</span></span></td>
<td><span data-ttu-id="2c5b5-151">-0</span><span class="sxs-lookup"><span data-stu-id="2c5b5-151">-0</span></span></td>
<td><span data-ttu-id="2c5b5-152">+0</span><span class="sxs-lookup"><span data-stu-id="2c5b5-152">+0</span></span></td>
<td><span data-ttu-id="2c5b5-153">src1</span><span class="sxs-lookup"><span data-stu-id="2c5b5-153">src1</span></span></td>
<td><span data-ttu-id="2c5b5-154">+inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-154">+inf</span></span></td>
<td><span data-ttu-id="2c5b5-155">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-155">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c5b5-156"><strong>+0</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-156"><strong>+0</strong></span></span></td>
<td><span data-ttu-id="2c5b5-157">-inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-157">-inf</span></span></td>
<td><span data-ttu-id="2c5b5-158">src1</span><span class="sxs-lookup"><span data-stu-id="2c5b5-158">src1</span></span></td>
<td><span data-ttu-id="2c5b5-159">+0</span><span class="sxs-lookup"><span data-stu-id="2c5b5-159">+0</span></span></td>
<td><span data-ttu-id="2c5b5-160">+0</span><span class="sxs-lookup"><span data-stu-id="2c5b5-160">+0</span></span></td>
<td><span data-ttu-id="2c5b5-161">src1</span><span class="sxs-lookup"><span data-stu-id="2c5b5-161">src1</span></span></td>
<td><span data-ttu-id="2c5b5-162">+inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-162">+inf</span></span></td>
<td><span data-ttu-id="2c5b5-163">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-163">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c5b5-164"><strong>+ F</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-164"><strong>+F</strong></span></span></td>
<td><span data-ttu-id="2c5b5-165">-inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-165">-inf</span></span></td>
<td><span data-ttu-id="2c5b5-166">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="2c5b5-166">+-F or +-0</span></span></td>
<td><span data-ttu-id="2c5b5-167">src0</span><span class="sxs-lookup"><span data-stu-id="2c5b5-167">src0</span></span></td>
<td><span data-ttu-id="2c5b5-168">src0</span><span class="sxs-lookup"><span data-stu-id="2c5b5-168">src0</span></span></td>
<td><span data-ttu-id="2c5b5-169">+ F</span><span class="sxs-lookup"><span data-stu-id="2c5b5-169">+F</span></span></td>
<td><span data-ttu-id="2c5b5-170">+inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-170">+inf</span></span></td>
<td><span data-ttu-id="2c5b5-171">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-171">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c5b5-172"><strong>+ INF</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-172"><strong>+inf</strong></span></span></td>
<td><span data-ttu-id="2c5b5-173">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-173">NaN</span></span></td>
<td><span data-ttu-id="2c5b5-174">+inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-174">+inf</span></span></td>
<td><span data-ttu-id="2c5b5-175">+inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-175">+inf</span></span></td>
<td><span data-ttu-id="2c5b5-176">+inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-176">+inf</span></span></td>
<td><span data-ttu-id="2c5b5-177">+inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-177">+inf</span></span></td>
<td><span data-ttu-id="2c5b5-178">+inf</span><span class="sxs-lookup"><span data-stu-id="2c5b5-178">+inf</span></span></td>
<td><span data-ttu-id="2c5b5-179">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-179">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c5b5-180"><strong>NaN</strong></span><span class="sxs-lookup"><span data-stu-id="2c5b5-180"><strong>NaN</strong></span></span></td>
<td><span data-ttu-id="2c5b5-181">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-181">NaN</span></span></td>
<td><span data-ttu-id="2c5b5-182">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-182">NaN</span></span></td>
<td><span data-ttu-id="2c5b5-183">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-183">NaN</span></span></td>
<td><span data-ttu-id="2c5b5-184">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-184">NaN</span></span></td>
<td><span data-ttu-id="2c5b5-185">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-185">NaN</span></span></td>
<td><span data-ttu-id="2c5b5-186">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-186">NaN</span></span></td>
<td><span data-ttu-id="2c5b5-187">NaN</span><span class="sxs-lookup"><span data-stu-id="2c5b5-187">NaN</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2c5b5-188">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c5b5-188">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2c5b5-189">Vertice</span><span class="sxs-lookup"><span data-stu-id="2c5b5-189">Vertex</span></span> | <span data-ttu-id="2c5b5-190">Hull</span><span class="sxs-lookup"><span data-stu-id="2c5b5-190">Hull</span></span> | <span data-ttu-id="2c5b5-191">Dominio</span><span class="sxs-lookup"><span data-stu-id="2c5b5-191">Domain</span></span> | <span data-ttu-id="2c5b5-192">Geometria</span><span class="sxs-lookup"><span data-stu-id="2c5b5-192">Geometry</span></span> | <span data-ttu-id="2c5b5-193">Pixel</span><span class="sxs-lookup"><span data-stu-id="2c5b5-193">Pixel</span></span> | <span data-ttu-id="2c5b5-194">Calcolo</span><span class="sxs-lookup"><span data-stu-id="2c5b5-194">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2c5b5-195">X</span><span class="sxs-lookup"><span data-stu-id="2c5b5-195">X</span></span>      | <span data-ttu-id="2c5b5-196">X</span><span class="sxs-lookup"><span data-stu-id="2c5b5-196">X</span></span>    | <span data-ttu-id="2c5b5-197">X</span><span class="sxs-lookup"><span data-stu-id="2c5b5-197">X</span></span>      | <span data-ttu-id="2c5b5-198">X</span><span class="sxs-lookup"><span data-stu-id="2c5b5-198">X</span></span>        | <span data-ttu-id="2c5b5-199">X</span><span class="sxs-lookup"><span data-stu-id="2c5b5-199">X</span></span>     | <span data-ttu-id="2c5b5-200">X</span><span class="sxs-lookup"><span data-stu-id="2c5b5-200">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2c5b5-201">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="2c5b5-201">Minimum Shader Model</span></span>

<span data-ttu-id="2c5b5-202">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c5b5-202">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2c5b5-203">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2c5b5-203">Shader Model</span></span>                                              | <span data-ttu-id="2c5b5-204">Supportato</span><span class="sxs-lookup"><span data-stu-id="2c5b5-204">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2c5b5-205">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2c5b5-205">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2c5b5-206">sì</span><span class="sxs-lookup"><span data-stu-id="2c5b5-206">yes</span></span>       |
| [<span data-ttu-id="2c5b5-207">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="2c5b5-207">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2c5b5-208">no</span><span class="sxs-lookup"><span data-stu-id="2c5b5-208">no</span></span>        |
| [<span data-ttu-id="2c5b5-209">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="2c5b5-209">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2c5b5-210">no</span><span class="sxs-lookup"><span data-stu-id="2c5b5-210">no</span></span>        |
| [<span data-ttu-id="2c5b5-211">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c5b5-211">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2c5b5-212">no</span><span class="sxs-lookup"><span data-stu-id="2c5b5-212">no</span></span>        |
| [<span data-ttu-id="2c5b5-213">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c5b5-213">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2c5b5-214">no</span><span class="sxs-lookup"><span data-stu-id="2c5b5-214">no</span></span>        |
| [<span data-ttu-id="2c5b5-215">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c5b5-215">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2c5b5-216">no</span><span class="sxs-lookup"><span data-stu-id="2c5b5-216">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2c5b5-217">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c5b5-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c5b5-218">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c5b5-218">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





