---
title: sample_c_lz (SM4-ASM)
description: Esegue un filtro di confronto. Questa istruzione si comporta come esempio \_ c, ad eccezione di LOD è 0 e i derivati vengono ignorati.
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ec2889dd3ea4c86af51c8e36bf2e302c6ad4dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398234"
---
# <a name="sample_c_lz-sm4---asm"></a><span data-ttu-id="7bdf4-104">esempio \_ c \_ LZ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="7bdf4-104">sample\_c\_lz (sm4 - asm)</span></span>

<span data-ttu-id="7bdf4-105">Esegue un filtro di confronto.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-105">Performs a comparison filter.</span></span> <span data-ttu-id="7bdf4-106">Questa istruzione si comporta come [esempio \_ c](sample-c--sm4---asm-.md), ad eccezione di LOD è 0 e i derivati vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-106">This instruction behaves like [sample\_c](sample-c--sm4---asm-.md), except LOD is 0, and derivatives are ignored.</span></span>



| <span data-ttu-id="7bdf4-107">esempio \_ c \_ LZ \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource. r,//deve essere. r swizzle srcSampler, srcReferenceValue//componente singolo selezionato</span><span class="sxs-lookup"><span data-stu-id="7bdf4-107">sample\_c\_lz\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="7bdf4-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="7bdf4-108">Item</span></span>                                                                                                                                       | <span data-ttu-id="7bdf4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bdf4-109">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bdf4-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="7bdf4-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="7bdf4-111">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-111">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="7bdf4-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="7bdf4-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="7bdf4-113">\[in \] un set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-113">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="7bdf4-114">Per ulteriori informazioni, vedere l'istruzione di [esempio](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="7bdf4-114">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="7bdf4-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="7bdf4-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="7bdf4-116">\[in \] un registro di trama.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-116">\[in\] A texture register.</span></span> <span data-ttu-id="7bdf4-117">Per ulteriori informazioni, vedere l'istruzione di **esempio** .</span><span class="sxs-lookup"><span data-stu-id="7bdf4-117">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="7bdf4-118"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="7bdf4-118"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="7bdf4-119">\[in \] un registro del campionatore.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-119">\[in\] A sampler register.</span></span> <span data-ttu-id="7bdf4-120">Per ulteriori informazioni, vedere l'istruzione di **esempio** .</span><span class="sxs-lookup"><span data-stu-id="7bdf4-120">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="7bdf4-121"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="7bdf4-121"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="7bdf4-122">\[in \] un registro con un singolo componente selezionato, che viene utilizzato nel confronto.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-122">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="7bdf4-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="7bdf4-123">Remarks</span></span>

<span data-ttu-id="7bdf4-124">"LZ" sta per il livello zero.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-124">The "lz" stands for level-zero.</span></span> <span data-ttu-id="7bdf4-125">Poiché i derivati vengono ignorati, questa istruzione è disponibile in shader diversi dal pixel shader.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-125">Because derivatives are ignored, this instruction is available in shaders other than the Pixel Shader.</span></span>

<span data-ttu-id="7bdf4-126">Se questa istruzione viene usata con una trama mipmap, viene campionato il valore LOD 0, a meno che il campionatore non disponga di un morsetto LOD che inserisce il valore LOD in un altro punto o se è presente una polarizzazione LOD, che può semplicemente essere polarizzata a partire da 0.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-126">If this instruction is used with a mipmapped texture, LOD 0 gets sampled, unless the sampler has an LOD clamp which places the LOD somewhere else, or if there is an LOD Bias, which would simply bias starting from 0.</span></span> <span data-ttu-id="7bdf4-127">Poiché i derivati vengono ignorati, il filtro anisotropico si comporta come filtro di applicazione del filtro.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-127">Because derivatives are ignored, anisotropic filtering behaves as isotropic filtering.</span></span>

<span data-ttu-id="7bdf4-128">In pixel shader questa istruzione può essere usata all'interno di un controllo di flusso variabile quando le coordinate di trama sono derivate nello shader, a differenza dell' **esempio \_ c**.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-128">In Pixel Shaders, this instruction can be used inside varying flow control when the texture coordinates are derived in the shader, unlike **sample\_c**.</span></span>

<span data-ttu-id="7bdf4-129">Il recupero da uno slot di input a cui non è associato alcun elemento restituisce 0 per tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-129">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="7bdf4-130">Questa istruzione è disponibile in tutti gli shader, non solo nel pixel shader, per coerenza.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-130">This instruction is available in all shaders, not just the Pixel Shader, for consistency.</span></span>



| <span data-ttu-id="7bdf4-131">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="7bdf4-131">Vertex Shader</span></span> | <span data-ttu-id="7bdf4-132">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="7bdf4-132">Geometry Shader</span></span> | <span data-ttu-id="7bdf4-133">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="7bdf4-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7bdf4-134">X</span><span class="sxs-lookup"><span data-stu-id="7bdf4-134">X</span></span>             | <span data-ttu-id="7bdf4-135">X</span><span class="sxs-lookup"><span data-stu-id="7bdf4-135">X</span></span>               | <span data-ttu-id="7bdf4-136">x</span><span class="sxs-lookup"><span data-stu-id="7bdf4-136">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7bdf4-137">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="7bdf4-137">Minimum Shader Model</span></span>

<span data-ttu-id="7bdf4-138">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="7bdf4-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7bdf4-139">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="7bdf4-139">Shader Model</span></span>                                              | <span data-ttu-id="7bdf4-140">Supportato</span><span class="sxs-lookup"><span data-stu-id="7bdf4-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7bdf4-141">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="7bdf4-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7bdf4-142">sì</span><span class="sxs-lookup"><span data-stu-id="7bdf4-142">yes</span></span>       |
| [<span data-ttu-id="7bdf4-143">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="7bdf4-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7bdf4-144">sì</span><span class="sxs-lookup"><span data-stu-id="7bdf4-144">yes</span></span>       |
| [<span data-ttu-id="7bdf4-145">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="7bdf4-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7bdf4-146">sì</span><span class="sxs-lookup"><span data-stu-id="7bdf4-146">yes</span></span>       |
| [<span data-ttu-id="7bdf4-147">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7bdf4-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7bdf4-148">no</span><span class="sxs-lookup"><span data-stu-id="7bdf4-148">no</span></span>        |
| [<span data-ttu-id="7bdf4-149">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7bdf4-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7bdf4-150">no</span><span class="sxs-lookup"><span data-stu-id="7bdf4-150">no</span></span>        |
| [<span data-ttu-id="7bdf4-151">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7bdf4-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7bdf4-152">no</span><span class="sxs-lookup"><span data-stu-id="7bdf4-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7bdf4-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7bdf4-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bdf4-154">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7bdf4-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





