---
title: samplepos (SM 4.1-ASM)
description: Esegue una query sulla posizione di un campione in una visualizzazione risorse shader specificata o nell'rasterizzatore.
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910a542dafddb8b855e218f8702c746220780d6e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398287"
---
# <a name="samplepos-sm41---asm"></a><span data-ttu-id="bf49a-103">samplepos (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="bf49a-103">samplepos (sm4.1 - asm)</span></span>

<span data-ttu-id="bf49a-104">Esegue una query sulla posizione di un campione in una visualizzazione risorse shader specificata o nell'rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="bf49a-104">Queries the position of a sample in a given shader resource view or in the rasterizer.</span></span>



| <span data-ttu-id="bf49a-105">samplepos dest \[ . mask \] , srcResource \[ . Swizzle \] , sampleIndex (operando scalare)</span><span class="sxs-lookup"><span data-stu-id="bf49a-105">samplepos dest\[.mask\], srcResource\[.swizzle\], sampleIndex (scalar operand)</span></span> |
|--------------------------------------------------------------------------------|



 



| <span data-ttu-id="bf49a-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="bf49a-106">Item</span></span>                                                                                                               | <span data-ttu-id="bf49a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf49a-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="bf49a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="bf49a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="bf49a-109">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bf49a-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="bf49a-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="bf49a-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="bf49a-111">\[nella \] risorsa shader.</span><span class="sxs-lookup"><span data-stu-id="bf49a-111">\[in\] The shader resource.</span></span><br/>                         |
| <span data-ttu-id="bf49a-112"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span><span class="sxs-lookup"><span data-stu-id="bf49a-112"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span></span><br/> | <span data-ttu-id="bf49a-113">\[nell' \] indice dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="bf49a-113">\[in\] The index of the sample.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="bf49a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf49a-114">Remarks</span></span>

<span data-ttu-id="bf49a-115">Questa istruzione restituisce la posizione di esempio 2D di *sampleIndex* di esempio per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="bf49a-115">This instruction returns the 2D sample position of sample *sampleIndex* for the given resource.</span></span> <span data-ttu-id="bf49a-116">È valido solo per le risorse che possono essere caricate tramite [**ld2dms**](ld2dms--sm4-1---asm-.md) , a meno che il rasterizzatore non sia specificato come *srcResource*.</span><span class="sxs-lookup"><span data-stu-id="bf49a-116">It is valid only for resources that can be loaded using [**ld2dms**](ld2dms--sm4-1---asm-.md) unless the rasterizer is specified as *srcResource*.</span></span>

<span data-ttu-id="bf49a-117">*srcResource* può essere un registro t \# (visualizzazione risorse shader) o un registro rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="bf49a-117">*srcResource* can be a t\# register (a shader resource view) or a rasterizer register.</span></span>

<span data-ttu-id="bf49a-118">L'istruzione calcola il vettore a virgola mobile (xposition, yposition, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="bf49a-118">The instruction computes the floating point vector (Xposition, Yposition, 0, 0).</span></span>

<span data-ttu-id="bf49a-119">Swizzle in *srcResource* consente di swizzled arbitrariamente i valori restituiti prima che vengano scritti nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="bf49a-119">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span> <span data-ttu-id="bf49a-120">La posizione di esempio è relativa al centro del pixel, in base al sistema di coordinate dei pixel.</span><span class="sxs-lookup"><span data-stu-id="bf49a-120">The sample position is relative to the pixel's center, based on the Pixel Coordinate System.</span></span>

<span data-ttu-id="bf49a-121">Se *sampleIndex* è fuori limite, viene restituito zero vector.</span><span class="sxs-lookup"><span data-stu-id="bf49a-121">If *sampleIndex* is out of bounds a zero vector is returned.</span></span> <span data-ttu-id="bf49a-122">Se non è presente alcuna risorsa associata allo slot specificato, viene restituito 0.</span><span class="sxs-lookup"><span data-stu-id="bf49a-122">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="bf49a-123">**samplepos** può essere usato per elementi come i resolver personalizzati nel codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="bf49a-123">**samplepos** can be used for things like custom resolves in shader code.</span></span>

<span data-ttu-id="bf49a-124">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="bf49a-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bf49a-125">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="bf49a-125">Vertex Shader</span></span> | <span data-ttu-id="bf49a-126">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="bf49a-126">Geometry Shader</span></span> | <span data-ttu-id="bf49a-127">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="bf49a-127">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="bf49a-128">x</span><span class="sxs-lookup"><span data-stu-id="bf49a-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bf49a-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="bf49a-129">Minimum Shader Model</span></span>

<span data-ttu-id="bf49a-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="bf49a-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bf49a-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="bf49a-131">Shader Model</span></span>                                              | <span data-ttu-id="bf49a-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="bf49a-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bf49a-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="bf49a-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bf49a-134">sì</span><span class="sxs-lookup"><span data-stu-id="bf49a-134">yes</span></span>       |
| [<span data-ttu-id="bf49a-135">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="bf49a-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bf49a-136">sì</span><span class="sxs-lookup"><span data-stu-id="bf49a-136">yes</span></span>       |
| [<span data-ttu-id="bf49a-137">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="bf49a-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bf49a-138">no</span><span class="sxs-lookup"><span data-stu-id="bf49a-138">no</span></span>        |
| [<span data-ttu-id="bf49a-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf49a-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bf49a-140">no</span><span class="sxs-lookup"><span data-stu-id="bf49a-140">no</span></span>        |
| [<span data-ttu-id="bf49a-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf49a-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bf49a-142">no</span><span class="sxs-lookup"><span data-stu-id="bf49a-142">no</span></span>        |
| [<span data-ttu-id="bf49a-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf49a-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bf49a-144">no</span><span class="sxs-lookup"><span data-stu-id="bf49a-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bf49a-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf49a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf49a-146">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf49a-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





