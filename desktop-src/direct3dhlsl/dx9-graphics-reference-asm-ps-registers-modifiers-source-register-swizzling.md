---
title: Registro di origine swizzling (riferimenti per HLSL PS)
description: Swizzling si riferisce alla possibilità di copiare qualsiasi componente del registro di origine in qualsiasi componente di registro temporaneo. Swizzling non influisce sui dati del registro di origine. Prima dell'esecuzione di un'istruzione, i dati in un registro di origine vengono copiati in un registro temporaneo.
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ffc655129740f112a3ade9eb40c0bbe29dfc1fb
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104335684"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a><span data-ttu-id="81b8b-105">Registro di origine swizzling (riferimenti per HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="81b8b-105">Source register swizzling (HLSL PS reference)</span></span>

<span data-ttu-id="81b8b-106">Swizzling si riferisce alla possibilità di copiare qualsiasi componente del registro di origine in qualsiasi componente di registro temporaneo.</span><span class="sxs-lookup"><span data-stu-id="81b8b-106">Swizzling refers to the ability to copy any source register component to any temporary register component.</span></span> <span data-ttu-id="81b8b-107">Swizzling non influisce sui dati del registro di origine.</span><span class="sxs-lookup"><span data-stu-id="81b8b-107">Swizzling does not affect the source register data.</span></span> <span data-ttu-id="81b8b-108">Prima dell'esecuzione di un'istruzione, i dati in un registro di origine vengono copiati in un registro temporaneo.</span><span class="sxs-lookup"><span data-stu-id="81b8b-108">Before an instruction runs, the data in a source register is copied to a temporary register.</span></span>

## <a name="source-swizzling"></a><span data-ttu-id="81b8b-109">Swizzling di origine</span><span class="sxs-lookup"><span data-stu-id="81b8b-109">Source Swizzling</span></span>

<span data-ttu-id="81b8b-110">Swizzle di origine consente ai singoli componenti di un registro di origine di assumere il valore di uno dei quattro componenti dello stesso registro di origine prima che il registro venga letto per il calcolo.</span><span class="sxs-lookup"><span data-stu-id="81b8b-110">Source swizzle allows individual component of a source register to take on the value of any of the four components of the same source register before the register is read for computation.</span></span>

<span data-ttu-id="81b8b-111">Ad esempio, il zxxy swizzle significa:</span><span class="sxs-lookup"><span data-stu-id="81b8b-111">For example, the .zxxy swizzle means:</span></span>

-   <span data-ttu-id="81b8b-112">il componente. x prenderà il valore del componente. z</span><span class="sxs-lookup"><span data-stu-id="81b8b-112">.x component will take on the value of .z component</span></span>
-   <span data-ttu-id="81b8b-113">il componente. y accetta il valore del componente. x</span><span class="sxs-lookup"><span data-stu-id="81b8b-113">.y component will take on the value of .x component</span></span>
-   <span data-ttu-id="81b8b-114">il componente. z prenderà il valore del componente. x</span><span class="sxs-lookup"><span data-stu-id="81b8b-114">.z component will take on the value of .x component</span></span>
-   <span data-ttu-id="81b8b-115">il componente. w prenderà il valore del componente y</span><span class="sxs-lookup"><span data-stu-id="81b8b-115">.w component will take on the value of .y component</span></span>

<span data-ttu-id="81b8b-116">I componenti possono essere visualizzati in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="81b8b-116">The components can appear in any order.</span></span> <span data-ttu-id="81b8b-117">Se vengono specificati meno di quattro componenti, l'ultimo componente viene ripetuto.</span><span class="sxs-lookup"><span data-stu-id="81b8b-117">If fewer than four components are specified, the last component is repeated.</span></span> <span data-ttu-id="81b8b-118">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="81b8b-118">For example:</span></span>


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



<span data-ttu-id="81b8b-119">Se non viene specificato alcun componente, non viene applicato alcun swizzling.</span><span class="sxs-lookup"><span data-stu-id="81b8b-119">If no component is specified, no swizzling is applied.</span></span>

<span data-ttu-id="81b8b-120">Per alcune istruzioni sono previste restrizioni per swizzle di origine.</span><span class="sxs-lookup"><span data-stu-id="81b8b-120">Some instructions have restrictions for source swizzle.</span></span> <span data-ttu-id="81b8b-121">Sono elencate nelle pagine di riferimento all'istruzione rispettata.</span><span class="sxs-lookup"><span data-stu-id="81b8b-121">They are listed in the respected instruction reference pages.</span></span>



| <span data-ttu-id="81b8b-122">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="81b8b-122">Pixel shader versions</span></span> | <span data-ttu-id="81b8b-123">1\_1</span><span class="sxs-lookup"><span data-stu-id="81b8b-123">1\_1</span></span> | <span data-ttu-id="81b8b-124">1\_2</span><span class="sxs-lookup"><span data-stu-id="81b8b-124">1\_2</span></span> | <span data-ttu-id="81b8b-125">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="81b8b-125">1\_3</span></span> | <span data-ttu-id="81b8b-126">1\_4</span><span class="sxs-lookup"><span data-stu-id="81b8b-126">1\_4</span></span> | <span data-ttu-id="81b8b-127">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="81b8b-127">2\_0</span></span> | <span data-ttu-id="81b8b-128">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="81b8b-128">2\_x</span></span> | <span data-ttu-id="81b8b-129">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="81b8b-129">2\_sw</span></span> | <span data-ttu-id="81b8b-130">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="81b8b-130">3\_0</span></span> | <span data-ttu-id="81b8b-131">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="81b8b-131">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="81b8b-132">.x</span><span class="sxs-lookup"><span data-stu-id="81b8b-132">.x</span></span>                    |      |      |      | <span data-ttu-id="81b8b-133">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-133">x</span></span>    | <span data-ttu-id="81b8b-134">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-134">x</span></span>    | <span data-ttu-id="81b8b-135">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-135">x</span></span>    | <span data-ttu-id="81b8b-136">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-136">x</span></span>     | <span data-ttu-id="81b8b-137">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-137">x</span></span>    | <span data-ttu-id="81b8b-138">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-138">x</span></span>     |
| <span data-ttu-id="81b8b-139">. y</span><span class="sxs-lookup"><span data-stu-id="81b8b-139">.y</span></span>                    |      |      |      | <span data-ttu-id="81b8b-140">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-140">x</span></span>    | <span data-ttu-id="81b8b-141">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-141">x</span></span>    | <span data-ttu-id="81b8b-142">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-142">x</span></span>    | <span data-ttu-id="81b8b-143">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-143">x</span></span>     | <span data-ttu-id="81b8b-144">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-144">x</span></span>    | <span data-ttu-id="81b8b-145">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-145">x</span></span>     |
| <span data-ttu-id="81b8b-146">. z</span><span class="sxs-lookup"><span data-stu-id="81b8b-146">.z</span></span>                    | <span data-ttu-id="81b8b-147">x\*</span><span class="sxs-lookup"><span data-stu-id="81b8b-147">x\*</span></span>  | <span data-ttu-id="81b8b-148">x\*</span><span class="sxs-lookup"><span data-stu-id="81b8b-148">x\*</span></span>  | <span data-ttu-id="81b8b-149">x\*</span><span class="sxs-lookup"><span data-stu-id="81b8b-149">x\*</span></span>  | <span data-ttu-id="81b8b-150">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-150">x</span></span>    | <span data-ttu-id="81b8b-151">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-151">x</span></span>    | <span data-ttu-id="81b8b-152">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-152">x</span></span>    | <span data-ttu-id="81b8b-153">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-153">x</span></span>     | <span data-ttu-id="81b8b-154">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-154">x</span></span>    | <span data-ttu-id="81b8b-155">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-155">x</span></span>     |
| <span data-ttu-id="81b8b-156">. w</span><span class="sxs-lookup"><span data-stu-id="81b8b-156">.w</span></span>                    | <span data-ttu-id="81b8b-157">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-157">x</span></span>    | <span data-ttu-id="81b8b-158">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-158">x</span></span>    | <span data-ttu-id="81b8b-159">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-159">x</span></span>    | <span data-ttu-id="81b8b-160">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-160">x</span></span>    | <span data-ttu-id="81b8b-161">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-161">x</span></span>    | <span data-ttu-id="81b8b-162">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-162">x</span></span>    | <span data-ttu-id="81b8b-163">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-163">x</span></span>     | <span data-ttu-id="81b8b-164">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-164">x</span></span>    | <span data-ttu-id="81b8b-165">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-165">x</span></span>     |
| <span data-ttu-id="81b8b-166">. xyzw (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="81b8b-166">.xyzw (default)</span></span>       | <span data-ttu-id="81b8b-167">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-167">x</span></span>    | <span data-ttu-id="81b8b-168">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-168">x</span></span>    | <span data-ttu-id="81b8b-169">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-169">x</span></span>    | <span data-ttu-id="81b8b-170">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-170">x</span></span>    | <span data-ttu-id="81b8b-171">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-171">x</span></span>    | <span data-ttu-id="81b8b-172">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-172">x</span></span>    | <span data-ttu-id="81b8b-173">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-173">x</span></span>     | <span data-ttu-id="81b8b-174">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-174">x</span></span>    | <span data-ttu-id="81b8b-175">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-175">x</span></span>     |
| <span data-ttu-id="81b8b-176">.yzxw</span><span class="sxs-lookup"><span data-stu-id="81b8b-176">.yzxw</span></span>                 |      |      |      |      | <span data-ttu-id="81b8b-177">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-177">x</span></span>    | <span data-ttu-id="81b8b-178">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-178">x</span></span>    | <span data-ttu-id="81b8b-179">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-179">x</span></span>     | <span data-ttu-id="81b8b-180">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-180">x</span></span>    | <span data-ttu-id="81b8b-181">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-181">x</span></span>     |
| <span data-ttu-id="81b8b-182">.zxyw</span><span class="sxs-lookup"><span data-stu-id="81b8b-182">.zxyw</span></span>                 |      |      |      |      | <span data-ttu-id="81b8b-183">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-183">x</span></span>    | <span data-ttu-id="81b8b-184">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-184">x</span></span>    | <span data-ttu-id="81b8b-185">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-185">x</span></span>     | <span data-ttu-id="81b8b-186">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-186">x</span></span>    | <span data-ttu-id="81b8b-187">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-187">x</span></span>     |
| <span data-ttu-id="81b8b-188">.wzyx</span><span class="sxs-lookup"><span data-stu-id="81b8b-188">.wzyx</span></span>                 |      |      |      |      | <span data-ttu-id="81b8b-189">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-189">x</span></span>    | <span data-ttu-id="81b8b-190">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-190">x</span></span>    | <span data-ttu-id="81b8b-191">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-191">x</span></span>     | <span data-ttu-id="81b8b-192">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-192">x</span></span>    | <span data-ttu-id="81b8b-193">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-193">x</span></span>     |
| <span data-ttu-id="81b8b-194">swizzle arbitrario</span><span class="sxs-lookup"><span data-stu-id="81b8b-194">arbitrary swizzle</span></span>     |      |      |      |      |      | <span data-ttu-id="81b8b-195">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-195">x</span></span>    | <span data-ttu-id="81b8b-196">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-196">x</span></span>     | <span data-ttu-id="81b8b-197">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-197">x</span></span>    | <span data-ttu-id="81b8b-198">x</span><span class="sxs-lookup"><span data-stu-id="81b8b-198">x</span></span>     |



 

<span data-ttu-id="81b8b-199">\* Disponibile solo se la maschera di scrittura della destinazione è. w (. a).</span><span class="sxs-lookup"><span data-stu-id="81b8b-199">\* Only available if destination write mask is .w (.a).</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="81b8b-200">Swizzle arbitrario</span><span class="sxs-lookup"><span data-stu-id="81b8b-200">Arbitrary Swizzle</span></span>

<span data-ttu-id="81b8b-201">Swizzles può essere applicato ai registri di origine in un ordine arbitrario; ovvero qualsiasi registro di origine può assumere qualsiasi maschera di componente, in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="81b8b-201">Swizzles can be applied to source registers in an arbitrary order; that is, any source register can take any component mask, in any order.</span></span>

## <a name="replicate-swizzle"></a><span data-ttu-id="81b8b-202">Replica swizzle</span><span class="sxs-lookup"><span data-stu-id="81b8b-202">Replicate Swizzle</span></span>

<span data-ttu-id="81b8b-203">Replica swizzle copia un componente in un altro.</span><span class="sxs-lookup"><span data-stu-id="81b8b-203">Replicate swizzle copies one component to another.</span></span> <span data-ttu-id="81b8b-204">È necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).</span><span class="sxs-lookup"><span data-stu-id="81b8b-204">This is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81b8b-205">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81b8b-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81b8b-206">Modificatori del registro di origine pixel shader</span><span class="sxs-lookup"><span data-stu-id="81b8b-206">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[<span data-ttu-id="81b8b-207">PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 registri PS 1 \_ \_ \_ \_ 3 \_ \_ PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="81b8b-207">ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[<span data-ttu-id="81b8b-208">\_registri PS 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="81b8b-208">ps\_2\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[<span data-ttu-id="81b8b-209">\_registri PS 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="81b8b-209">ps\_2\_x Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[<span data-ttu-id="81b8b-210">\_registri PS 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="81b8b-210">ps\_3\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




