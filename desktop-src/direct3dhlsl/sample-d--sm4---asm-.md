---
title: sample_d (SM4-ASM)
description: Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato. | sample_d (SM4-ASM)
ms.assetid: 9CF57C4A-C0D1-4D57-A5EE-62BBBB291438
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe2d3ad310c18ff2bb10e101c95e0267d534fed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995637"
---
# <a name="sample_d-sm4---asm"></a><span data-ttu-id="f8928-104">esempio \_ d (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f8928-104">sample\_d (sm4 - asm)</span></span>

<span data-ttu-id="f8928-105">Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato.</span><span class="sxs-lookup"><span data-stu-id="f8928-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="f8928-106">Ssample \_ d \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler, srcXDerivatives \[ . Swizzle \] , srcYDerivatives \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f8928-106">ssample\_d\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcXDerivatives\[.swizzle\], srcYDerivatives\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f8928-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f8928-107">Item</span></span>                                                                                                                               | <span data-ttu-id="f8928-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8928-108">Description</span></span>                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8928-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f8928-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                    | <span data-ttu-id="f8928-110">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f8928-110">\[in\] The address of the results of the operation.</span></span><br/>                                                                  |
| <span data-ttu-id="f8928-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="f8928-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                     | <span data-ttu-id="f8928-112">\[in \] un set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="f8928-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="f8928-113">Per ulteriori informazioni, vedere l'istruzione di [esempio](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="f8928-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/>      |
| <span data-ttu-id="f8928-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="f8928-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                 | <span data-ttu-id="f8928-115">\[in \] un registro di trama.</span><span class="sxs-lookup"><span data-stu-id="f8928-115">\[in\] A texture register.</span></span> <span data-ttu-id="f8928-116">Per ulteriori informazioni, vedere l'istruzione di **esempio** .</span><span class="sxs-lookup"><span data-stu-id="f8928-116">For more information see the **sample** instruction.</span></span><br/>                                      |
| <span data-ttu-id="f8928-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="f8928-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                     | <span data-ttu-id="f8928-118">\[in \] un registro del campionatore.</span><span class="sxs-lookup"><span data-stu-id="f8928-118">\[in\] A sampler register.</span></span> <span data-ttu-id="f8928-119">Per ulteriori informazioni, vedere l'istruzione di **esempio** .</span><span class="sxs-lookup"><span data-stu-id="f8928-119">For more information see the **sample** instruction.</span></span><br/>                                      |
| <span data-ttu-id="f8928-120"><span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*</span><span class="sxs-lookup"><span data-stu-id="f8928-120"><span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*</span></span><br/> | <span data-ttu-id="f8928-121">\[nei \] derivati per l'indirizzo di origine nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="f8928-121">\[in\] The derivatives for the source address in the x direction.</span></span> <span data-ttu-id="f8928-122">Per ulteriori informazioni, vedere la sezione **osservazioni** .</span><span class="sxs-lookup"><span data-stu-id="f8928-122">For more information, see the **Remarks** section.</span></span><br/> |
| <span data-ttu-id="f8928-123"><span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*</span><span class="sxs-lookup"><span data-stu-id="f8928-123"><span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*</span></span><br/> | <span data-ttu-id="f8928-124">\[nei \] derivati per l'indirizzo di origine nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="f8928-124">\[in\] The derivatives for the source address in the y direction.</span></span> <span data-ttu-id="f8928-125">Per ulteriori informazioni, vedere la sezione **osservazioni** .</span><span class="sxs-lookup"><span data-stu-id="f8928-125">For more information, see the **Remarks** section.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f8928-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8928-126">Remarks</span></span>

<span data-ttu-id="f8928-127">Questa istruzione si comporta come l'istruzione di [esempio](sample--sm4---asm-.md) , ad eccezione del fatto che i derivati per l'indirizzo di origine nella direzione x e la direzione y sono forniti rispettivamente da parametri aggiuntivi, *srcXDerivatives* e *srcYDerivatives*.</span><span class="sxs-lookup"><span data-stu-id="f8928-127">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction, except that derivatives for the source address in the x direction and the y direction are provided by extra parameters, *srcXDerivatives* and *srcYDerivatives*, respectively.</span></span> <span data-ttu-id="f8928-128">Questi derivati si trovano nello spazio delle coordinate di trama normalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8928-128">These derivatives are in normalized texture coordinate space.</span></span>

<span data-ttu-id="f8928-129">I componenti r, g e b di *srcXDerivatives* (POS-swizzle) forniscono du/DX, DV/DX e DW/DX.</span><span class="sxs-lookup"><span data-stu-id="f8928-129">The r, g and b components of *srcXDerivatives* (POS-swizzle) provide du/dx, dv/dx and dw/dx.</span></span> <span data-ttu-id="f8928-130">Il componente ' a' (POS-swizzle) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f8928-130">The 'a' component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="f8928-131">I componenti r, g e b di *srcYDerivatives* (POS-swizzle) forniscono du/DY, DV/dy e DW/dy.</span><span class="sxs-lookup"><span data-stu-id="f8928-131">The r, g and b components of *srcYDerivatives* (POS-swizzle) provide du/dy, dv/dy and dw/dy.</span></span> <span data-ttu-id="f8928-132">Il componente ' a' (POS-swizzle) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f8928-132">The 'a' component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="f8928-133">A differenza dell'istruzione di **esempio** , che consente di condividere un singolo calcolo di LOD in un timbro 2x2, il **campione \_ d** deve calcolare LOD in modo completamente indipendente, per ogni pixel quando viene usato nel pixel shader.</span><span class="sxs-lookup"><span data-stu-id="f8928-133">Unlike the **sample** instruction, which is permitted to share a single LOD calculation across a 2x2 stamp, **sample\_d** must calculate LOD completely independently, per-pixel when used in the Pixel Shader.</span></span>

<span data-ttu-id="f8928-134">Se gli input derivati per **Sample \_ d** provengono da istruzioni di calcolo derivate nel pixel shader e i valori includono inf/Nan, il comportamento di **Sample \_ d** potrebbe non corrispondere all'istruzione di **esempio** , che calcola in modo implicito il derivato.</span><span class="sxs-lookup"><span data-stu-id="f8928-134">If the derivative inputs to **sample\_d** came from derivative calculation instructions in the Pixel Shader and the values include INF/NaN, the behavior of **sample\_d** may not match the **sample** instruction, which implicitly computes the derivative.</span></span> <span data-ttu-id="f8928-135">I valori INF/NaN possono influire in modo diverso sul calcolo LOD.</span><span class="sxs-lookup"><span data-stu-id="f8928-135">The INF/NaN values may affect the LOD calculation differently.</span></span>

<span data-ttu-id="f8928-136">Il recupero da uno slot di input a cui non è associato alcun elemento restituisce 0 per tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="f8928-136">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

### <a name="restrictions"></a><span data-ttu-id="f8928-137">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="f8928-137">Restrictions</span></span>

-   <span data-ttu-id="f8928-138">l' **esempio \_ d** eredita le stesse restrizioni dell'istruzione di **esempio** , oltre a una restrizione aggiuntiva riportata di seguito per i parametri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="f8928-138">**sample\_d** inherits the same restrictions as the **sample** instruction, plus additional an restriction below for its additional parameters.</span></span>
-   <span data-ttu-id="f8928-139">*srcXDerivatives* e *srcYDerivatives* devono essere Temp (r \# /x \# ), constantBuffer (CB \# ), i registri di input (v \# ) o i valori immediati.</span><span class="sxs-lookup"><span data-stu-id="f8928-139">*srcXDerivatives* and *srcYDerivatives* must be temp (r\#/x\#), constantBuffer (cb\#), input (v\#) registers or immediate value(s).</span></span>

<span data-ttu-id="f8928-140">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="f8928-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f8928-141">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="f8928-141">Vertex Shader</span></span> | <span data-ttu-id="f8928-142">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="f8928-142">Geometry Shader</span></span> | <span data-ttu-id="f8928-143">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="f8928-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f8928-144">X</span><span class="sxs-lookup"><span data-stu-id="f8928-144">X</span></span>             | <span data-ttu-id="f8928-145">X</span><span class="sxs-lookup"><span data-stu-id="f8928-145">X</span></span>               | <span data-ttu-id="f8928-146">x</span><span class="sxs-lookup"><span data-stu-id="f8928-146">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f8928-147">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f8928-147">Minimum Shader Model</span></span>

<span data-ttu-id="f8928-148">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="f8928-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f8928-149">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f8928-149">Shader Model</span></span>                                              | <span data-ttu-id="f8928-150">Supportato</span><span class="sxs-lookup"><span data-stu-id="f8928-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f8928-151">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="f8928-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f8928-152">sì</span><span class="sxs-lookup"><span data-stu-id="f8928-152">yes</span></span>       |
| [<span data-ttu-id="f8928-153">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="f8928-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f8928-154">sì</span><span class="sxs-lookup"><span data-stu-id="f8928-154">yes</span></span>       |
| [<span data-ttu-id="f8928-155">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="f8928-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f8928-156">sì</span><span class="sxs-lookup"><span data-stu-id="f8928-156">yes</span></span>       |
| [<span data-ttu-id="f8928-157">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8928-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f8928-158">no</span><span class="sxs-lookup"><span data-stu-id="f8928-158">no</span></span>        |
| [<span data-ttu-id="f8928-159">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8928-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f8928-160">no</span><span class="sxs-lookup"><span data-stu-id="f8928-160">no</span></span>        |
| [<span data-ttu-id="f8928-161">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8928-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f8928-162">no</span><span class="sxs-lookup"><span data-stu-id="f8928-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f8928-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8928-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8928-164">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8928-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





