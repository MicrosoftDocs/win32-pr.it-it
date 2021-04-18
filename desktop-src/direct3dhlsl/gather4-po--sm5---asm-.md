---
title: gather4_po (SM5-ASM)
description: Variante di gather4, ma anziché supportare un offset immediato \-8.. 7 \, l'offset viene visualizzato come parametro per l'istruzione e dispone anche di un intervallo più ampio di \-32.. 31 \.
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9197fee97645333d37d589db36c3774852b12229
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976426"
---
# <a name="gather4_po-sm5---asm"></a><span data-ttu-id="e85dd-103">gather4 \_ po (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e85dd-103">gather4\_po (sm5 - asm)</span></span>

<span data-ttu-id="e85dd-104">Variante di [gather4](gather4--sm5---asm-.md), ma anziché supportare un offset immediato \[ -8.. 7 \] , l'offset viene visualizzato come parametro per l'istruzione e dispone anche di un intervallo più ampio di \[ -32.. 31 \] .</span><span class="sxs-lookup"><span data-stu-id="e85dd-104">A variant of [gather4](gather4--sm5---asm-.md), but instead of supporting an immediate offset \[-8..7\], the offset comes as a parameter to the instruction, and also has larger range of \[-32..31\].</span></span>



| <span data-ttu-id="e85dd-105">gather4 \_ po dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcOffset \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="e85dd-105">gather4\_po dest\[.mask\], srcAddress\[.swizzle\], srcOffset\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.select\_component\]</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e85dd-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="e85dd-106">Item</span></span>                                                                                                               | <span data-ttu-id="e85dd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e85dd-107">Description</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e85dd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e85dd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="e85dd-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e85dd-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="e85dd-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="e85dd-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="e85dd-111">\[in \] un set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="e85dd-111">\[in\] A set of texture coordinates.</span></span><br/>               |
| <span data-ttu-id="e85dd-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span><span class="sxs-lookup"><span data-stu-id="e85dd-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span></span><br/>         | <span data-ttu-id="e85dd-113">\[nell' \] offset.</span><span class="sxs-lookup"><span data-stu-id="e85dd-113">\[in\] The offset.</span></span><br/>                                 |
| <span data-ttu-id="e85dd-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="e85dd-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="e85dd-115">\[in \] un registro di trama.</span><span class="sxs-lookup"><span data-stu-id="e85dd-115">\[in\] A texture register.</span></span><br/>                         |
| <span data-ttu-id="e85dd-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="e85dd-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="e85dd-117">\[in \] un registro del campionatore.</span><span class="sxs-lookup"><span data-stu-id="e85dd-117">\[in\] A sampler register.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="e85dd-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="e85dd-118">Remarks</span></span>

<span data-ttu-id="e85dd-119">I primi due componenti del parametro offset a 4 vettori forniscono offset integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="e85dd-119">The first two components of the 4-vector offset parameter supply 32-bit integer offsets.</span></span> <span data-ttu-id="e85dd-120">Gli altri componenti di questo parametro vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="e85dd-120">The other components of this parameter are ignored.</span></span>

<span data-ttu-id="e85dd-121">I 6 bit meno significativi di ogni valore di offset vengono rispettati come valore con segno, producendo un \[ intervallo di-32.. 31. \]</span><span class="sxs-lookup"><span data-stu-id="e85dd-121">The 6 least significant bits of each offset value is honored as a signed value, yielding \[-32..31\] range.</span></span>

<span data-ttu-id="e85dd-122">Questa istruzione funziona solo con le trame 2D, a differenza di **gather4**, che funziona anche con TextureCubes.</span><span class="sxs-lookup"><span data-stu-id="e85dd-122">This instruction only works with 2D textures, unlike **gather4**, which also works with TextureCubes.</span></span>

<span data-ttu-id="e85dd-123">Le uniche modalità rispettate nel campionatore sono le modalità di indirizzamento.</span><span class="sxs-lookup"><span data-stu-id="e85dd-123">The only modes honored in the sampler are the addressing modes.</span></span> <span data-ttu-id="e85dd-124">Viene utilizzata solo la MIP più dettagliata nella visualizzazione risorse.</span><span class="sxs-lookup"><span data-stu-id="e85dd-124">Only the most detailed mip in the resource view is used.</span></span>

<span data-ttu-id="e85dd-125">Se l'indirizzo cade in un centro Texel, questo non significa che gli altri Texel possono essere azzerati.</span><span class="sxs-lookup"><span data-stu-id="e85dd-125">If the address falls on a texel center, this does not mean the other texels can be zeroed out.</span></span>

<span data-ttu-id="e85dd-126">Il parametro *srcSampler* include \[ . Select ( \_ componente), che consente il recupero di \] qualsiasi singolo componente di una trama, inclusa la restituzione di valori predefiniti per i componenti mancanti.</span><span class="sxs-lookup"><span data-stu-id="e85dd-126">The *srcSampler* parameter includes \[.select\_component\], allowing any single component of a texture to be retrieved, including returning defaults for missing components.</span></span>

<span data-ttu-id="e85dd-127">Per i formati con componenti float32, se il valore recuperato è normalizzato, denormalizzato, +-0 o +-INF, viene restituito allo shader inalterato.</span><span class="sxs-lookup"><span data-stu-id="e85dd-127">For formats with float32 components, if the value being fetched is normalized, denormalized, +-0 or +-INF, it is returned to the shader unaltered.</span></span> <span data-ttu-id="e85dd-128">NaN viene restituito come NaN, ma la rappresentazione di bit esatta di NaN può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="e85dd-128">NaN is returned as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="e85dd-129">Per TextureCubes, alcune sintesi del quarto Texel mancante devono verificarsi negli angoli, quindi la nozione di restituzione di bit invariati per il Texel sintetizzato non si applica e le denormazioni potrebbero essere scaricate.</span><span class="sxs-lookup"><span data-stu-id="e85dd-129">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply, and denorms could be flushed.</span></span>

<span data-ttu-id="e85dd-130">Usare questa istruzione per estendere l'intervallo di offset di **gather4** in modo che sia più grande e programmabile.</span><span class="sxs-lookup"><span data-stu-id="e85dd-130">Use this instruction to extend offset range of **gather4** to be larger and programmable.</span></span> <span data-ttu-id="e85dd-131">Il suffisso "po" sul nome indica "offset programmabile".</span><span class="sxs-lookup"><span data-stu-id="e85dd-131">The "po" suffix on the name means "programmable offset".</span></span>

<span data-ttu-id="e85dd-132">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e85dd-132">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e85dd-133">Vertice</span><span class="sxs-lookup"><span data-stu-id="e85dd-133">Vertex</span></span> | <span data-ttu-id="e85dd-134">Hull</span><span class="sxs-lookup"><span data-stu-id="e85dd-134">Hull</span></span> | <span data-ttu-id="e85dd-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="e85dd-135">Domain</span></span> | <span data-ttu-id="e85dd-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="e85dd-136">Geometry</span></span> | <span data-ttu-id="e85dd-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="e85dd-137">Pixel</span></span> | <span data-ttu-id="e85dd-138">Calcolo</span><span class="sxs-lookup"><span data-stu-id="e85dd-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e85dd-139">X</span><span class="sxs-lookup"><span data-stu-id="e85dd-139">X</span></span>      | <span data-ttu-id="e85dd-140">X</span><span class="sxs-lookup"><span data-stu-id="e85dd-140">X</span></span>    | <span data-ttu-id="e85dd-141">X</span><span class="sxs-lookup"><span data-stu-id="e85dd-141">X</span></span>      | <span data-ttu-id="e85dd-142">X</span><span class="sxs-lookup"><span data-stu-id="e85dd-142">X</span></span>        | <span data-ttu-id="e85dd-143">X</span><span class="sxs-lookup"><span data-stu-id="e85dd-143">X</span></span>     | <span data-ttu-id="e85dd-144">X</span><span class="sxs-lookup"><span data-stu-id="e85dd-144">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e85dd-145">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="e85dd-145">Minimum Shader Model</span></span>

<span data-ttu-id="e85dd-146">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e85dd-146">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e85dd-147">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="e85dd-147">Shader Model</span></span>                                              | <span data-ttu-id="e85dd-148">Supportato</span><span class="sxs-lookup"><span data-stu-id="e85dd-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e85dd-149">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="e85dd-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e85dd-150">sì</span><span class="sxs-lookup"><span data-stu-id="e85dd-150">yes</span></span>       |
| [<span data-ttu-id="e85dd-151">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="e85dd-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e85dd-152">no</span><span class="sxs-lookup"><span data-stu-id="e85dd-152">no</span></span>        |
| [<span data-ttu-id="e85dd-153">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="e85dd-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e85dd-154">no</span><span class="sxs-lookup"><span data-stu-id="e85dd-154">no</span></span>        |
| [<span data-ttu-id="e85dd-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e85dd-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e85dd-156">no</span><span class="sxs-lookup"><span data-stu-id="e85dd-156">no</span></span>        |
| [<span data-ttu-id="e85dd-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e85dd-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e85dd-158">no</span><span class="sxs-lookup"><span data-stu-id="e85dd-158">no</span></span>        |
| [<span data-ttu-id="e85dd-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e85dd-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e85dd-160">no</span><span class="sxs-lookup"><span data-stu-id="e85dd-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e85dd-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e85dd-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e85dd-162">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e85dd-162">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





