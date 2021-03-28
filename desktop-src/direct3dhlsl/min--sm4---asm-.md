---
title: min (SM4-ASM)
description: Valore minimo float per componente.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584aee077735b717bf76d148d4d0db4357a7d95
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117221"
---
# <a name="min-sm4---asm"></a><span data-ttu-id="e3218-103">min (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e3218-103">min (sm4 - asm)</span></span>

<span data-ttu-id="e3218-104">Valore minimo float per componente.</span><span class="sxs-lookup"><span data-stu-id="e3218-104">Component-wise float minimum.</span></span>



| <span data-ttu-id="e3218-105">min \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="e3218-105">min\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e3218-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="e3218-106">Item</span></span>                                                            | <span data-ttu-id="e3218-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3218-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3218-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e3218-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e3218-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e3218-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="e3218-110">*dest*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="e3218-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="e3218-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="e3218-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="e3218-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e3218-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e3218-113">\[nei \] componenti da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="e3218-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                  |
| <span data-ttu-id="e3218-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="e3218-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="e3218-115">\[nei \] componenti da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="e3218-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="e3218-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3218-116">Remarks</span></span>

><span data-ttu-id="e3218-117">= viene usato al posto di > in modo che se min (x, y) = x then Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="e3218-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="e3218-118">NaN ha una gestione speciale.</span><span class="sxs-lookup"><span data-stu-id="e3218-118">NaN has special handling.</span></span> <span data-ttu-id="e3218-119">Se un operando di origine è NaN, viene restituito l'altro operando di origine e viene effettuata la scelta per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="e3218-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="e3218-120">Se entrambi sono NaN, viene restituita qualsiasi rappresentazione NaN.</span><span class="sxs-lookup"><span data-stu-id="e3218-120">If both are NaN, any NaN representation is returned.</span></span> <span data-ttu-id="e3218-121">Questo è conforme alle nuove regole IEEE 754R.</span><span class="sxs-lookup"><span data-stu-id="e3218-121">This conforms to new IEEE 754R rules.</span></span>

<span data-ttu-id="e3218-122">Le denormazioni vengono scaricate, con il segno mantenuto, prima del confronto.</span><span class="sxs-lookup"><span data-stu-id="e3218-122">Denorms are flushed, with the sign preserved, before comparison.</span></span> <span data-ttu-id="e3218-123">Tuttavia, il risultato scritto in *dest* potrebbe o non essere denormalizzato.</span><span class="sxs-lookup"><span data-stu-id="e3218-123">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="e3218-124">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="e3218-124">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="e3218-125">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="e3218-125">F means finite real number.</span></span>



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="e3218-126">**src1 src0->**</span><span class="sxs-lookup"><span data-stu-id="e3218-126">**src0 src1->**</span></span> | <span data-ttu-id="e3218-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="e3218-127">**-inf**</span></span> | <span data-ttu-id="e3218-128">**F**</span><span class="sxs-lookup"><span data-stu-id="e3218-128">**F**</span></span>        | <span data-ttu-id="e3218-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="e3218-129">**+inf**</span></span> | <span data-ttu-id="e3218-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="e3218-130">**NaN**</span></span> |
| <span data-ttu-id="e3218-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="e3218-131">**-inf**</span></span>           | <span data-ttu-id="e3218-132">-inf</span><span class="sxs-lookup"><span data-stu-id="e3218-132">-inf</span></span>     | <span data-ttu-id="e3218-133">-inf</span><span class="sxs-lookup"><span data-stu-id="e3218-133">-inf</span></span>         | <span data-ttu-id="e3218-134">-inf</span><span class="sxs-lookup"><span data-stu-id="e3218-134">-inf</span></span>     | <span data-ttu-id="e3218-135">-inf</span><span class="sxs-lookup"><span data-stu-id="e3218-135">-inf</span></span>    |
| <span data-ttu-id="e3218-136">**F**</span><span class="sxs-lookup"><span data-stu-id="e3218-136">**F**</span></span>              | <span data-ttu-id="e3218-137">-inf</span><span class="sxs-lookup"><span data-stu-id="e3218-137">-inf</span></span>     | <span data-ttu-id="e3218-138">src0 o src1</span><span class="sxs-lookup"><span data-stu-id="e3218-138">src0 or src1</span></span> | <span data-ttu-id="e3218-139">src0</span><span class="sxs-lookup"><span data-stu-id="e3218-139">src0</span></span>     | <span data-ttu-id="e3218-140">src0</span><span class="sxs-lookup"><span data-stu-id="e3218-140">src0</span></span>    |
| <span data-ttu-id="e3218-141">**-INF**</span><span class="sxs-lookup"><span data-stu-id="e3218-141">**-inf**</span></span>           | <span data-ttu-id="e3218-142">-inf</span><span class="sxs-lookup"><span data-stu-id="e3218-142">-inf</span></span>     | <span data-ttu-id="e3218-143">src1</span><span class="sxs-lookup"><span data-stu-id="e3218-143">src1</span></span>         | <span data-ttu-id="e3218-144">+inf</span><span class="sxs-lookup"><span data-stu-id="e3218-144">+inf</span></span>     | <span data-ttu-id="e3218-145">+inf</span><span class="sxs-lookup"><span data-stu-id="e3218-145">+inf</span></span>    |
| <span data-ttu-id="e3218-146">**NaN**</span><span class="sxs-lookup"><span data-stu-id="e3218-146">**NaN**</span></span>            | <span data-ttu-id="e3218-147">-inf</span><span class="sxs-lookup"><span data-stu-id="e3218-147">-inf</span></span>     | <span data-ttu-id="e3218-148">src1</span><span class="sxs-lookup"><span data-stu-id="e3218-148">src1</span></span>         | <span data-ttu-id="e3218-149">+inf</span><span class="sxs-lookup"><span data-stu-id="e3218-149">+inf</span></span>     | <span data-ttu-id="e3218-150">NaN</span><span class="sxs-lookup"><span data-stu-id="e3218-150">NaN</span></span>     |



 

<span data-ttu-id="e3218-151">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e3218-151">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e3218-152">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="e3218-152">Vertex Shader</span></span> | <span data-ttu-id="e3218-153">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="e3218-153">Geometry Shader</span></span> | <span data-ttu-id="e3218-154">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="e3218-154">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e3218-155">x</span><span class="sxs-lookup"><span data-stu-id="e3218-155">x</span></span>             | <span data-ttu-id="e3218-156">x</span><span class="sxs-lookup"><span data-stu-id="e3218-156">x</span></span>               | <span data-ttu-id="e3218-157">x</span><span class="sxs-lookup"><span data-stu-id="e3218-157">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e3218-158">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="e3218-158">Minimum Shader Model</span></span>

<span data-ttu-id="e3218-159">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="e3218-159">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e3218-160">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="e3218-160">Shader Model</span></span>                                              | <span data-ttu-id="e3218-161">Supportato</span><span class="sxs-lookup"><span data-stu-id="e3218-161">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e3218-162">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="e3218-162">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e3218-163">sì</span><span class="sxs-lookup"><span data-stu-id="e3218-163">yes</span></span>       |
| [<span data-ttu-id="e3218-164">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="e3218-164">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e3218-165">sì</span><span class="sxs-lookup"><span data-stu-id="e3218-165">yes</span></span>       |
| [<span data-ttu-id="e3218-166">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="e3218-166">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e3218-167">sì</span><span class="sxs-lookup"><span data-stu-id="e3218-167">yes</span></span>       |
| [<span data-ttu-id="e3218-168">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3218-168">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e3218-169">no</span><span class="sxs-lookup"><span data-stu-id="e3218-169">no</span></span>        |
| [<span data-ttu-id="e3218-170">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3218-170">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e3218-171">no</span><span class="sxs-lookup"><span data-stu-id="e3218-171">no</span></span>        |
| [<span data-ttu-id="e3218-172">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3218-172">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e3218-173">no</span><span class="sxs-lookup"><span data-stu-id="e3218-173">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e3218-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e3218-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3218-175">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3218-175">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





