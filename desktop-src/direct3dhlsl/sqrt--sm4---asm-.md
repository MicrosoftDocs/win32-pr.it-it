---
title: sqrt (SM4-ASM)
description: Radice quadrata in base al componente.
ms.assetid: B860D656-7F01-484F-909F-A5C9A61C52C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a12afaf5b2366dac15c953d509a6814b48a6b9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398246"
---
# <a name="sqrt-sm4---asm"></a><span data-ttu-id="a5ca1-103">sqrt (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a5ca1-103">sqrt (sm4 - asm)</span></span>

<span data-ttu-id="a5ca1-104">Radice quadrata in base al componente.</span><span class="sxs-lookup"><span data-stu-id="a5ca1-104">Component-wise square root.</span></span>



| <span data-ttu-id="a5ca1-105">sqrt \[ \_ Sab \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a5ca1-105">sqrt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="a5ca1-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a5ca1-106">Item</span></span>                                                            | <span data-ttu-id="a5ca1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5ca1-107">Description</span></span>                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a5ca1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a5ca1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a5ca1-109">\[nel \] risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a5ca1-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="a5ca1-110">*dest* = sqrt (*src0*)</span><span class="sxs-lookup"><span data-stu-id="a5ca1-110">*dest* = sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="a5ca1-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a5ca1-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a5ca1-112">\[nei \] componenti per i quali assumere la radice quadrata.</span><span class="sxs-lookup"><span data-stu-id="a5ca1-112">\[in\] The components for which to take the square root.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="a5ca1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5ca1-113">Remarks</span></span>

<span data-ttu-id="a5ca1-114">La precisione è 1 ULP rispetto.</span><span class="sxs-lookup"><span data-stu-id="a5ca1-114">Precision is 1 ulp.</span></span>

<span data-ttu-id="a5ca1-115">Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.</span><span class="sxs-lookup"><span data-stu-id="a5ca1-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="a5ca1-116">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="a5ca1-116">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
|          | <span data-ttu-id="a5ca1-117">**-INF**</span><span class="sxs-lookup"><span data-stu-id="a5ca1-117">**-inf**</span></span> | <span data-ttu-id="a5ca1-118">**-F**</span><span class="sxs-lookup"><span data-stu-id="a5ca1-118">**-F**</span></span> | <span data-ttu-id="a5ca1-119">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="a5ca1-119">**-denorm**</span></span> | <span data-ttu-id="a5ca1-120">**-0**</span><span class="sxs-lookup"><span data-stu-id="a5ca1-120">**-0**</span></span> | <span data-ttu-id="a5ca1-121">**+0**</span><span class="sxs-lookup"><span data-stu-id="a5ca1-121">**+0**</span></span> | <span data-ttu-id="a5ca1-122">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="a5ca1-122">**+denorm**</span></span> | <span data-ttu-id="a5ca1-123">**+ F**</span><span class="sxs-lookup"><span data-stu-id="a5ca1-123">**+F**</span></span> | <span data-ttu-id="a5ca1-124">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="a5ca1-124">**+inf**</span></span> | <span data-ttu-id="a5ca1-125">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a5ca1-125">**NaN**</span></span> |
| <span data-ttu-id="a5ca1-126">**dest**</span><span class="sxs-lookup"><span data-stu-id="a5ca1-126">**dest**</span></span> | <span data-ttu-id="a5ca1-127">NaN</span><span class="sxs-lookup"><span data-stu-id="a5ca1-127">NaN</span></span>      | <span data-ttu-id="a5ca1-128">NaN</span><span class="sxs-lookup"><span data-stu-id="a5ca1-128">NaN</span></span>    | <span data-ttu-id="a5ca1-129">-0</span><span class="sxs-lookup"><span data-stu-id="a5ca1-129">-0</span></span>          | <span data-ttu-id="a5ca1-130">-0</span><span class="sxs-lookup"><span data-stu-id="a5ca1-130">-0</span></span>     | <span data-ttu-id="a5ca1-131">+0</span><span class="sxs-lookup"><span data-stu-id="a5ca1-131">+0</span></span>     | <span data-ttu-id="a5ca1-132">+0</span><span class="sxs-lookup"><span data-stu-id="a5ca1-132">+0</span></span>          | <span data-ttu-id="a5ca1-133">+ F</span><span class="sxs-lookup"><span data-stu-id="a5ca1-133">+F</span></span>     | <span data-ttu-id="a5ca1-134">+inf</span><span class="sxs-lookup"><span data-stu-id="a5ca1-134">+inf</span></span>     | <span data-ttu-id="a5ca1-135">NaN</span><span class="sxs-lookup"><span data-stu-id="a5ca1-135">NaN</span></span>     |



 

<span data-ttu-id="a5ca1-136">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a5ca1-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a5ca1-137">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="a5ca1-137">Vertex Shader</span></span> | <span data-ttu-id="a5ca1-138">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="a5ca1-138">Geometry Shader</span></span> | <span data-ttu-id="a5ca1-139">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="a5ca1-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a5ca1-140">x</span><span class="sxs-lookup"><span data-stu-id="a5ca1-140">x</span></span>             | <span data-ttu-id="a5ca1-141">x</span><span class="sxs-lookup"><span data-stu-id="a5ca1-141">x</span></span>               | <span data-ttu-id="a5ca1-142">x</span><span class="sxs-lookup"><span data-stu-id="a5ca1-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a5ca1-143">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="a5ca1-143">Minimum Shader Model</span></span>

<span data-ttu-id="a5ca1-144">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="a5ca1-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a5ca1-145">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="a5ca1-145">Shader Model</span></span>                                              | <span data-ttu-id="a5ca1-146">Supportato</span><span class="sxs-lookup"><span data-stu-id="a5ca1-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a5ca1-147">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="a5ca1-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a5ca1-148">sì</span><span class="sxs-lookup"><span data-stu-id="a5ca1-148">yes</span></span>       |
| [<span data-ttu-id="a5ca1-149">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="a5ca1-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a5ca1-150">sì</span><span class="sxs-lookup"><span data-stu-id="a5ca1-150">yes</span></span>       |
| [<span data-ttu-id="a5ca1-151">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="a5ca1-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a5ca1-152">sì</span><span class="sxs-lookup"><span data-stu-id="a5ca1-152">yes</span></span>       |
| [<span data-ttu-id="a5ca1-153">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5ca1-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a5ca1-154">no</span><span class="sxs-lookup"><span data-stu-id="a5ca1-154">no</span></span>        |
| [<span data-ttu-id="a5ca1-155">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5ca1-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a5ca1-156">no</span><span class="sxs-lookup"><span data-stu-id="a5ca1-156">no</span></span>        |
| [<span data-ttu-id="a5ca1-157">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5ca1-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a5ca1-158">no</span><span class="sxs-lookup"><span data-stu-id="a5ca1-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a5ca1-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a5ca1-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5ca1-160">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5ca1-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





