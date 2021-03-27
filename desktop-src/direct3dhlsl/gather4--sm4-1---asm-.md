---
title: gather4 (SM 4.1-ASM)
description: Raccoglie i quattro Texel che verrebbero usati in un'operazione di filtraggio bilineare e li imballa in un unico registro. | gather4 (SM 4.1-ASM)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84387bfe027e30b338b4701ec941a9d4e1b5e242
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981559"
---
# <a name="gather4-sm41---asm"></a><span data-ttu-id="db99e-104">gather4 (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="db99e-104">gather4 (sm4.1 - asm)</span></span>

<span data-ttu-id="db99e-105">Raccoglie i quattro Texel che verrebbero usati in un'operazione di filtraggio bilineare e li imballa in un unico registro.</span><span class="sxs-lookup"><span data-stu-id="db99e-105">Gathers the four texels that would be used in a bi-linear filtering operation and packs them into a single register.</span></span>



| <span data-ttu-id="db99e-106">gather4 \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] srcSampler. r</span><span class="sxs-lookup"><span data-stu-id="db99e-106">gather4\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\] srcSampler.r</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="db99e-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="db99e-107">Item</span></span>                                                                                                               | <span data-ttu-id="db99e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db99e-108">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db99e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="db99e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="db99e-110">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="db99e-110">\[in\] The address of the result of the operation.</span></span><br/>                                                                                                       |
| <span data-ttu-id="db99e-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="db99e-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="db99e-112">\[in \] contiene le coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="db99e-112">\[in\] Contains the texture coordinates.</span></span> <br/>                                                                                                                |
| <span data-ttu-id="db99e-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="db99e-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="db99e-114">\[in \] un registro delle risorse.</span><span class="sxs-lookup"><span data-stu-id="db99e-114">\[in\] A resource register.</span></span> <br/> <span data-ttu-id="db99e-115">Swizzle consente il swizzled arbitrario dei valori restituiti prima che vengano scritti in *dest*.</span><span class="sxs-lookup"><span data-stu-id="db99e-115">The swizzle allows the returned values to be swizzled arbitrarily before they are written to *dest*.</span></span> <br/>            |
| <span data-ttu-id="db99e-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="db99e-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="db99e-117">\[in \] un registro del campionatore.</span><span class="sxs-lookup"><span data-stu-id="db99e-117">\[in\] A sampler register.</span></span><br/> <span data-ttu-id="db99e-118">Questo parametro deve avere un Swizzle. r (rosso), che indica che il valore del canale R viene copiato in *dest*.</span><span class="sxs-lookup"><span data-stu-id="db99e-118">This parameter must have a .r (red) swizzle, which indicates that the value of the R channel is copied to *dest*.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="db99e-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="db99e-119">Remarks</span></span>

<span data-ttu-id="db99e-120">Questa operazione funziona solo con trame 2D o mappa cubi a canale singolo.</span><span class="sxs-lookup"><span data-stu-id="db99e-120">This operation only works with single channel 2D or CubeMap textures.</span></span> <span data-ttu-id="db99e-121">Per le trame 2D vengono usate solo le modalità di indirizzamento del campionatore e viene usato il livello superiore di qualsiasi piramide MIP.</span><span class="sxs-lookup"><span data-stu-id="db99e-121">For 2D textures only the addressing modes of the sampler are used and the top level of any mip pyramid is used.</span></span>

<span data-ttu-id="db99e-122">Questa istruzione si comporta come l'istruzione di [esempio](sample--sm4---asm-.md) , ma non viene generato un campione filtrato.</span><span class="sxs-lookup"><span data-stu-id="db99e-122">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="db99e-123">I quattro esempi che contribuiscono al filtraggio vengono inseriti in xyzw in senso antiorario a partire dall'esempio in basso a sinistra della posizione sottoposta a query.</span><span class="sxs-lookup"><span data-stu-id="db99e-123">The four samples that would contribute to filtering are placed into xyzw in counter clockwise order starting with the sample to the lower left of the queried location.</span></span> <span data-ttu-id="db99e-124">Equivale al campionamento dei punti con (u, v) le coordinate di trama Delta nei percorsi seguenti: (-, +), (+, +), (+,-), (-,-), dove la grandezza dei Delta è sempre metà di un Texel.</span><span class="sxs-lookup"><span data-stu-id="db99e-124">This is the same as point sampling with (u,v) texture coordinate deltas at the following locations: (-,+),(+,+),(+,-),(-,-), where the magnitude of the deltas are always half a texel.</span></span>

<span data-ttu-id="db99e-125">Per le trame mappa cubi quando un footprint bidirezionale si estende su un Texel perimetrale dal volto adiacente vengono usati.</span><span class="sxs-lookup"><span data-stu-id="db99e-125">For CubeMap textures when a bi-linear footprint spans an edge texels from the neighboring face are used.</span></span> <span data-ttu-id="db99e-126">Gli angoli utilizzano le stesse regole dell'istruzione di **esempio** ; ovvero l'angolo sconosciuto è considerato la media dei tre angoli della faccia con inping.</span><span class="sxs-lookup"><span data-stu-id="db99e-126">Corners use the same rules as the **sample** instruction; that is the unkown corner is considered the average of the three impinging face corners.</span></span>

<span data-ttu-id="db99e-127">Le restrizioni relative al formato di trama applicabili alle istruzioni di **esempio** sono valide anche per l'istruzione **gather4** .</span><span class="sxs-lookup"><span data-stu-id="db99e-127">The texture format restrictions that apply to the **sample** instructions also apply to the **gather4** instruction.</span></span>

<span data-ttu-id="db99e-128">Per le implementazioni dell'hardware, le ottimizzazioni nei filtri bilineari tradizionali che rilevano esempi direttamente nei Texel e ignorano la lettura di Texel che non possono essere utilizzate con **gather4**.</span><span class="sxs-lookup"><span data-stu-id="db99e-128">For hardware implementations, optimizations in traditional bilinear filtering that detect samples directly on texels and skip reading of texels that would have weight 0 cannot be leveraged with **gather4**.</span></span> <span data-ttu-id="db99e-129">**gather4** restituisce sempre tutti i Texel richiesti.</span><span class="sxs-lookup"><span data-stu-id="db99e-129">**gather4** always returns all requested texels.</span></span>

<span data-ttu-id="db99e-130">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="db99e-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="db99e-131">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="db99e-131">Vertex Shader</span></span> | <span data-ttu-id="db99e-132">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="db99e-132">Geometry Shader</span></span> | <span data-ttu-id="db99e-133">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="db99e-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="db99e-134">x</span><span class="sxs-lookup"><span data-stu-id="db99e-134">x</span></span>             | <span data-ttu-id="db99e-135">x</span><span class="sxs-lookup"><span data-stu-id="db99e-135">x</span></span>               | <span data-ttu-id="db99e-136">x</span><span class="sxs-lookup"><span data-stu-id="db99e-136">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="db99e-137">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="db99e-137">Minimum Shader Model</span></span>

<span data-ttu-id="db99e-138">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="db99e-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="db99e-139">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="db99e-139">Shader Model</span></span>                                              | <span data-ttu-id="db99e-140">Supportato</span><span class="sxs-lookup"><span data-stu-id="db99e-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="db99e-141">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="db99e-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="db99e-142">sì</span><span class="sxs-lookup"><span data-stu-id="db99e-142">yes</span></span>       |
| [<span data-ttu-id="db99e-143">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="db99e-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="db99e-144">sì</span><span class="sxs-lookup"><span data-stu-id="db99e-144">yes</span></span>       |
| [<span data-ttu-id="db99e-145">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="db99e-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="db99e-146">no</span><span class="sxs-lookup"><span data-stu-id="db99e-146">no</span></span>        |
| [<span data-ttu-id="db99e-147">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db99e-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="db99e-148">no</span><span class="sxs-lookup"><span data-stu-id="db99e-148">no</span></span>        |
| [<span data-ttu-id="db99e-149">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db99e-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="db99e-150">no</span><span class="sxs-lookup"><span data-stu-id="db99e-150">no</span></span>        |
| [<span data-ttu-id="db99e-151">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db99e-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="db99e-152">no</span><span class="sxs-lookup"><span data-stu-id="db99e-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="db99e-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db99e-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db99e-154">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db99e-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





