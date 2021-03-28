---
title: deriv_rtx_fine (SM5-ASM)
description: Calcola la frequenza di modifica dei componenti. | deriv_rtx_fine (SM5-ASM)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73061e3220704cf2c19e28b4d6d434fda43fb941
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995608"
---
# <a name="deriv_rtx_fine-sm5---asm"></a><span data-ttu-id="782b5-104">derivare \_ RTX \_ fine (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="782b5-104">deriv\_rtx\_fine (sm5 - asm)</span></span>

<span data-ttu-id="782b5-105">Calcola la frequenza di modifica dei componenti.</span><span class="sxs-lookup"><span data-stu-id="782b5-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="782b5-106">derivare \_ RTX \_ fine \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="782b5-106">deriv\_rtx\_fine\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="782b5-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="782b5-107">Item</span></span>                                                            | <span data-ttu-id="782b5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="782b5-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="782b5-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="782b5-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="782b5-110">\[nell' \] indirizzo dei risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="782b5-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="782b5-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="782b5-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="782b5-112">\[nei \] componenti dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="782b5-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="782b5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="782b5-113">Remarks</span></span>

<span data-ttu-id="782b5-114">Questa istruzione calcola la frequenza di modifica del contenuto di ogni componente float32 di *src0* (post-swizzle), per quanto riguarda la direzione renderTarget x (RTX) o la direzione renderTarget y (vedere [derivate \_ valore \_ fine](deriv-rty-fine--sm5---asm-.md)).</span><span class="sxs-lookup"><span data-stu-id="782b5-114">This instruction computes the rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction (see [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md)).</span></span> <span data-ttu-id="782b5-115">Ogni pixel nell'indicatore 2x2 ottiene una coppia univoca di calcoli derivati x/y</span><span class="sxs-lookup"><span data-stu-id="782b5-115">Each pixel in the 2x2 stamp gets a unique pair of x/y derivative calculations</span></span>

<span data-ttu-id="782b5-116">I dati nella chiamata di pixel shader corrente partecipano sempre al calcolo della derivata richiesta.</span><span class="sxs-lookup"><span data-stu-id="782b5-116">The data in the current pixel shader invocation always participates in the calculation of the requested derivative.</span></span> <span data-ttu-id="782b5-117">Nel quadrato 2x2 pixel, il pixel corrente rientra in, il derivato x è il Delta della riga di 2 pixel, incluso il pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="782b5-117">In the 2x2 pixel quad the current pixel falls within, the x derivative is the delta of the row of 2 pixels including the current pixel.</span></span> <span data-ttu-id="782b5-118">La derivata y è il Delta della colonna di 2 pixel, incluso il pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="782b5-118">The y derivative is the delta of the column of 2 pixels including the current pixel.</span></span> <span data-ttu-id="782b5-119">Non esiste alcuna specifica che impone il modo in cui i quad di 2x2 verranno allineati o affiancati su una primitiva.</span><span class="sxs-lookup"><span data-stu-id="782b5-119">There is no specification dictating how the 2x2 quads will be aligned or tiled over a primitive.</span></span>

<span data-ttu-id="782b5-120">I derivati vengono calcolati a un livello fine (calcolo univoco della coppia di derivati x/y per ogni pixel in un quad 2x2).</span><span class="sxs-lookup"><span data-stu-id="782b5-120">Derivatives are calculated at a fine level (unique calculation of the x/y derivative pair for each pixel in a 2x2 quad).</span></span> <span data-ttu-id="782b5-121">Questa istruzione e [derivano \_ valore \_ fine](deriv-rty-fine--sm5---asm-.md) sono alternative per [derivare \_ RTX \_ grossolane](deriv-rtx-coarse--sm5---asm-.md) e [derivare \_ valore \_ grossolane](deriv-rty-coarse--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="782b5-121">This instruction and [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md) are alternatives to [deriv\_rtx\_coarse](deriv-rtx-coarse--sm5---asm-.md) and [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md).</span></span> <span data-ttu-id="782b5-122">Queste \_ \_ istruzioni derivate grossolane e fine rappresentano una sostituzione per **derivare \_ RTX** . queste istruzioni derivate \_ grossolane e \_ belle sono una sostituzione per derivare **\_ RTX** e **derivare \_ valore** dai modelli shader precedenti.</span><span class="sxs-lookup"><span data-stu-id="782b5-122">These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtx** These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtx** and **deriv\_rty** from previous shader models.</span></span>

<span data-ttu-id="782b5-123">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="782b5-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="782b5-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="782b5-124">Vertex</span></span> | <span data-ttu-id="782b5-125">Hull</span><span class="sxs-lookup"><span data-stu-id="782b5-125">Hull</span></span> | <span data-ttu-id="782b5-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="782b5-126">Domain</span></span> | <span data-ttu-id="782b5-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="782b5-127">Geometry</span></span> | <span data-ttu-id="782b5-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="782b5-128">Pixel</span></span> | <span data-ttu-id="782b5-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="782b5-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="782b5-130">X</span><span class="sxs-lookup"><span data-stu-id="782b5-130">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="782b5-131">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="782b5-131">Minimum Shader Model</span></span>

<span data-ttu-id="782b5-132">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="782b5-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="782b5-133">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="782b5-133">Shader Model</span></span>                                              | <span data-ttu-id="782b5-134">Supportato</span><span class="sxs-lookup"><span data-stu-id="782b5-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="782b5-135">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="782b5-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="782b5-136">sì</span><span class="sxs-lookup"><span data-stu-id="782b5-136">yes</span></span>       |
| [<span data-ttu-id="782b5-137">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="782b5-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="782b5-138">no</span><span class="sxs-lookup"><span data-stu-id="782b5-138">no</span></span>        |
| [<span data-ttu-id="782b5-139">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="782b5-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="782b5-140">no</span><span class="sxs-lookup"><span data-stu-id="782b5-140">no</span></span>        |
| [<span data-ttu-id="782b5-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="782b5-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="782b5-142">no</span><span class="sxs-lookup"><span data-stu-id="782b5-142">no</span></span>        |
| [<span data-ttu-id="782b5-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="782b5-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="782b5-144">no</span><span class="sxs-lookup"><span data-stu-id="782b5-144">no</span></span>        |
| [<span data-ttu-id="782b5-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="782b5-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="782b5-146">no</span><span class="sxs-lookup"><span data-stu-id="782b5-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="782b5-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="782b5-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="782b5-148">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="782b5-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





