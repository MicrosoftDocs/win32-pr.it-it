---
title: Differenze di pixel shader
description: Differenze di pixel shader
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a74b5cc7588220fdc5173c470f7852ee9ef763d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399212"
---
# <a name="pixel-shader-differences"></a><span data-ttu-id="153de-103">Differenze di pixel shader</span><span class="sxs-lookup"><span data-stu-id="153de-103">Pixel Shader Differences</span></span>

## <a name="instruction-slots"></a><span data-ttu-id="153de-104">Slot di istruzioni</span><span class="sxs-lookup"><span data-stu-id="153de-104">Instruction Slots</span></span>

<span data-ttu-id="153de-105">Ogni versione supporta un numero diverso di slot di istruzioni massime.</span><span class="sxs-lookup"><span data-stu-id="153de-105">Each version supports a different number of maximum instruction slots.</span></span>



| <span data-ttu-id="153de-106">Versione</span><span class="sxs-lookup"><span data-stu-id="153de-106">Version</span></span>  | <span data-ttu-id="153de-107">Numero massimo di slot di istruzioni</span><span class="sxs-lookup"><span data-stu-id="153de-107">Maximum number of instruction slots</span></span>                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="153de-108">PS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="153de-108">ps\_1\_1</span></span> | <span data-ttu-id="153de-109">4 trama + 8 aritmetica</span><span class="sxs-lookup"><span data-stu-id="153de-109">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="153de-110">PS \_ 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="153de-110">ps\_1\_2</span></span> | <span data-ttu-id="153de-111">4 trama + 8 aritmetica</span><span class="sxs-lookup"><span data-stu-id="153de-111">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="153de-112">PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="153de-112">ps\_1\_3</span></span> | <span data-ttu-id="153de-113">4 trama + 8 aritmetica</span><span class="sxs-lookup"><span data-stu-id="153de-113">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="153de-114">PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="153de-114">ps\_1\_4</span></span> | <span data-ttu-id="153de-115">6 trama + 8 aritmetico per fase</span><span class="sxs-lookup"><span data-stu-id="153de-115">6 texture + 8 arithmetic per phase</span></span>                                                                                    |
| <span data-ttu-id="153de-116">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="153de-116">ps\_2\_0</span></span> | <span data-ttu-id="153de-117">32 trama + 64 aritmetico</span><span class="sxs-lookup"><span data-stu-id="153de-117">32 texture + 64 arithmetic</span></span>                                                                                            |
| <span data-ttu-id="153de-118">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="153de-118">ps\_2\_x</span></span> | <span data-ttu-id="153de-119">96 minimo e fino al numero di slot in D3DCAPS9. D3DPSHADERCAPS2 \_ 0. NumInstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="153de-119">96 minimum, and up to the number of slots in D3DCAPS9.D3DPSHADERCAPS2\_0.NumInstructionSlots.</span></span> <span data-ttu-id="153de-120">Vedere D3DPSHADERCAPS2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="153de-120">See D3DPSHADERCAPS2\_0.</span></span> |
| <span data-ttu-id="153de-121">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="153de-121">ps\_3\_0</span></span> | <span data-ttu-id="153de-122">512 minimo e fino al numero di slot in D3DCAPS9. MaxPixelShader30InstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="153de-122">512 minimum, and up to the number of slots in D3DCAPS9.MaxPixelShader30InstructionSlots.</span></span> <span data-ttu-id="153de-123">Vedere D3DPSHADERCAPS2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="153de-123">See D3DPSHADERCAPS2\_0.</span></span>      |



 

<span data-ttu-id="153de-124">Per informazioni sulle limitazioni degli shader software, vedere [software shaders](dx9-graphics-reference-asm-software-shaders.md).</span><span class="sxs-lookup"><span data-stu-id="153de-124">For information about the limitations of software shaders, see [Software Shaders](dx9-graphics-reference-asm-software-shaders.md).</span></span>

## <a name="flow-control-nesting-limits"></a><span data-ttu-id="153de-125">Limiti di nidificazione del controllo di flusso</span><span class="sxs-lookup"><span data-stu-id="153de-125">Flow Control Nesting Limits</span></span>

-   <span data-ttu-id="153de-126">Vedere [limitazioni del controllo di flusso](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="153de-126">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>

## <a name="ps_1_x-features"></a><span data-ttu-id="153de-127">Funzionalità di PS \_ 1 \_ x</span><span class="sxs-lookup"><span data-stu-id="153de-127">ps\_1\_x Features</span></span>

<span data-ttu-id="153de-128">Nuove istruzioni:</span><span class="sxs-lookup"><span data-stu-id="153de-128">New instructions:</span></span>

<span data-ttu-id="153de-129">Vedere [ \_ \_ le istruzioni PS 1 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="153de-129">See [ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).</span></span>

<span data-ttu-id="153de-130">Nuovi registri:</span><span class="sxs-lookup"><span data-stu-id="153de-130">New registers:</span></span>

<span data-ttu-id="153de-131">Vedere i registri PS 1 [ \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS 1 \_ \_ 3 \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="153de-131">See [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="ps_2_0-features"></a><span data-ttu-id="153de-132">Funzionalità di PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="153de-132">ps\_2\_0 Features</span></span>

<span data-ttu-id="153de-133">Nuove funzionalità:</span><span class="sxs-lookup"><span data-stu-id="153de-133">New features:</span></span>

-   <span data-ttu-id="153de-134">Tre nuovi swizzles-. yzxw,. zxyw,. wzyx</span><span class="sxs-lookup"><span data-stu-id="153de-134">Three new swizzles - .yzxw, .zxyw, .wzyx</span></span>
-   <span data-ttu-id="153de-135">Il numero di [registri temporanei](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) è aumentato a 12</span><span class="sxs-lookup"><span data-stu-id="153de-135">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) increased to 12</span></span>
-   <span data-ttu-id="153de-136">Numero di registri di [Registro float costanti](dx9-graphics-reference-asm-ps-registers-constant-float.md) (c \# ) aumentati a 32</span><span class="sxs-lookup"><span data-stu-id="153de-136">Number of [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md) registers (c\#) increased to 32</span></span>
-   <span data-ttu-id="153de-137">Il numero di [registri delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)s (t) è \# aumentato a 8</span><span class="sxs-lookup"><span data-stu-id="153de-137">Number of [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)s (t\#) increased to 8</span></span>

<span data-ttu-id="153de-138">Nuove istruzioni:</span><span class="sxs-lookup"><span data-stu-id="153de-138">New instructions:</span></span>

-   <span data-ttu-id="153de-139">Istruzioni di installazione- [DCL-(SM2, SM3-PS ASM)](dcl---ps.md), [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)</span><span class="sxs-lookup"><span data-stu-id="153de-139">Setup instructions - [dcl - (sm2, sm3 - ps asm)](dcl---ps.md), [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)</span></span>
-   <span data-ttu-id="153de-140">Istruzioni aritmetiche [-ABS-PS](abs---ps.md), [CRS-PS](crs---ps.md), [dp2add-PS](dp2add---ps.md), [Exp-PS](exp---ps.md), [FRC-PS](frc---ps.md), [log-PS](log---ps.md), [M3X2-PS](m3x2---ps.md), [M3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), m4x3 [-PS](m4x3---ps.md), [M4x4-PS](m4x4---ps.md), [max-PS](max---ps.md), [min-PS](min---ps.md), [NRM-PS](nrm---ps.md), [POW-PS](pow---ps.md), [RCP-](rcp---ps.md)PS, [RSQ-PS](rsq---ps.md), [SinCos-PS](sincos---ps.md)</span><span class="sxs-lookup"><span data-stu-id="153de-140">Arithmetic instructions - [abs - ps](abs---ps.md), [crs - ps](crs---ps.md), [dp2add - ps](dp2add---ps.md), [exp - ps](exp---ps.md), [frc - ps](frc---ps.md), [log - ps](log---ps.md), [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), [m4x4 - ps](m4x4---ps.md), [max - ps](max---ps.md), [min - ps](min---ps.md), [nrm - ps](nrm---ps.md), [pow - ps](pow---ps.md), [rcp - ps](rcp---ps.md), [rsq - ps](rsq---ps.md), [sincos - ps](sincos---ps.md)</span></span>
-   <span data-ttu-id="153de-141">Istruzioni di trama- [texld-PS \_ 2 \_ 0 e su](texld---ps-2-0.md) (sintassi diversa), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)</span><span class="sxs-lookup"><span data-stu-id="153de-141">Texture instructions - [texld - ps\_2\_0 and up](texld---ps-2-0.md) (different syntax), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)</span></span>

<span data-ttu-id="153de-142">Nuovi registri:</span><span class="sxs-lookup"><span data-stu-id="153de-142">New registers:</span></span>

-   <span data-ttu-id="153de-143">[Campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) / \# i</span><span class="sxs-lookup"><span data-stu-id="153de-143">[Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#)</span></span>

## <a name="ps_2_x-features"></a><span data-ttu-id="153de-144">Funzionalità di PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="153de-144">ps\_2\_x Features</span></span>

<span data-ttu-id="153de-145">Nuove funzionalità (vedere [**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)):</span><span class="sxs-lookup"><span data-stu-id="153de-145">New features (See [**D3DPSHADERCAPS2\_0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).):</span></span>

-   <span data-ttu-id="153de-146">Controllo dinamico di flusso</span><span class="sxs-lookup"><span data-stu-id="153de-146">Dynamic flow control</span></span>
-   <span data-ttu-id="153de-147">Controllo di flusso statico</span><span class="sxs-lookup"><span data-stu-id="153de-147">Static flow control</span></span>
-   <span data-ttu-id="153de-148">Annidamento per istruzioni di controllo di flusso statiche e dinamiche</span><span class="sxs-lookup"><span data-stu-id="153de-148">Nesting for dynamic and static flow control instructions</span></span>
-   <span data-ttu-id="153de-149">Il numero di [registri temporanei](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ) è aumentato</span><span class="sxs-lookup"><span data-stu-id="153de-149">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r\#) increased</span></span>
-   <span data-ttu-id="153de-150">Swizzle di origine arbitrario</span><span class="sxs-lookup"><span data-stu-id="153de-150">Arbitrary source swizzle</span></span>
-   <span data-ttu-id="153de-151">Istruzioni gradiente</span><span class="sxs-lookup"><span data-stu-id="153de-151">Gradient instructions</span></span>
-   <span data-ttu-id="153de-152">Predicazione</span><span class="sxs-lookup"><span data-stu-id="153de-152">Predication</span></span>
-   <span data-ttu-id="153de-153">Nessun limite di lettura della trama dipendente</span><span class="sxs-lookup"><span data-stu-id="153de-153">No dependent texture read limit</span></span>
-   <span data-ttu-id="153de-154">Nessun limite di istruzioni di trama</span><span class="sxs-lookup"><span data-stu-id="153de-154">No texture instruction limit</span></span>

<span data-ttu-id="153de-155">Nuove istruzioni:</span><span class="sxs-lookup"><span data-stu-id="153de-155">New instructions:</span></span>

-   <span data-ttu-id="153de-156">Istruzioni per il controllo di flusso statico: [se bool-PS](if-bool---ps.md), [Call-PS](call---ps.md), [callnz bool-PS](callnz-bool---ps.md), [else-PS](else---ps.md), [endif-PS](endif---ps.md), [Rep-PS](rep---ps.md), [endrep-PS](endrep---ps.md), [Label-PS](label---ps.md), [ret-PS](ret---ps.md)</span><span class="sxs-lookup"><span data-stu-id="153de-156">Static flow control instructions - [if bool - ps](if-bool---ps.md), [call - ps](call---ps.md), [callnz bool - ps](callnz-bool---ps.md), [else - ps](else---ps.md), [endif - ps](endif---ps.md), [rep - ps](rep---ps.md), [endrep - ps](endrep---ps.md), [label - ps](label---ps.md), [ret - ps](ret---ps.md)</span></span>
-   <span data-ttu-id="153de-157">Istruzioni per il controllo dinamico del flusso- [break-PS](break---ps.md), [break \_ comp-PS](break-comp---ps.md), [Breakp-PS](break-p---ps.md), [callnz prede-PS](callnz-pred---ps.md), [if \_ comp-PS](if-comp---ps.md), [if prede-PS](if-pred---ps.md), [setp \_ comp-PS](setp-comp---ps.md)</span><span class="sxs-lookup"><span data-stu-id="153de-157">Dynamic flow control instructions - [break - ps](break---ps.md), [break\_comp - ps](break-comp---ps.md), [breakp - ps](break-p---ps.md), [callnz pred - ps](callnz-pred---ps.md), [if\_comp - ps](if-comp---ps.md), [if pred - ps](if-pred---ps.md), [setp\_comp - ps](setp-comp---ps.md)</span></span>
-   <span data-ttu-id="153de-158">Istruzioni aritmetiche- [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)</span><span class="sxs-lookup"><span data-stu-id="153de-158">Arithmetic instructions - [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)</span></span>
-   <span data-ttu-id="153de-159">Istruzione di trama- [texldd-PS](texldd---ps.md)</span><span class="sxs-lookup"><span data-stu-id="153de-159">Texture instruction - [texldd - ps](texldd---ps.md)</span></span>

<span data-ttu-id="153de-160">Nuovi registri:</span><span class="sxs-lookup"><span data-stu-id="153de-160">New registers:</span></span>

-   <span data-ttu-id="153de-161">[Registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0)</span><span class="sxs-lookup"><span data-stu-id="153de-161">[Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0)</span></span>

## <a name="ps_3_0-features"></a><span data-ttu-id="153de-162">Funzionalità di PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="153de-162">ps\_3\_0 Features</span></span>

<span data-ttu-id="153de-163">Nuove funzionalità:</span><span class="sxs-lookup"><span data-stu-id="153de-163">New features:</span></span>

-   <span data-ttu-id="153de-164">10 [registri di input](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)consolidati s (v \# )</span><span class="sxs-lookup"><span data-stu-id="153de-164">Consolidated 10 [Input Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)s (v\#)</span></span>
-   <span data-ttu-id="153de-165">[Registro colori input](dx9-graphics-reference-asm-ps-registers-input-color.md) indicizzabile (v \# ) con [registro contatori cicli](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al)</span><span class="sxs-lookup"><span data-stu-id="153de-165">Indexable [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) with the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL)</span></span>
-   <span data-ttu-id="153de-166">Il numero di [registri temporanei](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ) è aumentato a 32</span><span class="sxs-lookup"><span data-stu-id="153de-166">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r\#) increased to 32</span></span>
-   <span data-ttu-id="153de-167">Il numero di [registri float costanti](dx9-graphics-reference-asm-ps-registers-constant-float.md)(c \# ) è aumentato a 224</span><span class="sxs-lookup"><span data-stu-id="153de-167">Number of [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c\#) increased to 224</span></span>

<span data-ttu-id="153de-168">Nuove istruzioni:</span><span class="sxs-lookup"><span data-stu-id="153de-168">New instructions:</span></span>

-   <span data-ttu-id="153de-169">Istruzioni di installazione [- \_ semantica DCL (SM3-PS ASM)](dcl-usage---ps.md)</span><span class="sxs-lookup"><span data-stu-id="153de-169">Setup instruction - [dcl\_semantics (sm3 - ps asm)](dcl-usage---ps.md)</span></span>
-   <span data-ttu-id="153de-170">Istruzioni per il flusso statico- [ciclo PS](loop---ps.md), [EndLoop-PS](endloop---ps.md)</span><span class="sxs-lookup"><span data-stu-id="153de-170">Static flow instructions - [loop - ps](loop---ps.md), [endloop - ps](endloop---ps.md)</span></span>
-   <span data-ttu-id="153de-171">Istruzione aritmetica- [SinCos-PS](sincos---ps.md) (nuova sintassi)</span><span class="sxs-lookup"><span data-stu-id="153de-171">Arithmetic instruction - [sincos - ps](sincos---ps.md) (new syntax)</span></span>
-   <span data-ttu-id="153de-172">Istruzione di trama- [texldl-PS](texldl---ps.md)</span><span class="sxs-lookup"><span data-stu-id="153de-172">Texture instruction - [texldl - ps](texldl---ps.md)</span></span>

<span data-ttu-id="153de-173">Nuovi registri:</span><span class="sxs-lookup"><span data-stu-id="153de-173">New registers:</span></span>

-   <span data-ttu-id="153de-174">[Registro di input](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# )</span><span class="sxs-lookup"><span data-stu-id="153de-174">[Input Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v\#)</span></span>
-   <span data-ttu-id="153de-175">[Position Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos)</span><span class="sxs-lookup"><span data-stu-id="153de-175">[Position Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos)</span></span>
-   <span data-ttu-id="153de-176">[Registro viso](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)</span><span class="sxs-lookup"><span data-stu-id="153de-176">[Face Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)</span></span>

## <a name="related-topics"></a><span data-ttu-id="153de-177">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="153de-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="153de-178">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="153de-178">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 