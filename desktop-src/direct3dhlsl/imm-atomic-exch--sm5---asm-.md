---
title: imm_atomic_exch (SM5-ASM)
description: Immediato scambio atomico in memoria.
ms.assetid: D06AE57E-52A4-4579-84FF-7DE9E713A5E3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb38cd696af079c5ae7dc896db619b95dd1d1d6c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117213"
---
# <a name="imm_atomic_exch-sm5---asm"></a><span data-ttu-id="ccfd7-103">IMM \_ Atomic \_ Exch (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ccfd7-103">imm\_atomic\_exch (sm5 - asm)</span></span>

<span data-ttu-id="ccfd7-104">Immediato scambio atomico in memoria.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-104">Immediate atomic exchange to memory.</span></span>



| <span data-ttu-id="ccfd7-105">IMM \_ Atomic \_ Exch dst0 \[ . Single \_ Component \_ mask \] , DST1, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="ccfd7-105">imm\_atomic\_exch dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="ccfd7-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="ccfd7-106">Item</span></span>                                                                                                           | <span data-ttu-id="ccfd7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccfd7-107">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccfd7-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="ccfd7-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="ccfd7-109">\[in \] contiene il valore di *DST1* prima della scrittura.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-109">\[in\] Contains the value from *dst1* before the write.</span></span><br/>                                                                |
| <span data-ttu-id="ccfd7-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="ccfd7-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="ccfd7-111">\[in \] una visualizzazione di accesso non ordinato (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="ccfd7-111">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="ccfd7-112">In compute shader questo può essere anche la memoria condivisa del gruppo di thread (g \# ).</span><span class="sxs-lookup"><span data-stu-id="ccfd7-112">In the Compute Shader this can also be Thread Group Shared Memory (g\#).</span></span> <br/> |
| <span data-ttu-id="ccfd7-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="ccfd7-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="ccfd7-114">\[nell' \] indirizzo di memoria.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-114">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="ccfd7-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ccfd7-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="ccfd7-116">\[nel \] valore da scrivere in *Dst1* in *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-116">\[in\] The value to write to *dst1* at *dstAddress*.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="ccfd7-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ccfd7-117">Remarks</span></span>

<span data-ttu-id="ccfd7-118">Questa istruzione esegue un singolo componente a 32 bit che scrive l'operando *src0* in *DST1* a 32 bit per indirizzo componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-118">This instruction performs a single component 32-bit value write of operand *src0* to *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="ccfd7-119">Se *DST1* è un u \# , potrebbe essere stato dichiarato come RAW, tipizzato o strutturato.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-119">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="ccfd7-120">Se tipizzata, deve essere dichiarata come UINT/SINT con il formato di risorsa associato R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="ccfd7-121">Se *DST1* è g \# , deve essere dichiarato come RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-121">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="ccfd7-122">Il numero di componenti presi dall'indirizzo è determinato dalla dimensionalità della risorsa dichiarata in *DST1*.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-122">The number of components taken from the address is determined by the dimensionality of the resource declared at *dst1*.</span></span>

<span data-ttu-id="ccfd7-123">Il valore originale a 32 bit nella memoria di destinazione viene scritto in *dst0*.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-123">The original 32-bit value in the destination memory is written to *dst0*.</span></span>

<span data-ttu-id="ccfd7-124">L'intera operazione viene eseguita in modo atomico.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-124">The entire operation is performed atomically.</span></span>

<span data-ttu-id="ccfd7-125">Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato scartato in precedenza nell'esecuzione o se una chiamata di pixel/campione esiste solo per fungere da helper per un pixel/campione reale per i derivati, questa istruzione non modifica la memoria *DST1* e il valore restituito non è definito.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-125">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="ccfd7-126">L'indirizzamento fuori dall'indirizzamento su u \# non comporta la scrittura in memoria, tranne nel caso in cui l'u \# sia strutturato e l'offset dei byte nello struct (secondo componente dell'indirizzo) provochi l'accesso fuori limite, quindi l'intero contenuto del UAV diventa non definito.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-126">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="ccfd7-127">L'indirizzamento fuori limite su u \# o g \# causa la restituzione di un risultato non definito allo shader in *dst0*.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-127">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="ccfd7-128">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ccfd7-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ccfd7-129">Vertice</span><span class="sxs-lookup"><span data-stu-id="ccfd7-129">Vertex</span></span> | <span data-ttu-id="ccfd7-130">Hull</span><span class="sxs-lookup"><span data-stu-id="ccfd7-130">Hull</span></span> | <span data-ttu-id="ccfd7-131">Dominio</span><span class="sxs-lookup"><span data-stu-id="ccfd7-131">Domain</span></span> | <span data-ttu-id="ccfd7-132">Geometria</span><span class="sxs-lookup"><span data-stu-id="ccfd7-132">Geometry</span></span> | <span data-ttu-id="ccfd7-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="ccfd7-133">Pixel</span></span> | <span data-ttu-id="ccfd7-134">Calcolo</span><span class="sxs-lookup"><span data-stu-id="ccfd7-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ccfd7-135">X</span><span class="sxs-lookup"><span data-stu-id="ccfd7-135">X</span></span>     | <span data-ttu-id="ccfd7-136">X</span><span class="sxs-lookup"><span data-stu-id="ccfd7-136">X</span></span>       |



 

<span data-ttu-id="ccfd7-137">Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ccfd7-137">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="ccfd7-138">Vertice</span><span class="sxs-lookup"><span data-stu-id="ccfd7-138">Vertex</span></span> | <span data-ttu-id="ccfd7-139">Hull</span><span class="sxs-lookup"><span data-stu-id="ccfd7-139">Hull</span></span> | <span data-ttu-id="ccfd7-140">Dominio</span><span class="sxs-lookup"><span data-stu-id="ccfd7-140">Domain</span></span> | <span data-ttu-id="ccfd7-141">Geometria</span><span class="sxs-lookup"><span data-stu-id="ccfd7-141">Geometry</span></span> | <span data-ttu-id="ccfd7-142">Pixel</span><span class="sxs-lookup"><span data-stu-id="ccfd7-142">Pixel</span></span> | <span data-ttu-id="ccfd7-143">Calcolo</span><span class="sxs-lookup"><span data-stu-id="ccfd7-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ccfd7-144">X</span><span class="sxs-lookup"><span data-stu-id="ccfd7-144">X</span></span>      | <span data-ttu-id="ccfd7-145">X</span><span class="sxs-lookup"><span data-stu-id="ccfd7-145">X</span></span>    | <span data-ttu-id="ccfd7-146">X</span><span class="sxs-lookup"><span data-stu-id="ccfd7-146">X</span></span>      | <span data-ttu-id="ccfd7-147">X</span><span class="sxs-lookup"><span data-stu-id="ccfd7-147">X</span></span>        | <span data-ttu-id="ccfd7-148">X</span><span class="sxs-lookup"><span data-stu-id="ccfd7-148">X</span></span>     | <span data-ttu-id="ccfd7-149">X</span><span class="sxs-lookup"><span data-stu-id="ccfd7-149">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ccfd7-150">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="ccfd7-150">Minimum Shader Model</span></span>

<span data-ttu-id="ccfd7-151">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="ccfd7-151">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ccfd7-152">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="ccfd7-152">Shader Model</span></span>                                              | <span data-ttu-id="ccfd7-153">Supportato</span><span class="sxs-lookup"><span data-stu-id="ccfd7-153">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ccfd7-154">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="ccfd7-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ccfd7-155">sì</span><span class="sxs-lookup"><span data-stu-id="ccfd7-155">yes</span></span>       |
| [<span data-ttu-id="ccfd7-156">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="ccfd7-156">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ccfd7-157">no</span><span class="sxs-lookup"><span data-stu-id="ccfd7-157">no</span></span>        |
| [<span data-ttu-id="ccfd7-158">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="ccfd7-158">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ccfd7-159">no</span><span class="sxs-lookup"><span data-stu-id="ccfd7-159">no</span></span>        |
| [<span data-ttu-id="ccfd7-160">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ccfd7-160">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ccfd7-161">no</span><span class="sxs-lookup"><span data-stu-id="ccfd7-161">no</span></span>        |
| [<span data-ttu-id="ccfd7-162">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ccfd7-162">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ccfd7-163">no</span><span class="sxs-lookup"><span data-stu-id="ccfd7-163">no</span></span>        |
| [<span data-ttu-id="ccfd7-164">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ccfd7-164">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ccfd7-165">no</span><span class="sxs-lookup"><span data-stu-id="ccfd7-165">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ccfd7-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ccfd7-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccfd7-167">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ccfd7-167">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





