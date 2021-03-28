---
title: gather4 (SM5-ASM)
description: Raccoglie i quattro Texel che verrebbero usati in un'operazione di filtraggio bilineare e li imballa in un unico registro. | gather4 (SM5-ASM)
ms.assetid: 5F93BB70-7696-48E4-BCD3-91D5D42FF63E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5657265738f12331afc7596286f02170de2a635
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234710"
---
# <a name="gather4-sm5---asm"></a><span data-ttu-id="dea93-104">gather4 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="dea93-104">gather4 (sm5 - asm)</span></span>

<span data-ttu-id="dea93-105">Raccoglie i quattro Texel che verrebbero usati in un'operazione di filtraggio bilineare e li imballa in un unico registro.</span><span class="sxs-lookup"><span data-stu-id="dea93-105">Gathers the four texels that would be used in a bi-linear filtering operation and packs them into a single register.</span></span> <span data-ttu-id="dea93-106">Questa istruzione funziona solo con trame 2D o mappa cubi, incluse le matrici.</span><span class="sxs-lookup"><span data-stu-id="dea93-106">This instruction only works with 2D or CubeMap textures, including arrays.</span></span> <span data-ttu-id="dea93-107">Vengono utilizzate solo le modalità di indirizzamento del campionatore e viene utilizzato il livello principale di qualsiasi piramide MIP.</span><span class="sxs-lookup"><span data-stu-id="dea93-107">Only the addressing modes of the sampler are used and the top level of any mip pyramid is used.</span></span>



| <span data-ttu-id="dea93-108">gather4 \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="dea93-108">gather4\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.select\_component\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="dea93-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="dea93-109">Item</span></span>                                                                                                               | <span data-ttu-id="dea93-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dea93-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="dea93-111"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="dea93-111"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="dea93-112">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dea93-112">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="dea93-113"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="dea93-113"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="dea93-114">\[in \] un set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="dea93-114">\[in\] A set of texture coordinates.</span></span><br/>                |
| <span data-ttu-id="dea93-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="dea93-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="dea93-116">\[in \] un registro di trama.</span><span class="sxs-lookup"><span data-stu-id="dea93-116">\[in\] A texture register.</span></span><br/>                          |
| <span data-ttu-id="dea93-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="dea93-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="dea93-118">\[in \] un registro del campionatore.</span><span class="sxs-lookup"><span data-stu-id="dea93-118">\[in\] A sampler register.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="dea93-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="dea93-119">Remarks</span></span>

<span data-ttu-id="dea93-120">Questa istruzione si comporta come l'istruzione di [**esempio**](sample--sm4---asm-.md) , ma non viene generato un campione filtrato.</span><span class="sxs-lookup"><span data-stu-id="dea93-120">This instruction behaves like the [**sample**](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="dea93-121">I quattro esempi che contribuiscono al filtraggio vengono inseriti in xyzw in senso antiorario a partire dall'esempio in basso a sinistra della posizione sottoposta a query.</span><span class="sxs-lookup"><span data-stu-id="dea93-121">The four samples that would contribute to filtering are placed into xyzw in counter clockwise order starting with the sample to the lower left of the queried location.</span></span> <span data-ttu-id="dea93-122">Equivale al campionamento dei punti con (u, v) le coordinate di trama Delta nei percorsi seguenti: (-, +), (+, +), (+,-), (-,-), dove la grandezza dei Delta è sempre metà di un Texel.</span><span class="sxs-lookup"><span data-stu-id="dea93-122">This is the same as point sampling with (u,v) texture coordinate deltas at the following locations: (-,+),(+,+),(+,-),(-,-), where the magnitude of the deltas are always half a texel.</span></span>

<span data-ttu-id="dea93-123">Per le trame mappa cubi, quando un'impronta bi lineare si estende su un bordo, vengono usati i Texel del volto adiacente.</span><span class="sxs-lookup"><span data-stu-id="dea93-123">For CubeMap textures, when a bi-linear footprint spans an edge, texels from the neighboring face are used.</span></span> <span data-ttu-id="dea93-124">Gli angoli utilizzano le stesse regole dell'istruzione di [**esempio**](sample--sm4---asm-.md) ; ovvero, l'angolo sconosciuto viene considerato la media dei tre angoli della faccia di cui si sta effettuando il ping.</span><span class="sxs-lookup"><span data-stu-id="dea93-124">Corners use the same rules as the [**sample**](sample--sm4---asm-.md) instruction; that is, the unknown corner is considered the average of the three impinging face corners.</span></span>

<span data-ttu-id="dea93-125">Sono presenti restrizioni relative al formato di trama che si applicano a **gather4** , espresse nell'elenco dei formati.</span><span class="sxs-lookup"><span data-stu-id="dea93-125">There are texture format restrictions that apply to **gather4** which are expressed in the format list.</span></span>

<span data-ttu-id="dea93-126">Swizzle in *srcResource* consente di swizzled arbitrariamente i valori restituiti prima che vengano scritti nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="dea93-126">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="dea93-127">Il componente. Select \_ in *srcSampler* sceglie il componente della trama di origine (r/g/b/a) da cui leggere 4 Texel.</span><span class="sxs-lookup"><span data-stu-id="dea93-127">The .select\_component on *srcSampler* chooses which component of the source texture (r/g/b/a) to read 4 texels from.</span></span>

<span data-ttu-id="dea93-128">Per i formati con componenti float32, se il valore recuperato è normalizzato, denormalizzato, +-0 o +-INF, viene restituito allo shader inalterato.</span><span class="sxs-lookup"><span data-stu-id="dea93-128">For formats with float32 components, if the value being fetched is normalized, denormalized, +-0 or +-INF, it is returned to the shader unaltered.</span></span> <span data-ttu-id="dea93-129">NaN viene restituito come NaN, ma la rappresentazione di bit esatta di NaN può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="dea93-129">NaN is returned as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="dea93-130">Per TextureCubes, alcune sintesi del quarto Texel mancante devono verificarsi in corrispondenza degli angoli, quindi la restituzione di bit invariati per il Texel sintetizzato non si applica e le denormazioni potrebbero essere scaricate.</span><span class="sxs-lookup"><span data-stu-id="dea93-130">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so returning bits unchanged for the synthesized texel does not apply, and denorms could be flushed.</span></span>

<span data-ttu-id="dea93-131">Per le implementazioni dell'hardware, le ottimizzazioni nei filtri bilineari tradizionali che rilevano esempi direttamente nei Texel e ignorano la lettura di Texel che non possono essere utilizzate con questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="dea93-131">For hardware implementations, optimizations in traditional bilinear filtering that detect samples directly on texels and skip reading of texels that would have weight 0 cannot be leveraged with this instruction.</span></span> <span data-ttu-id="dea93-132">*gather4* restituisce sempre tutti i Texel richiesti.</span><span class="sxs-lookup"><span data-stu-id="dea93-132">*gather4* always returns all requested texels.</span></span>

<span data-ttu-id="dea93-133">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="dea93-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dea93-134">Vertice</span><span class="sxs-lookup"><span data-stu-id="dea93-134">Vertex</span></span> | <span data-ttu-id="dea93-135">Hull</span><span class="sxs-lookup"><span data-stu-id="dea93-135">Hull</span></span> | <span data-ttu-id="dea93-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="dea93-136">Domain</span></span> | <span data-ttu-id="dea93-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="dea93-137">Geometry</span></span> | <span data-ttu-id="dea93-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="dea93-138">Pixel</span></span> | <span data-ttu-id="dea93-139">Calcolo</span><span class="sxs-lookup"><span data-stu-id="dea93-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="dea93-140">X</span><span class="sxs-lookup"><span data-stu-id="dea93-140">X</span></span>      | <span data-ttu-id="dea93-141">X</span><span class="sxs-lookup"><span data-stu-id="dea93-141">X</span></span>    | <span data-ttu-id="dea93-142">X</span><span class="sxs-lookup"><span data-stu-id="dea93-142">X</span></span>      | <span data-ttu-id="dea93-143">X</span><span class="sxs-lookup"><span data-stu-id="dea93-143">X</span></span>        | <span data-ttu-id="dea93-144">X</span><span class="sxs-lookup"><span data-stu-id="dea93-144">X</span></span>     | <span data-ttu-id="dea93-145">X</span><span class="sxs-lookup"><span data-stu-id="dea93-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dea93-146">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="dea93-146">Minimum Shader Model</span></span>

<span data-ttu-id="dea93-147">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="dea93-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="dea93-148">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="dea93-148">Shader Model</span></span>                                              | <span data-ttu-id="dea93-149">Supportato</span><span class="sxs-lookup"><span data-stu-id="dea93-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dea93-150">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="dea93-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dea93-151">sì</span><span class="sxs-lookup"><span data-stu-id="dea93-151">yes</span></span>       |
| [<span data-ttu-id="dea93-152">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="dea93-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dea93-153">no</span><span class="sxs-lookup"><span data-stu-id="dea93-153">no</span></span>        |
| [<span data-ttu-id="dea93-154">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="dea93-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dea93-155">no</span><span class="sxs-lookup"><span data-stu-id="dea93-155">no</span></span>        |
| [<span data-ttu-id="dea93-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dea93-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dea93-157">no</span><span class="sxs-lookup"><span data-stu-id="dea93-157">no</span></span>        |
| [<span data-ttu-id="dea93-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dea93-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dea93-159">no</span><span class="sxs-lookup"><span data-stu-id="dea93-159">no</span></span>        |
| [<span data-ttu-id="dea93-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dea93-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dea93-161">no</span><span class="sxs-lookup"><span data-stu-id="dea93-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dea93-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dea93-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dea93-163">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dea93-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





