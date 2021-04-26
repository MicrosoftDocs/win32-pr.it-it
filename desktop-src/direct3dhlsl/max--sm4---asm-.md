---
title: max (sm4 - asm)
description: Valore massimo float per componente.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64d88c581828f2563f6d5d8a6c57de6400f9bbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994728"
---
# <a name="max-sm4---asm"></a><span data-ttu-id="eb291-103">max (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="eb291-103">max (sm4 - asm)</span></span>

<span data-ttu-id="eb291-104">Valore massimo float per componente.</span><span class="sxs-lookup"><span data-stu-id="eb291-104">Component-wise float maximum.</span></span>



| <span data-ttu-id="eb291-105">max \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="eb291-105">max\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="eb291-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="eb291-106">Item</span></span>                                                            | <span data-ttu-id="eb291-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb291-107">Description</span></span>                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb291-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="eb291-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="eb291-109">\[in \] Risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="eb291-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="eb291-110">*dest*  =  *src0*  >=  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="eb291-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="eb291-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="eb291-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="eb291-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="eb291-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="eb291-113">\[in \] Componenti da confrontare con *src1*.</span><span class="sxs-lookup"><span data-stu-id="eb291-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                    |
| <span data-ttu-id="eb291-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="eb291-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="eb291-115">\[in \] Componenti da confrontare con *src0*.</span><span class="sxs-lookup"><span data-stu-id="eb291-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="eb291-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb291-116">Remarks</span></span>

><span data-ttu-id="eb291-117">= viene usato anziché > in modo che se min(x,y) = x allora max(x,y) = y.</span><span class="sxs-lookup"><span data-stu-id="eb291-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="eb291-118">NaN ha una gestione speciale.</span><span class="sxs-lookup"><span data-stu-id="eb291-118">NaN has special handling.</span></span> <span data-ttu-id="eb291-119">Se un operando di origine è NaN, viene restituito l'altro operando di origine e la scelta viene effettuata per componente.</span><span class="sxs-lookup"><span data-stu-id="eb291-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="eb291-120">Se entrambi sono NaN, viene restituita qualsiasi rappresentazione NaN.</span><span class="sxs-lookup"><span data-stu-id="eb291-120">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="eb291-121">I denorm vengono scaricati con il segno mantenuto prima del confronto.</span><span class="sxs-lookup"><span data-stu-id="eb291-121">Denorms are flushed with sign preserved before the comparison.</span></span> <span data-ttu-id="eb291-122">Tuttavia, il risultato scritto *in dest* può essere scaricato o meno.</span><span class="sxs-lookup"><span data-stu-id="eb291-122">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="eb291-123">Nella tabella seguente vengono illustrati i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichi alcun overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="eb291-123">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="eb291-124">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="eb291-124">F means finite real number.</span></span>



| <span data-ttu-id="eb291-125">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="eb291-125">**src0 src1->**</span></span> | <span data-ttu-id="eb291-126">**-inf**</span><span class="sxs-lookup"><span data-stu-id="eb291-126">**-inf**</span></span> | <span data-ttu-id="eb291-127">**F**</span><span class="sxs-lookup"><span data-stu-id="eb291-127">**F**</span></span>        | <span data-ttu-id="eb291-128">**+inf**</span><span class="sxs-lookup"><span data-stu-id="eb291-128">**+inf**</span></span> | <span data-ttu-id="eb291-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="eb291-129">**NaN**</span></span> |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="eb291-130">**-inf**</span><span class="sxs-lookup"><span data-stu-id="eb291-130">**-inf**</span></span>           | <span data-ttu-id="eb291-131">-inf</span><span class="sxs-lookup"><span data-stu-id="eb291-131">-inf</span></span>     | <span data-ttu-id="eb291-132">src1</span><span class="sxs-lookup"><span data-stu-id="eb291-132">src1</span></span>         | <span data-ttu-id="eb291-133">+inf</span><span class="sxs-lookup"><span data-stu-id="eb291-133">+inf</span></span>     | <span data-ttu-id="eb291-134">-inf</span><span class="sxs-lookup"><span data-stu-id="eb291-134">-inf</span></span>    |
| <span data-ttu-id="eb291-135">**F**</span><span class="sxs-lookup"><span data-stu-id="eb291-135">**F**</span></span>              | <span data-ttu-id="eb291-136">src0</span><span class="sxs-lookup"><span data-stu-id="eb291-136">src0</span></span>     | <span data-ttu-id="eb291-137">src0 o src1</span><span class="sxs-lookup"><span data-stu-id="eb291-137">src0 or src1</span></span> | <span data-ttu-id="eb291-138">+inf</span><span class="sxs-lookup"><span data-stu-id="eb291-138">+inf</span></span>     | <span data-ttu-id="eb291-139">src0</span><span class="sxs-lookup"><span data-stu-id="eb291-139">src0</span></span>    |
| <span data-ttu-id="eb291-140">**+inf**</span><span class="sxs-lookup"><span data-stu-id="eb291-140">**+inf**</span></span>           | <span data-ttu-id="eb291-141">+inf</span><span class="sxs-lookup"><span data-stu-id="eb291-141">+inf</span></span>     | <span data-ttu-id="eb291-142">+inf</span><span class="sxs-lookup"><span data-stu-id="eb291-142">+inf</span></span>         | <span data-ttu-id="eb291-143">+inf</span><span class="sxs-lookup"><span data-stu-id="eb291-143">+inf</span></span>     | <span data-ttu-id="eb291-144">+inf</span><span class="sxs-lookup"><span data-stu-id="eb291-144">+inf</span></span>    |
| <span data-ttu-id="eb291-145">**NaN**</span><span class="sxs-lookup"><span data-stu-id="eb291-145">**NaN**</span></span>            | <span data-ttu-id="eb291-146">-inf</span><span class="sxs-lookup"><span data-stu-id="eb291-146">-inf</span></span>     | <span data-ttu-id="eb291-147">src1</span><span class="sxs-lookup"><span data-stu-id="eb291-147">src1</span></span>         | <span data-ttu-id="eb291-148">+inf</span><span class="sxs-lookup"><span data-stu-id="eb291-148">+inf</span></span>     | <span data-ttu-id="eb291-149">NaN</span><span class="sxs-lookup"><span data-stu-id="eb291-149">NaN</span></span>     |



 

<span data-ttu-id="eb291-150">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="eb291-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="eb291-151">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="eb291-151">Vertex Shader</span></span> | <span data-ttu-id="eb291-152">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="eb291-152">Geometry Shader</span></span> | <span data-ttu-id="eb291-153">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="eb291-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="eb291-154">x</span><span class="sxs-lookup"><span data-stu-id="eb291-154">x</span></span>             | <span data-ttu-id="eb291-155">x</span><span class="sxs-lookup"><span data-stu-id="eb291-155">x</span></span>               | <span data-ttu-id="eb291-156">x</span><span class="sxs-lookup"><span data-stu-id="eb291-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eb291-157">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="eb291-157">Minimum Shader Model</span></span>

<span data-ttu-id="eb291-158">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="eb291-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="eb291-159">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="eb291-159">Shader Model</span></span>                                              | <span data-ttu-id="eb291-160">Supportato</span><span class="sxs-lookup"><span data-stu-id="eb291-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="eb291-161">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="eb291-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="eb291-162">sì</span><span class="sxs-lookup"><span data-stu-id="eb291-162">yes</span></span>       |
| [<span data-ttu-id="eb291-163">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="eb291-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="eb291-164">sì</span><span class="sxs-lookup"><span data-stu-id="eb291-164">yes</span></span>       |
| [<span data-ttu-id="eb291-165">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="eb291-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eb291-166">sì</span><span class="sxs-lookup"><span data-stu-id="eb291-166">yes</span></span>       |
| [<span data-ttu-id="eb291-167">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb291-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eb291-168">no</span><span class="sxs-lookup"><span data-stu-id="eb291-168">no</span></span>        |
| [<span data-ttu-id="eb291-169">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb291-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eb291-170">no</span><span class="sxs-lookup"><span data-stu-id="eb291-170">no</span></span>        |
| [<span data-ttu-id="eb291-171">Modello shader 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb291-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eb291-172">no</span><span class="sxs-lookup"><span data-stu-id="eb291-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="eb291-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb291-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb291-174">Shader Model 4 Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb291-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





