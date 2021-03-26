---
title: Maschera di scrittura registro di destinazione
description: Una maschera di scrittura controlla i componenti di un registro di destinazione che vengono scritti dopo il completamento di un'istruzione.
ms.assetid: 376a28c8-8a88-4807-a8ab-f59448d965e8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f649770b84174dbb716967e9d941034c3966f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955839"
---
# <a name="destination-register-write-mask"></a><span data-ttu-id="41360-103">Maschera di scrittura registro di destinazione</span><span class="sxs-lookup"><span data-stu-id="41360-103">Destination Register Write Mask</span></span>

<span data-ttu-id="41360-104">Una maschera di scrittura controlla i componenti di un registro di destinazione che vengono scritti dopo il completamento di un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="41360-104">A write mask controls which components of a destination register are written after an instruction is completed.</span></span> <span data-ttu-id="41360-105">È consentita una maschera di scrittura di output purché i componenti si trovino nell'ordine di. RGBA o. xyzw.</span><span class="sxs-lookup"><span data-stu-id="41360-105">An output write mask is allowed as long as the components are in the order of .rgba or .xyzw.</span></span> <span data-ttu-id="41360-106">Ovvero. RBA e. XW sono maschere valide.</span><span class="sxs-lookup"><span data-stu-id="41360-106">That is, .rba and .xw are valid masks.</span></span> <span data-ttu-id="41360-107">I registri di trama includono un set di regole e registri non di trama hanno un altro set di regole.</span><span class="sxs-lookup"><span data-stu-id="41360-107">Texture registers have one set of rules and non-texture registers have another set of rules.</span></span>

## <a name="syntax"></a><span data-ttu-id="41360-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41360-108">Syntax</span></span>



| <span data-ttu-id="41360-109">DST. writemask</span><span class="sxs-lookup"><span data-stu-id="41360-109">dst.writemask</span></span> |
|---------------|



 

<span data-ttu-id="41360-110">dove</span><span class="sxs-lookup"><span data-stu-id="41360-110">where</span></span>

-   <span data-ttu-id="41360-111">DST è un registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="41360-111">dst is a destination register.</span></span>
-   <span data-ttu-id="41360-112">writemask è una sequenza di maschere da entrambi i set: (x, y, z, w) o (rosso, verde, blu, alfa).</span><span class="sxs-lookup"><span data-stu-id="41360-112">writemask is a sequence of masks from either set: (x,y,z,w) or (red, green, blue, alpha).</span></span>

## <a name="remarks"></a><span data-ttu-id="41360-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="41360-113">Remarks</span></span>

<span data-ttu-id="41360-114">Sono disponibili le seguenti maschere di scrittura di destinazione.</span><span class="sxs-lookup"><span data-stu-id="41360-114">The following destination write masks are available.</span></span>



| <span data-ttu-id="41360-115">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="41360-115">Pixel shader versions</span></span> | <span data-ttu-id="41360-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="41360-116">1\_1</span></span> | <span data-ttu-id="41360-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="41360-117">1\_2</span></span> | <span data-ttu-id="41360-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="41360-118">1\_3</span></span> | <span data-ttu-id="41360-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="41360-119">1\_4</span></span> | <span data-ttu-id="41360-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="41360-120">2\_0</span></span> | <span data-ttu-id="41360-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="41360-121">2\_x</span></span> | <span data-ttu-id="41360-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="41360-122">2\_sw</span></span> | <span data-ttu-id="41360-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="41360-123">3\_0</span></span> | <span data-ttu-id="41360-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="41360-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="41360-125">. xyzw (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41360-125">.xyzw (default)</span></span>       | <span data-ttu-id="41360-126">x</span><span class="sxs-lookup"><span data-stu-id="41360-126">x</span></span>    | <span data-ttu-id="41360-127">x</span><span class="sxs-lookup"><span data-stu-id="41360-127">x</span></span>    | <span data-ttu-id="41360-128">x</span><span class="sxs-lookup"><span data-stu-id="41360-128">x</span></span>    | <span data-ttu-id="41360-129">x</span><span class="sxs-lookup"><span data-stu-id="41360-129">x</span></span>    | <span data-ttu-id="41360-130">x</span><span class="sxs-lookup"><span data-stu-id="41360-130">x</span></span>    | <span data-ttu-id="41360-131">x</span><span class="sxs-lookup"><span data-stu-id="41360-131">x</span></span>    | <span data-ttu-id="41360-132">x</span><span class="sxs-lookup"><span data-stu-id="41360-132">x</span></span>     | <span data-ttu-id="41360-133">x</span><span class="sxs-lookup"><span data-stu-id="41360-133">x</span></span>    | <span data-ttu-id="41360-134">x</span><span class="sxs-lookup"><span data-stu-id="41360-134">x</span></span>     |
| <span data-ttu-id="41360-135">. xyz</span><span class="sxs-lookup"><span data-stu-id="41360-135">.xyz</span></span>                  | <span data-ttu-id="41360-136">x</span><span class="sxs-lookup"><span data-stu-id="41360-136">x</span></span>    | <span data-ttu-id="41360-137">x</span><span class="sxs-lookup"><span data-stu-id="41360-137">x</span></span>    | <span data-ttu-id="41360-138">x</span><span class="sxs-lookup"><span data-stu-id="41360-138">x</span></span>    | <span data-ttu-id="41360-139">x</span><span class="sxs-lookup"><span data-stu-id="41360-139">x</span></span>    | <span data-ttu-id="41360-140">x</span><span class="sxs-lookup"><span data-stu-id="41360-140">x</span></span>    | <span data-ttu-id="41360-141">x</span><span class="sxs-lookup"><span data-stu-id="41360-141">x</span></span>    | <span data-ttu-id="41360-142">x</span><span class="sxs-lookup"><span data-stu-id="41360-142">x</span></span>     | <span data-ttu-id="41360-143">x</span><span class="sxs-lookup"><span data-stu-id="41360-143">x</span></span>    | <span data-ttu-id="41360-144">x</span><span class="sxs-lookup"><span data-stu-id="41360-144">x</span></span>     |
| <span data-ttu-id="41360-145">. w</span><span class="sxs-lookup"><span data-stu-id="41360-145">.w</span></span>                    | <span data-ttu-id="41360-146">x</span><span class="sxs-lookup"><span data-stu-id="41360-146">x</span></span>    | <span data-ttu-id="41360-147">x</span><span class="sxs-lookup"><span data-stu-id="41360-147">x</span></span>    | <span data-ttu-id="41360-148">x</span><span class="sxs-lookup"><span data-stu-id="41360-148">x</span></span>    | <span data-ttu-id="41360-149">x</span><span class="sxs-lookup"><span data-stu-id="41360-149">x</span></span>    | <span data-ttu-id="41360-150">x</span><span class="sxs-lookup"><span data-stu-id="41360-150">x</span></span>    | <span data-ttu-id="41360-151">x</span><span class="sxs-lookup"><span data-stu-id="41360-151">x</span></span>    | <span data-ttu-id="41360-152">x</span><span class="sxs-lookup"><span data-stu-id="41360-152">x</span></span>     | <span data-ttu-id="41360-153">x</span><span class="sxs-lookup"><span data-stu-id="41360-153">x</span></span>    | <span data-ttu-id="41360-154">x</span><span class="sxs-lookup"><span data-stu-id="41360-154">x</span></span>     |
| <span data-ttu-id="41360-155">maschera arbitraria</span><span class="sxs-lookup"><span data-stu-id="41360-155">arbitrary mask</span></span>        |      |      |      | <span data-ttu-id="41360-156">x</span><span class="sxs-lookup"><span data-stu-id="41360-156">x</span></span>    | <span data-ttu-id="41360-157">x</span><span class="sxs-lookup"><span data-stu-id="41360-157">x</span></span>    | <span data-ttu-id="41360-158">x</span><span class="sxs-lookup"><span data-stu-id="41360-158">x</span></span>    | <span data-ttu-id="41360-159">x</span><span class="sxs-lookup"><span data-stu-id="41360-159">x</span></span>     | <span data-ttu-id="41360-160">x</span><span class="sxs-lookup"><span data-stu-id="41360-160">x</span></span>    | <span data-ttu-id="41360-161">x</span><span class="sxs-lookup"><span data-stu-id="41360-161">x</span></span>     |



 

<span data-ttu-id="41360-162">La maschera arbitraria consente di combinare qualsiasi set di canali per produrre una maschera.</span><span class="sxs-lookup"><span data-stu-id="41360-162">The arbitrary mask allows any set of channels to be combined to produce a mask.</span></span> <span data-ttu-id="41360-163">I canali devono essere elencati nell'ordine r, g, b, a, ad esempio Register. RBA, che aggiorna i canali rosso, blu e alfa della destinazione.</span><span class="sxs-lookup"><span data-stu-id="41360-163">The channels must be listed in the order r, g, b, a - for example, register.rba, which updates the red, blue, and alpha channels of the destination.</span></span> <span data-ttu-id="41360-164">La maschera arbitraria è disponibile nella versione 1 \_ 4 o successiva.</span><span class="sxs-lookup"><span data-stu-id="41360-164">The arbitrary mask is available in version 1\_4 or higher.</span></span>

<span data-ttu-id="41360-165">Se non viene specificata alcuna maschera di scrittura di destinazione, per impostazione predefinita viene applicata la maschera di scrittura di destinazione al case RGBA.</span><span class="sxs-lookup"><span data-stu-id="41360-165">If no destination write mask is specified, the destination write mask defaults to the rgba case.</span></span> <span data-ttu-id="41360-166">In altre parole, vengono aggiornati tutti i canali nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="41360-166">In other words, all channels in the destination register are updated.</span></span>

<span data-ttu-id="41360-167">Per le versioni \_ da 1 0 a 1 \_ 3, l'istruzione aritmetica [DP3-PS](dp3---ps.md) DP3 può usare solo le maschere di scrittura dell'output con estensione RGB o RGBA.</span><span class="sxs-lookup"><span data-stu-id="41360-167">For versions 1\_0 to 1\_3, the [dp3 - ps](dp3---ps.md) dp3 arithmetic instruction can use only the .rgb or .rgba output write masks.</span></span>

<span data-ttu-id="41360-168">Le maschere di scrittura del registro di destinazione sono supportate solo per operazioni aritmetiche.</span><span class="sxs-lookup"><span data-stu-id="41360-168">Destination register write masks are supported for arithmetic operations only.</span></span> <span data-ttu-id="41360-169">Non possono essere usati nelle istruzioni per l'indirizzamento delle trame, fatta eccezione per le istruzioni della versione 1 \_ 4, [texcrd-PS](texcrd---ps.md) e [texld-PS \_ 2 \_ 0](texld---ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="41360-169">They cannot be used on texture addressing instructions, with the exception of the version 1\_4 instructions, [texcrd - ps](texcrd---ps.md) and [texld - ps\_2\_0 and up](texld---ps-2-0.md).</span></span>

<span data-ttu-id="41360-170">Per impostazione predefinita, vengono scritti tutti e quattro i canali colori.</span><span class="sxs-lookup"><span data-stu-id="41360-170">The default is to write all four color channels.</span></span>


```
// All four color channels can be written by explicitly listing them.
mul r0.rgba, t0, v0

// Or, the default mask can be used to write all four channels.
mul r0, t0, v0
```



<span data-ttu-id="41360-171">La maschera di scrittura alfa è detta anche maschera di scrittura scalare, perché usa la pipeline scalare.</span><span class="sxs-lookup"><span data-stu-id="41360-171">The alpha write mask is also referred to as the scalar write mask, because it uses the scalar pipeline.</span></span>


```
add r0.a, t1, v1
```



<span data-ttu-id="41360-172">Quindi, questa istruzione inserisce in modo efficace la somma del componente alfa di T1 e del componente alfa di V1 in r0. a.</span><span class="sxs-lookup"><span data-stu-id="41360-172">So this instruction effectively puts the sum of the alpha component of t1 and the alpha component of v1 into r0.a.</span></span>

<span data-ttu-id="41360-173">La maschera di scrittura colori viene utilizzata per controllare la scrittura nei canali dei colori.</span><span class="sxs-lookup"><span data-stu-id="41360-173">The color write mask is used to control writing to the color channels.</span></span>


```
// The color write mask is also referred to as the vector write mask, 
//   because it uses the vector pipeline.
mul r0.rgb, t0, v0
```



<span data-ttu-id="41360-174">Per la versione 1 \_ 4, le maschere di scrittura di destinazione possono essere usate in qualsiasi combinazione purché le maschere siano ordinate come r, g, b, a.</span><span class="sxs-lookup"><span data-stu-id="41360-174">For version 1\_4, destination write masks can be used in any combination as long as the masks are ordered r,g,b,a.</span></span>


```
// This example updates the red, blue, and alpha channels.
mov r0.rba, r1
```



<span data-ttu-id="41360-175">Un'istruzione co-emesso consente di emettere due istruzioni potenzialmente diverse contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="41360-175">A co-issued instruction allows two potentially different instructions to be issued simultaneously.</span></span> <span data-ttu-id="41360-176">Questa operazione viene eseguita eseguendo le istruzioni della pipeline Alpha e della pipeline RGB.</span><span class="sxs-lookup"><span data-stu-id="41360-176">This is accomplished by executing the instructions in the alpha pipeline and the RGB pipeline.</span></span>


```
  mul r0.rgb, t0, v0
+ add r1.a,   t1, c1
```



<span data-ttu-id="41360-177">Il vantaggio di abbinare le istruzioni in questo modo è che consente di eseguire diverse operazioni nella pipeline vettoriale e scalare in parallelo.</span><span class="sxs-lookup"><span data-stu-id="41360-177">The advantage of pairing instructions this way is that it allows different operations to be performed in the vector and scalar pipeline in parallel.</span></span>

<span data-ttu-id="41360-178">Questi registri di output del vertex shader sono limitati alle seguenti maschere di scrittura:</span><span class="sxs-lookup"><span data-stu-id="41360-178">These vertex shader output registers are restricted to the following write masks:</span></span>



| <span data-ttu-id="41360-179">Tipo di registro</span><span class="sxs-lookup"><span data-stu-id="41360-179">Register Type</span></span> | <span data-ttu-id="41360-180">Maschera di scrittura obbligatoria</span><span class="sxs-lookup"><span data-stu-id="41360-180">Required Write Mask</span></span>                                              |
|---------------|------------------------------------------------------------------|
| <span data-ttu-id="41360-181">oFog</span><span class="sxs-lookup"><span data-stu-id="41360-181">oFog</span></span>          | <span data-ttu-id="41360-182">Nessuna maschera di scrittura esplicita consentita in questo registro scalare</span><span class="sxs-lookup"><span data-stu-id="41360-182">no explicit write mask is allowed on this scalar register</span></span>        |
| <span data-ttu-id="41360-183">oPts</span><span class="sxs-lookup"><span data-stu-id="41360-183">oPts</span></span>          | <span data-ttu-id="41360-184">Nessuna maschera di scrittura esplicita consentita in questo registro scalare</span><span class="sxs-lookup"><span data-stu-id="41360-184">no explicit write mask is allowed on this scalar register</span></span>        |
| <span data-ttu-id="41360-185">oPos</span><span class="sxs-lookup"><span data-stu-id="41360-185">oPos</span></span>          | <span data-ttu-id="41360-186">. xyzw (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41360-186">.xyzw(which is the default)</span></span>                                      |
| <span data-ttu-id="41360-187">oT\#</span><span class="sxs-lookup"><span data-stu-id="41360-187">oT\#</span></span>          | <span data-ttu-id="41360-188">maschera combinata:. x \| . XY \| . xyz \| . xyzw (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41360-188">combined mask: .x \| .xy \| .xyz \| .xyzw (which is the default)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="41360-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41360-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41360-190">Modificatori del registro pixel shader</span><span class="sxs-lookup"><span data-stu-id="41360-190">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




