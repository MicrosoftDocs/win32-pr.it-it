---
title: SinCos (SM4-ASM)
description: Sin (componente-Wise) e cos (THETA) per Theta in radianti.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2dd8fc3b011758f071cdcd273e34eb8a7f6421f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992992"
---
# <a name="sincos-sm4---asm"></a><span data-ttu-id="67db0-103">SinCos (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="67db0-103">sincos (sm4 - asm)</span></span>

<span data-ttu-id="67db0-104">Sin (componente-Wise) e cos (THETA) per Theta in radianti.</span><span class="sxs-lookup"><span data-stu-id="67db0-104">Component-wise sin(theta) and cos(theta) for theta in radians.</span></span>



| <span data-ttu-id="67db0-105">SinCos \[ \_ Sat \] destSIN \[ . mask \] , destCOS \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="67db0-105">sincos\[\_sat\] destSIN\[.mask\], destCOS\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------------|



 



| <span data-ttu-id="67db0-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="67db0-106">Item</span></span>                                                                                               | <span data-ttu-id="67db0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67db0-107">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="67db0-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span><span class="sxs-lookup"><span data-stu-id="67db0-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span></span><br/> | <span data-ttu-id="67db0-109">\[nell' \] indirizzo di sin (*src0*) calcolato per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="67db0-109">\[in\] The address of sin(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="67db0-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span><span class="sxs-lookup"><span data-stu-id="67db0-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span></span><br/> | <span data-ttu-id="67db0-111">\[nell' \] indirizzo di cos (*src0*), calcolato per componente.</span><span class="sxs-lookup"><span data-stu-id="67db0-111">\[in\] The address of cos(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="67db0-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="67db0-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                    | <span data-ttu-id="67db0-113">\[nei \] componenti per i quali calcolare sin e cos.</span><span class="sxs-lookup"><span data-stu-id="67db0-113">\[in\] The components for which to compute sin and cos.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="67db0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="67db0-114">Remarks</span></span>

<span data-ttu-id="67db0-115">Se il risultato non è necessario, è possibile specificare *destSIN* e *destCOS* come null anziché specificare un registro.</span><span class="sxs-lookup"><span data-stu-id="67db0-115">If the result is not needed, you can specify *destSIN* and *destCOS* as NULL instead of specifying a register.</span></span>

<span data-ttu-id="67db0-116">I valori theta possono essere qualsiasi valore a virgola mobile IEEE a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="67db0-116">Theta values can be any IEEE 32-bit floating point values.</span></span>

<span data-ttu-id="67db0-117">L'errore assoluto massimo è 0,0008 nell'intervallo da-100 \* pi a + 100 \* pi.</span><span class="sxs-lookup"><span data-stu-id="67db0-117">The maximum absolute error is 0.0008 in the interval from -100\*Pi to +100\*Pi.</span></span>

<span data-ttu-id="67db0-118">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.</span><span class="sxs-lookup"><span data-stu-id="67db0-118">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="67db0-119">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="67db0-119">F means finite-real number.</span></span>



|             |          |              |             |        |        |             |              |          |         |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| <span data-ttu-id="67db0-120">**src**</span><span class="sxs-lookup"><span data-stu-id="67db0-120">**src**</span></span>     | <span data-ttu-id="67db0-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="67db0-121">**-inf**</span></span> | <span data-ttu-id="67db0-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="67db0-122">**-F**</span></span>       | <span data-ttu-id="67db0-123">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="67db0-123">**-denorm**</span></span> | <span data-ttu-id="67db0-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="67db0-124">**-0**</span></span> | <span data-ttu-id="67db0-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="67db0-125">**+0**</span></span> | <span data-ttu-id="67db0-126">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="67db0-126">**+denorm**</span></span> | <span data-ttu-id="67db0-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="67db0-127">**+F**</span></span>       | <span data-ttu-id="67db0-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="67db0-128">**+inf**</span></span> | <span data-ttu-id="67db0-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="67db0-129">**NaN**</span></span> |
| <span data-ttu-id="67db0-130">**destSIN**</span><span class="sxs-lookup"><span data-stu-id="67db0-130">**destSIN**</span></span> | <span data-ttu-id="67db0-131">NaN</span><span class="sxs-lookup"><span data-stu-id="67db0-131">NaN</span></span>      | <span data-ttu-id="67db0-132">\[da-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="67db0-132">\[-1 to +1\]</span></span> | <span data-ttu-id="67db0-133">-0</span><span class="sxs-lookup"><span data-stu-id="67db0-133">-0</span></span>          | <span data-ttu-id="67db0-134">-0</span><span class="sxs-lookup"><span data-stu-id="67db0-134">-0</span></span>     | <span data-ttu-id="67db0-135">+0</span><span class="sxs-lookup"><span data-stu-id="67db0-135">+0</span></span>     | <span data-ttu-id="67db0-136">+0</span><span class="sxs-lookup"><span data-stu-id="67db0-136">+0</span></span>          | <span data-ttu-id="67db0-137">\[da-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="67db0-137">\[-1 to +1\]</span></span> | <span data-ttu-id="67db0-138">NaN</span><span class="sxs-lookup"><span data-stu-id="67db0-138">NaN</span></span>      | <span data-ttu-id="67db0-139">NaN</span><span class="sxs-lookup"><span data-stu-id="67db0-139">NaN</span></span>     |
| <span data-ttu-id="67db0-140">**destCOS**</span><span class="sxs-lookup"><span data-stu-id="67db0-140">**destCOS**</span></span> | <span data-ttu-id="67db0-141">NaN</span><span class="sxs-lookup"><span data-stu-id="67db0-141">NaN</span></span>      | <span data-ttu-id="67db0-142">\[da-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="67db0-142">\[-1 to +1\]</span></span> | <span data-ttu-id="67db0-143">+1</span><span class="sxs-lookup"><span data-stu-id="67db0-143">+1</span></span>          | <span data-ttu-id="67db0-144">+1</span><span class="sxs-lookup"><span data-stu-id="67db0-144">+1</span></span>     | <span data-ttu-id="67db0-145">+1</span><span class="sxs-lookup"><span data-stu-id="67db0-145">+1</span></span>     | <span data-ttu-id="67db0-146">+1</span><span class="sxs-lookup"><span data-stu-id="67db0-146">+1</span></span>          | <span data-ttu-id="67db0-147">\[da-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="67db0-147">\[-1 to +1\]</span></span> | <span data-ttu-id="67db0-148">NaN</span><span class="sxs-lookup"><span data-stu-id="67db0-148">NaN</span></span>      | <span data-ttu-id="67db0-149">NaN</span><span class="sxs-lookup"><span data-stu-id="67db0-149">NaN</span></span>     |



 

<span data-ttu-id="67db0-150">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="67db0-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="67db0-151">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="67db0-151">Vertex Shader</span></span> | <span data-ttu-id="67db0-152">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="67db0-152">Geometry Shader</span></span> | <span data-ttu-id="67db0-153">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="67db0-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="67db0-154">x</span><span class="sxs-lookup"><span data-stu-id="67db0-154">x</span></span>             | <span data-ttu-id="67db0-155">x</span><span class="sxs-lookup"><span data-stu-id="67db0-155">x</span></span>               | <span data-ttu-id="67db0-156">x</span><span class="sxs-lookup"><span data-stu-id="67db0-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="67db0-157">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="67db0-157">Minimum Shader Model</span></span>

<span data-ttu-id="67db0-158">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="67db0-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="67db0-159">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="67db0-159">Shader Model</span></span>                                              | <span data-ttu-id="67db0-160">Supportato</span><span class="sxs-lookup"><span data-stu-id="67db0-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="67db0-161">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="67db0-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="67db0-162">sì</span><span class="sxs-lookup"><span data-stu-id="67db0-162">yes</span></span>       |
| [<span data-ttu-id="67db0-163">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="67db0-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="67db0-164">sì</span><span class="sxs-lookup"><span data-stu-id="67db0-164">yes</span></span>       |
| [<span data-ttu-id="67db0-165">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="67db0-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="67db0-166">sì</span><span class="sxs-lookup"><span data-stu-id="67db0-166">yes</span></span>       |
| [<span data-ttu-id="67db0-167">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67db0-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="67db0-168">no</span><span class="sxs-lookup"><span data-stu-id="67db0-168">no</span></span>        |
| [<span data-ttu-id="67db0-169">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67db0-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="67db0-170">no</span><span class="sxs-lookup"><span data-stu-id="67db0-170">no</span></span>        |
| [<span data-ttu-id="67db0-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67db0-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="67db0-172">no</span><span class="sxs-lookup"><span data-stu-id="67db0-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="67db0-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67db0-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67db0-174">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67db0-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





