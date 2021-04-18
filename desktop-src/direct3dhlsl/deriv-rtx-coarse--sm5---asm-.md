---
title: deriv_rtx_coarse (SM5-ASM)
description: Calcola la frequenza di modifica dei componenti. | deriv_rtx_coarse (SM5-ASM)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2355b6db6aef9e85959d6359053fea76b48af0a5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995397"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a><span data-ttu-id="5935b-104">derivate \_ RTX \_ grossolane (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5935b-104">deriv\_rtx\_coarse (sm5 - asm)</span></span>

<span data-ttu-id="5935b-105">Calcola la frequenza di modifica dei componenti.</span><span class="sxs-lookup"><span data-stu-id="5935b-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="5935b-106">derivate \_ RTX a \_ grosse \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="5935b-106">deriv\_rtx\_coarse\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------|



 



| <span data-ttu-id="5935b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="5935b-107">Item</span></span>                                                            | <span data-ttu-id="5935b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5935b-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5935b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5935b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5935b-110">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5935b-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="5935b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5935b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5935b-112">\[nei \] componenti dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5935b-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="5935b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5935b-113">Remarks</span></span>

<span data-ttu-id="5935b-114">Questa istruzione calcola la frequenza di modifica del contenuto di ogni componente float32 di *src0* (post-swizzle), per quanto riguarda la direzione renderTarget x (RTX) o la direzione renderTarget y (vedere [derivate \_ valore \_ grossolane](deriv-rty-coarse--sm5---asm-.md)).</span><span class="sxs-lookup"><span data-stu-id="5935b-114">This instruction computes the rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction (see [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md)).</span></span> <span data-ttu-id="5935b-115">Viene calcolata solo una singola coppia derivata x e y per ogni timbro 2x2 di pixel.</span><span class="sxs-lookup"><span data-stu-id="5935b-115">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="5935b-116">I dati nella chiamata di pixel shader corrente possono o non possono partecipare al calcolo del derivato richiesto, perché il derivato verrà calcolato solo una volta per ogni Quad 2x2.</span><span class="sxs-lookup"><span data-stu-id="5935b-116">The data in the current pixel shader invocation may or may not participate in the calculation of the requested derivative, because the derivative will be calculated only once per 2x2 quad.</span></span> <span data-ttu-id="5935b-117">Ad esempio, il derivato x può essere un Delta dalla prima riga di pixel e la direzione y ([derivate \_ valore \_ grossolane](deriv-rty-coarse--sm5---asm-.md)) potrebbe essere un Delta dalla colonna di sinistra di pixel.</span><span class="sxs-lookup"><span data-stu-id="5935b-117">For example, the x derivative could be a delta from the top row of pixels, and the y direction ([deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md)) could be a delta from the left column of pixels.</span></span> <span data-ttu-id="5935b-118">Il calcolo esatto spetta al fornitore dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="5935b-118">The exact calculation is up to the hardware vendor.</span></span> <span data-ttu-id="5935b-119">Non esiste inoltre alcuna specifica che impone il modo in cui i quadrupli 2x2 verranno allineati o affiancati su una primitiva.</span><span class="sxs-lookup"><span data-stu-id="5935b-119">There is also no specification dictating how the 2x2 quads will be aligned or tiled over a primitive.</span></span>

<span data-ttu-id="5935b-120">I derivati vengono calcolati a un livello grossolano, una volta per ogni quad di 2x2 pixel.</span><span class="sxs-lookup"><span data-stu-id="5935b-120">Derivatives are calculated at a coarse level, once per 2x2 pixel quad.</span></span> <span data-ttu-id="5935b-121">Questa istruzione e [derivano \_ valore \_ grossolane](deriv-rty-coarse--sm5---asm-.md) sono alternative alla [derivazione di \_ RTX \_ fine](deriv-rtx-fine--sm5---asm-.md) e [derivano \_ valore \_ fine](deriv-rty-fine--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="5935b-121">This instruction and [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md) are alternatives to [deriv\_rtx\_fine](deriv-rtx-fine--sm5---asm-.md) and [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md).</span></span> <span data-ttu-id="5935b-122">Queste \_ \_ istruzioni derivate grossolane e fine rappresentano una sostituzione per **derivare \_ rtxderiv \_ valore** dai modelli shader precedenti.</span><span class="sxs-lookup"><span data-stu-id="5935b-122">These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtxderiv\_rty** from previous shader models .</span></span>

<span data-ttu-id="5935b-123">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="5935b-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5935b-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="5935b-124">Vertex</span></span> | <span data-ttu-id="5935b-125">Hull</span><span class="sxs-lookup"><span data-stu-id="5935b-125">Hull</span></span> | <span data-ttu-id="5935b-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="5935b-126">Domain</span></span> | <span data-ttu-id="5935b-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="5935b-127">Geometry</span></span> | <span data-ttu-id="5935b-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="5935b-128">Pixel</span></span> | <span data-ttu-id="5935b-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="5935b-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5935b-130">X</span><span class="sxs-lookup"><span data-stu-id="5935b-130">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5935b-131">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="5935b-131">Minimum Shader Model</span></span>

<span data-ttu-id="5935b-132">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="5935b-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5935b-133">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="5935b-133">Shader Model</span></span>                                              | <span data-ttu-id="5935b-134">Supportato</span><span class="sxs-lookup"><span data-stu-id="5935b-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5935b-135">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="5935b-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5935b-136">sì</span><span class="sxs-lookup"><span data-stu-id="5935b-136">yes</span></span>       |
| [<span data-ttu-id="5935b-137">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="5935b-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5935b-138">no</span><span class="sxs-lookup"><span data-stu-id="5935b-138">no</span></span>        |
| [<span data-ttu-id="5935b-139">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="5935b-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5935b-140">no</span><span class="sxs-lookup"><span data-stu-id="5935b-140">no</span></span>        |
| [<span data-ttu-id="5935b-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5935b-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5935b-142">no</span><span class="sxs-lookup"><span data-stu-id="5935b-142">no</span></span>        |
| [<span data-ttu-id="5935b-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5935b-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5935b-144">no</span><span class="sxs-lookup"><span data-stu-id="5935b-144">no</span></span>        |
| [<span data-ttu-id="5935b-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5935b-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5935b-146">no</span><span class="sxs-lookup"><span data-stu-id="5935b-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5935b-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5935b-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5935b-148">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5935b-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





