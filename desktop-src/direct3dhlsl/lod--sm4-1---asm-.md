---
title: LOD (SM 4.1-ASM)
description: Restituisce il livello di dettaglio (LOD) che verrebbe usato per il filtro della trama.
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c1ca5a22a735945b76a60c175c665c5cf58fb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719411"
---
# <a name="lod-sm41---asm"></a><span data-ttu-id="20ad7-103">LOD (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="20ad7-103">lod (sm4.1 - asm)</span></span>

<span data-ttu-id="20ad7-104">Restituisce il livello di dettaglio (LOD) che verrebbe usato per il filtro della trama.</span><span class="sxs-lookup"><span data-stu-id="20ad7-104">Returns the level of detail (LOD) that would be used for texture filtering.</span></span>



| <span data-ttu-id="20ad7-105">LOD dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler</span><span class="sxs-lookup"><span data-stu-id="20ad7-105">lod dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler</span></span> |
|--------------------------------------------------------------------------------|



 



| <span data-ttu-id="20ad7-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="20ad7-106">Item</span></span>                                                                                                               | <span data-ttu-id="20ad7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20ad7-107">Description</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="20ad7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="20ad7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="20ad7-109">\[nell' \] indirizzo dei risultati.</span><span class="sxs-lookup"><span data-stu-id="20ad7-109">\[in\] The address of the results.</span></span><br/>   |
| <span data-ttu-id="20ad7-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="20ad7-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="20ad7-111">\[in \] un set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="20ad7-111">\[in\] A set of texture coordinates.</span></span><br/> |
| <span data-ttu-id="20ad7-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="20ad7-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="20ad7-113">\[in \] un registro di trama.</span><span class="sxs-lookup"><span data-stu-id="20ad7-113">\[in\] A texture register.</span></span><br/>           |
| <span data-ttu-id="20ad7-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="20ad7-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="20ad7-115">\[in \] un registro del campionatore.</span><span class="sxs-lookup"><span data-stu-id="20ad7-115">\[in\] A sampler register.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="20ad7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="20ad7-116">Remarks</span></span>

<span data-ttu-id="20ad7-117">Questo comportamento è analogo all'istruzione di [esempio](sample--sm4---asm-.md) , ma non viene generato un campione filtrato.</span><span class="sxs-lookup"><span data-stu-id="20ad7-117">This behaves like the [sample](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="20ad7-118">L'istruzione calcola il vettore seguente (ClampedLOD, NonClampedLOD, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="20ad7-118">The instruction computes the following vector (ClampedLOD, NonClampedLOD, 0, 0).</span></span> <span data-ttu-id="20ad7-119">NonClampedLOD è un valore LOD calcolato che ignora tutti i bloccaggi dal campionatore o dalla trama (ad esempio, può restituire valori negativi). ClampedLOD è un valore LOD calcolato che verrebbe usato dall'istruzione di **esempio** effettiva.</span><span class="sxs-lookup"><span data-stu-id="20ad7-119">NonClampedLOD is a computed LOD value that ignores any clamping from either the sampler or the texture (ie: it can return negative values.) ClampedLOD is a computed LOD value that would be used by the actual **sample** instruction.</span></span> <span data-ttu-id="20ad7-120">Swizzle in *srcResource* consente di swizzled arbitrariamente i valori restituiti prima che vengano scritti nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="20ad7-120">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="20ad7-121">Se non è presente alcuna risorsa associata allo slot specificato, viene restituito 0.</span><span class="sxs-lookup"><span data-stu-id="20ad7-121">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="20ad7-122">Se il campionatore utilizza un filtro anisotropico, il LOD deve corrispondere al livello MIP frazionario basato sull'asse più piccolo dell'impronta ellittica.</span><span class="sxs-lookup"><span data-stu-id="20ad7-122">If the sampler is using anisotropic filtering the LOD should correspond to the fractional mip level based on the smaller axis of the elliptical footprint.</span></span>

<span data-ttu-id="20ad7-123">Questa operazione è valida per i tipi di trama seguenti: Texture1D, Texture2D, Texture3D e TextureCube.</span><span class="sxs-lookup"><span data-stu-id="20ad7-123">This is valid for the following texture types: Texture1D, Texture2D, Texture3D and TextureCube.</span></span>

<span data-ttu-id="20ad7-124">L'istruzione **LOD** non è definita se usata con un campionatore che specifica il filtro MIP del punto, in particolare, qualsiasi \_ enumerazione del filtro D3D10 che termina in un \_ punto MIP.</span><span class="sxs-lookup"><span data-stu-id="20ad7-124">The **lod** instruction is not defined when used with a sampler that specifies point mip filtering, specifically, any D3D10\_FILTER enum that ends in MIP\_POINT.</span></span> <span data-ttu-id="20ad7-125">Un esempio è D3D10 \_ FILTRARE \_ il \_ \_ punto MIP min mag \_ .)</span><span class="sxs-lookup"><span data-stu-id="20ad7-125">(An example of this would be D3D10\_FILTER\_MIN\_MAG\_MIP\_POINT.)</span></span>

<span data-ttu-id="20ad7-126">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="20ad7-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="20ad7-127">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="20ad7-127">Vertex Shader</span></span> | <span data-ttu-id="20ad7-128">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="20ad7-128">Geometry Shader</span></span> | <span data-ttu-id="20ad7-129">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="20ad7-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="20ad7-130">x</span><span class="sxs-lookup"><span data-stu-id="20ad7-130">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="20ad7-131">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="20ad7-131">Minimum Shader Model</span></span>

<span data-ttu-id="20ad7-132">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="20ad7-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="20ad7-133">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="20ad7-133">Shader Model</span></span>                                              | <span data-ttu-id="20ad7-134">Supportato</span><span class="sxs-lookup"><span data-stu-id="20ad7-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="20ad7-135">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="20ad7-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="20ad7-136">sì</span><span class="sxs-lookup"><span data-stu-id="20ad7-136">yes</span></span>       |
| [<span data-ttu-id="20ad7-137">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="20ad7-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="20ad7-138">sì</span><span class="sxs-lookup"><span data-stu-id="20ad7-138">yes</span></span>       |
| [<span data-ttu-id="20ad7-139">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="20ad7-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="20ad7-140">no</span><span class="sxs-lookup"><span data-stu-id="20ad7-140">no</span></span>        |
| [<span data-ttu-id="20ad7-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20ad7-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="20ad7-142">no</span><span class="sxs-lookup"><span data-stu-id="20ad7-142">no</span></span>        |
| [<span data-ttu-id="20ad7-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20ad7-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="20ad7-144">no</span><span class="sxs-lookup"><span data-stu-id="20ad7-144">no</span></span>        |
| [<span data-ttu-id="20ad7-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20ad7-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="20ad7-146">no</span><span class="sxs-lookup"><span data-stu-id="20ad7-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="20ad7-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="20ad7-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20ad7-148">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20ad7-148">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





