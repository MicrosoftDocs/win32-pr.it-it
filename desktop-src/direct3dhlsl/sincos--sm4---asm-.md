---
title: sincos (sm4 - asm)
description: Sin per componente (theta) e cos(theta) per theta in radianti.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c03118ff9a1fc2d958eaa6eb1a550a6dbf672a2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997018"
---
# <a name="sincos-sm4---asm"></a><span data-ttu-id="730e2-103">sincos (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="730e2-103">sincos (sm4 - asm)</span></span>

<span data-ttu-id="730e2-104">Sin per componente (theta) e cos(theta) per theta in radianti.</span><span class="sxs-lookup"><span data-stu-id="730e2-104">Component-wise sin(theta) and cos(theta) for theta in radians.</span></span>



| <span data-ttu-id="730e2-105">sincos \[ \_ sat \] destSIN \[ .mask \] , destCOS \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="730e2-105">sincos\[\_sat\] destSIN\[.mask\], destCOS\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------------|



 



| <span data-ttu-id="730e2-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="730e2-106">Item</span></span>                                                                                               | <span data-ttu-id="730e2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="730e2-107">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="730e2-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span><span class="sxs-lookup"><span data-stu-id="730e2-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span></span><br/> | <span data-ttu-id="730e2-109">\[in \] L'indirizzo di sin(*src0*), calcolato per componente.</span><span class="sxs-lookup"><span data-stu-id="730e2-109">\[in\] The address of sin(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="730e2-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span><span class="sxs-lookup"><span data-stu-id="730e2-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span></span><br/> | <span data-ttu-id="730e2-111">\[in \] Indirizzo di cos(*src0*), calcolato per componente.</span><span class="sxs-lookup"><span data-stu-id="730e2-111">\[in\] The address of cos(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="730e2-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="730e2-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                    | <span data-ttu-id="730e2-113">\[in \] Componenti per cui calcolare sin e cos.</span><span class="sxs-lookup"><span data-stu-id="730e2-113">\[in\] The components for which to compute sin and cos.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="730e2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="730e2-114">Remarks</span></span>

<span data-ttu-id="730e2-115">Se il risultato non è necessario, è possibile specificare *destSIN* e *destCOS* come NULL anziché specificare un registro.</span><span class="sxs-lookup"><span data-stu-id="730e2-115">If the result is not needed, you can specify *destSIN* and *destCOS* as NULL instead of specifying a register.</span></span>

<span data-ttu-id="730e2-116">I valori theta possono essere qualsiasi valore a virgola mobile IEEE a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="730e2-116">Theta values can be any IEEE 32-bit floating point values.</span></span>

<span data-ttu-id="730e2-117">L'errore assoluto massimo è 0,0008 nell'intervallo da -100 \* Pi a +100 \* Pi.</span><span class="sxs-lookup"><span data-stu-id="730e2-117">The maximum absolute error is 0.0008 in the interval from -100\*Pi to +100\*Pi.</span></span>

<span data-ttu-id="730e2-118">La tabella seguente mostra i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.</span><span class="sxs-lookup"><span data-stu-id="730e2-118">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="730e2-119">F indica un numero finito reale.</span><span class="sxs-lookup"><span data-stu-id="730e2-119">F means finite-real number.</span></span>



| <span data-ttu-id="730e2-120">**src**</span><span class="sxs-lookup"><span data-stu-id="730e2-120">**src**</span></span>     | <span data-ttu-id="730e2-121">**-inf**</span><span class="sxs-lookup"><span data-stu-id="730e2-121">**-inf**</span></span> | <span data-ttu-id="730e2-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="730e2-122">**-F**</span></span>       | <span data-ttu-id="730e2-123">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="730e2-123">**-denorm**</span></span> | <span data-ttu-id="730e2-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="730e2-124">**-0**</span></span> | <span data-ttu-id="730e2-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="730e2-125">**+0**</span></span> | <span data-ttu-id="730e2-126">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="730e2-126">**+denorm**</span></span> | <span data-ttu-id="730e2-127">**+F**</span><span class="sxs-lookup"><span data-stu-id="730e2-127">**+F**</span></span>       | <span data-ttu-id="730e2-128">**+inf**</span><span class="sxs-lookup"><span data-stu-id="730e2-128">**+inf**</span></span> | <span data-ttu-id="730e2-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="730e2-129">**NaN**</span></span> |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| <span data-ttu-id="730e2-130">**destSIN**</span><span class="sxs-lookup"><span data-stu-id="730e2-130">**destSIN**</span></span> | <span data-ttu-id="730e2-131">NaN</span><span class="sxs-lookup"><span data-stu-id="730e2-131">NaN</span></span>      | <span data-ttu-id="730e2-132">\[Da -1 a +1\]</span><span class="sxs-lookup"><span data-stu-id="730e2-132">\[-1 to +1\]</span></span> | <span data-ttu-id="730e2-133">-0</span><span class="sxs-lookup"><span data-stu-id="730e2-133">-0</span></span>          | <span data-ttu-id="730e2-134">-0</span><span class="sxs-lookup"><span data-stu-id="730e2-134">-0</span></span>     | <span data-ttu-id="730e2-135">+0</span><span class="sxs-lookup"><span data-stu-id="730e2-135">+0</span></span>     | <span data-ttu-id="730e2-136">+0</span><span class="sxs-lookup"><span data-stu-id="730e2-136">+0</span></span>          | <span data-ttu-id="730e2-137">\[Da -1 a +1\]</span><span class="sxs-lookup"><span data-stu-id="730e2-137">\[-1 to +1\]</span></span> | <span data-ttu-id="730e2-138">NaN</span><span class="sxs-lookup"><span data-stu-id="730e2-138">NaN</span></span>      | <span data-ttu-id="730e2-139">NaN</span><span class="sxs-lookup"><span data-stu-id="730e2-139">NaN</span></span>     |
| <span data-ttu-id="730e2-140">**destCOS**</span><span class="sxs-lookup"><span data-stu-id="730e2-140">**destCOS**</span></span> | <span data-ttu-id="730e2-141">NaN</span><span class="sxs-lookup"><span data-stu-id="730e2-141">NaN</span></span>      | <span data-ttu-id="730e2-142">\[Da -1 a +1\]</span><span class="sxs-lookup"><span data-stu-id="730e2-142">\[-1 to +1\]</span></span> | <span data-ttu-id="730e2-143">+1</span><span class="sxs-lookup"><span data-stu-id="730e2-143">+1</span></span>          | <span data-ttu-id="730e2-144">+1</span><span class="sxs-lookup"><span data-stu-id="730e2-144">+1</span></span>     | <span data-ttu-id="730e2-145">+1</span><span class="sxs-lookup"><span data-stu-id="730e2-145">+1</span></span>     | <span data-ttu-id="730e2-146">+1</span><span class="sxs-lookup"><span data-stu-id="730e2-146">+1</span></span>          | <span data-ttu-id="730e2-147">\[Da -1 a +1\]</span><span class="sxs-lookup"><span data-stu-id="730e2-147">\[-1 to +1\]</span></span> | <span data-ttu-id="730e2-148">NaN</span><span class="sxs-lookup"><span data-stu-id="730e2-148">NaN</span></span>      | <span data-ttu-id="730e2-149">NaN</span><span class="sxs-lookup"><span data-stu-id="730e2-149">NaN</span></span>     |



 

<span data-ttu-id="730e2-150">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="730e2-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="730e2-151">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="730e2-151">Vertex Shader</span></span> | <span data-ttu-id="730e2-152">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="730e2-152">Geometry Shader</span></span> | <span data-ttu-id="730e2-153">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="730e2-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="730e2-154">x</span><span class="sxs-lookup"><span data-stu-id="730e2-154">x</span></span>             | <span data-ttu-id="730e2-155">x</span><span class="sxs-lookup"><span data-stu-id="730e2-155">x</span></span>               | <span data-ttu-id="730e2-156">x</span><span class="sxs-lookup"><span data-stu-id="730e2-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="730e2-157">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="730e2-157">Minimum Shader Model</span></span>

<span data-ttu-id="730e2-158">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="730e2-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="730e2-159">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="730e2-159">Shader Model</span></span>                                              | <span data-ttu-id="730e2-160">Supportato</span><span class="sxs-lookup"><span data-stu-id="730e2-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="730e2-161">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="730e2-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="730e2-162">sì</span><span class="sxs-lookup"><span data-stu-id="730e2-162">yes</span></span>       |
| [<span data-ttu-id="730e2-163">Modello shader 4.1</span><span class="sxs-lookup"><span data-stu-id="730e2-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="730e2-164">sì</span><span class="sxs-lookup"><span data-stu-id="730e2-164">yes</span></span>       |
| [<span data-ttu-id="730e2-165">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="730e2-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="730e2-166">sì</span><span class="sxs-lookup"><span data-stu-id="730e2-166">yes</span></span>       |
| [<span data-ttu-id="730e2-167">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="730e2-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="730e2-168">no</span><span class="sxs-lookup"><span data-stu-id="730e2-168">no</span></span>        |
| [<span data-ttu-id="730e2-169">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="730e2-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="730e2-170">no</span><span class="sxs-lookup"><span data-stu-id="730e2-170">no</span></span>        |
| [<span data-ttu-id="730e2-171">Modello shader 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="730e2-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="730e2-172">no</span><span class="sxs-lookup"><span data-stu-id="730e2-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="730e2-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="730e2-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="730e2-174">Shader Model 4 Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="730e2-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





