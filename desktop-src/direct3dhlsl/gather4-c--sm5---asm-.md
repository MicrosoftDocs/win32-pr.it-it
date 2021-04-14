---
title: gather4_c (SM5-ASM)
description: Uguale a gather4, ad eccezione del fatto che questa operazione di Instrut esegue il confronto sui Texel, in modo simile all'esempio \_ c.
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35414aa2cd4d9f0686ab7a5cc17b94caa960cec1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993136"
---
# <a name="gather4_c-sm5---asm"></a><span data-ttu-id="bf31f-103">gather4 \_ c (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="bf31f-103">gather4\_c (sm5 - asm)</span></span>

<span data-ttu-id="bf31f-104">Uguale a [**gather4**](gather4--sm5---asm-.md), ad eccezione del fatto che questa operazione di Instrut esegue il confronto sui Texel, in modo simile all' [**esempio \_ c**](sample-c--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="bf31f-104">Same as [**gather4**](gather4--sm5---asm-.md), except this instrution performs comparison on texels, similar to [**sample\_c**](sample-c--sm4---asm-.md).</span></span>



| <span data-ttu-id="bf31f-105">gather4 \_ c \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . R \] , srcReferenceValue</span><span class="sxs-lookup"><span data-stu-id="bf31f-105">gather4\_c\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.R\], srcReferenceValue</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="bf31f-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="bf31f-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="bf31f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf31f-107">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf31f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="bf31f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="bf31f-109">\[nell' \] indirizzo del risultato dell'operazione</span><span class="sxs-lookup"><span data-stu-id="bf31f-109">\[in\] The address of the result of the operation</span></span><br/>                                    |
| <span data-ttu-id="bf31f-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="bf31f-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="bf31f-111">\[in \] un set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="bf31f-111">\[in\] A set of texture coordinates.</span></span><br/>                                                 |
| <span data-ttu-id="bf31f-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="bf31f-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="bf31f-113">\[in \] un registro di trama.</span><span class="sxs-lookup"><span data-stu-id="bf31f-113">\[in\] A texture register.</span></span><br/>                                                           |
| <span data-ttu-id="bf31f-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="bf31f-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="bf31f-115">\[in \] un registro del campionatore.</span><span class="sxs-lookup"><span data-stu-id="bf31f-115">\[in\] A sampler register.</span></span><br/>                                                           |
| <span data-ttu-id="bf31f-116"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="bf31f-116"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="bf31f-117">\[in \] un registro con un singolo componente selezionato, che viene utilizzato nel confronto.</span><span class="sxs-lookup"><span data-stu-id="bf31f-117">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bf31f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf31f-118">Remarks</span></span>

<span data-ttu-id="bf31f-119">Vedere l' [**esempio \_ c**](sample-c--sm4---asm-.md) per una descrizione del modo in cui *srcReferenceValue* viene confrontato con ogni Texel recuperato.</span><span class="sxs-lookup"><span data-stu-id="bf31f-119">See [**sample\_c**](sample-c--sm4---asm-.md) for a description of how *srcReferenceValue* gets compared against each fetched texel.</span></span> <span data-ttu-id="bf31f-120">A differenza dell' **esempio \_ c**, **gather4 \_ c** restituisce ogni risultato del confronto, anziché filtrarli.</span><span class="sxs-lookup"><span data-stu-id="bf31f-120">Unlike **sample\_c**, **gather4\_c** returns each comparison result, rather than filtering them.</span></span>

<span data-ttu-id="bf31f-121">Per gli angoli TextureCube, in cui sono presenti tre Texel reali ed è necessario sintetizzare un quarto, la sintesi deve verificarsi dopo il passaggio di confronto.</span><span class="sxs-lookup"><span data-stu-id="bf31f-121">For TextureCube corners, where there are three real texels and a fourth must be synthesized, the synthesis must occur after the comparison step.</span></span> <span data-ttu-id="bf31f-122">Ciò significa che il risultato del confronto restituito per sommarizza Texel può essere 0, 0,33, 0,66 o 1.</span><span class="sxs-lookup"><span data-stu-id="bf31f-122">This means the returned comparison result for the syntesized texel can be 0, 0.33 , 0.66 , or 1.</span></span> <span data-ttu-id="bf31f-123">Alcune implementazioni possono restituire solo 0 o 1 per il Texel sintetizzato.</span><span class="sxs-lookup"><span data-stu-id="bf31f-123">Some implementations may only return either 0 or 1 for the synthesized texel.</span></span> <span data-ttu-id="bf31f-124">A parte questo elenco di risultati possibili, il metodo per sintetizzare il Texel non è specificato.</span><span class="sxs-lookup"><span data-stu-id="bf31f-124">Aside from this listing of possible results, the method for synthesizing the texel is unspecified.</span></span>

<span data-ttu-id="bf31f-125">Per i formati con componenti float32, se il valore recuperato è normalizzato, o +-INF, viene usato nell'operazione di confronto non toccata.</span><span class="sxs-lookup"><span data-stu-id="bf31f-125">For formats with float32 components, if the value being fetched is normalized, or +-INF, it is used in the comparison operation untouched.</span></span> <span data-ttu-id="bf31f-126">NaN viene utilizzato nell'operazione di confronto come NaN, ma è possibile modificare la rappresentazione di bit esatta di NaN.</span><span class="sxs-lookup"><span data-stu-id="bf31f-126">NaN is used in the comparison operation as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="bf31f-127">Le denormazioni vengono scaricate fino a zero nel confronto.</span><span class="sxs-lookup"><span data-stu-id="bf31f-127">Denorms are flushed to zero going into the comparison.</span></span> <span data-ttu-id="bf31f-128">Per TextureCubes, alcune sintesi del quarto Texel mancante devono verificarsi negli angoli, quindi la nozione di restituzione di bit invariati per il Texel sintetizzato non è applicabile.</span><span class="sxs-lookup"><span data-stu-id="bf31f-128">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply.</span></span>

<span data-ttu-id="bf31f-129">I formati supportati per *gather4 \_ c* sono identici a quelli supportati per l' *esempio \_ c*.</span><span class="sxs-lookup"><span data-stu-id="bf31f-129">Formats supported for *gather4\_c* are same as those supported for *sample\_c*.</span></span> <span data-ttu-id="bf31f-130">Si tratta di formati a componente singolo, di conseguenza. R su *srcSampler*, anziché un swizzle arbitrario.</span><span class="sxs-lookup"><span data-stu-id="bf31f-130">These are single-component formats, thus the .R on *srcSampler*, rather than an arbitrary swizzle.</span></span> <span data-ttu-id="bf31f-131">**gather4 \_ c** in una risorsa non associata restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="bf31f-131">**gather4\_c** on an unbound resource returns 0.</span></span>

<span data-ttu-id="bf31f-132">Usare questa istruzione per il filtro personalizzato della mappa Shadow.</span><span class="sxs-lookup"><span data-stu-id="bf31f-132">Use this instruction for custom shadow map filtering.</span></span>

<span data-ttu-id="bf31f-133">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="bf31f-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bf31f-134">Vertice</span><span class="sxs-lookup"><span data-stu-id="bf31f-134">Vertex</span></span> | <span data-ttu-id="bf31f-135">Hull</span><span class="sxs-lookup"><span data-stu-id="bf31f-135">Hull</span></span> | <span data-ttu-id="bf31f-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="bf31f-136">Domain</span></span> | <span data-ttu-id="bf31f-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="bf31f-137">Geometry</span></span> | <span data-ttu-id="bf31f-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="bf31f-138">Pixel</span></span> | <span data-ttu-id="bf31f-139">Calcolo</span><span class="sxs-lookup"><span data-stu-id="bf31f-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bf31f-140">X</span><span class="sxs-lookup"><span data-stu-id="bf31f-140">X</span></span>      | <span data-ttu-id="bf31f-141">X</span><span class="sxs-lookup"><span data-stu-id="bf31f-141">X</span></span>    | <span data-ttu-id="bf31f-142">X</span><span class="sxs-lookup"><span data-stu-id="bf31f-142">X</span></span>      | <span data-ttu-id="bf31f-143">X</span><span class="sxs-lookup"><span data-stu-id="bf31f-143">X</span></span>        | <span data-ttu-id="bf31f-144">X</span><span class="sxs-lookup"><span data-stu-id="bf31f-144">X</span></span>     | <span data-ttu-id="bf31f-145">X</span><span class="sxs-lookup"><span data-stu-id="bf31f-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bf31f-146">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="bf31f-146">Minimum Shader Model</span></span>

<span data-ttu-id="bf31f-147">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="bf31f-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="bf31f-148">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="bf31f-148">Shader Model</span></span>                                              | <span data-ttu-id="bf31f-149">Supportato</span><span class="sxs-lookup"><span data-stu-id="bf31f-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bf31f-150">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="bf31f-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bf31f-151">sì</span><span class="sxs-lookup"><span data-stu-id="bf31f-151">yes</span></span>       |
| [<span data-ttu-id="bf31f-152">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="bf31f-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bf31f-153">no</span><span class="sxs-lookup"><span data-stu-id="bf31f-153">no</span></span>        |
| [<span data-ttu-id="bf31f-154">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="bf31f-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bf31f-155">no</span><span class="sxs-lookup"><span data-stu-id="bf31f-155">no</span></span>        |
| [<span data-ttu-id="bf31f-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf31f-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bf31f-157">no</span><span class="sxs-lookup"><span data-stu-id="bf31f-157">no</span></span>        |
| [<span data-ttu-id="bf31f-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf31f-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bf31f-159">no</span><span class="sxs-lookup"><span data-stu-id="bf31f-159">no</span></span>        |
| [<span data-ttu-id="bf31f-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf31f-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bf31f-161">no</span><span class="sxs-lookup"><span data-stu-id="bf31f-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bf31f-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf31f-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf31f-163">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf31f-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





