---
title: imm_atomic_imin (SM5-ASM)
description: Segno atomico immediato da min a memoria. Restituisce un valore in memoria prima dell'operazione max.
ms.assetid: 8E104FFA-D086-49FD-9063-B950B6B1548B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c48b39da642105cacc0936abe1874d81c88e79b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335559"
---
# <a name="imm_atomic_imin-sm5---asm"></a><span data-ttu-id="352fc-104">IMM \_ Atomic \_ Imin (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="352fc-104">imm\_atomic\_imin (sm5 - asm)</span></span>

<span data-ttu-id="352fc-105">Segno atomico immediato da min a memoria.</span><span class="sxs-lookup"><span data-stu-id="352fc-105">Immediate atomic signed min to memory.</span></span> <span data-ttu-id="352fc-106">Restituisce un valore in memoria prima dell'operazione max.</span><span class="sxs-lookup"><span data-stu-id="352fc-106">Returns value in memory before the max operation.</span></span>



| <span data-ttu-id="352fc-107">IMM \_ Atomic \_ Imin dst0 \[ . Single \_ Component \_ mask \] , DST1, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="352fc-107">imm\_atomic\_imin dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="352fc-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="352fc-108">Item</span></span>                                                                                                           | <span data-ttu-id="352fc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="352fc-109">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="352fc-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="352fc-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="352fc-111">\[in \] contiene il valore di *DST1* prima di questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="352fc-111">\[in\] Contains the value from *dst1* before this instruction.</span></span><br/>                                                         |
| <span data-ttu-id="352fc-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="352fc-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="352fc-113">\[in \] una visualizzazione di accesso non ordinato (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="352fc-113">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="352fc-114">In compute shader questo può essere anche la memoria condivisa del gruppo di thread (g \# ).</span><span class="sxs-lookup"><span data-stu-id="352fc-114">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="352fc-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="352fc-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="352fc-116">\[nell' \] indirizzo di memoria.</span><span class="sxs-lookup"><span data-stu-id="352fc-116">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="352fc-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="352fc-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="352fc-118">\[nel \] valore da confrontare con *Dst1* in *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="352fc-118">\[in\] The value to compare to *dst1* at *dstAddress*.</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="352fc-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="352fc-119">Remarks</span></span>

<span data-ttu-id="352fc-120">Questa istruzione esegue un singolo componente con segno a 32 bit dell'operando *src0* con *DST1* a 32 bit per indirizzo di componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="352fc-120">Thisi instruction performs a single component 32-bit signed minimum of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="352fc-121">Se *DST1* è un u \# , potrebbe essere stato dichiarato come RAW, tipizzato o strutturato.</span><span class="sxs-lookup"><span data-stu-id="352fc-121">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="352fc-122">Se tipizzata, deve essere dichiarata come UINT/SINT con il formato di risorsa associato R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="352fc-122">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="352fc-123">Se *DST1* è g \# , deve essere dichiarato come RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="352fc-123">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="352fc-124">Il valore in *DST1* Memory prima del valore min viene restituito a *dst0*.</span><span class="sxs-lookup"><span data-stu-id="352fc-124">The value in *dst1* memory before min is returned to *dst0*.</span></span>

<span data-ttu-id="352fc-125">Il numero di componenti presi dall'indirizzo è determinato dalla dimensionalità di *DST1*.</span><span class="sxs-lookup"><span data-stu-id="352fc-125">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="352fc-126">L'intera operazione viene eseguita in modo atomico.</span><span class="sxs-lookup"><span data-stu-id="352fc-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="352fc-127">Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato scartato in precedenza nell'esecuzione o se una chiamata di pixel/campione esiste solo per fungere da helper per un pixel/campione reale per i derivati, questa istruzione non modifica la memoria *DST1* e il valore restituito non è definito.</span><span class="sxs-lookup"><span data-stu-id="352fc-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="352fc-128">L'indirizzamento fuori dall'indirizzamento su u \# non comporta la scrittura in memoria, tranne nel caso in cui l'u \# sia strutturato e l'offset dei byte nello struct (secondo componente dell'indirizzo) provochi l'accesso fuori limite, quindi l'intero contenuto del UAV diventa non definito.</span><span class="sxs-lookup"><span data-stu-id="352fc-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="352fc-129">L'indirizzamento fuori limite su u \# o g \# causa la restituzione di un risultato non definito allo shader in *dst0*.</span><span class="sxs-lookup"><span data-stu-id="352fc-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="352fc-130">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="352fc-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="352fc-131">Vertice</span><span class="sxs-lookup"><span data-stu-id="352fc-131">Vertex</span></span> | <span data-ttu-id="352fc-132">Hull</span><span class="sxs-lookup"><span data-stu-id="352fc-132">Hull</span></span> | <span data-ttu-id="352fc-133">Dominio</span><span class="sxs-lookup"><span data-stu-id="352fc-133">Domain</span></span> | <span data-ttu-id="352fc-134">Geometria</span><span class="sxs-lookup"><span data-stu-id="352fc-134">Geometry</span></span> | <span data-ttu-id="352fc-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="352fc-135">Pixel</span></span> | <span data-ttu-id="352fc-136">Calcolo</span><span class="sxs-lookup"><span data-stu-id="352fc-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="352fc-137">X</span><span class="sxs-lookup"><span data-stu-id="352fc-137">X</span></span>     | <span data-ttu-id="352fc-138">X</span><span class="sxs-lookup"><span data-stu-id="352fc-138">X</span></span>       |



 

<span data-ttu-id="352fc-139">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="352fc-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="352fc-140">Vertice</span><span class="sxs-lookup"><span data-stu-id="352fc-140">Vertex</span></span> | <span data-ttu-id="352fc-141">Hull</span><span class="sxs-lookup"><span data-stu-id="352fc-141">Hull</span></span> | <span data-ttu-id="352fc-142">Dominio</span><span class="sxs-lookup"><span data-stu-id="352fc-142">Domain</span></span> | <span data-ttu-id="352fc-143">Geometria</span><span class="sxs-lookup"><span data-stu-id="352fc-143">Geometry</span></span> | <span data-ttu-id="352fc-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="352fc-144">Pixel</span></span> | <span data-ttu-id="352fc-145">Calcolo</span><span class="sxs-lookup"><span data-stu-id="352fc-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="352fc-146">X</span><span class="sxs-lookup"><span data-stu-id="352fc-146">X</span></span>      | <span data-ttu-id="352fc-147">X</span><span class="sxs-lookup"><span data-stu-id="352fc-147">X</span></span>    | <span data-ttu-id="352fc-148">X</span><span class="sxs-lookup"><span data-stu-id="352fc-148">X</span></span>      | <span data-ttu-id="352fc-149">X</span><span class="sxs-lookup"><span data-stu-id="352fc-149">X</span></span>        | <span data-ttu-id="352fc-150">X</span><span class="sxs-lookup"><span data-stu-id="352fc-150">X</span></span>     | <span data-ttu-id="352fc-151">X</span><span class="sxs-lookup"><span data-stu-id="352fc-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="352fc-152">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="352fc-152">Minimum Shader Model</span></span>

<span data-ttu-id="352fc-153">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="352fc-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="352fc-154">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="352fc-154">Shader Model</span></span>                                              | <span data-ttu-id="352fc-155">Supportato</span><span class="sxs-lookup"><span data-stu-id="352fc-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="352fc-156">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="352fc-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="352fc-157">sì</span><span class="sxs-lookup"><span data-stu-id="352fc-157">yes</span></span>       |
| [<span data-ttu-id="352fc-158">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="352fc-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="352fc-159">no</span><span class="sxs-lookup"><span data-stu-id="352fc-159">no</span></span>        |
| [<span data-ttu-id="352fc-160">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="352fc-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="352fc-161">no</span><span class="sxs-lookup"><span data-stu-id="352fc-161">no</span></span>        |
| [<span data-ttu-id="352fc-162">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="352fc-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="352fc-163">no</span><span class="sxs-lookup"><span data-stu-id="352fc-163">no</span></span>        |
| [<span data-ttu-id="352fc-164">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="352fc-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="352fc-165">no</span><span class="sxs-lookup"><span data-stu-id="352fc-165">no</span></span>        |
| [<span data-ttu-id="352fc-166">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="352fc-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="352fc-167">no</span><span class="sxs-lookup"><span data-stu-id="352fc-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="352fc-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="352fc-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="352fc-169">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="352fc-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





