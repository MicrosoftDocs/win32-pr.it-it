---
title: atomic_cmp_store (SM5-ASM)
description: Confronto atomico e scrittura in memoria.
ms.assetid: 1B97E983-11A9-47E4-B274-E94083837C6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26a5292d65b32988017044a2ec52680848dffbef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719441"
---
# <a name="atomic_cmp_store-sm5---asm"></a><span data-ttu-id="ac6d2-103">\_ \_ Archivio di CMP atomico (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ac6d2-103">atomic\_cmp\_store (sm5 - asm)</span></span>

<span data-ttu-id="ac6d2-104">Confronto atomico e scrittura in memoria.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-104">Atomic compare and write to memory.</span></span>



| <span data-ttu-id="ac6d2-105">Atomic \_ CMP \_ Store DST, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ Component \] , src1 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="ac6d2-105">atomic\_cmp\_store dst, dstAddress\[.swizzle\], src0\[.select\_component\], src1\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="ac6d2-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="ac6d2-106">Item</span></span>                                                                                                           | <span data-ttu-id="ac6d2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac6d2-107">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac6d2-108"><span id="dst"></span><span id="DST"></span>*DST*</span><span class="sxs-lookup"><span data-stu-id="ac6d2-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="ac6d2-109">\[nei \] componenti da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-109">\[in\] The components to compare with *src0*.</span></span> <span data-ttu-id="ac6d2-110">Questo valore deve essere una visualizzazione di accesso non ordinato (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="ac6d2-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="ac6d2-111">Nel compute shader può anche essere la memoria condivisa del gruppo di thread (g \# ).</span><span class="sxs-lookup"><span data-stu-id="ac6d2-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="ac6d2-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="ac6d2-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="ac6d2-113">\[nell' \] indirizzo di memoria.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="ac6d2-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ac6d2-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="ac6d2-115">\[nel \] valore a 32 bit da confrontare con l' *ora legale*.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-115">\[in\] The 32-bit value to compare with *dst*.</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="ac6d2-116"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="ac6d2-116"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                                | <span data-ttu-id="ac6d2-117">\[nel \] valore da scrivere in memoria se i valori confrontati sono identici.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-117">\[in\] The value to write to memory if the compared values are identical.</span></span> <br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="ac6d2-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac6d2-118">Remarks</span></span>

<span data-ttu-id="ac6d2-119">Questa istruzione esegue un confronto tra i valori a 32 bit del singolo componente dell'operando *src0* con *DST* a 32 bit per ogni indirizzo del componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-119">This instruction performs a single component 32-bit value compare of operand *src0* with *dst* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="ac6d2-120">Se i valori confrontati sono identici, il valore a 32 bit a singolo componente in *src1* viene scritto nella memoria di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-120">If the compared values are identical, the single-component 32-bit value in *src1* is written to destination memory.</span></span> <span data-ttu-id="ac6d2-121">In caso contrario, la destinazione non viene modificata.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-121">Otherwise, the destination is not changed.</span></span>

<span data-ttu-id="ac6d2-122">L'intera operazione di confronto e scrittura viene eseguita in modo atomico.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-122">The entire compare and write operation is performed atomically.</span></span>

<span data-ttu-id="ac6d2-123">Se *DST* è un u \# , può essere dichiarato come RAW, tipizzato o strutturato.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-123">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="ac6d2-124">Se tipizzata, deve essere dichiarata come UINT/SINT con il formato di risorsa associato R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-124">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="ac6d2-125">Se *DST* è g \# , deve essere dichiarato come RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-125">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="ac6d2-126">Il numero di componenti presi dall'indirizzo è determinato dalla dimensionalità dell'ora legale u \# o g \# .</span><span class="sxs-lookup"><span data-stu-id="ac6d2-126">The number of components taken from the address is determined by the dimensionality of dst u\# or g\#.</span></span>

<span data-ttu-id="ac6d2-127">Non viene restituito nulla allo shader.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-127">Nothing is returned to the shader.</span></span>

<span data-ttu-id="ac6d2-128">Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato scartato in precedenza durante l'esecuzione o se un'istruzione pixel/Sample non modifica la memoria *DST* (in modo invisibile all'utente).</span><span class="sxs-lookup"><span data-stu-id="ac6d2-128">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="ac6d2-129">L'indirizzamento fuori dall'indirizzamento su u \# non comporta la scrittura in memoria, tranne nel caso in cui l'u \# sia strutturato e l'offset dei byte nello struct (secondo componente dell'indirizzo) provochi l'accesso fuori limite, quindi l'intero contenuto del UAV diventa non definito.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-129">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="ac6d2-130">All'esterno dei limiti che puntano a g \# (i limiti di tale particolare g \# , anziché di tutta la memoria condivisa), l'intero contenuto di tutta la memoria condivisa diventa indefinito.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-130">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="ac6d2-131">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ac6d2-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ac6d2-132">Vertice</span><span class="sxs-lookup"><span data-stu-id="ac6d2-132">Vertex</span></span> | <span data-ttu-id="ac6d2-133">Hull</span><span class="sxs-lookup"><span data-stu-id="ac6d2-133">Hull</span></span> | <span data-ttu-id="ac6d2-134">Dominio</span><span class="sxs-lookup"><span data-stu-id="ac6d2-134">Domain</span></span> | <span data-ttu-id="ac6d2-135">Geometria</span><span class="sxs-lookup"><span data-stu-id="ac6d2-135">Geometry</span></span> | <span data-ttu-id="ac6d2-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="ac6d2-136">Pixel</span></span> | <span data-ttu-id="ac6d2-137">Calcolo</span><span class="sxs-lookup"><span data-stu-id="ac6d2-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ac6d2-138">X</span><span class="sxs-lookup"><span data-stu-id="ac6d2-138">X</span></span>     | <span data-ttu-id="ac6d2-139">X</span><span class="sxs-lookup"><span data-stu-id="ac6d2-139">X</span></span>       |



 

<span data-ttu-id="ac6d2-140">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ac6d2-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="ac6d2-141">Vertice</span><span class="sxs-lookup"><span data-stu-id="ac6d2-141">Vertex</span></span> | <span data-ttu-id="ac6d2-142">Hull</span><span class="sxs-lookup"><span data-stu-id="ac6d2-142">Hull</span></span> | <span data-ttu-id="ac6d2-143">Dominio</span><span class="sxs-lookup"><span data-stu-id="ac6d2-143">Domain</span></span> | <span data-ttu-id="ac6d2-144">Geometria</span><span class="sxs-lookup"><span data-stu-id="ac6d2-144">Geometry</span></span> | <span data-ttu-id="ac6d2-145">Pixel</span><span class="sxs-lookup"><span data-stu-id="ac6d2-145">Pixel</span></span> | <span data-ttu-id="ac6d2-146">Calcolo</span><span class="sxs-lookup"><span data-stu-id="ac6d2-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ac6d2-147">X</span><span class="sxs-lookup"><span data-stu-id="ac6d2-147">X</span></span>      | <span data-ttu-id="ac6d2-148">X</span><span class="sxs-lookup"><span data-stu-id="ac6d2-148">X</span></span>    | <span data-ttu-id="ac6d2-149">X</span><span class="sxs-lookup"><span data-stu-id="ac6d2-149">X</span></span>      | <span data-ttu-id="ac6d2-150">X</span><span class="sxs-lookup"><span data-stu-id="ac6d2-150">X</span></span>        | <span data-ttu-id="ac6d2-151">X</span><span class="sxs-lookup"><span data-stu-id="ac6d2-151">X</span></span>     | <span data-ttu-id="ac6d2-152">X</span><span class="sxs-lookup"><span data-stu-id="ac6d2-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ac6d2-153">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="ac6d2-153">Minimum Shader Model</span></span>

<span data-ttu-id="ac6d2-154">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ac6d2-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ac6d2-155">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="ac6d2-155">Shader Model</span></span>                                              | <span data-ttu-id="ac6d2-156">Supportato</span><span class="sxs-lookup"><span data-stu-id="ac6d2-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ac6d2-157">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="ac6d2-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ac6d2-158">sì</span><span class="sxs-lookup"><span data-stu-id="ac6d2-158">yes</span></span>       |
| [<span data-ttu-id="ac6d2-159">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="ac6d2-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ac6d2-160">no</span><span class="sxs-lookup"><span data-stu-id="ac6d2-160">no</span></span>        |
| [<span data-ttu-id="ac6d2-161">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="ac6d2-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ac6d2-162">no</span><span class="sxs-lookup"><span data-stu-id="ac6d2-162">no</span></span>        |
| [<span data-ttu-id="ac6d2-163">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac6d2-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ac6d2-164">no</span><span class="sxs-lookup"><span data-stu-id="ac6d2-164">no</span></span>        |
| [<span data-ttu-id="ac6d2-165">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac6d2-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ac6d2-166">no</span><span class="sxs-lookup"><span data-stu-id="ac6d2-166">no</span></span>        |
| [<span data-ttu-id="ac6d2-167">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac6d2-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ac6d2-168">no</span><span class="sxs-lookup"><span data-stu-id="ac6d2-168">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ac6d2-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ac6d2-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac6d2-170">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac6d2-170">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





