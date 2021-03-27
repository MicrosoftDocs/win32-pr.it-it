---
title: deriv_rty (SM4-ASM)
description: 'Render: destinazione y equivalente di RTX di derivazione \_ .'
ms.assetid: F78F2DBD-9428-4F34-85AD-276DF54C52D1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e4517782c687473b4789229334b4cafc94b989
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857750"
---
# <a name="deriv_rty-sm4---asm"></a><span data-ttu-id="01525-103">derivare \_ valore (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="01525-103">deriv\_rty (sm4 - asm)</span></span>

<span data-ttu-id="01525-104">Render: destinazione y equivalente di [ \_ RTX di derivazione](deriv-rtx--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="01525-104">Render-target y equivalent of [deriv\_rtx](deriv-rtx--sm4---asm-.md).</span></span>



| <span data-ttu-id="01525-105">derivare \_ valore \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="01525-105">deriv\_rty\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="01525-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="01525-106">Item</span></span>                                                            | <span data-ttu-id="01525-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01525-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="01525-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="01525-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="01525-109">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="01525-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="01525-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="01525-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="01525-111">\[nel \] componente dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="01525-111">\[in\] The component in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="01525-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="01525-112">Remarks</span></span>

<span data-ttu-id="01525-113">Viene calcolata solo una singola coppia derivata x e y per ogni timbro 2x2 di pixel.</span><span class="sxs-lookup"><span data-stu-id="01525-113">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="01525-114">Questa operazione dipende dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="01525-114">This operation is hardware dependent.</span></span>

<span data-ttu-id="01525-115">Implementazione dell'rasterizzazione dei riferimenti per i triangoli:</span><span class="sxs-lookup"><span data-stu-id="01525-115">Reference rasterizer implementation for triangles:</span></span>

-   <span data-ttu-id="01525-116">Pixel shader esegue sempre lo shader su 2x2 quad di pixel in contemporanea (anche attraverso il controllo di flusso, mascherando i pixel disabilitati).</span><span class="sxs-lookup"><span data-stu-id="01525-116">Pixel Shader always runs Shader over 2x2 quad of pixels in lockstep (even through flow control, masking disabled pixels).</span></span>
-   <span data-ttu-id="01525-117">I quad hanno sempre le coordinate dei pixel numerate (entrambe x e y) per il pixel superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="01525-117">Quads always have even numbered pixel coordinates (both x and y) for top-left pixel.</span></span>
-   <span data-ttu-id="01525-118">I pixel fittizi vengono spenti primitivi se la primitiva è troppo piccola per riempire un quad 2x2.</span><span class="sxs-lookup"><span data-stu-id="01525-118">Dummy pixels run off primitive if primitive is too small to fill a 2x2 quad.</span></span>
-   <span data-ttu-id="01525-119">la [derivazione \_ RTX](deriv-rtx--sm4---asm-.md) viene calcolata scegliendo 2 pixel: il pixel corrente e l'altro pixel con la stessa coordinata y del quad.</span><span class="sxs-lookup"><span data-stu-id="01525-119">[deriv\_rtx](deriv-rtx--sm4---asm-.md) is computed by first choosing 2 pixels: the current pixel and the other pixel with the same y coordinate from the quad.</span></span> <span data-ttu-id="01525-120">Il risultato viene quindi calcolato come: *src0*(Odd x pixel)- *src0*(anche x pixel) \[ per componente\]</span><span class="sxs-lookup"><span data-stu-id="01525-120">Then, the result is calculated as: *src0*(odd x pixel) - *src0*(even x pixel) \[per-component\]</span></span>
-   <span data-ttu-id="01525-121">la **derivazione \_ valore** viene calcolata scegliendo 2 pixel: il pixel corrente e l'altro pixel con la stessa coordinata x del quad.</span><span class="sxs-lookup"><span data-stu-id="01525-121">**deriv\_rty** is computed by first choosing 2 pixels: the current pixel and the other pixel with the same x coordinate from the quad.</span></span> <span data-ttu-id="01525-122">Il risultato viene quindi calcolato come: *src0*(pixel dispari y)- *src0*(anche pixel y) \[ per componente\]</span><span class="sxs-lookup"><span data-stu-id="01525-122">Then, the result is calculated as: *src0*(odd y pixel) - *src0*(even y pixel) \[per-component\]</span></span>

<span data-ttu-id="01525-123">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="01525-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="01525-124">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="01525-124">Vertex Shader</span></span> | <span data-ttu-id="01525-125">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="01525-125">Geometry Shader</span></span> | <span data-ttu-id="01525-126">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="01525-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="01525-127">x</span><span class="sxs-lookup"><span data-stu-id="01525-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="01525-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="01525-128">Minimum Shader Model</span></span>

<span data-ttu-id="01525-129">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="01525-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="01525-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="01525-130">Shader Model</span></span>                                              | <span data-ttu-id="01525-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="01525-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="01525-132">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="01525-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="01525-133">sì</span><span class="sxs-lookup"><span data-stu-id="01525-133">yes</span></span>       |
| [<span data-ttu-id="01525-134">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="01525-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="01525-135">sì</span><span class="sxs-lookup"><span data-stu-id="01525-135">yes</span></span>       |
| [<span data-ttu-id="01525-136">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="01525-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="01525-137">sì</span><span class="sxs-lookup"><span data-stu-id="01525-137">yes</span></span>       |
| [<span data-ttu-id="01525-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01525-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="01525-139">no</span><span class="sxs-lookup"><span data-stu-id="01525-139">no</span></span>        |
| [<span data-ttu-id="01525-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01525-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="01525-141">no</span><span class="sxs-lookup"><span data-stu-id="01525-141">no</span></span>        |
| [<span data-ttu-id="01525-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01525-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="01525-143">no</span><span class="sxs-lookup"><span data-stu-id="01525-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="01525-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="01525-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01525-145">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01525-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





