---
title: Assembly Shader Model 4
description: Assembly Shader Model 4
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20c7ff5d2a171228223d52db28d3bae6007068c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044751"
---
# <a name="shader-model-4-assembly"></a><span data-ttu-id="8a3e6-103">Assembly Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="8a3e6-103">Shader Model 4 Assembly</span></span>

<span data-ttu-id="8a3e6-104">Shader Model 4 richiede di programmare gli shader in HLSL.</span><span class="sxs-lookup"><span data-stu-id="8a3e6-104">Shader Model 4 requires you to program shaders in HLSL.</span></span> <span data-ttu-id="8a3e6-105">Tuttavia, il compilatore shader compila il codice HLSL nell'assembly in esecuzione nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a3e6-105">However, the shader compiler compiles the HLSL code into assembly that runs on the device.</span></span> <span data-ttu-id="8a3e6-106">Se si usa PIX per Windows per eseguire il debug degli shader, è possibile scegliere di visualizzare il codice dello shader in HLSL o assembly.</span><span class="sxs-lookup"><span data-stu-id="8a3e6-106">If you are using PIX for Windows to debug your shaders, you can choose to display shader code in either HLSL or assembly.</span></span> <span data-ttu-id="8a3e6-107">Questa sezione elenca le istruzioni di assembly Shader Model 4 e Shader Model 4,1 che possono verificarsi durante il debug di uno shader.</span><span class="sxs-lookup"><span data-stu-id="8a3e6-107">This section lists the Shader Model 4 and Shader Model 4.1 assembly instructions that you may encounter when debugging a shader.</span></span>

<dl>

[<span data-ttu-id="8a3e6-108">Modificatori di istruzione</span><span class="sxs-lookup"><span data-stu-id="8a3e6-108">Instruction Modifiers</span></span>](instruction-modifiers.md)  
[<span data-ttu-id="8a3e6-109">add</span><span class="sxs-lookup"><span data-stu-id="8a3e6-109">add</span></span>](add--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-110">and</span><span class="sxs-lookup"><span data-stu-id="8a3e6-110">and</span></span>](and--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-111">break</span><span class="sxs-lookup"><span data-stu-id="8a3e6-111">break</span></span>](break--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-112">breakc</span><span class="sxs-lookup"><span data-stu-id="8a3e6-112">breakc</span></span>](breakc--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-113">call</span><span class="sxs-lookup"><span data-stu-id="8a3e6-113">call</span></span>](call--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-114">callc</span><span class="sxs-lookup"><span data-stu-id="8a3e6-114">callc</span></span>](callc--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-115">case</span><span class="sxs-lookup"><span data-stu-id="8a3e6-115">case</span></span>](case--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-116">continuare</span><span class="sxs-lookup"><span data-stu-id="8a3e6-116">continue</span></span>](continue--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-117">continuec</span><span class="sxs-lookup"><span data-stu-id="8a3e6-117">continuec</span></span>](continuec--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-118">tagliare</span><span class="sxs-lookup"><span data-stu-id="8a3e6-118">cut</span></span>](cut--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-119">\_constantBuffer DCL</span><span class="sxs-lookup"><span data-stu-id="8a3e6-119">dcl\_constantBuffer</span></span>](dcl-constantbuffer.md)  
[<span data-ttu-id="8a3e6-120">\_globalFlags DCL</span><span class="sxs-lookup"><span data-stu-id="8a3e6-120">dcl\_globalFlags</span></span>](dcl-globalflags.md)  
[<span data-ttu-id="8a3e6-121">\_immediateConstantBuffer DCL</span><span class="sxs-lookup"><span data-stu-id="8a3e6-121">dcl\_immediateConstantBuffer</span></span>](dcl-immediateconstantbuffer.md)  
[<span data-ttu-id="8a3e6-122">\_indexableTemp DCL</span><span class="sxs-lookup"><span data-stu-id="8a3e6-122">dcl\_indexableTemp</span></span>](dcl-indexabletemp.md)  
[<span data-ttu-id="8a3e6-123">\_indexRange DCL</span><span class="sxs-lookup"><span data-stu-id="8a3e6-123">dcl\_indexRange</span></span>](dcl-indexrange.md)  
[<span data-ttu-id="8a3e6-124">\_input DCL</span><span class="sxs-lookup"><span data-stu-id="8a3e6-124">dcl\_input</span></span>](dcl-input.md)  
[<span data-ttu-id="8a3e6-125">\_input DCL \_ SV</span><span class="sxs-lookup"><span data-stu-id="8a3e6-125">dcl\_input\_sv</span></span>](dcl-input-sv.md)  
[<span data-ttu-id="8a3e6-126">\_vPrim di input DCL</span><span class="sxs-lookup"><span data-stu-id="8a3e6-126">dcl\_input vPrim</span></span>](dcl-input-vprim.md)  
[<span data-ttu-id="8a3e6-127">\_maxOutputVertexCount DCL</span><span class="sxs-lookup"><span data-stu-id="8a3e6-127">dcl\_maxOutputVertexCount</span></span>](dcl-maxoutputvertexcount.md)  
[<span data-ttu-id="8a3e6-128">output di DCL \_</span><span class="sxs-lookup"><span data-stu-id="8a3e6-128">dcl\_output</span></span>](dcl-output.md)  
[<span data-ttu-id="8a3e6-129">\_oDepth output \_ DCL</span><span class="sxs-lookup"><span data-stu-id="8a3e6-129">dcl\_output\_oDepth</span></span>](dcl-output-odepth.md)  
[<span data-ttu-id="8a3e6-130">\_SGV output \_ DCL</span><span class="sxs-lookup"><span data-stu-id="8a3e6-130">dcl\_output\_sgv</span></span>](dcl-output-sgv.md)  
[<span data-ttu-id="8a3e6-131">\_SIV output di DCL \_</span><span class="sxs-lookup"><span data-stu-id="8a3e6-131">dcl\_output\_siv</span></span>](dcl-output-siv.md)  
[<span data-ttu-id="8a3e6-132">\_outputTopology DCL</span><span class="sxs-lookup"><span data-stu-id="8a3e6-132">dcl\_outputTopology</span></span>](dcl-outputtopology.md)  
[<span data-ttu-id="8a3e6-133">\_risorsa DCL</span><span class="sxs-lookup"><span data-stu-id="8a3e6-133">dcl\_resource</span></span>](dcl-resource.md)  
[<span data-ttu-id="8a3e6-134">\_campionatore DCL</span><span class="sxs-lookup"><span data-stu-id="8a3e6-134">dcl\_sampler</span></span>](dcl-sampler.md)  
[<span data-ttu-id="8a3e6-135">Temp di DCL \_</span><span class="sxs-lookup"><span data-stu-id="8a3e6-135">dcl\_temps</span></span>](dcl-temps.md)  
[<span data-ttu-id="8a3e6-136">default</span><span class="sxs-lookup"><span data-stu-id="8a3e6-136">default</span></span>](default--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-137">derivazione \_ RTX</span><span class="sxs-lookup"><span data-stu-id="8a3e6-137">deriv\_rtx</span></span>](deriv-rtx--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-138">derivazione \_ valore</span><span class="sxs-lookup"><span data-stu-id="8a3e6-138">deriv\_rty</span></span>](deriv-rty--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-139">rimuovere</span><span class="sxs-lookup"><span data-stu-id="8a3e6-139">discard</span></span>](discard--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-140">div</span><span class="sxs-lookup"><span data-stu-id="8a3e6-140">div</span></span>](div--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-141">DP2</span><span class="sxs-lookup"><span data-stu-id="8a3e6-141">dp2</span></span>](dp2--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-142">dp3</span><span class="sxs-lookup"><span data-stu-id="8a3e6-142">dp3</span></span>](dp3--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-143">DP4</span><span class="sxs-lookup"><span data-stu-id="8a3e6-143">dp4</span></span>](dp4--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-144">else</span><span class="sxs-lookup"><span data-stu-id="8a3e6-144">else</span></span>](else--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-145">Emit</span><span class="sxs-lookup"><span data-stu-id="8a3e6-145">emit</span></span>](emit--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-146">emitThenCut</span><span class="sxs-lookup"><span data-stu-id="8a3e6-146">emitThenCut</span></span>](emitthencut--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-147">endif</span><span class="sxs-lookup"><span data-stu-id="8a3e6-147">endif</span></span>](endif--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-148">endloop</span><span class="sxs-lookup"><span data-stu-id="8a3e6-148">endloop</span></span>](endloop--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-149">endswitch</span><span class="sxs-lookup"><span data-stu-id="8a3e6-149">endswitch</span></span>](endswitch--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-150">eq</span><span class="sxs-lookup"><span data-stu-id="8a3e6-150">eq</span></span>](eq--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-151">exp</span><span class="sxs-lookup"><span data-stu-id="8a3e6-151">exp</span></span>](exp--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-152">FRC</span><span class="sxs-lookup"><span data-stu-id="8a3e6-152">frc</span></span>](frc--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-153">ftoi</span><span class="sxs-lookup"><span data-stu-id="8a3e6-153">ftoi</span></span>](ftoi--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-154">ftou</span><span class="sxs-lookup"><span data-stu-id="8a3e6-154">ftou</span></span>](ftou--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-155">ge</span><span class="sxs-lookup"><span data-stu-id="8a3e6-155">ge</span></span>](ge--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-156">IAdd</span><span class="sxs-lookup"><span data-stu-id="8a3e6-156">iadd</span></span>](iadd--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-157">ibfe</span><span class="sxs-lookup"><span data-stu-id="8a3e6-157">ibfe</span></span>](dne--sm5---asm-.md)  
[<span data-ttu-id="8a3e6-158">IEQ</span><span class="sxs-lookup"><span data-stu-id="8a3e6-158">ieq</span></span>](ieq--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-159">if</span><span class="sxs-lookup"><span data-stu-id="8a3e6-159">if</span></span>](if--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-160">IgE</span><span class="sxs-lookup"><span data-stu-id="8a3e6-160">ige</span></span>](ige--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-161">ILT</span><span class="sxs-lookup"><span data-stu-id="8a3e6-161">ilt</span></span>](ilt--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-162">imad</span><span class="sxs-lookup"><span data-stu-id="8a3e6-162">imad</span></span>](imad--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-163">Imin</span><span class="sxs-lookup"><span data-stu-id="8a3e6-163">imin</span></span>](imin--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-164">IMUL</span><span class="sxs-lookup"><span data-stu-id="8a3e6-164">imul</span></span>](imul--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-165">ine</span><span class="sxs-lookup"><span data-stu-id="8a3e6-165">ine</span></span>](ine--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-166">ineg</span><span class="sxs-lookup"><span data-stu-id="8a3e6-166">ineg</span></span>](ineg--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-167">ishl</span><span class="sxs-lookup"><span data-stu-id="8a3e6-167">ishl</span></span>](ishl--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-168">ISHR</span><span class="sxs-lookup"><span data-stu-id="8a3e6-168">ishr</span></span>](ishr--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-169">itof</span><span class="sxs-lookup"><span data-stu-id="8a3e6-169">itof</span></span>](itof--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-170">label</span><span class="sxs-lookup"><span data-stu-id="8a3e6-170">label</span></span>](label--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-171">LD</span><span class="sxs-lookup"><span data-stu-id="8a3e6-171">ld</span></span>](ld--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-172">log</span><span class="sxs-lookup"><span data-stu-id="8a3e6-172">log</span></span>](log--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-173">loop</span><span class="sxs-lookup"><span data-stu-id="8a3e6-173">loop</span></span>](loop--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-174">lt</span><span class="sxs-lookup"><span data-stu-id="8a3e6-174">lt</span></span>](lt--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-175">pazzo</span><span class="sxs-lookup"><span data-stu-id="8a3e6-175">mad</span></span>](mad--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-176">max</span><span class="sxs-lookup"><span data-stu-id="8a3e6-176">max</span></span>](max--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-177">min</span><span class="sxs-lookup"><span data-stu-id="8a3e6-177">min</span></span>](min--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-178">MOV</span><span class="sxs-lookup"><span data-stu-id="8a3e6-178">mov</span></span>](mov--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-179">movc</span><span class="sxs-lookup"><span data-stu-id="8a3e6-179">movc</span></span>](movc--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-180">mul</span><span class="sxs-lookup"><span data-stu-id="8a3e6-180">mul</span></span>](mul--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-181">ne</span><span class="sxs-lookup"><span data-stu-id="8a3e6-181">ne</span></span>](ne--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-182">NOP</span><span class="sxs-lookup"><span data-stu-id="8a3e6-182">nop</span></span>](nop--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-183">not</span><span class="sxs-lookup"><span data-stu-id="8a3e6-183">not</span></span>](not--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-184">or</span><span class="sxs-lookup"><span data-stu-id="8a3e6-184">or</span></span>](or--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-185">ResInfo</span><span class="sxs-lookup"><span data-stu-id="8a3e6-185">resinfo</span></span>](resinfo--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-186">RET</span><span class="sxs-lookup"><span data-stu-id="8a3e6-186">ret</span></span>](ret--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-187">retc</span><span class="sxs-lookup"><span data-stu-id="8a3e6-187">retc</span></span>](retc--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-188">Round \_ ne</span><span class="sxs-lookup"><span data-stu-id="8a3e6-188">round\_ne</span></span>](round-ne--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-189">Round \_ NI</span><span class="sxs-lookup"><span data-stu-id="8a3e6-189">round\_ni</span></span>](round-ni--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-190">Round \_ pi</span><span class="sxs-lookup"><span data-stu-id="8a3e6-190">round\_pi</span></span>](round-pi--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-191">Round \_ z</span><span class="sxs-lookup"><span data-stu-id="8a3e6-191">round\_z</span></span>](round-z--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-192">RSQ</span><span class="sxs-lookup"><span data-stu-id="8a3e6-192">rsq</span></span>](rsq--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-193">esempio</span><span class="sxs-lookup"><span data-stu-id="8a3e6-193">sample</span></span>](sample--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-194">esempio \_ b</span><span class="sxs-lookup"><span data-stu-id="8a3e6-194">sample\_b</span></span>](sample-b--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-195">esempio \_ c</span><span class="sxs-lookup"><span data-stu-id="8a3e6-195">sample\_c</span></span>](sample-c--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-196">esempio \_ c \_ LZ</span><span class="sxs-lookup"><span data-stu-id="8a3e6-196">sample\_c\_lz</span></span>](sample-c-lz--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-197">esempio \_ d</span><span class="sxs-lookup"><span data-stu-id="8a3e6-197">sample\_d</span></span>](sample-d--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-198">esempio \_ l</span><span class="sxs-lookup"><span data-stu-id="8a3e6-198">sample\_l</span></span>](sample-l--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-199">SinCos</span><span class="sxs-lookup"><span data-stu-id="8a3e6-199">sincos</span></span>](sincos--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-200">sqrt</span><span class="sxs-lookup"><span data-stu-id="8a3e6-200">sqrt</span></span>](sqrt--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-201">switch</span><span class="sxs-lookup"><span data-stu-id="8a3e6-201">switch</span></span>](switch--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-202">udiv</span><span class="sxs-lookup"><span data-stu-id="8a3e6-202">udiv</span></span>](udiv--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-203">uge</span><span class="sxs-lookup"><span data-stu-id="8a3e6-203">uge</span></span>](uge--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-204">Ultimate</span><span class="sxs-lookup"><span data-stu-id="8a3e6-204">ult</span></span>](ult--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-205">Martina</span><span class="sxs-lookup"><span data-stu-id="8a3e6-205">umad</span></span>](umad--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-206">Umax</span><span class="sxs-lookup"><span data-stu-id="8a3e6-206">umax</span></span>](umax--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-207">Umin</span><span class="sxs-lookup"><span data-stu-id="8a3e6-207">umin</span></span>](umin--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-208">umul</span><span class="sxs-lookup"><span data-stu-id="8a3e6-208">umul</span></span>](umul--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-209">ushr</span><span class="sxs-lookup"><span data-stu-id="8a3e6-209">ushr</span></span>](ushr--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-210">utof</span><span class="sxs-lookup"><span data-stu-id="8a3e6-210">utof</span></span>](utof--sm4---asm-.md)  
[<span data-ttu-id="8a3e6-211">XOR</span><span class="sxs-lookup"><span data-stu-id="8a3e6-211">xor</span></span>](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a><span data-ttu-id="8a3e6-212">Assembly del modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="8a3e6-212">Shader Model 4.1 Assembly</span></span>

<span data-ttu-id="8a3e6-213">Il modello di Shader 4,1 supporta tutte le istruzioni per il modello di Shader 4,0 e le istruzioni aggiuntive seguenti:</span><span class="sxs-lookup"><span data-stu-id="8a3e6-213">Shader Model 4.1 supports all of the Shader Model 4.0 instructions and the following additional instructions:</span></span>

<dl>

[<span data-ttu-id="8a3e6-214">gather4</span><span class="sxs-lookup"><span data-stu-id="8a3e6-214">gather4</span></span>](gather4--sm4-1---asm-.md)  
[<span data-ttu-id="8a3e6-215">ld2dms</span><span class="sxs-lookup"><span data-stu-id="8a3e6-215">ld2dms</span></span>](ld2dms--sm4-1---asm-.md)  
[<span data-ttu-id="8a3e6-216">trama</span><span class="sxs-lookup"><span data-stu-id="8a3e6-216">lod</span></span>](lod--sm4-1---asm-.md)  
[<span data-ttu-id="8a3e6-217">sampleinfo</span><span class="sxs-lookup"><span data-stu-id="8a3e6-217">sampleinfo</span></span>](sampleinfo--sm4-1---asm-.md)  
[<span data-ttu-id="8a3e6-218">samplepos</span><span class="sxs-lookup"><span data-stu-id="8a3e6-218">samplepos</span></span>](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="8a3e6-219">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a3e6-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a3e6-220">Informazioni di riferimento su ASM shader</span><span class="sxs-lookup"><span data-stu-id="8a3e6-220">Asm Shader Reference</span></span>](dx9-graphics-reference-asm.md)
</dt> <dt>

[<span data-ttu-id="8a3e6-221">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="8a3e6-221">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




