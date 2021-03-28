---
title: atomic_imin (SM5-ASM)
description: Intero con segno atomico minimo alla memoria.
ms.assetid: C30C7CDE-1024-4E69-959E-2D3122BF9AA7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d961bd0c14a064b2530a80f5d0cbc032998353
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335596"
---
# <a name="atomic_imin-sm5---asm"></a><span data-ttu-id="caac7-103">Atomic \_ Imin (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="caac7-103">atomic\_imin (sm5 - asm)</span></span>

<span data-ttu-id="caac7-104">Intero con segno atomico minimo alla memoria.</span><span class="sxs-lookup"><span data-stu-id="caac7-104">Atomic signed integer minimum to memory.</span></span>



| <span data-ttu-id="caac7-105">\_componente Atomic Imin DST, dstAddress \[ . Swizzle \] , src0 \[ . Select \_\]</span><span class="sxs-lookup"><span data-stu-id="caac7-105">atomic\_imin dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|----------------------------------------------------------------------|



 



| <span data-ttu-id="caac7-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="caac7-106">Item</span></span>                                                                                                           | <span data-ttu-id="caac7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="caac7-107">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caac7-108"><span id="dst"></span><span id="DST"></span>*DST*</span><span class="sxs-lookup"><span data-stu-id="caac7-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="caac7-109">\[nei \] componenti da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="caac7-109">\[in\] The components to compare to *src0*.</span></span> <span data-ttu-id="caac7-110">Questo valore deve essere una visualizzazione di accesso non ordinato (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="caac7-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="caac7-111">Nel compute shader può anche essere la memoria condivisa del gruppo di thread (g \# ).</span><span class="sxs-lookup"><span data-stu-id="caac7-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="caac7-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="caac7-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="caac7-113">\[nell' \] indirizzo di memoria.</span><span class="sxs-lookup"><span data-stu-id="caac7-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="caac7-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="caac7-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="caac7-115">\[nei \] componenti da confrontare con l' *ora legale*.</span><span class="sxs-lookup"><span data-stu-id="caac7-115">\[in\] The components to compare to *dst*.</span></span><br/>                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="caac7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="caac7-116">Remarks</span></span>

<span data-ttu-id="caac7-117">Questa istruzione esegue un singolo componente con segno a 32 bit di *src0* dell'operando nell' *ora legale* a 32 bit per indirizzo componente *dstAddress*, eseguito atomicamente.</span><span class="sxs-lookup"><span data-stu-id="caac7-117">This instruction performs a single component 32-bit signed minimum of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span>

<span data-ttu-id="caac7-118">Il numero di componenti presi dall'indirizzo è determinato dalla dimensionalità dell' *ora legale* u \# o g \# .</span><span class="sxs-lookup"><span data-stu-id="caac7-118">The number of components taken from the address is determined by the dimensionality of *dst* u\# or g\#.</span></span>

<span data-ttu-id="caac7-119">Se *DST* è un u \# , può essere dichiarato come RAW, tipizzato o strutturato.</span><span class="sxs-lookup"><span data-stu-id="caac7-119">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="caac7-120">Se tipizzata, deve essere dichiarata come UINT/SINT con il formato di risorsa associato R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="caac7-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="caac7-121">Se *DST* è g \# , deve essere dichiarato come RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="caac7-121">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="caac7-122">Non viene restituito nulla allo shader.</span><span class="sxs-lookup"><span data-stu-id="caac7-122">Nothing is returned to the shader.</span></span>

<span data-ttu-id="caac7-123">Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato scartato in precedenza nell'esecuzione o se una chiamata di pixel/campione esiste solo per fungere da helper per un pixel/campione reale per i derivati, questa istruzione non modifica la memoria *DST* (in modo invisibile all'utente).</span><span class="sxs-lookup"><span data-stu-id="caac7-123">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or if a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="caac7-124">L'indirizzamento fuori dall'indirizzamento su u \# non comporta la scrittura in memoria, tranne nel caso in cui l'u \# sia strutturato e l'offset dei byte nello struct (secondo componente dell'indirizzo) provochi l'accesso fuori limite, quindi l'intero contenuto del UAV diventa non definito.</span><span class="sxs-lookup"><span data-stu-id="caac7-124">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="caac7-125">All'esterno dei limiti che puntano a g \# (i limiti di tale particolare g \# , anziché di tutta la memoria condivisa), l'intero contenuto di tutta la memoria condivisa diventa indefinito.</span><span class="sxs-lookup"><span data-stu-id="caac7-125">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="caac7-126">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="caac7-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="caac7-127">Vertice</span><span class="sxs-lookup"><span data-stu-id="caac7-127">Vertex</span></span> | <span data-ttu-id="caac7-128">Hull</span><span class="sxs-lookup"><span data-stu-id="caac7-128">Hull</span></span> | <span data-ttu-id="caac7-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="caac7-129">Domain</span></span> | <span data-ttu-id="caac7-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="caac7-130">Geometry</span></span> | <span data-ttu-id="caac7-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="caac7-131">Pixel</span></span> | <span data-ttu-id="caac7-132">Calcolo</span><span class="sxs-lookup"><span data-stu-id="caac7-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="caac7-133">X</span><span class="sxs-lookup"><span data-stu-id="caac7-133">X</span></span>     | <span data-ttu-id="caac7-134">X</span><span class="sxs-lookup"><span data-stu-id="caac7-134">X</span></span>       |



 

<span data-ttu-id="caac7-135">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="caac7-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="caac7-136">Vertice</span><span class="sxs-lookup"><span data-stu-id="caac7-136">Vertex</span></span> | <span data-ttu-id="caac7-137">Hull</span><span class="sxs-lookup"><span data-stu-id="caac7-137">Hull</span></span> | <span data-ttu-id="caac7-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="caac7-138">Domain</span></span> | <span data-ttu-id="caac7-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="caac7-139">Geometry</span></span> | <span data-ttu-id="caac7-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="caac7-140">Pixel</span></span> | <span data-ttu-id="caac7-141">Calcolo</span><span class="sxs-lookup"><span data-stu-id="caac7-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="caac7-142">X</span><span class="sxs-lookup"><span data-stu-id="caac7-142">X</span></span>      | <span data-ttu-id="caac7-143">X</span><span class="sxs-lookup"><span data-stu-id="caac7-143">X</span></span>    | <span data-ttu-id="caac7-144">X</span><span class="sxs-lookup"><span data-stu-id="caac7-144">X</span></span>      | <span data-ttu-id="caac7-145">X</span><span class="sxs-lookup"><span data-stu-id="caac7-145">X</span></span>        | <span data-ttu-id="caac7-146">X</span><span class="sxs-lookup"><span data-stu-id="caac7-146">X</span></span>     | <span data-ttu-id="caac7-147">X</span><span class="sxs-lookup"><span data-stu-id="caac7-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="caac7-148">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="caac7-148">Minimum Shader Model</span></span>

<span data-ttu-id="caac7-149">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="caac7-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="caac7-150">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="caac7-150">Shader Model</span></span>                                              | <span data-ttu-id="caac7-151">Supportato</span><span class="sxs-lookup"><span data-stu-id="caac7-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="caac7-152">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="caac7-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="caac7-153">sì</span><span class="sxs-lookup"><span data-stu-id="caac7-153">yes</span></span>       |
| [<span data-ttu-id="caac7-154">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="caac7-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="caac7-155">no</span><span class="sxs-lookup"><span data-stu-id="caac7-155">no</span></span>        |
| [<span data-ttu-id="caac7-156">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="caac7-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="caac7-157">no</span><span class="sxs-lookup"><span data-stu-id="caac7-157">no</span></span>        |
| [<span data-ttu-id="caac7-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="caac7-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="caac7-159">no</span><span class="sxs-lookup"><span data-stu-id="caac7-159">no</span></span>        |
| [<span data-ttu-id="caac7-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="caac7-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="caac7-161">no</span><span class="sxs-lookup"><span data-stu-id="caac7-161">no</span></span>        |
| [<span data-ttu-id="caac7-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="caac7-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="caac7-163">no</span><span class="sxs-lookup"><span data-stu-id="caac7-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="caac7-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="caac7-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caac7-165">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="caac7-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





