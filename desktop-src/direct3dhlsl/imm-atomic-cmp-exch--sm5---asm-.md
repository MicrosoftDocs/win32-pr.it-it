---
title: imm_atomic_cmp_exch (SM5-ASM)
description: Confronto immediato e scambio di memoria.
ms.assetid: 317A69E1-0E0A-45C8-8E0A-B88659ADBECC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63e1be030d7cce0d6f0a581788db39a599272b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857798"
---
# <a name="imm_atomic_cmp_exch-sm5---asm"></a><span data-ttu-id="8d5ac-103">IMM \_ Atomic \_ CMP \_ Exch (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8d5ac-103">imm\_atomic\_cmp\_exch (sm5 - asm)</span></span>

<span data-ttu-id="8d5ac-104">Confronto immediato e scambio di memoria.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-104">Immediate compare and exchange to memory.</span></span>



| <span data-ttu-id="8d5ac-105">IMM \_ Atomic \_ CMP \_ Exch dst0 \[ . Single \_ Component \_ mask \] , DST1, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ Component \] , src1 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="8d5ac-105">imm\_atomic\_cmp\_exch dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\], src1\[.select\_component\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="8d5ac-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="8d5ac-106">Item</span></span>                                                                                                           | <span data-ttu-id="8d5ac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d5ac-107">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d5ac-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="8d5ac-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="8d5ac-109">\[out \] contiene *DST1* prima della scrittura.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-109">\[out\] Contains *dst1* before the write.</span></span><br/>                                                                              |
| <span data-ttu-id="8d5ac-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="8d5ac-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="8d5ac-111">\[in \] una visualizzazione di accesso non ordinato (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="8d5ac-111">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="8d5ac-112">In compute shader questo può essere anche la memoria condivisa del gruppo di thread (g \# ).</span><span class="sxs-lookup"><span data-stu-id="8d5ac-112">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="8d5ac-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="8d5ac-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="8d5ac-114">\[nella \] memoria di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-114">\[in\] The destination memory.</span></span><br/>                                                                                         |
| <span data-ttu-id="8d5ac-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8d5ac-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="8d5ac-116">\[nel \] valore da confrontare con *DST1*.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-116">\[in\] The value to compare to *dst1*.</span></span><br/>                                                                                 |
| <span data-ttu-id="8d5ac-117"><span id="scr1"></span><span id="SCR1"></span>*scr1*</span><span class="sxs-lookup"><span data-stu-id="8d5ac-117"><span id="scr1"></span><span id="SCR1"></span>*scr1*</span></span><br/>                                                | <span data-ttu-id="8d5ac-118">\[nel \] valore scritto nella memoria di destinazione se i valori confrontati sono identici.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-118">\[in\] The value written to the destination memory if the compared values are identical.</span></span><br/>                               |



 

<span data-ttu-id="8d5ac-119">Questa istruzione esegue un confronto di valori a 32 bit a singolo componente dell'operando *src0* con *DST1* a 32 bit per indirizzo del componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-119">This instruction performs a single component 32-bit value compare of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="8d5ac-120">Se *DST1* è un u \# , potrebbe essere stato dichiarato come RAW, tipizzato o strutturato.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-120">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="8d5ac-121">Se tipizzata, deve essere dichiarata come UINT/SINT con il formato di risorsa associato R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-121">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="8d5ac-122">Se *DST1* è g \# , deve essere dichiarato come RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-122">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="8d5ac-123">Se i valori confrontati sono identici, il valore a 32 bit a singolo componente in *src1* viene scritto nella memoria di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-123">If the compared values are identical, the single-component 32-bit value in *src1* is written to the destination memory.</span></span> <span data-ttu-id="8d5ac-124">In caso contrario, la memoria di destinazione non viene modificata.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-124">Otherwise, the destination memory is not changed.</span></span>

<span data-ttu-id="8d5ac-125">Il valore originale a 32 bit nella memoria di destinazione viene sempre scritto in *dst0*.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-125">The original 32-bit value in the destination memory is always written to *dst0*.</span></span>

<span data-ttu-id="8d5ac-126">L'intera operazione viene eseguita in modo atomico.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="8d5ac-127">Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato scartato in precedenza nell'esecuzione o se una chiamata di pixel/campione esiste solo per fungere da helper per un pixel/campione reale per i derivati, questa istruzione non modifica la memoria *DST1* e il valore restituito non è definito.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="8d5ac-128">L'indirizzamento fuori dall'indirizzamento su u \# non comporta la scrittura in memoria, tranne nel caso in cui l'u \# sia strutturato e l'offset dei byte nello struct (secondo componente dell'indirizzo) provochi l'accesso fuori limite, quindi l'intero contenuto del UAV diventa non definito.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="8d5ac-129">L'indirizzamento fuori limite su u \# o g \# causa la restituzione di un risultato non definito allo shader in *dst0*.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="8d5ac-130">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="8d5ac-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8d5ac-131">Vertice</span><span class="sxs-lookup"><span data-stu-id="8d5ac-131">Vertex</span></span> | <span data-ttu-id="8d5ac-132">Hull</span><span class="sxs-lookup"><span data-stu-id="8d5ac-132">Hull</span></span> | <span data-ttu-id="8d5ac-133">Dominio</span><span class="sxs-lookup"><span data-stu-id="8d5ac-133">Domain</span></span> | <span data-ttu-id="8d5ac-134">Geometria</span><span class="sxs-lookup"><span data-stu-id="8d5ac-134">Geometry</span></span> | <span data-ttu-id="8d5ac-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="8d5ac-135">Pixel</span></span> | <span data-ttu-id="8d5ac-136">Calcolo</span><span class="sxs-lookup"><span data-stu-id="8d5ac-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8d5ac-137">X</span><span class="sxs-lookup"><span data-stu-id="8d5ac-137">X</span></span>     | <span data-ttu-id="8d5ac-138">X</span><span class="sxs-lookup"><span data-stu-id="8d5ac-138">X</span></span>       |



 

<span data-ttu-id="8d5ac-139">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8d5ac-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="8d5ac-140">Vertice</span><span class="sxs-lookup"><span data-stu-id="8d5ac-140">Vertex</span></span> | <span data-ttu-id="8d5ac-141">Hull</span><span class="sxs-lookup"><span data-stu-id="8d5ac-141">Hull</span></span> | <span data-ttu-id="8d5ac-142">Dominio</span><span class="sxs-lookup"><span data-stu-id="8d5ac-142">Domain</span></span> | <span data-ttu-id="8d5ac-143">Geometria</span><span class="sxs-lookup"><span data-stu-id="8d5ac-143">Geometry</span></span> | <span data-ttu-id="8d5ac-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="8d5ac-144">Pixel</span></span> | <span data-ttu-id="8d5ac-145">Calcolo</span><span class="sxs-lookup"><span data-stu-id="8d5ac-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8d5ac-146">X</span><span class="sxs-lookup"><span data-stu-id="8d5ac-146">X</span></span>      | <span data-ttu-id="8d5ac-147">X</span><span class="sxs-lookup"><span data-stu-id="8d5ac-147">X</span></span>    | <span data-ttu-id="8d5ac-148">X</span><span class="sxs-lookup"><span data-stu-id="8d5ac-148">X</span></span>      | <span data-ttu-id="8d5ac-149">X</span><span class="sxs-lookup"><span data-stu-id="8d5ac-149">X</span></span>        | <span data-ttu-id="8d5ac-150">X</span><span class="sxs-lookup"><span data-stu-id="8d5ac-150">X</span></span>     | <span data-ttu-id="8d5ac-151">X</span><span class="sxs-lookup"><span data-stu-id="8d5ac-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8d5ac-152">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="8d5ac-152">Minimum Shader Model</span></span>

<span data-ttu-id="8d5ac-153">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="8d5ac-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8d5ac-154">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="8d5ac-154">Shader Model</span></span>                                              | <span data-ttu-id="8d5ac-155">Supportato</span><span class="sxs-lookup"><span data-stu-id="8d5ac-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8d5ac-156">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="8d5ac-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8d5ac-157">sì</span><span class="sxs-lookup"><span data-stu-id="8d5ac-157">yes</span></span>       |
| [<span data-ttu-id="8d5ac-158">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="8d5ac-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8d5ac-159">no</span><span class="sxs-lookup"><span data-stu-id="8d5ac-159">no</span></span>        |
| [<span data-ttu-id="8d5ac-160">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="8d5ac-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8d5ac-161">no</span><span class="sxs-lookup"><span data-stu-id="8d5ac-161">no</span></span>        |
| [<span data-ttu-id="8d5ac-162">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d5ac-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8d5ac-163">no</span><span class="sxs-lookup"><span data-stu-id="8d5ac-163">no</span></span>        |
| [<span data-ttu-id="8d5ac-164">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d5ac-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8d5ac-165">no</span><span class="sxs-lookup"><span data-stu-id="8d5ac-165">no</span></span>        |
| [<span data-ttu-id="8d5ac-166">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d5ac-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8d5ac-167">no</span><span class="sxs-lookup"><span data-stu-id="8d5ac-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8d5ac-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d5ac-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d5ac-169">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d5ac-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





