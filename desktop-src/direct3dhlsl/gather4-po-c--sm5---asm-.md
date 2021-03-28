---
title: gather4_po_c (SM5-ASM)
description: Si comporta allo stesso modo di gather4 \_ po, ad eccezione delle operazioni di confronto sui Texel, in modo simile all'esempio \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b07dcad08b4d117a453a3c97e461e6b9b4cab6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398275"
---
# <a name="gather4_po_c-sm5---asm"></a><span data-ttu-id="b53d1-103">gather4 \_ po \_ c (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b53d1-103">gather4\_po\_c (sm5 - asm)</span></span>

<span data-ttu-id="b53d1-104">Si comporta allo stesso modo di [**gather4 \_ po**](gather4-po--sm5---asm-.md), ad eccezione delle operazioni di confronto sui Texel, in modo simile all' [**esempio \_ c**](sample-c--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="b53d1-104">Behaves the same as [**gather4\_po**](gather4-po--sm5---asm-.md), except performs comparison on texels, similar to [**sample\_c**](sample-c--sm4---asm-.md).</span></span>



| <span data-ttu-id="b53d1-105">gather4 \_ po \_ c dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcOffset \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . R \] , srcReferenceValue</span><span class="sxs-lookup"><span data-stu-id="b53d1-105">gather4\_po\_c dest\[.mask\], srcAddress\[.swizzle\], srcOffset\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.R\], srcReferenceValue</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b53d1-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="b53d1-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="b53d1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b53d1-107">Description</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b53d1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b53d1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="b53d1-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b53d1-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="b53d1-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="b53d1-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="b53d1-111">\[in \] un set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="b53d1-111">\[in\] A set of texture coordinates.</span></span><br/>               |
| <span data-ttu-id="b53d1-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span><span class="sxs-lookup"><span data-stu-id="b53d1-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span></span><br/>                                 | <span data-ttu-id="b53d1-113">\[nell' \] offset.</span><span class="sxs-lookup"><span data-stu-id="b53d1-113">\[in\] The offset.</span></span><br/>                                 |
| <span data-ttu-id="b53d1-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="b53d1-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="b53d1-115">\[in \] un registro di trama.</span><span class="sxs-lookup"><span data-stu-id="b53d1-115">\[in\] A texture register.</span></span><br/>                         |
| <span data-ttu-id="b53d1-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="b53d1-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="b53d1-117">\[in \] un registro del campionatore.</span><span class="sxs-lookup"><span data-stu-id="b53d1-117">\[in\] A sampler register.</span></span><br/>                         |
| <span data-ttu-id="b53d1-118"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="b53d1-118"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="b53d1-119">\[in \] singolo componente selezionato.</span><span class="sxs-lookup"><span data-stu-id="b53d1-119">\[in\] Single component selected.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b53d1-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="b53d1-120">Remarks</span></span>

<span data-ttu-id="b53d1-121">Vedere l' [**esempio \_ c**](sample-c--sm4---asm-.md) per informazioni sulla modalità di confronto di *srcReferenceValue* con ogni Texel recuperato.</span><span class="sxs-lookup"><span data-stu-id="b53d1-121">See [**sample\_c**](sample-c--sm4---asm-.md) for information about how *srcReferenceValue* is compared against each fetched texel.</span></span> <span data-ttu-id="b53d1-122">A differenza di **esempio \_ c**, *gather4 \_ po \_ c* restituisce ogni risultato del confronto, anziché filtrarli.</span><span class="sxs-lookup"><span data-stu-id="b53d1-122">Unlike **sample\_c**, *gather4\_po\_c* returns each comparison result, rather than filtering them.</span></span>

<span data-ttu-id="b53d1-123">Questa istruzione, come **gather4 \_ po**, funziona solo con le trame 2D.</span><span class="sxs-lookup"><span data-stu-id="b53d1-123">This instruction, like **gather4\_po**, only works with 2D textures.</span></span> <span data-ttu-id="b53d1-124">A differenza di [**gather4 \_ c**](gather4-c--sm5---asm-.md), che funziona anche con TextureCubes.</span><span class="sxs-lookup"><span data-stu-id="b53d1-124">This is unlike [**gather4\_c**](gather4-c--sm5---asm-.md), which also works with TextureCubes.</span></span>

<span data-ttu-id="b53d1-125">Per i formati con componenti float32, se il valore recuperato è normalizzato, o +-INF, viene usato nell'operazione di confronto non toccata.</span><span class="sxs-lookup"><span data-stu-id="b53d1-125">For formats with float32 components, if the value being fetched is normalized, or +-INF, it is used in the comparison operation untouched.</span></span> <span data-ttu-id="b53d1-126">NaN viene utilizzato nell'operazione di confronto come NaN, ma è possibile modificare la rappresentazione di bit esatta di NaN.</span><span class="sxs-lookup"><span data-stu-id="b53d1-126">NaN is used in the comparison operation as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="b53d1-127">Le denormazioni vengono scaricate fino a zero nel confronto.</span><span class="sxs-lookup"><span data-stu-id="b53d1-127">Denorms are flushed to zero going into the comparison.</span></span> <span data-ttu-id="b53d1-128">Per TextureCubes, alcune sintesi del quarto Texel mancante devono verificarsi negli angoli, quindi la nozione di restituzione di bit invariati per il Texel sintetizzato non è applicabile.</span><span class="sxs-lookup"><span data-stu-id="b53d1-128">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply.</span></span>

<span data-ttu-id="b53d1-129">I formati supportati per **gather4 \_ po \_ c** sono identici a quelli supportati per l' **esempio \_ c**.</span><span class="sxs-lookup"><span data-stu-id="b53d1-129">Formats supported for **gather4\_po\_c** are same as those supported for **sample\_c**.</span></span> <span data-ttu-id="b53d1-130">Si tratta di formati a componente singolo, di conseguenza. R su srcSampler, anziché un swizzle arbitrario.</span><span class="sxs-lookup"><span data-stu-id="b53d1-130">These are single-component formats, thus the .R on srcSampler, rather than an arbitrary swizzle.</span></span>

<span data-ttu-id="b53d1-131">**gather4 \_ po \_ c** in una risorsa non associata restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="b53d1-131">**gather4\_po\_c** on an unbound resource returns 0.</span></span>

<span data-ttu-id="b53d1-132">Utilizzare questo metodo per il filtro della mappa Shadow.</span><span class="sxs-lookup"><span data-stu-id="b53d1-132">Use this method for shadow map filtering.</span></span>

<span data-ttu-id="b53d1-133">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b53d1-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b53d1-134">Vertice</span><span class="sxs-lookup"><span data-stu-id="b53d1-134">Vertex</span></span> | <span data-ttu-id="b53d1-135">Hull</span><span class="sxs-lookup"><span data-stu-id="b53d1-135">Hull</span></span> | <span data-ttu-id="b53d1-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="b53d1-136">Domain</span></span> | <span data-ttu-id="b53d1-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="b53d1-137">Geometry</span></span> | <span data-ttu-id="b53d1-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="b53d1-138">Pixel</span></span> | <span data-ttu-id="b53d1-139">Calcolo</span><span class="sxs-lookup"><span data-stu-id="b53d1-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b53d1-140">X</span><span class="sxs-lookup"><span data-stu-id="b53d1-140">X</span></span>      | <span data-ttu-id="b53d1-141">X</span><span class="sxs-lookup"><span data-stu-id="b53d1-141">X</span></span>    | <span data-ttu-id="b53d1-142">X</span><span class="sxs-lookup"><span data-stu-id="b53d1-142">X</span></span>      | <span data-ttu-id="b53d1-143">X</span><span class="sxs-lookup"><span data-stu-id="b53d1-143">X</span></span>        | <span data-ttu-id="b53d1-144">X</span><span class="sxs-lookup"><span data-stu-id="b53d1-144">X</span></span>     | <span data-ttu-id="b53d1-145">X</span><span class="sxs-lookup"><span data-stu-id="b53d1-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b53d1-146">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b53d1-146">Minimum Shader Model</span></span>

<span data-ttu-id="b53d1-147">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b53d1-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b53d1-148">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b53d1-148">Shader Model</span></span>                                              | <span data-ttu-id="b53d1-149">Supportato</span><span class="sxs-lookup"><span data-stu-id="b53d1-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b53d1-150">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b53d1-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b53d1-151">sì</span><span class="sxs-lookup"><span data-stu-id="b53d1-151">yes</span></span>       |
| [<span data-ttu-id="b53d1-152">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="b53d1-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b53d1-153">no</span><span class="sxs-lookup"><span data-stu-id="b53d1-153">no</span></span>        |
| [<span data-ttu-id="b53d1-154">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="b53d1-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b53d1-155">no</span><span class="sxs-lookup"><span data-stu-id="b53d1-155">no</span></span>        |
| [<span data-ttu-id="b53d1-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b53d1-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b53d1-157">no</span><span class="sxs-lookup"><span data-stu-id="b53d1-157">no</span></span>        |
| [<span data-ttu-id="b53d1-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b53d1-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b53d1-159">no</span><span class="sxs-lookup"><span data-stu-id="b53d1-159">no</span></span>        |
| [<span data-ttu-id="b53d1-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b53d1-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b53d1-161">no</span><span class="sxs-lookup"><span data-stu-id="b53d1-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b53d1-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b53d1-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b53d1-163">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b53d1-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





