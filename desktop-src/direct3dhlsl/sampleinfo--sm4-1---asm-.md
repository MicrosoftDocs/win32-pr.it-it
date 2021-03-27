---
title: sampleinfo (SM 4.1-ASM)
description: Esegue una query sul numero di campioni in una determinata visualizzazione risorse shader o nell'rasterizzatore.
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d307dbc8c79618a6401737874a9f6e060a899ccc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857813"
---
# <a name="sampleinfo-sm41---asm"></a><span data-ttu-id="9bcfd-103">sampleinfo (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="9bcfd-103">sampleinfo (sm4.1 - asm)</span></span>

<span data-ttu-id="9bcfd-104">Esegue una query sul numero di campioni in una determinata visualizzazione risorse shader o nell'rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-104">Queries the number of samples in a given shader resource view or in the rasterizer.</span></span>



| <span data-ttu-id="9bcfd-105">\[\_uint \] dest \[ . mask \] , srcResource \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9bcfd-105">\[\_uint\] dest\[.mask\], srcResource\[.swizzle\]</span></span> |
|---------------------------------------------------|



 



| <span data-ttu-id="9bcfd-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="9bcfd-106">Item</span></span>                                                                                                               | <span data-ttu-id="9bcfd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bcfd-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9bcfd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9bcfd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="9bcfd-109">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="9bcfd-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="9bcfd-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="9bcfd-111">\[nella \] risorsa shader.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-111">\[in\] The shader resource.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="9bcfd-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bcfd-112">Remarks</span></span>

<span data-ttu-id="9bcfd-113">Questa istruzione restituisce il numero di campioni per la risorsa o il rasterizzatore specificato.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-113">This instruction returns the number of samples for the given resource or the rasterizer.</span></span> <span data-ttu-id="9bcfd-114">È valido solo per le risorse che possono essere caricate tramite [**ld2dms**](ld2dms--sm4-1---asm-.md) , a meno che il rasterizzatore non sia specificato come *srcResource*.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-114">It is valid only for resources that can be loaded using [**ld2dms**](ld2dms--sm4-1---asm-.md) unless the rasterizer is specified as *srcResource*.</span></span> <span data-ttu-id="9bcfd-115">*srcResource* potrebbe essere un registro t \# (visualizzazione risorse shader) o un registro rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-115">*srcResource* could be a t\# register (a shader resource view) or a rasterizer register.</span></span>

<span data-ttu-id="9bcfd-116">L'istruzione calcola il vettore (SampleCount, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="9bcfd-116">The instruction computes the vector (SampleCount,0,0,0).</span></span>

<span data-ttu-id="9bcfd-117">Swizzle in *srcResource* consente di swizzled arbitrariamente i valori restituiti prima che vengano scritti nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-117">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span> <span data-ttu-id="9bcfd-118">Il valore restituito è a virgola mobile, a meno che non \_ venga usato il modificatore uint, nel qual caso il valore restituito è Integer.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-118">The returned value is floating point, unless the \_uint modifier is used, in which case the returned value is integer.</span></span> <span data-ttu-id="9bcfd-119">Se non è presente alcuna risorsa associata allo slot specificato, viene restituito 0.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-119">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="9bcfd-120">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="9bcfd-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9bcfd-121">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="9bcfd-121">Vertex Shader</span></span> | <span data-ttu-id="9bcfd-122">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="9bcfd-122">Geometry Shader</span></span> | <span data-ttu-id="9bcfd-123">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="9bcfd-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9bcfd-124">X</span><span class="sxs-lookup"><span data-stu-id="9bcfd-124">X</span></span>             | <span data-ttu-id="9bcfd-125">X</span><span class="sxs-lookup"><span data-stu-id="9bcfd-125">X</span></span>               | <span data-ttu-id="9bcfd-126">x</span><span class="sxs-lookup"><span data-stu-id="9bcfd-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9bcfd-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="9bcfd-127">Minimum Shader Model</span></span>

<span data-ttu-id="9bcfd-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9bcfd-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="9bcfd-129">Shader Model</span></span>                                              | <span data-ttu-id="9bcfd-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="9bcfd-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9bcfd-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="9bcfd-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9bcfd-132">sì</span><span class="sxs-lookup"><span data-stu-id="9bcfd-132">yes</span></span>       |
| [<span data-ttu-id="9bcfd-133">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="9bcfd-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9bcfd-134">sì</span><span class="sxs-lookup"><span data-stu-id="9bcfd-134">yes</span></span>       |
| [<span data-ttu-id="9bcfd-135">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="9bcfd-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9bcfd-136">no</span><span class="sxs-lookup"><span data-stu-id="9bcfd-136">no</span></span>        |
| [<span data-ttu-id="9bcfd-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bcfd-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9bcfd-138">no</span><span class="sxs-lookup"><span data-stu-id="9bcfd-138">no</span></span>        |
| [<span data-ttu-id="9bcfd-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bcfd-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9bcfd-140">no</span><span class="sxs-lookup"><span data-stu-id="9bcfd-140">no</span></span>        |
| [<span data-ttu-id="9bcfd-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bcfd-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9bcfd-142">no</span><span class="sxs-lookup"><span data-stu-id="9bcfd-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9bcfd-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9bcfd-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bcfd-144">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bcfd-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





