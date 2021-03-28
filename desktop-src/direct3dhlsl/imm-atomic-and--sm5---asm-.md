---
title: imm_atomic_and (SM5-ASM)
description: Bit per bit atomico immediato e alla memoria. Restituisce il valore in memoria prima di e.
ms.assetid: DA2A70C3-57BD-41F0-865C-235AA4DF1A52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1567d3b4eb16a46b1be9badb8db7b39cc03b4b32
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976418"
---
# <a name="imm_atomic_and-sm5---asm"></a><span data-ttu-id="c9e2d-104">IMM \_ Atomic \_ e (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c9e2d-104">imm\_atomic\_and (sm5 - asm)</span></span>

<span data-ttu-id="c9e2d-105">Bit per bit atomico immediato e alla memoria.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-105">Immediate atomic bitwise AND to memory.</span></span> <span data-ttu-id="c9e2d-106">Restituisce il valore in memoria prima di e.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-106">Returns the value in memory before the AND.</span></span>



| <span data-ttu-id="c9e2d-107">IMM \_ Atomic \_ e dst0 \[ . Single \_ Component \_ mask \] , DST1, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="c9e2d-107">imm\_atomic\_and dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|-------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c9e2d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c9e2d-108">Item</span></span>                                                                                                           | <span data-ttu-id="c9e2d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9e2d-109">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9e2d-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="c9e2d-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="c9e2d-111">\[in \] contiene il valore di *DST1* prima di e.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-111">\[in\] Contains value from *dst1* before the AND.</span></span><br/>                                                                      |
| <span data-ttu-id="c9e2d-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="c9e2d-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="c9e2d-113">\[in \] una visualizzazione di accesso non ordinato (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="c9e2d-113">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="c9e2d-114">In compute shader questo può essere anche la memoria condivisa del gruppo di thread (g \# ).</span><span class="sxs-lookup"><span data-stu-id="c9e2d-114">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="c9e2d-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="c9e2d-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="c9e2d-116">\[nella \] memoria di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-116">\[in\] The destination memory.</span></span><br/>                                                                                         |
| <span data-ttu-id="c9e2d-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c9e2d-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="c9e2d-118">Valore per e con l' *ora legale*.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-118">The value to AND with *dst*.</span></span><br/>                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="c9e2d-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9e2d-119">Remarks</span></span>

<span data-ttu-id="c9e2d-120">Questa istruzione esegue un singolo componente bit per bit a 32 bit e di operando *src0* con *DST1* a 32 bit per indirizzo componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-120">This instruction performs a single component 32-bit bitwise AND of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="c9e2d-121">Se *DST1* è un u \# , potrebbe essere stato dichiarato come RAW, tipizzato o strutturato.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-121">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="c9e2d-122">Se tipizzata, deve essere dichiarata come UINT/SINT con il formato di risorsa associato R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-122">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="c9e2d-123">Se *DST1* è g \# , deve essere dichiarato come RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-123">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="c9e2d-124">Il valore nella memoria *DST1* prima di e viene restituito a *dst0*.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-124">The value in *dst1* memory before the AND is returned to *dst0*.</span></span>

<span data-ttu-id="c9e2d-125">L'intera operazione viene eseguita in modo atomico.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-125">The entire operation is performed atomically.</span></span>

<span data-ttu-id="c9e2d-126">Il numero di componenti presi dall'indirizzo è determinato dalla dimensionalità della risorsa dichiarata in *DST1*.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-126">The number of components taken from the address is determined by the dimensionality of the resource declared at *dst1*.</span></span>

<span data-ttu-id="c9e2d-127">Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato scartato in precedenza nell'esecuzione o se una chiamata di pixel/campione esiste solo per fungere da helper per un pixel/campione reale per i derivati, questa istruzione non modifica la memoria *DST1* e il valore restituito non è definito.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="c9e2d-128">L'indirizzamento fuori dall'indirizzamento su u \# non comporta la scrittura in memoria, tranne nel caso in cui l'u \# sia strutturato e l'offset dei byte nello struct (secondo componente dell'indirizzo) provochi l'accesso fuori limite, quindi l'intero contenuto del UAV diventa non definito.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="c9e2d-129">L'indirizzamento fuori limite su u \# o g \# causa la restituzione di un risultato non definito allo shader in *dst0*.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="c9e2d-130">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9e2d-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c9e2d-131">Vertice</span><span class="sxs-lookup"><span data-stu-id="c9e2d-131">Vertex</span></span> | <span data-ttu-id="c9e2d-132">Hull</span><span class="sxs-lookup"><span data-stu-id="c9e2d-132">Hull</span></span> | <span data-ttu-id="c9e2d-133">Dominio</span><span class="sxs-lookup"><span data-stu-id="c9e2d-133">Domain</span></span> | <span data-ttu-id="c9e2d-134">Geometria</span><span class="sxs-lookup"><span data-stu-id="c9e2d-134">Geometry</span></span> | <span data-ttu-id="c9e2d-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="c9e2d-135">Pixel</span></span> | <span data-ttu-id="c9e2d-136">Calcolo</span><span class="sxs-lookup"><span data-stu-id="c9e2d-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c9e2d-137">X</span><span class="sxs-lookup"><span data-stu-id="c9e2d-137">X</span></span>     | <span data-ttu-id="c9e2d-138">X</span><span class="sxs-lookup"><span data-stu-id="c9e2d-138">X</span></span>       |



 

<span data-ttu-id="c9e2d-139">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c9e2d-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="c9e2d-140">Vertice</span><span class="sxs-lookup"><span data-stu-id="c9e2d-140">Vertex</span></span> | <span data-ttu-id="c9e2d-141">Hull</span><span class="sxs-lookup"><span data-stu-id="c9e2d-141">Hull</span></span> | <span data-ttu-id="c9e2d-142">Dominio</span><span class="sxs-lookup"><span data-stu-id="c9e2d-142">Domain</span></span> | <span data-ttu-id="c9e2d-143">Geometria</span><span class="sxs-lookup"><span data-stu-id="c9e2d-143">Geometry</span></span> | <span data-ttu-id="c9e2d-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="c9e2d-144">Pixel</span></span> | <span data-ttu-id="c9e2d-145">Calcolo</span><span class="sxs-lookup"><span data-stu-id="c9e2d-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c9e2d-146">X</span><span class="sxs-lookup"><span data-stu-id="c9e2d-146">X</span></span>      | <span data-ttu-id="c9e2d-147">X</span><span class="sxs-lookup"><span data-stu-id="c9e2d-147">X</span></span>    | <span data-ttu-id="c9e2d-148">X</span><span class="sxs-lookup"><span data-stu-id="c9e2d-148">X</span></span>      | <span data-ttu-id="c9e2d-149">X</span><span class="sxs-lookup"><span data-stu-id="c9e2d-149">X</span></span>        | <span data-ttu-id="c9e2d-150">X</span><span class="sxs-lookup"><span data-stu-id="c9e2d-150">X</span></span>     | <span data-ttu-id="c9e2d-151">X</span><span class="sxs-lookup"><span data-stu-id="c9e2d-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c9e2d-152">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="c9e2d-152">Minimum Shader Model</span></span>

<span data-ttu-id="c9e2d-153">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9e2d-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c9e2d-154">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="c9e2d-154">Shader Model</span></span>                                              | <span data-ttu-id="c9e2d-155">Supportato</span><span class="sxs-lookup"><span data-stu-id="c9e2d-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c9e2d-156">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="c9e2d-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c9e2d-157">sì</span><span class="sxs-lookup"><span data-stu-id="c9e2d-157">yes</span></span>       |
| [<span data-ttu-id="c9e2d-158">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="c9e2d-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c9e2d-159">no</span><span class="sxs-lookup"><span data-stu-id="c9e2d-159">no</span></span>        |
| [<span data-ttu-id="c9e2d-160">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="c9e2d-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c9e2d-161">no</span><span class="sxs-lookup"><span data-stu-id="c9e2d-161">no</span></span>        |
| [<span data-ttu-id="c9e2d-162">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9e2d-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c9e2d-163">no</span><span class="sxs-lookup"><span data-stu-id="c9e2d-163">no</span></span>        |
| [<span data-ttu-id="c9e2d-164">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9e2d-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c9e2d-165">no</span><span class="sxs-lookup"><span data-stu-id="c9e2d-165">no</span></span>        |
| [<span data-ttu-id="c9e2d-166">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9e2d-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c9e2d-167">no</span><span class="sxs-lookup"><span data-stu-id="c9e2d-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c9e2d-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9e2d-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9e2d-169">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9e2d-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





