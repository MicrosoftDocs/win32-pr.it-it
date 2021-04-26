---
title: min (sm4 - asm)
description: Minimo float per componente.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8791589b77edc66eeab4b48f10f4a9b16b5cb2d9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993898"
---
# <a name="min-sm4---asm"></a><span data-ttu-id="80235-103">min (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="80235-103">min (sm4 - asm)</span></span>

<span data-ttu-id="80235-104">Minimo float per componente.</span><span class="sxs-lookup"><span data-stu-id="80235-104">Component-wise float minimum.</span></span>



| <span data-ttu-id="80235-105">min \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="80235-105">min\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="80235-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="80235-106">Item</span></span>                                                            | <span data-ttu-id="80235-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80235-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80235-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="80235-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="80235-109">\[in \] Risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="80235-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="80235-110">*dest*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="80235-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="80235-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="80235-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="80235-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="80235-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="80235-113">\[in \] Componenti da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="80235-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                  |
| <span data-ttu-id="80235-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="80235-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="80235-115">\[in \] Componenti da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="80235-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="80235-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="80235-116">Remarks</span></span>

><span data-ttu-id="80235-117">= viene usato anziché > in modo che se min(x,y) = x allora max(x,y) = y.</span><span class="sxs-lookup"><span data-stu-id="80235-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="80235-118">NaN ha una gestione speciale.</span><span class="sxs-lookup"><span data-stu-id="80235-118">NaN has special handling.</span></span> <span data-ttu-id="80235-119">Se un operando di origine è NaN, viene restituito l'altro operando di origine e la scelta viene effettuata per componente.</span><span class="sxs-lookup"><span data-stu-id="80235-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="80235-120">Se entrambi sono NaN, viene restituita qualsiasi rappresentazione NaN.</span><span class="sxs-lookup"><span data-stu-id="80235-120">If both are NaN, any NaN representation is returned.</span></span> <span data-ttu-id="80235-121">Questo è conforme alle nuove regole IEEE 754R.</span><span class="sxs-lookup"><span data-stu-id="80235-121">This conforms to new IEEE 754R rules.</span></span>

<span data-ttu-id="80235-122">I denorm vengono scaricati, con il segno mantenuto, prima del confronto.</span><span class="sxs-lookup"><span data-stu-id="80235-122">Denorms are flushed, with the sign preserved, before comparison.</span></span> <span data-ttu-id="80235-123">Tuttavia, il risultato scritto *in dest* può essere scaricato o meno.</span><span class="sxs-lookup"><span data-stu-id="80235-123">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="80235-124">La tabella seguente mostra i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="80235-124">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="80235-125">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="80235-125">F means finite real number.</span></span>



| <span data-ttu-id="80235-126">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="80235-126">**src0 src1->**</span></span> | <span data-ttu-id="80235-127">**-inf**</span><span class="sxs-lookup"><span data-stu-id="80235-127">**-inf**</span></span> | <span data-ttu-id="80235-128">**F**</span><span class="sxs-lookup"><span data-stu-id="80235-128">**F**</span></span>        | <span data-ttu-id="80235-129">**+inf**</span><span class="sxs-lookup"><span data-stu-id="80235-129">**+inf**</span></span> | <span data-ttu-id="80235-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="80235-130">**NaN**</span></span> |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="80235-131">**-inf**</span><span class="sxs-lookup"><span data-stu-id="80235-131">**-inf**</span></span>           | <span data-ttu-id="80235-132">-inf</span><span class="sxs-lookup"><span data-stu-id="80235-132">-inf</span></span>     | <span data-ttu-id="80235-133">-inf</span><span class="sxs-lookup"><span data-stu-id="80235-133">-inf</span></span>         | <span data-ttu-id="80235-134">-inf</span><span class="sxs-lookup"><span data-stu-id="80235-134">-inf</span></span>     | <span data-ttu-id="80235-135">-inf</span><span class="sxs-lookup"><span data-stu-id="80235-135">-inf</span></span>    |
| <span data-ttu-id="80235-136">**F**</span><span class="sxs-lookup"><span data-stu-id="80235-136">**F**</span></span>              | <span data-ttu-id="80235-137">-inf</span><span class="sxs-lookup"><span data-stu-id="80235-137">-inf</span></span>     | <span data-ttu-id="80235-138">src0 o src1</span><span class="sxs-lookup"><span data-stu-id="80235-138">src0 or src1</span></span> | <span data-ttu-id="80235-139">src0</span><span class="sxs-lookup"><span data-stu-id="80235-139">src0</span></span>     | <span data-ttu-id="80235-140">src0</span><span class="sxs-lookup"><span data-stu-id="80235-140">src0</span></span>    |
| <span data-ttu-id="80235-141">**-inf**</span><span class="sxs-lookup"><span data-stu-id="80235-141">**-inf**</span></span>           | <span data-ttu-id="80235-142">-inf</span><span class="sxs-lookup"><span data-stu-id="80235-142">-inf</span></span>     | <span data-ttu-id="80235-143">src1</span><span class="sxs-lookup"><span data-stu-id="80235-143">src1</span></span>         | <span data-ttu-id="80235-144">+inf</span><span class="sxs-lookup"><span data-stu-id="80235-144">+inf</span></span>     | <span data-ttu-id="80235-145">+inf</span><span class="sxs-lookup"><span data-stu-id="80235-145">+inf</span></span>    |
| <span data-ttu-id="80235-146">**NaN**</span><span class="sxs-lookup"><span data-stu-id="80235-146">**NaN**</span></span>            | <span data-ttu-id="80235-147">-inf</span><span class="sxs-lookup"><span data-stu-id="80235-147">-inf</span></span>     | <span data-ttu-id="80235-148">src1</span><span class="sxs-lookup"><span data-stu-id="80235-148">src1</span></span>         | <span data-ttu-id="80235-149">+inf</span><span class="sxs-lookup"><span data-stu-id="80235-149">+inf</span></span>     | <span data-ttu-id="80235-150">NaN</span><span class="sxs-lookup"><span data-stu-id="80235-150">NaN</span></span>     |



 

<span data-ttu-id="80235-151">Questa istruzione si applica alle fasi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="80235-151">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="80235-152">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="80235-152">Vertex Shader</span></span> | <span data-ttu-id="80235-153">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="80235-153">Geometry Shader</span></span> | <span data-ttu-id="80235-154">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="80235-154">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="80235-155">x</span><span class="sxs-lookup"><span data-stu-id="80235-155">x</span></span>             | <span data-ttu-id="80235-156">x</span><span class="sxs-lookup"><span data-stu-id="80235-156">x</span></span>               | <span data-ttu-id="80235-157">x</span><span class="sxs-lookup"><span data-stu-id="80235-157">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="80235-158">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="80235-158">Minimum Shader Model</span></span>

<span data-ttu-id="80235-159">Questa funzione è supportata nei modelli di shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="80235-159">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="80235-160">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="80235-160">Shader Model</span></span>                                              | <span data-ttu-id="80235-161">Supportato</span><span class="sxs-lookup"><span data-stu-id="80235-161">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="80235-162">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="80235-162">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="80235-163">sì</span><span class="sxs-lookup"><span data-stu-id="80235-163">yes</span></span>       |
| [<span data-ttu-id="80235-164">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="80235-164">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="80235-165">sì</span><span class="sxs-lookup"><span data-stu-id="80235-165">yes</span></span>       |
| [<span data-ttu-id="80235-166">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="80235-166">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="80235-167">sì</span><span class="sxs-lookup"><span data-stu-id="80235-167">yes</span></span>       |
| [<span data-ttu-id="80235-168">Modello shader 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80235-168">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="80235-169">no</span><span class="sxs-lookup"><span data-stu-id="80235-169">no</span></span>        |
| [<span data-ttu-id="80235-170">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80235-170">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="80235-171">no</span><span class="sxs-lookup"><span data-stu-id="80235-171">no</span></span>        |
| [<span data-ttu-id="80235-172">Modello shader 1 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="80235-172">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="80235-173">no</span><span class="sxs-lookup"><span data-stu-id="80235-173">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="80235-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80235-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80235-175">Assembly del modello shader 4 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="80235-175">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





