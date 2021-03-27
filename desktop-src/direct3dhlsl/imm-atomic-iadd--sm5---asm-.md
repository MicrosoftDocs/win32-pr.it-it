---
title: imm_atomic_iadd (SM5-ASM)
description: Intero atomico immediato Aggiungi alla memoria. Restituisce il valore in memoria prima dell'aggiunta.
ms.assetid: 24136B4C-D37C-4449-A318-57145BB8D8E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2695e23707fb61cd576748e2e83829cd7dc65259
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398272"
---
# <a name="imm_atomic_iadd-sm5---asm"></a><span data-ttu-id="5ccec-104">IMM \_ Atomic \_ IAdd (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5ccec-104">imm\_atomic\_iadd (sm5 - asm)</span></span>

<span data-ttu-id="5ccec-105">Intero atomico immediato Aggiungi alla memoria.</span><span class="sxs-lookup"><span data-stu-id="5ccec-105">Immediate atomic integer add to memory.</span></span> <span data-ttu-id="5ccec-106">Restituisce il valore in memoria prima dell'aggiunta.</span><span class="sxs-lookup"><span data-stu-id="5ccec-106">Returns the value in memory before the add.</span></span>



| <span data-ttu-id="5ccec-107">IMM \_ Atomic \_ IAdd dst0 \[ . Single \_ Component \_ mask \] , DST1, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="5ccec-107">imm\_atomic\_iadd dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="5ccec-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5ccec-108">Item</span></span>                                                                                                           | <span data-ttu-id="5ccec-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ccec-109">Description</span></span>                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ccec-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="5ccec-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="5ccec-111">\[in \] contiene il valore in *DST1* prima della scrittura.</span><span class="sxs-lookup"><span data-stu-id="5ccec-111">\[in\] Contains the value in *dst1* before the write.</span></span> <br/>                                                                           |
| <span data-ttu-id="5ccec-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="5ccec-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="5ccec-113">Questo valore deve essere una visualizzazione di accesso non ordinato (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="5ccec-113">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="5ccec-114">Nel compute shader può anche essere la memoria condivisa del gruppo di thread (g \# ).</span><span class="sxs-lookup"><span data-stu-id="5ccec-114">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="5ccec-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="5ccec-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="5ccec-116">\[nella \] memoria nAddress.</span><span class="sxs-lookup"><span data-stu-id="5ccec-116">\[in\] The memory naddress.</span></span><br/>                                                                                                      |
| <span data-ttu-id="5ccec-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5ccec-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="5ccec-118">\[nel \] valore da aggiungere a *DST1*.</span><span class="sxs-lookup"><span data-stu-id="5ccec-118">\[in\] The value to add to *dst1*.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="5ccec-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ccec-119">Remarks</span></span>

<span data-ttu-id="5ccec-120">Questa istruzione esegue un singolo componente a 32 bit Integer aggiunta di operando *src0* con *DST1* a 32 bit per indirizzo componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="5ccec-120">This instruction performs a single component 32-bit integer add of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span> <span data-ttu-id="5ccec-121">La firma non è sensibile.</span><span class="sxs-lookup"><span data-stu-id="5ccec-121">It is insensitive to sign.</span></span>

<span data-ttu-id="5ccec-122">Se *DST1* è un u \# , potrebbe essere stato dichiarato come RAW, tipizzato o strutturato.</span><span class="sxs-lookup"><span data-stu-id="5ccec-122">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="5ccec-123">Se tipizzata, deve essere dichiarata come UINT/SINT con il formato di risorsa associato R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="5ccec-123">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="5ccec-124">Se *DST1* è g \# , deve essere dichiarato come RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="5ccec-124">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="5ccec-125">Il valore in *DST1* Memory prima dell'aggiunta viene restituito a *dst0*.</span><span class="sxs-lookup"><span data-stu-id="5ccec-125">The value in *dst1* memory before addition is returned to *dst0*.</span></span>

<span data-ttu-id="5ccec-126">Il numero di componenti presi dall'indirizzo è determinato dalla dimensionalità di *DST1*.</span><span class="sxs-lookup"><span data-stu-id="5ccec-126">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="5ccec-127">L'intera operazione viene eseguita in modo atomico.</span><span class="sxs-lookup"><span data-stu-id="5ccec-127">The entire operation is performed atomically.</span></span>

<span data-ttu-id="5ccec-128">Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato scartato in precedenza nell'esecuzione o se una chiamata di pixel/campione esiste solo per fungere da helper per un pixel/campione reale per i derivati, questa istruzione non modifica la memoria *DST1* e il valore restituito non è definito.</span><span class="sxs-lookup"><span data-stu-id="5ccec-128">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="5ccec-129">L'indirizzamento fuori dall'indirizzamento su u \# non comporta la scrittura in memoria, tranne nel caso in cui l'u \# sia strutturato e l'offset dei byte nello struct (secondo componente dell'indirizzo) provochi l'accesso fuori limite, quindi l'intero contenuto del UAV diventa non definito.</span><span class="sxs-lookup"><span data-stu-id="5ccec-129">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="5ccec-130">L'indirizzamento fuori limite su u \# o g \# causa la restituzione di un risultato non definito allo shader in *dst0*.</span><span class="sxs-lookup"><span data-stu-id="5ccec-130">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="5ccec-131">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="5ccec-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5ccec-132">Vertice</span><span class="sxs-lookup"><span data-stu-id="5ccec-132">Vertex</span></span> | <span data-ttu-id="5ccec-133">Hull</span><span class="sxs-lookup"><span data-stu-id="5ccec-133">Hull</span></span> | <span data-ttu-id="5ccec-134">Dominio</span><span class="sxs-lookup"><span data-stu-id="5ccec-134">Domain</span></span> | <span data-ttu-id="5ccec-135">Geometria</span><span class="sxs-lookup"><span data-stu-id="5ccec-135">Geometry</span></span> | <span data-ttu-id="5ccec-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="5ccec-136">Pixel</span></span> | <span data-ttu-id="5ccec-137">Calcolo</span><span class="sxs-lookup"><span data-stu-id="5ccec-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5ccec-138">X</span><span class="sxs-lookup"><span data-stu-id="5ccec-138">X</span></span>     | <span data-ttu-id="5ccec-139">X</span><span class="sxs-lookup"><span data-stu-id="5ccec-139">X</span></span>       |



 

<span data-ttu-id="5ccec-140">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5ccec-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="5ccec-141">Vertice</span><span class="sxs-lookup"><span data-stu-id="5ccec-141">Vertex</span></span> | <span data-ttu-id="5ccec-142">Hull</span><span class="sxs-lookup"><span data-stu-id="5ccec-142">Hull</span></span> | <span data-ttu-id="5ccec-143">Dominio</span><span class="sxs-lookup"><span data-stu-id="5ccec-143">Domain</span></span> | <span data-ttu-id="5ccec-144">Geometria</span><span class="sxs-lookup"><span data-stu-id="5ccec-144">Geometry</span></span> | <span data-ttu-id="5ccec-145">Pixel</span><span class="sxs-lookup"><span data-stu-id="5ccec-145">Pixel</span></span> | <span data-ttu-id="5ccec-146">Calcolo</span><span class="sxs-lookup"><span data-stu-id="5ccec-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5ccec-147">X</span><span class="sxs-lookup"><span data-stu-id="5ccec-147">X</span></span>      | <span data-ttu-id="5ccec-148">X</span><span class="sxs-lookup"><span data-stu-id="5ccec-148">X</span></span>    | <span data-ttu-id="5ccec-149">X</span><span class="sxs-lookup"><span data-stu-id="5ccec-149">X</span></span>      | <span data-ttu-id="5ccec-150">X</span><span class="sxs-lookup"><span data-stu-id="5ccec-150">X</span></span>        | <span data-ttu-id="5ccec-151">X</span><span class="sxs-lookup"><span data-stu-id="5ccec-151">X</span></span>     | <span data-ttu-id="5ccec-152">X</span><span class="sxs-lookup"><span data-stu-id="5ccec-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5ccec-153">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="5ccec-153">Minimum Shader Model</span></span>

<span data-ttu-id="5ccec-154">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="5ccec-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5ccec-155">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="5ccec-155">Shader Model</span></span>                                              | <span data-ttu-id="5ccec-156">Supportato</span><span class="sxs-lookup"><span data-stu-id="5ccec-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5ccec-157">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="5ccec-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5ccec-158">sì</span><span class="sxs-lookup"><span data-stu-id="5ccec-158">yes</span></span>       |
| [<span data-ttu-id="5ccec-159">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="5ccec-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5ccec-160">no</span><span class="sxs-lookup"><span data-stu-id="5ccec-160">no</span></span>        |
| [<span data-ttu-id="5ccec-161">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="5ccec-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5ccec-162">no</span><span class="sxs-lookup"><span data-stu-id="5ccec-162">no</span></span>        |
| [<span data-ttu-id="5ccec-163">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ccec-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5ccec-164">no</span><span class="sxs-lookup"><span data-stu-id="5ccec-164">no</span></span>        |
| [<span data-ttu-id="5ccec-165">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ccec-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5ccec-166">no</span><span class="sxs-lookup"><span data-stu-id="5ccec-166">no</span></span>        |
| [<span data-ttu-id="5ccec-167">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ccec-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5ccec-168">no</span><span class="sxs-lookup"><span data-stu-id="5ccec-168">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5ccec-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5ccec-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ccec-170">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ccec-170">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





