---
title: sample_l (SM4-ASM)
description: Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato. | sample_l (SM4-ASM)
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd83d81e4648cc9eae5f8e0166013dcca512a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353361"
---
# <a name="sample_l-sm4---asm"></a><span data-ttu-id="01acc-104">\_l di esempio (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="01acc-104">sample\_l (sm4 - asm)</span></span>

<span data-ttu-id="01acc-105">Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato.</span><span class="sxs-lookup"><span data-stu-id="01acc-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="01acc-106">esempio \_ l \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler, srcLOD. Select \_ Component</span><span class="sxs-lookup"><span data-stu-id="01acc-106">sample\_l\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcLOD.select\_component</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="01acc-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="01acc-107">Item</span></span>                                                                                                               | <span data-ttu-id="01acc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01acc-108">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01acc-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="01acc-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="01acc-110">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="01acc-110">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="01acc-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="01acc-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="01acc-112">\[in \] un set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="01acc-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="01acc-113">Per ulteriori informazioni, vedere l'istruzione di [esempio](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="01acc-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="01acc-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="01acc-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="01acc-115">\[in \] un registro di trama.</span><span class="sxs-lookup"><span data-stu-id="01acc-115">\[in\] A texture register.</span></span> <span data-ttu-id="01acc-116">Per ulteriori informazioni, vedere l'istruzione di **esempio** .</span><span class="sxs-lookup"><span data-stu-id="01acc-116">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="01acc-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="01acc-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="01acc-118">\[in \] un registro del campionatore.</span><span class="sxs-lookup"><span data-stu-id="01acc-118">\[in\] A sampler register.</span></span> <span data-ttu-id="01acc-119">Per ulteriori informazioni, vedere l'istruzione di **esempio** .</span><span class="sxs-lookup"><span data-stu-id="01acc-119">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="01acc-120"><span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*</span><span class="sxs-lookup"><span data-stu-id="01acc-120"><span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*</span></span><br/>                     | <span data-ttu-id="01acc-121">\[in \] LOD.</span><span class="sxs-lookup"><span data-stu-id="01acc-121">\[in\] The LOD.</span></span><br/>                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="01acc-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="01acc-122">Remarks</span></span>

<span data-ttu-id="01acc-123">Questa istruzione è identica a [Sample](sample--sm4---asm-.md), ad eccezione del fatto che il valore di LOD viene fornito direttamente dall'applicazione come valore scalare, che non rappresenta alcuna anisotropia.</span><span class="sxs-lookup"><span data-stu-id="01acc-123">This instruction is identical to [sample](sample--sm4---asm-.md), except that LOD is provided directly by the application as a scalar value, representing no anisotropy.</span></span> <span data-ttu-id="01acc-124">Questa istruzione è disponibile in tutte le fasi dello shader progammable.</span><span class="sxs-lookup"><span data-stu-id="01acc-124">This instruction is available in all progammable Shader stages.</span></span>

<span data-ttu-id="01acc-125">**esempio \_ l** esegue il campionamento della trama usando *srcLOD* come LOD.</span><span class="sxs-lookup"><span data-stu-id="01acc-125">**sample\_l** samples the texture using *srcLOD* to be the LOD.</span></span> <span data-ttu-id="01acc-126">Se il valore LOD è <= 0, viene scelto zero'th (maggiore mappa) con il filtro di ingrandimento applicato (se applicabile in base alla modalità di filtro).</span><span class="sxs-lookup"><span data-stu-id="01acc-126">If the LOD value is <= 0, the zero'th (biggest map) is chosen, with the magnify filter applied (if applicable based on the filter mode).</span></span> <span data-ttu-id="01acc-127">Dal momento che *srcLOD* è un valore a virgola mobile, il valore frazionario viene usato per interpolare tra due livelli MIP, se il filtro minimizzare è lineare o con filtro anisotropico.</span><span class="sxs-lookup"><span data-stu-id="01acc-127">Because *srcLOD* is a floating point value, the fractional value is used to interpolate between two mip levels, if the minify filter is LINEAR or with anisotropic filtering.</span></span>

<span data-ttu-id="01acc-128">l' **esempio \_ l** ignora i derivati degli indirizzi, quindi il comportamento del filtro è esclusivamente del filtro dei tipi.</span><span class="sxs-lookup"><span data-stu-id="01acc-128">**sample\_l** ignores address derivatives, so filtering behavior is purely isotropic.</span></span> <span data-ttu-id="01acc-129">Poiché i derivati vengono ignorati, il filtro anisotropico si comporta come filtro di applicazione del filtro.</span><span class="sxs-lookup"><span data-stu-id="01acc-129">Because derivatives are ignored, anisotropic filtering behaves as isotropic filtering.</span></span>

<span data-ttu-id="01acc-130">Gli Stati del campionatore MIPLODBIAS e MAX/MINMIPLEVEL vengono rispettati.</span><span class="sxs-lookup"><span data-stu-id="01acc-130">Sampler states MIPLODBIAS and MAX/MINMIPLEVEL are honored.</span></span>

<span data-ttu-id="01acc-131">Se usato nel pixel shader, l' **esempio \_ l** implica che la scelta di LOD è per pixel, senza alcun effetto dai pixel adiacenti, ad esempio nello stesso timbro 2x2.</span><span class="sxs-lookup"><span data-stu-id="01acc-131">When used in the Pixel Shader, **sample\_l** implies that the choice of LOD is per-pixel, with no effect from neighboring pixels, for example in the same 2x2 stamp.</span></span>

<span data-ttu-id="01acc-132">Il recupero da uno slot di input a cui non è associato alcun elemento restituisce 0 per tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="01acc-132">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="01acc-133">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="01acc-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="01acc-134">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="01acc-134">Vertex Shader</span></span> | <span data-ttu-id="01acc-135">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="01acc-135">Geometry Shader</span></span> | <span data-ttu-id="01acc-136">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="01acc-136">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="01acc-137">X</span><span class="sxs-lookup"><span data-stu-id="01acc-137">X</span></span>             | <span data-ttu-id="01acc-138">X</span><span class="sxs-lookup"><span data-stu-id="01acc-138">X</span></span>               | <span data-ttu-id="01acc-139">x</span><span class="sxs-lookup"><span data-stu-id="01acc-139">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="01acc-140">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="01acc-140">Minimum Shader Model</span></span>

<span data-ttu-id="01acc-141">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="01acc-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="01acc-142">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="01acc-142">Shader Model</span></span>                                              | <span data-ttu-id="01acc-143">Supportato</span><span class="sxs-lookup"><span data-stu-id="01acc-143">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="01acc-144">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="01acc-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="01acc-145">sì</span><span class="sxs-lookup"><span data-stu-id="01acc-145">yes</span></span>       |
| [<span data-ttu-id="01acc-146">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="01acc-146">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="01acc-147">sì</span><span class="sxs-lookup"><span data-stu-id="01acc-147">yes</span></span>       |
| [<span data-ttu-id="01acc-148">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="01acc-148">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="01acc-149">sì</span><span class="sxs-lookup"><span data-stu-id="01acc-149">yes</span></span>       |
| [<span data-ttu-id="01acc-150">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01acc-150">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="01acc-151">no</span><span class="sxs-lookup"><span data-stu-id="01acc-151">no</span></span>        |
| [<span data-ttu-id="01acc-152">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01acc-152">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="01acc-153">no</span><span class="sxs-lookup"><span data-stu-id="01acc-153">no</span></span>        |
| [<span data-ttu-id="01acc-154">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01acc-154">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="01acc-155">no</span><span class="sxs-lookup"><span data-stu-id="01acc-155">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="01acc-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="01acc-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01acc-157">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01acc-157">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





