---
title: atomic_iadd (SM5-ASM)
description: Integer atomico aggiunto alla memoria.
ms.assetid: 093C7FA5-41BF-4BDD-A35D-1AACE8CB9B5C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a8652d4e29aae9f32a84f7a4e4d477abd54b7c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335604"
---
# <a name="atomic_iadd-sm5---asm"></a><span data-ttu-id="aedf0-103">Atomic \_ IAdd (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="aedf0-103">atomic\_iadd (sm5 - asm)</span></span>

<span data-ttu-id="aedf0-104">Integer atomico aggiunto alla memoria.</span><span class="sxs-lookup"><span data-stu-id="aedf0-104">Atomic integer add to memory.</span></span>



| <span data-ttu-id="aedf0-105">\_componente Atomic IAdd DST, dstAddress \[ . Swizzle \] , src0 \[ . Select \_\]</span><span class="sxs-lookup"><span data-stu-id="aedf0-105">atomic\_iadd dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|----------------------------------------------------------------------|



 



| <span data-ttu-id="aedf0-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="aedf0-106">Item</span></span>                                                                                                           | <span data-ttu-id="aedf0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aedf0-107">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aedf0-108"><span id="dst"></span><span id="DST"></span>*DST*</span><span class="sxs-lookup"><span data-stu-id="aedf0-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="aedf0-109">\[nei \] componenti da aggiungere con *src0*.</span><span class="sxs-lookup"><span data-stu-id="aedf0-109">\[in\] The components to add with *src0*.</span></span> <span data-ttu-id="aedf0-110">Questo valore deve essere una visualizzazione di accesso non ordinato (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="aedf0-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="aedf0-111">Nel compute shader può anche essere la memoria condivisa del gruppo di thread (g \# ).</span><span class="sxs-lookup"><span data-stu-id="aedf0-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="aedf0-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="aedf0-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="aedf0-113">\[nell' \] indirizzo di memoria.</span><span class="sxs-lookup"><span data-stu-id="aedf0-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="aedf0-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="aedf0-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="aedf0-115">\[nei \] componenti da aggiungere all' *ora legale*.</span><span class="sxs-lookup"><span data-stu-id="aedf0-115">\[in\] The components to add to *dst*.</span></span><br/>                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="aedf0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="aedf0-116">Remarks</span></span>

<span data-ttu-id="aedf0-117">Questa istruzione esegue un singolo componente a 32 bit Integer aggiunto dell'operando *src0* nell' *ora legale* a 32 bit per indirizzo componente *dstAddress*, eseguito atomicamente.</span><span class="sxs-lookup"><span data-stu-id="aedf0-117">This instruction performs a single component 32-bit integer add of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span> <span data-ttu-id="aedf0-118">Questa istruzione non è sensibile per la firma.</span><span class="sxs-lookup"><span data-stu-id="aedf0-118">This instruction is insensitive to sign.</span></span>

<span data-ttu-id="aedf0-119">Il numero di componenti presi dall'indirizzo è determinato dalla dimensionalità dell' *ora legale* u \# o g \# .</span><span class="sxs-lookup"><span data-stu-id="aedf0-119">The number of components taken from the address is determined by the dimensionality of *dst* u\# or g\#.</span></span>

<span data-ttu-id="aedf0-120">Se *DST* è un u \# , può essere dichiarato come RAW, tipizzato o strutturato.</span><span class="sxs-lookup"><span data-stu-id="aedf0-120">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="aedf0-121">Se tipizzata, deve essere dichiarata come UINT/SINT con il formato di risorsa associato R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="aedf0-121">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="aedf0-122">Se *DST* è g \# , deve essere dichiarato come RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="aedf0-122">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="aedf0-123">Non viene restituito nulla allo shader.</span><span class="sxs-lookup"><span data-stu-id="aedf0-123">Nothing is returned to the shader.</span></span>

<span data-ttu-id="aedf0-124">Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato scartato in precedenza nell'esecuzione o se una chiamata di pixel/campione esiste solo per fungere da helper per un pixel/campione reale per i derivati, questa istruzione non modifica la memoria *DST* (in modo invisibile all'utente).</span><span class="sxs-lookup"><span data-stu-id="aedf0-124">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or if a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="aedf0-125">L'indirizzamento fuori dall'indirizzamento su u \# non comporta la scrittura in memoria, tranne nel caso in cui l'u \# sia strutturato e l'offset dei byte nello struct (secondo componente dell'indirizzo) provochi l'accesso fuori limite, quindi l'intero contenuto del UAV diventa non definito.</span><span class="sxs-lookup"><span data-stu-id="aedf0-125">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="aedf0-126">All'esterno dei limiti che puntano a g \# (i limiti di tale particolare g \# , anziché di tutta la memoria condivisa), l'intero contenuto di tutta la memoria condivisa diventa indefinito.</span><span class="sxs-lookup"><span data-stu-id="aedf0-126">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="aedf0-127">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="aedf0-127">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="aedf0-128">Vertice</span><span class="sxs-lookup"><span data-stu-id="aedf0-128">Vertex</span></span> | <span data-ttu-id="aedf0-129">Hull</span><span class="sxs-lookup"><span data-stu-id="aedf0-129">Hull</span></span> | <span data-ttu-id="aedf0-130">Dominio</span><span class="sxs-lookup"><span data-stu-id="aedf0-130">Domain</span></span> | <span data-ttu-id="aedf0-131">Geometria</span><span class="sxs-lookup"><span data-stu-id="aedf0-131">Geometry</span></span> | <span data-ttu-id="aedf0-132">Pixel</span><span class="sxs-lookup"><span data-stu-id="aedf0-132">Pixel</span></span> | <span data-ttu-id="aedf0-133">Calcolo</span><span class="sxs-lookup"><span data-stu-id="aedf0-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="aedf0-134">X</span><span class="sxs-lookup"><span data-stu-id="aedf0-134">X</span></span>     | <span data-ttu-id="aedf0-135">X</span><span class="sxs-lookup"><span data-stu-id="aedf0-135">X</span></span>       |



 

<span data-ttu-id="aedf0-136">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aedf0-136">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="aedf0-137">Vertice</span><span class="sxs-lookup"><span data-stu-id="aedf0-137">Vertex</span></span> | <span data-ttu-id="aedf0-138">Hull</span><span class="sxs-lookup"><span data-stu-id="aedf0-138">Hull</span></span> | <span data-ttu-id="aedf0-139">Dominio</span><span class="sxs-lookup"><span data-stu-id="aedf0-139">Domain</span></span> | <span data-ttu-id="aedf0-140">Geometria</span><span class="sxs-lookup"><span data-stu-id="aedf0-140">Geometry</span></span> | <span data-ttu-id="aedf0-141">Pixel</span><span class="sxs-lookup"><span data-stu-id="aedf0-141">Pixel</span></span> | <span data-ttu-id="aedf0-142">Calcolo</span><span class="sxs-lookup"><span data-stu-id="aedf0-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="aedf0-143">X</span><span class="sxs-lookup"><span data-stu-id="aedf0-143">X</span></span>      | <span data-ttu-id="aedf0-144">X</span><span class="sxs-lookup"><span data-stu-id="aedf0-144">X</span></span>    | <span data-ttu-id="aedf0-145">X</span><span class="sxs-lookup"><span data-stu-id="aedf0-145">X</span></span>      | <span data-ttu-id="aedf0-146">X</span><span class="sxs-lookup"><span data-stu-id="aedf0-146">X</span></span>        | <span data-ttu-id="aedf0-147">X</span><span class="sxs-lookup"><span data-stu-id="aedf0-147">X</span></span>     | <span data-ttu-id="aedf0-148">X</span><span class="sxs-lookup"><span data-stu-id="aedf0-148">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="aedf0-149">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="aedf0-149">Minimum Shader Model</span></span>

<span data-ttu-id="aedf0-150">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="aedf0-150">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="aedf0-151">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="aedf0-151">Shader Model</span></span>                                              | <span data-ttu-id="aedf0-152">Supportato</span><span class="sxs-lookup"><span data-stu-id="aedf0-152">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="aedf0-153">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="aedf0-153">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="aedf0-154">sì</span><span class="sxs-lookup"><span data-stu-id="aedf0-154">yes</span></span>       |
| [<span data-ttu-id="aedf0-155">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="aedf0-155">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="aedf0-156">no</span><span class="sxs-lookup"><span data-stu-id="aedf0-156">no</span></span>        |
| [<span data-ttu-id="aedf0-157">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="aedf0-157">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="aedf0-158">no</span><span class="sxs-lookup"><span data-stu-id="aedf0-158">no</span></span>        |
| [<span data-ttu-id="aedf0-159">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aedf0-159">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="aedf0-160">no</span><span class="sxs-lookup"><span data-stu-id="aedf0-160">no</span></span>        |
| [<span data-ttu-id="aedf0-161">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aedf0-161">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="aedf0-162">no</span><span class="sxs-lookup"><span data-stu-id="aedf0-162">no</span></span>        |
| [<span data-ttu-id="aedf0-163">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aedf0-163">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="aedf0-164">no</span><span class="sxs-lookup"><span data-stu-id="aedf0-164">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aedf0-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aedf0-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aedf0-166">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aedf0-166">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





