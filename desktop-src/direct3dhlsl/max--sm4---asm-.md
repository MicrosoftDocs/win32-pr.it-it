---
title: Max (SM4-ASM)
description: Valore massimo float per componente.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f24618897eacf250f2b924f6dde3745a32a7172
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398205"
---
# <a name="max-sm4---asm"></a><span data-ttu-id="92367-103">Max (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="92367-103">max (sm4 - asm)</span></span>

<span data-ttu-id="92367-104">Valore massimo float per componente.</span><span class="sxs-lookup"><span data-stu-id="92367-104">Component-wise float maximum.</span></span>



| <span data-ttu-id="92367-105">Max \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="92367-105">max\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="92367-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="92367-106">Item</span></span>                                                            | <span data-ttu-id="92367-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92367-107">Description</span></span>                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92367-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="92367-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="92367-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="92367-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="92367-110">*dest*  =  *src0*  >=  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="92367-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="92367-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="92367-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="92367-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="92367-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="92367-113">\[nei \] componenti da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="92367-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                    |
| <span data-ttu-id="92367-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="92367-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="92367-115">\[nei \] componenti da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="92367-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="92367-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="92367-116">Remarks</span></span>

><span data-ttu-id="92367-117">= viene usato al posto di > in modo che se min (x, y) = x then Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="92367-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="92367-118">NaN ha una gestione speciale.</span><span class="sxs-lookup"><span data-stu-id="92367-118">NaN has special handling.</span></span> <span data-ttu-id="92367-119">Se un operando di origine è NaN, viene restituito l'altro operando di origine e viene effettuata la scelta per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="92367-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="92367-120">Se entrambi sono NaN, viene restituita qualsiasi rappresentazione NaN.</span><span class="sxs-lookup"><span data-stu-id="92367-120">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="92367-121">Le denormazioni vengono scaricate con il segno mantenuto prima del confronto.</span><span class="sxs-lookup"><span data-stu-id="92367-121">Denorms are flushed with sign preserved before the comparison.</span></span> <span data-ttu-id="92367-122">Tuttavia, il risultato scritto in *dest* potrebbe o non essere denormalizzato.</span><span class="sxs-lookup"><span data-stu-id="92367-122">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="92367-123">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="92367-123">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="92367-124">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="92367-124">F means finite real number.</span></span>



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="92367-125">**src1 src0->**</span><span class="sxs-lookup"><span data-stu-id="92367-125">**src0 src1->**</span></span> | <span data-ttu-id="92367-126">**-INF**</span><span class="sxs-lookup"><span data-stu-id="92367-126">**-inf**</span></span> | <span data-ttu-id="92367-127">**F**</span><span class="sxs-lookup"><span data-stu-id="92367-127">**F**</span></span>        | <span data-ttu-id="92367-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="92367-128">**+inf**</span></span> | <span data-ttu-id="92367-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="92367-129">**NaN**</span></span> |
| <span data-ttu-id="92367-130">**-INF**</span><span class="sxs-lookup"><span data-stu-id="92367-130">**-inf**</span></span>           | <span data-ttu-id="92367-131">-inf</span><span class="sxs-lookup"><span data-stu-id="92367-131">-inf</span></span>     | <span data-ttu-id="92367-132">src1</span><span class="sxs-lookup"><span data-stu-id="92367-132">src1</span></span>         | <span data-ttu-id="92367-133">+inf</span><span class="sxs-lookup"><span data-stu-id="92367-133">+inf</span></span>     | <span data-ttu-id="92367-134">-inf</span><span class="sxs-lookup"><span data-stu-id="92367-134">-inf</span></span>    |
| <span data-ttu-id="92367-135">**F**</span><span class="sxs-lookup"><span data-stu-id="92367-135">**F**</span></span>              | <span data-ttu-id="92367-136">src0</span><span class="sxs-lookup"><span data-stu-id="92367-136">src0</span></span>     | <span data-ttu-id="92367-137">src0 o src1</span><span class="sxs-lookup"><span data-stu-id="92367-137">src0 or src1</span></span> | <span data-ttu-id="92367-138">+inf</span><span class="sxs-lookup"><span data-stu-id="92367-138">+inf</span></span>     | <span data-ttu-id="92367-139">src0</span><span class="sxs-lookup"><span data-stu-id="92367-139">src0</span></span>    |
| <span data-ttu-id="92367-140">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="92367-140">**+inf**</span></span>           | <span data-ttu-id="92367-141">+inf</span><span class="sxs-lookup"><span data-stu-id="92367-141">+inf</span></span>     | <span data-ttu-id="92367-142">+inf</span><span class="sxs-lookup"><span data-stu-id="92367-142">+inf</span></span>         | <span data-ttu-id="92367-143">+inf</span><span class="sxs-lookup"><span data-stu-id="92367-143">+inf</span></span>     | <span data-ttu-id="92367-144">+inf</span><span class="sxs-lookup"><span data-stu-id="92367-144">+inf</span></span>    |
| <span data-ttu-id="92367-145">**NaN**</span><span class="sxs-lookup"><span data-stu-id="92367-145">**NaN**</span></span>            | <span data-ttu-id="92367-146">-inf</span><span class="sxs-lookup"><span data-stu-id="92367-146">-inf</span></span>     | <span data-ttu-id="92367-147">src1</span><span class="sxs-lookup"><span data-stu-id="92367-147">src1</span></span>         | <span data-ttu-id="92367-148">+inf</span><span class="sxs-lookup"><span data-stu-id="92367-148">+inf</span></span>     | <span data-ttu-id="92367-149">NaN</span><span class="sxs-lookup"><span data-stu-id="92367-149">NaN</span></span>     |



 

<span data-ttu-id="92367-150">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="92367-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="92367-151">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="92367-151">Vertex Shader</span></span> | <span data-ttu-id="92367-152">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="92367-152">Geometry Shader</span></span> | <span data-ttu-id="92367-153">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="92367-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="92367-154">x</span><span class="sxs-lookup"><span data-stu-id="92367-154">x</span></span>             | <span data-ttu-id="92367-155">x</span><span class="sxs-lookup"><span data-stu-id="92367-155">x</span></span>               | <span data-ttu-id="92367-156">x</span><span class="sxs-lookup"><span data-stu-id="92367-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="92367-157">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="92367-157">Minimum Shader Model</span></span>

<span data-ttu-id="92367-158">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="92367-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="92367-159">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="92367-159">Shader Model</span></span>                                              | <span data-ttu-id="92367-160">Supportato</span><span class="sxs-lookup"><span data-stu-id="92367-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="92367-161">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="92367-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="92367-162">sì</span><span class="sxs-lookup"><span data-stu-id="92367-162">yes</span></span>       |
| [<span data-ttu-id="92367-163">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="92367-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="92367-164">sì</span><span class="sxs-lookup"><span data-stu-id="92367-164">yes</span></span>       |
| [<span data-ttu-id="92367-165">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="92367-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="92367-166">sì</span><span class="sxs-lookup"><span data-stu-id="92367-166">yes</span></span>       |
| [<span data-ttu-id="92367-167">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92367-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="92367-168">no</span><span class="sxs-lookup"><span data-stu-id="92367-168">no</span></span>        |
| [<span data-ttu-id="92367-169">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92367-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="92367-170">no</span><span class="sxs-lookup"><span data-stu-id="92367-170">no</span></span>        |
| [<span data-ttu-id="92367-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92367-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="92367-172">no</span><span class="sxs-lookup"><span data-stu-id="92367-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="92367-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="92367-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92367-174">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92367-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





